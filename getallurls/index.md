---
Title: getallurls
Homepage: https://github.com/lc/gau
Repository: https://gitlab.com/kalilinux/packages/getallurls
Architectures: any
Version: 1.0.7-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### getallurls
 
  This package contains getallurls (gau). It fetches known URLs from
  AlienVault's Open Threat Exchange (https://otx.alienvault.com), the Wayback
  Machine, and Common Crawl for any given domain. Inspired by Tomnomnom's
  waybackurls.
 
 **Installed size:** `6.42 MB`  
 **How to install:** `sudo apt install getallurls`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### getallurls
 
 
 ```
 root@kali:~# getallurls -h
 Usage of getallurls:
   -json
     	write output as json
   -o string
     	filename to write results to
   -p string
     	HTTP proxy to use
   -providers string
     	providers to fetch urls for (default "wayback,otx,commoncrawl")
   -random-agent
     	use random user-agent
   -retries uint
     	amount of retries for http client (default 5)
   -subs
     	include subdomains of target domain
   -v	enable verbose mode
   -version
     	show gau version
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
