---
Title: httprobe
Homepage: https://github.com/tomnomnom/httprobe
Repository: https://gitlab.com/kalilinux/packages/httprobe
Architectures: any
Version: 0.2-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### httprobe
 
  This package contains a tool to test a domains list. It takes a list of
  domains and probe for working http and https servers.
 
 **Installed size:** `4.43 MB`  
 **How to install:** `sudo apt install httprobe`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### httprobe
 
 Tool to find working http and https servers from a domains list
 
 ```
 root@kali:~# httprobe -h
 Usage of httprobe:
   -c int
     	set the concurrency level (split equally between HTTPS and HTTP requests) (default 20)
   -method string
     	HTTP method to use (default "GET")
   -p value
     	add additional probe (proto:port)
   -prefer-https
     	only try plain HTTP if HTTPS fails
   -s	skip the default probes (http:80 and https:443)
   -t int
     	timeout (milliseconds) (default 10000)
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
