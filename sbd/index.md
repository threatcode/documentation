---
Title: sbd
Homepage: https://mirrors.kernel.org/gentoo/distfiles/sbd-1.37.tar.gz
Repository: https://gitlab.com/kalilinux/packages/sbd
Architectures: any
Version: 1.37-1kali5
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-post-exploitation kali-tools-windows-resources 
Icon: images/sbd-logo.svg
PackagesInfo: |
 ### sbd
 
  sbd is a Netcat-clone, designed to be portable and offer strong encryption. It
  runs on Unix-like operating systems and on Microsoft Win32. sbd features
  AES-CBC-128 + HMAC-SHA1 encryption (by Christophe Devine), program execution
  (-e option), choosing source port, continuous reconnection with delay, and
  some other nice features. sbd supports TCP/IP communication only.
 
 **Installed size:** `163 KB`  
 **How to install:** `sudo apt install sbd`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### sbd
 
 
 ```
 root@kali:~# sbd -h
 sbd 1.37 Copyright (C) 2004 Michel Blomgren <michel.blomgren@tigerteam.se>
 $Id: sbd.c,v 1.37 2005/08/21 22:40:47 shadow Exp $
 
 This program is free software; you can redistribute it and/or modify it under
 the terms of the GNU General Public License as published by the Free Software
 Foundation; either version 2 of the License, or (at your option) any later
 version.
 
 connect (tcp): sbd [-options] host port
 listen (tcp):  sbd -l -p port [-options]
 options:
     -l          listen for incoming connection
     -p n        choose port to listen on, or source port to connect out from
     -a address  choose an address to listen on or connect out from
     -e prog     program to execute after connect (e.g. -e cmd.exe or -e bash)
     -r n        infinitely respawn/reconnect, pause for n seconds between
                 connection attempts. -r0 can be used to re-listen after
                 disconnect (just like a regular daemon)
     -c on|off   encryption on/off. specify whether you want to use the built-in
                 AES-CBC-128 + HMAC-SHA1 encryption implementation (by
                 Christophe Devine - http://www.cr0.net:8040/) or not
                 default is: -c on
     -k secret   override default phrase to use for encryption (secret must be
                 shared between client and server)
     -q          hush, quiet, don't print anything (overrides -v)
     -v          be verbose
     -n          toggle numeric-only IP addresses (don't do DNS resolution). if
                 you specify -n twice, original state will be active (i.e. -n
                 works like a on/off switch)
     -m          toggle monitoring (snooping) on/off (only used with the -e
                 option). snooping can also be turned on by specifying -vv (-v
                 two times)
     -P prefix   add prefix (+ a hardcoded separator) to all outbound data.
                 this option is mostly only useful for sbd in "chat mode" (to
                 prefix lines you send with your nickname)
     -H on|off   highlight incoming data with a hardcoded (color) escape
                 sequence (for e.g. chatting). default is: -H off
     -V          print version banner and exit (include that output in your
                 bug report and send bug report to michel.blomgren@tigerteam.se)
 unix-like OS specific options:
     -s          invoke a shell, nothing else. if sbd is setuid 0, it'll invoke
                 a root shell
     -w n        "immobility timeout" in seconds for idle read/write operations
                 and program execution (the -e option)
     -D on|off   fork and run in background (daemonize). default: -D off
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## sbd Usage Example

On the server, listen for a connection (`-l`) on port 4444 (`-p 4444`), execute bash on connection (`-e bash`) and display verbose output (`-v`) with no name resolution (`-n`).

On the client, connect to the remote server IP address (`192.168.1.202`) and port (`4444`).

```
root@kali:~# sbd -l -p 4444 -e bash -v -n
listening on port 4444
```

```
root@kali:~# sbd 192.168.1.202 4444
id
uid=0(root) gid=0(root) groups=0(root)
```
