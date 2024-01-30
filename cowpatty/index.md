---
Title: cowpatty
Homepage: https://www.willhackforsushi.com/?page_id=50
Repository: https://salsa.debian.org/pkg-security-team/cowpatty
Architectures: any
Version: 4.8-3
Metapackages: kali-linux-everything kali-linux-large kali-tools-802-11 kali-tools-wireless 
Icon: images/cowpatty-logo.svg
PackagesInfo: |
 ### cowpatty
 
  If you are auditing WPA-PSK or WPA2-PSK networks, you can use
  this tool to identify weak passphrases that were used to generate the
  PMK.  Supply a libpcap capture file that includes the 4-way handshake, a
  dictionary file of passphrases to guess with, and the SSID for the
  network.
 
 **Installed size:** `77 KB`  
 **How to install:** `sudo apt install cowpatty`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libpcap0.8 
 * libssl3 
 {{< /spoiler >}}
 
 ##### cowpatty
 
 Brute-force dictionary attack against WPA-PSK
 
 ```
 root@kali:~# cowpatty -h
 cowpatty 4.8 - WPA-PSK dictionary attack. <jwright@hasborg.com>
 
 Usage: cowpatty [options]
 
 	-f 	Dictionary file
 	-d 	Hash file (genpmk)
 	-r 	Packet capture file
 	-s 	Network SSID (enclose in quotes if SSID includes spaces)
 	-c 	Check for valid 4-way frames, does not crack
 	-h 	Print this help information and exit
 	-v 	Print verbose information (more -v for more verbosity)
 	-V 	Print program version and exit
 
 ```
 
 - - -
 
 ##### genpmk
 
 WPA-PSK precomputation attack
 
 ```
 root@kali:~# genpmk -h
 genpmk 1.3 - WPA-PSK precomputation attack. <jwright@hasborg.com>
 Usage: genpmk [options]
 
 	-f 	Dictionary file
 	-d 	Output hash file
 	-s 	Network SSID
 	-h 	Print this help information and exit
 	-v 	Print verbose information (more -v for more verbosity)
 	-V 	Print program version and exit
 
 After precomputing the hash file, run cowpatty with the -d argument.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## genpmk Usage Example

Use the provided dictionary file (`-f /usr/share/wordlists/nmap.lst`) to generate a hashfile, saving it to a file (`-d cowpatty_dict`) for the given ESSID (`-s securenet`):

```
root@kali:~# genpmk -f /usr/share/wordlists/nmap.lst -d cowpatty_dict -s securenet
genpmk 1.3 - WPA-PSK precomputation attack. \&lt;jwright@hasborg.com\&gt;
File cowpatty_dict does not exist, creating.
key no. 1000: pinkgirl
1641 passphrases tested in 3.60 seconds: 456.00 passphrases/second
```

## cowpatty Usage Example

Use the provided hashfile (`-d cowpatty_dict`), read the packet capture (`-r Kismet-20181113-13-37-00-1.pcapdump`), and crack the password for the given ESSID (`-s 6F36E6`):

```
root@kali:~# cowpatty -d cowpatty_dict -r Kismet-20181113-13-37-00-1.pcapdump -s 6F36E6
cowpatty 4.8 - WPA-PSK dictionary attack. <jwright@hasborg.com>

Collected all necessary data to mount crack against WPA2/PSK passphrase.
Starting dictionary attack. Please be patient.

The PSK is "12345678".

5 passphrases tested in 0.00 seconds: 50000.00 passphrases/second
```
