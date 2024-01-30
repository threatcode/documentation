---
Title: ohrwurm
Homepage: http://mazzoo.de/blog/2006/08/25#ohrwurm
Repository: https://gitlab.com/kalilinux/packages/ohrwurm
Architectures: any
Version: 0.1-1kali4
Metapackages: kali-linux-everything kali-linux-large kali-tools-voip kali-tools-vulnerability 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### ohrwurm
 
  ohrwurm is a small and simple RTP fuzzer that has been
  successfully tested on a small number of SIP phones.
  Features:
   
      - reads SIP messages to get information of the RTP port
      numbers
      - reading SIP can be omitted by providing the RTP port
      numbers, sothat any RTP traffic can be fuzzed
      - RTCP traffic can be suppressed to avoid that codecs
      - learn about the "noisy line"
      - special care is taken to break RTP handling itself
      - the RTP payload is fuzzed with a constant BER
      - the BER is configurable
      - requires arpspoof from dsniff to do the MITM attack
      - requires both phones to be in a switched LAN (GW
      operation only works partially)
 
 **Installed size:** `32 KB`  
 **How to install:** `sudo apt install ohrwurm`  
 
 {{< spoiler "Dependencies:" >}}
 * dsniff
 * libc6 
 * libpcap0.8 
 {{< /spoiler >}}
 
 ##### ohrwurm
 
 
 ```
 root@kali:~# ohrwurm -h
 ohrwurm-0.1
 
 usage: ohrwurm -a <IP target a> -b <IP target b> [-s <randomseed>] [-e <bit error ratio in %>] [-i <interface>] [-A <RTP port a> -B <RTP port b>]
 
 	-a <IPv4 address A in dot-decimal notation> SIP phone A
 	-b <IPv4 address B in dot-decimal notation> SIP phone B
 	-s <integer> randomseed (default: read from /dev/urandom)
 	-e <double> bit error ratio in % (default: 1.230000)
 	-i <interfacename> network interface (default: eth0)
 	-t suppress RTCP packets (default: dont suppress)
 	-A <port number> of RTP port on IP a (requires -B)
 	-B <port number> of RTP port on IP b (requires -A)
 	   note: using -A and -B skips SIP sniffing, any RTP can be fuzzed
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## ohrwurm Usage Example

Fuzz two hosts (`-a 192.168.1.123 -b 192.168.1.15`), both on port 6970 (`-A 6970 -B 6970`), through interface eth0 (`-i eth0`):

```
root@kali:~# ohrwurm -a 192.168.1.123 -b 192.168.1.15 -A 6970 -B 6970 -i eth0
ohrwurm-0.1
using random seed 2978455466
```
