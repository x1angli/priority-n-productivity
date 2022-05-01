# Broken Microsoft Store in Windows 10

## Problem Desc
unable to turn on Microsoft Store -- either just stuck at the splash screen, or totally dead app. 

Analysis: Media Feature Pack is one of the dependencies of MS Store, but such dependency has been neglected. Especially, if you are using Windows 10 N (the one without Media Features), you may run into this issue.

## Solution
just install [Media Feature Pack for N](https://www.microsoft.com/en-us/software-download/mediafeaturepack). and you'll be all set.

### None of following approaches worked (at least for me)
1. Toggling off "background apps" switch: right-mouse-click "Micro Store" in start menu -> "App Settings" -> turning off the "background apps" switch
2. Running Windows' built-in troubleshooter
3. Re-regsitering AppxManifest thru PowerShell
4. Running "wsreset.exe"

### Related discussion
Plenty of answers were posted on [Microsoft Answers](https://answers.microsoft.com/en-us/windows/forum/windows_10-windows_store/how-to-fix-ms-windows-storepurgecaches-app-didnt/30d1fce9-733d-4b27-bf14-e88ce7e77fbf)

# Slow harddrive (SSD) 

## Solution 
Turn off BitLocker

## What I tried as well
1. Attempting to switch from "ATA" mode to "ACHI" mode -- unfortunately, such option in the BIOS settings is not applicable to begin with.
3. Updating BIOS / firmware
4. Shutting down the built-in Windows Defender / Microsoft Security Essentials
5. Turning off firewall
6. Uninstalling  bloatware 

# Error 0x800f0954 upon installing xxx (e.g. dotNET Framework 3.5)

## Solution
Disabling custom WSUS (Windows Server Update Services) server

If `reg query HKLM\Software\Policies\Microsoft\Windows\WindowsUpdate\AU /v UseWUServer` returns `1`, then it indicates WSUS is customized. Then just turn it off

# Unable to run any Virtual Machine 
* "Virtual Machine could not be started because the hypervisor is not running" when running Hyper-V
* "Please enable the Virtual Machine Platform Windows feature and ensure virtualization is enabled in the BIOS." when running WSL

## Solution
1. run `bcdedit` in command line, 
2. if you found `hypervisorlaunchtype` is off
3. run `bcdedit /set hypervisorlaunchtype auto` and restart computer


