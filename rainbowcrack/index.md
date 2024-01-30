---
Title: rainbowcrack
Homepage: https://project-rainbowcrack.com/index.htm
Repository: https://gitlab.com/kalilinux/packages/rainbowcrack
Architectures: amd64
Version: 1.8-0kali2
Metapackages: kali-linux-everything kali-linux-large kali-tools-passwords 
Icon: images/rainbowcrack-logo.svg
PackagesInfo: |
 ### rainbowcrack
 
  RainbowCrack is a general propose implementation of
  Philippe Oechslin's faster time-memory trade-off technique.
  It crack hashes with rainbow tables.
   
  RainbowCrack uses time-memory tradeoff algorithm to crack
  hashes. It differs from the hash crackers that use brute
  force algorithm.
 
 **Installed size:** `497 KB`  
 **How to install:** `sudo apt install rainbowcrack`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libgcc-s1 
 * libstdc++6 
 {{< /spoiler >}}
 
 ##### rcrack
 
 
 ```
 root@kali:~# rcrack -h
 RainbowCrack 1.8
 Copyright 2020 RainbowCrack Project. All rights reserved.
 http://project-rainbowcrack.com/
 
 usage: ./rcrack path [path] [...] -h hash
        ./rcrack path [path] [...] -l hash_list_file
        ./rcrack path [path] [...] -lm pwdump_file
        ./rcrack path [path] [...] -ntlm pwdump_file
 path:              directory where rainbow tables (*.rt, *.rtc) are stored
 -h hash:           load single hash
 -l hash_list_file: load hashes from a file, each hash in a line
 -lm pwdump_file:   load lm hashes from pwdump file
 -ntlm pwdump_file: load ntlm hashes from pwdump file
 
 implemented hash algorithms:
     lm HashLen=8 PlaintextLen=0-7
     ntlm HashLen=16 PlaintextLen=0-15
     md5 HashLen=16 PlaintextLen=0-15
     sha1 HashLen=20 PlaintextLen=0-20
     sha256 HashLen=32 PlaintextLen=0-20
 
 examples:
     ./rcrack . -h 5d41402abc4b2a76b9719d911017c592
     ./rcrack . -l hash.txt
 ```
 
 - - -
 
 ##### rt2rtc
 
 
 ```
 root@kali:~# rt2rtc -h
 no rainbow table found
 ```
 
 - - -
 
 ##### rtc2rt
 
 
 ```
 root@kali:~# rtc2rt -h
 no rainbow table found
 ```
 
 - - -
 
 ##### rtgen
 
 
 ```
 root@kali:~# rtgen -h
 RainbowCrack 1.8
 Copyright 2020 RainbowCrack Project. All rights reserved.
 http://project-rainbowcrack.com/
 
 usage: rtgen hash_algorithm charset plaintext_len_min plaintext_len_max table_index chain_len chain_num part_index
        rtgen hash_algorithm charset plaintext_len_min plaintext_len_max table_index -bench
 
 hash algorithms implemented:
     lm HashLen=8 PlaintextLen=0-7
     ntlm HashLen=16 PlaintextLen=0-15
     md5 HashLen=16 PlaintextLen=0-15
     sha1 HashLen=20 PlaintextLen=0-20
     sha256 HashLen=32 PlaintextLen=0-20
 
 examples:
     rtgen md5 loweralpha 1 7 0 1000 1000 0
     rtgen md5 loweralpha 1 7 0 -bench
 ```
 
 - - -
 
 ##### rtmerge
 
 
 
 - - -
 
 ##### rtsort
 
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
