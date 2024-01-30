---
Title: tundeep
Homepage: https://www.adampalmer.me/iodigitalsec/tundeep/
Repository: https://gitlab.com/kalilinux/packages/tundeep
Architectures: any
Version: 1.1~git20190802-0kali2
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### tundeep
 
  The tool resides [almost] entirely in user space on the victim aside from the
  pcap requirement.
 
 **Installed size:** `48 KB`  
 **How to install:** `sudo apt install tundeep`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libpcap0.8 
 * zlib1g 
 {{< /spoiler >}}
 
 ##### tundeep
 
 
 ```
 root@kali:~# tundeep -h
 tundeep: option requires an argument -- 'h'
 Option -h error.
 *** tundeep v1.0_20170728 by Adam Palmer <adam@adampalmer.me> ***
 Usage: tundeep <-i iface|[-t|-T] tapiface> <-h ip> <-p port> [-6] [-C] <-c|-s> [-x tapip] [-y tapmask] [-u tapmac] [-b bpf] [-d udp mode] [-e udp remote] [-K]
 
 -6 IPv6 mode
 -C compress mode
 -K disable checksum
 -a print all pcap devs
 -b "bpf"
 -i interface to bind to
 -h IP to bind to/connect to
 -p port to bind to/connect to
 -c client mode
 -s server mode
 -d udp mode
 -e udp peer
 -t tap interface 
 -T ipv6 tap interface 
 -u tap mac 
 -x if -t mode, set iface ip, if -T mode, set iface ipv6 ip
 -y if -t mode, set iface mask, if -T mode, set iface ipv6 prefixlen
 --------------------
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
