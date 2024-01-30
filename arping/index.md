---
Title: arping
Homepage: http://www.habets.pp.se/synscan/programs.php?prog=arping
Repository: https://salsa.debian.org/debian/arping
Architectures: any
Version: 2.23-1
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-information-gathering 
Icon: images/arping-logo.svg
PackagesInfo: |
 ### arping
 
  The arping utility sends ARP and/or ICMP requests to the specified host
  and displays the replies. The host may be specified by its hostname,
  its IP address, or its MAC address.
 
 **Installed size:** `77 KB`  
 **How to install:** `sudo apt install arping`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libnet1 
 * libpcap0.8 
 * libseccomp2 
 {{< /spoiler >}}
 
 ##### arping
 
 Sends arp and/or ip pings to a given host
 
 ```
 root@kali:~# arping --help
 ARPing 2.23, by Thomas Habets <thomas@habets.se>
 usage: arping [ -0aAbdDeFpPqrRuUvzZ ] [ -w <sec> ] [ -W <sec> ] [ -S <host/ip> ]
               [ -T <host/ip ] [ -s <MAC> ] [ -t <MAC> ] [ -c <count> ]
               [ -C <count> ] [ -i <interface> ] [ -m <type> ] [ -g <group> ]
               [ -V <vlan> ] [ -Q <priority> ] <host/ip/MAC | -B>
 
 Options:
 
     -0     Use this option to ping with source IP address 0.0.0.0. Use this
            when you haven't configured your interface yet.  Note that  this
            may  get  the  MAC-ping  unanswered.   This  is  an alias for -S
            0.0.0.0.
     -a     Audiable ping.
     -A     Only count addresses matching  requested  address  (This  *WILL*
            break  most things you do. Only useful if you are arpinging many
            hosts at once. See arping-scan-net.sh for an example).
     -b     Like -0 but source broadcast source  address  (255.255.255.255).
            Note that this may get the arping unanswered since it's not nor-
            mal behavior for a host.
     -B     Use instead of host if you want to address 255.255.255.255.
     -c count
            Only send count requests.
     -C count
            Only wait for this many replies, regardless of -c and -w.
     -d     Find duplicate replies. Exit with 1 if there are answers from
            two different MAC addresses.
     -D     Display answers as exclamation points and missing packets as dots.
     -e     Like -a but beep when there is no reply.
     -F     Don't try to be smart about the interface name.  (even  if  this
            switch is not given, -i overrides smartness)
     -g group
            setgid() to this group instead of the nobody group.
     -h     Displays a help message and exits.
     -i interface
            Use the specified interface.
     -m type
            Type of timestamp to use for incoming packets. Use -vv when
            pinging to list available ones.
     -q     Does not display messages, except error messages.
     -Q pri 802.1p priority to set. Should be used with 802.1Q (-V).
            Defaults to 0.
     -r     Raw output: only the MAC/IP address is displayed for each reply.
     -R     Raw output: Like -r but shows "the other one", can  be  combined
            with -r.
     -s MAC Set source MAC address. You may need to use -p with this.
     -S IP  Like  -b and -0 but with set source address.  Note that this may
            get the arping unanswered if the target does not have routing to
            the  IP.  If you don't own the IP you are using, you may need to
            turn on promiscious mode on the interface (with -p).  With  this
            switch  you can find out what IP-address a host has without tak-
            ing an IP-address yourself.
     -t MAC Set target MAC address to use when pinging IP address.
     -T IP  Use -T as target address when pinging MACs that won't respond to
            a broadcast ping but perhaps to a directed broadcast.
            Example:
            To check the address of MAC-A, use knowledge of MAC-B and  IP-B.
            $ arping -S <IP-B> -s <MAC-B> -p <MAC-A>
     -p     Turn  on  promiscious  mode  on interface, use this if you don't
            "own" the MAC address you are using.
     -P     Send ARP replies instead of requests. Useful with -U.
     -u     Show index=received/sent instead  of  just  index=received  when
            pinging MACs.
     -U     Send unsolicited ARP.
     -v     Verbose output. Use twice for more messages.
     -V num 802.1Q tag to add. Defaults to no VLAN tag.
     -w sec Specify a timeout before ping exits regardless of how many
            packets have been sent or received.
     -W sec Time to wait between pings.
     -z     Enable seccomp
     -Z     Disable seccomp (default)
 Report bugs to: thomas@habets.se
 Arping home page: <http://www.habets.pp.se/synscan/>
 Development repo: http://github.com/ThomasHabets/arping
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
