---
Title: apache-users
Homepage: https://labs.portcullis.co.uk/downloads/
Repository: https://gitlab.com/kalilinux/packages/apache-users
Architectures: any
Version: 2.1-1kali6
Metapackages: kali-linux-everything kali-linux-large kali-tools-web 
Icon: images/apache-users-logo.svg
PackagesInfo: |
 ### apache-users
 
  This Perl script will enumerate the usernames on any
  system that uses Apache with the UserDir module.
 
 **Installed size:** `13 KB`  
 **How to install:** `sudo apt install apache-users`  
 
 {{< spoiler "Dependencies:" >}}
 * libio-all-lwp-perl
 * libio-socket-ip-perl
 * libparallel-forkmanager-perl
 {{< /spoiler >}}
 
 ##### apache-users
 
 
 ```
 root@kali:~# apache-users -h
 
 USAGE: apache-users [-h 1.2.3.4] [-l names] [-p 80] [-s (SSL Support 1=true 0=false)] [-e 403 (http code)] [-t threads]
 
  
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## apache-users Usage Example

Run against the remote host (`-h 192.168.1.202`), passing a dictionary of usernames (`-l /usr/share/wordlists/metasploit/unix_users.txt`), the port to use (`-p 80`), disable SSL (`-s 0`), specify the HTTP error code (`-e 403`), using 10 threads (`-t 10`):

```
root@kali:~# apache-users -h 192.168.1.202 -l /usr/share/wordlists/metasploit/unix_users.txt -p 80 -s 0 -e 403 -t 10
```
