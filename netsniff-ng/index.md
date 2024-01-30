---
Title: netsniff-ng
Homepage: http://netsniff-ng.org/
Repository: https://salsa.debian.org/debian/netsniff-ng
Architectures: any
Version: 0.6.8-3
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-respond kali-tools-sniffing-spoofing 
Icon: images/netsniff-ng-logo.svg
PackagesInfo: |
 ### netsniff-ng
 
  netsniff-ng is a high performance Linux network sniffer for packet inspection.
  It can be used for protocol analysis, reverse engineering or network
  debugging. The gain of performance is reached by 'zero-copy' mechanisms, so
  that the kernel does not need to copy packets from kernelspace to userspace.
   
  netsniff-ng toolkit currently consists of the following utilities:
   
   * netsniff-ng: a zero-copy packet analyzer, pcap capturing/replaying tool
   * trafgen: a multithreaded low-level zero-copy network packet generator
   * mausezahn: high-level packet generator for appliances with Cisco-CLI
   * ifpps: a top-like kernel networking and system statistics tool
   * curvetun: a lightweight curve25519-based multiuser IP tunnel
   * astraceroute: an autonomous system trace route and DPI testing utility
   * flowtop: a top-like netfilter connection tracking tool
   * bpfc: a [seccomp-]BPF (Berkeley packet filter) compiler, JIT disassembler
 
 **Installed size:** `2.04 MB`  
 **How to install:** `sudo apt install netsniff-ng`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libcli1.10 
 * libgeoip1 
 * libncurses6 
 * libnet1 
 * libnetfilter-conntrack3 
 * libnl-3-200 
 * libnl-genl-3-200 
 * libnl-route-3-200 
 * libpcap0.8 
 * libsodium23 
 * libtinfo6 
 * liburcu8 
 * zlib1g 
 {{< /spoiler >}}
 
 ##### astraceroute
 
 Autonomous system trace route utility
 
 ```
 root@kali:~# astraceroute -h
 astraceroute 0.6.8, autonomous system trace route utility
 http://www.netsniff-ng.org
 
 Usage: astraceroute [options]
 Options:
  -H|--host <host>        Host/IPv4/IPv6 to lookup AS route to
  -p|--port <port>        Hosts port to lookup AS route to
  -i|-d|--dev <device>    Networking device, e.g. eth0
  -b|--bind <IP>          IP address to bind to, Must specify -6 for an IPv6 address
  -f|--init-ttl <ttl>     Set initial TTL
  -m|--max-ttl <ttl>      Set maximum TTL (def: 30)
  -q|--num-probes <num>   Number of max probes for each hop (def: 2)
  -x|--timeout <sec>      Probe response timeout in sec (def: 3)
  -X|--payload <string>   Specify a payload string to test DPIs
  -l|--totlen <len>       Specify total packet len
  -4|--ipv4               Use IPv4-only requests
  -6|--ipv6               Use IPv6-only requests
  -n|--numeric            Do not do reverse DNS lookup for hops
  -u|--update             Update GeoIP databases
  -L|--latitude           Show latitude and longitude
  -N|--dns                Do a reverse DNS lookup for hops
  -S|--syn                Set TCP SYN flag
  -A|--ack                Set TCP ACK flag
  -F|--fin                Set TCP FIN flag
  -P|--psh                Set TCP PSH flag
  -U|--urg                Set TCP URG flag
  -R|--rst                Set TCP RST flag
  -E|--ecn-syn            Send ECN SYN packets (RFC3168)
  -t|--tos <tos>          Set the IP TOS field
  -G|--nofrag             Set do not fragment bit
  -Z|--show-packet        Show returned packet on each hop
  -v|--version            Print version and exit
  -h|--help               Print this help and exit
 
 Examples:
   IPv4 trace of AS with TCP SYN probe (this will most-likely pass):
     astraceroute -i eth0 -N -S -H netsniff-ng.org
   IPv4 trace of AS with TCP ECN SYN probe:
     astraceroute -i eth0 -N -E -H netsniff-ng.org
   IPv4 trace of AS with TCP FIN probe:
     astraceroute -i eth0 -N -F -H netsniff-ng.org
   IPv4 trace of AS with Xmas probe:
     astraceroute -i eth0 -N -FPU -H netsniff-ng.org
   IPv4 trace of AS with Null probe with ASCII payload:
     astraceroute -i eth0 -N -H netsniff-ng.org -X "censor-me" -Z
   IPv6 trace of AS up to www.6bone.net:
     astraceroute -6 -i eth0 -S -E -N -H www.6bone.net
 
 Note:
   If the TCP probe did not give any results, then astraceroute will
   automatically probe for classic ICMP packets! To gather more
   information about astraceroute's fetched AS numbers, see e.g.
   http://bgp.he.net/AS<number>!
 
 Please report bugs at https://github.com/netsniff-ng/netsniff-ng/issues
 Copyright (C) 2011-2013 Daniel Borkmann <dborkma@tik.ee.ethz.ch>
 Swiss federal institute of technology (ETH Zurich)
 License: GNU GPL version 2.0
 This is free software: you are free to change and redistribute it.
 There is NO WARRANTY, to the extent permitted by law.
 ```
 
 - - -
 
 ##### bpfc
 
 A Berkeley Packet Filter assembler and compiler
 
 ```
 root@kali:~# bpfc -h
 bpfc 0.6.8, a tiny BPF compiler
 http://www.netsniff-ng.org
 
 Usage: bpfc [options] || bpfc <program>
 Options:
   -i|--input <program/->  Berkeley Packet Filter file/stdin
   -p|--cpp                Run bpf program through C preprocessor
   -D|--define             Add macro/define for C preprocessor
   -f|--format <format>    Output format: C|netsniff-ng|xt_bpf|tcpdump
   -b|--bypass             Bypass filter validation (e.g. for bug testing)
   -V|--verbose            Be more verbose
   -d|--dump               Dump supported instruction table
   -v|--version            Print version and exit
   -h|--help               Print this help and exit
 
 Examples:
   bpfc fubar
   bpfc fubar > foo (bpfc -f C -i fubar > foo) -->  netsniff-ng -f foo ...
   bpfc -f tcpdump -i fubar > foo -->  tcpdump -ddd like ...
   bpfc -f xt_bpf -b -p -i fubar
   iptables -A INPUT -m bpf --bytecode "`./bpfc -f xt_bpf -i fubar`" -j LOG
   bpfc -   (read from stdin)
 Note:
   Generation of seccomp-BPF filters are fully supported as well.
 
 Please report bugs at https://github.com/netsniff-ng/netsniff-ng/issues
 Copyright (C) 2011-2013 Daniel Borkmann <dborkma@tik.ee.ethz.ch>,
 Swiss federal institute of technology (ETH Zurich)
 License: GNU GPL version 2.0
 This is free software: you are free to change and redistribute it.
 There is NO WARRANTY, to the extent permitted by law.
 ```
 
 - - -
 
 ##### curvetun
 
 A lightweight curve25519 ip4/6 tunnel
 
 ```
 root@kali:~# curvetun -h
 curvetun 0.6.8, lightweight curve25519-based IP tunnel
 http://www.netsniff-ng.org
 
 Usage: curvetun [options]
 Options, general:
   -d|--dev <tun>          Networking tunnel device, e.g. tun0
   -p|--port <num>         Server port number (mandatory)
   -t|--stun <server>      Show public IP/Port mapping via STUN
   -c|--client[=alias]     Client mode, server alias optional
   -k|--keygen             Generate public/private keypair
   -x|--export             Export your public data for remote servers
   -C|--dumpc              Dump parsed clients
   -S|--dumps              Dump parsed servers
   -D|--nofork             Do not daemonize
   -s|--server             Server mode, options follow below
   -N|--no-logging         Disable server logging (for better anonymity)
   -u|--udp                Use UDP as carrier instead of TCP
   -4|--ipv4               Tunnel devices are IPv4
   -6|--ipv6               Tunnel devices are IPv6
   -v|--version            Print version and exit
   -h|--help               Print this help and exit
 
 Example:
   See curvetun's man page for a configuration example.
   curvetun --server -4 -u -N --port 6666 --stun stunserver.org
   curvetun --client=ethz
 
   curvetun --keygen
   curvetun --export
 Note:
   There is no default port specified, so that you are forced
   to select your own! For client/server status messages see syslog!
   This software is an experimental prototype intended for researchers.
 
 Secret ingredient: 7647-14-5
 
 
 Please report bugs at https://github.com/netsniff-ng/netsniff-ng/issues
 Copyright (C) 2011-2013 Daniel Borkmann <dborkma@tik.ee.ethz.ch>,
 Swiss federal institute of technology (ETH Zurich)
 License: GNU GPL version 2.0
 This is free software: you are free to change and redistribute it.
 There is NO WARRANTY, to the extent permitted by law.
 ```
 
 - - -
 
 ##### flowtop
 
 Top-like netfilter TCP/UDP/SCTP/DCCP/ICMP(v6) flow tracking
 
 ```
 root@kali:~# flowtop -h
 flowtop 0.6.8, top-like netfilter TCP/UDP/SCTP/.. flow tracking
 http://www.netsniff-ng.org
 
 Usage: flowtop [options]
 Options:
   -4|--ipv4              Show only IPv4 flows (default)
   -6|--ipv6              Show only IPv6 flows (default)
   -T|--tcp               Show only TCP flows (default)
   -U|--udp               Show only UDP flows
   -D|--dccp              Show only DCCP flows
   -I|--icmp              Show only ICMP/ICMPv6 flows
   -S|--sctp              Show only SCTP flows
   -n|--no-dns            Don't perform hostname lookup
   -G|--no-geoip          Don't perform GeoIP lookup
   -s|--show-src          Also show source, not only dest
   -b|--bits              Show rates in bits/s instead of bytes/s
   -u|--update            Update GeoIP databases
   -t|--interval <time>   Refresh time in seconds (default 1s)
   -v|--version           Print version and exit
   -h|--help              Print this help and exit
 
 Examples:
   flowtop
   flowtop -46UTDISs
 
 Note:
   If netfilter is not running, you can activate it with e.g.:
    iptables -A INPUT -p tcp -m state --state ESTABLISHED -j ACCEPT
    iptables -A OUTPUT -p tcp -m state --state NEW,ESTABLISHED -j ACCEPT
 
 Please report bugs at https://github.com/netsniff-ng/netsniff-ng/issues
 Copyright (C) 2011-2013 Daniel Borkmann <dborkma@tik.ee.ethz.ch>
 Copyright (C) 2011-2012 Emmanuel Roullit <emmanuel.roullit@gmail.com>
 Swiss federal institute of technology (ETH Zurich)
 License: GNU GPL version 2.0
 This is free software: you are free to change and redistribute it.
 There is NO WARRANTY, to the extent permitted by law.
 ```
 
 - - -
 
 ##### ifpps
 
 Top-like networking and system statistics
 
 ```
 root@kali:~# ifpps -h
 ifpps 0.6.8, top-like kernel networking and system statistics
 http://www.netsniff-ng.org
 
 Usage: ifpps [options] || ifpps <netdev>
 Options:
   -d|--dev <netdev>      Device to fetch statistics for e.g., eth0
   -n|--num-cpus <num>    Number of top hitter CPUs in ncurses mode (def: 5)
   -t|--interval <time>   Refresh time in ms (default 1000 ms)
   -c|--csv               Output to terminal as Gnuplot-ready data
   -l|--loop              Continuous CSV output
   -m|--median            Display median values
   -o|--omit-header       Do not print the CSV header
   -p|--promisc           Promiscuous mode
   -P|--percentage        Show percentage of theoretical line rate
   -W|--no-warn           Suppress warnings
   -v|--version           Print version and exit
   -h|--help              Print this help and exit
 
 Examples:
   ifpps eth0
   ifpps -pd eth0
   ifpps -lpcd wlan0 > plot.dat
 
 Note:
   On 10G cards, RX/TX statistics are usually accumulated each > 1sec.
   Thus, in those situations, it's good to use a -t of 10sec.
 
 Please report bugs at https://github.com/netsniff-ng/netsniff-ng/issues
 Copyright (C) 2009-2013 Daniel Borkmann <dborkma@tik.ee.ethz.ch>
 Swiss federal institute of technology (ETH Zurich)
 Copyright (C) 2013 Tobias Klauser <tklauser@distanz.ch>
 License: GNU GPL version 2.0
 This is free software: you are free to change and redistribute it.
 There is NO WARRANTY, to the extent permitted by law.
 ```
 
 - - -
 
 ##### mausezahn
 
 A fast versatile packet generator with Cisco-cli
 
 ```
 root@kali:~# mausezahn -h
 
 mausezahn 0.6.8, a fast versatile traffic generator
 http://www.netsniff-ng.org
 
 Usage: mausezahn [options] [interface] <keyword>|<arg-string>|<hex-string>
 Options:
   -x <port>             Interactive mode with telnet CLI, default port: 25542
   -l <ip>               Listen address to bind to when in interactive mode, default: 0.0.0.0
   -4                    IPv4 mode (default)
   -6                    IPv6 mode
   -R <PRIO>             Set socket priority
   -c <count>            Send packet count times, default:1, infinite:0
   -d <delay>            Apply delay between transmissions. The delay value can be
                         specified in usec (default, no additional unit needed), or in
                         msec (e.g. 100m or 100msec), or in seconds (e.g. 100s or 100sec)
   -r                    Multiplies the specified delay with a random value
   -p <length>           Pad the raw frame to specified length (using random bytes)
   -a <srcmac|keyword>   Use specified source mac address, no matter what has
                         been specified with other arguments; keywords see below,
                         Default is own interface
   -b <dstmac|keyword>   Same with destination mac address; keywords:
      rand               Use a random MAC address
      bc                 Use a broadcast MAC address
      own                Use own interface MAC address (default for source MAC)
      stp                Use IEEE 802.1d STP multicast address
      cisco              Use Cisco multicast address as used for CDP, VTP, or PVST+
   -A <srcip>            Use specified source IP address (default is own interface IP)
   -B <dstip|dnsname>    Send packet to specified destination IP or domain name
   -P <ascii payload>    Use the specified ASCII payload
   -f <filename>         Read the ASCII payload from a file
   -F <filename>         Read the hexadecimal payload from a file
   -Q <[CoS:]vlan>       Specify 802.1Q VLAN tag and optional Class of Service, you can
                         specify multiple 802.1Q VLAN tags (QinQ...) by separating them
                         via a comma or a period (e.g. '5:10,20,2:30')
   -t <packet-type|help> Specify packet type for autobuild (you don't need to care for
                         encapsulations in lower layers, most packet types allow/require
                         additional packet-specific arguments in an <arg-string>;
                         Currently supported types: arp, bpdu, cdp, ip, icmp, udp, tcp,
                         dns, rtp, syslog, lldp and more;
                         For context-help use 'help' as <arg-string>!
   -T <packet-type>      Specify packet type for server mode, currently only rtp is supported;
                         Enter -T help or -T rtp help for further information
   -M <MPLS-label>       Insert a MPLS label, enter '-M help' for a syntax description
   -V|VV|...             Verbose and more verbose mode
   -q                    Quiet mode, even omit 'important' standard short messages
   -S                    Simulation mode: DOES NOT put anything on the wire, this is
                         typically combined with one of the verbose modes (v or V)
   -v                    Show version
   -h                    Print this help
 
 Examples:
   mausezahn -x 99
   mausezahn -c 0 -d 2s -t bpdu conf
   mausezahn -t cdp change -c 0
   mausezahn -t syslog sev=3 -P "You have been mausezahned." -A 10.1.1.109 -B 192.168.7.7
   mausezahn eth0 -A rand -B 1.1.1.1 -c 0 -t tcp "dp=1-1023, flags=syn"
 
 Note:
   This tool is targeted for network developers! You should
   be aware of what you are doing and what these options above
   mean! Only use this tool in an isolated LAN that you own!
 
 Please report bugs to <bugs@netsniff-ng.org>
 Copyright (C) 2008-2010 Herbert Haas <herbert@perihel.at>,
 Copyright (C) 2011 Daniel Borkmann <dborkma@tik.ee.ethz.ch>,
 Swiss federal institute of technology (ETH Zurich)
 License: GNU GPL version 2.0
 This is free software: you are free to change and redistribute it.
 There is NO WARRANTY, to the extent permitted by law.
 
 ```
 
 - - -
 
 ##### netsniff-ng
 
 The packet sniffing beast
 
 ```
 root@kali:~# netsniff-ng -h
 netsniff-ng 0.6.8, the packet sniffing beast
 http://www.netsniff-ng.org
 
 Usage: netsniff-ng [options] [filter-expression]
 Options:
   -i|-d|--dev|--in <dev|pcap|->  Input source as netdev, pcap or pcap stdin
   -o|--out <dev|pcap|dir|cfg|->  Output sink as netdev, pcap, directory, trafgen, or stdout
   -C|--fanout-group <id>         Join packet fanout group
   -K|--fanout-type <type>        Apply fanout discipline: hash|lb|cpu|rnd|roll|qm
   -L|--fanout-opts <opts>        Additional fanout options: defrag|roll
   -f|--filter <bpf-file|-|expr>  Use BPF filter from bpfc file/stdin or tcpdump-like expression
   -t|--type <type>               Filter for: host|broadcast|multicast|others|outgoing
   -F|--interval <size|time>      Dump interval if -o is a dir: <num>KiB/MiB/GiB/s/sec/min/hrs
   -R|--rfraw                     Capture or inject raw 802.11 frames
   -n|--num <0|uint>              Number of packets until exit (def: 0)
   -P|--prefix <name>             Prefix for pcaps stored in directory
   -O|--overwrite <N>             Limit the number of pcaps to N (file names use numbers 0 to N-1)
   -T|--magic <pcap-magic>        Pcap magic number/pcap format to store, see -D
   -w|--cooked                    Use Linux "cooked" header instead of link header
   -D|--dump-pcap-types           Dump pcap types and magic numbers and quit
   -B|--dump-bpf                  Dump generated BPF assembly
   -r|--rand                      Randomize packet forwarding order (dev->dev)
   -M|--no-promisc                No promiscuous mode for netdev
   -A|--no-sock-mem               Don't tune core socket memory
   -N|--no-hwtimestamp            Disable hardware time stamping
   -m|--mmap                      Mmap(2) pcap file I/O, e.g. for replaying pcaps
   -G|--sg                        Scatter/gather pcap file I/O
   -c|--clrw                      Use slower read(2)/write(2) I/O
   -S|--ring-size <size>          Specify ring size to: <num>KiB/MiB/GiB
   -k|--kernel-pull <uint>        Kernel pull from user interval in us (def: 10us)
   -J|--jumbo-support             Support replay/fwd 64KB Super Jumbo Frames (def: 2048B)
   -b|--bind-cpu <cpu>            Bind to specific CPU
   -u|--user <userid>             Drop privileges and change to userid
   -g|--group <groupid>           Drop privileges and change to groupid
   -H|--prio-high                 Make this high priority process
   -Q|--notouch-irq               Do not touch IRQ CPU affinity of NIC
   -s|--silent                    Do not print captured packets
   -q|--less                      Print less-verbose packet information
   -X|--hex                       Print packet data in hex format
   -l|--ascii                     Print human-readable packet data
   -U|--update                    Update GeoIP databases
   -V|--verbose                   Be more verbose
   -v|--version                   Show version and exit
   -h|--help                      Guess what?!
 
 Examples:
   netsniff-ng --in eth0 --out dump.pcap -s -T 0xa1b2c3d4 --bind-cpu 0 tcp or udp
   netsniff-ng --in wlan0 --rfraw --out dump.pcap --silent --bind-cpu 0
   netsniff-ng --in dump.pcap --mmap --out eth0 -k1000 --silent --bind-cpu 0
   netsniff-ng --in dump.pcap --out dump.cfg --silent --bind-cpu 0
   netsniff-ng --in dump.pcap --out dump2.pcap --silent tcp
   netsniff-ng --in eth0 --out eth1 --silent --bind-cpu 0 -J --type host
   netsniff-ng --in eth1 --out /opt/probe/ -s -m --interval 100MiB -b 0
   netsniff-ng --in vlan0 --out dump.pcap -c -u `id -u bob` -g `id -g bob`
   netsniff-ng --in any --filter http.bpf --jumbo-support --ascii -V
 
 Note:
   For introducing bit errors, delays with random variation and more
   while replaying pcaps, make use of tc(8) with its disciplines (e.g. netem).
 
 Please report bugs at https://github.com/netsniff-ng/netsniff-ng/issues
 Copyright (C) 2009-2013 Daniel Borkmann <dborkma@tik.ee.ethz.ch>
 Copyright (C) 2009-2012 Emmanuel Roullit <emmanuel.roullit@gmail.com>
 Copyright (C) 2012 Markus Amend <markus@netsniff-ng.org>
 Swiss federal institute of technology (ETH Zurich)
 License: GNU GPL version 2.0
 This is free software: you are free to change and redistribute it.
 There is NO WARRANTY, to the extent permitted by law.
 ```
 
 - - -
 
 ##### trafgen
 
 A fast, multithreaded network packet generator
 
 ```
 root@kali:~# trafgen -h
 trafgen 0.6.8, multithreaded zero-copy network packet generator
 http://www.netsniff-ng.org
 
 Usage: trafgen [options] [packet]
 Options:
   -i|-c|--in|--conf <cfg/->             Packet configuration file/stdin
   -o|-d|--out|--dev <netdev|.cfg|.pcap> Networking device or configuration file i.e., eth0
   -p|--cpp                              Run packet config through C preprocessor
   -D|--define                           Add macro/define for C preprocessor
   -J|--jumbo-support                    Support 64KB super jumbo frames (def: 2048B)
   -R|--rfraw                            Inject raw 802.11 frames
   -s|--smoke-test <ipv4>                Probe if machine survived fuzz-tested packet
   -n|--num <uint>                       Number of packets until exit (def: 0)
   -r|--rand                             Randomize packet selection (def: round robin)
   -P|--cpus <uint>                      Specify number of forks(<= CPUs) (def: #CPUs)
   -t|--gap <time>                       Set approx. interpacket gap (s/ms/us/ns, def: us)
   -b|--rate <rate>                      Send traffic at specified rate (pps/B/kB/MB/GB/kbit/Mbit/Gbit/KiB/MiB/GiB)
   -S|--ring-size <size>                 Manually set mmap size (KiB/MiB/GiB)
   -E|--seed <uint>                      Manually set srand(3) seed
   -u|--user <userid>                    Drop privileges and change to userid
   -g|--group <groupid>                  Drop privileges and change to groupid
   -H|--prio-high                        Make this high priority process
   -A|--no-sock-mem                      Don't tune core socket memory
   -Q|--notouch-irq                      Do not touch IRQ CPU affinity of NIC
   -q|--qdisc-path                       Enable qdisc kernel path (default off since 3.14)
   -V|--verbose                          Be more verbose
   -C|--no-cpu-stats                     Do not print CPU time statistics on exit
   -v|--version                          Show version and exit
   -e|--example                          Show built-in packet config example
   -h|--help                             Guess what?!
 
 Examples:
   trafgen --dev eth0 --conf trafgen.cfg
   trafgen -e | trafgen -i - -o eth0 --cpp -n 1
   trafgen --dev eth0 --conf fuzzing.cfg --smoke-test 10.0.0.1
   trafgen --dev wlan0 --rfraw --conf beacon-test.txf -V --cpus 2
   trafgen --dev eth0 --conf frag_dos.cfg --rand --gap 1000us
   trafgen --dev eth0 --conf icmp.cfg --rand --num 1400000 -k1000
   trafgen --dev eth0 --conf tcp_syn.cfg -u `id -u bob` -g `id -g bob`
   trafgen --dev eth0 '{ fill(0xff, 6), 0x00, 0x02, 0xb3, rnd(3), c16(0x0800), fill(0xca, 64) }'
 
 Arbitrary packet config examples (e.g. trafgen -e > trafgen.cfg):
   Run packet on  all CPUs:              { fill(0xff, 64) csum16(0, 64) }
   Run packet only on CPU1:    cpu(1):   { rnd(64), 0b11001100, 0xaa }
   Run packet only on CPU1-2:  cpu(1-2): { drnd(64),'a',csum16(1, 8),'b',42 }
 
 Generate config files from existing pcap using netsniff-ng:
   netsniff-ng --in dump.pcap --out dump.cfg
 
 Note:
   Smoke/fuzz test example: machine A, 10.0.0.2 (trafgen) is directly
   connected to machine B (test kernel), 10.0.0.1. If ICMP reply fails
   we assume the kernel crashed, thus we print the packet and quit.
   In case you find a ping-of-death, please mention trafgen in your
   commit message of the fix!
 
   For introducing bit errors, delays with random variation and more,
   make use of tc(8) with its different disciplines, i.e. netem.
 
   For generating different package distributions, you can use scripting
   to generate a trafgen config file with packet ratios as:
 
      IMIX             64:7,  570:4,  1518:1
      Tolly            64:55,  78:5,   576:17, 1518:23
      Cisco            64:7,  594:4,  1518:1
      RPR Trimodal     64:60, 512:20, 1518:20
      RPR Quadrimodal  64:50, 512:15, 1518:15, 9218:20
 
 Please report bugs at https://github.com/netsniff-ng/netsniff-ng/issues
 Copyright (C) 2011-2013 Daniel Borkmann <dborkma@tik.ee.ethz.ch>,
 Swiss federal institute of technology (ETH Zurich)
 License: GNU GPL version 2.0
 This is free software: you are free to change and redistribute it.
 There is NO WARRANTY, to the extent permitted by law.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
