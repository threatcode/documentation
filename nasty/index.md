---
Title: nasty
Homepage: https://github.com/folkertvanheusden/nasty
Repository: https://salsa.debian.org/pkg-security-team/nasty
Architectures: any
Version: 0.6+git20220929.9830b7a-1
Metapackages: kali-linux-everything kali-tools-forensics kali-tools-respond 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### nasty
 
  Nasty is a program that helps you to recover the passphrase of your PGP or
  GPG-key in case you forget or lost it. The following features will make things
  easier:
   - set minimum/maximum length of the passphrase
   - incremental mode, random mode or reads a file for guessing
   - charset filter
   
  This package is useful in forensics investigations.
 
 **Installed size:** `37 KB`  
 **How to install:** `sudo apt install nasty`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libgpgme11 
 {{< /spoiler >}}
 
 ##### nasty
 
 A tool which helps you to recover your GPG passphrase
 
 ```
 root@kali:~# nasty -h
 -a x	set minimum length of passphrase
 -b x	set maximum length
 -m x	set guessing mode:
 	incremental: try them all
 	random: try at random
 	file: read phrases from file (use -i)
 -i x	file to read the passphrases from
 -f x	file to write the found passphrase to
 -c x... charset, one or more from the following:
 	a: a-z
 	A: A-Z
 	0: 0-9
 	.: all ascii values (32...126)
 	+: 32...255 (default(!))
 -k x	filter string to select a key
 -v 	enable verbose mode
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
