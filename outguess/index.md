---
Title: outguess
Homepage: https://github.com/resurrecting-open-source-projects/outguess
Repository: https://salsa.debian.org/pkg-security-team/outguess
Architectures: any
Version: 1:0.4-2
Metapackages: kali-linux-everything kali-tools-crypto-stego 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### outguess
 
  OutGuess is a universal tool for steganography that allows the insertion
  of hidden information into the redundant bits of data sources. The nature
  of the data source is irrelevant to the core of OutGuess.
   
  The program relies on data specific handlers that will extract redundant
  bits and write them back after modification. The supported formats are
  JPEG, PPM and PNM.
   
  This package is useful in forensics investigations and security actions.
 
 **Installed size:** `230 KB`  
 **How to install:** `sudo apt install outguess`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### histogram
 
 
 
 - - -
 
 ##### outguess
 
 Universal steganographic tool
 
 ```
 root@kali:~# outguess -h
 OutGuess 0.4 Universal Stego 1999-2021 Niels Provos and others
 
 outguess [options] [<input file> [<output file>]]
 	-h           print this usage help text and exit
 	-[sS] <n>    iteration start, capital letter for 2nd dataset
 	-[iI] <n>    iteration limit
 	-[kK] <key>  key
 	-[dD] <name> filename of dataset
 	-[eE]        use error correcting encoding
 	-p <param>   parameter passed to destination data handler
 	-r           retrieve message from data
 	-x <n>       number of key derivations to be tried
 	-m           mark pixels that have been modified
 	-t           collect statistic information
 	-F[+-]       turns statistical steganalysis foiling on/off.
 	             The default is on.
 ```
 
 - - -
 
 ##### outguess-extract
 
 Universal steganographic tool
 
 ```
 root@kali:~# outguess-extract -h
 OutGuess 0.4 Universal Stego 1999-2021 Niels Provos and others
 
 outguess-extract [options] [<input file> [<output file>]]
 	-h           print this usage help text and exit
 	-[sS] <n>    iteration start, capital letter for 2nd dataset
 	-[iI] <n>    iteration limit
 	-[kK] <key>  key
 	-[dD] <name> filename of dataset
 	-[eE]        use error correcting encoding
 	-p <param>   parameter passed to destination data handler
 	-r           retrieve message from data
 	-x <n>       number of key derivations to be tried
 	-m           mark pixels that have been modified
 	-t           collect statistic information
 	-F[+-]       turns statistical steganalysis foiling on/off.
 	             The default is on.
 ```
 
 - - -
 
 ##### seek_script
 
 Script using OutGuess to find an image that yields the best embedding
 
 ```
 root@kali:~# seek_script -h
 The file /tmp/fortune does not exist
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
