---
Title: redsocks
Homepage: http://darkk.net.ru/redsocks/
Repository: https://salsa.debian.org/debian/redsocks
Architectures: any
Version: 0.5-2
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-web 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### redsocks
 
  Redsocks is a daemon running on the local system, that will transparently
  tunnel any TCP connection via a remote SOCKS4, SOCKS5 or HTTP proxy server. It
  uses the system firewall's redirection facility to intercept TCP connections,
  thus the redirection is system-wide, with fine-grained control, and does
  not depend on LD_PRELOAD libraries.
   
  Redsocks supports tunneling TCP connections and UDP packets. It has
  authentication support for both, SOCKS and HTTP proxies.
   
  Also included is a small DNS server returning answers with the "truncated" flag
  set for any UDP query, forcing the resolver to use TCP.
 
 **Installed size:** `157 KB`  
 **How to install:** `sudo apt install redsocks`  
 
 {{< spoiler "Dependencies:" >}}
 * adduser
 * libc6 
 * libevent-core-2.1-7 
 * lsb-base 
 {{< /spoiler >}}
 
 ##### redsocks
 
 Redirect any TCP connection to a SOCKS or HTTP proxy
 
 ```
 root@kali:~# redsocks -h
 Usage: redsocks [-?hvt] [-c config] [-p pidfile]
   -h, -?       this message
   -v           print version
   -t           test config syntax
   -p           write pid to pidfile
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
