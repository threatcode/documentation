---
Title: sipvicious
Homepage: https://github.com/EnableSecurity/sipvicious
Repository: https://salsa.debian.org/debian/sipvicious
Architectures: all
Version: 0.3.3-2
Metapackages: kali-linux-everything kali-linux-large kali-tools-passwords kali-tools-voip kali-tools-vulnerability 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### sipvicious
 
  SIPVicious suite is a set of tools that can be used
  to audit SIP based VoIP systems. This suite has five
  tools: svmap, svwar, svcrack, svreport, svcrash.
   
  svmap is a sip scanner. When launched against ranges
  of ip address space, it will identify any SIP servers
  which it finds on the way.
   
  svwar identifies working extension lines on a PBX.
  Also tells you if extension line requires authentication or not.
   
  svcrack is a password cracker making use of digest authentication.
  It is able to crack passwords on both registrar servers and proxy
  servers.
   
  svreport is able to manage sessions created by the rest of the tools
  and export to pdf, xml, csv and plain text.
   
  svcrash responds to svwar and svcrack SIP messages with a message
  that causes old versions to crash.
 
 **Installed size:** `197 KB`  
 **How to install:** `sudo apt install sipvicious`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-pkg-resources
 * python3-scapy
 {{< /spoiler >}}
 
 ##### svcrack
 
 Online password guessing tool for SIP devices
 
 ```
 root@kali:~# svcrack -h
 Usage: svcrack -u username [options] target
 examples:
 svcrack -u100 -d dictionary.txt udp://10.0.0.1:5080
 svcrack -u100 -r1-9999 -z4 10.0.0.1
 
 
 Options:
   --version             show program's version number and exit
   -h, --help            show this help message and exit
   -p PORT, --port=PORT  Destination port of the SIP device - eg -p 5060
   -v, --verbose         Increase verbosity
   -q, --quiet           Quiet mode
   -P PORT, --localport=PORT
                         Source port for our packets
   -x IP, --externalip=IP
                         IP Address to use as the external ip. Specify this if
                         you have multiple interfaces or if you are behind NAT
   -b BINDINGIP, --bindingip=BINDINGIP
                         By default we bind to all interfaces. This option
                         overrides that and binds to the specified ip address
   -t SELECTTIME, --timeout=SELECTTIME
                         This option allows you to trottle the speed at which
                         packets are sent. Change this if you're losing
                         packets. For example try 0.5.
   -R, --reportback      Send the author an exception traceback. Currently
                         sends the command line parameters and the traceback
   -A, --autogetip       Automatically get the current IP address. This is
                         useful when you are not getting any responses back due
                         to SIPVicious not resolving your local IP.
   -s NAME, --save=NAME  save the session. Has the benefit of allowing you to
                         resume a previous scan and allows you to export scans
   --resume=NAME         resume a previous scan
   -c, --enablecompact   enable compact mode. Makes packets smaller but
                         possibly less compatible
   -u USERNAME, --username=USERNAME
                         username to try crack
   -d DICTIONARY, --dictionary=DICTIONARY
                         specify a dictionary file with passwords or - for
                         stdin
   -r RANGE, --range=RANGE
                         specify a range of numbers. example:
                         100-200,300-310,400
   -e EXTENSION, --extension=EXTENSION
                         Extension to crack. Only specify this when the
                         extension is different from the username.
   -z PADDING, --zeropadding=PADDING
                         the number of zeros used to padd the password. the
                         options "-r 1-9999 -z 4"would give 0001 0002 0003 ...
                         9999
   -n, --reusenonce      Reuse nonce. Some SIP devices don't mind you reusing
                         the nonce (making them vulnerable to replay attacks).
                         Speeds up the cracking.
   -T TEMPLATE, --template=TEMPLATE
                         A format string which allows us to specify a template
                         for the extensionsexample svwar.py -e 1-999
                         --template="123%#04i999" would scan between 1230001999
                         to 1230999999"
   --maximumtime=MAXIMUMTIME
                         Maximum time in seconds to keep sending requests
                         without receiving a response back
   -D, --enabledefaults  Scan for default / typical passwords such
                         as1000,2000,3000 ... 1100, etc. This option is off by
                         default.Use --enabledefaults to enable this
                         functionality
   --domain=DOMAIN       force a specific domain name for the SIP message, eg.
                         example.org
   --requesturi=REQUESTURI
                         force the first line URI to a specific value; e.g.
                         sip:999@example.org
   -6                    Scan an IPv6 address
   -m METHOD, --method=METHOD
                         Specify a SIP method to use
 ```
 
 - - -
 
 ##### svcrash
 
 Stop unauthorized scans from svcrack/svwar tool
 
 ```
 root@kali:~# svcrash -h
 Usage: svcrash [options]
 
 Options:
   --version        show program's version number and exit
   -h, --help       show this help message and exit
   --auto           Automatically send responses to attacks
   --astlog=ASTLOG  Path for the asterisk full logfile
   -d IPADDR        specify attacker's ip address
   -p PORT          specify attacker's port
   -b               bruteforce the attacker's port
 ```
 
 - - -
 
 ##### svmap
 
 Scanner that searches for SIP devices on a given network
 
 ```
 root@kali:~# svmap -h
 Usage: svmap [options] host1 host2 hostrange
 Scans for SIP devices on a given network
 
 examples:
 
 svmap 10.0.0.1-10.0.0.255 172.16.131.1 sipvicious.org/22 10.0.1.1/241.1.1.1-20 1.1.2-20.* 4.1.*.*
 
 svmap -s session1 --randomize 10.0.0.1/8
 
 svmap --resume session1 -v
 
 svmap -p5060-5062 10.0.0.3-20 -m INVITE
 
 
 
 Options:
   --version             show program's version number and exit
   -h, --help            show this help message and exit
   -p PORT, --port=PORT  Destination port or port ranges of the SIP device - eg
                         -p5060,5061,8000-8100
   -v, --verbose         Increase verbosity
   -q, --quiet           Quiet mode
   -P PORT, --localport=PORT
                         Source port for our packets
   -x IP, --externalip=IP
                         IP Address to use as the external ip. Specify this if
                         you have multiple interfaces or if you are behind NAT
   -b BINDINGIP, --bindingip=BINDINGIP
                         By default we bind to all interfaces. This option
                         overrides that and binds to the specified ip address
   -t SELECTTIME, --timeout=SELECTTIME
                         This option allows you to trottle the speed at which
                         packets are sent. Change this if you're losing
                         packets. For example try 0.5.
   -R, --reportback      Send the author an exception traceback. Currently
                         sends the command line parameters and the traceback
   -A, --autogetip       Automatically get the current IP address. This is
                         useful when you are not getting any responses back due
                         to SIPVicious not resolving your local IP.
   -s NAME, --save=NAME  save the session. Has the benefit of allowing you to
                         resume a previous scan and allows you to export scans
   --resume=NAME         resume a previous scan
   -c, --enablecompact   enable compact mode. Makes packets smaller but
                         possibly less compatible
   --randomscan          Scan random IP addresses
   -i scan1, --input=scan1
                         Scan IPs which were found in a previous scan. Pass the
                         session name as the argument
   -I scan1, --inputtext=scan1
                         Scan IPs from a text file - use the same syntax as
                         command line but with new lines instead of commas.
                         Pass the file name as the argument
   -m METHOD, --method=METHOD
                         Specify the request method - by default this is
                         OPTIONS.
   -d, --debug           Print SIP messages received
   --first=FIRST         Only send the first given number of messages (i.e.
                         usually used to scan only X IPs)
   -e EXTENSION, --extension=EXTENSION
                         Specify an extension - by default this is not set
   --randomize           Randomize scanning instead of scanning consecutive ip
                         addresses
   --srv                 Scan the SRV records for SIP on the destination domain
                         name.The targets have to be domain names - example.org
                         domain1.com
   --fromname=FROMNAME   specify a name for the from header
   -6, --ipv6            scan an IPv6 address
 ```
 
 - - -
 
 ##### svreport
 
 Report engine manage sessions from previous scans with SIPVicious
 
 ```
 root@kali:~# svreport -h
 Usage: svreport [command] [options]
 
 Supported commands:
 
                 - list:	lists all scans
 
                 - export:	exports the given scan to a given format
 
                 - delete:	deletes the scan
 
                 - stats:	print out some statistics of interest
 
                 - search:	search for a specific string in the user agent (svmap)
 
 examples:
 
       svreport.py list
 
       svreport.py export -f pdf -o scan1.pdf -s scan1
 
       svreport.py delete -s scan1
 
 
 
 Options:
   --version             show program's version number and exit
   -h, --help            show this help message and exit
   -v, --verbose         Increase verbosity
   -q, --quiet           Quiet mode
   -t SESSIONTYPE, --type=SESSIONTYPE
                         Type of session. This is usually either svmap, svwar
                         or svcrack. If not set I will try to find the best
                         match
   -s SESSION, --session=SESSION
                         Name of the session
   -f FORMAT, --format=FORMAT
                         Format type. Can be stdout, pdf, xml, csv or txt
   -o OUTPUTFILE, --output=OUTPUTFILE
                         Output filename
   -n                    Do not resolve the ip address
   -c, --count           Used togather with 'list' command to count the number
                         of entries
 ```
 
 - - -
 
 ##### svwar
 
 Extension line scanner
 
 ```
 root@kali:~# svwar -h
 Usage: svwar [options] target
 examples:
 svwar -e100-999 udp://10.0.0.1:5080
 svwar -d dictionary.txt 10.0.0.2
 
 
 Options:
   --version             show program's version number and exit
   -h, --help            show this help message and exit
   -p PORT, --port=PORT  Destination port of the SIP device - eg -p 5060
   -v, --verbose         Increase verbosity
   -q, --quiet           Quiet mode
   -P PORT, --localport=PORT
                         Source port for our packets
   -x IP, --externalip=IP
                         IP Address to use as the external ip. Specify this if
                         you have multiple interfaces or if you are behind NAT
   -b BINDINGIP, --bindingip=BINDINGIP
                         By default we bind to all interfaces. This option
                         overrides that and binds to the specified ip address
   -t SELECTTIME, --timeout=SELECTTIME
                         This option allows you to trottle the speed at which
                         packets are sent. Change this if you're losing
                         packets. For example try 0.5.
   -R, --reportback      Send the author an exception traceback. Currently
                         sends the command line parameters and the traceback
   -A, --autogetip       Automatically get the current IP address. This is
                         useful when you are not getting any responses back due
                         to SIPVicious not resolving your local IP.
   -s NAME, --save=NAME  save the session. Has the benefit of allowing you to
                         resume a previous scan and allows you to export scans
   --resume=NAME         resume a previous scan
   -c, --enablecompact   enable compact mode. Makes packets smaller but
                         possibly less compatible
   -d DICTIONARY, --dictionary=DICTIONARY
                         specify a dictionary file with possible extension
                         names or - for stdin
   -m OPTIONS, --method=OPTIONS
                         specify a request method. The default is REGISTER.
                         Other possible methods are OPTIONS and INVITE
   -e RANGE, --extensions=RANGE
                         specify an extension or extension range  example: -e
                         100-999,1000-1500,9999
   -z PADDING, --zeropadding=PADDING
                         the number of zeros used to padd the username.the
                         options "-e 1-9999 -z 4" would give 0001 0002 0003 ...
                         9999
   --force               Force scan, ignoring initial sanity checks.
   -T TEMPLATE, --template=TEMPLATE
                         A format string which allows us to specify a template
                         for the extensionsexample svwar.py -e 1-999
                         --template="123%#04i999" would scan between 1230001999
                         to 1230999999"
   -D, --enabledefaults  Scan for default / typical extensions such
                         as1000,2000,3000 ... 1100, etc. This option is off by
                         default.Use --enabledefaults to enable this
                         functionality
   --maximumtime=MAXIMUMTIME
                         Maximum time in seconds to keep sending requests
                         without receiving a response back
   --domain=DOMAIN       force a specific domain name for the SIP message, eg.
                         -d example.org
   --debug               Print SIP messages received
   -6                    scan an IPv6 address
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## svmap Usage Example

Scan the given network range (`192.168.1.0/24`) and display verbose output (`-v`):

```
root@kali:~# svmap 192.168.1.0/24 -v
INFO:DrinkOrSip:trying to get self ip .. might take a while
INFO:root:start your engines
INFO:DrinkOrSip:Looks like we received a SIP request from 192.168.1.202:5060
INFO:DrinkOrSip:Looks like we received a SIP request from 192.168.1.202:5060
INFO:DrinkOrSip:Looks like we received a SIP request from 192.168.1.202:5060
```
