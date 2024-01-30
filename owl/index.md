---
Title: owl
Homepage: https://owlink.org/
Repository: https://gitlab.com/kalilinux/packages/owl
Architectures: any
Version: 0~git20220130-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### owl
 
  This package contains an open implementation of the Apple Wireless Direct Link
  (AWDL) ad hoc protocol for Linux and macOS written in C and part of the Open
  Wireless Link project.
   
  OWL runs in user space and makes use of Linux’s Netlink API for Wi-Fi specific
  operations such as channel switching and to integrate itself in the Linux
  networking stack by providing a virtual network interface such that existing
  IPv6-capable programs can use AWDL without modification.
 
 **Installed size:** `85 KB`  
 **How to install:** `sudo apt install owl`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libev4 
 * libnl-3-200 
 * libnl-genl-3-200 
 * libnl-route-3-200 
 * libpcap0.8 
 * radiotap-library
 {{< /spoiler >}}
 
 ##### owl
 
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
