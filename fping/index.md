---
Title: fping
Homepage: https://www.fping.org/
Repository: https://salsa.debian.org/debian/fping
Architectures: any
Version: 5.1-1
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-information-gathering 
Icon: images/fping-logo.svg
PackagesInfo: |
 ### fping
 
  fping is a ping like program which uses the Internet Control Message Protocol
  (ICMP) echo request to determine if a target host is responding.  fping
  differs from ping in that you can specify any number of targets on the command
  line, or specify a file containing the lists of targets to ping.  Instead of
  sending to one target until it times out or replies, fping will send out a
  ping packet and move on to the next target in a round-robin fashion.
 
 **Installed size:** `93 KB`  
 **How to install:** `sudo apt install fping`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libcap2-bin
 * netbase
 {{< /spoiler >}}
 
 ##### fping
 
 Send ICMP ECHO_REQUEST packets to network hosts
 
 ```
 root@kali:~# fping -h
 Usage: fping [options] [targets...]
 
 Probing options:
    -4, --ipv4         only ping IPv4 addresses
    -6, --ipv6         only ping IPv6 addresses
    -b, --size=BYTES   amount of ping data to send, in bytes (default: 56)
    -B, --backoff=N    set exponential backoff factor to N (default: 1.5)
    -c, --count=N      count mode: send N pings to each target
    -f, --file=FILE    read list of targets from a file ( - means stdin)
    -g, --generate     generate target list (only if no -f specified)
                       (give start and end IP in the target list, or a CIDR address)
                       (ex. fping -g 192.168.1.0 192.168.1.255 or fping -g 192.168.1.0/24)
    -H, --ttl=N        set the IP TTL value (Time To Live hops)
    -I, --iface=IFACE  bind to a particular interface
    -l, --loop         loop mode: send pings forever
    -m, --all          use all IPs of provided hostnames (e.g. IPv4 and IPv6), use with -A
    -M, --dontfrag     set the Don't Fragment flag
    -O, --tos=N        set the type of service (tos) flag on the ICMP packets
    -p, --period=MSEC  interval between ping packets to one target (in ms)
                       (in loop and count modes, default: 1000 ms)
    -r, --retry=N      number of retries (default: 3)
    -R, --random       random packet data (to foil link data compression)
    -S, --src=IP       set source address
    -t, --timeout=MSEC individual target initial timeout (default: 500 ms,
                       except with -l/-c/-C, where it's the -p period up to 2000 ms)
 
 Output options:
    -a, --alive        show targets that are alive
    -A, --addr         show targets by address
    -C, --vcount=N     same as -c, report results in verbose format
    -d, --rdns         show targets by name (force reverse-DNS lookup)
    -D, --timestamp    print timestamp before each output line
    -e, --elapsed      show elapsed time on return packets
    -i, --interval=MSEC  interval between sending ping packets (default: 10 ms)
    -n, --name         show targets by name (reverse-DNS lookup for target IPs)
    -N, --netdata      output compatible for netdata (-l -Q are required)
    -o, --outage       show the accumulated outage time (lost packets * packet interval)
    -q, --quiet        quiet (don't show per-target/per-ping results)
    -Q, --squiet=SECS  same as -q, but add interval summary every SECS seconds
    -s, --stats        print final stats
    -u, --unreach      show targets that are unreachable
    -v, --version      show version
    -x, --reachable=N  shows if >=N hosts are reachable or not
 ```
 
 - - -
 
 ##### fping6
 
 Backwards compatibility with fping below version 4.0
 
 ```
 root@kali:~# fping6 -h
 Usage: fping6 [options] [targets...]
 
 Probing options:
    -4, --ipv4         only ping IPv4 addresses
    -6, --ipv6         only ping IPv6 addresses
    -b, --size=BYTES   amount of ping data to send, in bytes (default: 56)
    -B, --backoff=N    set exponential backoff factor to N (default: 1.5)
    -c, --count=N      count mode: send N pings to each target
    -f, --file=FILE    read list of targets from a file ( - means stdin)
    -g, --generate     generate target list (only if no -f specified)
                       (give start and end IP in the target list, or a CIDR address)
                       (ex. fping6 -g 192.168.1.0 192.168.1.255 or fping6 -g 192.168.1.0/24)
    -H, --ttl=N        set the IP TTL value (Time To Live hops)
    -I, --iface=IFACE  bind to a particular interface
    -l, --loop         loop mode: send pings forever
    -m, --all          use all IPs of provided hostnames (e.g. IPv4 and IPv6), use with -A
    -M, --dontfrag     set the Don't Fragment flag
    -O, --tos=N        set the type of service (tos) flag on the ICMP packets
    -p, --period=MSEC  interval between ping packets to one target (in ms)
                       (in loop and count modes, default: 1000 ms)
    -r, --retry=N      number of retries (default: 3)
    -R, --random       random packet data (to foil link data compression)
    -S, --src=IP       set source address
    -t, --timeout=MSEC individual target initial timeout (default: 500 ms,
                       except with -l/-c/-C, where it's the -p period up to 2000 ms)
 
 Output options:
    -a, --alive        show targets that are alive
    -A, --addr         show targets by address
    -C, --vcount=N     same as -c, report results in verbose format
    -d, --rdns         show targets by name (force reverse-DNS lookup)
    -D, --timestamp    print timestamp before each output line
    -e, --elapsed      show elapsed time on return packets
    -i, --interval=MSEC  interval between sending ping packets (default: 10 ms)
    -n, --name         show targets by name (reverse-DNS lookup for target IPs)
    -N, --netdata      output compatible for netdata (-l -Q are required)
    -o, --outage       show the accumulated outage time (lost packets * packet interval)
    -q, --quiet        quiet (don't show per-target/per-ping results)
    -Q, --squiet=SECS  same as -q, but add interval summary every SECS seconds
    -s, --stats        print final stats
    -u, --unreach      show targets that are unreachable
    -v, --version      show version
    -x, --reachable=N  shows if >=N hosts are reachable or not
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
