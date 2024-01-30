---
Title: oclgausscrack
Homepage: https://github.com/jsteube/oclGaussCrack
Repository: https://gitlab.com/kalilinux/packages/oclgausscrack
Architectures: i386 amd64
Version: 1.3-1kali3
Metapackages: kali-linux-everything kali-tools-gpu kali-tools-passwords 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### oclgausscrack
 
  The goal of the program is to crack the verification hash of the encrypted
  payload of the Gauss Virus.
   
     Uses OpenCL to accelerate the 10k MD5 loop
     Uses optimizations also used in oclHashcat-plus for maximum performance
     Able to handle multi-GPU setups (of the same type)
     VCL (Virtual CL) v1.18 compatible
     Open Source
     Supports integration into distributed computing environments
     Supports resume
 
 **Installed size:** `125 KB`  
 **How to install:** `sudo apt install oclgausscrack`  
 
 ##### gausscombinator
 
 
 ```
 root@kali:~# gausscombinator -h
 usage: ./gaussCombinator.bin file1 file2
 ```
 
 - - -
 
 ##### gaussfilter
 
 
 
 - - -
 
 ##### oclgausscrack
 
 
 ```
 root@kali:~# oclgausscrack -h
 Loading Kernel...
 Initializing OpenCL...
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

