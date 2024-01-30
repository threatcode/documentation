---
Title: ferret-sidejack
Homepage: https://github.com/robertdavidgraham/ferret
Repository: https://gitlab.com/kalilinux/packages/ferret-sidejack
Architectures: any
Version: 3.0.1-1kali10
Metapackages: kali-linux-everything kali-linux-large kali-tools-sniffing-spoofing kali-tools-web 
Icon: images/ferret-sidejack-logo.svg
PackagesInfo: |
 ### ferret-sidejack
 
  This tool extracts interesting bits from network traffic.
  One use is to feed the "hamster" tool. Another use is to
  dump the output intoa text file, then use indexers and grep
  programs to analyze it.
 
 **Installed size:** `379 KB`  
 **How to install:** `sudo apt install ferret-sidejack`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libgcc-s1 
 * libpcap-dev
 * libstdc++6 
 {{< /spoiler >}}
 
 ##### ferret-sidejack
 
 
 ```
 root@kali:~# ferret-sidejack -h
 -- FERRET 3.0.1 - 2007-2012 (c) Errata Security
 -- build = Feb 10 2023 19:15:01 (64-bits)
 -- libpcap version 1.10.4 (with TPACKET_V3)
 options:
  -i <adapter>    Sniffs the wire(less) attached to that network adapter. 
                  Must have libpcap or winpcap installed to work.
  -r <files>      Read files in off-line mode. Can use wildcards, such as 
                  using "ferret -r *.pcap". Doesn't need libpcap to work.
  -c <file>       Reads in more advanced parameters from a file.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
