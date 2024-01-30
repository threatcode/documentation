---
Title: windows-privesc-check
Homepage: https://pentestmonkey.net/tools/windows-privesc-check
Repository: https://gitlab.com/kalilinux/packages/windows-privesc-check
Architectures: all
Version: 2.0.0+svn197-0kali5
Metapackages: kali-linux-everything kali-tools-windows-resources 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### windows-privesc-check
 
  Windows-privesc-check is standalone executable that runs on Windows systems
  (tested on XP, Windows 7 only so far). It tries to find misconfigurations that
  could allow local unprivileged users to escalate privileges to other users or
  to access local apps (e.g. databases).
   
  It is written in python and converted to an executable using pyinstaller so it
  can be easily uploaded and run (as opposed to unzipping python + other
  dependencies). It can run either as a normal user or as Administrator
  (obviously it does a better job when running as Administrator because it can
  read more files).
 
 **Installed size:** `7.95 MB`  
 **How to install:** `sudo apt install windows-privesc-check`  
 
 {{< spoiler "Dependencies:" >}}
 * kali-defaults 
 {{< /spoiler >}}
 
 ##### windows-privesc-check
 
 
 ```
 root@kali:~# windows-privesc-check -h
 
 > windows-privesc-check ~ Windows privilege escalation checking tool
 
 /usr/share/windows-resources/windows-privesc-check
 `-- windows-privesc-check2.exe
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
