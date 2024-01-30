---
Title: bruteforce-luks
Homepage: https://github.com/glv2/bruteforce-luks
Repository: https://salsa.debian.org/pkg-security-team/bruteforce-luks
Architectures: linux-any
Version: 1.4.0-4
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### bruteforce-luks
 
  The program is used to try discovery a password for encrypted LUKS volume used
  to security reasons. It works trying decrypt at least one of the key slots by
  trying all the possible passwords. It is used in forensics and is especially
  useful if you know something about the password (i.e. you forgot a part of your
  password but still remember most of it).
   
  Because of cryptography complexity, crack the password of a LUKS volume without
  knowing anything about it would take way too much time (unless the password is
  really short and/or weak).
 
 **Installed size:** `47 KB`  
 **How to install:** `sudo apt install bruteforce-luks`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libcryptsetup12 
 {{< /spoiler >}}
 
 ##### bruteforce-luks
 
 Try to find the password of a LUKS volume
 
 ```
 root@kali:~# bruteforce-luks --help
 
 bruteforce-luks 1.4.0
 
 Usage: bruteforce-luks [options] <path to LUKS volume>
 
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
 
 Sending a USR1 signal to a running bruteforce-luks process
 makes it print progress info to standard error and continue.
 
 Error: unknown option: '-'.
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
