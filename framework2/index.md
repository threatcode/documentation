---
Title: framework2
Homepage: https://www.metasploit.com
Repository: https://gitlab.com/kalilinux/packages/framework2
Architectures: all
Version: 2.0-1kali3
Metapackages: kali-linux-everything kali-linux-large 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### framework2
 
  Version 2 of the Metasploit Framework.
  No longer updated but still useful, particularly for shellcode.
 
 **Installed size:** `7.82 MB`  
 **How to install:** `sudo apt install framework2`  
 
 {{< spoiler "Dependencies:" >}}
 * kali-defaults
 * perl
 {{< /spoiler >}}
 
 ##### framework2
 
 
 ```
 root@kali:~# framework2 -h
 
 > framework2 ~ Metasploit Framework 2
 
 /usr/share/framework2
 |-- data
 |-- docs
 |-- encoders
 |-- exploits
 |-- extras
 |-- lib
 |-- msfcli
 |-- msfconsole
 |-- msfdldebug
 |-- msfelfscan
 |-- msfencode
 |-- msflogdump
 |-- msfpayload
 |-- msfpescan
 |-- msfupdate
 |-- msfweb
 |-- nops
 |-- payloads
 |-- sdk
 |-- src
 |-- t
 `-- tools
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
