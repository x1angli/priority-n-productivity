# Recap：今天课程的总结

## 1. 安装python与准备环境

### 1.1 安装Anaconda全家桶，并且相应地设置
Anaconda全家桶集成了Python语言，numpy+scipy+matplotlib等最常用的数学包，Jupyter交互式执行器，Spyder和VSCode的下载器，
请按照 [这篇cookbook](cookbook-setting_up-anaconda-w-tuna.md) https://github.com/x1angli/priority-n-productivity/blob/master/cookbook-setting_up-anaconda-w-tuna.md里的

#### 1.1.1 从TUNA上下载和安装Anaconda全家桶
https://mirrors.tuna.tsinghua.edu.cn/anaconda/archive/

#### 1.1.2 设置conda的channels
照上面的cookbook里的做就行了
需要将main+free+pro这三个，或者将main+free这两个conda channel指向TUNA的镜像
如果需要，也可以把pytorch或者更多的conda channel指向TUNA的镜像
（至于为什么这么锁碎，为什么不是三并一的Anaconda，可以参照 [这里](https://github.com/tuna/issues/issues/307#issuecomment-374014053) 以及 [这里](https://github.com/tuna/issues/issues/417#issuecomment-434544876) ） 

#### 1.1.3 设置Jupyter的起始目录
照cookbook里的做就行了，做的时候需要注意路径需要改成自己想要的

### 1.2 更新和设置python
在python命令行下，以管理员权限运行下列命令

     python -m ensurepip --default-pip
     python -m pip install --upgrade pip
     pip install pip -U
     pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple

### 1.3 其他
对于那些在windows下经常安装不了的包（比如tensorflow, openCV），建议从个人开发者那儿下载已经编译成二进制的包
Unofficial Windows Binaries for Python Extension Packages
https://www.lfd.uci.edu/~gohlke/pythonlibs/


## 2. 常见教程

### 2.1 Python教程
* https://www.w3schools.com/python/
    * 看到“File Handling”就可以了
* https://docs.python.org/3/tutorial/
    * 注意：这是官方的python教程，特别详细（rong2 chang2），建议有的放矢

### 2.2 numpy教程 与 数据科学
* https://docs.scipy.org/doc/numpy-1.15.0/user/quickstart.html
* https://www.tutorialspoint.com/numpy/numpy_arithmetic_operations.htm
* https://jakevdp.github.io/PythonDataScienceHandbook/index.html
    * 这个是我认为不错的，里面介绍了IPython的使用，NumPy和Pandas作为数据和统计的基础包，Matplotlib画图，还有最重要的机器学习，所以建议有兴趣的同学精读

### 2.4 rLabbe的Karlman Filters教程
* https://github.com/rlabbe/Kalman-and-Bayesian-Filters-in-Python
    * 注意：上面这个教程比较详细和综合，建议有的放矢
* 图解卡尔曼滤波（英文）  http://www.bzarg.com/p/how-a-kalman-filter-works-in-pictures
    * 图解卡尔曼滤波（中文翻译）  https://blog.csdn.net/u010720661/article/details/63253509
