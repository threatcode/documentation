---
Title: copy-router-config
Homepage: https://www.offsec.com
Repository: https://gitlab.com/kalilinux/packages/copy-router-config
Architectures: all
Version: 1.0-1kali5
Metapackages: kali-linux-everything kali-linux-large kali-tools-vulnerability 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### copy-router-config
 
  This package copies configuration files from Cisco devices
  running SNMP.
 
 **Installed size:** `12 KB`  
 **How to install:** `sudo apt install copy-router-config`  
 
 {{< spoiler "Dependencies:" >}}
 * perl-cisco-copyconfig
 {{< /spoiler >}}
 
 ##### copy-router-config.pl
 
 
 ```
 root@kali:~# copy-router-config.pl -h
 
 ######################################################
 # Copy Cisco Router config  - Using SNMP
 # Hacked up by muts - muts@offensive-security.com
 #######################################################
 
 Usage : ./copy-copy-config.pl <router-ip> <tftp-serverip> <community> 
 
 Make sure a TFTP server is set up, prefferably running from /tmp ! 
 
 ```
 
 - - -
 
 ##### merge-router-config.pl
 
 
 ```
 root@kali:~# merge-router-config.pl -h
 
 ######################################################
 # Merge Cisco Router config  - Using SNMP
 # Hacked up by muts - muts@offensive-security.com
 #######################################################
 
 Usage : ./merge-copy-config.pl <router-ip> <tftp-serverip> <community> 
 
 Make sure a TFTP server is set up, prefferably running from /tmp ! 
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## copy-router-config Usage Example

Copy the config from the router (`192.168.1.1`) to the TFTP server (`192.168.1.15`), authenticating with the community string (`private`):

```
root@kali:~# copy-router-config.pl 192.168.1.1 192.168.1.15 private
```

## merge-router-config Usage Example

Merge the config with the router (`192.168.1.1`), copying from the TFTP server (`192.168.1.15`), using the community string (`private`):

```
root@kali:~# merge-router-config.pl 192.168.1.1 192.168.1.15 private
```
