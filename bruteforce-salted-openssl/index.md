---
Title: bruteforce-salted-openssl
Homepage: https://github.com/glv2/bruteforce-salted-openssl
Repository: https://salsa.debian.org/pkg-security-team/bruteforce-salted-openssl
Architectures: any
Version: 1.4.2-4
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### bruteforce-salted-openssl
 
  bruteforce-salted-openssl try to find the passphrase or password of a file
  that was encrypted with the openssl command. It can be used in two ways:
   
     - Try all possible passwords given a charset.
     - Try all passwords in a file (dictionary).
   
  bruteforce-salted-openssl have the following features:
   
     - You can specify the number of threads to use when cracking a file.
     - The program should be able to use all the digests and symmetric ciphers
       available with the OpenSSL libraries installed on your system.
     - Sending a USR1 signal to a running bruteforce-salted-openssl process
       makes it print progress and continue.
     - There are an exhaustive mode and a dictionary mode.
   
  In the exhaustive mode the program tries to decrypt the file by trying all
  possible passwords. It is especially useful if you know something about the
  password (i.e. you forgot a part of your password but still remember most of
  it). Finding the password of the file without knowing anything about it would
  take way too much time (unless the password is really short and/or weak).
  There are some command line options to specify:
   
     - The minimum password length to try.
     - The maximum password length to try.
     - The beginning of the password.
     - The end of the password.
     - The character set to use (among the characters of the current locale).
   
  In dictionary mode the program tries to decrypt the file by trying all the
  passwords contained in a file. The file must have one password per line.
   
  This package is useful for security, pentests and forensics investigations.
 
 **Installed size:** `54 KB`  
 **How to install:** `sudo apt install bruteforce-salted-openssl`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libssl3 
 {{< /spoiler >}}
 
 ##### bruteforce-salted-openssl
 
 Try to find the passphrase for files encrypted with OpenSSL
 
 ```
 root@kali:~# bruteforce-salted-openssl --help
 
 bruteforce-salted-openssl 1.4.2
 
 Usage: bruteforce-salted-openssl [options] <filename>
 
 Options:
   -1           Stop the program after finding the first password candidate.
 
   -a           List the available cipher and digest algorithms.
 
   -B <file>    Search using binary passwords (instead of character passwords).
                Write candidates to <file>.
 
   -b <string>  Beginning of the password.
                  default: ""
 
   -c <cipher>  Cipher for decryption.
                  default: aes-256-cbc
 
   -d <digest>  Digest for key and initialization vector generation.
                  default: md5
 
   -e <string>  End of the password.
                  default: ""
 
   -f <file>    Read the passwords from a file instead of generating them.
 
   -h           Show help and quit.
 
   -L <n>       Limit the maximum number of tested passwords to <n>.
 
   -l <length>  Minimum password length (beginning and end included).
                  default: 1
 
   -M <string>  Consider the decryption as successful when the data starts
                with <string>. Without this option, the decryption is considered
                as successful when the data contains mostly printable ASCII
                characters (at least 90%).
 
   -p <n>       Preview and check the first N decrypted bytes for the magic string.
                If the magic string is present, try decrypting the rest of the data.
                  default: 1024
 
   -m <length>  Maximum password length (beginning and end included).
                  default: 8
 
   -N           Ignore decryption errors (similar to openssl -nopad).
 
   -n           Ignore salt (similar to openssl -nosalt).
 
   -s <string>  Password character set.
                default: "0123456789ABCDEFGHIJKLMNOPQRSTU
                          VWXYZabcdefghijklmnopqrstuvwxyz"
 
   -t <n>       Number of threads to use.
                  default: 1
 
   -v <n>       Print progress info every n seconds.
   -w <file>    Restore the state of a previous session if the file exists,
                then write the state to the file regularly (~ every minute).
 
 Sending a USR1 signal to a running bruteforce-salted-openssl process
 makes it print progress info to standard error and continue.
 
 Error: unknown option: '-'.
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
