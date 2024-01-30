---
Title: nipper-ng
Homepage: 
Repository: https://gitlab.com/kalilinux/packages/nipper-ng
Architectures: any
Version: 0.11.10-1kali2
Metapackages: kali-linux-everything kali-linux-large kali-tools-identify 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### nipper-ng
 
  Nipper-ng is the next generation of nippper, and will always remain free and
  open source. This software will be used to make observations about the security
  configurations of many different device types such as routers, firewalls,
  and switches of a network infrastructure.
   
  This is a fork from nipper 0.11.10 release of the GNUv3 GPL code.
 
 **Installed size:** `761 KB`  
 **How to install:** `sudo apt install nipper-ng`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### nipper
 
 Network Infrastructure Parser. Produces reports based of network device configuration file settings.
 
 ```
 root@kali:~# nipper --help
                      _                           ____
                _ __ (_)_ __  _ __   ___ _ __    / ->/|
               | '_ \| | '_ \| '_ \ / _ \ '__|  /<-_/ |
               | | | | | |_) | |_) |  __/ |     |   | /
               |_| |_|_| .__/| .__/ \___|_|     |___|/
                       |_|   |_|
 
                            Version 0.11.10
                      http://nipper.titania.co.uk
              Copyright (C) 2006-2008 Ian Ventura-Whiting
 
 Nipper is a  Network Infrastructure  Configuration Parser.  Nipper takes
 a network infrastructure  device configuration,  processes the  file and
 details security-related  issues with detailed  recommendations.  Nipper
 was previous known as CiscoParse.
 
 By default, input is retrieved from stdin and is output (in HTML format)
 to stdout.
 
 Command:
     nipper [Options]
 
 General Options:
     --input=<file>
     Specifies a  device configuration  file to  process.  For CheckPoint
     Firewall-1 configurations, the input should be the conf directory.
 
     --output=<file> | --report=<file>
     Specified an output file for the report.
 
     --csv=<file>
     Want to output the network filtering configuration to a CSV file?.
 
     --version
     Displays the program version.
 
 Example:
     The  example   below  will   process  a   Cisco   IOS-based   router
     configuration file called ios.conf  and output  the report to a file
     called report.html.
 
     nipper --ios-router --input=ios.conf --output=report.html
 
 For additional help:
     --help[=<topic>]
     Show  the  online help  or show  the  additional  help on  the topic
     specified.  The help  topics  are;  GENERAL,  DEVICES,  DEVICES-ADV,
     SNMP,  REPORT, REPORT-ADV,  REPORT-SECT, REPORT-HTML,  REPORT-LATEX,
     AUDIT-ACL, AUDIT-PASS, AUDIT-ADV or CONFIG-FILE.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
