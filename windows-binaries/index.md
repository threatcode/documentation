---
Title: windows-binaries
Homepage: https://www.kali.org
Repository: https://gitlab.com/kalilinux/packages/windows-binaries
Architectures: all
Version: 0.6.10
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-windows-resources 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### windows-binaries
 
  A collection of Windows executables for use on penetration tests.
 
 **Installed size:** `5.53 MB`  
 **How to install:** `sudo apt install windows-binaries`  
 
 {{< spoiler "Dependencies:" >}}
 * kali-defaults 
 {{< /spoiler >}}
 
 ##### windows-binaries
 
 
 ```
 root@kali:~# windows-binaries -h
 
 > windows-binaries ~ Various pentesting Windows binaries
 
 /usr/share/windows-resources/binaries
 |-- enumplus
 |-- exe2bat.exe
 |-- fgdump
 |-- fport
 |-- klogger.exe
 |-- mbenum
 |-- nbtenum
 |-- nc.exe
 |-- plink.exe
 |-- radmin.exe
 |-- vncviewer.exe
 |-- wget.exe
 `-- whoami.exe
 ```
 
 - - -
 
 ##### windows-resources
 
 
 ```
 root@kali:~# windows-resources -h
 /usr/share/windows-resources
 |-- binaries
 |-- dbd
 |-- heartleech
 |-- hyperion
 |-- mimikatz
 |-- ncat
 |-- nishang -> ../nishang
 |-- ollydbg
 |-- powercat
 |-- powershell-empire -> ../powershell-empire
 |-- powersploit
 |-- sbd
 |-- secure-socket-funneling
 |-- shellter
 |-- sqldict
 |-- tftpd32
 |-- wce
 `-- windows-privesc-check
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
