---
Title: finalrecon
Homepage: https://github.com/thewhiteh4t/FinalRecon
Repository: https://gitlab.com/kalilinux/packages/finalrecon
Architectures: all
Version: 1.1.6-0kali2
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### finalrecon
 
  A fast and simple Python script for web reconnaissance that follows
  a modular structure and provides detailed information on various areas.
 
 **Installed size:** `374 KB`  
 **How to install:** `sudo apt install finalrecon`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-aiodns
 * python3-aiohttp
 * python3-bs4
 * python3-dnslib
 * python3-lxml
 * python3-psycopg2
 * python3-requests
 * python3-tldextract
 {{< /spoiler >}}
 
 ##### finalrecon
 
 
 ```
 root@kali:~# finalrecon -h
 usage: finalrecon [-h] [--headers] [--sslinfo] [--whois] [--crawl] [--dns]
                   [--sub] [--dir] [--wayback] [--ps] [--full] [-dt DT]
                   [-pt PT] [-T T] [-w W] [-r] [-s] [-sp SP] [-d D] [-e E]
                   [-o O]
                   url
 
 FinalRecon - The Last Web Recon Tool You Will Need | v1.1.6
 
 positional arguments:
   url         Target URL
 
 options:
   -h, --help  show this help message and exit
   --headers   Header Information
   --sslinfo   SSL Certificate Information
   --whois     Whois Lookup
   --crawl     Crawl Target
   --dns       DNS Enumeration
   --sub       Sub-Domain Enumeration
   --dir       Directory Search
   --wayback   Wayback URLs
   --ps        Fast Port Scan
   --full      Full Recon
 
 Extra Options:
   -dt DT      Number of threads for directory enum [ Default : 30 ]
   -pt PT      Number of threads for port scan [ Default : 50 ]
   -T T        Request Timeout [ Default : 30.0 ]
   -w W        Path to Wordlist [ Default : wordlists/dirb_common.txt ]
   -r          Allow Redirect [ Default : False ]
   -s          Toggle SSL Verification [ Default : True ]
   -sp SP      Specify SSL Port [ Default : 443 ]
   -d D        Custom DNS Servers [ Default : 1.1.1.1 ]
   -e E        File Extensions [ Example : txt, xml, php ]
   -o O        Export Format [ Default : txt ]
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
