---
Title: wpa-sycophant
Homepage: https://github.com/sensepost/wpa_sycophant
Repository: https://gitlab.com/kalilinux/packages/wpa-sycophant
Architectures: any
Version: 1.0+git20210103-0kali3
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### wpa-sycophant
 
  This package contains a tool to relay phase 2 authentication attempts to
  access corporate wireless without cracking the password.
   
  To use this technique it is required that you run a rogue access point so that
  a legitimate user will connect to you so that you may relay the authentication
  attempt to Sycophant.
 
 **Installed size:** `866 KB`  
 **How to install:** `sudo apt install wpa-sycophant`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libnl-3-200 
 * libnl-genl-3-200 
 * libssl3 
 {{< /spoiler >}}
 
 ##### wpa_sycophant
 
 
 ```
 root@kali:~# wpa_sycophant -h
 Usage: sudo wpa_sycophant -c /etc/wpa-sycophant/wpa_sycophant_example.conf -i wlan0
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
