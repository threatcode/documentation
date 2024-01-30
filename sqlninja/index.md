---
Title: sqlninja
Homepage: https://sqlninja.sourceforge.net/
Repository: https://gitlab.com/kalilinux/packages/sqlninja
Architectures: all
Version: 0.2.6-r1-1kali3
Metapackages: kali-linux-everything kali-linux-large kali-tools-database kali-tools-web 
Icon: images/sqlninja-logo.svg
PackagesInfo: |
 ### sqlninja
 
  Fancy going from a SQL Injection on Microsoft SQL Server to
  a full GUI access on the DB? Take a few new SQL Injection
  tricks, add a couple of remote shots in the registry to
  disable Data Execution Prevention, mix with a little Perl
  that automatically generates a debug script, put all this
  in a shaker with a Metasploit wrapper, shake well and you
  have just one of the attack modules of sqlninja!
 
 **Installed size:** `1.00 MB`  
 **How to install:** `sudo apt install sqlninja`  
 
 {{< spoiler "Dependencies:" >}}
 * libio-socket-ip-perl
 * libnet-dns-perl
 * libnet-pcap-perl
 * libnet-rawip-perl
 * libnetpacket-perl
 * perl
 {{< /spoiler >}}
 
 ##### sqlninja
 
 
 ```
 root@kali:~# sqlninja --help
 /usr/bin/sqlninja version [unknown] calling Getopt::Std::getopts (version 1.13 [paranoid]),
 running under Perl version 5.36.0.
 
 Usage: sqlninja [-OPTIONS [-MORE_OPTIONS]] [--] [PROGRAM_ARG1 ...]
 
 The following single-character options are accepted:
 	With arguments: -m -f -p -w -u -d
 	Boolean (without arguments): -g -v
 
 Options may be merged together.  -- stops processing of options.
 Space is not required between options and their arguments.
   [Now continuing due to backward compatibility and excessive paranoia.
    See 'perldoc Getopt::Std' about $Getopt::Std::STANDARD_HELP_VERSION.]
 Usage: /usr/bin/sqlninja
 	-m <mode> : Required. Available modes are:
 	    t/test - test whether the injection is working
 	    f/fingerprint - fingerprint user, xp_cmdshell and more
 	    b/bruteforce - bruteforce sa account
 	    e/escalation - add user to sysadmin server role
 	    x/resurrectxp - try to recreate xp_cmdshell
 	    u/upload - upload a .scr file
 	    s/dirshell - start a direct shell
 	    k/backscan - look for an open outbound port
 	    r/revshell - start a reverse shell
 	    d/dnstunnel - attempt a dns tunneled shell
 	    i/icmpshell - start a reverse ICMP shell
 	    c/sqlcmd - issue a 'blind' OS command
 	    m/metasploit - wrapper to Metasploit stagers
 	-f <file> : configuration file (default: sqlninja.conf)
 	-p <password> : sa password
 	-w <wordlist> : wordlist to use in bruteforce mode (dictionary method
 	                only)
 	-g : generate debug script and exit (only valid in upload mode)
 	-v : verbose output
 	-d <mode> : activate debug
 	    1 - print each injected command
 	    2 - print each raw HTTP request
 	    3 - print each raw HTTP response
 	    all - all of the above
 	...see sqlninja-howto.html for details
 	 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## sqlninja Usage Example

Connect to the target in test mode (`-m t`) with the specified config file (`-f /root/sqlninja.conf`):

```
root@kali:~# sqlninja -m t -f /root/sqlninja.conf
Sqlninja rel. 0.2.6-r1
Copyright (C) 2006-2011 icesurfer <r00t@northernfortress.net>
[+] Parsing /root/sqlninja.conf...
[+] Target is: 192.168.1.51:80
[+] Trying to inject a 'waitfor delay'....
```
