---
Title: ftester
Homepage: https://dev.inversepath.com/ftester/
Repository: https://gitlab.com/kalilinux/packages/ftester
Architectures: all
Version: 1.0-1kali3
Metapackages: kali-linux-everything kali-linux-large kali-tools-information-gathering kali-tools-web 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### ftester
 
  The Firewall Tester (FTester) is a tool designed for testing firewall
  filtering policies and Intrusion Detection System (IDS) capabilities.
   
  Features:
   * firewall testing
   * IDS testing
   * simulation of real tcp connections for stateful inspection firewalls and IDS
   * TCP connection spoofing
   * IP fragmentation / TCP segmentation
   * IDS evasion techniques
 
 **Installed size:** `91 KB`  
 **How to install:** `sudo apt install ftester`  
 
 {{< spoiler "Dependencies:" >}}
 * libnet-pcap-perl
 * libnet-rawip-perl
 * libnetpacket-perl
 * perl
 {{< /spoiler >}}
 
 ##### freport
 
 
 ```
 root@kali:~# freport -h
 Usage /usr/bin/freport ftest.log ftestd.log at /usr/bin/freport line 15.
 ```
 
 - - -
 
 ##### ftest
 
 
 ```
 root@kali:~# ftest --help
 /usr/bin/ftest version [unknown] calling Getopt::Std::getopts (version 1.13 [paranoid]),
 running under Perl version 5.36.0.
 
 Usage: ftest [-OPTIONS [-MORE_OPTIONS]] [--] [PROGRAM_ARG1 ...]
 
 The following single-character options are accepted:
 	With arguments: -c -d -e -f -g -k -m -p -s -t
 	Boolean (without arguments): -F -r -v
 
 Options may be merged together.  -- stops processing of options.
 Space is not required between options and their arguments.
   [Now continuing due to backward compatibility and excessive paranoia.
    See 'perldoc Getopt::Std' about $Getopt::Std::STANDARD_HELP_VERSION.]
 FTester client v1.0
 Copyright (C) 2001-2006 Andrea Barisani <andrea@inversepath.com>
 
 Configuration options:
   -f <conf_file>
   -c <source_ip>:<source_port>:<dest_ip>:<dest_port>:<flags>:<protocol>:<tos>
   -v <verbose>
 
 Timing options:
   -d <delay, 0.25 = 250 ms>
   -s <sleep time, 1 = 1 s>
 
 Evasion options:
   -e <evasion method>
   -t <ids_ttl>
 
 Connection options:
   -r <reset connection>
   -F <end connection>
   -g <IP fragments number, es. 4|IP fragments size, es. 16b>
   -p <TCP segments number, es. 4|TCP segments size, es 6b>
   -k <cksum value, es. 60000>
   -m <marker>
 
 ```
 
 - - -
 
 ##### ftestd
 
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
