---
Title: veil
Homepage: https://github.com/Veil-Framework/Veil
Repository: https://gitlab.com/kalilinux/packages/veil
Architectures: i386 amd64 all
Version: 3.1.14-0kali2
Metapackages: kali-linux-everything kali-tools-post-exploitation kali-tools-social-engineering 
Icon: images/veil-logo.svg
PackagesInfo: |
 ### veil
 
  Veil is a tool designed to generate metasploit payloads that bypass
  common anti-virus solutions. It replaces the package veil-evasion.
 
 **Installed size:** `871 KB`  
 **How to install:** `sudo apt install veil`  
 
 {{< spoiler "Dependencies:" >}}
 * git
 * metasploit-framework
 * mingw-w64
 * mono-mcs
 * python3
 * python3-pycryptodome
 * ruby
 * sudo
 * unzip
 * wine
 {{< /spoiler >}}
 
 ##### veil
 
 
 ```
 root@kali:~# veil -h
  ==========================================================================
                  Veil (Setup Script) | [Updated]: 2018-05-08
  ==========================================================================
      [Web]: https://www.veil-framework.com/ | [Twitter]: @VeilFramework
  ==========================================================================
 
                  os = kali
           osversion = 2023.4
        osmajversion = 2023
                arch = x86_64
            trueuser = kali
    userprimarygroup = kali
         userhomedir = /home/kali
             rootdir = /usr/share/veil
             veildir = /var/lib/veil
           outputdir = /var/lib/veil/output
     dependenciesdir = /var/lib/veil/setup-dependencies
             winedir = /var/lib/veil/wine
           winedrive = /var/lib/veil/wine/drive_c
             gempath = Z:\var\lib\veil\wine\drive_c\Ruby187\bin\gem
 
  [I] Kali Linux 2023.4 x86_64 detected...
 
 
 
  [?] Are you sure you wish to install Veil?
 
      Continue with installation? ([y]es/[s]ilent/[N]o): 
 ```
 
 - - -
 
 ### veil-catapult
 
  This is a transitional package. It can safely be removed.
 
 **Installed size:** `12 KB`  
 **How to install:** `sudo apt install veil-catapult`  
 
 {{< spoiler "Dependencies:" >}}
 * veil
 {{< /spoiler >}}
 
 
 - - -
 
 ### veil-evasion
 
  This is a transitional package. It can safely be removed.
 
 **Installed size:** `12 KB`  
 **How to install:** `sudo apt install veil-evasion`  
 
 {{< spoiler "Dependencies:" >}}
 * veil
 {{< /spoiler >}}
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
