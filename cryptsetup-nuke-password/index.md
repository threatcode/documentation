---
Title: cryptsetup-nuke-password
Homepage: https://salsa.debian.org/pkg-security-team/cryptsetup-nuke-password
Repository: https://salsa.debian.org/pkg-security-team/cryptsetup-nuke-password
Architectures: any
Version: 4+nmu1+kali1
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-protect 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### cryptsetup-nuke-password
 
  Installing this package lets you configure a special "nuke password" that
  can be used to destroy the encryption keys required to unlock the encrypted
  partitions. This password can be entered in the usual early-boot prompt
  asking the passphrase to unlock the encrypted partition(s).
   
  This provides a relatively stealth way to make your data unreadable in
  case you fear that your computer is going to be seized.
   
  After installation, use “dpkg-reconfigure cryptsetup-nuke-password” to
  configure your nuke password.
 
 **Installed size:** `61 KB`  
 **How to install:** `sudo apt install cryptsetup-nuke-password`  
 
 {{< spoiler "Dependencies:" >}}
 * cryptsetup-bin
 * debconf  | debconf-2.0
 * libc6 
 * libcrypt1 
 {{< /spoiler >}}
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
