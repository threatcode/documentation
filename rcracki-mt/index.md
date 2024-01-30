---
Title: rcracki-mt
Homepage: https://freerainbowtables.com/
Repository: https://gitlab.com/kalilinux/packages/rcracki-mt
Architectures: any
Version: 0.7.0-1kali4
Metapackages: kali-linux-everything kali-linux-large kali-tools-passwords 
Icon: images/rcracki-mt-logo.svg
PackagesInfo: |
 ### rcracki-mt
 
  rcracki_mt is our modified version of rcrack which supports
  hybrid and indexed tables. In addition to that, it also
  adds multi-core support
 
 **Installed size:** `386 KB`  
 **How to install:** `sudo apt install rcracki-mt`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libgcc-s1 
 * libssl3 
 * libstdc++6 
 {{< /spoiler >}}
 
 ##### rcracki_mt
 
 
 ```
 root@kali:~# rcracki_mt -h
 Using 1 threads for pre-calculation and false alarm checking...
 no rainbow table found
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## rcracki_mt Usage Example

Crack the password hash (`-h 5d41402abc4b2a76b9719d911017c592`) using 4 CPU cores (`-t 4`) and the specified rainbow tables (`tables2/md5/`):

```
root@kali:~# rcracki_mt -h 5d41402abc4b2a76b9719d911017c592 -t 4 tables2/md5/
Using 4 threads for pre-calculation and false alarm checking...
Found 440 rainbowtable files...

md5_mixalpha-numeric-space#1-8_0_60000x27443102_distrrtgen[p][i]_109.rti2:
Chain Position is now 27443102
192101714 bytes read, disk access time: 1.19 s
searching for 1 hash...
cryptanalysis time: 0.26 s
```
