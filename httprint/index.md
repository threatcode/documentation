---
Title: httprint
Homepage: https://www.net-square.com/httprint.html
Repository: https://gitlab.com/kalilinux/packages/httprint
Architectures: i386 amd64
Version: 0.301-0kali4
Metapackages: kali-linux-everything kali-tools-web 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### httprint
 
  httprint is a web server fingerprinting tool. It relies on web server
  characteristics to accurately identify web servers, despite the fact that they
  may have been obfuscated by changing the server banner strings, or by plug-ins
  such as mod_security or servermask. httprint can also be used to detect web
  enabled devices which do not have a server banner string, such as wireless
  access points, routers, switches, cable modems, etc. httprint uses text
  signature strings and it is very easy to add signatures to the signature
  database.
 
 **Installed size:** `1.45 MB`  
 **How to install:** `sudo apt install httprint`  
 
 ##### httprint
 
 
 ```
 root@kali:~# httprint -h
 httprint v0.301 (beta) - web server fingerprinting tool
 (c) 2003-2005 net-square solutions pvt. ltd. - see readme.txt
 http://net-square.com/httprint/
 httprint@net-square.com
 
 Usage:
 
 httprint {-h <host> | -i <input file> | -x <nmap xml file>} -s <signatures> [... options]
 
 -h <host>            host can be either an IP address, a symbolic name,
                      an IP range or a URL.
 -i <input text file> file containing list of hosts as described above
                      in text format.
 -x <nmap xml file>   Nmap -oX option generated xml file as input file.
                      Ports which can be considered as http ports are taken
                      from the nmapportlist.txt file.
 -s <signatures>      file containing http fingerprint signatures.
 
 Options:
 
 -o <output file>     output in html format.
 -oc <output file>    output in csv format.
 -ox <output file>    output in xml format.
 -noautossl           Disable automatic detection of SSL.
 -tp <ping timeout>   Ping timeout in milliseconds.
                      Default is 4000 ms. Maximum 30000 ms.
 -ct <1-100>          Default is 75. Do not change.
 -ua <User Agent>     Default is Mozilla/4.0 (compatible; MSIE 5.01;
                      Windows NT 5.0.
 -t <timeout>         Connection/read timeout in milliseconds.
                      Default is 10000 ms. Maximum 100000 ms.
 -r <retry>           Number of retries. Default is 3. Maximum 30.
 -P0                  Turn ICMP ping off.
 -nr                  No redirection. Do not automatically follow 301,
                      302 responses. Enabled by default.
 -th <threads>        Number of threads. Default is 8. Maximum 64.
 -?                   Displays this message.
 
 Examples:
 
 httprint -h www1.example.com -s signatures.txt
 httprint -h https://www2.example.com/ -s signatures.txt
 httprint -h http://www3.example.com:8080/ -s signatures.txt
 httprint -h www1.example.com -s signatures.txt -noautossl
 httprint -h 10.0.1.1-10.0.1.254 -s signatures.txt -o 10_0_1_x.html
 httprint -x nmap.xml -s signatures.txt -oc report.csv
 httprint -x nmap.xml -s signatures.txt -ox report.xml
 httprint -i input.txt -s signatures.txt -o output.html -th 16
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
