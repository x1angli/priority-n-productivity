Setting up Windows (here, I mean Windows 10) can be frustrating and time consuming. In this cookbook I will list all the trivialities I encountered when using Windows

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



