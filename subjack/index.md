---
Title: subjack
Homepage: https://github.com/haccer/subjack
Repository: https://gitlab.com/kalilinux/packages/subjack
Architectures: any
Version: 2.1-0kali2
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### subjack
 
  This package contains a Subdomain Takeover tool written in Go designed to scan
  a list of subdomains concurrently and identify ones that are able to be
  hijacked. With Go's speed and efficiency, this tool really stands out when it
  comes to mass-testing. Always double check the results manually to rule out
  false positives.
   
  Subjack will also check for subdomains attached to domains that don't exist
  (NXDOMAIN) and are available to be registered.
 
 **Installed size:** `10.73 MB`  
 **How to install:** `sudo apt install subjack`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### subjack
 
 
 ```
 root@kali:~# subjack -h
 Usage of subjack:
   -a	Find those hidden gems by sending requests to every URL. (Default: Requests are only sent to URLs with identified CNAMEs).
   -c string
     	Path to configuration file. (default "/usr/share/subjack/fingerprints.json")
   -d string
     	Domain.
   -m	Flag the presence of a dead record, but valid CNAME entry.
   -o string
     	Output results to file (Subjack will write JSON if file ends with '.json').
   -ssl
     	Force HTTPS connections (May increase accuracy (Default: http://).
   -t int
     	Number of concurrent threads (Default: 10). (default 10)
   -timeout int
     	Seconds to wait before connection timeout (Default: 10). (default 10)
   -v	Display more information per each request.
   -w string
     	Path to wordlist.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
