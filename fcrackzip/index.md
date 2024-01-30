---
Title: fcrackzip
Homepage: http://oldhome.schmorp.de/marc/fcrackzip.html
Repository: https://salsa.debian.org/pkg-security-team/fcrackzip
Architectures: any
Version: 1.0-11
Metapackages: kali-linux-everything kali-linux-large kali-tools-forensics kali-tools-passwords kali-tools-respond 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### fcrackzip
 
  fcrackzip is a fast password cracker partly written in assembler. It is
  able to crack password protected zip files with brute force or dictionary
  based attacks, optionally testing with unzip its results. It can also crack
  cpmask'ed images.
   
  This package is useful for pentesters, ethical hackers and forensics
  experts.
 
 **Installed size:** `81 KB`  
 **How to install:** `sudo apt install fcrackzip`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### fcrackzip
 
 A Free/Fast Zip Password Cracker
 
 ```
 root@kali:~# fcrackzip -h
 
 fcrackzip version 1.0, a fast/free zip password cracker
 written by Marc Lehmann <pcg@goof.com> You can find more info on
 http://www.goof.com/pcg/marc/
 
 USAGE: fcrackzip
           [-b|--brute-force]            use brute force algorithm
           [-D|--dictionary]             use a dictionary
           [-B|--benchmark]              execute a small benchmark
           [-c|--charset characterset]   use characters from charset
           [-h|--help]                   show this message
           [--version]                   show the version of this program
           [-V|--validate]               sanity-check the algorithm
           [-v|--verbose]                be more verbose
           [-p|--init-password string]   use string as initial password/file
           [-l|--length min-max]         check password with length min to max
           [-u|--use-unzip]              use unzip to weed out wrong passwords
           [-m|--method num]             use method number "num" (see below)
           [-2|--modulo r/m]             only calculcate 1/m of the password
           file...                    the zipfiles to crack
 
 methods compiled in (* = default):
 
  0: cpmask
  1: zip1
 *2: zip2, USE_MULT_TAB
 
 ```
 
 - - -
 
 ##### fcrackzipinfo
 
 Display zip information
 
 ```
 root@kali:~# fcrackzipinfo --help
 
 fcrackzip version 1.0, zipinfo - tell me about a zip file
 written by Marc Lehmann <pcg@goof.com> You can find more info on
 http://www.goof.com/pcg/marc/
 
 USAGE: zipinfo file...                the zipfiles to parse
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
