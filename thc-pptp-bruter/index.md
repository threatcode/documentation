---
Title: thc-pptp-bruter
Homepage: http://www.thc.org/releases.php
Repository: https://gitlab.com/kalilinux/packages/thc-pptp-bruter
Architectures: any
Version: 0.1.4-1kali4
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-passwords 
Icon: images/thc-pptp-bruter-logo.svg
PackagesInfo: |
 ### thc-pptp-bruter
 
  Brute force program against pptp vpn endpoints (tcp port 1723).  Fully
  standalone. Supports latest MSChapV2 authentication. Tested against Windows
  and Cisco gateways.  Exploits a weakness in Microsoft's anti-brute force
  implementation which makes it possible to try 300 passwords the second.
 
 **Installed size:** `47 KB`  
 **How to install:** `sudo apt install thc-pptp-bruter`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libssl3 
 {{< /spoiler >}}
 
 ##### thc-pptp-bruter
 
 
 ```
 root@kali:~# thc-pptp-bruter -h
 thc-pptp-bruter [options] <remote host IP>
   -v        Verbose output / Debug output
   -W        Disable windows hack [default: enabled]
   -u <user> User [default: administrator]
   -w <file> Wordlist file [default: stdin]
   -p <n>    PPTP port [default: 1723]
   -n <n>    Number of parallel tries [default: 5]
   -l <n>    Limit to n passwords / sec [default: 100]
 
 Windows-Hack reuses the LCP connection with the same caller-id. This
 gets around MS's anti-brute forcing protection. It's enabled by default.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
