住处新装了光猫，几百兆的光纤上网。按理，这么贵的价格上网应该神速，然鹅令人匪夷所思的是，从微博到微信好友圈，经常会出现页面加载卡顿、部分图片显示不出来等诡异情况……

笔者的排查之路，就这么开始了

## 问题出在哪儿？

1. 通过Chrome浏览器的开发者模式排查后得知：那些浏览器无法得到有效内容的请求，集中在几个CDN的域名。以微博为例，在同一个页面发出的请求中，`wx1.sinaimg.cn`下的图片可正常显示，但到了`wx4.sinaimg.cn`便显示红色的“fail”。
2. 进一步通过`nslookup`, `dig`, `ping`等命令排查，发现问题主要集中在如下2个原因：

    a) DNS服务器解析超时或解析错误；

    光猫在PPPOE时会采用ISP自带的DNS，同时从路由再到上网终端均打开了DHCP自动获取DNS，这就导致了终端实质上在采用ISP自带的DNS，而且偏偏……你懂的，ISP的DNS普遍很挫；


    b) DNS服务器虽然能返回正常结果，但是却ping不通……
    
    浏览器试图通过v6的主机IP地址向主机发起请求，但是ISP并未完全打开IPv6，导致访问失败。

## 做了哪些操作？

1. 既然终端误以为“存在畅通的IPv6链路”，那就在路由器和光猫上**禁用IPv6**，*断了终端的这个妄想*。这样即使DNS同时返回v6和v4的结果，浏览器和APP都只会用v4的地址访问，避免了混淆。

1. ISP给提供的DNS就扔了。虽然ISP的DNS服务器平均访问延迟短，但毕竟不稳定、且经常掉链子，甚至还有DNS污染问题……因此，从路由器到光猫都把DNS改成**手动**设置的自测好用的**公共DNS**。

1. 除了将DNS的来源设置成公共DNS以外，利用路由器或终端自带的DNS缓存功能也很重要。这是由于公共DNS虽然真香，但毕竟平均访问延时时间偏长，因此必须在本地设法加一个recursive的缓存。

    a) 其实缓存的设置也有讲究：路由器会自带DNS缓存，怀疑是 BIND 或 Dnsmasq （可能路由自带的固件的DNS程序更简单低级），导致无法自行定制
    
    b) 为了实现比较强大的功能，采取在PC终端上自建DNS服务器的方法。为了在轻量级服务器和功能性上的折衷，**推荐使用 [CoreDNS](https://github.com/coredns/coredns)**。下载到本地后，记得**设置`Corefile`**。笔者`Corefile`长成下面这样子：
        
        .:53 {
            forward . 223.5.5.5:53
            cache 600 
        }
    意思就是在本地开一个DNS服务器，并且所有的结果从阿里云的DNS上读取，读取完了在本地缓存600秒（也就是10分钟）。读者可以根据自身的网络情况自行设置，本文就不再展开CoreDNS的详细设置了。
    
    c) 把CoreDNS设置成**开机启动**,  创建一个快捷方式，目标Target为：`C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe -ExecutionPolicy Bypass -NoLogo -NonInteractive -NoProfile -WindowStyle Hidden -Command "D:\your\path\coredns.exe -conf D:\your\path\Corefile"`，Start in这一栏要成`"D:\your\path\coredns.exe"`
    
    快捷方式一般是创建在在Windows的全部用户的启动组`"%ALLUSERSPROFILE%\Microsoft\Windows\Start Menu\Programs\StartUp"`下
    
    当然，你也可以创建在当然用户的启动组，即`"%USERPROFILE%\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Startup\"`下  
    
    至于如何在Linux下通过把启动项加入`init.d`中的操作，比较简单且通用 ，本文就不再赘述了。
    
    d) 最后，务必记得**把本地网络连接的DNS设置成手动，IP为`127.0.0.1`**。

## 效果怎么样？

真香。

其实，很多时候网速慢，并不是硬件瓶颈或ISP的带宽过低导致，而是优化不够。

最后还是要吐槽一下：
1. 都9012年了，路由器的官方固件的DNS依然很烂……
2. 都9012年了，Windows依然没有好用的自带的DNS……
3. ……
