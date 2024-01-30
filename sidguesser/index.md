---
Title: sidguesser
Homepage: http://www.cqure.net/wp/tools/database/sidguesser/
Repository: https://gitlab.com/kalilinux/packages/sidguesser
Architectures: any
Version: 1.0.5-1kali2
Metapackages: kali-linux-everything kali-linux-large kali-tools-database kali-tools-web 
Icon: images/sidguesser-logo.svg
PackagesInfo: |
 ### sidguesser
 
  Guesses sids/instances against an Oracle database according
  to a predefined dictionary file. The speed is slow (80-100
  guesses per second) but it does the job.
 
 **Installed size:** `25 KB`  
 **How to install:** `sudo apt install sidguesser`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### sidguess
 
 
 ```
 root@kali:~# sidguess -h
 
 SIDGuesser v1.0.5 by patrik@cqure.net
 -------------------------------------
 sidguess -i <ip> -d <dictionary> [options]
 
 options:
     -p <portnr> Use specific port (default 1521)
     -r <report> Report to file
     -m <mode>   findfirst OR findall(default)
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## sidguess Usage Example

Attack the server (`-i 192.168.1.205`) using a dictionary file (`-d /usr/share/wordlists/metasploit/unix_users.txt`):

```
root@kali:~# sidguess -i 192.168.1.205 -d /usr/share/wordlists/metasploit/unix_users.txt

SIDGuesser v1.0.5 by patrik@cqure.net
-------------------------------------

Starting Dictionary Attack (<space> for stats, Q for quit) ...
```
