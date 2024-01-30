---
Title: portspoof
Homepage: https://github.com/drk1wi/portspoof
Repository: https://gitlab.com/kalilinux/packages/portspoof
Architectures: any
Version: 1.3+git20230902.399f60e-0kali2
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### portspoof
 
  This package contains a service to enhance OS security through a set of following
  techniques:
     * All 65535 TCP ports are always open
       Instead of informing an attacker that a particular port is in a CLOSED or
       FILTERED state Portspoof will return SYN+ACK for every port connection
       attempt/
     * Every open TCP port emulates a service
       Portspoof has a huge database of dynamic service signatures, that will be
       used to generate fake banners and fool scanners.
   
  This tool requires configuration before use.
 
 **Installed size:** `1.06 MB`  
 **How to install:** `sudo apt install portspoof`  
 
 {{< spoiler "Dependencies:" >}}
 * iptables
 * libc6 
 * libgcc-s1 
 * libstdc++6 
 {{< /spoiler >}}
 
 ##### portspoof
 
 
 ```
 root@kali:~# portspoof --help
 Try ` portspoof -h' for more information.
 
 ```
 
 - - -
 
 ##### portspoof-start
 
 
 ```
 root@kali:~# portspoof-start -h
 Before running portspoof, you need to adapt the configuration
 Read /usr/share/doc/portspoof/README.Debian
 ```
 
 - - -
 
 ##### portspoof-stop
 
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
