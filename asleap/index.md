---
Title: asleap
Homepage: https://www.willhackforsushi.com/
Repository: https://gitlab.com/kalilinux/packages/asleap
Architectures: any
Version: 2.3~git20201128.254acab-0kali1
Metapackages: kali-linux-everything kali-linux-large kali-tools-802-11 kali-tools-wireless 
Icon: images/asleap-logo.svg
PackagesInfo: |
 ### asleap
 
  Demonstrates a serious deficiency in proprietary Cisco LEAP networks.
 
 **Installed size:** `230 KB`  
 **How to install:** `sudo apt install asleap`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libpcap0.8 
 {{< /spoiler >}}
 
 ##### asleap
 
 
 ```
 root@kali:~# asleap -h
 asleap 2.3 - actively recover LEAP/PPTP passwords. <jwright@hasborg.com>
 Usage: asleap [options]
 
 	-r 	Read from a libpcap file
 	-i 	Interface to capture on
 	-f 	Dictionary file with NT hashes
 	-n 	Index file for NT hashes
 	-s 	Skip the check to make sure authentication was successful
 	-h 	Output this help information and exit
 	-v 	Print verbose information (more -v for more verbosity)
 	-V 	Print program version and exit
 	-C 	Challenge value in colon-delimited bytes
 	-R 	Response value in colon-delimited bytes
 	-W 	ASCII dictionary file (special purpose)
 
 ```
 
 - - -
 
 ##### genkeys
 
 
 ```
 root@kali:~# genkeys -h
 genkeys 2.3 - generates lookup file for asleap. <jwright@hasborg.com>
 Usage: genkeys [options]
 
 	-r 	Input dictionary file, one word per line
 	-f 	Output pass+hash filename
 	-n 	Output index filename
 	-h 	Last 2 hash bytes to filter with (optional)
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## genkeys Usage Example

Read in a dictionary file (`-r /usr/share/wordlists/nmap.lst)`, provide an output filename (`-f asleap.dat`), and an output index filename (`-n asleap.idx)`:

```
root@kali:~# genkeys -r /usr/share/wordlists/nmap.lst -f asleap.dat -n asleap.idx
genkeys 2.2 - generates lookup file for asleap. <jwright@hasborg.com>
Generating hashes for passwords (this may take some time) ...Done.
5085 hashes written in 0.29 seconds:  17463.18 hashes/second
Starting sort (be patient) ...Done.
Completed sort in 16254 compares.
Creating index file (almost finished) ...Done.
asleap Usage Examples
```

Read a capture file (-r leap.dump), provide the hashfile filename (`-f asleap.dat)`, the hashfile index (`-n asleap.idx`), and skip the authentication check `(-s`):

```
root@kali:~# asleap -r leap.dump -f asleap.dat -n asleap.idx -s
asleap 2.2 - actively recover LEAP/PPTP passwords. <jwright@hasborg.com>

Captured LEAP exchange information:
    username:          qa_leap
    challenge:         0786aea0215bc30a
    response:          7f6a14f11eeb980fda11bf83a142a8744f00683ad5bc5cb6
    hash bytes:        4a39
    NT hash:           a1fc198bdbf5833a56fb40cdd1a64a39
    password:          qaleap
```

Crack a challenge (`-C 58:16:d5:ac:4b:dc:e4:0f`) and response (`-R 50:ae:a3:0a:10:9e:28:f9:33:1b:44:b1:3d:9e:20:91:85:e8:2e:c3:c5:4c:00:23`) from freeradius, using a wordlist (`-W password.lst`):

```
root@kali:~# asleap -C 58:16:d5:ac:4b:dc:e4:0f -R 50:ae:a3:0a:10:9e:28:f9:33:1b:44:b1:3d:9e:20:91:85:e8:2e:c3:c5:4c:00:23 -W password.lst
asleap 2.2 - actively recover LEAP/PPTP passwords. <jwright@hasborg.com>
Using wordlist mode with "password.lst".
    hash bytes:        586c
    NT hash:           8846f7eaee8fb117ad06bdd830b7586c
    password:          password
```
