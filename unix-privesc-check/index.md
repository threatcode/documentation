---
Title: unix-privesc-check
Homepage: http://pentestmonkey.net/tools/audit/unix-privesc-check
Repository: https://gitlab.com/kalilinux/packages/unix-privesc-check
Architectures: all
Version: 1.4-0kali1
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-vulnerability 
Icon: images/unix-privesc-check-logo.svg
PackagesInfo: |
 ### unix-privesc-check
 
  Unix-privesc-checker is a script that runs on Unix systems
  (tested on Solaris 9, HPUX 11, Various Linuxes, FreeBSD 6.2).
  It tries to find misconfigurations that could allow local
  unprivileged users to escalate privileges to other users or
  to access local apps (e.g. databases).
   
  It is written as a single shell script so it can be easily
  uploaded and run (as opposed to un-tarred, compiled and
  installed). It can run either as a normal user or as root
  (obviously it does a better job when running as root because
  it can read more files).
 
 **Installed size:** `85 KB`  
 **How to install:** `sudo apt install unix-privesc-check`  
 
 ##### unix-privesc-check
 
 
 ```
 root@kali:~# unix-privesc-check -h
 unix-privesc-check v1.4 ( http://pentestmonkey.net/tools/unix-privesc-check )
 
 Usage: unix-privesc-check { standard | detailed }
 
 "standard" mode: Speed-optimised check of lots of security settings.
 
 "detailed" mode: Same as standard mode, but also checks perms of open file
                  handles and called files (e.g. parsed from shell scripts,
                  linked .so files).  This mode is slow and prone to false 
                  positives but might help you find more subtle flaws in 3rd
                  party programs.
 
 This script checks file permissions and other settings that could allow
 local users to escalate privileges.
 
 Use of this script is only permitted on systems which you have been granted
 legal permission to perform a security assessment of.  Apart from this 
 condition the GPL v2 applies.
 
 Search the output for the word 'WARNING'.  If you don't see it then this
 script didn't find any problems.
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## unix-privesc-check Usage Example

```
root@kali:~# unix-privesc-check standard
Assuming the OS is: linux
Starting unix-privesc-check v1.4 ( http://pentestmonkey.net/tools/unix-privesc-check )

This script checks file permissions and other settings that could allow
local users to escalate privileges.

Use of this script is only permitted on systems which you have been granted
legal permission to perform a security assessment of.  Apart from this
condition the GPL v2 applies.

Search the output below for the word 'WARNING'.  If you don't see it then
this script didn't find any problems.


############################################
Recording hostname
############################################
kali

############################################
Recording uname
############################################
Linux kali 3.12-kali1-amd64 #1 SMP Debian 3.12.9-1kali1 (2014-05-13) x86_64 GNU/Linux

############################################
Recording Interface IP addresses
```
