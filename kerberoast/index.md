---
Title: kerberoast
Homepage: https://github.com/nidem/kerberoast
Repository: https://gitlab.com/kalilinux/packages/kerberoast
Architectures: all
Version: 0.0~git20221231.cc5aa6e-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### kerberoast
 
  This package contains a series of tools for attacking MS Kerberos
  implementations:
    - extract all accounts in use as SPN using built in MS tools
    - extract the acquired tickets from ram with Mimikatz
    - crack with tgsrepcrack
    - request Ticket(s)
    - etc
 
 **Installed size:** `81 KB`  
 **How to install:** `sudo apt install kerberoast`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-pyasn1
 * python3-scapy
 {{< /spoiler >}}
 
 ##### kerberoast
 
 
 ```
 root@kali:~# kerberoast -h
 
 > kerberoast ~ tools for attacking MS Kerberos implementations
 
 /usr/share/kerberoast
 |-- GetUserSPNs.ps1
 |-- GetUserSPNs.vbs
 |-- extracttgsrepfrompcap.py
 |-- kerberoast.py
 |-- kerberos.py
 |-- kirbi2john.py
 |-- krbroast-pcap2hashcat.py
 |-- pac.py
 `-- tgsrepcrack.py
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
