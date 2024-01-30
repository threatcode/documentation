---
Title: amap
Homepage: https://www.thc.org
Repository: https://gitlab.com/kalilinux/packages/amap
Architectures: any
Version: 5.4-4kali3
Metapackages: kali-linux-everything kali-linux-large 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### amap
 
  AMAP stands for Application MAPper. It is a next-generation scanning
  tool for pentesters. It attempts to identify applications even if they
  are running on a different port than normal.
   
  It also identifies non-ascii based applications. This is achieved by
  sending trigger packets, and looking up the responses in a list of
  response strings.
 
 **Installed size:** `177 KB`  
 **How to install:** `sudo apt install amap`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### amap
 
 A powerful application mapper
 
 ```
 root@kali:~# amap -h
 amap v5.4 (c) 2011 by van Hauser <vh@thc.org> www.thc.org/thc-amap
 Syntax: amap [-A|-B|-P|-W] [-1buSRHUdqv] [[-m] -o <file>] [-D <file>] [-t/-T sec] [-c cons] [-C retries] [-p proto] [-i <file>] [target port [port] ...]
 Modes:
   -A         Map applications: send triggers and analyse responses (default)
   -B         Just grab banners, do not send triggers
   -P         No banner or application stuff - be a (full connect) port scanner
 Options:
   -1         Only send triggers to a port until 1st identification. Speeeeed!
   -6         Use IPv6 instead of IPv4
   -b         Print ascii banner of responses
   -i FILE    Nmap machine readable outputfile to read ports from
   -u         Ports specified on commandline are UDP (default is TCP)
   -R         Do NOT identify RPC service
   -H         Do NOT send application triggers marked as potentially harmful
   -U         Do NOT dump unrecognised responses (better for scripting)
   -d         Dump all responses
   -v         Verbose mode, use twice (or more!) for debug (not recommended :-)
   -q         Do not report closed ports, and do not print them as unidentified
   -o FILE [-m] Write output to file FILE, -m creates machine readable output
   -c CONS    Amount of parallel connections to make (default 32, max 256)
   -C RETRIES Number of reconnects on connect timeouts (see -T) (default 3)
   -T SEC     Connect timeout on connection attempts in seconds (default 5)
   -t SEC     Response wait timeout in seconds (default 5)
   -p PROTO   Only send triggers for this protocol (e.g. ftp)
   TARGET PORT   The target address and port(s) to scan (additional to -i)
 amap is a tool to identify application protocols on target ports.
 Note: this version was NOT compiled with SSL support!
 Usage hint: Options "-bqv" are recommended, add "-1" for fast/rush checks.
 ```
 
 - - -
 
 ##### amap
 
 A powerful application mapper
 
 ```
 root@kali:~# amap -h
 amap v5.4 (c) 2011 by van Hauser <vh@thc.org> www.thc.org/thc-amap
 Syntax: amap [-A|-B|-P|-W] [-1buSRHUdqv] [[-m] -o <file>] [-D <file>] [-t/-T sec] [-c cons] [-C retries] [-p proto] [-i <file>] [target port [port] ...]
 Modes:
   -A         Map applications: send triggers and analyse responses (default)
   -B         Just grab banners, do not send triggers
   -P         No banner or application stuff - be a (full connect) port scanner
 Options:
   -1         Only send triggers to a port until 1st identification. Speeeeed!
   -6         Use IPv6 instead of IPv4
   -b         Print ascii banner of responses
   -i FILE    Nmap machine readable outputfile to read ports from
   -u         Ports specified on commandline are UDP (default is TCP)
   -R         Do NOT identify RPC service
   -H         Do NOT send application triggers marked as potentially harmful
   -U         Do NOT dump unrecognised responses (better for scripting)
   -d         Dump all responses
   -v         Verbose mode, use twice (or more!) for debug (not recommended :-)
   -q         Do not report closed ports, and do not print them as unidentified
   -o FILE [-m] Write output to file FILE, -m creates machine readable output
   -c CONS    Amount of parallel connections to make (default 32, max 256)
   -C RETRIES Number of reconnects on connect timeouts (see -T) (default 3)
   -T SEC     Connect timeout on connection attempts in seconds (default 5)
   -t SEC     Response wait timeout in seconds (default 5)
   -p PROTO   Only send triggers for this protocol (e.g. ftp)
   TARGET PORT   The target address and port(s) to scan (additional to -i)
 amap is a tool to identify application protocols on target ports.
 Note: this version was NOT compiled with SSL support!
 Usage hint: Options "-bqv" are recommended, add "-1" for fast/rush checks.
 ```
 
 - - -
 
 ##### amap6
 
 
 ```
 root@kali:~# amap6 -h
 amap v5.4 (c) 2011 by van Hauser <vh@thc.org> www.thc.org/thc-amap
 Syntax: amap6 [-A|-B|-P|-W] [-1buSRHUdqv] [[-m] -o <file>] [-D <file>] [-t/-T sec] [-c cons] [-C retries] [-p proto] [-i <file>] [target port [port] ...]
 Modes:
   -A         Map applications: send triggers and analyse responses (default)
   -B         Just grab banners, do not send triggers
   -P         No banner or application stuff - be a (full connect) port scanner
 Options:
   -1         Only send triggers to a port until 1st identification. Speeeeed!
   -4         Use IPv4 instead of IPv6
   -b         Print ascii banner of responses
   -i FILE    Nmap machine readable outputfile to read ports from
   -u         Ports specified on commandline are UDP (default is TCP)
   -R         Do NOT identify RPC service
   -H         Do NOT send application triggers marked as potentially harmful
   -U         Do NOT dump unrecognised responses (better for scripting)
   -d         Dump all responses
   -v         Verbose mode, use twice (or more!) for debug (not recommended :-)
   -q         Do not report closed ports, and do not print them as unidentified
   -o FILE [-m] Write output to file FILE, -m creates machine readable output
   -c CONS    Amount of parallel connections to make (default 32, max 256)
   -C RETRIES Number of reconnects on connect timeouts (see -T) (default 3)
   -T SEC     Connect timeout on connection attempts in seconds (default 5)
   -t SEC     Response wait timeout in seconds (default 5)
   -p PROTO   Only send triggers for this protocol (e.g. ftp)
   TARGET PORT   The target address and port(s) to scan (additional to -i)
 amap is a tool to identify application protocols on target ports.
 Note: this version was NOT compiled with SSL support!
 Usage hint: Options "-bqv" are recommended, add "-1" for fast/rush checks.
 ```
 
 - - -
 
 ##### amapcrap
 
 
 ```
 root@kali:~# amapcrap -h
 amapcrap v5.4 (c) 2011 by van Hauser/THC <vh@thc.org>
 
 Syntax: amapcrap [-S] [-u] [-m 0ab] [-M min,max] [-n connects] [-N delay] [-w delay] [-e] [-v] TARGET PORT
 
 Options:
     -S           use SSL after TCP connect (not usuable with -u)
     -u           use UDP protocol (default: TCP) (not usable with -c)
     -n connects  maximum number of connects (default: unlimited)
     -N delay     delay between connects in ms (default: 0)
     -w delay     delay before closing the port (default: 250)
     -e           do NOT stop when a response was made by the server
     -v           verbose mode
     -m 0ab       send as random crap:0-nullbytes, a-letters+spaces, b-binary
     -M min,max   minimum and maximum length of random crap
     TARGET PORT  target (ip or dns) and port to send random crap
 
 This tool sends random data to a silent port to illicit a response, which can
 then be used within amap for future detection. It outputs proper amap
 appdefs definitions. Note: by default all modes are activated (0:10%, a:40%,
 b:50%). Mode 'a' always sends one line with letters and spaces which end with
 \r\n. Visit our homepage at http://www.thc.org
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## amap Usage Example

Scan port `80` on `192.168.1.15`. Display the received banners (`b`), do not display closed ports (`q`), and use verbose output (`v`):

```
root@kali:~# amap -bqv 192.168.1.15 80
Using trigger file /etc/amap/appdefs.trig ... loaded 30 triggers
Using response file /etc/amap/appdefs.resp ... loaded 346 responses
Using trigger file /etc/amap/appdefs.rpc ... loaded 450 triggers

amap v5.4 (www.thc.org/thc-amap) started at 2014-05-13 19:07:16 - APPLICATION MAPPING mode

Total amount of tasks to perform in plain connect mode: 23
Protocol on 192.168.1.15:80/tcp (by trigger ssl) matches http - banner: \n\n501 Method Not Implemented\n\n
<h1>Method Not Implemented</h1>
\n

to /index.html not supported.
\n

\n

<hr />

\n

<address>Apache/2.2.22 (Debian) Server at 12
Protocol on 192.168.1.15:80/tcp (by trigger ssl) matches http-apache-2 - banner: \n\n501 Method Not Implemented\n\n</address>
<h1>Method Not Implemented</h1>
\n

to /index.html not supported.
\n

\n

<hr />

\n

<address>Apache/2.2.22 (Debian) Server at 12
Waiting for timeout on 19 connections ...</address>amap v5.4 finished at 2014-05-13 19:07:22
```
