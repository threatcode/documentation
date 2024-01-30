---
Title: fiked
Homepage: https://www.roe.ch/FakeIKEd
Repository: https://gitlab.com/kalilinux/packages/fiked
Architectures: any
Version: 0.0.5-1kali6
Metapackages: kali-linux-everything kali-linux-large kali-tools-sniffing-spoofing 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### fiked
 
  FakeIKEd, or fiked for short, is a fake IKE daemon
  supporting just enough of the standards and Cisco
  extensions to attack commonly found insecure Cisco VPN
  PSK+XAUTH based IPsec authentication setups in what could
  be described as a semi MitM attack. Fiked can impersonate a
  VPN gateway’s IKE responder in order to capture XAUTH login
  credentials; it doesn’t currently do the client part of
  full MitM.
 
 **Installed size:** `172 KB`  
 **How to install:** `sudo apt install fiked`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libgcrypt20 
 * libnet1 
 {{< /spoiler >}}
 
 ##### fiked
 
 A fake IKE PSK+XAUTH daemon based on vpnc
 
 ```
 root@kali:~# fiked --help
 fiked: invalid option -- '-'
 Usage: fiked [-rdqhV] -g gw -k id:psk [-k ..] [-u user] [-l file] [-L file]
 	-r	use raw socket: forge ip src addr to match <gateway> (disables -u)
 	-d	detach from tty and run as a daemon (implies -q)
 	-q	be quiet, don't write anything to stdout
 	-h	print help and exit
 	-V	print version and exit
 	-g gw	VPN gateway address to impersonate
 	-k i:k	pre-shared key aka. group password, shared secret, prefixed
 		with its group/key id (first -k sets default)
 	-u user	drop privileges to unprivileged user account
 	-l file	append results to credential log file
 	-L file	verbous logging to file instead of stdout
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
