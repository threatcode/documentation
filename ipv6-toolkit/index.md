---
archived: "true"
Title: ipv6-toolkit
Homepage: https://www.si6networks.com/tools/ipv6toolkit/
Repository: https://gitlab.com/kalilinux/packages/ipv6-toolkit
Architectures: any
Version: 2.1+git20210331-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### ipv6-toolkit
 
  Included tools:
   - addr6: An IPv6 address analysis and manipulation tool.
   - flow6: A tool to perform a security asseessment of the IPv6 Flow Label.
   - frag6: A tool to perform IPv6 fragmentation-based attacks and to perform a
     security assessment of a number of fragmentation-related aspects.
   - icmp6: A tool to perform attacks based on ICMPv6 error messages.
   - jumbo6: A tool to assess potential flaws in the handling of IPv6 Jumbograms.
   - na6: A tool to send arbitrary Neighbor Advertisement messages.
   - ni6: A tool to send arbitrary ICMPv6 Node Information messages, and assess
     possible flaws in the processing of such packets.
   - ns6: A tool to send arbitrary Neighbor Solicitation messages.
   - ra6: A tool to send arbitrary Router Advertisement messages.
   - rd6: A tool to send arbitrary ICMPv6 Redirect messages.
   - rs6: A tool to send arbitrary Router Solicitation messages.
   - scan6: An IPv6 address scanning tool.
   - tcp6: A tool to send arbitrary TCP segments and perform a variety of TCP-
     based attacks.
 
 **Installed size:** `3.46 MB`  
 **How to install:** `sudo apt install ipv6-toolkit`  
 
 {{< spoiler "Dependencies:" >}}
 * ieee-data
 * libc6 
 * libpcap0.8 
 {{< /spoiler >}}
 
 ##### addr6
 
 An IPv6 address analysis and manipulation tool
 
 ```
 root@kali:~# addr6 -h
 SI6 Networks' IPv6 Toolkit v3.0 (Buffy)
 addr6: An IPv6 address analysis and conversion tool
 
 usage: addr6 (-i | -a) [-c | -d | -r | -s | -q] [-v] [-h]
 
 OPTIONS:
   --address, -a             IPv6 address to be decoded
   --gen-addr, -A            Generate a randmized address for the specified prefix
   --stdin, -i               Read IPv6 addresses from stdin (standard input)
   --print-fixed, -f         Print addresses in expanded/fixed format
   --print-canonic, -c       Print IPv6 addresses in canonic form
   --print-reverse, -r       Print reversed IPv6 address
   --print-decode, -d        Decode IPv6 addresses
   --print-stats, -s         Print statistics about IPv6 addresses
   --print-response, -R      Print result of address filters
   --print-pattern, -x       Analyze addresses pattern
   --print-uni-preflen, -P   Print unique prefixes of a specified length
   --block-dup, -q           Discard duplicate IPv6 addresses
   --block-dup-preflen, -p   Discard duplicate prefixes of specified length
   --accept, -j              Accept IPv6 addresses from specified IPv6 prefix
   --accept-type, -b         Accept IPv6 addresses of specified type
   --accept-scope, -k        Accept IPv6 addresses of specified scope
   --accept-utype, -w        Accept IPv6 unicast addresses of specified type
   --accept-iid, -g          Accept IPv6 addresses with IIDs of specified type
   --block, -J               Block IPv6 addresses from specified IPv6 prefix
   --block-type, -B          Block IPv6 addresses of specified type
   --block-scope, -K         Block IPv6 addresses of specified scope
   --block-utype, -W         Block IPv6 unicast addresses of specified type
   --block-iid, -G           Block IPv6 addresses with IIDs of specified type
   --verbose, -v             Be verbose
   --help, -h                Print help for the addr6 tool
 
  Programmed by Fernando Gont for SI6 Networks <https://www.si6networks.com>
  Please send any bug reports to <fgont@si6networks.com>
 
 ```
 
 - - -
 
 ##### blackhole6
 
 A tool to find IPv6 blackholes
 
 ```
 root@kali:~# man blackhole6
 BLACKHOLE6(1)               General Commands Manual              BLACKHOLE6(1)
 
 NAME
        blackhole6 - A tool to find IPv6 blackholes
 
 SYNOPSIS
        blackhole6 DESTINATION [PARAMETERS]
 
 DESCRIPTION
        blackhole6 is a tool to isolate IPv6 blackholes.
 
        SCRIPTS
 
        get-mx
 
        This script takes no further arguments, and operates as follows:
 
            + The tool reads domain names from standard-input (oner per line),
              and obtains the MX for the corresponding domain.
 
            + Lines where the first non-blank character is the numeral sign (#)
              are consdered to contain comments, and hence are ignored.
 
            + The format of the resulting output is:
 
              # DOMAIN_NAME (CANONIC_NAME)
              MX_RECORD_1
              MX_RECORD_2
 
        get-ns
 
        This script takes no further arguments, and operates as follows:
 
            + The tool reads domain names from standard-input (oner per line),
              and obtains the NS records for the corresponding domain.
 
            + Lines where the first non-blank character is the numeral sign (#)
              are consdered to contain comments, and hence are ignored.
 
            + The format of the resulting output is:
 
              # DOMAIN_NAME (CANONIC_NAME)
              MX_RECORD_1
              MX_RECORD_2
 
        trace-do8-tcp trace-do8-icmp trace-do256-tcp trace-do256-icmp
 
        These  scripts  are meant to obtain information about where in the net-
        work packets employing IPv6 Extension Headers are being  dropped.  They
        test the path with IPv6 packets containing TCP or ICMPv6 payloads and a
        Destination Options Header of 8 or 256 bytes. Based on the obtained re-
        sults, the tool can infer what is the system causing the packet drops.
 
        trace-hbh8-tcp trace-hbh8-icmp trace-hbh256-tcp trace-hbh256-icmp
 
        These  scripts  are meant to obtain information about where in the net-
        work packets employing IPv6 Extension Headers are being  dropped.  They
        test the path with IPv6 packets containing TCP or ICMPv6 payloads and a
        Hop-by-Hop Options Header of 8 or 256 bytes. Based on the obtained  re-
        sults, the tool can infer what is the system causing the packet drops.
 
        trace-fh256-tcp trace-fh256-icmp
 
        These  scripts  are meant to obtain information about where in the net-
        work packets employing IPv6 Extension Headers are being  dropped.  They
        test  the  path with IPv6 packets containing TCP or ICMPv6 payloads re-
        sulting in IPv6 fragments of around 256 bytes. Based  on  the  obtained
        results,  the  tool  can  infer  what  is the system causing the packet
        drops.
 
        trace-do8-tcp-stdin trace-do8-icmp-stdin  trace-do256-tcp-stdin  trace-
        do256-icmp-stdin
 
        These  scripts  are meant to obtain information about where in the net-
        work packets employing IPv6 Extension Headers are being  dropped.  They
        test the path with IPv6 packets containing TCP or ICMPv6 payloads and a
        Destination Options Header of 8 or 256 bytes. Based on the obtained re-
        sults,  the tool can infer what is the system causing the packet drops.
        These tools read one IPv6 address per line form standard input and, for
        each of those addresses, information is printed with the following syn-
        tax:
 
        trace-hbh8-tcp-stdin    trace-hbh8-icmp-stdin    trace-hbh256-tcp-stdin
        trace-hbh256-icmp-stdin
 
        These  scripts  are meant to obtain information about where in the net-
        work packets employing IPv6 Extension Headers are being  dropped.  They
        test the path with IPv6 packets containing TCP or ICMPv6 payloads and a
        Hop-by-Hop Options Header of 8 or 256 bytes. Based on the obtained  re-
        sults,  the tool can infer what is the system causing the packet drops.
        These tools read one IPv6 address per line form standard input and, for
        each of those addresses, information is printed with the following syn-
        tax:
 
        trace-fh256-tcp-stdin trace-fh256-icmp-stdin
 
        These scripts are meant to obtain information about where in  the  net-
        work  packets  employing IPv6 Extension Headers are being dropped. They
        test the path with IPv6 packets containing TCP or ICMPv6  payloads  re-
        sulting  in  IPv6  fragments of around 256 bytes. Based on the obtained
        results, the tool can infer what  is  the  system  causing  the  packet
        drops.  These  tools read one IPv6 address per line form standard input
        and, for each of those addresses, information is printed with the  fol-
        lowing syntax:
 
        -h, --help
 
               Print help information for the scan6 tool.
 
 EXAMPLES
        The  following  sections  illustrate  typical  use cases of the script6
        tool.
 
        Example #1
 
        # scan6 -i eth0 -L -e -v
 
        Perform host scanning on the local network ("-L" option)  using  inter-
        face  "eth0"  ("-i" option). Use both ICMPv6 echo requests and unrecog-
        nized IPv6 options of type 10xxxxxx (default).  Print  link-link  layer
        addresses along with IPv6 addresses ("-e" option). Be verbose ("-v" op-
        tion).
 
        Example #2
 
        #  scan6  -d  2001:db8::/64  --tgt-virtual-machines   all   --ipv4-host
        10.10.10.0/24
 
        Scan  for  virtual  machines (both VirtualBox and vmware) in the prefix
        2001:db8::/64. The additional information about  the  IPv4  prefix  em-
        ployed by the host system is leveraged to reduce the search space.
 
        Example #3
 
        #   scan6  -d  2001:db8::/64  --tgt-ipv4-embedded  ipv4-32  --ipv4-host
        10.10.10.0/24
 
        Scan for IPv6 addresses of the network  2001:db8::/64  that  embed  the
        IPv4 prefix 10.10.10.0/24 (with the 32-bit encoding).
 
        Example #4
 
        # scan6 -d 2001:db8:0-500:0-1000
 
        Scan  for  IPv6 addresses of the network 2001:db8::/64, varying the two
        lowest order 16-bit words of the  addresses  in  the  range  0-500  and
        0-1000, respectively.
 
        Example #5
 
        # scan6 -d fc00::/64 --tgt-vendor 'Dell Inc' -p tcp
 
        Scan  for network devices manufactured by 'Dell Inc' in the target pre-
        fix fc00::/64. The tool will employ TCP segments as the  probe  packets
        (rather than the default ICMPv6 echo requests).
 
        Example #6
 
        # scan6 -i eth0 -L -S 66:55:44:33:22:11 -p unrec -P global -v
 
        Use  the "eth0" interface ("-i" option) to perform host-scanning on the
        local network ("-L" option). The Ethernet  Source  Address  is  set  to
        "66:55:44:33:22:11" ("-S" option). The probe packets will be IPv6 pack-
        ets with unrecognized options of type 10xxxxxx ("-p" option). The  tool
        will  only  print IPv6 global addresses ("-P" option). The tool will be
        verbose.
 
        Example #7
 
        # scan6 -d 2001:db8::/64 -w KNOWN_IIDS
 
        Perform an address scan of a set of known  hosts  listed  in  the  file
        KNOWN_IIDS,  at  remote network 2001:db8::/64. The target addresses are
        obtaining by concatenating the network prefix  2001:db8::/64  with  the
        interface IDs of each of the addresses fund in the file KNOWN_IIDS.
 
        Example #8
 
        # scan6 -i eth0 -L -P global --print-unique -e
 
        Use  the "eth0" interface ("-i" option) to perform host-scanning on the
        local network ("-L" option). Print only global unicast addresses  ("-P"
        option),   and   at   most   one  IPv6  address  per  Ethernet  address
        ("--print-unique" option). Ethernet addresses  will  be  printed  along
        with the corresponiding IPv6 address ("-e" option).
 
        Example #9
 
        # scan6 -m knownprefixes.txt -w knowniids.txt -l -z 60 -t -v
 
        Build  the list of targets from the IPv6 prefixes contained in the file
        'knownprefixes.txt' and the Interface IDs (IIDs) contained in the  file
        'knowniids.txt'. Poll the targets periodically ("-l" option), and sleep
        60 seconds after each iteration ("-z" option). Print a timestamp  along
        the IPv6 address of each alive node ("-t" option). Be verbose ("-v" op-
        tion).
 
 AUTHOR
        The script6 tool and the corresponding manual pages  were  produced  by
        Fernando     Gont     <fgont@si6networks.com>    for    SI6    Networks
        <http://www.si6networks.com>.
 
 COPYRIGHT
        Copyright (c) 2014-2015 Fernando Gont.
 
        Permission is granted to copy, distribute and/or modify  this  document
        under  the  terms of the GNU Free Documentation License, Version 1.3 or
        any later version published by the Free Software  Foundation;  with  no
        Invariant  Sections,  no Front-Cover Texts, and no Back-Cover Texts.  A
        copy  of  the   license   is   available   at   <http://www.gnu.org/li-
        censes/fdl.html>.
 
                                                                  BLACKHOLE6(1)
 ```
 
 - - -
 
 ##### flow6
 
 A security assessment tool for the IPv6 Flow Label field
 
 ```
 root@kali:~# flow6 -h
 SI6 Networks' IPv6 Toolkit v3.0 (Buffy)
 flow6: Security assessment tool for the IPv6 Flow Label field
 
 usage: flow6 -d DST_ADDR [-i INTERFACE] [-S LINK_SRC_ADDR] [-D LINK-DST-ADDR]
        [-s SRC_ADDR[/LEN]] [-A HOP_LIMIT] [-P PROTOCOL] [-p PORT]
        [-W] [-v] [-h]
 
 OPTIONS:
   --interface, -i           Network interface
   --link-src-addr, -S       Link-layer Destination Address
   --link-dst-addr, -D       Link-layer Source Address
   --src-addr, -s            IPv6 Source Address
   --dst-addr, -d            IPv6 Destination Address
   --hop-limit, -A           IPv6 Hop Limit
   --protocol, -P            IPv6 Payload protocol (valid: TCP, UDP)
   --dst-port, -p            Transport Protocol Destination Port
   --flow-label-policy, -W   Assess the Flow Label generation policy
   --help, -h                Print help for the flow6 tool
   --verbose, -v             Be verbose
 
 Programmed by Fernando Gont on behalf of SI6 Networks <https://www.si6networks.com>
 Please send any bug reports to <fgont@si6networks.com>
 
 ```
 
 - - -
 
 ##### frag6
 
 A security assessment tool for IPv6 fragmentation
 
 ```
 root@kali:~# frag6 -h
 SI6 Networks' IPv6 Toolkit v3.0 (Buffy)
 frag6: A security assessment tool for attack vectors based on IPv6 fragments
 
 usage: frag6 -d DST_ADDR [-i INTERFACE] [-S LINK_SRC_ADDR] [-D LINK-DST-ADDR]
        [-s SRC_ADDR[/LEN]] [-A HOP_LIMIT] [-u DST_OPT_HDR_SIZE]
        [-U DST_OPT_U_HDR_SIZE] [-H HBH_OPT_HDR_SIZE] [-P FRAG_SIZE]
        [-O FRAG_TYPE] [-o FRAG_OFFSET] [-I FRAG_ID] [-T] [-n]
        [-p | -W | -X | -F N_FRAGS] [-l] [-z SECONDS] [-v] [-h]
 
 OPTIONS:
   --interface, -i           Network interface
   --link-src-addr, -S       Link-layer Destination Address
   --link-dst-addr, -D       Link-layer Source Address
   --src-addr, -s            IPv6 Source Address
   --dst-addr, -d            IPv6 Destination Address
   --hop-limit, -A           IPv6 Hop Limit
   --dst-opt-hdr, -u         Destination Options Header (Fragmentable Part)
   --dst-opt-u-hdr, -U       Destination Options Header (Unfragmentable Part)
   --hbh-opt-hdr, -H         Hop by Hop Options Header
   --frag-size, -P           IPv6 fragment payload size
   --frag-type, -O           IPv6 Fragment Type {first, last, middle, atomic}
   --frag-offset, -o         IPv6 Fragment Offset
   --frag-id, -I             IPv6 Fragment Identification
   --no-timestamp, -T        Do not include a timestamp in the payload
   --no-responses, -n        Do not print responses to transmitted packets
   --frag-reass-policy, -p   Assess fragment reassembly policy
   --frag-id-policy, -W      Assess the Fragment ID generation policy
   --pod-attack, -X          Perform a 'Ping of Death' attack
   --flood-frags, -F         Flood target with IPv6 fragments
   --loop, -l                Send IPv6 fragments periodically
   --sleep, -z               Pause between sending IPv6 fragments
   --verbose, -v             Be verbose
   --help, -h                Print help for the frag6 tool
 
 Programmed by Fernando Gont for SI6 Networks <https://www.si6networks.com>
 Please send any bug reports to <fgont@si6networks.com>
 
 ```
 
 - - -
 
 ##### icmp6
 
 A security assessment tool for attack vectors based on ICMPv6 packets
 
 ```
 root@kali:~# icmp6 -h
 SI6 Networks' IPv6 Toolkit v3.0 (Buffy)
 icmp6: Security assessment tool for attack vectors based on ICMPv6 error messages
 
 usage: icmp6 [-i INTERFACE] [-s SRC_ADDR[/LEN]] [-d DST_ADDR]
        [-S LINK_SRC_ADDR] [-D LINK-DST-ADDR] [-c HOP_LIMIT] [-y FRAG_SIZE]
        [-u DST_OPT_HDR_SIZE] [-U DST_OPT_U_HDR_SIZE] [-H HBH_OPT_HDR_SIZE]
        [-t TYPE[:CODE] | -e CODE | -A CODE -V CODE -R CODE] [-r TARGET_ADDR]
        [-x PEER_ADDR] [-c HOP_LIMIT] [-m MTU] [-O POINTER] [-p PAYLOAD_TYPE]
        [-P PAYLOAD_SIZE] [-n] [-a SRC_PORTL[:SRC_PORTH]]
        [-o DST_PORTL[:DST_PORTH]] [-X TCP_FLAGS] [-q TCP_SEQ] [-Q TCP_ACK]
        [-V TCP_URP] [-w TCP_WIN] [-M] [-j PREFIX[/LEN]] [-k PREFIX[/LEN]]
        [-J LINK_ADDR] [-K LINK_ADDR] [-b PREFIX[/LEN]] [-g PREFIX[/LEN]]
        [-B LINK_ADDR] [-G LINK_ADDR] [-f] [-L | -l] [-z] [-v] [-h]
 
 OPTIONS:
   --interface, -i             Network interface
   --src-addr, -s              IPv6 Source Address
   --dst-addr, -d              IPv6 Destination Address
   --hop-limit, -c             IPv6 Hop Limit
   --frag-hdr. -y              Fragment Header
   --dst-opt-hdr, -u           Destination Options Header (Fragmentable Part)
   --dst-opt-u-hdr, -U         Destination Options Header (Unfragmentable Part)
   --hbh-opt-hdr, -H           Hop by Hop Options Header
   --link-src-addr, -S         Link-layer Destination Address
   --link-dst-addr, -D         Link-layer Source Address
   --icmp6, -t                 ICMPv6 Type:Code
   --icmp6-dest-unreach, -e    ICMPv6 Destination Unreachable
   --icmp6-packet-too-big, -E  ICMPv6 Packet Too Big
   --icmp6-time-exceeded, -A   ICMPv6 Time Exceeeded
   --icmp6-param-problem, -R   ICMPv6 Parameter Problem
   --mtu, -m                   Next-Hop MTU (ICMPv6 Packet Too Big)
   --pointer, -O               Pointer (ICMPv6 Parameter Problem
   --payload-type, -p          Redirected Header Payload Type
   --payload-size, -P          Redirected Header Payload Size
   --no-payload, -n            Do not include a Redirected Header Option
   --ipv6-hlim, -C             ICMPv6 Payload's Hop Limit
   --target-addr, -r           ICMPv6 Payload's IPv6 Source Address
   --peer-addr, -x             ICMPv6 Payload's IPv6 Destination Address
   --target-port, -o           ICMPv6 Payload's Source Port
   --peer-port, -a             ICMPv6 Payload's Destination Port
   --tcp-flags, -X             ICMPv6 Payload's TCP Flags
   --tcp-seq, -q               ICMPv6 Payload's TCP SEQ Number
   --tcp-ack, -Q               ICMPv6 Payload's TCP ACK Number
   --tcp-urg, -V               ICMPv6 Payload's TCP URG Pointer
   --tcp-win, -w               ICMPv6 Payload's TCP Window
   --resp-mcast, -M            Respond to Multicast Packets
   --block-src, -j             Block IPv6 Source Address prefix
   --block-dst, -k             Block IPv6 Destination Address prefix
   --block-link-src, -J        Block Ethernet Source Address
   --block-link-dst, -K        Block Ethernet Destination Address
   --accept-src, -b            Accept IPv6 Source Address prefix
   --accept-dst, -g            Accept IPv6 Destination Address prefix
   --accept-link-src, -B       Accept Ethernet Source Address
   --accept-link-dst, -G       Accept Ethernet Destination Address
   --sanity-filters, -f        Add sanity filters
   --listen, -L                Listen to incoming traffic
   --loop, -l                  Send periodic ICMPv6 error messages
   --sleep, -z                 Pause between sending ICMPv6 error messages
   --help, -h                  Print help for the icmp6 tool
   --verbose, -v               Be verbose
 
  Programmed by Fernando Gont for SI6 Networks <https://www.si6networks.com>
  Please send any bug reports to <fgont@si6networks.com>
 
 ```
 
 - - -
 
 ##### jumbo6
 
 A security assessment tool for attack vectors based on IPv6 jumbograms
 
 ```
 root@kali:~# jumbo6 -h
 SI6 Networks' IPv6 Toolkit v3.0 (Buffy)
 jumbo6: Security assessment tool for attack vectors based on IPv6 jumbo packets
 
 usage: jumbo6 -d DST_ADDR [-i INTERFACE] [-S LINK_SRC_ADDR] [-D LINK-DST-ADDR]
        [-s SRC_ADDR[/LEN]] [-A HOP_LIMIT] [-H HBH_OPT_HDR_SIZE] 
        [-U DST_OPT_U_HDR_SIZE] [-y FRAG_SIZE] [-u DST_OPT_HDR_SIZE]
        [-q IPV6_LENGTH] [-Q JUMBO_LENGTH] [-P PAYLOAD_SIZE] [-j PREFIX[/LEN]]
        [-k PREFIX[/LEN]] [-J LINK_ADDR] [-K LINK_ADDR] [-b PREFIX[/LEN]]
        [-g PREFIX[/LEN]] [-B LINK_ADDR] [-G LINK_ADDR] [-L | -l] [-z SECONDS]
        [-v] [-h]
 
 OPTIONS:
   --interface, -i           Network interface
   --link-src-addr, -S       Link-layer Destination Address
   --link-dst-addr, -D       Link-layer Source Address
   --src-addr, -s            IPv6 Source Address
   --dst-addr, -d            IPv6 Destination Address
   --hop-limit, -A           IPv6 Hop Limit
   --frag-hdr. -y            Fragment Header
   --dst-opt-hdr, -u         Destination Options Header (Fragmentable Part)
   --dst-opt-u-hdr, -U       Destination Options Header (Unfragmentable Part)
   --hbh-opt-hdr, -H         Hop by Hop Options Header
   --ipv6-length, -q         IPv6 Payload Length
   --jumbo-length, -Q        Jumbo Payload Length
   --payload-size, -P        ICMPv6 payload size
   --loop, -l                Send periodic Jumbo messages
   --sleep, -z               Pause between sending Redirect messages
   --listen, -L              Listen to incoming packets
   --verbose, -v             Be verbose
   --help, -h                Print help for the jumbo6 tool
 
 Programmed by Fernando Gont on behalf of SI6 Networks <https://www.si6networks.com>
 Please send any bug reports to <fgont@si6networks.com>
 
 ```
 
 - - -
 
 ##### messi
 
 
 
 - - -
 
 ##### mldq6
 
 A security assessment tool for attack vectors based on ICMPv6 MLD Query messages
 
 ```
 root@kali:~# mldq6 -h
 SI6 Networks' IPv6 Toolkit v3.0 (Buffy)
 mldq6: Security assessment tool for attack vectors based on MLD Query messages
 
 usage: mldq6 -i INTERFACE [-s SRC_ADDR[/LEN]] [-d DST_ADDR] [-A HOP_LIMIT] [-y FRAG_SIZE] [-u DST_OPT_HDR_SIZE] [-U DST_OPT_U_HDR_SIZE] [-H HBH_OPT_HDR_SIZE] [-S LINK_SRC_ADDR] [-D LINK-DST-ADDR] [-E LINK_ADDR] [-e] [-m MLD_ADDR] [-r MLD_RESP_DELAY ] [-F N_SOURCES] [-z SECONDS] [-l] [-v] [-h]
 
 OPTIONS:
   --interface, -i            Network interface
   --src-addr, -s             IPv6 Source Address
   --dst-addr, -d             IPv6 Destination Address
   --hop-limit, -A            IPv6 Hop Limit
   --frag-hdr. -y             Fragment Header
   --dst-opt-hdr, -u          Destination Options Header (Fragmentable Part)
   --dst-opt-u-hdr, -U        Destination Options Header (Unfragmentable Part)
   --hbh-opt-hdr, -H          Hop by Hop Options Header
   --link-src-addr, -S        Link-layer Destination Address
   --link-dst-addr, -D        Link-layer Source Address
   --src-link-opt, -E         Source link-layer address option
   --add-slla-opt, -e         Add Source link-layer address option
   --mld-addr, -m             MLD Query Multicast Address
   --mld-resp-delay, -r       MLD Query Maximum Response Delay [ms]
   --flood-sources, -F        Number of Source Addresses to forge randomly
   --loop, -l                 Send MLD Query periodically
   --sleep, -z                Pause between peiodic MLD Queries [sec]
   --help, -h                 Print help for the mldq6 tool
   --verbose, -v              Be verbose
 
 Programmed by Fernando Gont for SI6 Networks <https://www.si6networks.com>
 Please send any bug reports to <fgont@si6networks.com>
 ```
 
 - - -
 
 ##### na6
 
 A security assessment tool for attack vectors based on ICMPv6 Neighbor Advertisement messages
 
 ```
 root@kali:~# na6 -h
 SI6 Networks' IPv6 Toolkit v3.0 (Buffy)
 na6: Security Assessment tool for attack vectors based on NA messages
 
 usage: na6 -i INTERFACE [-s SRC_ADDR[/LEN]] [-d DST_ADDR] [-S LINK_SRC_ADDR] [-y FRAG_SIZE] [-u DST_OPT_HDR_SIZE] [-U DST_OPT_U_HDR_SIZE] [-H HBH_OPT_HDR_SIZE] [-D LINK-DST-ADDR] [-t TARGET_ADDR[/LEN]] [-r] [-c] [-o] [-E LINK_ADDR] [-e] [-j PREFIX[/LEN]] [-k PREFIX[/LEN]] [-J LINK_ADDR] [-K LINK_ADDR] [-w PREFIX[/LEN]] [-b PREFIX[/LEN]] [-g PREFIX[/LEN]] [-B LINK_ADDR] [-G LINK_ADDR] [-W PREFIX[/LEN]] [-F N_SOURCES] [-T N_TARGETS] [-L | -l] [-z] [-v] [-V] [-h]
 
 OPTIONS:
   --interface, -i            Network interface
   --src-addr, -s             IPv6 Source Address
   --dst-addr, -d             IPv6 Destination Address
   --frag-hdr. -y             Fragment Header
   --dst-opt-hdr, -u          Destination Options Header (Fragmentable Part)
   --dst-opt-u-hdr, -U        Destination Options Header (Unfragmentable Part)
   --hbh-opt-hdr, -H          Hop by Hop Options Header
   --link-src-addr, -S        Link-layer Destination Address
   --link-dst-addr, -D        Link-layer Source Address
   --target, -t               ND IPv6 Target Address
   --target-lla-opt, -E       Source link-layer address option
   --add-tlla-opt, -e         Add Source link-layer address option
   --router, -r               Set the 'Router Flag'
   --solicited, -c            Set the 'Solicited' flag
   --override, -o             Set the 'Override' flag
   --block-src, -j            Block IPv6 Source Address prefix
   --block-dst, -k            Block IPv6 Destination Address prefix
   --block-link-src, -J       Block Ethernet Source Address
   --block-link-dst, -K       Block Ethernet Destination Address
   --block-target, -w         Block ND Target IPv6 prefix
   --accept-src, -b           Accept IPv6 Source Address prefix
   --accept-dst, -g           Accept IPv6 Destination Address prefix
   --accept-link-src, -B      Accept Ethernet Source Address
   --accept-link-dst, -G      Accept Ethernet Destination Address
   --accept-target, -W        Accept ND Target IPv6 prefix
   --flood-targets, -T        Flood with NA's for multiple Target Addresses
   --flood-sources, -F        Number of Source Addresses to forge randomly
   --listen, -L               Listen to Neighbor Solicitation messages
   --loop, -l                 Send periodic Neighbor Advertisements
   --sleep, -z                Pause between sending NA messages
   --help, -h                 Print help for the na6 tool
   --verbose, -v              Be verbose
 
 Programmed by Fernando Gont for SI6 Networks <https://www.si6networks.com>
 Please send any bug reports to <fgont@si6networks.com>
 
 ```
 
 - - -
 
 ##### ni6
 
 A security assessment tool for attack vectors based on ICMPv6 Node Information messages
 
 ```
 root@kali:~# ni6 -h
 SI6 Networks' IPv6 Toolkit v3.0 (Buffy)
 ni6: Security assessment tool for attack vectors based on ICMPv6 NI messages
 
 usage:
  ni6 [-i INTERFACE] [-S LINK_SRC_ADDR | -R] [-D LINK-DST-ADDR] 
      [-s SRC_ADDR[/LEN] | -r] [-d DST_ADDR] [-c HOP_LIMIT] [-y FRAG_SIZE]
      [-u DST_OPT_HDR_SIZE] [-U DST_OPT_U_HDR_SIZE] [-H HBH_OPT_HDR_SIZE] 
      [-P SIZE | -6 IPV6_ADDR | -4 IPV4_ADDR | -n NAME | -N LEN | -x LEN -o TYPE]
      [-Z SIZE] [-e] [-C ICMP6_CODE] [-q NI_QTYPE] [-X NI_FLAGS]
      [-P SIZE | -w IPV6_ADDR | -W IPV4_ADDR | -a NAME | -A LEN | -Q LEN -O TYPE]
      [-E] [-j PREFIX[/LEN]] [-k PREFIX[/LEN]] [-J LINK_ADDR]
      [-K LINK_ADDR] [-b PREFIX[/LEN]] [-g PREFIX[/LEN]] [-B LINK_ADDR]
      [-G LINK_ADDR] [-L | -l] [-z] [-v] [-h]
 
 OPTIONS:
   --interface, -i            Network interface
   --link-src-addr, -S        Link-layer Destination Address
   --link-dst-addr, -D        Link-layer Source Address
   --src-addr, -s             IPv6 Source Address
   --dst-addr, -d             IPv6 Destination Address
   --hop-limit, -c            IPv6 Hop Limit
   --frag-hdr. -y             Fragment Header
   --dst-opt-hdr, -u          Destination Options Header (Fragmentable Part)
   --dst-opt-u-hdr, -U        Destination Options Header (Unfragmentable Part)
   --hbh-opt-hdr, -H          Hop by Hop Options Header
   --payload-size, -P         ICMPv6 NI payload size
   --subject-ipv6. -6         Subject IPv6 Address
   --subject-ipv4, -4         Subject IPv4 address
   --subject-name, -n         Subject Name
   --subject-fname, -N        Forge Subject Name of specific length
   --subject-ename, -x        For (malformed) Subject name of specified length
   --subject-nloop, -o        Subject is a Name with a DNS compression loop
   --max-label-size, -Z       Maximum DNS label size (defaults to 63)
   --sname-slabel, -e         Subject Name is a single-label name
   --code, -C                 ICMPv6 code
   --qtype, -q                ICMPv6 NI Qtype
   --flags, -X                ICMPv6 NI flags
   --data-ipv6, -w            Data IPv6 Address
   --data-ipv4, W             Data IPv4 Address
   --data-name, -a            Data Name
   --data-fname, -A           Forge Data Name of specific length
   --data-ename, -Q           For (malformed) Data Name of specified length
   --data-nloop, -O           Data is a Name with a DNS compression loop
   --dname-slabel, -E         Subject Name is a single-label name
   --block-src, -j            Block IPv6 Source Address prefix
   --block-dst, -k            Block IPv6 Destination Address prefix
   --block-link-src, -J       Block Ethernet Source Address
   --block-link-dst, -K       Block Ethernet Destination Address
   --accept-src, -b           Accept IPv6 Source Address prefix
   --accept-dst, -g           Accept IPv6 Destination Address prefix
   --accept-link-src, -B      Accept Ethernet Source Address
   --accept-link-dst, -G      Accept Ethernet Destination Address
   --forge-src-addr, -r       Forge IPv6 Source Address
   --forge-link-src-addr, -R  Forge link-layer Source Address
   --loop, -l                 Send periodic ICMPv6 error messages
   --sleep, -z                Pause between sending ICMPv6 messages
   --listen, -L               Listen to incoming traffic
   --help, -h                 Print help for the ni6 tool
   --verbose, -v              Be verbose
 
  Programmed by Fernando Gont for SI6 Networks <https://www.si6networks.com>
  Please send any bug reports to <fgont@si6networks.com>
 
 ```
 
 - - -
 
 ##### ns6
 
 A security assessment tool for attack vectors based on ICMPv6 Neighbor Solicitation messages
 
 ```
 root@kali:~# ns6 -h
 SI6 Networks' IPv6 Toolkit v3.0 (Buffy)
 ns6: Security assessment tool for attack vectors based on NS messages
 
 usage: ns6 -i INTERFACE [-s SRC_ADDR[/LEN]] [-d DST_ADDR] [-y FRAG_SIZE] [-u DST_OPT_HDR_SIZE] [-U DST_OPT_U_HDR_SIZE] [-H HBH_OPT_HDR_SIZE] [-S LINK_SRC_ADDR] [-D LINK-DST-ADDR] [-E LINK_ADDR] [-e] [-t TARGET_ADDR[/LEN]] [-F N_SOURCES] [-T N_TARGETS] [-z SECONDS] [-l] [-v] [-h]
 
 OPTIONS:
   --interface, -i            Network interface
   --src-addr, -s             IPv6 Source Address
   --dst-addr, -d             IPv6 Destination Address
   --frag-hdr. -y             Fragment Header
   --dst-opt-hdr, -u          Destination Options Header (Fragmentable Part)
   --dst-opt-u-hdr, -U        Destination Options Header (Unfragmentable Part)
   --hbh-opt-hdr, -H          Hop by Hop Options Header
   --link-src-addr, -S        Link-layer Destination Address
   --link-dst-addr, -D        Link-layer Source Address
   --target-address, -t       ND Target Address
   --source-lla-opt, -E       Source link-layer address option
   --add-slla-opt, -e         Add Source link-layer address option
   --flood-sources, -F        Number of Source Addresses to forge randomly
   --flood-targets, -T        Flood with NA's for multiple Target Addresses
   --loop, -l                 Send Neighbor Solicitations periodically
   --sleep, -z                Pause between peiodic Neighbor Solicitations
   --help, -h                 Print help for the ns6 tool
   --verbose, -v              Be verbose
 
 Programmed by Fernando Gont for SI6 Networks <https://www.si6networks.com>
 Please send any bug reports to <fgont@si6networks.com>
 ```
 
 - - -
 
 ##### path6
 
 A versatile IPv6-based traceroute tool
 
 ```
 root@kali:~# path6 -h
 SI6 Networks' IPv6 Toolkit v3.0 (Buffy)
 path6: A versatile IPv6 traceroute
 
 usage: path6 -d DST_ADDR [-i INTERFACE] [-S LINK_SRC_ADDR] [-D LINK-DST-ADDR]
        [-s SRC_ADDR[/LEN]] [-u DST_OPT_HDR_SIZE] [-U DST_OPT_U_HDR_SIZE]
        [-H HBH_OPT_HDR_SIZE] [-y FRAG:SIZE] [-f FLOW_LABEL]
        [-m MODE] [-p PROBE_TYPE] [-P PAYLOAD_SIZE] [-a DST_PORT] 
        [-X TCP_FLAGS] [-r RATE_LIMIT] [-v] [-h]
 
 OPTIONS:
   --interface, -i           Network interface
   --link-src-addr, -S       Link-layer Destination Address
   --link-dst-addr, -D       Link-layer Source Address
   --src-addr, -s            IPv6 Source Address
   --dst-addr, -d            IPv6 Destination Address
   --frag-hdr. -y            Fragment Header
   --dst-opt-hdr, -u         Destination Options Header (Fragmentable Part)
   --dst-opt-u-hdr, -U       Destination Options Header (Unfragmentable Part)
   --hbh-opt-hdr, -H         Hop by Hop Options Header
   --flow-label, -f          Specifies the Flow Label Value (or 'random')
   --output-mode, -m         Specifies output mode (e.g. 'script')
   --probe-type, -p          Probe type {icmp, tcp, udp, ah, esp}
   --payload-size, -P        Payload Size
   --dst-port, -a            Transport-layer Destination Port
   --tcp-flags, -X           TCP Flags
   --rate-limit, -r          Rate limit the probe packets
   --verbose, -v             Be verbose
   --help, -h                Print help for the path6 tool
 
 Programmed by Fernando Gont for SI6 Networks <https://www.si6networks.com>
 Please send any bug reports to <fgont@si6networks.com>
 
 ```
 
 - - -
 
 ##### ra6
 
 A security assessment tool for attack vectors based on ICMPv6 Router Advertisement messages
 
 ```
 root@kali:~# ra6 -h
 SI6 Networks' IPv6 Toolkit v3.0 (Buffy)
 ra6: Security assessment tool for attack vectors based on RA messages
 
 usage: ra6 -i INTERFACE [-s SRC_ADDR[/LEN]] [-d DST_ADDR] [-y FRAG_SIZE] [-u DST_OPT_HDR_SIZE] [-U DST_OPT_U_HDR_SIZE] [-H HBH_OPT_HDR_SIZE] [-S LINK_SRC_ADDR] [-D LINK_DST_ADDR] [-c CUR_HOP] [-t ROUTER_LIFETIME] [-r REACHABLE_TIME] [-x RETRANS_TIMER] [-m] [-o] [-a] [-q] [-p PREFERENCE] [-E LINK_ADDR] [-e] [-P PREFIX/LEN[#FLAGS[#VALID[#PREFERRED]]]] [-M MTU] [-N [LIFETIME[#DNS_ADDR]]] [-R PREFIX/LEN[#PREF[#LIFETIME]]] [-f N_PREFIXES] [-F N_SOURCES] [-w N_ROUTES] [-W N_ADDRS[#ADDRSPEROPT]] [-j PREFIX[/LEN]] [-k PREFIX[/LEN]] [-J LINK_ADDR] [-K LINK_ADDR] [-b PREFIX[/LEN]] [-g PREFIX[/LEN]] [-B LINK_ADDR] [-G LINK_ADDR]  [-L] [-v] [-h]
 
 OPTIONS:
   --interface, -i            Network interface
   --src-addr, -s             IPv6 Source Address
   --dst-addr, -d             IPv6 Destination Address (or IPv6 prefix when flooding)
   --frag-hdr. -y             Fragment Header
   --dst-opt-hdr, -u          Destination Options Header (Fragmentable Part)
   --dst-opt-u-hdr, -U        Destination Options Header (Unfragmentable Part)
   --hbh-opt-hdr, -H          Hop by Hop Options Header
   --managed, -m              Set de Managed bit
   --other, -o                Set the Other bit
   --home-agent, -a           Set the Home Agent bit
   --nd-proxy, -q             Set the ND Proxy bit
   --lifetime, -t             Router Lifetime
   --reachable, -r            Reachable time
   --preference, -p           Preference
   --retrans, -x              Retrans Timer
   --curhop, -c               CurHop (advised Hop Limit)
   --prefix-opt, -P           Prefix option (Prefix/Len#flags#valid#preferred)
   --mtu-opt, -M              MTU option
   --src-link-opt, -E         Source link-layer address option
   --add-slla-opt, -e         Add Source link-layer address option
   --link-src-addr, -S        Link-layer Source Address
   --link-dst-addr, -D        Link-layer Destination Address
   --route-opt, -R            Route Information option (Prefix/Len#pref#lifetime)
   --rdnss-opt, -N            Recursive DNS Server option (lifetime#IPv6addr)
   --flood-sources, -F        Number of Source Addresses to forge randomly
   --flood-prefixes, -f       Number of Prefix options to forge randomly
   --flood-routes, -w         Number of Route Info options to forge randomly
   --flood-dns, -W            Number of RDNSS options to forge randomly
   --loop, -l                 Send periodic Router Advertisements
   --sleep, -z                Pause between sending RA messages
   --listen, -L               Listen to Router Solicitation messagres
   --block-src, -j            Block IPv6 Source Address prefix
   --block-dst, -k            Block IPv6 Destination Address prefix
   --block-link-src, -J       Block Ethernet Source Address
   --block-link-dst, -K       Block Ethernet Destination Address
   --accept-src, -b           Accept IPv6 Source Address prefix
   --accept-dst, -g           Accept IPv6 Destination Address prefix
   --accept-link-src, -B      Accept Ethernet Source Address
   --accept-link-dst, -G      Accept Ethernet Destination Address
   --verbose, -v              Be verbose
   --help, -h                 Print help for the ra6 tool
 
 Programmed by Fernando Gont for SI6 Networks <https://www.si6networks.com>
 Please send any bug reports to <fgont@si6networks.com>
 ```
 
 - - -
 
 ##### rd6
 
 A security assessment tool for attack vectors based on ICMPv6 Redirect messages
 
 ```
 root@kali:~# rd6 -h
 SI6 Networks' IPv6 Toolkit v3.0 (Buffy)
 rd6: Security assessment tool for attack vectors based on Redirect messages
 
 usage: rd6 [-i INTERFACE] [-s SRC_ADDR[/LEN]] [-d DST_ADDR] [-S LINK_SRC_ADDR] [-D LINK-DST-ADDR] [-A HOP_LIMIT] [-y FRAG_SIZE] [-u DST_OPT_HDR_SIZE] [-U DST_OPT_U_HDR_SIZE] [-H HBH_OPT_HDR_SIZE] [-r RD_DESTADDR/LEN] [-t RD_TARGETADDR/LEN] [-p PAYLOAD_TYPE] [-P PAYLOAD_SIZE] [-n] [-c HOP_LIMIT] [-x SRC_ADDR] [-a SRC_PORT] [-o DST_PORT] [-X TCP_FLAGS] [-q TCP_SEQ] [-Q TCP_ACK] [-V TCP_URP] [-w TCP_WIN] [-M] [-O] [-N] [-E LINK_ADDR] [-e] [-j PREFIX[/LEN]] [-k PREFIX[/LEN]] [-J LINK_ADDR] [-K LINK_ADDR] [-b PREFIX[/LEN]] [-g PREFIX[/LEN]] [-B LINK_ADDR] [-G LINK_ADDR] [-f] [-R N_DESTS] [-T N_TARGETS] [-F N_SOURCES] [-L | -l] [-z] [-v] [-h]
 
 OPTIONS:
   --interface, -i           Network interface
   --src-addr, -s            IPv6 Source Address
   --dst-addr, -d            IPv6 Destination Address
   --hop-limit, -A           IPv6 Hop Limit
   --frag-hdr. -y            Fragment Header
   --dst-opt-hdr, -u         Destination Options Header (Fragmentable Part)
   --dst-opt-u-hdr, -U       Destination Options Header (Unfragmentable Part)
   --hbh-opt-hdr, -H         Hop by Hop Options Header
   --link-src-addr, -S       Link-layer Destination Address
   --link-dst-addr, -D       Link-layer Source Address
   --redir-dest, -r          Redirect Destination Address
   --redir-target, -t        Redirect Target Address
   --payload-type, -p        Redirected Header Payload Type
   --payload-size, -P        Redirected Header Payload Size
   --no-payload, -n          Do not include a Redirected Header Option
   --ipv6-hlim, -c           Redirected Header Payload's Hop Limit
   --peer-addr, -x           Redirected Header Payload's IPv6 Source Address
   --peer-port, -a           Redirected Header Payload's Source Port
   --redir-port, -o          Redirected Header Payload's Destination Port
   --tcp-flags, -X           Redirected Header Payload's TCP Flags
   --tcp-seq, -q             Redirected Header Payload's TCP SEQ Number
   --tcp-ack, -Q             Redirected Header Payload's TCP ACK Number
   --tcp-urg, -V             Redirected Header Payload's TCP URG Pointer
   --tcp-win, -w             Redirected Header Payload's TCP Window
   --resp-mcast, -M          Respond to Multicast Packets
   --make-onlink, -O         Make victim on-link
   --learn-router, -N        Dynamically learn local router addresses
   --target-lla-opt, -E      Target link-layer address option
   --add-tlla-opt, -e        Add Target link-layer address option
   --block-src, -j           Block IPv6 Source Address prefix
   --block-dst, -k           Block IPv6 Destination Address prefix
   --block-link-src, -J      Block Ethernet Source Address
   --block-link-dst, -K      Block Ethernet Destination Address
   --accept-src, -b          Accept IPv6 Source Address prefix
   --accept-dst, -g          Accept IPv6 Destination Address prefix
   --accept-link-src, -B     Accept Ethernet Source Address
   --accept-link-dst, -G     Accept Ethernet Destination Address
   --sanity-filters, -f      Add sanity filters
   --flood-dests, -R         Flood with multiple Redirect Destination Addresses
   --flood-targets, -T       Flood with multiple Redirect Target Addresses
   --flood-sources, -F       Flood with multiple IPv6 Source Addresses
   --listen, -L              Listen to incoming packets
   --loop, -l                Send periodic Redirect messages
   --sleep, -z               Pause between sending Redirect messages
   --help, -h                Print help for the rd6 tool
   --verbose, -v             Be verbose
 
 Programmed by Fernando Gont for SI6 Networks <https://www.si6networks.com>
 Please send any bug reports to <fgont@si6networks.com>
 ```
 
 - - -
 
 ##### rs6
 
 A security assessment tool for attack vectors based on ICMPv6 Router Solicitation messages
 
 ```
 root@kali:~# rs6 -h
 SI6 Networks' IPv6 Toolkit v3.0 (Buffy)
 rs6: Security assessment tool for attack vectors based on RS messages
 
 usage: rs6 -i INTERFACE [-s SRC_ADDR[/LEN]] [-d DST_ADDR] [-y FRAG_SIZE] [-u DST_OPT_HDR_SIZE] [-U DST_OPT_U_HDR_SIZE] [-H HBH_OPT_HDR_SIZE] [-S LINK_SRC_ADDR] [-D LINK-DST-ADDR] [-E LINK_ADDR] [-e] [-F N_SOURCES] [-z SECONDS] [-l] [-v] [-h]
 
 OPTIONS:
   --interface, -i            Network interface
   --src-addr, -s             IPv6 Source Address
   --dst-addr, -d             IPv6 Destination Address
   --frag-hdr. -y             Fragment Header
   --dst-opt-hdr, -u          Destination Options Header (Fragmentable Part)
   --dst-opt-u-hdr, -U        Destination Options Header (Unfragmentable Part)
   --hbh-opt-hdr, -H          Hop by Hop Options Header
   --link-src-addr, -S        Link-layer Destination Address
   --link-dst-addr, -D        Link-layer Source Address
   --src-link-opt, -E         Source link-layer address option
   --add-slla-opt, -e         Add Source link-layer address option
   --flood-sources, -F        Number of Source Addresses to forge randomly
   --loop, -l                 Send Router Solicitations periodically
   --sleep, -z                Pause between peiodic Router Solicitations
   --help, -h                 Print help for the rs6 tool
   --verbose, -v              Be verbose
 
 Programmed by Fernando Gont for SI6 Networks <https://www.si6networks.com>
 Please send any bug reports to <fgont@si6networks.com>
 ```
 
 - - -
 
 ##### scan6
 
 An IPv6 host scanner
 
 ```
 root@kali:~# scan6 -h
 SI6 Networks' IPv6 Toolkit v3.0 (Buffy)
 scan6: An advanced IPv6 scanning tool
 
 usage: scan6 (-L | -d) [-i INTERFACE] [-s SRC_ADDR[/LEN] | -f] 
        [-S LINK_SRC_ADDR | -F] [-p PROBE_TYPE] [-Z PAYLOAD_SIZE] [-o SRC_PORT]
        [-a DST_PORT] [-X TCP_FLAGS] [-P ADDRESS_TYPE] [-q] [-e] [-t]
        [-x RETRANS] [-o TIMEOUT] [-V VM_TYPE] [-b] [-B ENCODING] [-g]
        [-k IEEE_OUI] [-K VENDOR] [-m PREFIXES_FILE] [-w IIDS_FILE] [-W IID]
        [-Q IPV4_PREFIX[/LEN]] [-T] [-I INC_SIZE] [-r RATE(bps|pps)] [-l]
        [-z SECONDS] [-c CONFIG_FILE] [-v] [-h]
 
 OPTIONS:
   --interface, -i             Network interface
   --src-addr, -s              IPv6 Source Address
   --dst-addr, -d              IPv6 Destination Range or Prefix
   --prefixes-file, -m         Prefixes file
   --link-src-addr, -S         Link-layer Destination Address
   --probe-type, -p            Probe type for host scanning {echo, unrec, all}
   --port-scan, -j             Port scan type and range {tcp,udp}:port_low[-port_hi]
   --tcp-scan-type, -G         TCP port-scanning type {syn,fin,null,xmas,ack}
   --payload-size, -Z          TCP/UDP Payload Size
   --src-port, -o              TCP/UDP Source Port
   --dst-port, -a              TCP/UDP Destination Port
   --tcp-flags, -X             TCP Flags
   --print-type, -P            Print address type {local, global, all}
   --print-unique, -q          Print only one IPv6 addresses per Ethernet address
   --print-link-addr, -e       Print link-layer addresses
   --print-timestamp, -t       Print timestamp for each alive node
   --retrans, -x               Number of retransmissions of each probe
   --timeout, -O               Timeout in seconds (default: 1 second)
   --local-scan, -L            Scan the local subnet
   --rand-src-addr, -f         Randomize the IPv6 Source Address
   --rand-link-src-addr, -F    Randomize the Ethernet Source Address
   --tgt-virtual-machines, -V  Target virtual machines
   --tgt-low-byte, -b          Target low-byte addresses
   --tgt-ipv4, -B              Target embedded-IPv4 addresses
   --tgt-port, -g              Target embedded-port addresses
   --tgt-ieee-oui, -k          Target IPv6 addresses embedding IEEE OUI
   --tgt-vendor, -K            Target IPv6 addresses for vendor's IEEE OUIs
   --tgt-iids-file, -w         Target Interface IDs (IIDs) in specified file
   --tgt-iid, -W               Target Interface IDs (IIDs)
   --ipv4-host, -Q             Host IPv4 Address/Prefix
   --sort-ouis, -T             Sort IEEE OUIs
   --inc-size, -I              Increments size
   --rate-limit, -r            Rate limit the address scan to specified rate
   --loop, -l                  Send periodic probes to the specified targets
   --sleep, -z                 Pause between periodic probes
   --config-file, -c           Use alternate configuration file
   --help, -h                  Print help for the scan6 tool
   --verbose, -v               Be verbose
 
  Programmed by Fernando Gont for SI6 Networks <https://www.si6networks.com>
  Please send any bug reports to <fgont@si6networks.com>
 
 ```
 
 - - -
 
 ##### script6
 
 A tool to make complex IPv6 tasks easy script6 SCRIPT [PARAMETERS ]
 
 ```
 root@kali:~# man script6
 SCRIPT6(1)                  General Commands Manual                 SCRIPT6(1)
 
 NAME
        script6 - A tool to make complex IPv6 tasks easy script6 SCRIPT [PARAM-
        ETERS]
 
 DESCRIPTION
        script6 is a set up scripts that make frequent  and/or  rather  complex
        IPv6-related tasks easy.
 
        SCRIPTS
 
        get-aaaa
 
        This script takes no further arguments, and operates as follows:
 
            + The tool reads domain names from standard-input (one per line),
              and obtains the AAAA records for the corresponding domain. If the
              domain name does not contain AAAA records, the tool will add
              the suffix "www.", in the hopes that the resulting domain name
              might contain some.
 
            + Lines where the first non-blank character is the numeral sign (#)
              are consdered to contain comments, and hence are ignored.
 
            + The format of the resulting output is:
 
              # DOMAIN_NAME (CANONIC_NAME)
              IPV6_ADDRESS_1
              IPV6_ADDRESS_2
 
        get-mx
 
        This script takes no further arguments, and operates as follows:
 
            + The tool reads domain names from standard-input (oner per line),
              and obtains the MX for the corresponding domain.
 
            + Lines where the first non-blank character is the numeral sign (#)
              are consdered to contain comments, and hence are ignored.
 
            + The format of the resulting output is:
 
              # DOMAIN_NAME (CANONIC_NAME)
              MX_RECORD_1
              MX_RECORD_2
 
        get-ns
 
        This script takes no further arguments, and operates as follows:
 
            + The tool reads domain names from standard-input (oner per line),
              and obtains the NS records for the corresponding domain.
 
            + Lines where the first non-blank character is the numeral sign (#)
              are consdered to contain comments, and hence are ignored.
 
            + The format of the resulting output is:
 
              # DOMAIN_NAME (CANONIC_NAME)
              NS_RECORD_1
              NS_RECORD_2
 
        get-asn6
 
        Obtain  the  Origin  Autonomous System (AS) number corresponding to the
        specified address.
 
        get-as6
 
        Obtain information about the Origin Autonomous System (AS)  correspond-
        ing  to the specified address.
 
        get-alexa-domains
 
        This script takes no further arguments, and operates as follows:
 
            + It reads from standard input lines with the same format as those
            of Alexa's Top 1M web sites. That is, lines with the following syntax:
 
            RANKING,DOMAIN_NAME
 
            + It extracts the domain name from each line, and prints the
               corresponding domain name to standard output.
 
        This  script  is  typically  useful  for  extracting  domain names from
        Alexa's Top 1M web sites file, such that they can be processed by other
        tools (e.g. the get-aaaa command of script6).
 
        get-trace-stats
 
        This  command  causes  the script6 tool to read from standard input the
        results of a "script6 trace" command (typically piped from a file), and
        produce statistics based on such results.
 
        Among the statistics produced by this command are:
 
           * Packet drop rate: That is, the percentage of destination IPv6
             addresses that result unreachable if IPv6 extension headers are
             employed.
 
           *  Packet  drop  rate  by  different  AS: That is, the percentage of
        packet
             drops that occur at an Autonomous System (AS) other than the AS
             corresponding to the destination IPv6 address.
 
           * Packet drop rate by same AS: That is, the percentage of packet
             drops that occur at the same Autonomous System (AS) as that
             corresponding to the destination IPv6 address.
 
           * Delta-Hops statistics:  Statistics  regarding  the  Delta-Hops  at
        which
             the  packet  drops occur, with "delta-hops" defined as "the number
        of
             hops from the intended destination".
 
        The get-trace-stats performs a number of sanity  checks  on  the  input
        data (i.e., the output from "script6 trace"). For example, if a line of
        input indicates that the last responding node  for  the  non-EH-enabled
        path6 command is not the intended destination, this means that the des-
        tination is unreachable even when no IPv6  extension  headers  are  em-
        ployed, and hence the corresponding line will be discarded.
 
        trace DESTINATION [EHTYPE[EHSIZE]] [PROTOCOL [DESTPORT]]]
 
        The  trace command causes the script6 to read IPv6 addresses from stan-
        dard input (typically piped from a file). For each  IPv6  address,  the
        script6  will  try  to isolate IPv6 blackholes resulting from employing
        IPv6 extension headers. By default, the probe packets (containing  IPv6
        Extension  Headers)  are IPv6 packets with a Destination Options Header
        of 8 bytes, encapsulating an ICMPv6 Echo Request message. However, this
        can  be overridden by specifying the EHTYPE {DO,HBH,FH}, EHSIZE (an in-
        teger), PROTOCOL {tcp,udp,icmpv6}, and DESTPORT (a short  integer)  pa-
        rameters.
 
        The  "trace"  command  of the script6 tool internally employs the path6
        tool of the toolkit as follows. Let us assume that we want  to  isolate
        an   IPv6   blackhole  on  the  path  towards  the  destination  system
        2001:db8:d::1. Firstly, script6 will obtain the output of path6 towards
        such destination:
 
                  1. 2001:db8:1:1000::1
                  2. 2001:db8:2:2000::4
                  3. 2001:db8:2:4000::1
                  4. 2001:db8:3:4000::1
                  5. 2001:db8:3:1000::1
                  6. 2001:db8:4:4000::1
                  7. 2001:db8:4:1000::1
                  8. 2001:db8:5:5000::1
                  9. 2001:db8:5:6000::1
                  10. 2001:db8:d::1
 
        Subsequently, script6 will obtain the output of EH-enabled path6 to the
        same destination:
 
                  1. 2001:db8:1:1000::1
                  2. 2001:db8:2:2000::4
                  3. 2001:db8:2:4000::1
                  4. 2001:db8:3:4000::1
                  5. 2001:db8:3:1000::1
                  6. 2001:db8:4:4000::1
 
        For the sake of brevity, let us refer to the  last-responding  node  in
        the EH-enabled path6 ("2001:db8:4:4000::1" in this case) as "M". Assum-
        ing both packets in both path6 commands employ the same path,  we  will
        refer to "the node following the last responding node in the EH-enabled
        path6" ("2001:db8:4:1000::1" in our case), as "M+1", etc.
 
        Based on traceroute information above, which node is the  one  actually
        dropping  the  EH-enabled  packets  will depend on whether the dropping
        node filters packets on ingress or the egress. If the former, the drop-
        ping node will be M+1.  If the latter, the dropping node will be  "M".
 
        path6 assumes that nodes perform ingress-filtering.  Thus, in our exam-
        ple above the last responding node to the EH-enabled  traceroute  ("M")
        is  "2001:db8:4:4000::1",  and  therefore we assume the "node" dropping
        node to be "2001:db8:4:1000::1" ("M+1").
 
        The resulting output will have the following syntax:
 
                DEST#LAST_NOEH#HOPS_NOEH#LAST_EH$HOPS_EH#DROPN#DROPN2
 
        where:
 
           * DEST: Destination IPv6 address (as read from standard input).
             In our example above, this would be 2001:db8:d::1.
 
           * LAST_NOEH: Last responding IPv6 address for the path6 command
             with no IPv6 extension headers (this will be the same as DEST
             if there is a working path to the destination). In our example
             above, this would be 2001:db8:d::1.
 
           * HOPS_NOEH: Number of hops to LAST_NOEH. In our example above,
             this would be "10".
 
           * LAST_EH: Last responding IPv6 address in the EH-enabled path6
             command. In our example above, this would be 2001:db8:4:4000::1.
 
           * HOPS_EH: Number of hops to LAST_EH. In our example above, this
             would be "6".
 
           * DROPN: Dropping node (M+1 in our explanation above). In our
             example above, this would be 2001:db8:4:1000::1.
 
           * DROPN: Node after the dropping node (M+2). In our example,
             this would be 2001:db8:5:5000::1.
 
        The output of the "trace" command is meant to be processed by the  get-
        trace-stats command of the script6 tool. Please check the blackhole6(1)
        tool for a more human-friendly tool for isolating IPv6 blackholes.
 
 EXAMPLES
        The following sections illustrate typical  use  cases  of  the  script6
        tool.
 
        Example #1
 
        $ script6 get-asn 2001:db8::1
 
        Obtain  the  Origin  Autonomous System (AS) number corresponding to the
        IPv6 address 2001:db8::1.
 
        Example #2
 
        $ script6 get-as 2001:db8::1
 
        Obtain information about the Origin Autonomous System (AS)  correspond-
        ing to the IPv6 address 2001:db8::1.
 
        Example #3
 
        $ cat domains.txt | script6 get-aaaa > domains-aaaa.txt
 
        Map  the  domain  names  contained  in the file "domains.txt" into AAAA
        records, and save the results in the file "domains-aaaa.txt".
 
        Example #4
 
        # cat domains-aaaa.txt | script6 trace do8  tcp  port  25  >  trace-re-
        sults.txt
 
        Find  IPv6  blackholes  in  the path to each of the IPv6 addresses con-
        tained in the file "domains-aaaa.txt" (one per line), and save the  re-
        sults to the file "trace-results.txt". The probe packets to be employed
        are IPv6 packets with a Destination Options header of 8 bytes, encapsu-
        lating a TCP segment with the Destinatio Port set to 25.
 
        Example #5
 
        $ cat trace-results.txt | script6 get-trace-stats
 
        Produce  statistics based on the trace results from the file "trace-re-
        sults.txt" (produced with "script6 trace").
 
 SEE ALSO
        blackhole6(1) path6(1)
 
        IETF RFC7872 (available at: <http://tools.ietf.org/html/rfc7872>) for a
        discussion of support of IPv6 Extension Headers in the public Internet.
 
 AUTHOR
        The  script6  tool  and the corresponding manual pages were produced by
        Fernando    Gont    <fgont@si6networks.com>    for     SI6     Networks
        <http://www.si6networks.com>.
 
 COPYRIGHT
        Copyright (c) 2014-2015 Fernando Gont.
 
        Permission  is  granted to copy, distribute and/or modify this document
        under the terms of the GNU Free Documentation License, Version  1.3  or
        any  later  version  published by the Free Software Foundation; with no
        Invariant Sections, no Front-Cover Texts, and no Back-Cover  Texts.   A
        copy   of   the   license   is   available  at  <http://www.gnu.org/li-
        censes/fdl.html>.
 
                                                                     SCRIPT6(1)
 ```
 
 - - -
 
 ##### tcp6
 
 A security assessment tool for TCP/IPv6 implementations
 
 ```
 root@kali:~# tcp6 -h
 SI6 Networks' IPv6 Toolkit v3.0 (Buffy)
 tcp6: Security assessment tool for attack vectors based on TCP/IPv6 packets
 
 usage: tcp6 [-i INTERFACE] [-S LINK_SRC_ADDR] [-D LINK-DST-ADDR] [-s SRC_ADDR[/LEN]] [-d DST_ADDR] [-A HOP_LIMIT] [-y FRAG_SIZE] [-u DST_OPT_HDR_SIZE] [-U DST_OPT_U_HDR_SIZE] [-H HBH_OPT_HDR_SIZE] [-P PAYLOAD_SIZE] [-o SRC_PORT[/LEN]] [-a DST_PORT[/LEN]] [-X TCP_FLAGS] [-q TCP_SEQ] [-Q TCP_ACK] [-V TCP_URP] [-w TCP_WIN] [-c OPEN_MODE] [-C CLOSE_MODE] [-Z DATA] [-P PAYLOAD_SIZE] [-W WIN_MODE][-M WIN_MOD_MODE] [-r RATE] [-p PROBE_MODE] [-x RETRANS] [-N] [-n] [-j PREFIX[/LEN]] [-k PREFIX[/LEN]] [-J LINK_ADDR] [-K LINK_ADDR] [-b PREFIX[/LEN]] [-g PREFIX[/LEN]] [-B LINK_ADDR] [-G LINK_ADDR] [-F N_SOURCES] [-T N_PORTS] [-L | -l] [-z SECONDS] [-v] [-h]
 
 OPTIONS:
   --interface, -i           Network interface
   --src-addr, -s            IPv6 Source Address
   --dst-addr, -d            IPv6 Destination Address
   --hop-limit, -A           IPv6 Hop Limit
   --frag-hdr. -y            Fragment Header
   --dst-opt-hdr, -u         Destination Options Header (Fragmentable Part)
   --dst-opt-u-hdr, -U       Destination Options Header (Unfragmentable Part)
   --hbh-opt-hdr, -H         Hop by Hop Options Header
   --link-src-addr, -S       Link-layer Destination Address
   --link-dst-addr, -D       Link-layer Source Address
   --payload-size, -P        TCP Payload Size
   --src-port, -o            TCP Source Port (PORT[/LEN])
   --dst-port, -a            TCP Destination Port (PORT[/LEN])
   --tcp-flags, -X           TCP Flags
   --tcp-seq, -q             TCP Sequence Number
   --tcp-ack, -Q             TCP Acknowledgment Number
   --not-ack-data, -N        Do not acknowledge the TCP payload
   --not-ack-flags, -n       Do not acknowledge the TCP flags
   --tcp-urg, -V             TCP Urgent Pointer
   --tcp-win, -w             TCP Window
   --window-mode, -W         TCP Window mode {close,modulate}
   --win-modulation, -M      TCP Window modulation (WIN1:TIME1:WIN2:TIME2)
   --open-mode, -c           Open mode {simultaneous,passive,abort,active}
   --close-mode, -C          Close mode {simultaneous,passive,abort
                             active,FIN-WAIT-1,FIN-WAIT-2,LAST-ACK}
   --data, -Z                TCP payload data
   --rate-limit, -r          Rate limit the address scan to specified rate
   --probe-mode, -p          TCP probe mode {dump,script}
   --retrans, -x             Set number of TCP retransmissions
   --block-src, -j           Block IPv6 Source Address prefix
   --block-dst, -k           Block IPv6 Destination Address prefix
   --block-link-src, -J      Block Ethernet Source Address
   --block-link-dst, -K      Block Ethernet Destination Address
   --accept-src, -b          Accept IPv6 Source Address prefix
   --accept-dst, -g          Accept IPv6 Destination Address prefix
   --accept-link-src, -B     Accept Ethernet Source Address
   --accept-link-dst, -G     Accept Ethernet Destination Address
   --flood-sources, -F       Flood from multiple IPv6 Source Addresses
   --flood-ports, -T         Flood from multiple TCP Source Ports
   --listen, -L              Listen to incoming packets
   --loop, -l                Send periodic TCP segments
   --sleep, -z               Pause between sending TCP segments
   --help, -h                Print help for the tcp6 tool
   --verbose, -v             Be verbose
 
 Programmed by Fernando Gont for SI6 Networks <https://www.si6networks.com>
 Please send any bug reports to <fgont@si6networks.com>
 
 ```
 
 - - -
 
 ##### udp6
 
 A security assessment tool for UDP/IPv6 implementations
 
 ```
 root@kali:~# udp6 -h
 SI6 Networks' IPv6 Toolkit v3.0 (Buffy)
 udp6: Security assessment tool for attack vectors based on UDP/IPv6 packets
 
 usage: udp6 [-i INTERFACE] [-S LINK_SRC_ADDR] [-D LINK-DST-ADDR] [-s SRC_ADDR[/LEN]] [-d DST_ADDR] [-A HOP_LIMIT] [-y FRAG_SIZE] [-u DST_OPT_HDR_SIZE] [-U DST_OPT_U_HDR_SIZE] [-H HBH_OPT_HDR_SIZE] [-P PAYLOAD_SIZE] [-o SRC_PORT[/LEN]] [-a DST_PORT[/LEN]] [-N] [-f] [-j PREFIX[/LEN]] [-k PREFIX[/LEN]] [-J LINK_ADDR] [-K LINK_ADDR] [-b PREFIX[/LEN]] [-g PREFIX[/LEN]] [-B LINK_ADDR] [-G LINK_ADDR] [-F N_SOURCES] [-T N_PORTS] [-L | -l] [-z SECONDS] [-v] [-h]
 
 OPTIONS:
   --interface, -i           Network interface
   --src-addr, -s            IPv6 Source Address (ADDRESSS[/LEN])
   --dst-addr, -d            IPv6 Destination Address
   --hop-limit, -A           IPv6 Hop Limit
   --frag-hdr. -y            Fragment Header
   --dst-opt-hdr, -u         Destination Options Header (Fragmentable Part)
   --dst-opt-u-hdr, -U       Destination Options Header (Unfragmentable Part)
   --hbh-opt-hdr, -H         Hop by Hop Options Header
   --link-src-addr, -S       Link-layer Destination Address
   --link-dst-addr, -D       Link-layer Source Address
   --payload-size, -P        UDP Payload Size
   --src-port, -o            UDP Source Port (PORT[/LEN])
   --dst-port, -a            UDP Destination Port (PORT[/LEN])
   --data, -Z                UDP payload data
   --rate-limit, -r          Rate limit the address scan to specified rate
   --probe-mode, -p          UDP probe mode {dump,script}
   --block-src, -j           Block IPv6 Source Address prefix
   --block-dst, -k           Block IPv6 Destination Address prefix
   --block-link-src, -J      Block Ethernet Source Address
   --block-link-dst, -K      Block Ethernet Destination Address
   --accept-src, -b          Accept IPv6 Source Address prefix
   --accept-dst, -g          Accept IPv6 Destination Address prefix
   --accept-link-src, -B     Accept Ethernet Source Address
   --accept-link-dst, -G     Accept Ethernet Destination Address
   --flood-sources, -F       Flood from multiple IPv6 Source Addresses
   --flood-ports, -T         Flood from multiple UDP Source Ports
   --listen, -L              Listen to incoming packets
   --loop, -l                Send periodic UDP segments
   --sleep, -z               Pause between sending UDP segments
   --help, -h                Print help for the udp6 tool
   --verbose, -v             Be verbose
 
 Programmed by Fernando Gont for SI6 Networks <https://www.si6networks.com>
 Please send any bug reports to <fgont@si6networks.com>
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
