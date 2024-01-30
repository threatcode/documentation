---
archived: "true"
Title: netkit-ftp
Homepage: 
Repository: 
Architectures: any
Version: 0.17-35
Metapackages: kali-linux-arm kali-linux-core kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-linux-nethunter 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### ftp
 
  This is the user interface to the ARPANET standard File Transfer Protocol.
  The program allows a user to transfer files to and from a remote network
  site.
 
 **Installed size:** `137 KB`  
 **How to install:** `sudo apt install ftp`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libreadline8 
 * netbase
 {{< /spoiler >}}
 
 ##### netkit-ftp
 
 Internet file transfer program
 
 ```
 root@kali:~# netkit-ftp -h
 
 	Usage: { ftp | pftp } [-46pinegvtd] [hostname]
 	   -4: use IPv4 addresses only
 	   -6: use IPv6, nothing else
 	   -p: enable passive mode (default for pftp)
 	   -i: turn off prompting during mget
 	   -n: inhibit auto-login
 	   -e: disable readline support, if present
 	   -g: disable filename globbing
 	   -v: verbose mode
 	   -t: enable packet tracing [nonfunctional]
 	   -d: enable debugging
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
