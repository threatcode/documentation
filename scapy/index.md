---
Title: scapy
Homepage: https://scapy.net/
Repository: https://salsa.debian.org/pkg-security-team/scapy
Architectures: all
Version: 2.5.0+dfsg-2
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-linux-nethunter kali-tools-802-11 kali-tools-information-gathering kali-tools-passwords kali-tools-voip kali-tools-vulnerability kali-tools-wireless 
Icon: images/scapy-logo.svg
PackagesInfo: |
 ### python3-scapy
 
  Scapy is a powerful interactive packet manipulation tool, packet
  generator, network scanner, network discovery, packet sniffer, etc. It
  can for the moment replace hping, 85% of nmap, arpspoof, arp-sk, arping,
  tcpdump, tethereal, p0f, ....
   
  In scapy you define a set of packets, then it sends them, receives
  answers, matches requests with answers and returns a list of packet couples
  (request, answer) and a list of unmatched packets. This has the big advantage
  over tools like nmap or hping that an answer is not reduced to
  (open/closed/filtered), but is the whole packet.
   
  This package contains the Python 3 version of the library and scapy executable.
 
 **Installed size:** `6.45 MB`  
 **How to install:** `sudo apt install python3-scapy`  
 
 {{< spoiler "Dependencies:" >}}
 * netbase
 * python3
 {{< /spoiler >}}
 
 ##### scapy
 
 Interactive packet manipulation tool
 
 ```
 root@kali:~# scapy -h
 Usage: scapy.py [-s sessionfile] [-c new_startup_file] [-p new_prestart_file] [-C] [-P] [-H]
 Args:
 	-H: header-less start
 	-C: do not read startup file
 	-P: do not read pre-startup file
 
 ```
 
 - - -
 
 ##### scapy3
 
 Interactive packet manipulation tool
 
 ```
 root@kali:~# scapy3 -h
 Usage: scapy.py [-s sessionfile] [-c new_startup_file] [-p new_prestart_file] [-C] [-P] [-H]
 Args:
 	-H: header-less start
 	-C: do not read startup file
 	-P: do not read pre-startup file
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
