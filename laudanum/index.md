---
Title: laudanum
Homepage: https://sourceforge.net/projects/laudanum/
Repository: https://gitlab.com/kalilinux/packages/laudanum
Architectures: all
Version: 1.0+r36-0kali6
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-post-exploitation kali-tools-web 
Icon: images/laudanum-logo.svg
PackagesInfo: |
 ### laudanum
 
  Laudanum is a collection of injectable files, designed to
  be used in a pentest when SQL injection flaws are found and
  are in multiple languages for different environments.They
  provide functionality such as shell, DNS query, LDAP
  retrieval and others.
 
 **Installed size:** `199 KB`  
 **How to install:** `sudo apt install laudanum`  
 
 {{< spoiler "Dependencies:" >}}
 * kali-defaults
 * python3
 {{< /spoiler >}}
 
 ##### laudanum
 
 
 ```
 root@kali:~# laudanum -h
 
 > laudanum ~ Collection of injectable web files
 
 /usr/share/laudanum
 |-- asp
 |-- aspx
 |-- cfm
 |-- helpers
 |-- jsp
 |-- php
 `-- wordpress
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
