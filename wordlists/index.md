---
Title: wordlists
Homepage: https://www.kali.org
Repository: https://gitlab.com/kalilinux/packages/wordlists
Architectures: all
Version: 2023.2.0
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-information-gathering kali-tools-passwords kali-tools-vulnerability 
Icon: images/wordlists-logo.svg
PackagesInfo: |
 ### wordlists
 
  This package contains the rockyou.txt
  wordlist and has an installation size
  of 134 MB.
 
 **Installed size:** `50.90 MB`  
 **How to install:** `sudo apt install wordlists`  
 
 {{< spoiler "Dependencies:" >}}
 * kali-defaults 
 {{< /spoiler >}}
 
 ##### wordlists
 
 
 ```
 root@kali:~# wordlists -h
 
 > wordlists ~ Contains the rockyou wordlist
 
 /usr/share/wordlists
 |-- amass -> /usr/share/amass/wordlists
 |-- brutespray -> /usr/share/brutespray/wordlist
 |-- dirb -> /usr/share/dirb/wordlists
 |-- dirbuster -> /usr/share/dirbuster/wordlists
 |-- dnsmap.txt -> /usr/share/dnsmap/wordlist_TLAs.txt
 |-- fasttrack.txt -> /usr/share/set/src/fasttrack/wordlist.txt
 |-- fern-wifi -> /usr/share/fern-wifi-cracker/extras/wordlists
 |-- john.lst -> /usr/share/john/password.lst
 |-- legion -> /usr/share/legion/wordlists
 |-- metasploit -> /usr/share/metasploit-framework/data/wordlists
 |-- nmap.lst -> /usr/share/nmap/nselib/data/passwords.lst
 |-- rockyou.txt.gz
 |-- seclists -> /usr/share/seclists
 |-- sqlmap.txt -> /usr/share/sqlmap/data/txt/wordlist.txt
 |-- wfuzz -> /usr/share/wfuzz/wordlist
 `-- wifite.txt -> /usr/share/dict/wordlist-probable.txt
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## Wordlists Usage Examples

```
root@kali:~# ls -lh /usr/share/wordlists/
total 51M
lrwxrwxrwx 1 root root  25 Jan  3 13:59 dirb -> /usr/share/dirb/wordlists
lrwxrwxrwx 1 root root  30 Jan  3 13:59 dirbuster -> /usr/share/dirbuster/wordlists
lrwxrwxrwx 1 root root  35 Jan  3 13:59 dnsmap.txt -> /usr/share/dnsmap/wordlist_TLAs.txt
lrwxrwxrwx 1 root root  41 Jan  3 13:59 fasttrack.txt -> /usr/share/set/src/fasttrack/wordlist.txt
lrwxrwxrwx 1 root root  45 Jan  3 13:59 fern-wifi -> /usr/share/fern-wifi-cracker/extras/wordlists
lrwxrwxrwx 1 root root  46 Jan  3 13:59 metasploit -> /usr/share/metasploit-framework/data/wordlists
lrwxrwxrwx 1 root root  41 Jan  3 13:59 nmap.lst -> /usr/share/nmap/nselib/data/passwords.lst
-rw-r--r-- 1 root root 51M Mar  3  2013 rockyou.txt.gz
lrwxrwxrwx 1 root root  34 Jan  3 13:59 sqlmap.txt -> /usr/share/sqlmap/txt/wordlist.txt
lrwxrwxrwx 1 root root  25 Jan  3 13:59 wfuzz -> /usr/share/wfuzz/wordlist
root@kali:~#
root@kali:~# gunzip /usr/share/wordlists/rockyou.txt.gz
root@kali:~#
root@kali:~# wc -l /usr/share/wordlists/rockyou.txt; ls -lah /usr/share/wordlists/rockyou.txt
14344392 /usr/share/wordlists/rockyou.txt
-rw-r--r-- 1 root root 134M Mar  3  2013 /usr/share/wordlists/rockyou.txt
root@kali:~#
```
