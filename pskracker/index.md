---
Title: pskracker
Homepage: https://github.com/soxrok2212/PSKracker
Repository: https://gitlab.com/kalilinux/packages/pskracker
Architectures: amd64 arm64 all
Version: 0.3.1+git20230831-1kali3
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### pskracker
 
  This package contains a collection of WPA/WPA2/WPS default algorithms/password
  generators/pingens written in C. This is useful for testing/auditing wireless
  networks and contains bleeding edge algorithms.
 
 **Installed size:** `37 KB`  
 **How to install:** `sudo apt install pskracker`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * pskracker-data 
 {{< /spoiler >}}
 
 ##### pskracker
 
 
 ```
 root@kali:~# pskracker -h
 
  PSKracker 0.2.1 WiFi Security Auditing Toolkit
  Copyright (c) 2017-2019, soxrok2212 <soxrok2212@gmail.com>
 
  Usage: pskracker <arguments>
 
  Required Arguments:
 
 	-t, --target	: Target model number
 
  Optional Arguments:
 
 	-b, --bssid	: BSSID of target
 	-W, --wps	: Output possible WPS pin(s) only
 	-G, --guest	: Output possible guest WPA key(s) only
 	-s, --serial	: Serial number
 	-f, --force	: Force full output
 	-h, --help	: Display help/usage
 
  Example:
 
  pskracker -t <target model> -b <bssid> -s <serial number>
 
 ```
 
 - - -
 
 ### pskracker-data
 
  This package contains a collection of WPA/WPA2/WPS default algorithms/password
  generators/pingens written in C. This is useful for testing/auditing wireless
  networks and contains bleeding edge algorithms.
   
  This package contains the dicts directory.
 
 **Installed size:** `110.85 MB`  
 **How to install:** `sudo apt install pskracker-data`  
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
