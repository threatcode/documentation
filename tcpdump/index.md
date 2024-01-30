---
Title: tcpdump
Homepage: https://www.tcpdump.org/
Repository: https://salsa.debian.org/rfrancoise/tcpdump
Architectures: any
Version: 4.99.4-3
Metapackages: kali-linux-core kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-linux-nethunter kali-linux-wsl kali-tools-forensics kali-tools-information-gathering kali-tools-respond kali-tools-sniffing-spoofing 
Icon: images/tcpdump-logo.svg
PackagesInfo: |
 ### tcpdump
 
  This program allows you to dump the traffic on a network. tcpdump
  is able to examine IPv4, ICMPv4, IPv6, ICMPv6, UDP, TCP, SNMP, AFS
  BGP, RIP, PIM, DVMRP, IGMP, SMB, OSPF, NFS and many other packet
  types.
   
  It can be used to print out the headers of packets on a network
  interface, filter packets that match a certain expression. You can
  use this tool to track down network problems, to detect attacks
  or to monitor network activities.
 
 **Installed size:** `1.30 MB`  
 **How to install:** `sudo apt install tcpdump`  
 
 {{< spoiler "Dependencies:" >}}
 * adduser
 * libc6 
 * libpcap0.8 
 * libssl3 
 {{< /spoiler >}}
 
 ##### tcpdump
 
 Dump traffic on a network
 
 ```
 root@kali:~# tcpdump -h
 tcpdump version 4.99.4
 libpcap version 1.10.4 (with TPACKET_V3)
 OpenSSL 3.0.11 19 Sep 2023
 Usage: tcpdump [-AbdDefhHIJKlLnNOpqStuUvxX#] [ -B size ] [ -c count ] [--count]
 		[ -C file_size ] [ -E algo:secret ] [ -F file ] [ -G seconds ]
 		[ -i interface ] [ --immediate-mode ] [ -j tstamptype ]
 		[ -M secret ] [ --number ] [ --print ] [ -Q in|out|inout ]
 		[ -r file ] [ -s snaplen ] [ -T type ] [ --version ]
 		[ -V file ] [ -w file ] [ -W filecount ] [ -y datalinktype ]
 		[ --time-stamp-precision precision ] [ --micro ] [ --nano ]
 		[ -z postrotate-command ] [ -Z user ] [ expression ]
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
