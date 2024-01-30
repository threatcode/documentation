---
Title: intrace
Homepage: https://github.com/robertswiecki/intrace
Repository: https://gitlab.com/kalilinux/packages/intrace
Architectures: any
Version: 1.6-0kali2
Metapackages: kali-linux-everything kali-linux-large kali-tools-information-gathering 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### intrace
 
  InTrace is a traceroute-like application that enables users to enumerate IP
  hops exploiting existing TCP connections, both initiated from local network
  (local system) or from remote hosts. It could be useful for network
  reconnaissance and firewall bypassing.
 
 **Installed size:** `52 KB`  
 **How to install:** `sudo apt install intrace`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### intrace
 
 
 ```
 root@kali:~# intrace -h
 InTrace, version 1.6 (C)2007-2016 Robert Swiecki <robert@swiecki.net>
 2023/12/01 09:37:45.45931 <INFO> Usage: intrace <-h hostname> [-p <port>] [-d <debuglevel>] [-s <payloadsize>] [-4] [-6]
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## intrace Usage Example

Run a trace to the target host (`-h www.example.com`) using port 80 (`-p 80`) with a packet size of 4 bytes (`-s 4`):

```
root@kali:~# intrace -h www.example.com -p 80 -s 4
InTrace 1.5 -- R: 93.184.216.119/80 (80) L: 192.168.1.130/51654
Payload Size: 4 bytes, Seq: 0x0d6dbb02, Ack: 0x8605bff0
Status: Packets sent #8

  #  [src addr]         [icmp src addr]    [pkt type]
 1.  [192.168.1.1    ]  [93.184.216.119 ]  [ICMP_TIMXCEED]
 2.  [192.168.0.1    ]  [93.184.216.119 ]  [ICMP_TIMXCEED]
 3.  [  ---          ]  [  ---          ]  [NO REPLY]
 4.  [64.59.184.185  ]  [93.184.216.119 ]  [ICMP_TIMXCEED]
 5.  [66.163.70.25   ]  [93.184.216.119 ]  [ICMP_TIMXCEED]
 6.  [66.163.64.150  ]  [93.184.216.119 ]  [ICMP_TIMXCEED]
 7.  [66.163.75.117  ]  [93.184.216.119 ]  [ICMP_TIMXCEED]
 8.  [206.223.119.59 ]  [93.184.216.119 ]  [ICMP_TIMXCEED]
```
