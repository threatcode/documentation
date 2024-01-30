---
Title: eapmd5pass
Homepage: https://www.willhackforsushi.com/?page_id=67
Repository: https://gitlab.com/kalilinux/packages/eapmd5pass
Architectures: any
Version: 1.5-0kali1
Metapackages: kali-linux-everything kali-linux-large kali-tools-802-11 kali-tools-wireless 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### eapmd5pass
 
  EAP-MD5 is a legacy authentication mechanism that does not provide sufficient
  protection for user authentication credentials.  Users who authenticate using
  EAP-MD5 subject themselves to an offline dictionary attack vulnerability.
   
  This tool reads from a live network interface in monitor-mode, or from a
  stored libpcap capture file, and extracts the portions of the EAP-MD5
  authentication exchange.  Once the challenge and response portions have been
  collected from this exchange, eapmd5pass will mount an offline dictionary
  attack against the user's password.
 
 **Installed size:** `101 KB`  
 **How to install:** `sudo apt install eapmd5pass`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libpcap0.8 
 * libssl3 
 {{< /spoiler >}}
 
 ##### eapmd5pass
 
 
 ```
 root@kali:~# eapmd5pass -h
 eapmd5pass - Dictionary attack against EAP-MD5
 
 Usage: eapmd5pass [ -i <int> | -r <pcapfile> ] [ -w wordfile ] [options]
 
   -i <iface>	interface name
   -r <pcapfile>	read from a named libpcap file
   -w <wordfile>	use wordfile for possible passwords.
   -b <bssid>	BSSID of target network (default: all)
   -U <username>	Username of EAP-MD5 user.
   -C <chal>	EAP-MD5 challenge value.
   -R <response>	EAP-MD5 response value.
   -E <eapid>	EAP-MD5 response EAP ID value.
   -v		increase verbosity level (max 3)
   -V		version information
   -h		usage information
 
 The "-r" and "[-U|-C|-R|-E]" options are not meant to be used together.  Use -r
 when a packet capture is available.  Specify the username, challenge and
 response when available through other means.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
