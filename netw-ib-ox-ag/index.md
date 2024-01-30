---
Title: netw-ib-ox-ag
Homepage: http://ntwox.sourceforge.net/
Repository: 
Architectures: any all
Version: 5.39.0-1.5
Metapackages: kali-linux-everything kali-linux-large 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### netwag
 
  Netwag is a graphical front end for netwox which contains more than 200 tools.
  Netwag permits one to easily:
   
   - search amongst tools proposed in netwox
   - construct command line
   - run tools
   - keep an history of commands
 
 **Installed size:** `326 KB`  
 **How to install:** `sudo apt install netwag`  
 
 {{< spoiler "Dependencies:" >}}
 * netwox 
 * tk
 * xterm | x-terminal-emulator
 {{< /spoiler >}}
 
 ##### netwag
 
 Graphical front end for netwox
 
 ```
 root@kali:~# netwag -h
 application-specific initialization failed: Command-specific options:
  -sync:     Use synchronous mode for display server
  -colormap: Colormap for main window
  -display:  Display to use
  -geometry: Initial geometry for window
  -name:     Name to use for application
  -visual:   Visual for main window
  -use:      Id of window in which to embed application
  --:        Marks the end of the options
  -help:     Print summary of command-line options and abort
 Error in startup script: can't read "tk_version": no such variable
     while executing
 "netwag_glo_check_version "Tk" $tk_version 8"
     (file "/usr/bin/netwag" line 236)
 ```
 
 - - -
 
 ### netwag-doc
 
  Netwag is a graphical front end for netwox which contains more than 200 tools.
  Netwag permits one to easily:
   
   - search amongst tools proposed in netwox
   - construct command line
   - run tools
   - keep an history of commands
   
  This package contains documentation for netwag.
 
 **Installed size:** `65 KB`  
 **How to install:** `sudo apt install netwag-doc`  
 
 
 - - -
 
 ### netwox
 
  Toolbox netwox helps to find and solve network problems.
   
  It provides more than 200 tools :
   - sniff, spoof
   - clients, servers
   - DNS, FTP, HTTP, IRC, NNTP, SMTP, SNMP, SYSLOG, TELNET, TFTP
   - scan, ping traceroute
   - etc.
   
  Those tools can be used to quickly spot a problem in a complex network.
  They are oriented towards network administrators and security auditors.
 
 **Installed size:** `1.97 MB`  
 **How to install:** `sudo apt install netwox`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libnet1 
 * libpcap0.8 
 {{< /spoiler >}}
 
 ##### netwox
 
 Examples/tools of the network library netwib
 
 ```
 root@kali:~# man netwox
 NETWOX(1)                   General Commands Manual                  NETWOX(1)
 
 NAME
        netwox - examples/tools of the network library netwib
 
 VERSION
        The version installed on this system is 5.39.0.
 
 IMPORTANT
        Manpage  do  not  contain  a  lot  of  information.  Rather  read  net-
        wox-5.39.0-doc_html.tgz.
 
 SYNOPSIS
        netwox number [ parameters... ]
        netwox number --help
        netwox number --help2
        netwox
 
 PRESENTATION
        Toolbox netwox helps to find and solve network problems.
 
        It provides 223 tools :
         - udp/tcp clients/servers
         - spoofing
         - sniffing
         - address conversion
         - etc.
 
        Netwox is mainly oriented towards network administrators  and  security
        auditors.
 
        Some  tools are only a simplified implementation, while others are very
        sophisticated.
 
        Netwox is available under the GNU GPL license.
 
 DESCRIPTION
        number number of the tool to use
 
        parameters
               parameters for the chosen tool number.  Parameter  --help  shows
               help.  Parameter --help2 shows description.
 
        When  using netwox without number and parameters, it enters interactive
        help mode. In this mode, the user has to select a category by  pressing
        a  key. Then by choosing a tool number, its corresponding usage is dis-
        played. Note: netwag is easier than interactive help mode.
 
 EXAMPLES
        netwox 23 --help
               display simple help for tool number 23
 
        netwox 23 --help2
               display full description of tool 23. It  also  display  its  de-
               scription.
 
        netwox 23
               run tool 23
 
        netwox 23 --extended
               run tool 23 with --extended parameter
 
        netwox 23 -e
               run tool 23 with -e parameter (synonym for --extended)
 
        All  the  tools  are  not  described  in  this  manpage.   Reading net-
        wox-5.39.0-doc_html.tgz is recommended.
 
 SEE ALSO
        netwib(3) netwag(1)
 
                                   08/07/2012                         NETWOX(1)
 ```
 
 - - -
 
 ### netwox-doc
 
  Toolbox netwox helps to find and solve network problems.
   
  It provides more than 200 tools :
   - sniff, spoof
   - clients, servers
   - DNS, FTP, HTTP, IRC, NNTP, SMTP, SNMP, SYSLOG, TELNET, TFTP
   - scan, ping traceroute
   - etc.
   
  Those tools can be used to quickly spot a problem in a complex network.
  They are oriented towards network administrators and security auditors.
   
  This package contains documentation for netwox.
 
 **Installed size:** `802 KB`  
 **How to install:** `sudo apt install netwox-doc`  
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
