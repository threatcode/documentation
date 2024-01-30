---
Title: nbtscan
Homepage: https://github.com/resurrecting-open-source-projects/nbtscan
Repository: https://salsa.debian.org/pkg-security-team/nbtscan
Architectures: any
Version: 1.7.2-2
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-information-gathering kali-tools-vulnerability 
Icon: images/nbtscan-logo.svg
PackagesInfo: |
 ### nbtscan
 
  NBTscan is a program for scanning IP networks for NetBIOS name information.
  It sends NetBIOS status query to each address in supplied range and lists
  received information in human readable form. For each responded host it
  lists IP address, NetBIOS computer name, logged-in user name and MAC address
  (such as Ethernet).
   
  This program is useful for security checks, network discovery and forensics
  investigations.
 
 **Installed size:** `57 KB`  
 **How to install:** `sudo apt install nbtscan`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### nbtscan
 
 Scan networks for NetBIOS name information
 
 ```
 root@kali:~# nbtscan --help
 
 NBTscan version 1.7.2.
 This is a free software and it comes with absolutely no warranty.
 You can use, distribute and modify it under terms of GNU GPL 2+.
 
 
 Usage:
 nbtscan [-v] [-d] [-e] [-l] [-t timeout] [-b bandwidth] [-r] [-q] [-s separator] [-m retransmits] (-f filename)|(<scan_range>) 
 	-v		verbose output. Print all names received
 			from each host
 	-d		dump packets. Print whole packet contents.
 	-e		Format output in /etc/hosts format.
 	-l		Format output in lmhosts format.
 			Cannot be used with -v, -s or -h options.
 	-t timeout	wait timeout milliseconds for response.
 			Default 1000.
 	-b bandwidth	Output throttling. Slow down output
 			so that it uses no more that bandwidth bps.
 			Useful on slow links, so that ougoing queries
 			don't get dropped.
 	-r		use local port 137 for scans. Win95 boxes
 			respond to this only.
 			You need to be root to use this option on Unix.
 	-q		Suppress banners and error messages,
 	-s separator	Script-friendly output. Don't print
 			column and record headers, separate fields with separator.
 	-h		Print human-readable names for services.
 			Can only be used with -v option.
 	-m retransmits	Number of retransmits. Default 0.
 	-f filename	Take IP addresses to scan from file filename.
 			-f - makes nbtscan take IP addresses from stdin.
 	<scan_range>	what to scan. Can either be single IP
 			like 192.168.1.1 or
 			range of addresses in one of two forms: 
 			xxx.xxx.xxx.xxx/xx or xxx.xxx.xxx.xxx-xxx.
 Examples:
 	nbtscan -r 192.168.1.0/24
 		Scans the whole C-class network.
 	nbtscan 192.168.1.25-137
 		Scans a range from 192.168.1.25 to 192.168.1.137
 	nbtscan -v -s : 192.168.1.0/24
 		Scans C-class network. Prints results in script-friendly
 		format using colon as field separator.
 		Produces output like that:
 		192.168.0.1:NT_SERVER:00U
 		192.168.0.1:MY_DOMAIN:00G
 		192.168.0.1:ADMINISTRATOR:03U
 		192.168.0.2:OTHER_BOX:00U
 		...
 	nbtscan -f iplist
 		Scans IP addresses specified in file iplist.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
