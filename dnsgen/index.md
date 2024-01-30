---
Title: dnsgen
Homepage: https://github.com/ProjectAnte/dnsgen
Repository: https://gitlab.com/kalilinux/packages/dnsgen
Architectures: all
Version: 1.0.4+git20200324-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### dnsgen
 
  This package provides a generator of a combination of domain names from the
  provided input. Combinations are created based on wordlist. Custom words are
  extracted per execution.
 
 **Installed size:** `37 KB`  
 **How to install:** `sudo apt install dnsgen`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-click
 * python3-tldextract
 {{< /spoiler >}}
 
 ##### dnsgen
 
 
 ```
 root@kali:~# dnsgen --help
 Usage: dnsgen [OPTIONS] FILENAME
 
 Options:
   -l, --wordlen INTEGER RANGE  Min length of custom words extracted from
                                domains.  [1<=x<=100]
   -w, --wordlist PATH          Path to custom wordlist.
   -f, --fast                   Fast generation.
   --help                       Show this message and exit.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
