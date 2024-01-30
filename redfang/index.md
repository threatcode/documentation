---
Title: redfang
Homepage: 
Repository: https://gitlab.com/kalilinux/packages/redfang
Architectures: any
Version: 2.5-1kali3
Metapackages: kali-linux-everything kali-linux-large kali-tools-bluetooth kali-tools-wireless 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### redfang
 
  fang is a small proof-of-concept application to find non
  discoveredable bluetooth devices. This is done by brute
  forcing the last six (6) bytes of the bluetooth address of
  the device and doing a read_remote_name().
 
 **Installed size:** `40 KB`  
 **How to install:** `sudo apt install redfang`  
 
 {{< spoiler "Dependencies:" >}}
 * libbluetooth3 
 * libc6 
 {{< /spoiler >}}
 
 ##### fang
 
 
 ```
 root@kali:~# fang -h
 redfang - the bluetooth hunter ver 2.5
 (c)2003 @stake Inc
 author:   Ollie Whitehouse <ollie@atstake.com>
 enhanced: threads by Simon Halsall <s.halsall@eris.qinetiq.com>
 enhanced: device info discovery by Stephen Kapp <skapp@atstake.com>
 usage:
    fang [options]
 
 options:
    -r	range      i.e. 00803789EE76-00803789EEff
    -o	filename   Output Scan to Text Logfile
      	           An address can also be manf+nnnnnn, where manf
      	           is listed with the -l option and nnnnnn is the
      	           tail of the address. All addresses must be 12
      	           characters long
    -t	timeout    The connect timeout, this is 10000 by default
      	           Which is quick and yields results, increase for
      	           reliability
    -n	num        The number of dongles
    -d	           Show debug information
    -s	           Perform Bluetooth Discovery
    -l	           Show device manufacturer codes
 
    -h              Display help
 
 The devices are assumed to be hci0 to hci(n) where (n) is the number
 of threads -1, this is currently not configurable but maybe at a
 later date
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## redfang Usage Example

Scan the given range (`-r 00803789EE76-00803789EEff`) and discover Bluetooth devices (`-s`):

```
root@kali:~# fang -r 00803789EE76-00803789EEff -s
redfang - the bluetooth hunter ver 2.5
(c)2003 @stake Inc
author:   Ollie Whitehouse <ollie@atstake.com>
enhanced: threads by Simon Halsall <s.halsall@eris.qinetiq.com>
enhanced: device info discovery by Stephen Kapp <skapp@atstake.com>
Scanning 138 address(es)
Address range 00:80:37:89:ee:76 -> 00:80:37:89:ee:ff
Performing Bluetooth Discovery...
```
