---
Title: ngrep
Homepage: https://github.com/jpr5/ngrep
Repository: https://salsa.debian.org/rfrancoise/ngrep
Architectures: any
Version: 1.47+ds1-5
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### ngrep
 
  ngrep strives to provide most of GNU grep's common features,
  applying them to the network layer.  ngrep is a pcap-aware tool that
  will allow you to specify extended regular expressions to match
  against data payloads of packets.  It currently recognizes TCP, UDP
  and ICMP across Ethernet, PPP, SLIP and null interfaces, and
  understands bpf filter logic in the same fashion as more common
  packet sniffing tools, such as tcpdump and snoop.
 
 **Installed size:** `78 KB`  
 **How to install:** `sudo apt install ngrep`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libnet1 
 * libpcap0.8 
 * libpcre2-8-0 
 {{< /spoiler >}}
 
 ##### ngrep
 
 Network grep
 
 ```
 root@kali:~# ngrep -h
 usage: ngrep <-hNXViwqpevxlDtTRM> <-IO pcap_dump> <-n num> <-d dev> <-A num>
              <-s snaplen> <-S limitlen> <-W normal|byline|single|none> <-c cols>
              <-P char> <-F file>             <-K count>
              <match expression> <bpf filter>
    -h  is help/usage
    -V  is version information
    -q  is be quiet (don't print packet reception hash marks)
    -e  is show empty packets
    -i  is ignore case
    -v  is invert match
    -R  is don't do privilege revocation logic
    -x  is print in alternate hexdump format
    -X  is interpret match expression as hexadecimal
    -w  is word-regex (expression must match as a word)
    -p  is don't go into promiscuous mode
    -l  is make stdout line buffered
    -D  is replay pcap_dumps with their recorded time intervals
    -t  is print timestamp every time a packet is matched
    -T  is print delta timestamp every time a packet is matched
          specify twice for delta from first match
    -M  is don't do multi-line match (do single-line match instead)
    -I  is read packet stream from pcap format file pcap_dump
    -O  is dump matched packets in pcap format to pcap_dump
    -n  is look at only num packets
    -A  is dump num packets after a match
    -s  is set the bpf caplen
    -S  is set the limitlen on matched packets
    -W  is set the dump format (normal, byline, single, none)
    -c  is force the column width to the specified size
    -P  is set the non-printable display char to what is specified
    -F  is read the bpf filter from the specified file
    -N  is show sub protocol number
    -d  is use specified device instead of the pcap default
    -K  is send N packets to kill observed connections
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
