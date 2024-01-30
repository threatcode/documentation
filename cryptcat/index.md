---
Title: cryptcat
Homepage: http://farm9.com/content/Free_Tools/cryptcat_linux2.tar
Repository: https://gitlab.com/kalilinux/packages/cryptcat
Architectures: any
Version: 20031202-5kali7
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### cryptcat
 
  Cryptcat is a simple Unix utility which reads and writes data across
  network connections, using TCP or UDP protocol while encrypting the
  data being transmitted.
  It is designed to be a reliable "back-end" tool that can be used directly
  or easily driven by other programs and scripts.  At the same time, it is a
  feature-rich network debugging and exploration tool, since it can create
  almost any kind of connection you would need and has several interesting
  built-in capabilities.
 
 **Installed size:** `80 KB`  
 **How to install:** `sudo apt install cryptcat`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libgcc-s1 
 * libstdc++6 
 {{< /spoiler >}}
 
 ##### cryptcat
 
 Twofish encryption enabled version of nc(1)
 
 ```
 root@kali:~# cryptcat -h
 [v1.10]
 connect to somewhere:	nc [-options] hostname port[s] [ports] ... 
 listen for inbound:	nc -l -p port [-options] [hostname] [port]
 options:
 	-g gateway		source-routing hop point[s], up to 8
 	-G num			source-routing pointer: 4, 8, 12, ...
 	-h			this cruft
 	-i secs			delay interval for lines sent, ports scanned
 	-l			listen mode, for inbound connects
 	-n			numeric-only IP addresses, no DNS
 	-o file			hex dump of traffic
 	-p port			local port number
 	-r			randomize local and remote ports
 	-s addr			local source address
 	-u			UDP mode
 	-v			verbose [use twice to be more verbose]
 	-w secs			timeout for connects and final net reads
 	-z			zero-I/O mode [used for scanning]
 port numbers can be individual or ranges: lo-hi [inclusive]
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## cryptcat Usage Example

On the server, listen for a connection (`-l`) on port 4444 (`-p 4444`) and don’t do name resolution (`-n`). Redirect all data to a file (`> dataxfer`). On the client, connect to the remote IP address (`192.168.1.202`) on port 4444 (`4444`) and pipe in the data to be transferred (`< /tmp/juicyinfo)`:

```
root@kali:~# cryptcat -l -p 4444 -n > dataxfer

root@kali:~# cryptcat 192.168.1.202 4444 < /tmp/juicyinfo
```
