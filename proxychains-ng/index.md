---
Title: proxychains-ng
Homepage: https://github.com/rofl0r/proxychains-ng
Repository: https://salsa.debian.org/debian/proxychains-ng
Architectures: any
Version: 4.16-3
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-post-exploitation kali-tools-web 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### libproxychains4
 
  Proxychains is a UNIX program, that hooks network-related libc functions
  in dynamically linked programs via a preloaded DLL (dlsym(), LD_PRELOAD)
  and redirects the connections through SOCKS4a/5 or HTTP proxies.
  It supports TCP only (no UDP/ICMP etc).
   
  This project, proxychains-ng, is the continuation of the unmaintained
  proxychains project (known as proxychains package in Debian).
   
  This package provides the runtime shared library used by proxychains-ng
  program.
 
 **Installed size:** `66 KB`  
 **How to install:** `sudo apt install libproxychains4`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 
 - - -
 
 ### proxychains4
 
  Proxychains is a UNIX program, that hooks network-related libc functions
  in dynamically linked programs via a preloaded DLL (dlsym(), LD_PRELOAD)
  and redirects the connections through SOCKS4a/5 or HTTP proxies.
  It supports TCP only (no UDP/ICMP etc).
   
  This project, proxychains-ng, is the continuation of the unmaintained
  proxychains project (known as proxychains package in Debian).
 
 **Installed size:** `66 KB`  
 **How to install:** `sudo apt install proxychains4`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libproxychains4 
 {{< /spoiler >}}
 
 ##### proxychains4
 
 Redirect connections through proxy servers
 
 ```
 root@kali:~# proxychains4 --help
 
 Usage:	proxychains4 -q -f config_file program_name [arguments]
 	-q makes proxychains quiet - this overrides the config setting
 	-f allows one to manually specify a configfile to use
 	for example : proxychains telnet somehost.com
 More help in README file
 
 ```
 
 - - -
 
 ##### proxychains4-daemon
 
 
 ```
 root@kali:~# proxychains4-daemon -h
 Proxychains-NG remote dns daemon
 --------------------------------
 usage: proxychains4-daemon -i listenip -p port -r remotesubnet
 all arguments are optional.
 by default listenip is 127.0.0.1, port 1053 and remotesubnet 224.
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
