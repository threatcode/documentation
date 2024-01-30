---
Title: dumpsterdiver
Homepage: https://github.com/securing/DumpsterDiver
Repository: https://gitlab.com/kalilinux/packages/dumpsterdiver
Architectures: all
Version: 0~git20200911-0kali2
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### dumpsterdiver
 
  This package contains a tool, which can analyze big volumes of data in search
  of hardcoded secrets like keys (e.g. AWS Access Key, Azure Share Key or SSH
  keys) or passwords. Additionally, it allows creating a simple search rules
  with basic conditions (e.g. report only csv files including at least 10 email
  addresses).
   
  The main idea of this tool is to detect any potential secret leaks.
 
 **Installed size:** `46 KB`  
 **How to install:** `sudo apt install dumpsterdiver`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-colorama
 * python3-passwordmeter
 * python3-termcolor
 {{< /spoiler >}}
 
 ##### DumpsterDiver
 
 
 ```
 root@kali:~# DumpsterDiver -h
 
 
        ___                          __             ___   _                
       / _ \ __ __ __ _   ___   ___ / /_ ___  ____ / _ \ (_)_  __ ___  ____
      / // // // //  ' \ / _ \ (_-</ __// -_)/ __// // // /| |/ // -_)/ __/
     /____/ \_,_//_/_/_// .__//___/\__/ \__//_/  /____//_/ |___/ \__//_/   
                       /_/                                                 
             
                                                        #Coded by @Rzepsky
 
 
 usage: DumpsterDiver.py [-h] -p LOCAL_PATH [-r] [-a] [-s] [-l [0,3]]
                         [-o OUTFILE] [--min-key MIN_KEY] [--max-key MAX_KEY]
                         [--entropy ENTROPY] [--min-pass MIN_PASS]
                         [--max-pass MAX_PASS]
                         [--pass-complex {1,2,3,4,5,6,7,8,9}]
                         [--grep-words GREP_WORDS [GREP_WORDS ...]]
                         [--exclude-files EXCLUDE_FILES [EXCLUDE_FILES ...]]
                         [--bad-expressions BAD_EXPRESSIONS [BAD_EXPRESSIONS ...]]
 
 options:
   -h, --help            show this help message and exit
 
 BASIC USAGE:
   -p LOCAL_PATH         path to the folder containing files to be analyzed
   -r, --remove          when this flag is set, then files which don't contain
                         any secret will be removed.
   -a, --advance         when this flag is set, then all files will be
                         additionally analyzed using rules specified in
                         '~/.dumpsterdiver/rules.yaml' file.
   -s, --secret          when this flag is set, then all files will be
                         additionally analyzed in search of hardcoded
                         passwords.
   -l [0,3], --level [0,3]
                         0 - searches for short (20-40 bytes long) keys, 
                             e.g. AWS Access Key ID. 
                         1 - (default) searches for typical (40-66 bytes long) keys, 
                             e.g. AWS Secret Access Key or Azure Shared Key. 
                         2 - searches for long (66-1800 bytes long) keys, 
                             e.g. SSH private key
                         3 - searches for any key (20-1800 bytes long), 
                             careful as it generates lots of false positives
                         
   -o OUTFILE            output file in JSON format.
 
 CONFIGURATION:
   --min-key MIN_KEY     specifies the minimum key length to be analyzed
                         (default is 20).
   --max-key MAX_KEY     specifies the maximum key length to be analyzed
                         (default is 80).
   --entropy ENTROPY     specifies the edge of high entropy (default is 4.3).
   --min-pass MIN_PASS   specifies the minimum password length to be analyzed
                         (default is 8). Requires adding '-s' flag to the
                         syntax.
   --max-pass MAX_PASS   specifies the maximum password length to be analyzed
                         (default is 12). Requires adding '-s' flag to the
                         syntax.
   --pass-complex {1,2,3,4,5,6,7,8,9}
                         specifies the edge of password complexity between 1
                         (trivial passwords) to 9 (very complex passwords)
                         (default is 8). Requires adding '-s' flag to the
                         syntax.
   --grep-words GREP_WORDS [GREP_WORDS ...]
                         specifies the grep words to look for. Multiple words
                         should be separated by space. Wildcards are supported.
                         Requires adding '-a' flag to the syntax.
   --exclude-files EXCLUDE_FILES [EXCLUDE_FILES ...]
                         specifies file names or extensions which shouldn't be
                         analyzed. File extension should contain '.' character
                         (e.g. '.pdf'). Multiple file names and extensions
                         should be separated by space.
   --bad-expressions BAD_EXPRESSIONS [BAD_EXPRESSIONS ...]
                         specifies bad expressions - if the DumpsterDiver find
                         such expression in a file, then this file won't be
                         analyzed. Multiple bad expressions should be separated
                         by space.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
