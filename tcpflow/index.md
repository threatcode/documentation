---
Title: tcpflow
Homepage: https://github.com/simsong/tcpflow
Repository: https://salsa.debian.org/debian/tcpflow
Architectures: any
Version: 1.6.1-3
Metapackages: kali-linux-everything kali-linux-large kali-tools-forensics kali-tools-respond kali-tools-sniffing-spoofing 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### tcpflow
 
  tcpflow is a program that captures data transmitted as part of TCP
  connections (flows), and stores the data in a way that is convenient
  for protocol analysis or debugging. A program like 'tcpdump' shows a
  summary of packets seen on the wire, but usually doesn't store the
  data that's actually being transmitted. In contrast, tcpflow
  reconstructs the actual data streams and stores each flow in a
  separate file for later analysis.
   
  tcpflow understands sequence numbers and will correctly reconstruct
  data streams regardless of retransmissions or out-of-order delivery.
  However, it currently does not understand IP fragments; flows
  containing IP fragments will not be recorded properly.
   
  tcpflow is based on the LBL Packet Capture Library and therefore
  supports the same rich filtering expressions that programs like
  'tcpdump' support. tcpflow can also rebuild flows from data captured
  with 'tcpdump -w'.
 
 **Installed size:** `810 KB`  
 **How to install:** `sudo apt install tcpflow`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libcairo2 
 * libgcc-s1 
 * libhttp-parser2.9 
 * libpcap0.8 
 * libssl3 
 * libstdc++6 
 * zlib1g 
 {{< /spoiler >}}
 
 ##### tcpflow
 
 TCP flow recorder
 
 ```
 root@kali:~# tcpflow -h
 TCPFLOW version 1.6.1
 
 usage: tcpflow [-aBcCDhIpsvVZ] [-b max_bytes] [-d debug_level] 
      [-[eE] scanner] [-f max_fds] [-F[ctTXMkmg]] [-h|--help] [-i iface]
      [-l files...] [-L semlock] [-m min_bytes] [-o outdir] [-r file] [-R file]
      [-S name=value] [-T template] [-U|--relinquish-privileges user] [-v|--verbose]
      [-w file] [-x scanner] [-X xmlfile] [-z|--chroot dir] [expression]
 
    -a: do ALL post-processing.
    -b max_bytes: max number of bytes per flow to save
    -d debug_level: debug level; default is 1
    -f: maximum number of file descriptors to use
    -h: print this help message (-hh for more help)
    -H: print detailed information about each scanner
    -i: network interface on which to listen
    -I: write for each flow another file *.findx to provide byte-indexed timestamps
    -g: output each flow in alternating colors (note change!)
    -l: treat non-flag arguments as input files rather than a pcap expression
    -L  semlock - specifies that writes are locked using a named semaphore
    -p: don't use promiscuous mode
    -q: quiet mode - do not print warnings
    -r file      : read packets from tcpdump pcap file (may be repeated)
    -R file      : read packets from tcpdump pcap file TO FINISH CONNECTIONS
    -v           : verbose operation equivalent to -d 10
    -V           : print version number and exit
    -w  file     : write packets not processed to file
    -o  outdir   : specify output directory (default '.')
    -X  filename : DFXML output to filename
    -m  bytes    : specifies skip that starts a new stream (default 16777216).
    -F{p} : filename prefix/suffix (-hh for options)
    -T{t} : filename template (-hh for options; default %A.%a-%B.%b%V%v%C%c)
    -Z       do not decompress gzip-compressed HTTP transactions
    -K: output|keep pcap flow structure.
 
 Security:
    -U user  relinquish privleges and become user (if running as root)
    -z dir   chroot to dir (requires that -U be used).
 
 Control of Scanners:
    -E scanner   - turn off all scanners except scanner
    -S name=value  Set a configuration parameter (-hh for info)
 
 Console output options:
    -B: binary output, even with -c or -C (normally -c or -C turn it off)
    -c: console print only (don't create files)
    -C: console print only, but without the display of source/dest header
    -0: don't print newlines after packets when printing to console
    -s: strip non-printable characters (change to '.')
    -J: output json format.
    -D: output in hex (useful to combine with -c or -C)
 
 expression: tcpdump-like filtering expression
 
 See the man page for additional information.
 
 ```
 
 - - -
 
 ##### tcpflow
 
 TCP flow recorder
 
 ```
 root@kali:~# tcpflow -h
 TCPFLOW version 1.6.1
 
 usage: tcpflow [-aBcCDhIpsvVZ] [-b max_bytes] [-d debug_level] 
      [-[eE] scanner] [-f max_fds] [-F[ctTXMkmg]] [-h|--help] [-i iface]
      [-l files...] [-L semlock] [-m min_bytes] [-o outdir] [-r file] [-R file]
      [-S name=value] [-T template] [-U|--relinquish-privileges user] [-v|--verbose]
      [-w file] [-x scanner] [-X xmlfile] [-z|--chroot dir] [expression]
 
    -a: do ALL post-processing.
    -b max_bytes: max number of bytes per flow to save
    -d debug_level: debug level; default is 1
    -f: maximum number of file descriptors to use
    -h: print this help message (-hh for more help)
    -H: print detailed information about each scanner
    -i: network interface on which to listen
    -I: write for each flow another file *.findx to provide byte-indexed timestamps
    -g: output each flow in alternating colors (note change!)
    -l: treat non-flag arguments as input files rather than a pcap expression
    -L  semlock - specifies that writes are locked using a named semaphore
    -p: don't use promiscuous mode
    -q: quiet mode - do not print warnings
    -r file      : read packets from tcpdump pcap file (may be repeated)
    -R file      : read packets from tcpdump pcap file TO FINISH CONNECTIONS
    -v           : verbose operation equivalent to -d 10
    -V           : print version number and exit
    -w  file     : write packets not processed to file
    -o  outdir   : specify output directory (default '.')
    -X  filename : DFXML output to filename
    -m  bytes    : specifies skip that starts a new stream (default 16777216).
    -F{p} : filename prefix/suffix (-hh for options)
    -T{t} : filename template (-hh for options; default %A.%a-%B.%b%V%v%C%c)
    -Z       do not decompress gzip-compressed HTTP transactions
    -K: output|keep pcap flow structure.
 
 Security:
    -U user  relinquish privleges and become user (if running as root)
    -z dir   chroot to dir (requires that -U be used).
 
 Control of Scanners:
    -E scanner   - turn off all scanners except scanner
    -S name=value  Set a configuration parameter (-hh for info)
 
 Console output options:
    -B: binary output, even with -c or -C (normally -c or -C turn it off)
    -c: console print only (don't create files)
    -C: console print only, but without the display of source/dest header
    -0: don't print newlines after packets when printing to console
    -s: strip non-printable characters (change to '.')
    -J: output json format.
    -D: output in hex (useful to combine with -c or -C)
 
 expression: tcpdump-like filtering expression
 
 See the man page for additional information.
 
 ```
 
 - - -
 
 ### tcpflow-nox
 
  tcpflow is a program that captures data transmitted as part of TCP
  connections (flows), and stores the data in a way that is convenient
  for protocol analysis or debugging. A program like 'tcpdump' shows a
  summary of packets seen on the wire, but usually doesn't store the
  data that's actually being transmitted. In contrast, tcpflow
  reconstructs the actual data streams and stores each flow in a
  separate file for later analysis.
   
  tcpflow understands sequence numbers and will correctly reconstruct
  data streams regardless of retransmissions or out-of-order delivery.
  However, it currently does not understand IP fragments; flows
  containing IP fragments will not be recorded properly.
   
  tcpflow is based on the LBL Packet Capture Library and therefore
  supports the same rich filtering expressions that programs like
  'tcpdump' support. tcpflow can also rebuild flows from data captured
  with 'tcpdump -w'.
   
  This package has no dependency on libcairo or any x11 libraries, and cannot
  generate graphical reports.
 
 **Installed size:** `645 KB`  
 **How to install:** `sudo apt install tcpflow-nox`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libgcc-s1 
 * libhttp-parser2.9 
 * libpcap0.8 
 * libssl3 
 * libstdc++6 
 * zlib1g 
 {{< /spoiler >}}
 
 ##### tcpflow
 
 TCP flow recorder
 
 ```
 root@kali:~# tcpflow -h
 TCPFLOW version 1.6.1
 
 usage: tcpflow [-aBcCDhIpsvVZ] [-b max_bytes] [-d debug_level] 
      [-[eE] scanner] [-f max_fds] [-F[ctTXMkmg]] [-h|--help] [-i iface]
      [-l files...] [-L semlock] [-m min_bytes] [-o outdir] [-r file] [-R file]
      [-S name=value] [-T template] [-U|--relinquish-privileges user] [-v|--verbose]
      [-w file] [-x scanner] [-X xmlfile] [-z|--chroot dir] [expression]
 
    -a: do ALL post-processing.
    -b max_bytes: max number of bytes per flow to save
    -d debug_level: debug level; default is 1
    -f: maximum number of file descriptors to use
    -h: print this help message (-hh for more help)
    -H: print detailed information about each scanner
    -i: network interface on which to listen
    -I: write for each flow another file *.findx to provide byte-indexed timestamps
    -g: output each flow in alternating colors (note change!)
    -l: treat non-flag arguments as input files rather than a pcap expression
    -L  semlock - specifies that writes are locked using a named semaphore
    -p: don't use promiscuous mode
    -q: quiet mode - do not print warnings
    -r file      : read packets from tcpdump pcap file (may be repeated)
    -R file      : read packets from tcpdump pcap file TO FINISH CONNECTIONS
    -v           : verbose operation equivalent to -d 10
    -V           : print version number and exit
    -w  file     : write packets not processed to file
    -o  outdir   : specify output directory (default '.')
    -X  filename : DFXML output to filename
    -m  bytes    : specifies skip that starts a new stream (default 16777216).
    -F{p} : filename prefix/suffix (-hh for options)
    -T{t} : filename template (-hh for options; default %A.%a-%B.%b%V%v%C%c)
    -Z       do not decompress gzip-compressed HTTP transactions
    -K: output|keep pcap flow structure.
 
 Security:
    -U user  relinquish privleges and become user (if running as root)
    -z dir   chroot to dir (requires that -U be used).
 
 Control of Scanners:
    -E scanner   - turn off all scanners except scanner
    -S name=value  Set a configuration parameter (-hh for info)
 
 Console output options:
    -B: binary output, even with -c or -C (normally -c or -C turn it off)
    -c: console print only (don't create files)
    -C: console print only, but without the display of source/dest header
    -0: don't print newlines after packets when printing to console
    -s: strip non-printable characters (change to '.')
    -J: output json format.
    -D: output in hex (useful to combine with -c or -C)
 
 expression: tcpdump-like filtering expression
 
 See the man page for additional information.
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
