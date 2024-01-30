---
Title: rephrase
Homepage: https://www.roguedaemon.net/rephrase/
Repository: https://salsa.debian.org/pkg-security-team/rephrase
Architectures: any
Version: 0.2-4
Metapackages: kali-linux-everything kali-tools-forensics kali-tools-respond 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### rephrase
 
  If you can nearly remember your GnuPG passphrase - but not quite - then
  Rephrase may be able to help. Tell Rephrase the parts of the passphrase you
  know, and any number of alternatives for the parts you're not sure about; and
  Rephrase will try all the alternatives, in all possible combinations, and tell
  you which combination (if any) gives you the correct passphrase.
 
 **Installed size:** `43 KB`  
 **How to install:** `sudo apt install rephrase`  
 
 {{< spoiler "Dependencies:" >}}
 * gnupg
 * libc6 
 {{< /spoiler >}}
 
 ##### rephrase
 
 Specialized passphrase recovery tool for GnuPG
 
 ```
 root@kali:~# rephrase -h
 rephrase (Rephrase) 0.2
 Copyright (C) 2003, 2014  Phil Lanch
 This program comes with ABSOLUTELY NO WARRANTY.
 This is free software, and you are welcome to redistribute it
 under certain conditions.  See the file COPYING for details.
 
 Usage: rephrase <key> | --gpg-key <key> | --gpg-symmetric <encrypted_file> | --luks <block_device>
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
