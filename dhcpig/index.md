---
Title: dhcpig
Homepage: https://github.com/kamorin/DHCPig
Repository: https://salsa.debian.org/pkg-security-team/dhcpig
Architectures: all
Version: 1.5-4
Metapackages: kali-linux-everything kali-linux-large kali-tools-vulnerability 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### dhcpig
 
  DHCPig initiates an advanced DHCP exhaustion attack. It will consume all IPs
  on the LAN, stop new users from obtaining IPs, release any IPs in use, then
  for good measure send gratuitous ARP and knock all windows hosts offline.
   
  It is based on the scapy library and requests admin privileges to execute.
  It has been tested on multiple Linux distributions and multiple DHCP servers
  (ISC, Windows 2k3/2k8, ...).
 
 **Installed size:** `55 KB`  
 **How to install:** `sudo apt install dhcpig`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-scapy
 {{< /spoiler >}}
 
 ##### dhcpig
 
 DHCP exhaustion script using scapy network library
 
 ```
 root@kali:~# dhcpig -h
 
 enhanced DHCP exhaustion attack.
 
 Doc:
     http://github.com/kamorin/DHCPig
 
 
 Usage:
     pig.py [-h -v -6 -1 -s -f -t -a -i -o -l -x -y -z -g -r -n -c ] <interface>
   
 Options:
     -h, --help                     <-- you are here :)
     -v, --verbosity                ...  0 ... no         (3)
                                         1 ... minimal
                                        10 ... default
                                        99 ... debug
                                        
     -6, --ipv6                     ... DHCPv6 (off, DHCPv4 by default)
     -1, --v6-rapid-commit          ... enable RapidCommit (2way ip assignment instead of 4way) (off)
     
     -s, --client-src               ... a list of client macs 00:11:22:33:44:55,00:11:22:33:44:56 (Default: <random>)
     -O, --request-options          ... option-codes to request e.g. 21,22,23 or 12,14-19,23 (Default: 0-80)
     
     -f, --fuzz                     ... randomly fuzz packets (off)
 
     -t, --threads                  ... number of sending threads (1)
     
     -a, --show-arp                 ... detect/print arp who_has (off)
     -i, --show-icmp                ... detect/print icmps requests (off)
     -o, --show-options             ... print lease infos (off)
     -l, --show-lease-confirm       ... detect/print dhcp replies (off)
     
     -g, --neighbors-attack-garp    ... knock off network segment using gratious arps (off)
     -r, --neighbors-attack-release ... release all neighbor ips (off)
     -n, --neighbors-scan-arp       ... arp neighbor scan (off)
     
     -x, --timeout-threads          ... thread spawn timer (0.4)
     -y, --timeout-dos              ... DOS timeout (8) (wait time to mass grat.arp)
     -z, --timeout-dhcprequest      ... dhcp request timeout (2)
     
     -c, --color                    ... enable color output (off)
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## dhcpig Usage Example

Exhaust all of the available DHCP addresses using the eth0 interface (`eth0`):

```
root@kali:~# pig.py eth0
WARNING: No route found for IPv6 destination :: (no default route?)

Sending DHCPDISCOVER on eth0
waiting for first DHCP Server response on eth0
```
