---
Title: netmask
Homepage: https://github.com/tlby/netmask
Repository: https://salsa.debian.org/debian/netmask
Architectures: any
Version: 2.4.4-3
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-information-gathering 
Icon: images/netmask-logo.svg
PackagesInfo: |
 ### netmask
 
  This is a tiny program handy if you work with firewalls or routers
  occasionally (possibly using this as a helper for shell scripts).  It can
  determine the smallest set of network masks to specify a range of hosts.
  It can also convert between common IP netmask and address formats.
 
 **Installed size:** `55 KB`  
 **How to install:** `sudo apt install netmask`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### netmask
 
 A netmask generation and conversion program
 
 ```
 root@kali:~# netmask -h
 This is netmask, an address netmask generation utility
 Usage: netmask spec [spec ...]
   -h, --help			Print a summary of the options
   -v, --version			Print the version number
   -d, --debug			Print status/progress information
   -s, --standard		Output address/netmask pairs
   -c, --cidr			Output CIDR format address lists
   -i, --cisco			Output Cisco style address lists
   -r, --range			Output ip address ranges
   -x, --hex			Output address/netmask pairs in hex
   -o, --octal			Output address/netmask pairs in octal
   -b, --binary			Output address/netmask pairs in binary
   -n, --nodns			Disable DNS lookups for addresses
   -f, --files			Treat arguments as input files
 Definitions:
   a spec can be any of:
     address
     address:address
     address:+address
     address/mask
   an address can be any of:
     N		decimal number
     0N		octal number
     0xN		hex number
     N.N.N.N	dotted quad
     hostname	dns domain name
   a mask is the number of bits set to one from the left
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
