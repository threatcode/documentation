---
Title: onesixtyone
Homepage: https://github.com/trailofbits/onesixtyone
Repository: https://salsa.debian.org/pkg-security-team/onesixtyone
Architectures: any
Version: 0.3.4-1
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-information-gathering kali-tools-passwords 
Icon: images/onesixtyone-logo.svg
PackagesInfo: |
 ### onesixtyone
 
  onesixtyone is a simple SNMP scanner which sends SNMP requests for the
  sysDescr value asynchronously with user-adjustable sending times and
  then logs the responses which gives the description of the software
  running on the device.
   
  Running onesixtyone on a class B network (switched 100Mbs with 1Gbs
  backbone) with -w 10 gives a performance of 3 seconds per class C, with
  no dropped packets, and all 65536 IP addresses were scanned in less than
  13 minutes.
 
 **Installed size:** `177 KB`  
 **How to install:** `sudo apt install onesixtyone`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### onesixtyone
 
 Fast and simple SNMP scanner
 
 ```
 root@kali:~# onesixtyone -h
 onesixtyone 0.3.3 [options] <host> <community>
   -c <communityfile> file with community names to try
   -i <inputfile>     file with target hosts
   -o <outputfile>    output log
   -p                 specify an alternate destination SNMP port
   -d                 debug mode, use twice for more information
 
   -s                 short mode, only print IP addresses
 
   -w n               wait n milliseconds (1/1000 of a second) between sending packets (default 10)
   -q                 quiet mode, do not print log to stdout, use with -o
 host is either an IPv4 address or an IPv4 address and a netmask
 default community names are: public private
 
 Max number of hosts : 		65536
 Max community length: 		32
 Max number of communities: 	16384
 
 
 examples: onesixtyone 192.168.4.0/24 public
           onesixtyone -c dict.txt -i hosts -o my.log -w 100
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
