---
Title: faraday-cli
Homepage: https://github.com/infobyte/faraday-cli
Repository: https://gitlab.com/kalilinux/packages/faraday-cli
Architectures: all
Version: 2.1.8-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### faraday-cli
 
  This package contains the official client that make automating your security
  workflows, easier.
 
 **Installed size:** `220 KB`  
 **How to install:** `sudo apt install faraday-cli`  
 
 {{< spoiler "Dependencies:" >}}
 * faraday
 * python3
 * python3-arrow
 * python3-click
 * python3-cmd2
 * python3-colorama
 * python3-faraday-plugins 
 * python3-jsonschema
 * python3-log-symbols
 * python3-packaging
 * python3-py-sneakers
 * python3-simple-rest-client
 * python3-spinners
 * python3-tabulate
 * python3-termcolor
 * python3-validators 
 * python3-yaml
 {{< /spoiler >}}
 
 ##### faraday-cli
 
 
 ```
 root@kali:~# faraday-cli -h
 usage: faraday-cli [-h] [command] ...
 
 Commands as arguments
 
 positional arguments:
   command       optional command to run, if no command given, enter an
                 interactive shell
   command_args  optional arguments for command
 
 options:
   -h, --help    show this help message and exit
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
