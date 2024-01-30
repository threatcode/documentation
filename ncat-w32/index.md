---
Title: ncat-w32
Homepage: https://nmap.org/ncat/
Repository: https://gitlab.com/kalilinux/packages/ncat-w32
Architectures: all
Version: 5.59beta1-1kali3
Metapackages: kali-linux-everything kali-linux-large kali-tools-windows-resources 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### ncat-w32
 
  Ncat is a feature-packed networking utility which reads and writes data across
  networks from the command line. Ncat was written for the Nmap Project as a
  much-improved reimplementation of the venerable Netcat. It uses both TCP and
  UDP for communication and is designed to be a reliable back-end tool to
  instantly provide network connectivity to other applications and users. Ncat
  will not only work with IPv4 and IPv6 but provides the user with a virtually
  limitless number of potential uses.
   
  Among Ncat’s vast number of features there is the ability to chain Ncats
  together, redirect both TCP and UDP ports to other sites, SSL support, and
  proxy connections via SOCKS4 or HTTP (CONNECT method) proxies (with optional
  proxy authentication as well). Some general principles apply to most
  applications and thus give you the capability of instantly adding networking
  support to software that would normally never support it.
 
 **Installed size:** `1.60 MB`  
 **How to install:** `sudo apt install ncat-w32`  
 
 {{< spoiler "Dependencies:" >}}
 * kali-defaults
 {{< /spoiler >}}
 
 ##### ncat-w32
 
 
 ```
 root@kali:~# ncat-w32 -h
 
 > ncat-w32 ~ Netcat for the 21st century
 
 /usr/share/windows-resources/ncat/
 |-- README
 `-- ncat.exe
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
