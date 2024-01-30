---
Title: shellfire
Homepage: https://github.com/unix-ninja/shellfire
Repository: https://gitlab.com/kalilinux/packages/shellfire
Architectures: all
Version: 0.11-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### shellfire
 
  This package contains an exploitation shell which focuses on exploiting LFI,
  RFI, and command injection vulnerabilities.
 
 **Installed size:** `71 KB`  
 **How to install:** `sudo apt install shellfire`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-requests
 {{< /spoiler >}}
 
 ##### shellfire
 
 
 ```
 root@kali:~# shellfire -h
 usage: shellfire [-h] [-c [CONFIG]] [-d] [--generate PAYLOAD] [--version]
 
 An exploitation shell for command injection vulnerabilities.
 
 options:
   -h, --help          show this help message and exit
   -c [CONFIG]         load a named config on startup.
   -d                  enable debugging (show queries during execution)
   --generate PAYLOAD  generate a payload to stdout. PAYLOAD can be "php" or
                       "aspnet".
   --version           display version and exit.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
