---
Title: arp-scan
Homepage: https://github.com/royhills/arp-scan
Repository: https://salsa.debian.org/pkg-security-team/arp-scan
Architectures: any
Version: 1.10.0-2
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### arp-scan
 
  arp-scan is a command-line tool that uses the ARP protocol to discover and
  fingerprint IP hosts on the local network. It is available for Linux and BSD
  under the GPL licence
 
 **Installed size:** `1.53 MB`  
 **How to install:** `sudo apt install arp-scan`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libcap2 
 * libpcap0.8 
 {{< /spoiler >}}
 
 ##### arp-fingerprint
 
 Fingerprint a system using ARP
 
 ```
 root@kali:~# arp-fingerprint -h
 Usage: arp-fingerprint [options] <target>
 Fingerprint the target system using arp-scan.
 
 'options' is one or more of:
         -h Display this usage message.
         -v Give verbose progress messages.
 	-o <option-string> Pass specified options to arp-scan
 	-l Fingerprint all targets in the local net.
 
 ```
 
 - - -
 
 ##### arp-scan
 
 Send ARP requests to target hosts and display responses
 
 ```
 root@kali:~# arp-scan -h
 Usage: arp-scan [options] [hosts...]
 
 Target hosts must be specified on the command line unless the --file or
 --localnet option is used.
 
 arp-scan uses raw sockets, which requires privileges on some systems:
 
 Linux with POSIX.1e capabilities support using libcap:
        arp-scan is capabilities aware. It requires CAP_NET_RAW in the permitted
        set and only enables that capability for the required functions.
 BSD and macOS:
        You need read/write access to /dev/bpf*
 Any operating system:
        Running as root or SUID root will work on any OS but other methods
        are preferable where possible.
 
 Targets can be IPv4 addresses or hostnames. You can also use CIDR notation
 (10.0.0.0/24) (network and broadcast included), ranges (10.0.0.1-10.0.0.10),
 and network:mask (10.0.0.0:255.255.255.0).
 
 Options:
 
 The data type for option arguments is shown by a letter in angle brackets: 
 
 <s> Character string.
 <i> Decimal integer, or hex if preceeded by 0x e.g. 2048 or 0x800.
 <f> Floating point decimal number.
 <m> MAC address, e.g. 01:23:45:67:89:ab or 01-23-45-67-89-ab (case insensitive)
 <a> IPv4 address e.g. 10.0.0.1
 <h> Hex encoded binary data. No leading 0x. (case insensitive).
 <x> Something else - see option description.
 
 General Options:
 
 --help or -h		Display this usage message and exit.
 
 --verbose or -v		Display verbose progress messages.
 			Can be used than once to increase verbosity. Max=3.
 
 --version or -V		Display program version details and exit.
 			Shows the version, license details, libpcap version,
 			and whether POSIX.1e capability support is included.
 
 --interface=<s> or -I <s> Use network interface <s>.
 			If this option is not specified, arp-scan will search
 			the system interface list for the lowest numbered,
 			configured up interface (excluding loopback).
 
 Host Selection:
 
 --file=<s> or -f <s>	Read hostnames or addresses from the specified file
 			One name or address pattern per line. Use "-" for stdin.
 
 --localnet or -l	Generate addresses from interface configuration.
 			Generates list from interface address and netmask
 			(network and broadcast included). You cannot use the
 			--file option or give targets on the command line.
 			Use --interface to specify the interface.
 
 MAC/Vendor Mapping Files:
 
 --ouifile=<s> or -O <s>	Use IEEE registry vendor mapping file <s>.
 			Default is ieee-oui.txt in the current directory. If
 			that is not found /usr/share/arp-scan/ieee-oui.txt
 			is used.
 
 --macfile=<s> or -m <s>	Use custom vendor mapping file <s>.
 			Default is mac-vendor.txt in the current directory.
 			If that is not found
 			/etc/arp-scan/mac-vendor.txt is used.
 
 Output Format Control:
 
 --quiet or -q		Display minimal output for each responding host.
 			Only the IP address and MAC address are displayed.
 			Reduces memory usage by about 5MB because the
 			vendor mapping files are not used. Only the ${ip}
 			and ${mac} fields are available for the --format
 			option if --quiet is specified.
 
 --plain or -x		Supress header and footer text.
 			Only display the responding host details. Useful if
 			the output will be parsed by a script.
 
 --ignoredups or -g	Don't display duplicate packets.
 			By default duplicate packets are flagged with
 			"(DUP: n)" where n is the number of times this
 			host has responded.
 
 --rtt or -D		Calculate and display the packet round-trip time.
 			The time is displayed in milliseconds and fractional
 			microseconds. Makes the ${rtt} field available for
 			--format.
 
 --format=<s> or -F <s>	Specify the output format string.
 			The format is a string that will be output for each
 			responding host. Host details can be included by
 			inserting references to fields using the syntax
 			"${field[;width]}". Fields are displayed right-
 			aligned unless the width is negative in which case
 			left alignment will be used. The following case-
 			insensitive field names are recognised:
 
 			IP	Host IPv4 address in dotted quad format
 			Name	Host name if --resolve option given
 			MAC	Host MAC address xx:xx:xx:xx:xx:xx
 			HdrMAC	Ethernet source addr if different
 			Vendor	Vendor details string
 			Padding	Padding after ARP packet in hex if nonzero
 			Framing	Framing type if not Ethernet_II
 			VLAN	802.1Q VLAD ID if present
 			Proto	ARP protocol if not 0x0800
 			DUP	Packet number for duplicate packets (>1)
 			RTT	Round trip time if --rtt option given
 			
 			Only the "ip" and "mac" fields are available if the
 			--quiet option is specified.
 			
 			Any characters that are not fields are output
 			verbatim. "\" introduces escapes:
 			
 			\n newline
 			\r carriage return
 			\t tab
 			\  suppress special meaning for following character
 			
 			You should enclose the --format argument in 'single
 			quotes' to protect special characters from the shell.
 			
 			Example: --format='${ip}\t${mac}\t${vendor}'
 
 Host List Randomisation:
 
 --random or -R		Randomise the target host list.
 
 --randomseed=<i>	Seed the pseudo random number generator.
 			Useful if you want a reproducible --random order.
 
 Output Timing and Retry:
 
 --retry=<i> or -r <i>	Set total number of attempts per host to <i>,
 			default=2.
 
 --backoff=<f> or -b <f>	Set backoff factor to <f>, default=1.50.
 			Multiplies timeout by <f> for each pass.
 
 --timeout=<i> or -t <i>	Set initial per host timeout to <i> ms, default=500.
 			This timeout is for the first packet sent to each host.
 			subsequent timeouts are multiplied by the backoff
 			factor which is set with --backoff.
 
 --interval=<x> or -i <x> Set minimum packet interval to <x>.
 			This controls the outgoing bandwidth usage by limiting
 			the packet rate. If you want to use up to a given
 			bandwidth it is easier to use the --bandwidth option
 			instead. The interval is in milliseconds, or
 			microseconds if "u" is appended.
 
 --bandwidth=<x> or -B <x> Set outbound bandwidth to <x>, default=256000.
 			The value is in bits per second. Append K for
 			kilobits or M for megabits (decimal multiples). You
 			cannot specify both --interval and --bandwidth.
 
 DNS Resolution:
 
 --numeric or -N		Targets must be IP addresses, not hostnames.
 			Can reduce startup time for large target lists.
 
 --resolve or -d		Resolve responding addresses to hostnames.
 			The default output format will display the hostname
 			instead of the IPv4 address. This option makes the
 			${name} field available for the --format option.
 
 Output ARP Packet:
 
 --arpsha=<m> or -u <m>	Set the ARP source Ethernet address.
 			Sets the 48-bit ar$sha field but does not change the
 			hardware address in the frame header, see --srcaddr
 			for how to change that address. Default is the
 			Ethernet address of the outgoing interface.
 
 --arptha=<m> or -w <m>	Set the ARP target Ethernet address.
 			Sets the 48-bit ar$tha field. The default is zero
 			because this field is not used for ARP request packets.
 
 --arphrd=<i> or -H <i>	Set the ARP hardware type, default=1.
 			Sets the 16-bit ar$hrd field. The default is 1
 			(ARPHRD_ETHER). Many operating systems also respond to
 			6 (ARPHRD_IEEE802)
 
 --arppro=<i> or -p <i>	Set the ARP protocol type, default=0x0800.
 			Sets the 16-bit ar$pro field. Most operating systems
 			only respond to 0x0800 (IPv4).
 
 --arphln=<i> or -a <i>	Set the hardware address length, default=6.
 			Sets the 8-bit ar$hln field. The lengths of the
 			ar$sha and ar$tha fields are not changed by this
 			option; it only changes the ar$hln field.
 
 --arppln=<i> or -P <i>	Set the protocol address length, default=4.
 			Sets the 8-bit ar$pln field. The lengths of the ar$spa
 			and ar$tpa fields are not changed by this option;
 			it only changes the ar$pln field.
 
 --arpop=<i> or -o <i>	Specify the ARP operation, default=1.
 			Sets the 16-bit ar$op field. Most operating systems
 			only respond to the value 1 (ARPOP_REQUEST).
 
 --arpspa=<a> or -s <a>	Set the source IPv4 address.
 			The address should be in dotted quad format, or the
 			string "dest", which sets the source address to
 			the target host address. The default is the outgoing
 			interface address. Sets the 32-bit ar$spa field. Some
 			operating systems only respond if the source address
 			is within the network of the receiving interface.
 			Setting ar$spa to the destination IP address can cause
 			some operating systems to report an address clash.
 
 Output Ethernet Header:
 
 --srcaddr=<m> or -S <m> Set the source Ethernet MAC address.
 			Default is the interface MAC address. This sets the
 			address in the Ethernet header. It does not change the
 			address in the ARP packet: use --arpsha to change
 			that address.
 
 --destaddr=<m> or -T <m> Set the destination MAC address.
 			Sets the destination address in the Ethernet
 			header. Default is ff:ff:ff:ff:ff:ff (broadcast)
 			Hosts also respond if the request is sent to their
 			unicast address, or to a multicast address they
 			are listening on.
 
 --prototype=<i> or -y <i> Sets the Ethernet protocol type, default=0x0806.
 			This sets the protocol type field in the Ethernet
 			header.
 
 --llc or -L		Use RFC 1042 LLC/SNAP encapsulation for 802.2 networks.
 			arp-scan will decode and display ARP responses in both
 			Ethernet-II and IEEE 802.2 formats irrespective of
 			this option.
 
 --vlan=<i> or -Q <i>	Use 802.1Q tagging with VLAN id <i>.
 			The id should be in the range 0 to 4095. arp-scan will
 			decode and display ARP responses in 802.1Q format
 			irrespective of this option.
 
 Misc Options:
 
 --limit=<i> or -M <i>	Exit after the specified number of hosts have responded.
 			arp-scan will exit with status 1 if the number of
 			responding hosts is less than the limit. Can be used
 			in scripts to check if fewer hosts respond without
 			having to parse the output.
 
 --pcapsavefile=<s> or -W <s>	Write received packets to pcap savefile <s>.
 			ARP responses will be written to the specified file
 			as well as being decoded and displayed.
 
 --snap=<i> or -n <i>	Set the pcap snap length to <i>. Default=64.
 			Specifies the frame capture length, including the
 			Ethernet header. The default is normally sufficient.
 
 --retry-send=<i> or -Y <i> Set number of send attempts, default=20.
 
 --retry-send-interval=<i> or -E <i> Set interval between send attempts.
 			Interval is in milliseconds or microseconds if "u"
 			is appended. default=5.
 
 --padding=<h> or -A <h>	Specify padding after packet data.
 			Set padding after the ARP request to hex value <h>.
 
 Report bugs or send suggestions at https://github.com/royhills/arp-scan
 See the arp-scan homepage at https://github.com/royhills/arp-scan
 ```
 
 - - -
 
 ##### get-iab
 
 
 
 - - -
 
 ##### get-oui
 
 Fetch the arp-scan OUI file from the ieee-data package
 
 ```
 root@kali:~# get-oui --help
 /usr/sbin/get-oui version [unknown] calling Getopt::Std::getopts (version 1.13 [paranoid]),
 running under Perl version 5.36.0.
 
 Usage: get-oui [-OPTIONS [-MORE_OPTIONS]] [--] [PROGRAM_ARG1 ...]
 
 The following single-character options are accepted:
 	With arguments: -f -u
 	Boolean (without arguments): -h -v
 
 Options may be merged together.  -- stops processing of options.
 Space is not required between options and their arguments.
   [Now continuing due to backward compatibility and excessive paranoia.
    See 'perldoc Getopt::Std' about $Getopt::Std::STANDARD_HELP_VERSION.]
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## arp-scan Usage Examples

Scan the local network, using the information from the primary network interface:

```
root@kali:~# arp-scan -l
Interface: eth0, datalink type: EN10MB (Ethernet)
Starting arp-scan 1.9 with 256 hosts (http://www.nta-monitor.com/tools/arp-scan/)
172.16.193.1 00:50:56:c0:00:08 VMware, Inc.
172.16.193.2 00:50:56:f1:18:a8 VMware, Inc.
172.16.193.254 00:50:56:e5:7b:87 VMware, Inc.

3 packets received by filter, 0 packets dropped by kernel
Ending arp-scan 1.9: 256 hosts scanned in 2.327 seconds (110.01 hosts/sec). 3 responded
```

Scan a subnet, specifying the interface to use and a custom source MAC address:

```
root@kali:~# arp-scan -I eth0 --srcaddr=DE:AD:BE:EF:CA:FE 192.168.86.0/24
Interface: eth0, datalink type: EN10MB (Ethernet)
Starting arp-scan 1.9 with 256 hosts (http://www.nta-monitor.com/tools/arp-scan/)
192.168.86.1 70:3a:cb:68:51:4c (Unknown)
192.168.86.3 00:08:9b:f6:f6:2f ICP Electronics Inc.
192.168.86.2 84:1b:5e:e5:66:af NETGEAR
192.168.86.4 00:11:32:4b:04:8a Synology Incorporated
192.168.86.7 b8:27:eb:89:ac:c3 Raspberry Pi Foundation
[...]
```
