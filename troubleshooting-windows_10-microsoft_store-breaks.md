# Troubleshooting case: How to fix broken Microsoft Store in Windows 10


## TL;DR 
If you are suffering from broken Microsoft Store in Windows 10 N, installing [Media Feature Pack for N](https://www.microsoft.com/en-us/software-download/mediafeaturepack) will be the solution. 

## Case Details
### Problem
This has been driving me nuts. It took me an entire day to figure out.
I'm unable to turn on Microsoft Store -- Sometimes it just shows up the splash screen, some other times there are no response at all!

There are plenty of replies postedn on [Microsoft Answers](https://answers.microsoft.com/en-us/windows/forum/windows_10-windows_store/how-to-fix-ms-windows-storepurgecaches-app-didnt/30d1fce9-733d-4b27-bf14-e88ce7e77fbf)

Regardless of whether a solution applies to fixing an user's problem or not, there is one thing for sure: Microsoft Windows 10 is buggy and crappy.
The first time this problem appeard was back in 2015, now it's 2019. Everytime there is a problem, there will be a solution -- provided by frustrated and furious users like you and me.

### Attempts:
Here are what I tried but all of them let me down:

#### 0. Toggle off "background apps" (it helps, but still does not work, so you may want to check this)
If Microsoft Store is running as a background app, you won't be able to see anything.
Otherwise, as a foreground app, you may be able to see a splash screen.
So, whenever you can't even see the splash screen of Microsoft Store, make sure you run this!
* Right-mouse-click "Microsoft Store" in start menu, then "App Settings"
* Toggle off "background apps" switch

#### 1. Run Windows' built-in troubleshooter (does not work)
* Type "troubleshoot Settings" in the Start Menu.
* Click on "Troubleshoot" on the left panel, "Windows Store Apps" on the right, then "Run the Troubleshooter"
* Follow the instruction
* In particular, ensuring UAC is turned on does not solve the problem

#### 2. Powershell script (does not work)
* Turn on Powershell with Administrative Privileges
* Run something like: 
    ```
    $manifest = (Get-AppxPackage Microsoft.WindowsStore).InstallLocation + '\AppxManifest.xml' ; Add-AppxPackage -DisableDevelopmentMode -Register $manifest 
    ```
    Note: there may be other types of scripts to run. I am just showing a specific example for illustration purpose. Of course feel free to try whatever you want
* Reboot the computer

#### 3. Reinstall Microsoft Store (does not work)
* I used a 3rd-party tool (e.g. CCleaner) to perform a forced uninstallation of Microsoft Store
* Re-installed Microsoft Store using the Powershell script above, but didn't work.

#### 4. Run "wsreset" (does not work)
* Run "wsreset.exe" utility
* And, an error message box "ms-windows-store:PurgeCaches The application didn’t start." poped up, indicating this attemp failed.

#### 5. Grant permissions to the folder (does not work)
* Take ownership of the folder "C:\Program Files\WindowsApps"
* Grant yourself and "All Application Packages" the "full control" priviledges

### Final solution:
Finally, it dawned upon me that I use castrated Windows N instead of the original version, I installed [Media Feature Pack for N](https://www.microsoft.com/en-us/software-download/mediafeaturepack). Now I can see all the flashy app tiles! 
