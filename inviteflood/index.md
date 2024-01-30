---
Title: inviteflood
Homepage: http://www.hackingvoip.com/sec_tools.html
Repository: https://gitlab.com/kalilinux/packages/inviteflood
Architectures: any
Version: 2.0-1kali2
Metapackages: kali-linux-everything kali-linux-large kali-tools-voip kali-tools-vulnerability 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### inviteflood
 
  A tool to perform SIP/SDP INVITE message flooding over
  UDP/IP. It was tested on a Linux Red Hat Fedora Core 4
  platform (Pentium IV, 2.5 GHz), but it is expected this
  tool will successfully build and execute on a variety of
  Linux distributions.
 
 **Installed size:** `33 KB`  
 **How to install:** `sudo apt install inviteflood`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libnet1 
 {{< /spoiler >}}
 
 ##### inviteflood
 
 
 ```
 root@kali:~# inviteflood -h
 
 inviteflood - Version 2.0
               June 09, 2006
  Usage:
  Mandatory -
 	interface (e.g. eth0)
 	target user (e.g. "" or john.doe or 5000 or "1+210-555-1212")
 	target domain (e.g. enterprise.com or an IPv4 address)
 	IPv4 addr of flood target (ddd.ddd.ddd.ddd)
 	flood stage (i.e. number of packets)
  Optional -
 	-a flood tool "From:" alias (e.g. jane.doe)
 	-i IPv4 source IP address [default is IP address of interface]
 	-S srcPort  (0 - 65535) [default is well-known discard port 9]
 	-D destPort (0 - 65535) [default is well-known SIP port 5060]
 	-l lineString line used by SNOM [default is blank]
 	-s sleep time btwn INVITE msgs (usec)
 	-h help - print this usage
 	-v verbose output mode
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## inviteflood Usage Example

Using the eth0 interface (`eth0`) and the provided user (`5000`), flood the target domain (`example.local`) and flood target (`192.168.1.5`) using 100 packets (`100`):

```
root@kali:~# inviteflood eth0 5000 example.local 192.168.1.5 100

inviteflood - Version 2.0
              June 09, 2006

source IPv4 addr:port   = 192.168.1.202:9
dest   IPv4 addr:port   = 192.168.1.5:5060
targeted UA             = 5000@192.168.1.1

Flooding destination with 100 packets
sent: 100
```
