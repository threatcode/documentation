---
Title: stegsnow
Homepage: https://www.darkside.com.au/snow
Repository: https://salsa.debian.org/pkg-security-team/stegsnow
Architectures: any
Version: 20130616-7
Metapackages: kali-linux-everything kali-tools-crypto-stego 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### stegsnow
 
  This utility can conceal messages in ASCII text by appending whitespaces to
  the end of lines. Because spaces and tabs are generally not visible in text
  viewers, the message is effectively hidden from casual observers. And if the
  built-in encryption is used, the message cannot be read even if it is detected.
   
  About the name: locating trailing whitespace in text is like finding a polar
  bear in a snowstorm. And it uses the ICE encryption algorithm, so the name is
  thematically consistent.
   
  This package is useful for personal security, forensics investigations and
  other actions.
 
 **Installed size:** `56 KB`  
 **How to install:** `sudo apt install stegsnow`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### stegsnow
 
 Whitespace steganography program
 
 ```
 root@kali:~# stegsnow -h
 Usage: stegsnow [-C] [-Q] [-S] [-V | --version] [-h | --help]
 	[-p passwd] [-l line-len] [-f file | -m message]
 	[infile [outfile]]
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
