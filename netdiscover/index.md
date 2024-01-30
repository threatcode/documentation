---
Title: netdiscover
Homepage: https://github.com/netdiscover-scanner/netdiscover
Repository: https://salsa.debian.org/debian/netdiscover
Architectures: any
Version: 0.10-3
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-information-gathering 
Icon: images/netdiscover-logo.svg
PackagesInfo: |
 ### netdiscover
 
  Netdiscover is an active/passive address reconnaissance tool, mainly
  developed for those wireless networks without dhcp server, when you
  are wardriving. It can be also used on hub/switched networks.
   
  Built on top of libnet and libpcap, it can passively detect online
  hosts, or search for them, by actively sending ARP requests.
   
  Netdiscover can also be used to inspect your network ARP traffic,
  or find network addresses using auto scan mode, which will scan for
  common local networks.
   
  Netdiscover uses the OUI table to show the vendor of the each MAC
  address discovered and is very useful for security checks or in
  pentests.
 
 **Installed size:** `2.75 MB`  
 **How to install:** `sudo apt install netdiscover`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libpcap0.8 
 {{< /spoiler >}}
 
 ##### netdiscover
 
 Active/passive ARP reconnaissance tool
 
 ```
 root@kali:~# netdiscover --help
 
 Netdiscover 0.10 [Active/passive ARP reconnaissance tool]
 Written by: Jaime Penalba <jpenalbae@gmail.com>
 
 Usage: netdiscover [-i device] [-r range | -l file | -p] [-m file] [-F filter] [-s time] [-c count] [-n node] [-dfPLNS]
   -i device: your network device
   -r range: scan a given range instead of auto scan. 192.168.6.0/24,/16,/8
   -l file: scan the list of ranges contained into the given file
   -p passive mode: do not send anything, only sniff
   -m file: scan a list of known MACs and host names
   -F filter: customize pcap filter expression (default: "arp")
   -s time: time to sleep between each ARP request (milliseconds)
   -c count: number of times to send each ARP request (for nets with packet loss)
   -n node: last source IP octet used for scanning (from 2 to 253)
   -d ignore home config files for autoscan and fast mode
   -f enable fastmode scan, saves a lot of time, recommended for auto
   -P print results in a format suitable for parsing by another program and stop after active scan
   -L similar to -P but continue listening after the active scan is completed
   -N Do not print header. Only valid when -P or -L is enabled.
   -S enable sleep time suppression between each request (hardcore mode)
 
 If -r, -l or -p are not enabled, netdiscover will scan for common LAN addresses.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
