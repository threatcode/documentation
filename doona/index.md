---
Title: doona
Homepage: https://github.com/wireghoul/doona
Repository: https://salsa.debian.org/pkg-security-team/doona
Architectures: all
Version: 1.0+git20190108-2
Metapackages: kali-linux-everything kali-linux-large 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### doona
 
  Doona is a fork of the Bruteforce Exploit Detector Tool (BED).
  BED is a program which is designed to check daemons for
  potential buffer overflows, format string bugs etc.
 
 **Installed size:** `128 KB`  
 **How to install:** `sudo apt install doona`  
 
 {{< spoiler "Dependencies:" >}}
 * perl
 {{< /spoiler >}}
 
 ##### doona
 
 Network fuzzer forked from bed
 
 ```
 root@kali:~# doona -h
 
  Doona 1.0 by Wireghoul (www.justanotherhacker.com)
 
 Usage:
 
  ./doona.pl -m [module] <options>
 
  -m <module>   = DICT/FINGER/FTP/HTTP/HTTP_MORE/HTTP_SP/HTTP_WEBDAV/IMAP/IRC/LPD/NNTP/PJL/POP/PROXY/RTSP/SMTP/SOCKS4/SOCKS5/TFTP/WHOIS
  -c <int>      = Execute a health check after every <int> fuzz cases
  -t <target>   = Host to check (default: localhost)
  -p <port>     = Port to connect to (default: module specific standard port)
  -o <timeout>  = seconds to wait after each test (default: 2 seconds)
  -r <index>    = Resumes fuzzing at test case index
  -k            = Keep trying until server passes a health check
  -d            = Dump test case to stdout (use in combination with -r)
  -M <num>      = Exit after executing <num> number of fuzz cases
  -h            = Help (this text)
  use "./doona.pl -m [module] -h" for module specific option.
 
  Only -m is a mandatory switch.
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## doona Usage Example

Use the HTTP plugin (`-m HTTP`) to fuzz the target (`-t 192.168.1.15`), stopping after 5 cases (`-M 5`):

```
root@kali:~# doona -m HTTP -t 192.168.1.15 -M 5

 Doona 1.0 by Wireghoul (www.justanotherhacker.com)

 + Buffer overflow testing
    1/37   [XAXAX] ......
Max requests (5) completed, index: 5
````
