Setting up Windows (here, I mean Windows 10) can be frustrating and time consuming. In this cookbook I will list all the trivialities I encountered when using Windows

## Windows Console-style Software Package Management
Windows users envy Mac's homebrew and Linux's apt and yum. Here are a bunch of sulutions that Windows users can install software

### Chocolatey
* Link: https://chocolatey.org/

#### Boxstarter (a virtual machine-like tool)
* Link: https://boxstarter.org/
> Boxstarter leverages Chocolatey packages to automate the installation of software and create repeatable, scripted Windows environments. Chocolatey makes installing software very easy with no user intervention. Boxstarter enhances Chocolatey's functionality and provides an environment that is optimized for installing a complete environment on a fresh OS install, as well as some other specific scenarios.

### Scoop
* Link: https://scoop.sh/
* Github Repo: https://github.com/lukesampson/scoop

Scoop 在 __用户目录__ 下创建了一个名为 scoop 的文件夹，并默认将软件安装到这个相对独立且隔离（isolated and independent）的环境下，从而保证环境的统一和路径不被污染。
scoop 通过 shim 来软链接一些应用，这样的设计让应用之间不会互相干扰。

__前提__ 
1.PowerShell >= 3
2.正常、稳定地访问 GitHub

## Changing Terminal Fonts
### Solution 1: Default code page 
__TL'DR:__ If you're a Win 10 user like me, just use [CMDer](http://cmder.net/) as an alternative of Windows' default Command Prompt, as it is more configurable.

### Solution 2: 

#### Add fonts
Default fonts Cmd.exe allows six fonts: Conslolas, Courier New, Lucida Console, Lucida Sans Typewriter, MS Gothic, NSimSun. All are ugly and wide
This only works if your code page is ANSI (1252). 
If your code page is not ANSI, change your Windows system locale to English with correspoinding region (e.g. English - United States).

* Bring up Registry Editor (run "regedit")
* Find the folder HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Console\TrueTypeFont
* Right click -> New -> String Value
* For the "Value Name", assign one more "0" than the last one (e.g. if you already have "00" in place, then just put in "000").
* For the "Value Data", put in the font name (e.g. "Droid Sans Pro")

#### Font size
If you stick with the default old MSDOS Raster Font, don't forget to switch the "Raster" font to "8 x 12" pixels.
!["8 x 12"](http://www.pagestart.com/images/386_Win7_CommandPrompt-03.jpg)


#### Window Size:
Just change the ‘Width’ and ‘Height’ from the default "80 x 25" to a larger value , any value that makes you happy. For me, I set it to "120"

#### Screen Buffer Size:
a) The ‘Width’ allows you to configure how many characters are displayed in a single line. I recommend setting it the same value as the ‘Width’ from ‘Window Size’
b) The ‘Height’ value determines the number of lines that are stored in memory. Set it to a large number such as "5000" (especially useful when the console is churning out piles of exception stack ^_|) 

#### Enhance the contrast
The default  RGB (Red, Green, Blue) values for the foreground fonts are 192. We can increase these values to a larger one like 230.
Also, we can make the background darker by decreasing its RGB values.



