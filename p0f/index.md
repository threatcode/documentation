---
Title: p0f
Homepage: http://lcamtuf.coredump.cx/p0f3/
Repository: https://salsa.debian.org/pkg-security-team/p0f
Architectures: any
Version: 3.09b-3
Metapackages: kali-linux-everything kali-linux-large kali-linux-nethunter kali-tools-information-gathering 
Icon: images/p0f-logo.svg
PackagesInfo: |
 ### p0f
 
  p0f performs passive OS detection based on SYN packets. Unlike nmap
  and queso, p0f does recognition without sending any data.
  Additionally, it is able to determine the distance to the remote
  host, and can be used to determine the structure of a foreign or
  local network. When running on the gateway of a network it is able
  to gather huge amounts of data and provide useful statistics. On a
  user-end computer it could be used as powerful IDS add-on. p0f
  supports full tcpdump-style filtering expressions, and has an
  extensible and detailed fingerprinting database.
 
 **Installed size:** `219 KB`  
 **How to install:** `sudo apt install p0f`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libpcap0.8 
 {{< /spoiler >}}
 
 ##### p0f
 
 Identify remote systems passively
 
 ```
 root@kali:~# p0f -h
 p0f: invalid option -- 'h'
 Usage: p0f [ ...options... ] [ 'filter rule' ]
 
 Network interface options:
 
   -i iface  - listen on the specified network interface
   -r file   - read offline pcap data from a given file
   -p        - put the listening interface in promiscuous mode
   -L        - list all available interfaces
 
 Operating mode and output settings:
 
   -f file   - read fingerprint database from 'file' (/etc/p0f/p0f.fp)
   -o file   - write information to the specified log file
   -s name   - answer to API queries at a named unix socket
   -u user   - switch to the specified unprivileged account and chroot
   -d        - fork into background (requires -o or -s)
 
 Performance-related options:
 
   -S limit  - limit number of parallel API connections (20)
   -t c,h    - set connection / host cache age limits (30s,120m)
   -m c,h    - cap the number of active connections / hosts (1000,10000)
 
 Optional filter expressions (man tcpdump) can be specified in the command
 line to prevent p0f from looking at incidental network traffic.
 
 Problems? You can reach the author at <lcamtuf@coredump.cx>.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## p0f Usage Example

Use interface eth0 (`-i eth0`) in promiscuous mode (`-p`), saving the results to a file (`-o /tmp/p0f.log`):

```
root@kali:~# p0f -i eth0 -p -o /tmp/p0f.log
-- p0f 3.09b by Michal Zalewski <lcamtuf@coredump.cx> ---

[+] Closed 1 file descriptor.
[+] Loaded 322 signatures from '/etc/p0f/p0f.fp'.
[+] Intercepting traffic on interface 'eth0'.
[+] Default packet filtering configured [+VLAN].
[+] Log file '/tmp/p0f.log' opened for writing.
[+] Entered main event loop.

.-[ 192.168.1.15/35834 -> 173.246.39.185/873 (syn) ]-
|
| client   = 192.168.1.15/35834
| os       = Linux 3.11 and newer
| dist     = 0
| params   = none
| raw_sig  = 4:64+0:0:1460:mss*20,7:mss,sok,ts,nop,ws:df,id+:0
```
