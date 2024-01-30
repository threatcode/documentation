---
Title: rarcrack
Homepage: http://rarcrack.sourceforge.net/
Repository: 
Architectures: any
Version: 0.2-1.1
Metapackages: kali-linux-everything kali-tools-passwords 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### rarcrack
 
  This program uses a brute force algorithm to guess your encrypted compressed
  file's password.
   
  This program can crack zip,7z and rar file passwords.
 
 **Installed size:** `51 KB`  
 **How to install:** `sudo apt install rarcrack`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libxml2 
 {{< /spoiler >}}
 
 ##### rarcrack
 
 
 ```
 root@kali:~# rarcrack --help
 RarCrack! 0.2 by David Zoltan Kedves (kedazo@gmail.com)
 
 Usage:   rarcrack encrypted_archive.ext [--threads NUM] [--type rar|zip|7z]
 
 Options: --help: show this screen.
          --type: you can specify the archive program, this needed when
                  the program couldn't detect the proper file type
          --threads: you can specify how many threads
                     will be run, maximum 12 (default: 2)
 
 Info:    This program supports only RAR, ZIP and 7Z encrypted archives.
          RarCrack! usually detects the archive type.
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
