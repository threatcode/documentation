---
Title: crackle
Homepage: https://github.com/mikeryan/crackle
Repository: https://gitlab.com/kalilinux/packages/crackle
Architectures: any
Version: 0.1~git01282014-0kali3
Metapackages: kali-linux-everything kali-tools-bluetooth kali-tools-passwords kali-tools-wireless 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### crackle
 
  crackle exploits a flaw in the BLE pairing process that allows an attacker to
  guess or very quickly brute force the TK (Temporary Key). With the TK and other
  data collected from the pairing process, the STK (Short Term Key) and later the
  LTK (Long Term Key) can be collected.
   
  With the STK and LTK, all communications between the master and the slave can
  be decrypted
 
 **Installed size:** `54 KB`  
 **How to install:** `sudo apt install crackle`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libpcap0.8 
 {{< /spoiler >}}
 
 ##### crackle
 
 
 ```
 root@kali:~# crackle -h
 Usage: crackle -i <input.pcap> [-o <output.pcap>] [-l <ltk>]
 Cracks Bluetooth Low Energy encryption (AKA Bluetooth Smart)
 
 Major modes:  Crack TK // Decrypt with LTK
 
 Crack TK:
 
     Input PCAP file must contain a complete pairing conversation. If any
     packet is missing, cracking will not proceed. The PCAP file will be
     decrypted if -o <output.pcap> is specified. If LTK exchange is in
     the PCAP file, the LTK will be dumped to stdout.
     
 Decrypt with LTK:
 
     Input PCAP file must contain at least LL_ENC_REQ and LL_ENC_RSP
     (which contain the SKD and IV). The PCAP file will be decrypted if
     the LTK is correct.
 
     LTK format: string of hex bytes, no separator, most-significant
     octet to least-significant octet.
 
     Example: -l 81b06facd90fe7a6e9bbd9cee59736a7
 
 Optional arguments:
     -v   Be verbose
     -t   Run tests against crypto engine
 
 Written by Mike Ryan <mikeryan@lacklustre.net>
 See web site for more info:
     http://lacklustre.net/projects/crackle/
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## crackle Usage Example
Read the input file (`-i ltk_exchange.pcap`) and write the decrypted output to disk (`-o ltk-decrypted.pcap`):

```
root@kali:~# crackle -i ltk_exchange.pcap -o ltk-decrypted.pcap


!!!
TK found: 000000
ding ding ding, using a TK of 0! Just Cracks(tm)
!!!

Warning: packet is too short to be encrypted (1), skipping
LTK found: 7f62c053f104a5bbe68b1d896a2ed49c
Done, processed 712 total packets, decrypted 3
```
