---
Title: koadic
Homepage: https://github.com/zerosum0x0/koadic
Repository: https://gitlab.com/kalilinux/packages/koadic
Architectures: all
Version: 0~git20210412-0kali4
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### koadic
 
  This package contains Koadic, or COM Command & Control. It is a Windows
  post-exploitation rootkit similar to other penetration testing tools such as
  Meterpreter and Powershell Empire. The major difference is that Koadic does
  most of its operations using Windows Script Host (a.k.a. JScript/VBScript),
  with compatibility in the core to support a default installation of Windows
  2000 with no service packs (and potentially even versions of NT4) all the way
  through Windows 10.
   
  It is possible to serve payloads completely in memory from stage 0 to beyond,
  as well as use cryptographically secure communications over SSL and TLS
  (depending on what the victim OS has enabled).
 
 **Installed size:** `7.51 MB`  
 **How to install:** `sudo apt install koadic`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-impacket
 * python3-pyasn1
 * python3-pypykatz
 * python3-rjsmin
 * python3-tabulate
 {{< /spoiler >}}
 
 ##### koadic
 
 
 ```
 root@kali:~# koadic -h
 usage: koadic [-h] [--autorun AUTORUN] [-o] [--restore RESTORE]
 
 options:
   -h, --help         show this help message and exit
   --autorun AUTORUN  a file containing commands to autorun at startup
   -o                 it is tuesday my dudes
   --restore RESTORE  a koadic restore json file
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
