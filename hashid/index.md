---
Title: hashid
Homepage: https://psypanda.github.io/hashID/
Repository: https://salsa.debian.org/pkg-security-team/hashid
Architectures: all
Version: 3.1.4-4
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-passwords 
Icon: images/hashid-logo.svg
PackagesInfo: |
 ### hashid
 
  Identify the different types of hashes used to encrypt data and especially
  passwords.
   
  hashID is a tool written in Python 3.x which supports the identification of
  over 175 unique hash types using regular expressions.
  It is able to identify a single hash or parse a file and identify the hashes
  within it.
  There is also a nodejs version of hashID available which is easily set up to
  provide online hash identification.
 
 **Installed size:** `84 KB`  
 **How to install:** `sudo apt install hashid`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 {{< /spoiler >}}
 
 ##### hashid
 
 Identify the different types of hashes used to encrypt data
 
 ```
 root@kali:~# hashid -h
 usage: hashid.py [-h] [-e] [-m] [-j] [-o FILE] [--version] INPUT
 
 Identify the different types of hashes used to encrypt data
 
 positional arguments:
   INPUT                    input to analyze (default: STDIN)
 
 options:
   -e, --extended           list all possible hash algorithms including salted
                            passwords
   -m, --mode               show corresponding Hashcat mode in output
   -j, --john               show corresponding JohnTheRipper format in output
   -o FILE, --outfile FILE  write output to file
   -h, --help               show this help message and exit
   --version                show program's version number and exit
 
 License GPLv3+: GNU GPL version 3 or later <http://gnu.org/licenses/gpl.html>
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
