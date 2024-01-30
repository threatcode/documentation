---
Title: subfinder
Homepage: https://github.com/projectdiscovery/subfinder
Repository: https://gitlab.com/kalilinux/packages/subfinder
Architectures: any
Version: 2.6.0-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### subfinder
 
  This package contains a subdomain discovery tool that discovers valid
  subdomains for websites by using passive online sources. It has a simple
  modular architecture and is optimized for speed. subfinder is built for doing
  one thing only - passive subdomain enumeration, and it does that very well.
 
 **Installed size:** `21.48 MB`  
 **How to install:** `sudo apt install subfinder`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### subfinder
 
 
 ```
 root@kali:~# subfinder -h
 Subfinder is a subdomain discovery tool that discovers subdomains for websites by using passive online sources.
 
 Usage:
   subfinder [flags]
 
 Flags:
 INPUT:
    -d, -domain string[]  domains to find subdomains for
    -dL, -list string     file containing list of domains for subdomain discovery
 
 SOURCE:
    -s, -sources string[]           specific sources to use for discovery (-s crtsh,github). Use -ls to display all available sources.
    -recursive                      use only sources that can handle subdomains recursively (e.g. subdomain.domain.tld vs domain.tld)
    -all                            use all sources for enumeration (slow)
    -es, -exclude-sources string[]  sources to exclude from enumeration (-es alienvault,zoomeye)
 
 FILTER:
    -m, -match string[]   subdomain or list of subdomain to match (file or comma separated)
    -f, -filter string[]   subdomain or list of subdomain to filter (file or comma separated)
 
 RATE-LIMIT:
    -rl, -rate-limit int  maximum number of http requests to send per second
    -t int                number of concurrent goroutines for resolving (-active only) (default 10)
 
 UPDATE:
    -up, -update                 update subfinder to latest version
    -duc, -disable-update-check  disable automatic subfinder update check
 
 OUTPUT:
    -o, -output string       file to write output to
    -oJ, -json               write output in JSONL(ines) format
    -oD, -output-dir string  directory to write output (-dL only)
    -cs, -collect-sources    include all sources in the output (-json only)
    -oI, -ip                 include host IP in output (-active only)
 
 CONFIGURATION:
    -config string                flag config file (default "/root/.config/subfinder/config.yaml")
    -pc, -provider-config string  provider config file (default "/root/.config/subfinder/provider-config.yaml")
    -r string[]                   comma separated list of resolvers to use
    -rL, -rlist string            file containing list of resolvers to use
    -nW, -active                  display active subdomains only
    -proxy string                 http proxy to use with subfinder
    -ei, -exclude-ip              exclude IPs from the list of domains
 
 DEBUG:
    -silent             show only subdomains in output
    -version            show version of subfinder
    -v                  show verbose output
    -nc, -no-color      disable color in output
    -ls, -list-sources  list all available sources
    -stats              report source statistics
 
 OPTIMIZATION:
    -timeout int   seconds to wait before timing out (default 30)
    -max-time int  minutes to wait for enumeration results (default 10)
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
