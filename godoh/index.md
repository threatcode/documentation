---
Title: godoh
Homepage: https://github.com/sensepost/goDoH
Repository: https://gitlab.com/kalilinux/packages/godoh
Architectures: any
Version: 1.6+git20200517-0kali3
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### godoh
 
  This package contains a proof of concept Command and Control framework,
  written in Golang, that uses DNS-over-HTTPS as a transport medium. Currently
  supported providers include Google, Cloudflare but also contains the ability
  to use traditional DNS.
 
 **Installed size:** `7.42 MB`  
 **How to install:** `sudo apt install godoh`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### godoh
 
 
 ```
 root@kali:~# godoh -h
 A DNS (over-HTTPS) C2
     Version: 
 	By @leonjza from @sensepost
 
 Usage:
   godoh [flags]
   godoh [command]
 
 Available Commands:
   agent       Connect as an Agent to the DoH C2
   c2          Starts the godoh C2 server
   completion  Generate the autocompletion script for the specified shell
   help        Help about any command
   receive     Receive a file via DoH
   send        Send a file via DoH
   test        Test DNS communications
 
 Flags:
   -d, --domain string          DNS Domain to use. (ie: example.com)
   -h, --help                   help for godoh
   -p, --provider string        Preferred DNS provider to use. [possible: googlefront, google, cloudflare, quad9, raw] (default "google")
   -K, --validate-certificate   Validate DoH provider SSL certificates
 
 Use "godoh [command] --help" for more information about a command.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
