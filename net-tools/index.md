---
Title: net-tools
Homepage: http://sourceforge.net/projects/net-tools/
Repository: https://salsa.debian.org/debian/net-tools
Architectures: any
Version: 2.10-0.1
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-linux-nethunter kali-linux-wsl kali-tools-802-11 kali-tools-forensics kali-tools-identify kali-tools-post-exploitation kali-tools-respond kali-tools-sniffing-spoofing kali-tools-top10 kali-tools-wireless 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### net-tools
 
  This package includes the important tools for controlling the network
  subsystem of the Linux kernel.  This includes arp, ifconfig, netstat,
  rarp, nameif and route.  Additionally, this package contains utilities
  relating to particular network hardware types (plipconfig, slattach,
  mii-tool) and advanced aspects of IP configuration (iptunnel, ipmaddr).
   
  In the upstream package 'hostname' and friends are included. Those are
  not installed by this package, since there is a special "hostname*.deb".
 
 **Installed size:** `978 KB`  
 **How to install:** `sudo apt install net-tools`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libselinux1 
 {{< /spoiler >}}
 
 ##### arp
 
 Linux ARP kernel module.
 Manipulate the system ARP cache
 
 ```
 root@kali:~# arp -h
 Usage:
   arp [-vn]  [<HW>] [-i <if>] [-a] [<hostname>]             <-Display ARP cache
   arp [-v]          [-i <if>] -d  <host> [pub]               <-Delete ARP entry
   arp [-vnD] [<HW>] [-i <if>] -f  [<filename>]            <-Add entry from file
   arp [-v]   [<HW>] [-i <if>] -s  <host> <hwaddr> [temp]            <-Add entry
   arp [-v]   [<HW>] [-i <if>] -Ds <host> <if> [netmask <nm>] pub          <-''-
 
         -a                       display (all) hosts in alternative (BSD) style
         -e                       display (all) hosts in default (Linux) style
         -s, --set                set a new ARP entry
         -d, --delete             delete a specified entry
         -v, --verbose            be verbose
         -n, --numeric            don't resolve names
         -i, --device             specify network interface (e.g. eth0)
         -D, --use-device         read <hwaddr> from given device
         -A, -p, --protocol       specify protocol family
         -f, --file               read new entries from file or from /etc/ethers
 
   <HW>=Use '-H <hw>' to specify hardware address type. Default: ether
   List of possible hardware types (which support ARP):
 ```
 
 - - -
 
 ##### ifconfig
 
 Configure a network interface
 
 ```
 root@kali:~# ifconfig -h
 Usage:
   ifconfig [-a] [-v] [-s] <interface> [[<AF>] <address>]
   [add <address>[/<prefixlen>]]
   [del <address>[/<prefixlen>]]
   [[-]broadcast [<address>]]  [[-]pointopoint [<address>]]
   [netmask <address>]  [dstaddr <address>]  [tunnel <address>]
   [outfill <NN>] [keepalive <NN>]
   [hw <HW> <address>]  [mtu <NN>]
   [[-]trailers]  [[-]arp]  [[-]allmulti]
   [multicast]  [[-]promisc]
   [mem_start <NN>]  [io_addr <NN>]  [irq <NN>]  [media <type>]
   [txqueuelen <NN>]
   [name <newname>]
   [[-]dynamic]
   [up|down] ...
 
   <HW>=Hardware Type.
   List of possible hardware types:
   <AF>=Address family. Default: inet
   List of possible address families:
 ```
 
 - - -
 
 ##### ipmaddr
 
 
 ```
 root@kali:~# ipmaddr -h
 Usage: ipmaddr [ add | del ] MULTIADDR dev STRING
        ipmaddr show [ dev STRING ] [ ipv4 | ipv6 | link | all ]
        ipmaddr -V | -version
 ```
 
 - - -
 
 ##### iptunnel
 
 Create and manage IP tunnels
 
 ```
 root@kali:~# iptunnel -h
 Usage: iptunnel { add | change | del | show } [ NAME ]
           [ mode { ipip | gre | sit } ] [ remote ADDR ] [ local ADDR ]
           [ [i|o]seq ] [ [i|o]key KEY ] [ [i|o]csum ]
           [ ttl TTL ] [ tos TOS ] [ nopmtudisc ] [ dev PHYS_DEV ]
        iptunnel -V | --version
 
 Where: NAME := STRING
        ADDR := { IP_ADDRESS | any }
        TOS  := { NUMBER | inherit }
        TTL  := { 1..255 | inherit }
        KEY  := { DOTTED_QUAD | NUMBER }
 ```
 
 - - -
 
 ##### mii-tool
 
 View, manipulate media-independent interface status
 
 ```
 root@kali:~# mii-tool -h
 mii-tool: invalid option -- 'h'
 usage: mii-tool [-VvRrwl] [-A media,... | -F media] [-p addr] <interface ...>
        -V, --version               display version information
        -v, --verbose               more verbose output
        -R, --reset                 reset MII to poweron state
        -r, --restart               restart autonegotiation
        -w, --watch                 monitor for link status changes
        -l, --log                   with -w, write events to syslog
        -A, --advertise=media,...   advertise only specified media
        -F, --force=media           force specified media technology
        -p, --phy=addr              set PHY (MII address) to report
 media: 1000baseTx-HD, 1000baseTx-FD,
        100baseT4, 100baseTx-FD, 100baseTx-HD,
        10baseT-FD, 10baseT-HD,
        (to advertise both HD and FD) 1000baseTx, 100baseTx, 10baseT
 ```
 
 - - -
 
 ##### nameif
 
 Name network interfaces based on MAC addresses
 
 ```
 root@kali:~# nameif -h
 usage: nameif [-c configurationfile] [-s] {ifname macaddress}
 ```
 
 - - -
 
 ##### netstat
 
 Print network connections, routing tables, interface statistics, masquerade connections, and multicast memberships
 
 ```
 root@kali:~# netstat -h
 usage: netstat [-vWeenNcCF] [<Af>] -r         netstat {-V|--version|-h|--help}
        netstat [-vWnNcaeol] [<Socket> ...]
        netstat { [-vWeenNac] -i | [-cnNe] -M | -s [-6tuw] }
 
         -r, --route              display routing table
         -i, --interfaces         display interface table
         -g, --groups             display multicast group memberships
         -s, --statistics         display networking statistics (like SNMP)
         -M, --masquerade         display masqueraded connections
 
         -v, --verbose            be verbose
         -W, --wide               don't truncate IP addresses
         -n, --numeric            don't resolve names
         --numeric-hosts          don't resolve host names
         --numeric-ports          don't resolve port names
         --numeric-users          don't resolve user names
         -N, --symbolic           resolve hardware names
         -e, --extend             display other/more information
         -p, --programs           display PID/Program name for sockets
         -o, --timers             display timers
         -c, --continuous         continuous listing
 
         -l, --listening          display listening server sockets
         -a, --all                display all sockets (default: connected)
         -F, --fib                display Forwarding Information Base (default)
         -C, --cache              display routing cache instead of FIB
         -Z, --context            display SELinux security context for sockets
 
   <Socket>={-t|--tcp} {-u|--udp} {-U|--udplite} {-S|--sctp} {-w|--raw}
            {-x|--unix} --ax25 --ipx --netrom
   <AF>=Use '-6|-4' or '-A <af>' or '--<af>'; default: inet
   List of possible address families (which support routing):
 ```
 
 - - -
 
 ##### plipconfig
 
 Fine tune PLIP device parameters
 
 ```
 root@kali:~# plipconfig -h
 Usage: plipconfig interface [nibble NN] [trigger NN]
        plipconfig -V | --version
        plipconfig -h | --help
 ```
 
 - - -
 
 ##### rarp
 
 Manipulate the system RARP table
 
 ```
 root@kali:~# rarp -h
 Usage: rarp -a                               list entries in cache.
        rarp -d <hostname>                    delete entry from cache.
        rarp [<HW>] -s <hostname> <hwaddr>    add entry to cache.
        rarp -f                               add entries from /etc/ethers.
        rarp -V                               display program version.
 
   <HW>=Use '-H <hw>' to specify hardware address type. Default: ether
   List of possible hardware types (which support ARP):
 ```
 
 - - -
 
 ##### route
 
 Show / manipulate the IP routing table
 
 ```
 root@kali:~# route -h
 Usage: route [-nNvee] [-FC] [<AF>]           List kernel routing tables
        route [-v] [-FC] {add|del|flush} ...  Modify routing table for AF.
 
        route {-h|--help} [<AF>]              Detailed usage syntax for specified AF.
        route {-V|--version}                  Display version/author and exit.
 
         -v, --verbose            be verbose
         -n, --numeric            don't resolve names
         -e, --extend             display other/more information
         -F, --fib                display Forwarding Information Base (default)
         -C, --cache              display routing cache instead of FIB
 
   <AF>=Use -4, -6, '-A <af>' or '--<af>'; default: inet
   List of possible address families (which support routing):
 ```
 
 - - -
 
 ##### slattach
 
 Attach a network interface to a serial line
 
 ```
 root@kali:~# slattach -h
 Usage: slattach [-ehlLmnqv] [-k keepalive] [-o outfill] [-c cmd] [-s speed] [-p protocol] tty | -
        slattach -V | --version
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
