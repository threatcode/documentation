---
Title: irpas
Homepage: http://www.phenoelit.org/fr/tools.html
Repository: https://salsa.debian.org/pkg-security-team/irpas
Architectures: any
Version: 0.10-9
Metapackages: kali-linux-everything kali-linux-large kali-tools-information-gathering 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### irpas
 
  This package contains a collection of programs used for advanced network
  operations, testing, and debugging.
   
  CDP and the route injectors can be useful in a production network.
  Several other tools are useful for security and firewall testing.
  Finally some tools such as netenum are useful for general admin
  scripting.
   
  Like all powerful tools, it could cause great damage, so be careful.
   
      * cdp - Cisco discovery protocol packet sender
      * igrp - IGRP route injector
      * ass - Autonomous system scanner
      * irdp - IRDP sender
      * irdpresponder - IRDP responder
      * itrace - ICMP based traceroute
      * tctrace - TCP SYN based traceroute
      * protos - ICMP based port scanner
      * netmask - Asks for netmask via ICMP
      * file2cable - Dumps any binary file direct to ethernet
      * dfkaa - Troubleshoot devices formerly known as Ascend (Pipeline, etc)
      * netenum - Ping scanner designed for shell scripts
      * hsrp - HSRP failover tester
      * icmp_redirect - ICMP redirection system
      * timestamp - ICMP timestamp requester
      * dhcpx - DHCP server "exerciser"
 
 **Installed size:** `406 KB`  
 **How to install:** `sudo apt install irpas`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libpcap0.8 
 {{< /spoiler >}}
 
 ##### ass
 
 Autonomous system scanner
 
 ```
 root@kali:~# ass -h
 ass [-v[v[v]]] -i <interface> [-ApcMs] [-P IER12]
 	[-a <autonomous system start> -b <autonomous system stop>]
 	[-S <spoofed source IP>] [-D <destination ip>]
 	[-T <packets per delay>]
 	[-r <filename>]
 ```
 
 - - -
 
 ##### cdp
 
 Cdp packet generator
 
 ```
 root@kali:~# cdp -h
 cdp [-v] -i <interface> -m {0,1} ...
 
 Flood mode (-m 0):
 -n <number>	number of packets
 -l <number>	length of the device id
 -c <char>	character to fill in device id
 -r		randomize device id string
 
 Spoof mode (-m 1):
 -D <string>	Device id
 -P <string>	Port id
 -L <string>	Platform
 -S <string>	Software
 -F <string>	IP address
 -C <capabilities>
 	these are:
 	R - Router, T - Trans Bridge, B - Source Route Bridge
 	S - Switch, H - Host, I - IGMP, r - Repeater
 ```
 
 - - -
 
 ##### dfkaa
 
 
 ```
 root@kali:~# dfkaa -h
 dfkaa: invalid option -- 'h'
 Usage ... well. Look into the .c
 ```
 
 - - -
 
 ##### dhcpx
 
 
 ```
 root@kali:~# dhcpx -h
 dhcpx [-v[v[v]]] -i <interface> [-A] 
 	[-D <destination ip>]
 	[-t <discovery time in secs>]
 	[-u <ARP time in secs>]
 ```
 
 - - -
 
 ##### file2cable
 
 Sends a file as a raw ethernet frame
 
 ```
 root@kali:~# file2cable -h
 file2cable [-v] -i <interface> -f <file>
 ```
 
 - - -
 
 ##### hsrp
 
 
 ```
 root@kali:~# hsrp -h
 hsrp -i <interface> -v <virtual IP> -d <router ip> -a <authword>
 	-g <group> [-S <source>]
 EXAMPLE:
 while (true);
   do (./hsrp -d 224.0.0.2 -v192.168.1.22 -a cisco -g 1 -i eth0 ; sleep 3);
 done
 ```
 
 - - -
 
 ##### icmp_redirect
 
 
 ```
 root@kali:~# icmp_redirect -h
 icmp_redirect [-v[v[v]]] -i <interface> 
 	[-s <source net>/<source mask>]
 	[-d <destination net>/<destination mask>]
 	[-G <gateway IP>] [-w <delay>]
 	[-S <ip address>]
 ```
 
 - - -
 
 ##### igrp
 
 Igrp route injector
 
 ```
 root@kali:~# igrp -h
 Usage: 
 igrp [-v[v[v]]] -i <interface> -f <routes file> 
 	-a <autonomous system> [-b brute force end]
 	[-S <spoofed source IP>] [-D <destination ip>]
 ```
 
 - - -
 
 ##### inetmask
 
 Ask for the netmask via ICMP
 
 ```
 root@kali:~# inetmask -h
 inetmask: invalid option -- 'h'
 Usage: inetmask -d <destination> -t <timeout>
 ```
 
 - - -
 
 ##### irdp
 
 Irdp packet sender
 
 ```
 root@kali:~# irdp -h
 Usage: 
 irdp [-v (useless)] -i <interface> 
 	[-S <spoofed source IP>] [-D <destination ip>]
 	[-l <lifetime in sec, default: 1800>] [-p <preference>]
 ```
 
 - - -
 
 ##### irdpresponder
 
 Irdpresponder packet sender
 
 ```
 root@kali:~# irdpresponder -h
 Usage: 
 irdpresponder [-v[v[v]]] -i <interface>
 	[-S <spoofed source IP>] [-D <destination ip>]
 	[-l <lifetime in sec, default: 1800>] [-p <preference>]
 ```
 
 - - -
 
 ##### itrace
 
 Similar to traceroute, yet uses ICMP echo
 
 ```
 root@kali:~# itrace -h
 itrace: invalid option -- 'h'
 Usage: itrace [-vn] [-pX] [-mX] [-tX] -i<dev> -d<destination>
 
 -v	verbose
 -n	reverse lookup IPs
 -pX	send X probes (default=3)
 -mX	maximum TTL (default=30)
 -tX	timeout X sec (default=3)
 -i<dev>	use this device
 -d<des>	trace to this destination
 ```
 
 - - -
 
 ##### netenum
 
 
 ```
 root@kali:~# netenum -h
 error in enumerate
 ```
 
 - - -
 
 ##### protos
 
 
 ```
 root@kali:~# protos -h
 Usage: ./protos -i eth0 -d 10.1.2.3 -v
 -v             verbose
 -V             show which protocols are not supported
 -u             don't ping targets first
 -s             make the scan slow (for very remote devices)
 -L             show the long protocol name and it's reference (RFC)
 -p x           number of probes (default=5)
 -S x           sleeptime is x (default=1)
 -a x           continue scan afterwards for x seconds (default=3)
 -d dest        destination (IP or IP/MASK)
 -i interface   the eth0 stuff
 -W             don't scan, just print the protocol list
 ```
 
 - - -
 
 ##### tctrace
 
 Similar to traceroute, yet uses TCP SYN packets
 
 ```
 root@kali:~# tctrace -h
 tctrace: invalid option -- 'h'
 Usage: tctrace [-vn] [-pX] [-mX] [-tX] [-DX] [-SX] -i<dev> -d<destination>
 
 -v	verbose
 -n	reverse lookup IPs
 -pX	send X probes (default=3)
 -mX	maximum TTL (default=30)
 -tX	timeout X sec (default=3)
 -DX	destination port (default=80)
 -SX	source port (default=1064)
 -i<dev>	use this device
 -d<des>	trace to this destination
 ```
 
 - - -
 
 ##### timestamp
 
 
 ```
 root@kali:~# timestamp -h
 timestamp: invalid option -- 'h'
 Usage: timestamp -d <destination> -t <timeout>
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
