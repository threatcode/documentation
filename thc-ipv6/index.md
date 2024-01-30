---
Title: thc-ipv6
Homepage: http://www.thc.org/thc-ipv6/
Repository: https://salsa.debian.org/pkg-security-team/thc-ipv6
Architectures: linux-any
Version: 3.8-1
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-information-gathering 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### thc-ipv6
 
  Attack toolkit for testing IPv6 and ICMPv6 protocol weaknesses.
   
  Some of the tools included:
   
  alive6: an effective alive scanning.
   
  denial6: try a collection of denial-of-service tests against a
  target.
   
  detect-new-ip6: detect new ip6 devices which join the network.
   
  dnsdict6: parallelized dns ipv6 dictionary bruteforcer.
   
  dos-new-ip6: detect new ip6 devices and tell them that their chosen
  IP collides on the network (DOS).
   
  exploit6: test known ipv6 vulnerabilities against a target.
   
  fake_mld6: announce yourself in a multicast group of your choice on
  the net.
   
  fake_router6: announce yourself as a router on the network.
   
  flood_advertise6: flood a target with random neighbor advertisements.
   
  flood_router6: flood a target with random router advertisements.
   
  implementation6: performs various implementation checks on ipv6.
   
  parasite6: icmp neighbor solitication/advertisement spoofer.
   
  redir6: redirect traffic to you intelligently (man-in-the-middle)
  with a clever icmp6 redirect spoofer.
   
  rsmurf6: remote smurfer (known to work only against Linux at the
  moment).
   
  thcping6: sends a hand crafted ping6 packet.
   
  toobig6: mtu decreaser with the same intelligence as redir6.
 
 **Installed size:** `3.66 MB`  
 **How to install:** `sudo apt install thc-ipv6`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libnetfilter-queue1 
 * libpcap0.8 
 * libssl3 
 {{< /spoiler >}}
 
 ##### atk6-address6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-address6 -h
 atk6-address6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax:
 	atk6-address6 mac-address [ipv6-prefix]
 	atk6-address6 ipv4-address [ipv6-prefix]
 	atk6-address6 ipv6-address
 
 Converts a mac or IPv4 address to an IPv6 address (link local if no prefix is
 given as 2nd option) or, when given an IPv6 address, prints the mac or IPv4
 address. Prints all possible variations. Returns -1 on errors or the number of
 variations found
 ```
 
 - - -
 
 ##### atk6-alive6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-alive6 -h
 atk6-alive6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-alive6 [-CFHLMPSdlpvV] [-I srcip6] [-i file] [-o file] [-e opt] [-s port,..] [-a port,..] [-u port,..] [-T tag] [-W TIME] interface [unicast-or-multicast-address [remote-router]]
 
 Options:
  Output Options:
   -i file    check systems from input file
   -o file    write results to output file
   -v         verbose information (twice: detailed, thrice: dumping packets)
   -d         DNS resolve alive IPv6 addresses
  Enumerate Options:
   -M         enumerate hardware addresses (MAC) from input addresses (slow!)
   -C         enumerate common addresses of input networks, -CC for large scan
   -4 ipv4/range  test various IPv4 address encodings per network (eg 1.2.3.4/24)
  Alive Technique Options:
   -p         send a ping packet for alive check (default)
   -e dst,hop send an errornous packets: destination (default), hop-by-hop
   -s port,port,..  TCP-SYN packet to ports for alive check or "portscan"
   -a port,port,..  TCP-ACK packet to ports for alive check
   -u port,port,..  UDP packet to ports for alive check
   -F         firewall mode: -p -e dst -u 53 -s 22,25,80,443,9511 -a 9511
  Sending Options
   -n number  how often to send each packet (default: local 1, remote 2)
   -W time    time in ms to wait after sending a packet (default: 1)
   -S         slow mode, get best router for each remote target or when proxy-NA
   -I src[/mask]  use the specified IPv6 address as source. Use mask for random.
   -l         use link-local address for multicast addresses instead of global
   -P         only print addresses that would be scanned, no packets are sent!
   -m         raw mode (for network adapters where you do not have Ethernet)
  Help Options:
   -hh        show even more options
 
 Target address on command line or in input file can include ranges in the form
 of 2001:db8::1-fff or 2001:db8::1-2:0-ffff:0:0-ffff, etc.
 Do not use the ranges (from-to) option with -M, -C or -4.
 If you use SYN packets (-s/-F option), automatic OS detection is performed.
 Returns -1 on errors, 0 if a system was found alive or 1 if nothing was found.
 ```
 
 - - -
 
 ##### atk6-connect6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-connect6 -h
 connect6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-connect6 [-a | -A type] [-i] target-ip target-port
 
 Options:
   -a       send Hop-by-Hop Router Alert option
   -A type  like -a but lets you define the alarmtype (number)
   -i       interactive mode (like telnet)
   -I       end a linefeed, wait for a string, print it
   -O       try TCP Fast Open connection
   -w ms    wait time for connect in ms (default: 1000)
   -p       ping mode
 You can supply a %interface identifier to the target-ip
 Returns 0 on successful connect, 1 on timeout/reset
 ```
 
 - - -
 
 ##### atk6-connsplit6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-connsplit6 -h
 splitconnect6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: [-vd] atk6-connsplit6 INTERFACE client|server
 
 Options:
   -v   verbose mode
   -d   debug mode
 
 Manipulates all incoming (client) or outgoing (server) TCP connections that are
 from (server) or to (client) port 64446, and sets a new destinatin (server) or
 source (client) address.
 The purpose of this is a proof of concept to make connect analysis difficult.
 It is recommended to use the splitconnect6.sh script to control this tool.
 ```
 
 - - -
 
 ##### atk6-covert_send6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-covert_send6 -h
 atk6-covert_send6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-covert_send6 [-m mtu] [-k key] [-s resend] interface target file [port]
 
 Options:
   -m mtu     specifies the maximum MTU (default: interface MTU, min: 1000)
   -k key     encrypt the content with Blowfish-160
   -s resend  send each packet RESEND number of times, default: 1
 
 Sends the content of FILE covertly to the target, And its POC - don't except
 too much sophistication - its just put into the destination header.
 ```
 
 - - -
 
 ##### atk6-covert_send6d
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-covert_send6d -h
 atk6-covert_send6d 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-covert_send6d [-k key] interface file
 
 Options:
   -k key     decrypt the content with Blowfish-160
 
 Writes covertly received content to FILE.
 ```
 
 - - -
 
 ##### atk6-denial6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-denial6 -h
 atk6-denial6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-denial6 interface destination test-case-number
 
 Performs various denial of service attacks on a target
 If a system is vulnerable, it can crash or be under heavy load, so be careful!
 The following test cases are currently implemented:
   1 : large hop-by-hop header with router-alert and filled with unknown options
   2 : large destination header filled with unknown options
   3 : hop-by-hop header with router alert option plus 180 headers
   4 : hop-by-hop header with router alert option plus 178 headers + ping
   5 : AH header + ping
   6 : first fragments of a ping with a hop-by-hop header with router alert
   7 : large hop-by-hop header filled with unknown options (no router alert)
 
 ```
 
 - - -
 
 ##### atk6-detect-new-ip6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-detect-new-ip6 -h
 atk6-detect-new-ip6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-detect-new-ip6 interface [script]
 
 This tools detects new IPv6 addresses joining the local network.
 If script is supplied, it is executed with the detected IPv6 address as first
 and the interface as second command line option.
 
 ```
 
 - - -
 
 ##### atk6-detect_sniffer6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-detect_sniffer6 -h
 atk6-detect_sniffer6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-detect_sniffer6 interface [target6]
 
 Tests if systems on the local LAN are sniffing.
 Works against Windows, Linux, OS/X and *BSD
 If no target is given, the link-local-all-nodes address is used, which
 however not always works.
 ```
 
 - - -
 
 ##### atk6-dnsdict6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-dnsdict6 -h
 atk6-dnsdict6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-dnsdict6 [-d4] [-s|-m|-l|-x|-u] [-t THREADS] [-D] domain [dictionary-file]
 
 Enumerates a domain for DNS entries, it uses a dictionary file if supplied
 or a built-in list otherwise. This tool is based on dnsmap by gnucitizen.org.
 
 Options:
  -4      do also dump IPv4 addresses
  -t NO   specify the number of threads to use (default: 8, max: 32).
  -D      dump the selected built-in wordlist, no scanning.
  -d      display IPv6 information on NS and MX DNS domain information.
  -e      ignore no NS for domain errors
  -S      perform SRV service name guessing
  -[smlxu] choose the dictionary size by -s(mall=100), -m(edium=1419) (DEFAULT)
            -l(arge=2601), -x(treme=5886) or -u(ber=16724)
 
 ```
 
 - - -
 
 ##### atk6-dnsrevenum6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-dnsrevenum6 -h
 atk6-dnsrevenum6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-dnsrevenum6 [-t] dns-server ipv6address
 
 Performs a fast reverse DNS enumeration and is able to cope with slow servers.
 Option -t enables TCP instead of UDP (use this if you get many timeouts)
 Examples:
   atk6-dnsrevenum6 dns.test.com 2001:db8:42a8::/48
   atk6-dnsrevenum6 -t dns.test.com 8.a.2.4.8.b.d.0.1.0.0.2.ip6.arpa
 ```
 
 - - -
 
 ##### atk6-dnssecwalk
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-dnssecwalk -h
 atk6-dnssecwalk 3.8 (c) 2020 by Marc Heuse <mh@mh-sec.de> http://www.mh-sec.de
 
 Syntax: atk6-dnssecwalk [-e46t] dns-server domain
 
 Options:
  -e  ensure that the domain is present in found addresses, quit otherwise
  -4  resolve found entries to IPv4 addresses
  -6  resolve found entries to IPv6 addresses
  -t  use TCP instead of UDP
 
 Perform DNSSEC NSEC walking.
 
 Example: atk6-dnssecwalk dns.test.com test.com
 ```
 
 - - -
 
 ##### atk6-dos-new-ip6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-dos-new-ip6 -h
 atk6-dos-new-ip6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-dos-new-ip6 [-S] interface
 
 This tools prevents new IPv6 interfaces to come up, by sending answers to
 duplicate ip6 checks (DAD). This results in a DOS for new IPv6 devices.
 
 Option -S sends conflicting NS query instead of NA reply, but it restricts
 source randomization.
 
 ```
 
 - - -
 
 ##### atk6-dump_dhcp6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-dump_dhcp6 -h
 atk6-dump_dhcp6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-dump_dhcp6 [-V vendorid] interface [target]
 
 Options:
   -V vendorid  send vendorid number,string (e.g. 11,test)
   -N           use fe80:: as source
   -n           use empty mac as source
 
 DHCPv6 information tool. Dumps the available servers and their setup.
 You can specify a specific DHCPv6 server as destination.
 ```
 
 - - -
 
 ##### atk6-dump_router6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-dump_router6 -h
 atk6-dump_router6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-dump_router6 interface [target]
 
 Dumps all local routers and their information
 
 ```
 
 - - -
 
 ##### atk6-exploit6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-exploit6 -h
 atk6-exploit6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-exploit6 interface destination [test-case-number]
 
 Performs exploits of various CVE known IPv6 vulnerabilities on the destination
 Note that for exploitable overflows only 'AAA...' strings are used.
 If a system is vulnerable, it will crash, so be careful!
 ```
 
 - - -
 
 ##### atk6-extract_hosts6
 
 (unknown subject)
 
 ```
 root@kali:~# man atk6-extract_hosts6
 THC-IPv6(8)                 System Manager's Manual                THC-IPv6(8)
 
 NAME
        The Hacker Choice's IPv6 Attack Toolkit (aka thc-ipv6)
 
 SYNOPSIS
        tool [options] ...
 
        DESCRIPTION
               This  manual  page briefly documents each of the attack-toolkit6
               tools. Not all options are listed here, to see the full list  of
               options of each tool please invoke them with -h.
 
               Note  that  on Debian (if you read this on Debian) command names
               are prefixed with atk6- , so for example the tool alive6  should
               be invoked as atk6-alive6.  This is a Debian-only modification.
 
        address6 <mac-address/ipv4-address/ipv6-address> [ipv6-prefix]
               Converts a mac or ipv4 address to an ipv6 address (link local if
               no  prefix  is  given  as 2nd option) or, when given an ipv6 ad-
               dress, prints the mac or ipv4 address. Prints all possible vari-
               ations. Returns -1 on errors or the number of variations found.
 
        alive6 <interface> [unicast-or-multicast-address [remote-router]]
               Shows alive addresses in the segment. If you  specify  a  remote
               router,  the  packets are sent with a routing header prefixed by
               fragmentation.
 
        covert_send6 <interface> <target> <file> [port]
               Sends the content of FILE covertly to the target.
 
        covert_send6d <interface> <file>
               Writes received covertly content to FILE.
 
        denial6 <interface> <destination> <test-case-number>
               Performs various denial of service attacks on a target.
 
        detect_sniffer6 <interface> [target-ip]
               Tests if systems on the local LAN are  sniffing.  Works  against
               Windows, Linux, OS/X and *BSD systems.
 
        dnssecwalk [-e46] <dns-server> <domain>
               Performs DNSSEC NSEC walking.
 
        dos_mld <interface>
               This  tools  prevents new ipv6 interfaces to come up, by sending
               answers to duplicate ip6 checks (DAD). This results in a DOS for
               new ipv6 devices.
 
        dos-new-ip6 <interface>
               This tools prevents new ipv6 interfaces to come up,  by  sending
               answers to duplicate ip6 checks (DAD). This results in a DOS for
               new ipv6 devices.
 
        detect-new-ip6 <interface> [scriptname]
               This tools detects new ipv6 addresses joining the local network.
               If scriptname is supplied, it is executed with the detected IPv6
               address as option.
 
        dnsdict6 [-t THREADS] <domain> [dictionary-file]
               Enumerates  a  domain for DNS entries, it uses a dictionary file
               if supplied or a built-in list otherwise.
 
        dnsrevenum6 <dns-server> <ipv6-address>
               Performs a fast reverse DNS enumeration.
 
        dump_router6 <interface>
               Dumps all local routers and their information.
 
        dump_dhcp6 <interface>
               Dumps all DHCPv6 servers and their information
 
        exploit6 <interface> <destination> [test-case-number]
               Performs exploits of various CVE known IPv6  vulnerabilities  on
               the destination.
 
        extract_hosts6 <file>
               Prints the host parts of ipv6 addresses in file.
 
        extract_networks6 <interface>
               Prints the networks found in file.
 
        fake_advertise6 <interface> <ip-address> [target-address [own-mac-ad-
        dress]]
               Advertise  ipv6  address on the network (with own mac if not de-
               fined) sending it to the all-nodes multicast address if no  tar-
               get specified.
 
        fake_dhcps6 <interface> <network-address/prefix-length> <dns-server>
               Fake  DHCPv6  server. Used to configure an address and set a DNS
               server.
 
        fake_dns6d <interface> <ipv6-address>
               Fake DNS server that serves the same IPv6 address to any  lookup
               request.
 
        fake_dnsupdate6 <dns-server> <fqdn> <ipv6-address>
               Send false DNS update requests.
 
        fake_mipv6 <interface> <home-address> <home-agent-address> <care-of-ad-
        dress>
               If  the mobile IPv6 home-agent is mis-configured to accept MIPV6
               updates without IPSEC, this will redirect all packets for  home-
               address to care-of-address.
 
        fake_mld6 <interface> <multicast-address> [[target-address] [[ttl]
        [[own-ip] [own-mac-address]]]]
               Advertise yourself in a multicast group of your choice.
 
        fake_mld26 [-l] <interface> <add|delete|query> [multicast-address [tar-
        get-address [ttl [own-ip [own-mac-address [destination-mac-ad-
        dress]]]]]]
               This uses the MLDv2 protocol. Only a subset of what the protocol
               is able to do is possible to implement via a command line.
 
        fake_mldrouter6 [-l] <interface> <advertise|solicitate|terminate> [own-
        ip [own-mac-address]]
               Announce, delete or solicitate MLD router - yourself or others.
 
        fake_pim6 [-t ttl] [-s src6] [-d dst6] <interface> {<hello> [dr_prior-
        ity]|{join|prune} <neighbor6> <multicast6> <target6>}
               The hello command takes optionally the DR priority (default: 0).
 
        fake_router6 <interface> <router-ip-link-local
               network-address/prefix-length>   <mtu>   [mac-address]  Announce
               yourself as a router and try to become the default router.  If a
               non-existing mac-address is supplied, this results in a DOS.
 
        fake_router26 <interface>
               Like fake_router6 with more options available.
 
        fake_solicitate6 <interface> <solicited-ip>
               Solicits IPv6 address on the network, sending  it  to  the  all-
               nodes multicast address.
 
        firewall6 [-u] <interface> <destination> <port> [test-case-no]
               Performs  various  ACL bypass attempts to check implementations.
               Defaults to TCP ports, option -u switches to UDP.  For all  test
               cases to work, ICMPv6 ping to the destination must be allowed.
 
        flood_advertise6 <interface>
               Flood the local network with neighbor advertisements.
 
        flood_dhcpc6 <interface> [domain-name]
               DHCP  client flooder. Use to deplete the IP address pool a DHCP6
               server is offering. Note: if the pool is  very  large,  this  is
               rather senseless.
 
        flood_mld6 <interface>
               Flood the local network with MLD reports.
 
        flood_mld26 <interface>
               Flood the local network with MLDv2 reports.
 
        flood_mldrouter6 <interface>
               Flood the local network with MLD router advertisements.
 
        flood_redir6 [-HFD] interface [target] [oldrouter [newrouter]]
               Flood a target with ICMPv6 redirects
 
        flood_router6 <interface>
               Flood the local network with router advertisements.
 
        flood_router26 <interface>
               Similar to flood_router6 but with more options available.
 
        flood_rs6 [-sS] interface [target]
               Flood a network with ICMPv6 router solicitation messages
 
        flood_solicitate6 <interface> [target-ip]
               Flood the network with neighbor solicitations.
 
        four2six [-FHD] [-s src6] interface ipv6-to-ipv4-gateway ipv4-src
        ipv4-dst [port]
               Send  (spoofed)  packets  over  a 4to6 tunnel (IPv4 packets over
               IPv6 networks)
 
        fragmentation6 <interface> <target-ip>
               Performs fragment firewall and implementation checks,  including
               denial-of-service.
 
        fuzz_ip6 [-x] [-t number | -T number] [-p number] [-IFSDHRJ]
        [-1|-2|-3|-4|-5|-6|-7] <interface> <unicast-or-multicast-address> [ad-
        dress-in-data-pkt]
               Fuzzes an icmp6 packet.
 
        fuzz_dhcpc6 [-1|-2|-3|-4|-5|-6|-7|-8|-9|-A|-B|-C|-D|-m] [-f mac] [-l
        link] [-v ipv6] [-x xid] [-c client] [-o options] interface
               Fuzzes messages sent to a DHCPv6 client.
 
        fuzz_dhcps6 [-t number | -T number] [-e number | -T number] [-p number]
        [-md] [-1|-2|-3|-4|-5|-6|-7|-8] interface [domain-name]
               Fuzzes  a  DHCPv6 server on specified packet types.  implementa-
               tion6 <interface> <destination> [test-case-number] Performs some
               ipv6 implementation checks, can be used to test firewalls too.
 
        implementation6d <interface>
               Identifies test packets by the implementation6 tool,  useful  to
               check what packets passed a firewall.
 
        inject_alive6 [-ap] <interface>
               This  tool answers to keep-alive requests on PPPoE and 6in4 tun-
               nels; for PPPoE0t also sends keep-alive requests.  Note that the
               appropriate environment variable THC_IPV6_{PPPOE|6IN4}  must  be
               set.   Option -a will actively send alive requests every 15 sec-
               onds.  Option -p will not send replies to alive requests.
 
        inverse_lookup6 <interface> <mac-address>
               Performs an inverse address query, to  get  the  IPv6  addresses
               that  are  assigned to a MAC address. Note that only few systems
               support this yet.
 
        kill_router6 <interface> <target-ip>
               Announce that target router is going down to delete it from  the
               routing tables. If you supply a '*' as target-ip, this tool will
               sniff the network for RAs and immediately send the kill packet.
 
        ndpexhaust26 <interface> [-acpPTUrR] [-s sourceip6] <target-network>
               Flood  the target /64 network with ICMPv6 TooBig error messages.
               This tool version is manyfold more effective  than  ndpexhaust6.
               -a       add  a hop-by-hop header with router alert.  -c      do
               not calculate the checksum to save time.   -p       send  ICMPv6
               Echo  Requests.   -P       send ICMPv6 Echo Reply.  -T      send
               ICMPv6 Time-to-live-exceeded.  -U      send  ICMPv6  Unreachable
               (no  route).  -r      randomize the source from your /64 prefix.
               -R      randomize the source fully.  -s sourceip6  use  this  as
               source ipv6 address.
 
        ndpexhaust6 <interface> <target-network>
               Randomly pings IPs in target network.
 
        node_query6 <interface> <target-ip>
               Sends  an  ICMPv6 node query request to the target and dumps the
               replies.
 
        parasite6 <interface> [fake-mac]
               This is an "ARP spoofer" for IPv6, redirecting all local traffic
               to your own system (or nirvana if fake-mac does  not  exist)  by
               answering  falsely to Neighbor Solicitation requests, specifying
               FAKE-MAC results in a local DOS.
 
        passive_discovery6 <interface> [scriptname]
               Passively sniffs the network and  dump  all  client's  IPv6  ad-
               dresses  detected.  If scriptname is supplied, it is called with
               the detected IPv6 address as first and the interface  as  second
               parameters.
 
        randicmp6 <interface> <target-ip>
               Sends all ICMPv6 type and code combinations to target.
 
        redir6 <interface> <src-ip> <target-ip> <original-router> <new-router>
        [new-router-mac]
               Implant a route into src-ip, which redirects all traffic to tar-
               get-ip  to  new-ip.  You must know the router which would handle
               the route.  If the new-router-mac does not exist,  this  results
               in a DOS.
 
        redirsniff6 <interface> <victim-ip> <destination-ip> <original-router>
        [<new-router> [new-router-mac]]
               Implant  a  route into victim-ip, which redirects all traffic to
               destination-ip to new-router. You must  know  the  router  which
               would  handle  the  route.  If the new-router and new-router-mac
               does not exist, this results in a DoS.
 
        rsmurf6 <interface> <victim-ip>
               Smurfs the local network of the victim. Note: this depends on an
               implementation error, currently only verified on Linux (fixed in
               current versions).  Evil: "ff02::1" as victim will DOS your  lo-
               cal LAN completely.
 
        smurf6 <interface> <victim-ip> [multicast-network-address]
               Smurf  the  target  with ICMPv6 echo replies. Target of echo re-
               quest is the local all-nodes multicast address if not specified.
 
        sendpees6 <interface> <key_length> <prefix> <victim-ip>
               Send SEND neighbor solicitation messages and make target to ver-
               ify a lota CGA and RSA signatures.
 
        sendpeesmp6 <interface> <key_length> <prefix> <victim-ip>
               Multithreaded version of sendpees6.
 
        trace6 [-d] <interface> targetaddress [port]
               A basic but very fast traceroute6 program.
 
        thcping6 <interface> <src6> <dst6> <srcmac> <dstmac> <data>
               Craft your special ICMPv6 echo request packet.
 
        thcsyn6 [-AcDrRS] [-p port] [-s source-ip6] <interface> <target> <port>
               Flood the target port with TCP-SYN packets. If you supply "x" as
               port, it is randomized.
 
        toobig6 <interface> <target-ip> <existing-ip> <mtu>
               Implants the specified mtu on the target
 
 SEE ALSO
        nmap(1), amap(1), dsniff(8).
 
 AUTHOR
        thc-ipv6 was written by van Hauser <vh@thc.org> / THC
 
        The homepage for this toolkit is: https://github.com/vanhauser-thc/thc-
        ipv6
 
        This manual page was written by Maykel Moya <mmoya@mmoya.org>  and  Ar-
        turo  Borrero Gonzalez <arturo@debian.org>, for the Debian project (but
        may be used by others). It's based on previous work by  Michael  Gebet-
        sroither <gebi@grml.org>.
 
 Summer 2015                     ATTACK-TOOLKIT6                    THC-IPv6(8)
 ```
 
 - - -
 
 ##### atk6-extract_networks6
 
 (unknown subject)
 
 ```
 root@kali:~# man atk6-extract_networks6
 THC-IPv6(8)                 System Manager's Manual                THC-IPv6(8)
 
 NAME
        The Hacker Choice's IPv6 Attack Toolkit (aka thc-ipv6)
 
 SYNOPSIS
        tool [options] ...
 
        DESCRIPTION
               This  manual  page briefly documents each of the attack-toolkit6
               tools. Not all options are listed here, to see the full list  of
               options of each tool please invoke them with -h.
 
               Note  that  on Debian (if you read this on Debian) command names
               are prefixed with atk6- , so for example the tool alive6  should
               be invoked as atk6-alive6.  This is a Debian-only modification.
 
        address6 <mac-address/ipv4-address/ipv6-address> [ipv6-prefix]
               Converts a mac or ipv4 address to an ipv6 address (link local if
               no  prefix  is  given  as 2nd option) or, when given an ipv6 ad-
               dress, prints the mac or ipv4 address. Prints all possible vari-
               ations. Returns -1 on errors or the number of variations found.
 
        alive6 <interface> [unicast-or-multicast-address [remote-router]]
               Shows alive addresses in the segment. If you  specify  a  remote
               router,  the  packets are sent with a routing header prefixed by
               fragmentation.
 
        covert_send6 <interface> <target> <file> [port]
               Sends the content of FILE covertly to the target.
 
        covert_send6d <interface> <file>
               Writes received covertly content to FILE.
 
        denial6 <interface> <destination> <test-case-number>
               Performs various denial of service attacks on a target.
 
        detect_sniffer6 <interface> [target-ip]
               Tests if systems on the local LAN are  sniffing.  Works  against
               Windows, Linux, OS/X and *BSD systems.
 
        dnssecwalk [-e46] <dns-server> <domain>
               Performs DNSSEC NSEC walking.
 
        dos_mld <interface>
               This  tools  prevents new ipv6 interfaces to come up, by sending
               answers to duplicate ip6 checks (DAD). This results in a DOS for
               new ipv6 devices.
 
        dos-new-ip6 <interface>
               This tools prevents new ipv6 interfaces to come up,  by  sending
               answers to duplicate ip6 checks (DAD). This results in a DOS for
               new ipv6 devices.
 
        detect-new-ip6 <interface> [scriptname]
               This tools detects new ipv6 addresses joining the local network.
               If scriptname is supplied, it is executed with the detected IPv6
               address as option.
 
        dnsdict6 [-t THREADS] <domain> [dictionary-file]
               Enumerates  a  domain for DNS entries, it uses a dictionary file
               if supplied or a built-in list otherwise.
 
        dnsrevenum6 <dns-server> <ipv6-address>
               Performs a fast reverse DNS enumeration.
 
        dump_router6 <interface>
               Dumps all local routers and their information.
 
        dump_dhcp6 <interface>
               Dumps all DHCPv6 servers and their information
 
        exploit6 <interface> <destination> [test-case-number]
               Performs exploits of various CVE known IPv6  vulnerabilities  on
               the destination.
 
        extract_hosts6 <file>
               Prints the host parts of ipv6 addresses in file.
 
        extract_networks6 <interface>
               Prints the networks found in file.
 
        fake_advertise6 <interface> <ip-address> [target-address [own-mac-ad-
        dress]]
               Advertise  ipv6  address on the network (with own mac if not de-
               fined) sending it to the all-nodes multicast address if no  tar-
               get specified.
 
        fake_dhcps6 <interface> <network-address/prefix-length> <dns-server>
               Fake  DHCPv6  server. Used to configure an address and set a DNS
               server.
 
        fake_dns6d <interface> <ipv6-address>
               Fake DNS server that serves the same IPv6 address to any  lookup
               request.
 
        fake_dnsupdate6 <dns-server> <fqdn> <ipv6-address>
               Send false DNS update requests.
 
        fake_mipv6 <interface> <home-address> <home-agent-address> <care-of-ad-
        dress>
               If  the mobile IPv6 home-agent is mis-configured to accept MIPV6
               updates without IPSEC, this will redirect all packets for  home-
               address to care-of-address.
 
        fake_mld6 <interface> <multicast-address> [[target-address] [[ttl]
        [[own-ip] [own-mac-address]]]]
               Advertise yourself in a multicast group of your choice.
 
        fake_mld26 [-l] <interface> <add|delete|query> [multicast-address [tar-
        get-address [ttl [own-ip [own-mac-address [destination-mac-ad-
        dress]]]]]]
               This uses the MLDv2 protocol. Only a subset of what the protocol
               is able to do is possible to implement via a command line.
 
        fake_mldrouter6 [-l] <interface> <advertise|solicitate|terminate> [own-
        ip [own-mac-address]]
               Announce, delete or solicitate MLD router - yourself or others.
 
        fake_pim6 [-t ttl] [-s src6] [-d dst6] <interface> {<hello> [dr_prior-
        ity]|{join|prune} <neighbor6> <multicast6> <target6>}
               The hello command takes optionally the DR priority (default: 0).
 
        fake_router6 <interface> <router-ip-link-local
               network-address/prefix-length>   <mtu>   [mac-address]  Announce
               yourself as a router and try to become the default router.  If a
               non-existing mac-address is supplied, this results in a DOS.
 
        fake_router26 <interface>
               Like fake_router6 with more options available.
 
        fake_solicitate6 <interface> <solicited-ip>
               Solicits IPv6 address on the network, sending  it  to  the  all-
               nodes multicast address.
 
        firewall6 [-u] <interface> <destination> <port> [test-case-no]
               Performs  various  ACL bypass attempts to check implementations.
               Defaults to TCP ports, option -u switches to UDP.  For all  test
               cases to work, ICMPv6 ping to the destination must be allowed.
 
        flood_advertise6 <interface>
               Flood the local network with neighbor advertisements.
 
        flood_dhcpc6 <interface> [domain-name]
               DHCP  client flooder. Use to deplete the IP address pool a DHCP6
               server is offering. Note: if the pool is  very  large,  this  is
               rather senseless.
 
        flood_mld6 <interface>
               Flood the local network with MLD reports.
 
        flood_mld26 <interface>
               Flood the local network with MLDv2 reports.
 
        flood_mldrouter6 <interface>
               Flood the local network with MLD router advertisements.
 
        flood_redir6 [-HFD] interface [target] [oldrouter [newrouter]]
               Flood a target with ICMPv6 redirects
 
        flood_router6 <interface>
               Flood the local network with router advertisements.
 
        flood_router26 <interface>
               Similar to flood_router6 but with more options available.
 
        flood_rs6 [-sS] interface [target]
               Flood a network with ICMPv6 router solicitation messages
 
        flood_solicitate6 <interface> [target-ip]
               Flood the network with neighbor solicitations.
 
        four2six [-FHD] [-s src6] interface ipv6-to-ipv4-gateway ipv4-src
        ipv4-dst [port]
               Send  (spoofed)  packets  over  a 4to6 tunnel (IPv4 packets over
               IPv6 networks)
 
        fragmentation6 <interface> <target-ip>
               Performs fragment firewall and implementation checks,  including
               denial-of-service.
 
        fuzz_ip6 [-x] [-t number | -T number] [-p number] [-IFSDHRJ]
        [-1|-2|-3|-4|-5|-6|-7] <interface> <unicast-or-multicast-address> [ad-
        dress-in-data-pkt]
               Fuzzes an icmp6 packet.
 
        fuzz_dhcpc6 [-1|-2|-3|-4|-5|-6|-7|-8|-9|-A|-B|-C|-D|-m] [-f mac] [-l
        link] [-v ipv6] [-x xid] [-c client] [-o options] interface
               Fuzzes messages sent to a DHCPv6 client.
 
        fuzz_dhcps6 [-t number | -T number] [-e number | -T number] [-p number]
        [-md] [-1|-2|-3|-4|-5|-6|-7|-8] interface [domain-name]
               Fuzzes  a  DHCPv6 server on specified packet types.  implementa-
               tion6 <interface> <destination> [test-case-number] Performs some
               ipv6 implementation checks, can be used to test firewalls too.
 
        implementation6d <interface>
               Identifies test packets by the implementation6 tool,  useful  to
               check what packets passed a firewall.
 
        inject_alive6 [-ap] <interface>
               This  tool answers to keep-alive requests on PPPoE and 6in4 tun-
               nels; for PPPoE0t also sends keep-alive requests.  Note that the
               appropriate environment variable THC_IPV6_{PPPOE|6IN4}  must  be
               set.   Option -a will actively send alive requests every 15 sec-
               onds.  Option -p will not send replies to alive requests.
 
        inverse_lookup6 <interface> <mac-address>
               Performs an inverse address query, to  get  the  IPv6  addresses
               that  are  assigned to a MAC address. Note that only few systems
               support this yet.
 
        kill_router6 <interface> <target-ip>
               Announce that target router is going down to delete it from  the
               routing tables. If you supply a '*' as target-ip, this tool will
               sniff the network for RAs and immediately send the kill packet.
 
        ndpexhaust26 <interface> [-acpPTUrR] [-s sourceip6] <target-network>
               Flood  the target /64 network with ICMPv6 TooBig error messages.
               This tool version is manyfold more effective  than  ndpexhaust6.
               -a       add  a hop-by-hop header with router alert.  -c      do
               not calculate the checksum to save time.   -p       send  ICMPv6
               Echo  Requests.   -P       send ICMPv6 Echo Reply.  -T      send
               ICMPv6 Time-to-live-exceeded.  -U      send  ICMPv6  Unreachable
               (no  route).  -r      randomize the source from your /64 prefix.
               -R      randomize the source fully.  -s sourceip6  use  this  as
               source ipv6 address.
 
        ndpexhaust6 <interface> <target-network>
               Randomly pings IPs in target network.
 
        node_query6 <interface> <target-ip>
               Sends  an  ICMPv6 node query request to the target and dumps the
               replies.
 
        parasite6 <interface> [fake-mac]
               This is an "ARP spoofer" for IPv6, redirecting all local traffic
               to your own system (or nirvana if fake-mac does  not  exist)  by
               answering  falsely to Neighbor Solicitation requests, specifying
               FAKE-MAC results in a local DOS.
 
        passive_discovery6 <interface> [scriptname]
               Passively sniffs the network and  dump  all  client's  IPv6  ad-
               dresses  detected.  If scriptname is supplied, it is called with
               the detected IPv6 address as first and the interface  as  second
               parameters.
 
        randicmp6 <interface> <target-ip>
               Sends all ICMPv6 type and code combinations to target.
 
        redir6 <interface> <src-ip> <target-ip> <original-router> <new-router>
        [new-router-mac]
               Implant a route into src-ip, which redirects all traffic to tar-
               get-ip  to  new-ip.  You must know the router which would handle
               the route.  If the new-router-mac does not exist,  this  results
               in a DOS.
 
        redirsniff6 <interface> <victim-ip> <destination-ip> <original-router>
        [<new-router> [new-router-mac]]
               Implant  a  route into victim-ip, which redirects all traffic to
               destination-ip to new-router. You must  know  the  router  which
               would  handle  the  route.  If the new-router and new-router-mac
               does not exist, this results in a DoS.
 
        rsmurf6 <interface> <victim-ip>
               Smurfs the local network of the victim. Note: this depends on an
               implementation error, currently only verified on Linux (fixed in
               current versions).  Evil: "ff02::1" as victim will DOS your  lo-
               cal LAN completely.
 
        smurf6 <interface> <victim-ip> [multicast-network-address]
               Smurf  the  target  with ICMPv6 echo replies. Target of echo re-
               quest is the local all-nodes multicast address if not specified.
 
        sendpees6 <interface> <key_length> <prefix> <victim-ip>
               Send SEND neighbor solicitation messages and make target to ver-
               ify a lota CGA and RSA signatures.
 
        sendpeesmp6 <interface> <key_length> <prefix> <victim-ip>
               Multithreaded version of sendpees6.
 
        trace6 [-d] <interface> targetaddress [port]
               A basic but very fast traceroute6 program.
 
        thcping6 <interface> <src6> <dst6> <srcmac> <dstmac> <data>
               Craft your special ICMPv6 echo request packet.
 
        thcsyn6 [-AcDrRS] [-p port] [-s source-ip6] <interface> <target> <port>
               Flood the target port with TCP-SYN packets. If you supply "x" as
               port, it is randomized.
 
        toobig6 <interface> <target-ip> <existing-ip> <mtu>
               Implants the specified mtu on the target
 
 SEE ALSO
        nmap(1), amap(1), dsniff(8).
 
 AUTHOR
        thc-ipv6 was written by van Hauser <vh@thc.org> / THC
 
        The homepage for this toolkit is: https://github.com/vanhauser-thc/thc-
        ipv6
 
        This manual page was written by Maykel Moya <mmoya@mmoya.org>  and  Ar-
        turo  Borrero Gonzalez <arturo@debian.org>, for the Debian project (but
        may be used by others). It's based on previous work by  Michael  Gebet-
        sroither <gebi@grml.org>.
 
 Summer 2015                     ATTACK-TOOLKIT6                    THC-IPv6(8)
 ```
 
 - - -
 
 ##### atk6-fake_advertise6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-fake_advertise6 -h
 atk6-fake_advertise6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-fake_advertise6 [-DHF] [-Ors] [-n count] [-w seconds] interface ip-address-advertised [target-address [mac-address-advertised [source-ip-address]]]
 
 Advertise IPv6 address on the network (with own mac if not specified),
 sending it to the all-nodes multicast address if no target address is set.
 Source ip address is the address advertised if not set.
 
 Sending options:
   -n count    send how many packets (default: forever)
   -w seconds  wait time between the packets sent (default: 5)
   -m srcmac   the srcmac address to send from (not what is advertised!
 Flag options:
   -O  do NOT set the override flag (default: on)
   -r  DO set the router flag (default: off)
   -s  DO set the solicitate flag (default: off)
 ND Security evasion options (can be combined):
   -F  full evasion attack (no other evasion options allowed)
   -H  add a hop-by-hop header
   -f  add a one shot fragment header (can be specified multiple times)
   -D  add a large destination header which fragments the packet.
 ```
 
 - - -
 
 ##### atk6-fake_dhcps6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-fake_dhcps6 -h
 atk6-fake_dhcps6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-fake_dhcps6 interface network-address/prefix-length dns-server [dhcp-server-ip-address [mac-address]]
 
 Fake DHCPv6 server. Use to configure an address and set a DNS server
 ```
 
 - - -
 
 ##### atk6-fake_dns6d
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-fake_dns6d -h
 atk6-fake_dns6d 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-fake_dns6d interface ipv6-address [fake-ipv6-address [fake-mac]]
 Fake DNS server that serves the same IPv6 address to any lookup request
 You can use this together with parasite6 if clients have a fixed DNS server
 Note: very simple server. Does not honor multiple queries in a packet, norNS, MX, etc. lookups.
 ```
 
 - - -
 
 ##### atk6-fake_dnsupdate6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-fake_dnsupdate6 -h
 atk6-fake_dnsupdate6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-fake_dnsupdate6 dns-server full-qualified-host-dns-name ipv6address
 
 Example: atk6-fake_dnsupdate6 dns.test.com myhost.sub.test.com ::1
 
 ```
 
 - - -
 
 ##### atk6-fake_mipv6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-fake_mipv6 -h
 atk6-fake_mipv6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-fake_mipv6 interface home-address home-agent-address care-of-address
 
 If the mobile IPv6 home-agent is mis-configured to accept MIPV6 updates without
 IPSEC, this will redirect all packets for home-address to care-of-address
 ```
 
 - - -
 
 ##### atk6-fake_mld26
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-fake_mld26 -h
 atk6-fake_mld26 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-fake_mld26 [-l] interface add|delete|query [multicast-address [target-address-to-subscribe-from [ttl [own-ip [own-mac-address [destination-mac-address]]]]]]
 
 This uses the MLDv2 protocol. Only a subset of what the protocol is able to
 do is possible to implement via a command line. Code it if you need something.
 Ad(d)vertise or delete yourself - or anyone you want - in a multicast group of your choice
 Query ask on the network who is listening to multicast addresses
 Use -l to loop and send (in 5s intervals) until Control-C is pressed.
 ```
 
 - - -
 
 ##### atk6-fake_mld6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-fake_mld6 -h
 atk6-fake_mld6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-fake_mld6 [-l] interface add|delete|query [multicast-address [ttl [own-ip [own-mac-address [destination-mac-address]]]]]
 
 Ad(d)vertise or delete yourself - or anyone you want - in a multicast group of your choice
 Query ask on the network who is listening to multicast addresses
 Use -l to loop and send (in 5s intervals) until Control-C is pressed.
 ```
 
 - - -
 
 ##### atk6-fake_mldrouter6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-fake_mldrouter6 -h
 atk6-fake_mldrouter6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-fake_mldrouter6 [-l] interface advertise|solicitate|terminate [own-ip [own-mac-address]]
 
 Announce, delete or soliciated MLD router - sourself or others.
 Use -l to loop and send (in 5s intervals) until Control-C is pressed.
 ```
 
 - - -
 
 ##### atk6-fake_pim6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-fake_pim6 -h
 atk6-fake_pim6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax:
   atk6-fake_pim6 [-l|-f] [-t ttl] [-s src6] [-d dst6] interface hello [dr_priority]
   atk6-fake_pim6 [-l|-f] [-t ttl] [-s src6] [-d dst6] interface bootstrap bsr6 [bsr_prio [rp6]]
   atk6-fake_pim6 [-l|-f] [-t ttl] [-s src6] [-d dst6] interface assert multicast6 [metric [sender6]]
   atk6-fake_pim6 [-l|-f] [-t ttl] [-s src6] [-d dst6] interface join|prune neighbor6 multicast6 target6
 
 Options:
   -l       loop packet every 5 seconds
   -f       flood packet (with random values where useful, e.g src)
   -t ttl   specify a non-standard ttl
   -s src6  specify the source IPv6 address
   -d dst6  specify a non-standard destination IPv6 address
 
 The hello command takes optionally the DR priority (default: 0).
 The join and prune commands need the multicast group to modify, the target
 address that joins or leavs and the neighbor PIM router
 The bootstrap command needs the bootstraprouter address and optional its
 priority and the rendevouz-point.
 The assert command needs the concerning multicast address and optional its
 metric and multicast sender.
 ```
 
 - - -
 
 ##### atk6-fake_router26
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-fake_router26 -h
 atk6-fake_router26 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-fake_router26 [-E type] [-A network/prefix] [-R network/prefix] [-D dns-server] [-s sourceip] [-S sourcemac] [-ardl seconds] [-Tt ms] [-n no] [-i interval] interface [target]
 
 Options:
  -A network/prefix  add autoconfiguration network (up to 16 times)
  -a seconds         valid lifetime of prefix -A (defaults to 99999)
  -R network/prefix  add a route entry (up to 16 times)
  -r seconds         route entry lifetime of -R (defaults to 4096)
  -D dns-server      specify a DNS server (up to 16 times)
  -L searchlist      specify the DNS domain search list, separate entries with ,
  -d seconds         dns entry lifetime of -D (defaults to 4096
  -M mtu             the MTU to send, defaults to the interface setting
  -s sourceip        the source ip of the router, defaults to your link local
  -S sourcemac       the source mac of the router, defaults to your interface
  -f ethernetmac     the ethernet mac address to use to send the frames
  -l seconds         router lifetime (defaults to 2048)
  -T ms              reachable timer (defaults to 0)
  -t ms              retrans timer (defaults to 0)
  -p priority        priority "low", "medium", "high" (default), "reserved"
  -F flags           Set one or more of the following flags: managed, other,
                     homeagent, proxy, reserved; separate by comma
  -E type            Router Advertisement Guard Evasion option. Types: 
      F              full evasion (Windows and FreeBSD)
      H              simple hop-by-hop header
      1              simple one-shot fragmentation header (can add multiple)
      D              insert a large destination header so that it fragments
      O              overlapping fragments for keep-first targets (Win, BSD, Mac)
      o              overlapping fragments for keep-last targets (Linux, Solaris)
                     Examples: -E H111, -E D
  -m mac-address     if only one machine should receive the RAs (not with -E DoO)
  -i interval        time between RA packets (default: 5)
  -n number          number of RAs to send (default: unlimited)
  -X                 clean up by de-announcing fake router (default: disabled)
 
 Announce yourself as a router and try to become the default router.
 If a non-existing link-local or mac address is supplied, this results in a DOS.
 ```
 
 - - -
 
 ##### atk6-fake_router6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-fake_router6 -h
 atk6-fake_router6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-fake_router6 [-HFD] interface network-address/prefix-length [dns-server [router-ip-link-local [mtu [mac-address]]]]
 
 Announce yourself as a router and try to become the default router.
 If a non-existing link-local or mac address is supplied, this results in a DOS.
 Option -H adds hop-by-hop, -F fragmentation header and -D dst header.
 ```
 
 - - -
 
 ##### atk6-fake_solicitate6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-fake_solicitate6 -h
 atk6-fake_solicitate6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-fake_solicitate6 [-DHF] interface ip-address-solicitated [target-address [mac-address-solicitated [source-ip-address]]]
 
 Solicate IPv6 address on the network, sending it to the all-nodes multicast address
 ```
 
 - - -
 
 ##### atk6-firewall6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-firewall6 -h
 atk6-firewall6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-firewall6 [-Hu] interface destination port [test-case-no]
 
 Performs various ACL bypass attempts to check implementations.
 Defaults to TCP ports, option -u switches to UDP.
 Option -H prints the hop count.
 For all test cases to work, ICMPv6 ping to the destination must be allowed.
 ```
 
 - - -
 
 ##### atk6-flood_advertise6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-flood_advertise6 -h
 atk6-flood_advertise6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-flood_advertise6 [-k | -m mac] interface [target]
 
 Flood the local network with neighbor advertisements.
 Option -k sends with your real src mac, -m with a specified src mac, random for each packet otherwise.
 ```
 
 - - -
 
 ##### atk6-flood_dhcpc6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-flood_dhcpc6 -h
 atk6-flood_dhcpc6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-flood_dhcpc6 [-n|-N] [-1] [-d domain-name] interface [dhcpserver]
 
 DHCP client flooder. Use to deplete the IP address pool a DHCP6 server is
 offering. Note: if the pool is very large, this is rather senseless. :-)
 
 By default the link-local IP MAC address is random, however this won't work
 in some circumstances. -n will use the real MAC, -N the real MAC and
 link-local address. -1 will only solicate an address but not request it.
 If -N is not used, you should run parasite6 in parallel.
 Use -d to force DNS updates, you must specify a domain name.
 ```
 
 - - -
 
 ##### atk6-flood_mld26
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-flood_mld26 -h
 atk6-flood_mld26 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-flood_mld26 interface [target] [max_count]
 
 Flood the local network with MLDv2 reports.
 ```
 
 - - -
 
 ##### atk6-flood_mld6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-flood_mld6 -h
 atk6-flood_mld6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-flood_mld6 interface [target]
 
 Flood the local network with MLD reports.
 ```
 
 - - -
 
 ##### atk6-flood_mldrouter6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-flood_mldrouter6 -h
 atk6-flood_mldrouter6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-flood_mldrouter6 interface [target]
 
 Flood the local network with MLD router advertisements.
 ```
 
 - - -
 
 ##### atk6-flood_redir6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-flood_redir6 -h
 atk6-flood_redir6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-flood_redir6 [-HFD] interface [target] [oldrouter [newrouter]]
 
 Flood the local network with ICMPv6 redirect packets.
 -F/-D/-H add fragment/destination/hopbyhop header to bypass simple filters
 -a adds hopbyhop with router alert
 ```
 
 - - -
 
 ##### atk6-flood_router26
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-flood_router26 -h
 atk6-flood_router26 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-flood_router26 [-HFD] [-sSG] [-RPA] interface [target]
 
 Flood the local network with router advertisements.
 Each packet contains ~25 prefix and route enries
 Modes:
   default  sends both routing entries and prefix information
   -R       does only send routing entries, no prefix information
   -P       does only send prefix information, no routing entries
   -A       an attack to disable privacy extensions
 Options:
   -a       add a hopbyhop header with router alert
   -H       add a hopbyhop header to bypass RA guard security
   -f       add an atomic fragment header to bypass RA guard security
   -D       add a large destination header to bypass RA guard security
   -F       perform full RA guard evasion (disallows all other bypass options)
   -s       use small lifetimes, resulting in a more devasting impact
   -S       performs a slow start, which can increases the impact
   -G       gigantic packet of 64kb of prefix/route entries
   -m       add DHCPv6 managed/other flags to RA
 ```
 
 - - -
 
 ##### atk6-flood_router6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-flood_router6 -h
 atk6-flood_router6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-flood_router6 [-HFD] interface
 
 Flood the local network with router advertisements.
 -F/-D/-H add fragment/destination/hopbyhop header to bypass RA guard security.
 ```
 
 - - -
 
 ##### atk6-flood_rs6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-flood_rs6 -h
 atk6-flood_rs6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-flood_rs6 [-sS] interface [target]
 
 Flood the local network with ICMPv6 Router Soliciation packets.
 Option -s uses random source IPv6 addresses. Option -S also randomizes the MAC.
 ```
 
 - - -
 
 ##### atk6-flood_solicitate6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-flood_solicitate6 -h
 atk6-flood_solicitate6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-flood_solicitate6 [-k | -m mac] [-a] interface [target [query-address]]
 
 Flood the network with neighbor solicitations.
 if not supplied, target is random and query address is ff02::1
 Use -a to add a hopbyhop header with router alert, -k to send with your real
 mac, -m to specify a mac or its randomized otherwise.
 ```
 
 - - -
 
 ##### atk6-flood_unreach6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-flood_unreach6 -h
 atk6-flood_unreach6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-flood_unreach6 [-HFD] [-p|-h] [-r|-R] interface target
 
 Flood the target with ICMPv6 unreachable packets.
 -F/-D/-H add fragment/destination/hopbyhop header to bypass simple filters
 -p/-h    send port/host unreachable instead of network unreachable
 -r/-R    randomize source from /64 / randomize source completely
 ```
 
 - - -
 
 ##### atk6-four2six
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-four2six -h
 atk6-four2six 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-four2six [-FHD] [-m srcmac] [-s src6] [-p srcport] interface ipv6-to-ipv4-gateway ipv4-src ipv4-dst [port]
 
 Options:
   -F         insert atomic fragment header (can be set multiple times)
   -H         insert and empty hop-by-hop header
   -D         insert a large destination header that fragments the packet
   -p srcport  set a specific UDP source port or Ping ID
   -s src6    set a specific IPv6 source address
   -m srcmac  set a specific MAC source address
 
 Send an IPv4 packet to an IPv6 4to6 gateway. If a port is specified, a UDP packet is sent, otherwise an ICMPv4 ping.
 ```
 
 - - -
 
 ##### atk6-fragmentation6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-fragmentation6 -h
 atk6-fragmentation6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-fragmentation6 [-fp] [-n number] interface destination [test-case-no]
 
 -f activates flooding mode, no pauses between sends; -p disables first and
 final pings, -n number specifies how often each test is performed
 
 Performs fragment firewall and implementation checks, incl. denial-of-service.
 ```
 
 - - -
 
 ##### atk6-fragrouter6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-fragrouter6 -h
 fragrouter6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-fragrouter6 [-dv -f len -e count -t count] INTERFACE EVASION-METHOD
 
 Options:
   -f len    size of mini fragments (option 64, default 8)
   -e count  hop count to the IDS for evading (option 256 & 512)
   -t count  hop count to the target that reaches it
   -v        verbose mode, print all packets processed for evasion
 Evasion Methods:
   0     no manipulation
   1-31  the number of atomic fragmentation headers to insert
   32    use destination headers for 1-31 instead of fragmentation headers
   64    fragment each packet to 8 byte length pieces (or change with -f)
   128   a large destination header that fragments the packet
   256   insert fake TCP data with a hop count just for the IDS (-e)
   512   insert TCP connection reset packet with a hop count just to the IDS (-e)
  1024   insert fake fragmentation data with a hop count just for the IDS (-e)
  2048   insert faked seq/ack data TCP packet
 
 Performs NIDS/NIPS evasion to all defined packets that originate from your
 system or pass through it. All evasion methods can be combined (add together)
 with the exception that only either one of 64 or 128 can be used at once.
 Option 1024 can be used with 1..31 and 64. The evasion methods are processed in the following order: 256, 512, 2048, 1..31/33..63 then either 64 or 128 then 1024.
 Requires to set up ip6table rules that jump to NFQUEUE, use fragrouter6.sh
 which is a wrapper for ip6tables and fragrouter6!
 ```
 
 - - -
 
 ##### atk6-fuzz_dhcpc6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-fuzz_dhcpc6 -h
 atk6-fuzz_dhcpc6 3.8 (c) 2020 by Darrell Ambro www.github.com/vanhauser-thc/thc-ipv6
 Partially based on code by Brandon Hutcheson and Graeme Neilson
 
 Syntax: atk6-fuzz_dhcpc6  [-1|-2|-3|-4|-5|-6|-7|-8|-9|-A|-B|-C|-D|-m] -f mac -l link -v ipv6 -x xid -c client -o options interface
 
 Options:
   -1         fuzz DHCPv6 Solicit
   -2         fuzz DHCPv6 Advertise (default)
   -3         fuzz DHCPv6 Request
   -4         fuzz DHCPv6 Confirm
   -5         fuzz DHCPv6 Renew
   -6         fuzz DHCPv6 Rebind
   -7         fuzz DHCPv6 Reply
   -8         fuzz DHCPv6 Release
   -9         fuzz DHCPv6 Decline
   -A         fuzz DHCPv6 Reconfigure
   -B         fuzz DHCPv6 Information Request
   -C         fuzz DHCPv6 Relay-Forward
   -D         fuzz DHCPv6 Relay-reply
   -m         fuzz the message type as well
   -v ipv6    IPv6 address of victim (if not specified DHCP clients sending messages are attacked)
   -x xid     Transaction ID of victim - zero for random (ignored if -v not specified) 
   -c client  Client ID of victim - zero for random (ignored if -v not specified) 
   -f mac     spoof the mac address
   -l link    spoof the link address
   -o options DHCPv6 message options to send (default: abcdefghijklmonpqr)
        a  OPTION_SERVERID
        b  OPTION_IA_NA
        c  OPTION_IA_TA
        d  OPTION_IAADR
        e  OPTION_ORO
        f  OPTION_PREFERENCE
        g  OPTION_ELAPSED_TIME
        h  OPTION_RELAY_MSG
        i  OPTION_AUTH
        j  OPTION_UNICAST
        k  OPTION_STATUS_CODE
        l  OPTION_RAPID_COMMIT
        m  OPTION_USER_CLASS
        n  OPTION_VENDOR_CLASS
        o  OPTION_VENDOR_OPTS
        p  OPTION_INTERFACE_ID
        q  OPTION_RECONF_MSG
        r  OPTION_RECONF_ACCEPT
 
 Fuzz messages sent to a DHCPv6 client
 ```
 
 - - -
 
 ##### atk6-fuzz_dhcps6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-fuzz_dhcps6 -h
 atk6-fuzz_dhcps6 3.8 (c) 2020 by Brandon Hutcheson, Graeme Neilson and Ryan Ko www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-fuzz_dhcps6 [-t number | -T number] [-e number | -T number] [-p number] [-md] [-1|-2|-3|-4|-5|-6|-7|-8] interface [domain-name]
 
 Options:
  -1         fuzz DHCPv6 Solicit (default)
  -2         fuzz DHCPv6 Request
  -3         fuzz DHCPv6 Confirm
  -4         fuzz DHCPv6 Renew
  -5         fuzz DHCPv6 Rebind
  -6         fuzz DHCPv6 Release
  -7         fuzz DHCPv6 Decline
  -8         fuzz DHCPv6 Information Request
  -m         fuzz the message type as well
  -t number  continue from test no. number
  -e number  continue to test no. number
  -T number  only performs test no. number
  -n number  how many times to send each packet (default: 1)
  -f         spoof mac
  -F         spoof link address
  -w sec     wait number of seconds between packets (default: 0)
  -p number  perform an alive check every number of tests (default: none)
  -d         Use -d to force DNS updates, you can specify a domain name on the commandline.
 
 Fuzzes a DHCPv6 packets to a server
 You can only define one of -0 ... -4 types, defaults to -1.
 Returns -1 on error, 0 on tests done and targt alive or 1 on target crash.
 ```
 
 - - -
 
 ##### atk6-fuzz_ip6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-fuzz_ip6 -h
 atk6-fuzz_ip6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-fuzz_ip6 [-x] [-t number | -T number] [-p number] [-IFSDHRJ] [-X|-1|-2|-3|-4|-5|-6|-7|-8|-9|-0 port|-P type] interface unicast-or-multicast-address [address-in-data-pkt]
 
 Fuzzes an IPv6 packet with optional EHs and upper layer transport
 Options:
  -X         do not add any ICMP/TCP header (transport layer)
  -1         fuzz ICMP6 echo request (default)
  -2         fuzz ICMP6 neighbor solicitation
  -3         fuzz ICMP6 neighbor advertisement
  -4         fuzz ICMP6 router advertisement
  -5         fuzz multicast listener report packet
  -6         fuzz multicast listener done packet
  -7         fuzz multicast listener query packet
  -8         fuzz multicast listener v2 report packet
  -9         fuzz multicast listener v2 query packet
  -0         fuzz node query packet
  -s port    fuzz TCP-SYN packet against port
  -P type    fuzz PIMv2 type packet (hello, bootstrap, assert)
  -x         tries all 256 values for flag and byte types
  -t number  continue from test no. number
  -T number  only performs test no. number
  -p number  perform an alive check every number of tests (default: none)
  -a         do not perform initial and final alive test
  -n number  how many times to send each packet (default: 1)
  -I         fuzz the IP header too
  -F         add one-shot fragmentation, and fuzz it too (for 1)
  -S         add source-routing, and fuzz it too (for 1)
  -D         add destination header, and fuzz it too (for 1)
  -H         add hop-by-hop header, and fuzz it too (for 1 and 5-9)
  -R         add router alert header, and fuzz it too (for 5-9 and all)
  -J         add jumbo packet header, and fuzz it too (for 1)
 You can only define one of -0 ... -9, -P and -s, defaults to -1.
 Note that the -P fuzzing target should be ff02::d
 Returns -1 on error, 0 on tests done and targt alive or 1 on target crash.
 ```
 
 - - -
 
 ##### atk6-implementation6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-implementation6 -h
 atk6-implementation6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-implementation6 [-p] [-s sourceip6] interface destination [test-case-number]
 
 Options:
   -s sourceip6  use the specified source IPv6 address
   -p            do not perform an alive check at the beginning and end
 
 Performs some IPv6 implementation checks, can be used to test some
 firewall features too. Takes approx. 2 minutes to complete.
 ```
 
 - - -
 
 ##### atk6-implementation6d
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-implementation6d -h
 atk6-implementation6d 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-implementation6d interface
 
 Identifies test packets by the implementation6 tool, useful to check what
 packets passed a firewall
 ```
 
 - - -
 
 ##### atk6-inject_alive6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-inject_alive6 -h
 atk6-inject_alive6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-inject_alive6 [-ap] interface
 
 This tool answers to keep-alive requests on PPPoE and 6in4 tunnels; for PPPoE
 it also sends keep-alive requests.
 Note that the appropriate environment variable THC_IPV6_{PPPOE|6IN4} must be set
 Option -a will actively send alive requests every 15 seconds.
 Option -p will not send replies to alive requests.
 ```
 
 - - -
 
 ##### atk6-inverse_lookup6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-inverse_lookup6 -h
 atk6-inverse_lookup6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-inverse_lookup6 interface mac-address
 
 Performs an inverse address query, to get the IPv6 addresses that are assigned
 to a MAC address. Note that only few systems support this yet.
 ```
 
 - - -
 
 ##### atk6-kill_router6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-kill_router6 -h
 atk6-kill_router6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-kill_router6 [-HFD] interface router-address [srcmac [dstmac]]
 
 Announce that a target a router going down to delete it from the routing tables.
 If you supply a '*' as router-address, this tool will sniff the network for any
 RA packet and immediately send the kill packet.
 Option -H adds hop-by-hop, -F fragmentation header and -D dst header.
 ```
 
 - - -
 
 ##### atk6-ndpexhaust26
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-ndpexhaust26 -h
 atk6-ndpexhaust26 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-ndpexhaust26 [-acpPTUrRm] [-s sourceip6] interface target-network
 
 Options:
  -a      add a hop-by-hop header with router alert
  -c      do not calculate the checksum to save time
  -p      send ICMPv6 Echo Requests
  -P      send ICMPv6 Echo Reply
  -T      send ICMPv6 Time-to-live-exeeded
  -U      send ICMPv6 Unreachable (no route)
  -r      randomize the source from your /64 prefix
  -R      randomize the source fully
  -m      generate a maximum size packet
  -s sourceip6  use this as source IPv6 address
 
 Flood the target /64 network with ICMPv6 TooBig error messages.
 This tool version is manyfold more effective than ndpexhaust6.
 ```
 
 - - -
 
 ##### atk6-ndpexhaust6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-ndpexhaust6 -h
 !
 ! Please note: ndpexhaust6 is deprecated, please use ndpexhaust26!
 !
 
 atk6-ndpexhaust6 by mario fleischmann <mario.fleischmann@1und1.de>
 
 Syntax: atk6-ndpexhaust6 interface destination-network [sourceip]
 
 Randomly pings IPs in target network
 
 ```
 
 - - -
 
 ##### atk6-node_query6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-node_query6 -h
 atk6-node_query6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-node_query6 interface target
 
 Sends an ICMPv6 node query request to the target and dumps the replies.
 
 ```
 
 - - -
 
 ##### atk6-parasite6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-parasite6 -h
 atk6-parasite6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-parasite6 [-lRFHD] interface [fake-mac]
 
 This is an "ARP spoofer" for IPv6, redirecting all local traffic to your own
 system (or nirvana if fake-mac does not exist) by answering falsely to
 Neighbor Solitication requests
 Option -l loops and resends the packets per target every 5 seconds.
 Option -R will also try to inject the destination of the solicitation
 NS security bypass: -F fragment, -H hop-by-hop and -D large destination header
 ```
 
 - - -
 
 ##### atk6-passive_discovery6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-passive_discovery6 -h
 atk6-passive_discovery6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-passive_discovery6 [-Ds] [-m maxhop] [-R prefix] interface [script]
 
 Options:
  -D          do also dump destination addresses (does not work with -m)
  -s          do only print the addresses, no other output
  -m maxhop   the maximum number of hops a target which is dumped may be away.
              0 means local only, the maximum amount to make sense is usually 5
  -R prefix   exchange the defined prefix with the link local prefix
 
 Passivly sniffs the network and dump all client's IPv6 addresses detected.
 Note that in a switched environment you get better results when additionally
 starting parasite6, however this will impact the network.
 If a script name is specified after the interface, it is called with the
 detected ipv6 address as first and the interface as second option.
 ```
 
 - - -
 
 ##### atk6-randicmp6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-randicmp6 -h
 Syntax: atk6-randicmp6 [-p] [-s sourceip] interface destination [type [code]]
 
 Sends all ICMPv6 type and code combinations to destination.
 Option -s  sets the source IPv6 address.
 Option -p  will not print answers received.
 ```
 
 - - -
 
 ##### atk6-redir6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-redir6 -h
 atk6-redir6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-redir6 interface victim-ip target-ip original-router new-router [new-router-mac] [hop-limit]
 
 Implant a route into victim-ip, which redirects all traffic to target-ip to
 new-ip. You must know the router which would handle the route.
 If the new-router-mac does not exist, this results in a DOS.
 If the TTL of the target is not 64, then specify this is the last option.
 ```
 
 - - -
 
 ##### atk6-redirsniff6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-redirsniff6 -h
 atk6-redirsniff6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-redirsniff6 interface victim-ip destination-ip original-router [new-router [new-router-mac]]
 
 Implant a route into victim-ip, which redirects all traffic to destination-ip to
 new-router. This is done on all traffic that flows by that matches
 victim->target. You must know the router which would handle the route.
 If the new-router/-mac does not exist, this results in a DOS.
 You can supply a wildcard ('*') for victim-ip and/or destination-ip.
 ```
 
 - - -
 
 ##### atk6-rsmurf6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-rsmurf6 -h
 atk6-rsmurf6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-rsmurf6 interface victim-ip
 
 Smurfs the local network of the victim. Note: this depends on an
 implementation error, currently only verified on Linux.
 Evil: "ff02::1" as victim will DOS your local LAN completely
 ```
 
 - - -
 
 ##### atk6-sendpees6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-sendpees6 -h
 sendpees6 by willdamn <willdamn@gmail.com>
 
 Syntax: atk6-sendpees6 interface key_length prefix victim
 
 Send SEND neighbor solicitation messages and make target to verify a lota CGA and RSA signatures
 
 ```
 
 - - -
 
 ##### atk6-sendpeesmp6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-sendpeesmp6 -h
 original sendpees by willdamn <willdamn@gmail.com>
 modified sendpeesMP by Marcin Pohl <marcinpohl@gmail.com>
 Code based on thc-ipv6
 
 Syntax: atk6-sendpeesmp6 interface key_length prefix victim
 
 Send SEND neighbor solicitation messages and make target to verify a lota CGA and RSA signatures
 Example: atk6-sendpeesmp6 eth0 2048 fe80:: fe80::1
 
 ```
 
 - - -
 
 ##### atk6-smurf6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-smurf6 -h
 atk6-smurf6 3.8 (c) 2013 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-smurf6 [-i microseconds] interface victim-ip [multicast-network-address]
 
 Smurf the target with icmp echo replies. Target of echo request is the
 local all-nodes multicast address if not specified
 ```
 
 - - -
 
 ##### atk6-thcping6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-thcping6 -h
 atk6-thcping6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-thcping6 [-EafqxO] [-e ethertype] [-H t:l:v] [-D t:l:v] [-F dst] [-e ethertype] [-L length] [-N nextheader] [-V version] [-t ttl] [-c class] [-l label] [-d size] [-S port|-U port|-T type -C code] interface src6 dst6 [srcmac [dstmac [data]]]
 
 Options:
   -x              flood mode (doesn't check for replies)
   -w ms           wait time between packets in ms (default: 1000, if -n not 1)
   -a              add a hop-by-hop header with router alert option.
   -q              add a hop-by-hop header with quickstart option.
   -E              send as ethertype IPv4
   -e ethertype    send as specified ethertype (hexadecimal!)
   -H t:l:v        add a hop-by-hop header with special content
   -D t:l:v        add a destination header with special content
   -D "xxx"        add a large destination header which fragments the packet
   -f              add a one-shot fragementation header
   -F ipv6address  use source routing to this final destination
   -t ttl          specify TTL (default: 255)
   -c class        specify a class (0-4095)
   -l label        specify a label (0-1048575)
   -L length       set fake payload length (0-65535)
   -N nextheader   set fake next header (0-255)
   -V version      set IP version (0-15)
   -d data_size    define the size of the ping data buffer
   -O              send TCP Fast Open cookie request option (needs -S)
   -T number       ICMPv6 type to send (default: 128 = ping)
   -C number       ICMPv6 code to send (default: 0)
   -S port         use a TCP SYN packet on the defined port instead of ping
   -U port         use a UDP packet on the defined port instead of ping
   -n count        how often to send the packet (default: 1)
 t:l:v syntax: type:length:value, value is in hex, e.g. 1:2:0eab
 You can put an "x" into src6, srcmac and dstmac for an automatic value.
 
 Craft a ICMPv6/TCP/UDP packet with special IPv6 or EH header options.
 Returns -1 on error or no reply, 0 on normal reply or 1 on error reply.
 ```
 
 - - -
 
 ##### atk6-thcsyn6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-thcsyn6 -h
 atk6-thcsyn6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-thcsyn6 [-aAcdDfrORS] [-i microsecond] [-m dstmac] [-p port] [-s sourceip6] interface target port
 
 Options:
  -i      sending interval of packets (in microseconds)
  -a      add hop-by-hop header with router alert
  -d      add destination header (can be set up to 64 times)
  -f      add atomic fragmentation header (can be set up to 64 times)
  -A      send TCP-ACK packets
  -S      send TCP-SYN-ACK packets
  -r      randomize the source from your /64 prefix
  -R      randomize the source fully
  -D      randomize the destination (treat as /64)
  -O      add a TCP Fast Open cookie (SYN-only packets)
  -m dstmac     use this destination mac address
  -s sourceip6  use this as source IPv6 address
  -p port       use fixed source port
 
 Flood the target port with TCP-SYN packets. If you supply "x" as port, it
 is randomized.
 ```
 
 - - -
 
 ##### atk6-toobig6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-toobig6 -h
 atk6-toobig6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-toobig6 [-u] interface target-ip existing-ip mtu [hop-limit]
 
 Implants the specified mtu on the target.
 If the TTL of the target is not 64, then specify this as the last option.
 Option -u will send the TooBig without the spoofed ping6 from existing-ip.
 ```
 
 - - -
 
 ##### atk6-toobigsniff6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-toobigsniff6 -h
 atk6-toobigsniff6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-toobigsniff6 [-c] interface target mtu
 
 Sniff for packte from target and send an ICMPv6 too big error message based on
 that packet with the MTU specified. If you supply a '*' as-address, any global
 traffic sniffed will be used.
 If you supply the option -c the tool will not quit upon first packet match, but
 continue running and send packets until aborted.
 ```
 
 - - -
 
 ##### atk6-trace6
 
 (unknown subject)
 
 ```
 root@kali:~# atk6-trace6 -h
 atk6-trace6 3.8 (c) 2020 by van Hauser / THC <vh@thc.org> www.github.com/vanhauser-thc/thc-ipv6
 
 Syntax: atk6-trace6 [-abdtu] [-s src6] interface targetaddress [port]
 
 Options:
   -a       insert a hop-by-hop header with router alert option.
   -D       insert a destination extension header
   -E       insert a destination extension header with an invalid option
   -F       insert a one-shot fragmentation header
   -b       instead of an ICMP6 Ping, use TooBig (you will not see the target)
   -B       instead of an ICMP6 Ping, use PingReply (you will not see the target)
   -d       resolves the IPv6 addresses to DNS.
   -t       enables tunnel detection
   -u       use UDP instead of TCP if a port is supplied
   -r       raw mode (for adapters networks that have no ethernet)
   -s src6  specifies the source IPv6 address
 Maximum hop reach: 31
 
 A basic but very fast traceroute6 program.
 If no port is specified, ICMP6 Ping requests are used, otherwise TCP SYN
 packets to the specified port. Options D, E and F can be use multiple times.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## address6 Usage Example

Convert an IPv6 address to a MAC address and vice-versa:

```
root@kali:~# address6 fe80::76d4:35ff:fe4e:39c8
74:d4:35:4e:39:c8
root@kali:~# address6 74:d4:35:4e:39:c8
fe80::76d4:35ff:fe4e:39c8
```

## alive6 Usage Example

```
root@kali:~# alive6 eth0
Alive: fd77:7c68:420a:1:426c:8fff:fe1b:cb90 [ICMP parameter problem]
Alive: fd77:7c68:420a:1:20c:29ff:fee5:5bf4 [ICMP echo-reply]
Alive: fd77:7c68:420a:1:75d9:4f39:a46a:6f83 [ICMP echo-reply]
Alive: fd77:7c68:420a:1:6912:8e80:e02f:1969 [ICMP echo-reply]
Alive: fd77:7c68:420a:1:201:6cff:fe6f:ddd1 [ICMP echo-reply]
```

## detect-new-ip6 Usage Example

```
root@kali:~# detect-new-ip6 eth0
Started ICMP6 DAD detection (Press Control-C to end) ...
Detected new ip6 address: fe80::85d:9879:9251:853a
```

## dnsdict6 Usage Example

```
root@kali:~# dnsdict6 example.com
Starting DNS enumeration work on example.com. ...
Starting enumerating example.com. - creating 8 threads for 798 words...
Estimated time to completion: 1 to 2 minutes
www.example.com. => 2606:2800:220:6d:26bf:1447:1097:aa7
```
