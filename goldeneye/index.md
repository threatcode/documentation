---
Title: goldeneye
Homepage: https://github.com/jseidl/GoldenEye
Repository: https://salsa.debian.org/pkg-security-team/goldeneye
Architectures: all
Version: 1.2.0+git20191230-2
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### goldeneye
 
  GoldenEye is a HTTP DoS Test Tool. This tool can be used to test if
  a site is susceptible to Deny of Service (DoS) attacks. Is possible
  to open several parallel connections against a URL to check if the
  web server can be compromised.
   
  The program tests the security in networks and uses 'HTTP Keep Alive
  + NoCache' as attack vector.
   
  This package is useful for pentesters.
 
 **Installed size:** `963 KB`  
 **How to install:** `sudo apt install goldeneye`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 {{< /spoiler >}}
 
 ##### goldeneye
 
 HTTP DoS test tool
 
 ```
 root@kali:~# goldeneye -h
 
 -----------------------------------------------------------------------------------------------------------
 
 GoldenEye v2.1 by Jan Seidl <jseidl@wroot.org>
 
  USAGE: goldeneye <url> [OPTIONS]
 
  OPTIONS:
 	 Flag			Description						Default
 	 -u, --useragents	File with user-agents to use				(default: randomly generated)
 	 -w, --workers		Number of concurrent workers				(default: 10)
 	 -s, --sockets		Number of concurrent sockets				(default: 500)
 	 -m, --method		HTTP Method to use 'get' or 'post'  or 'random'		(default: get)
 	 -n, --nosslcheck	Do not verify SSL Certificate				(default: True)
 	 -d, --debug		Enable Debug Mode [more verbose output]			(default: False)
 	 -h, --help		Shows this help
 
 -----------------------------------------------------------------------------------------------------------
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
