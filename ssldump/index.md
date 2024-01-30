---
Title: ssldump
Homepage: https://github.com/adulau/ssldump
Repository: https://salsa.debian.org/pkg-security-team/ssldump
Architectures: any
Version: 1.5-1
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-information-gathering kali-tools-web 
Icon: images/ssldump-logo.svg
PackagesInfo: |
 ### ssldump
 
  This program will dump the traffic on a network and analyze it for
  SSLv3/TLS network traffic, typically used to secure TCP connections.
  When it identifies this traffic, it decodes the results.  When
  provided with the appropriate keying material, it will also decrypt
  the connections and display the application data traffic.
   
  ssldump is based on tcpdump, a network monitoring and data acquisition
  tool.
 
 **Installed size:** `180 KB`  
 **How to install:** `sudo apt install ssldump`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libjson-c5 
 * libnet1 
 * libpcap0.8 
 * libssl3 
 {{< /spoiler >}}
 
 ##### ssldump
 
 Dump SSL traffic on a network
 
 ```
 root@kali:~# ssldump --help
 ssldump: invalid option -- '-'
 Usage: ssldump [-r dumpfile] [-i interface] [-l sslkeylogfile] [-w outpcapfile]
                [-k keyfile] [-p password] [-vtaTnsAxVNde]
                [filter]
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
