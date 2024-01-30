---
Title: wordlistraider
Homepage: https://github.com/GregorBiswanger/WordlistRaider
Repository: https://gitlab.com/kalilinux/packages/wordlistraider
Architectures: all
Version: 1.0~git20200927-0kali2
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### wordlistraider
 
  This package contains a Python tool for preparing existing wordlists. It
  returns a selection of words that matches the passed conditions in an existing
  list.
  As an example you have a GB big wordlist and you only want passwords with a
  length of at least 8 characters. This optimizes word lists and saves
  unnecessary requests.
 
 **Installed size:** `30 KB`  
 **How to install:** `sudo apt install wordlistraider`  
 
 {{< spoiler "Dependencies:" >}}
 * figlet
 * python3
 * python3-colorama
 * python3-more-termcolor
 * python3-pyfiglet
 {{< /spoiler >}}
 
 ##### wordlistraider
 
 
 ```
 root@kali:~# wordlistraider -h
 __        __            _ _ _     _   ____       _     _           _ 
 \ \      / /__  _ __ __| | (_)___| |_|  _ \ __ _(_) __| | ___ _ __| |
  \ \ /\ / / _ \| '__/ _` | | / __| __| |_) / _` | |/ _` |/ _ \ '__| |
   \ V  V / (_) | | | (_| | | \__ \ |_|  _ < (_| | | (_| |  __/ |  |_|
    \_/\_/ \___/|_|  \__,_|_|_|___/\__|_| \_\__,_|_|\__,_|\___|_|  (_)
                                                                      
 
 Coded by Gregor Biswanger, Jürgen Gutsch & Community - Version 1.0
 usage: wordlistraider [-h] -w path to source file -t path to the target file
                       [--min MIN] [--max MAX] [-n NUMBERS]
                       [-s SPECIALCHARACTERS]
 
 Returns a selection of words that matches the passed conditions in an existing
 list.
 
 options:
   -h, --help            show this help message and exit
   -w path to source file, --wordlist path to source file
                         the wordlist to raid
   -t path to the target file, --target path to the target file
                         the target wordlist
   --min MIN, --minlength MIN
                         minimum length of password (default: 8)
   --max MAX, --maxlength MAX
                         maximum length of password
   -n NUMBERS, --numbers NUMBERS
                         password must include numbers (default: false)
   -s SPECIALCHARACTERS, --specialcharacters SPECIALCHARACTERS
                         includes passwords with special characters (default:
                         false)
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
