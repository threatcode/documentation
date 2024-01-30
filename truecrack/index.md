---
Title: truecrack
Homepage: https://github.com/lvaccaro/truecrack
Repository: https://gitlab.com/kalilinux/packages/truecrack
Architectures: any
Version: 3.6+git20150326-0kali3
Metapackages: kali-linux-everything kali-linux-large kali-tools-forensics kali-tools-gpu kali-tools-passwords kali-tools-respond 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### truecrack
 
  TrueCrack is a bruteforce password cracker for TrueCrypt
  (Copyright) volume.
  It is optimazed with Nvidia Cuda technology. It works with
  PBKDF2 (defined in PKCS5 v2.0) based on RIPEMD160 Key
  derivation function and XTS block cipher mode of operation
  used for hard disk encryption based on AES.
 
 **Installed size:** `2.61 MB`  
 **How to install:** `sudo apt install truecrack`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### truecrack
 
 Brute-force password cracker for TrueCrypt (Copyright) volumes.
 
 ```
 root@kali:~# truecrack -h
 TrueCrack v3.6
 Website: https://github.com/lvaccaro/truecrack
 Contact us: infotruecrack@gmail.com
 Bruteforce password cracker for Truecrypt volume. Optimazed with Nvidia Cuda technology.
 Based on TrueCrypt, freely available at http://www.truecrypt.org/
 Copyright (c) 2011 by Luca Vaccaro.
 
 Usage for Dictionary attack:
  truecrack -t truecrypt_file -w passwords_file [-k ripemd160 | -k sha512 | -k whirlpool] [-e aes | -e serpent | -e twofish] [-a blocks] [-b] [-H] [-r number]
 Usage for Alphabet attack:
  truecrack -t truecrypt_file -c alphabet [-s minlength] -m maxlength [-p string] [-k ripemd160 | -k sha512 | -k whirlpool] [-e aes | -e serpent | -e twofish] [-a blocks] [-b] [-H] [-r number]
 
 Options:
  -h --help					Display this information.
  -t --truecrypt <truecrypt_file>		Truecrypt volume file.
  -k --key <ripemd160 | sha512 | whirlpool>	Key derivation function (default ripemd160).
  -e --encryption <aes | serpent | twofish>	Encryption algorithm (default aes).
  -a --aggressive <blocks>			Number of parallel computations (board dependent).
  -w --wordlist <wordlist_file>			File of words, for Dictionary attack.
  -c --charset <alphabet>			Alphabet generator, for Alphabet attack.
  -s --startlength <minlength>			Starting length of passwords, for Alphabet attack (default 1).
  -m --maxlength <maxlength>			Maximum length of passwords, for Alphabet attack.
  -p --prefix <string>				Prefix the first part of the password, for Alphabet attack.
  -r --restore <number>				Restore the computation.
  -b --backup					Backup header instead of volume header.
  -H --hidden					Hidden Truecrypt volume.
  -v --verbose					Show computation messages.
 
 Sample for Dictionary attack:
  truecrack -t volume.tc -w dictionary.txt 
 Sample for Alphabet attack:
  truecrack -t volume.tc -c "1234567890" -s 4 -m 6
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## truecrack Usage Example

```
root@kali:~# truecrack -t truecrypt_vol -k ripemd160 -w passes.txt
TrueCrack v3.0
Website: http://code.google.com/p/truecrack
Contact us: infotruecrack@gmail.com
Found password:     "s3cr3t"
Password length:    "7"
Total computations: "78"
```
