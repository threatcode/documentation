---
Title: hakrawler
Homepage: https://github.com/hakluke/hakrawler
Repository: https://gitlab.com/kalilinux/packages/hakrawler
Architectures: any
Version: 2.0-kali1
Metapackages: kali-linux-everything kali-tools-web 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### hakrawler
 
  Fast golang web crawler for gathering URLs and JavaSript file locations.
  This is basically a simple implementation of the awesome Gocolly
  library.
 
 **Installed size:** `8.48 MB`  
 **How to install:** `sudo apt install hakrawler`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### hakrawler
 
 
 ```
 root@kali:~# hakrawler -h
 Usage of hakrawler:
   -d int
     	Depth to crawl. (default 2)
   -insecure
     	Disable TLS verification.
   -t int
     	Number of threads to utilise. (default 8)
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
