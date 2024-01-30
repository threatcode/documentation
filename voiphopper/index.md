---
Title: voiphopper
Homepage: https://sourceforge.net/projects/voiphopper
Repository: https://gitlab.com/kalilinux/packages/voiphopper
Architectures: any
Version: 2.04-1kali5
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-voip kali-tools-vulnerability 
Icon: images/voiphopper-logo.svg
PackagesInfo: |
 ### voiphopper
 
  VoIP Hopper is a GPLv3 licensed security tool, written in C
  that rapidly runs a VLAN Hop security test.  VoIP Hopper is
  a VoIP infrastructure security testing tool but also a tool
  that can be used to test the (in)security of VLANs.
 
 **Installed size:** `126 KB`  
 **How to install:** `sudo apt install voiphopper`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libpcap0.8 
 {{< /spoiler >}}
 
 ##### voiphopper
 
 
 ```
 root@kali:~# voiphopper -h
 VoIP Hopper Extended Usage:
 
 Miscellaneous Options:
 	-l (list available interfaces for CDP sniffing, then exit)
 	Example:  voiphopper -l
 	-m (Spoof the MAC Address, then exit)
 	Example:  voiphopper -i eth0 -m 00:07:0E:EA:50:86
 	-d (Delete the VLAN Interface, then exit)
 	Example:  voiphopper -d eth0.200
 	-V (Print the VoIP Hopper version, then exit)
 	Example:  voiphopper -V
 
 MAC Address Spoofing Options (used with -a, -v, or -c options):
 	-m (Spoof the MAC Address of existing interface, and new Interface)
 	-D -m (Spoof the MAC Address of only new Voice Interface)
 	Example:  voiphopper -i eth0 -m 00:07:0E:EA:50:86
 	Example:  voiphopper -i eth0 -D -m 00:07:0E:EA:50:86
 
 CDP Sniff Mode (-c 0)
 	Example:  voiphopper -i eth0 -c 0
 
 CDP Spoof Mode (-c 1):
 	-E <string> (Device ID)
 	-P <string> (Port ID)
 	-C <string> (Capabilities)
 	-L <string> (Platform)
 	-S <string> (Software)
 	-U <string> (Duplex)
 
 Example Usage for SIP Firmware Phone:
 voiphopper -i eth0 -c 1 -E 'SIP00070EEA5086' -P 'Port 1' -C Host -L 'Cisco IP Phone 7940' -S 'P003-08-8-00' -U 1
 
 Example Usage for SCCP Firmware Phone:
 voiphopper -i eth0 -c 1 -E 'SEP0070EEA5086' -P 'Port 1' -C Host -L 'Cisco IP Phone 7940' -S 'P00308000700' -U 1
 
 Example Usage for Phone with MAC Spoofing:
 voiphopper -i eth0 -m 00:07:0E:EA:50:86 -c 1 -E 'SEP00070EEA5086' -P 'Port 1' -C Host -L 'Cisco IP Phone 7940' -S 'P003-08-8-00' -U 1
 
 Avaya DHCP Option Mode (-a):
 	Example:  voiphopper -i eth0 -a
 	Example:  voiphopper -i eth0 -a -m 00:07:0E:EA:50:86
 
 VLAN Hop Mode (-v VLAN ID):
 	Example:  voiphopper -i eth0 -v 200
 	Example:  voiphopper -i eth0 -v 200 -D -m 00:07:0E:EA:50:86
 
 Alcatel VLAN Discovery (-t 0|1|2):
 	Example:  voiphopper -i eth0 -t 0
 	Example:  voiphopper -i eth0 -t 1
 	Example:  voiphopper -i eth0 -t 0 -m 00:80:9f:ad:42:42
 	Example:  voiphopper -i eth0 -t 1 -m 00:80:9f:ad:42:42
 	Example:  voiphopper -i eth0 -t 2 -v 800
 	Example:  voiphopper -i eth0 -t 2 -v 800 -m 00:80:9f:ad:42:42
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## voiphopper Usage Example

```
root@kali:~# voiphopper -i eth0 -z
VoIP Hopper assessment mode ~ Select 'q' to quit and 'h' for help menu.
Main Sniffer:  capturing packets on eth0
a
Analyzing ARP packets on default interface: eth0
New host #1 learned on eth0: (MAC): 78:ca:39:fe:0b:4c   (IP): 192.168.1.229
New host #2 learned on eth0: (MAC): 60:6b:bd:5a:b6:6c   (IP): 192.168.1.213
New host #3 learned on eth0: (MAC): 40:6c:8f:1b:cb:90   (IP): 192.168.1.232
a
Disabling analysis of ARP packets on default interface:  eth0
```
