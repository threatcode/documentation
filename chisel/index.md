---
Title: chisel
Homepage: https://github.com/jpillora/chisel
Repository: https://gitlab.com/kalilinux/packages/chisel
Architectures: any
Version: 1.9.1-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### chisel
 
  This package contains a fast TCP/UDP tunnel, transported over HTTP, secured
  via SSH. Single executable including both client and server.  Chisel is mainly
  useful for passing through firewalls, though it can also be used to provide a
  secure endpoint into your network.
 
 **Installed size:** `8.31 MB`  
 **How to install:** `sudo apt install chisel`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### chisel
 
 
 ```
 root@kali:~# chisel -h
 
   Usage: chisel [command] [--help]
 
   Version: 1.9.1-0kali1 (go1.21.3)
 
   Commands:
     server - runs chisel in server mode
     client - runs chisel in client mode
 
   Read more:
     https://github.com/jpillora/chisel
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
