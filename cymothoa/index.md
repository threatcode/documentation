---
Title: cymothoa
Homepage: https://cymothoa.sourceforge.net/
Repository: https://gitlab.com/kalilinux/packages/cymothoa
Architectures: i386 amd64
Version: 1-beta-1kali3
Metapackages: kali-linux-everything kali-linux-large kali-tools-post-exploitation 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### cymothoa
 
  Cymothoa is a stealth backdooring tool, that inject
  backdoor's shellcode into an existing process. The tool
  uses the ptrace library (available on nearly all * nix), to
  manipulate processes and infect them.
 
 **Installed size:** `90 KB`  
 **How to install:** `sudo apt install cymothoa`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### bgrep
 
 
 
 - - -
 
 ##### cymothoa
 
 
 ```
 root@kali:~# cymothoa -h
                               _                 
                           _  | |                
   ____ _   _ ____   ___ _| |_| |__   ___  _____ 
  / ___) | | |    \ / _ (_   _)  _ \ / _ \(____ |
 ( (___| |_| | | | | |_| || |_| | | | |_| / ___ |
  \____)\__  |_|_|_|\___/  \__)_| |_|\___/\_____|
       (____/  
 Ver.1 (beta) - Runtime shellcode injection, for stealthy backdoors...
 
 By codwizard (codwizard@gmail.com) and crossbower (crossbower@gmail.com)
 from ES-Malaria by ElectronicSouls (http://www.0x4553.org).
 
 Usage:
 	cymothoa -p <pid> -s <shellcode_number> [options]
 
 Main options:
 	-p	process pid
 	-s	shellcode number
 	-l	memory region name for shellcode injection (default /lib/ld)
 	  	search for "r-xp" permissions, see /proc/pid/maps...
 	-m	memory region name for persistent memory (default /lib/ld)
 	  	search for "rw-p" permissions, see /proc/pid/maps...
 	-h	print this help screen
 	-S	list available shellcodes
 
 Injection options (overwrite payload flags):
 	-f	fork parent process
 	-F	don't fork parent process
 	-b	create payload thread (probably you need also -F)
 	-B	don't create payload thread
 	-w	pass persistent memory address
 	-W	don't pass persistent memory address
 	-a	use alarm scheduler
 	-A	don't use alarm scheduler
 	-t	use setitimer scheduler
 	-T	don't use setitimer scheduler
 
 Payload arguments:
 	-j	set timer (seconds)
 	-k	set timer (microseconds)
 	-x	set the IP
 	-y	set the port number
 	-r	set the port number 2
 	-z	set the username (4 bytes)
 	-o	set the password (8 bytes)
 	-c	set the script code (ex: "#!/bin/sh\nls; exit 0")
 	  	escape codes will not be interpreted...
 ```
 
 - - -
 
 ##### udp_server
 
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## bgrep – Binary grep

```
root@kali:~# bgrep
bgrep version: 0.2
usage: bgrep <hex> [<path> [...]]
```

## udp_server – UDP server for Cymothoa

```
root@kali:~# udp_server
usage: udp_server port
```
