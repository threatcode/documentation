---
Title: pnscan
Homepage: https://github.com/ptrrkssn/pnscan
Repository: https://salsa.debian.org/pkg-security-team/pnscan
Architectures: any
Version: 1.14.1-2
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### pnscan
 
  Pnscan is a multi threaded port scanner that can scan a large network
  very quickly. If does not have all the features that nmap have but
  is much faster.
 
 **Installed size:** `65 KB`  
 **How to install:** `sudo apt install pnscan`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### pnscan
 
 Multi threaded port scanning tool
 
 ```
 root@kali:~# pnscan -h
 Usage: pnscan [<options>] [{<CIDR>|<host-range> <port-range>} | <service>]
 
 This program implements a multithreaded TCP port scanner.
 More information may be found at:
 	http://www.lysator.liu.se/~pen/pnscan
 
 Command line options:
 	-h             Display this information.
 	-V             Print version.
 	-v             Be verbose.
 	-d             Print debugging info.
 	-s             Lookup and print hostnames.
 	-i             Ignore case when scanning responses.
 	-S             Enable shutdown mode.
 	-l             Line oriented output.
 	-w<string>     Request string to send.
 	-W<hex list>   Hex coded request string to send.
 	-r<string>     Response string to look for.
 	-R<hex list>   Hex coded response string to look for.
 	-L<length>     Max bytes to print.
 	-t<msecs>      Connect/Write/Read timeout.
 	-n<workers>    Concurrent worker threads limit.
 ```
 
 - - -
 
 ##### t_listen
 
 
 ```
 root@kali:~# t_listen -h
 41926
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
