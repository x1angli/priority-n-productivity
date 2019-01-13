
### TL;DR 
If you are suffering from the random slowlyness/halts/stutter/freezing harddrive under Windows, the Windows's __BitLocker__ may be the culprit. 

### Problem
This has been driving me nuts. I bought a brand new Lenovo Thinkpad Carbon X1, with top-notch SSD for this price range. When I opened the box while it's delivered, I indeed expected "wow" 

Unfortunately, I found there are noticable and bothering random slowlyness/halts/stutter/freezing. Here is the configuration: 
* Windows 10 Pro
* [Samsung MZVLB512HAJQ](https://www.samsung.com/semiconductor/ssd/client-ssd/MZVLB512HAJQ/) PM981 (PCI Express Gen3 x4) SSD harddrive
* Intel i7 CPU

I googled the solutions. There are tons of webpages with replies saying, “me too”....


### Attempts:

Here is a list of what I tried but failed:
1. Switching from "ATA" mode to "ACHI" mode, as some webpages suggests, is not applicable -- because there is no such option in the BIOS settings to begin with. 
2. Updating BIOS / firmware does not help, either.
3. Shutting down the built-in Windows Defender / Microsoft Security Essentials does NOT solve the problem.
4. Also, shutting down firewall and uninstalling unnecessary bloatware do NOT solve the problem either.


### Solution:
Finally, I found all the harddrive partitions are encrypted by __BitLocker__, and I've heard BitLocker-encrypted systems are slower in Win 10 than in Win 7 [source](https://mspoweruser.com/heres-bitlocker-slower-windows-10-windows-7/). So, I used BitDefender to decrypt all the drives except the system drive (C:), and I re-installed a fresh copy of windows on C:. It's solved.
