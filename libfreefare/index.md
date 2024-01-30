---
Title: libfreefare
Homepage: https://code.google.com/p/libfreefare/
Repository: http://anonscm.debian.org/gitweb/?p=collab-maint/libfreefare.git;a=summary
Architectures: any all
Version: 0.4.0-2.1
Metapackages: kali-linux-everything kali-linux-large kali-tools-rfid kali-tools-wireless 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### libfreefare-bin
 
  The libfreefare project aims to provide a convenient API for MIFARE
  card manipulations.
   
  This package includes some binaries that are useful for development purposes.
 
 **Installed size:** `232 KB`  
 **How to install:** `sudo apt install libfreefare-bin`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libfreefare0 
 * libnfc6 
 {{< /spoiler >}}
 
 ##### mifare-classic-format
 
 
 ```
 root@kali:~# mifare-classic-format -h
 usage: mifare-classic-format [-fy] [keyfile]
 
 Options:
   -f      Fast format (only erase MAD)
   -y      Do not ask for confirmation (dangerous)
   keyfile Use keys from dump in addition to internal default keys
 ```
 
 - - -
 
 ##### mifare-classic-read-ndef
 
 
 ```
 root@kali:~# mifare-classic-read-ndef -h
 usage: mifare-classic-read-ndef -o FILE
 
 Options:
   -y     Do not ask for confirmation
   -o     Extract NDEF message if available in FILE
 ```
 
 - - -
 
 ##### mifare-classic-write-ndef
 
 
 ```
 root@kali:~# mifare-classic-write-ndef -h
 usage: mifare-classic-write-ndef -i FILE
 
 Options:
   -y     Do not ask for confirmation
   -i     Use FILE as NDEF message to write on card ("-" = stdin)
 ```
 
 - - -
 
 ##### mifare-desfire-access
 
 
 ```
 root@kali:~# mifare-desfire-access -h
 mifare-desfire-access: usage: mifare-desfire-access
 ```
 
 - - -
 
 ##### mifare-desfire-create-ndef
 
 
 ```
 root@kali:~# mifare-desfire-create-ndef -h
 This application turns Mifare DESFire targets into NFC Forum Type 4 Tags.
 usage: mifare-desfire-create-ndef [-y] [-K 11223344AABBCCDD]
 
 Options:
   -y     Do not ask for confirmation
   -K     Provide another PICC key than the default one
 ```
 
 - - -
 
 ##### mifare-desfire-ev1-configure-ats
 
 
 ```
 root@kali:~# mifare-desfire-ev1-configure-ats -h
 usage: mifare-desfire-ev1-configure-ats [-y] [-K 11223344AABBCCDD]
 
 Options:
   -y     Do not ask for confirmation (dangerous)
   -K     Provide another PICC key than the default one
 ```
 
 - - -
 
 ##### mifare-desfire-ev1-configure-default-key
 
 
 ```
 root@kali:~# mifare-desfire-ev1-configure-default-key -h
 usage: mifare-desfire-ev1-configure-default-key [-y]
 
 Options:
   -y     Do not ask for confirmation
 ```
 
 - - -
 
 ##### mifare-desfire-ev1-configure-random-uid
 
 
 ```
 root@kali:~# mifare-desfire-ev1-configure-random-uid -h
 usage: mifare-desfire-ev1-configure-random-uid [-y] [-K 11223344AABBCCDD]
 
 Options:
   -y     Do not ask for confirmation (dangerous)
   -K     Provide another PICC key than the default one
 ```
 
 - - -
 
 ##### mifare-desfire-format
 
 
 ```
 root@kali:~# mifare-desfire-format -h
 usage: mifare-desfire-format [-y] [-K 11223344AABBCCDD]
 
 Options:
   -y     Do not ask for confirmation (dangerous)
   -K     Provide another PICC key than the default one
 ```
 
 - - -
 
 ##### mifare-desfire-info
 
 
 ```
 root@kali:~# mifare-desfire-info -h
 mifare-desfire-info: usage: mifare-desfire-info
 ```
 
 - - -
 
 ##### mifare-desfire-read-ndef
 
 
 ```
 root@kali:~# mifare-desfire-read-ndef -h
 This application reads a NDEF payload from a Mifare DESFire formatted as NFC Forum Type 4 Tag.
 usage: mifare-desfire-read-ndef [-y] -o FILE [-k 11223344AABBCCDD]
 
 Options:
   -y     Do not ask for confirmation
   -o     Extract NDEF message if available in FILE
   -k     Provide another NDEF Tag Application key than the default one
 ```
 
 - - -
 
 ##### mifare-desfire-write-ndef
 
 
 ```
 root@kali:~# mifare-desfire-write-ndef -h
 This application writes a NDEF payload into a Mifare DESFire formatted as NFC Forum Type 4 Tag.
 usage: mifare-desfire-write-ndef [-y] -i FILE [-k 11223344AABBCCDD]
 
 Options:
   -y     Do not ask for confirmation
   -i     Use FILE as NDEF message to write on card ("-" = stdin)
   -k     Provide another NDEF Tag Application key than the default one
 ```
 
 - - -
 
 ##### mifare-ultralight-info
 
 
 ```
 root@kali:~# mifare-ultralight-info -h
 mifare-ultralight-info: usage: mifare-ultralight-info
 ```
 
 - - -
 
 ### libfreefare-dev
 
  The libfreefare project aims to provide a convenient API for MIFARE
  card manipulations.
   
  This package contains development files.
 
 **Installed size:** `162 KB`  
 **How to install:** `sudo apt install libfreefare-dev`  
 
 {{< spoiler "Dependencies:" >}}
 * libfreefare0 
 * libnfc-dev
 {{< /spoiler >}}
 
 
 - - -
 
 ### libfreefare-doc
 
  The libfreefare project aims to provide a convenient API for MIFARE
  card manipulations.
   
  This package contains document files.
 
 **Installed size:** `157 KB`  
 **How to install:** `sudo apt install libfreefare-doc`  
 
 
 - - -
 
 ### libfreefare0
 
  The libfreefare project aims to provide a convenient API for MIFARE
  card manipulations.
   
  This package contains the libfreefare library.
 
 **Installed size:** `111 KB`  
 **How to install:** `sudo apt install libfreefare0`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libnfc6 
 * libssl3 
 {{< /spoiler >}}
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
