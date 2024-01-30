---
Title: ident-user-enum
Homepage: https://pentestmonkey.net/tools/user-enumeration/ident-user-enum
Repository: https://gitlab.com/kalilinux/packages/ident-user-enum
Architectures: all
Version: 1.0-0kali3
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### ident-user-enum
 
  This package is a simple PERL script to query the ident service (113/TCP)
  in order to determine the owner of the process listening on each TCP port of
  a target system.
   
  This can help to prioritise target service during a pentest (you might want
  to attack services running as root first).
  Alternatively, the list of usernames gathered can be used for password
  guessing attacks on other network services.
 
 **Installed size:** `12 KB`  
 **How to install:** `sudo apt install ident-user-enum`  
 
 {{< spoiler "Dependencies:" >}}
 * libio-socket-ip-perl
 * libnet-ident-perl
 * perl
 {{< /spoiler >}}
 
 ##### ident-user-enum
 
 
 ```
 root@kali:~# ident-user-enum -h
 ident-user-enum v1.0 ( http://pentestmonkey.net/tools/ident-user-enum )
 
 Usage: ident-user-enum.pl ip port [ port [ port ... ] ]
 
 Queries the ident service (113/TCP) to determine the OS-level user running 
 the process listening on a given TCP port.  More than one port can be supplied.
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## Video

<script type="text/javascript" src="https://asciinema.org/a/107704.js" id="asciicast-107704" async></script>

## ident-user-enum Usage Examples

Scan the remote host (`192.168.1.13`) and determine which user is running the service on the specified ports (`22 139 445`).

```
root@kali:~# ident-user-enum 192.168.1.13 22 139 445
ident-user-enum v1.0 ( http://pentestmonkey.net/tools/ident-user-enum )

192.168.1.13:22 root
192.168.1.13:139    root
192.168.1.13:445    root
```
