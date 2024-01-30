---
Title: netcat
Homepage: http://www.stearns.org/nc/
Repository: https://salsa.debian.org/debian/netcat
Architectures: any
Version: 1.10-47
Metapackages: kali-linux-core kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-linux-nethunter kali-linux-wsl kali-tools-information-gathering kali-tools-vulnerability 
Icon: images/netcat-logo.svg
PackagesInfo: |
 ### netcat-traditional
 
  A simple Unix utility which reads and writes data across network
  connections using TCP or UDP protocol. It is designed to be a reliable
  "back-end" tool that can be used directly or easily driven by other
  programs and scripts. At the same time it is a feature-rich network
  debugging and exploration tool, since it can create almost any kind
  of connection you would need and has several interesting built-in
  capabilities.
   
  This is the "classic" netcat, written by *Hobbit*. It lacks many
  features found in netcat-openbsd.
 
 **Installed size:** `143 KB`  
 **How to install:** `sudo apt install netcat-traditional`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### nc.traditional
 
 TCP/IP swiss army knife
 
 ```
 root@kali:~# nc.traditional -h
 [v1.10-47]
 connect to somewhere:	nc [-options] hostname port[s] [ports] ... 
 listen for inbound:	nc -l -p port [-options] [hostname] [port]
 options:
 	-c shell commands	as `-e'; use /bin/sh to exec [dangerous!!]
 	-e filename		program to exec after connect [dangerous!!]
 	-b			allow broadcasts
 	-g gateway		source-routing hop point[s], up to 8
 	-G num			source-routing pointer: 4, 8, 12, ...
 	-h			this cruft
 	-i secs			delay interval for lines sent, ports scanned
         -k                      set keepalive option on socket
 	-l			listen mode, for inbound connects
 	-n			numeric-only IP addresses, no DNS
 	-o file			hex dump of traffic
 	-p port			local port number
 	-r			randomize local and remote ports
 	-q secs			quit after EOF on stdin and delay of secs
 	-s addr			local source address
 	-T tos			set Type Of Service
 	-t			answer TELNET negotiation
 	-u			UDP mode
 	-v			verbose [use twice to be more verbose]
 	-w secs			timeout for connects and final net reads
 	-C			Send CRLF as line-ending
 	-z			zero-I/O mode [used for scanning]
 port numbers can be individual or ranges: lo-hi [inclusive];
 hyphens in port names must be backslash escaped (e.g. 'ftp\-data').
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
