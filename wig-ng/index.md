---
Title: wig-ng
Homepage: https://github.com/6e726d/wig-ng
Repository: https://gitlab.com/kalilinux/packages/wig-ng
Architectures: all
Version: 0.1-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### wig-ng
 
  This package contains WIG (Wi-Fi Information Gathering), a utility for Wi-Fi
  device fingerprinting.
  Supported protocols and standards:
    * Apple Wireless Direct Link (AWDL)
    * Cisco Client Extension (CCX)
    * HP Printers Custom Information Element
    * Wi-Fi Direct (P2P)
    * Wi-Fi Protected Setup (WPS)
   
  This tool doesn't perform channel hopping, use tools such as chopping or
  airodump-ng.
 
 **Installed size:** `334 KB`  
 **How to install:** `sudo apt install wig-ng`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-impacket
 * python3-pcapy
 * python3-setproctitle
 {{< /spoiler >}}
 
 ##### wig-ng
 
 
 ```
 root@kali:~# wig-ng -h
 usage: wig-ng.py [-h] [-v] [-c count] [-a]
                  (-i network interface | -r pcap file | -R pcap directory)
 
 options:
   -h, --help            show this help message and exit
   -v, --verbose         Output verbosity (incremental).
   -c count, --concurrent count
                         Number of PCAP capture files to process
                         simultaneously.
   -a, --active          Some modules can perform frame injection, this is
                         define by setting the active mode.
   -i network interface, --interface network interface
                         IEEE 802.11 network interface on monitor mode.
   -r pcap file          PCAP capture file with IEEE 802.11 network traffic.
   -R pcap directory     Directory with PCAP capture files.
 ```
 
 - - -
 
 ##### wig-ng.py
 
 
 ```
 root@kali:~# wig-ng.py -h
 usage: wig-ng.py [-h] [-v] [-c count] [-a]
                  (-i network interface | -r pcap file | -R pcap directory)
 
 options:
   -h, --help            show this help message and exit
   -v, --verbose         Output verbosity (incremental).
   -c count, --concurrent count
                         Number of PCAP capture files to process
                         simultaneously.
   -a, --active          Some modules can perform frame injection, this is
                         define by setting the active mode.
   -i network interface, --interface network interface
                         IEEE 802.11 network interface on monitor mode.
   -r pcap file          PCAP capture file with IEEE 802.11 network traffic.
   -R pcap directory     Directory with PCAP capture files.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
