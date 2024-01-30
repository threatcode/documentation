---
Title: altdns
Homepage: https://github.com/infosec-au/altdns
Repository: https://gitlab.com/kalilinux/packages/altdns
Architectures: all
Version: 1.0.2-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### altdns
 
  This package contains a DNS recon tool that allows for the discovery of
  subdomains that conform to patterns. Altdns takes in words that could be
  present in subdomains under a domain (such as test, dev, staging) as well as
  takes in a list of subdomains that you know of.
   
  From these two lists that are provided as input to altdns, the tool then
  generates a massive output of "altered" or "mutated" potential subdomains that
  could be present. It saves this output so that it can then be used by your
  favourite DNS bruteforcing tool.
 
 **Installed size:** `37 KB`  
 **How to install:** `sudo apt install altdns`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3 
 * python3-dnspython
 * python3-termcolor
 * python3-tldextract
 {{< /spoiler >}}
 
 ##### altdns
 
 
 ```
 root@kali:~# altdns -h
 usage: altdns [-h] -i INPUT -o OUTPUT [-w WORDLIST] [-r] [-n] [-e]
               [-d DNSSERVER] [-s SAVE] [-t THREADS]
 
 options:
   -h, --help            show this help message and exit
   -i INPUT, --input INPUT
                         List of subdomains input
   -o OUTPUT, --output OUTPUT
                         Output location for altered subdomains
   -w WORDLIST, --wordlist WORDLIST
                         List of words to alter the subdomains with
   -r, --resolve         Resolve all altered subdomains
   -n, --add-number-suffix
                         Add number suffix to every domain (0-9)
   -e, --ignore-existing
                         Ignore existing domains in file
   -d DNSSERVER, --dnsserver DNSSERVER
                         IP address of resolver to use (overrides system
                         default)
   -s SAVE, --save SAVE  File to save resolved altered subdomains to
   -t THREADS, --threads THREADS
                         Amount of threads to run simultaneously
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
