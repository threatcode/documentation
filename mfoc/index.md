---
Title: mfoc
Homepage: https://github.com/nfc-tools/mfoc
Repository: https://salsa.debian.org/pkg-security-team/mfoc
Architectures: any
Version: 0.10.7+git20180724-2
Metapackages: kali-linux-everything kali-linux-large kali-linux-nethunter kali-tools-rfid kali-tools-wireless 
Icon: images/mfoc-logo.svg
PackagesInfo: |
 ### mfoc
 
  MFOC is an open source implementation of "offline nested" attack by Nethemba.
   
  This program allow one to recover authentication keys from MIFARE Classic card.
   
  Please note that MFOC is able to recover keys from target only if it have
  a known key: default one (hardcoded in MFOC) or custom one (user provided
  using command line).
 
 **Installed size:** `69 KB`  
 **How to install:** `sudo apt install mfoc`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libnfc6 
 {{< /spoiler >}}
 
 ##### mfoc
 
 MIFARE Classic offline cracker
 
 ```
 root@kali:~# mfoc -h
 Usage: mfoc [-h] [-k key] [-f file] ... [-P probnum] [-T tolerance] [-O output]
 
   h     print this help and exit
   k     try the specified key in addition to the default keys
   f     parses a file of keys to add in addition to the default keys 
   P     number of probes per sector, instead of default of 20
   T     nonce tolerance half-range, instead of default of 20
         (i.e., 40 for the total range, in both directions)
   O     file in which the card contents will be written (REQUIRED)
   D     file in which partial card info will be written in case PRNG is not vulnerable
 
 Example: mfoc -O mycard.mfd
 Example: mfoc -k ffffeeeedddd -O mycard.mfd
 Example: mfoc -f keys.txt -O mycard.mfd
 Example: mfoc -P 50 -T 30 -O mycard.mfd
 
 This is mfoc version 0.10.7.
 For more information, run: 'man mfoc'.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
