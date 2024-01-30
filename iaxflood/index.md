---
Title: iaxflood
Homepage: http://www.hackingexposedvoip.com/sec_tools.html
Repository: https://gitlab.com/kalilinux/packages/iaxflood
Architectures: any
Version: 0.1-1kali3
Metapackages: kali-linux-everything kali-linux-large kali-tools-voip kali-tools-vulnerability 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### iaxflood
 
  A UDP Inter-Asterisk_eXchange (i.e. IAX) packet was captured
  from an IAX channel between two Asterisk IP PBX's. The
  content of that packet is the source of the payload for the
  attack embodied by this tool. While the IAX protocol header
  might not match the Asterisk PBX you'll attack with this
  tool, it may require more processing on the part of the PBX
  than a simple udpflood without any payload that even
  resembles an IAX payload.
 
 **Installed size:** `25 KB`  
 **How to install:** `sudo apt install iaxflood`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### iaxflood
 
 
 ```
 root@kali:~# iaxflood -h
 usage: iaxflood sourcename destinationname numpackets
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## iaxflood Usage Example

Flood the VoIP server from the source (`192.168.1.202`) to the destination (`192.168.1.1`) by sending 500 packets (`500`):

```
root@kali:~# iaxflood 192.168.1.202 192.168.1.1 500
Will flood port 4569 from port 4569 500 times
We have IP_HDRINCL
```
