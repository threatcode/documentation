---
Title: cisco7crack
Homepage: https://github.com/madrisan/cisco7crack
Repository: https://salsa.debian.org/pkg-security-team/cisco7crack
Architectures: any
Version: 0.0~git20121221.f1c21dd-3
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### cisco7crack
 
  This tool is used to crack Cisco Type 7 passwords. Can be used to encrypt
  and decrypt Cisco device passwords.
   
  Originally designed in order to allow quick decryption of stored passwords,
  Type 7 passwords are not a secure form of password storage. There are many
  tools available that can easily decrypt these passwords. Use of Type 7
  passwords should be avoided unless required by a feature that is in use on
  the Cisco IOS device.
 
 **Installed size:** `28 KB`  
 **How to install:** `sudo apt install cisco7crack`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### cisco7crack
 
 Crypt and decrypt the cisco type 7 passwords
 
 ```
 root@kali:~# cisco7crack -h
 *** cisco7crack v2.3.4 - San Oct 19, 2002
     copyright (c) 2002 by Davide Madrisan <davide.madrisan@atlavia.it>
     the GNU GPLv2 applies to this program and code
 
 usage:
    cisco7crack [-q] -c [-{a|#<0..15>}] <plaintext>
    cisco7crack [-q] [-d] <ciphertext>
    cisco7crack [-h]
 
 flags:    means:
   -c        crypt <plaintext>
   -a        display all the ways to crypt <plaintext>
   -#<n>     display the n-th way to crypt <plaintext>
   -d        decrypt <ciphertext> (default option)
   -q        cause cisco7crack to be really quiet
   -h        display this brief usage summary
 
 examples are:
    cisco7crack -c#3 '@l1c3&b0b'
    cisco7crack -c#3 -q n0v3rb0s3
    cisco7crack 082F1C5A1A490D43000F5E033F78373B
 
    a=`cisco7crack -cq b@shscr1pt`  # (bash shell)
    [ $? -eq 0 ] && echo "crypt: $a" || echo "error!"
 
 enjoy cracking the Cisco IOS pesky passwords...
 for bugs and suggestions, please contact me by e-mail
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
