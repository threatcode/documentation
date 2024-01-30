---
Title: oscanner
Homepage: http://www.cqure.net/wp/tools/database/oscanner/
Repository: https://gitlab.com/kalilinux/packages/oscanner
Architectures: all
Version: 1.0.6-1kali3
Metapackages: kali-linux-everything kali-linux-large kali-tools-database kali-tools-web 
Icon: images/oscanner-logo.svg
PackagesInfo: |
 ### oscanner
 
  Oscanner is an Oracle assessment framework developed in Java.
  It has a plugin-based architecture and comes with a couple
  of plugins that currently do:
   
  - Sid Enumeration
  - Passwords tests (common & dictionary)
  - Enumerate Oracle version
  - Enumerate account roles
  - Enumerate account privileges
  - Enumerate account hashes
  - Enumerate audit information
  - Enumerate password policies
  - Enumerate database links
   
  The results are given in a graphical java tree.
 
 **Installed size:** `1.46 MB`  
 **How to install:** `sudo apt install oscanner`  
 
 {{< spoiler "Dependencies:" >}}
 * default-jre
 {{< /spoiler >}}
 
 ##### oscanner
 
 
 ```
 root@kali:~# oscanner -h
 	Oracle Scanner 1.0.6 by patrik@cqure.net
 	--------------------------------------
 	OracleScanner -s <ip> -r <repfile> [options]
 		-s	<servername>
 		-f	<serverlist>
 		-P	<portnr>
 		-v	be verbose
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## oscanner Usage Example

Scan the target server (`-s 192.168.1.15`) on port 1040 (`-P 1040`):

```
root@kali:~# oscanner -s 192.168.1.15 -P 1040
Oracle Scanner 1.0.6 by patrik@cqure.net
--------------------------------------------------
[-] Checking host 192.168.1.15
[x] Failed to enumerate sids from host
[-] Loading services/sids from service file
```
