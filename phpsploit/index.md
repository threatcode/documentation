---
Title: phpsploit
Homepage: https://github.com/nil0x42/phpsploit
Repository: https://gitlab.com/kalilinux/packages/phpsploit
Architectures: all
Version: 3.2+git20230725.c132bd9-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### phpsploit
 
  This package contains a remote control framework, aiming to provide a stealth
  interactive shell-like connection over HTTP between client and web server. It
  is a post-exploitation tool capable to maintain access to a compromised web
  server for privilege escalation purposes.
 
 **Installed size:** `877 KB`  
 **How to install:** `sudo apt install phpsploit`  
 
 {{< spoiler "Dependencies:" >}}
 * php
 * python3
 * python3-extproxy
 * python3-phpserialize
 * python3-pygments
 * python3-pyparsing
 * python3-socks
 {{< /spoiler >}}
 
 ##### phpsploit
 
 (unknown subject)
 
 ```
 root@kali:~# phpsploit -h
 usage: phpsploit [-h] [-v] [-c <FILE>] [-l <SESSION>] [-t <URL>] [-s <FILE>]
                  [-e <CMD>] [-i]
 
 The stealth post-exploitation framework
 
 options:
   -h, --help                      show this help message and exit
   -v, --version                   output version information and exit
   -c <FILE>, --config <FILE>      use alternative configuration file
   -l <SESSION>, --load <SESSION>  load session file
   -t <URL>, --target <URL>        set remote TARGET URL
   -s <FILE>, --source <FILE>      run commands from file (disables interactive
                                   mode)
   -e <CMD>, --eval <CMD>          run phpsploit command (disables interactive
                                   mode)
   -i, --interactive               force interactive mode if unset by `-e` or
                                   `-s`
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
