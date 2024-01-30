---
Title: webacoo
Homepage: https://github.com/anestisb/WeBaCoo
Repository: https://gitlab.com/kalilinux/packages/webacoo
Architectures: all
Version: 0.2.3-1kali3
Metapackages: kali-linux-everything kali-linux-large kali-tools-post-exploitation kali-tools-web 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### webacoo
 
  Scripts for creating Web backdoors using cookies, with module support
 
 **Installed size:** `65 KB`  
 **How to install:** `sudo apt install webacoo`  
 
 {{< spoiler "Dependencies:" >}}
 * libio-socket-socks-perl
 * liburi-perl
 * perl
 {{< /spoiler >}}
 
 ##### webacoo
 
 
 ```
 root@kali:~# webacoo -h
 
 	WeBaCoo 0.2.3 - Web Backdoor Cookie Script-Kit
 	Copyright (C) 2011-2012 Anestis Bechtsoudis
 	{ @anestisb | anestis@bechtsoudis.com | http(s)://bechtsoudis.com }
 
 
 Usage: webacoo [options]
 
 Options:
   -g		Generate backdoor code (-o is required)
 
   -f FUNCTION	PHP System function to use
 	FUNCTION
 		1: system 	(default)
 		2: shell_exec
 		3: exec
 		4: passthru
 		5: popen
 
   -o OUTPUT	Generated backdoor output filename
 
   -r 		Return un-obfuscated backdoor code
 
   -t		Establish remote "terminal" connection (-u is required)
 
   -u URL	Backdoor URL
 
   -e CMD	Single command execution mode (-t and -u are required)
 
   -m METHOD	HTTP method to be used (default is GET)
 
   -c C_NAME	Cookie name (default: "M-cookie")
 
   -d DELIM	Delimiter (default: New random for each request)
 
   -a AGENT	HTTP header user-agent (default exist)
 
   -p PROXY	Use proxy (tor, ip:port or user:pass:ip:port)
 
   -v LEVEL	Verbose level
 	LEVEL
 		0: no additional info (default)
 		1: print HTTP headers
 		2: print HTTP headers + data
 
   -l LOG	Log activity to file
 
   -h		Display help and exit
 
   update	Check for updates and apply if any
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
