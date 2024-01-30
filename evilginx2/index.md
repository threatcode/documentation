---
Title: evilginx2
Homepage: https://github.com/kgretzky/evilginx2
Repository: https://gitlab.com/kalilinux/packages/evilginx2
Architectures: any
Version: 3.2.0+ds1-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### evilginx2
 
  This package contains a man-in-the-middle attack framework used for phishing
  login credentials along with session cookies, which in turn allows to bypass
  2-factor authentication protection.
   
  This tool is a successor to Evilginx, released in 2017, which used a custom
  version of nginx HTTP server to provide man-in-the-middle functionality to act
  as a proxy between a browser and phished website. Present version is fully
  written in GO as a standalone application, which implements its own HTTP and
  DNS server, making it extremely easy to set up and use.
 
 **Installed size:** `9.29 MB`  
 **How to install:** `sudo apt install evilginx2`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### evilginx2
 
 
 ```
 root@kali:~# evilginx2 -h
 Usage of evilginx2:
   -c string
     	Configuration directory path
   -debug
     	Enable debug output
   -developer
     	Enable developer mode (generates self-signed certificates for all hostnames)
   -p string
     	Phishlets directory path
   -t string
     	HTML redirector pages directory path
   -v	Show version
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
