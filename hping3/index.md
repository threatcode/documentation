---
Title: hping3
Homepage: http://www.hping.org/
Repository: https://salsa.debian.org/debian/hping3
Architectures: any
Version: 3.a2.ds2-10
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-information-gathering kali-tools-vulnerability 
Icon: images/hping3-logo.svg
PackagesInfo: |
 ### hping3
 
  hping3 is a network tool able to send custom ICMP/UDP/TCP packets and
  to display target replies like ping does with ICMP replies. It handles
  fragmentation and arbitrary packet body and size, and can be used to
  transfer files under supported protocols. Using hping3, you can test
  firewall rules, perform (spoofed) port scanning, test network
  performance using different protocols, do path MTU discovery, perform
  traceroute-like actions under different protocols, fingerprint remote
  operating systems, audit TCP/IP stacks, etc.  hping3 is scriptable
  using the Tcl language.
 
 **Installed size:** `254 KB`  
 **How to install:** `sudo apt install hping3`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libpcap0.8 
 * libtcl8.6 
 {{< /spoiler >}}
 
 ##### hping3
 
 Send (almost) arbitrary TCP/IP packets to network hosts
 
 ```
 root@kali:~# hping3 -h
 usage: hping3 host [options]
   -h  --help      show this help
   -v  --version   show version
   -c  --count     packet count
   -i  --interval  wait (uX for X microseconds, for example -i u1000)
       --fast      alias for -i u10000 (10 packets for second)
       --faster    alias for -i u1000 (100 packets for second)
       --flood	   sent packets as fast as possible. Don't show replies.
   -n  --numeric   numeric output
   -q  --quiet     quiet
   -I  --interface interface name (otherwise default routing interface)
   -V  --verbose   verbose mode
   -D  --debug     debugging info
   -z  --bind      bind ctrl+z to ttl           (default to dst port)
   -Z  --unbind    unbind ctrl+z
       --beep      beep for every matching packet received
 Mode
   default mode     TCP
   -0  --rawip      RAW IP mode
   -1  --icmp       ICMP mode
   -2  --udp        UDP mode
   -8  --scan       SCAN mode.
                    Example: hping --scan 1-30,70-90 -S www.target.host
   -9  --listen     listen mode
 IP
   -a  --spoof      spoof source address
   --rand-dest      random destionation address mode. see the man.
   --rand-source    random source address mode. see the man.
   -t  --ttl        ttl (default 64)
   -N  --id         id (default random)
   -W  --winid      use win* id byte ordering
   -r  --rel        relativize id field          (to estimate host traffic)
   -f  --frag       split packets in more frag.  (may pass weak acl)
   -x  --morefrag   set more fragments flag
   -y  --dontfrag   set don't fragment flag
   -g  --fragoff    set the fragment offset
   -m  --mtu        set virtual mtu, implies --frag if packet size > mtu
   -o  --tos        type of service (default 0x00), try --tos help
   -G  --rroute     includes RECORD_ROUTE option and display the route buffer
   --lsrr           loose source routing and record route
   --ssrr           strict source routing and record route
   -H  --ipproto    set the IP protocol field, only in RAW IP mode
 ICMP
   -C  --icmptype   icmp type (default echo request)
   -K  --icmpcode   icmp code (default 0)
       --force-icmp send all icmp types (default send only supported types)
       --icmp-gw    set gateway address for ICMP redirect (default 0.0.0.0)
       --icmp-ts    Alias for --icmp --icmptype 13 (ICMP timestamp)
       --icmp-addr  Alias for --icmp --icmptype 17 (ICMP address subnet mask)
       --icmp-help  display help for others icmp options
 UDP/TCP
   -s  --baseport   base source port             (default random)
   -p  --destport   [+][+]<port> destination port(default 0) ctrl+z inc/dec
   -k  --keep       keep still source port
   -w  --win        winsize (default 64)
   -O  --tcpoff     set fake tcp data offset     (instead of tcphdrlen / 4)
   -Q  --seqnum     shows only tcp sequence number
   -b  --badcksum   (try to) send packets with a bad IP checksum
                    many systems will fix the IP checksum sending the packet
                    so you'll get bad UDP/TCP checksum instead.
   -M  --setseq     set TCP sequence number
   -L  --setack     set TCP ack
   -F  --fin        set FIN flag
   -S  --syn        set SYN flag
   -R  --rst        set RST flag
   -P  --push       set PUSH flag
   -A  --ack        set ACK flag
   -U  --urg        set URG flag
   -X  --xmas       set X unused flag (0x40)
   -Y  --ymas       set Y unused flag (0x80)
   --tcpexitcode    use last tcp->th_flags as exit code
   --tcp-mss        enable the TCP MSS option with the given value
   --tcp-timestamp  enable the TCP timestamp option to guess the HZ/uptime
 Common
   -d  --data       data size                    (default is 0)
   -E  --file       data from file
   -e  --sign       add 'signature'
   -j  --dump       dump packets in hex
   -J  --print      dump printable characters
   -B  --safe       enable 'safe' protocol
   -u  --end        tell you when --file reached EOF and prevent rewind
   -T  --traceroute traceroute mode              (implies --bind and --ttl 1)
   --tr-stop        Exit when receive the first not ICMP in traceroute mode
   --tr-keep-ttl    Keep the source TTL fixed, useful to monitor just one hop
   --tr-no-rtt	    Don't calculate/show RTT information in traceroute mode
 ARS packet description (new, unstable)
   --apd-send       Send the packet described with APD (see docs/APD.txt)
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## hping3 Usage Example

Use traceroute mode (`--traceroute`), be verbose (`-V`) in ICMP mode (`-1`) against the target (`www.example.com`):

```
root@kali:~# hping3 --traceroute -V -1 www.example.com
using eth0, addr: 192.168.1.15, MTU: 1500
HPING www.example.com (eth0 93.184.216.119): icmp mode set, 28 headers + 0 data bytes
hop=1 TTL 0 during transit from ip=192.168.1.1 name=UNKNOWN
hop=1 hoprtt=0.3 ms
hop=2 TTL 0 during transit from ip=192.168.0.1 name=UNKNOWN
hop=2 hoprtt=3.3 ms
```
