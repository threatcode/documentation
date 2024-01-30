---
Title: bruteforce-wallet
Homepage: https://github.com/glv2/bruteforce-wallet
Repository: https://salsa.debian.org/pkg-security-team/bruteforce-wallet
Architectures: any
Version: 1.5.3-6
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### bruteforce-wallet
 
  bruteforce-wallet try to find the password of an encrypted
  Peercoin (or Bitcoin, Litecoin, etc...) wallet file.
  It can be used in two ways:
   
     - Try all possible passwords given a charset.
     - Try all passwords in a file (dictionary).
   
  bruteforce-wallet have the following features:
   
     - You can specify the number of threads to use when cracking a file.
     - Sending a USR1 signal to a running bruteforce-wallet process
       makes it print progress and continue.
     - There are an exhaustive mode and a dictionary mode.
   
  In the exhaustive mode the program tries to decrypt one of the encrypted
  addresses in the wallet by trying all the possible passwords.
  It is especially useful if you know something about the password
  (i.e. you forgot a part of your password but still remember most of it).
  Finding the password of a wallet without knowing anything about it would
  take way too much time (unless the password is really short and/or weak).
  There are some command line options to specify:
   
     - The minimum password length to try.
     - The maximum password length to try.
     - The beginning of the password.
     - The end of the password.
     - The character set to use (among the characters of the current locale).
   
  In dictionary mode the program tries to decrypt one of the encrypted
  addresses in the wallet by trying all the passwords contained in a file.
  The file must have one password per line.
   
  This package is useful for finding the password for a Peercoin encrypted
  wallet file (or Bitcoin, Litecoin, etc ...) (i.e. wallet.dat).
 
 **Installed size:** `52 KB`  
 **How to install:** `sudo apt install bruteforce-wallet`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libdb5.3
 * libssl3 
 {{< /spoiler >}}
 
 ##### bruteforce-wallet
 
 Try to find the password of an encrypted wallet file
 
 ```
 root@kali:~# bruteforce-wallet --help
 
 bruteforce-wallet 1.5.3
 
 Usage: bruteforce-wallet [options] <wallet file>
 
 Options:
   -b <string>  Beginning of the password.
                  default: ""
   -e <string>  End of the password.
                  default: ""
   -f <file>    Read the passwords from a file instead of generating them.
   -h           Show help and quit.
   -l <length>  Minimum password length (beginning and end included).
                  default: 1
   -m <length>  Maximum password length (beginning and end included).
                  default: 8
   -s <string>  Password character set.
                  default: "0123456789ABCDEFGHIJKLMNOPQRSTU
                            VWXYZabcdefghijklmnopqrstuvwxyz"
   -t <n>       Number of threads to use.
                  default: 1
   -v <n>       Print progress info every n seconds.
   -w <file>    Restore the state of a previous session if the file exists,
                then write the state to the file regularly (~ every minute).
 
 Sending a USR1 signal to a running bruteforce-wallet process
 makes it print progress info to standard error and continue.
 
 Error: unknown option: '-'.
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
