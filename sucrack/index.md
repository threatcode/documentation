---
Title: sucrack
Homepage: https://labs.portcullis.co.uk/tools/sucrack/
Repository: https://salsa.debian.org/pkg-security-team/sucrack
Architectures: any
Version: 1.2.3-6
Metapackages: kali-linux-everything kali-linux-large kali-tools-passwords 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### sucrack
 
  sucrack is a multithreaded Linux/UNIX tool for cracking local
  user accounts via wordlist bruteforcing su. This tool comes in
  handy when you've gained access to a low-privilege user account
  but are allowed to su to other users. Many su implementations
  require a pseudo terminal to be attached in order to take the
  password from the user. This can't be easily achieved with a
  simple shell script. This tool, written in C, is highly
  efficient and can attempt multiple logins at the same time.
 
 **Installed size:** `50 KB`  
 **How to install:** `sudo apt install sucrack`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### sucrack
 
 Is a multithreaded Linux/UNIX tool for brute-force cracking of local user accounts via su.
 
 ```
 root@kali:~# sucrack -h
 yah, very funny!
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
