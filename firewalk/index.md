---
Title: firewalk
Homepage: http://packetfactory.openwall.net/projects/firewalk/
Repository: https://salsa.debian.org/pkg-security-team/firewalk
Architectures: any
Version: 5.0-5
Metapackages: kali-linux-everything kali-tools-information-gathering 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### firewalk
 
  Firewalk is an active reconnaissance network security tool that attempts to
  determine what layer 4 protocols a given IP forwarding device will pass. It
  works by sending out TCP or UDP packets with a TTL one hop greater than the
  targeted gateway. If the gateway allows the traffic, it will forward the
  packets to the next hop where they will expire and elicit an ICMP_TIME_EXCEEDED
  message. Otherwise, it will likely drop the packets and there will be no
  response.
   
  To get the correct IP TTL that will result in packets expiring one hop beyond
  the gateway, Firewalk needs to ramp up hop counts. It does this in the same
  manner that traceroute works. Once the scan is `bound` (that is, Firewalk
  knows the gateway hop count), it begins the scan. The ultimate destination host
  does not have to be reached, it only needs to be somewhere downstream, on the
  other side of the gateway, from the scanning host.
   
  Firewalk helps in assessing the security configuration of packet filtering
  devices, such as those used in firewall systems. It is relevant for network
  security assessments, like network penetration tests (pentests).
 
 **Installed size:** `50 KB`  
 **How to install:** `sudo apt install firewalk`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libdumbnet1 
 * libnet1 
 * libpcap0.8 
 {{< /spoiler >}}
 
 ##### firewalk
 
 Active Reconnaissance Network Security Tool with Extreme Prejudice
 
 ```
 root@kali:~# firewalk --help
 firewalk: invalid option -- '-'
 Usage : firewalk [options] target_gateway metric
 		   [-d 0 - 65535] destination port to use (ramping phase)
 		   [-h] program help
 		   [-i device] interface
 		   [-n] do not resolve IP addresses into hostnames
 		   [-p TCP | UDP] firewalk protocol
 		   [-r] strict RFC adherence
 		   [-S x - y, z] port range to scan
 		   [-s 0 - 65535] source port
 		   [-T 1 - 1000] packet read timeout in ms
 		   [-t 1 - 25] IP time to live
 		   [-v] program version
 		   [-x 1 - 8] expire vector
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## firewalk Usage Example

Scan ports 8079-8081 (`-S8079-8081`) through the eth0 interface (`-i eth0`), do not resolve hostnames (`-n`), use TCP (`-pTCP`) via the gateway (`192.168.1.1`) against the target IP (`192.168.0.1`):

```
root@kali:~# firewalk -S8079-8081  -i eth0 -n -pTCP 192.168.1.1 192.168.0.1
Firewalk 5.0 [gateway ACL scanner]
Firewalk state initialization completed successfully.
TCP-based scan.
Ramping phase source port: 53, destination port: 33434
Hotfoot through 192.168.1.1 using 192.168.0.1 as a metric.
Ramping Phase:
 1 (TTL  1): expired [192.168.1.1]
Binding host reached.
Scan bound at 2 hops.
Scanning Phase:
port 8079: *no response*
port 8080: A! open (port not listen) [192.168.0.1]
port 8081: *no response*

Scan completed successfully.

Total packets sent:                4
Total packet errors:               0
Total packets caught               2
Total packets caught of interest   2
Total ports scanned                3
Total ports open:                  1
Total ports unknown:               0
```
