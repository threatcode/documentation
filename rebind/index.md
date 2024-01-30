---
Title: rebind
Homepage: 
Repository: https://gitlab.com/kalilinux/packages/rebind
Architectures: any
Version: 0.3.4-1kali7
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-sniffing-spoofing 
Icon: images/rebind-logo.svg
PackagesInfo: |
 ### rebind
 
  Rebind is a tool that implements the multiple A record DNS
  rebinding attack. Although this tool was originally written
  to target home routers, it can be used to target any public
  (non RFC1918) IP address.
   
  Rebind provides an external attacker access to a target
  router's internal Web interface. This tool works on routers
  that implement the weak end system model in their IP stack,
  have specifically configured firewall rules, and who bind
  their Web service to the router's WAN interface. Note that
  remote administration does not need to be enabled for this
  attack to work. All that is required is that a user inside
  the target network surf to a Web site that is controlled,
  or has been compromised, by the attacker.
 
 **Installed size:** `2.60 MB`  
 **How to install:** `sudo apt install rebind`  
 
 ##### dns-rebind
 
 
 ```
 root@kali:~# dns-rebind -h
 
 Rebind v0.3.4
 
 Usage: dns-rebind [OPTIONS]
 
 	-i <interface>	Specify the network interface to bind to
 	-d <fqdn>     	Specify your registered domain name
 	-u <user>     	Specify the Basic Authentication user name [admin]
 	-a <pass>     	Specify the Basic Authentication password [admin]
 	-r <path>     	Specify the initial URL request path [/]
 	-t <ip>       	Specify a comma separated list of target IP addresses [client IP]
 	-n <time>     	Specify the callback interval in milliseconds [2000]
 	-p <port>     	Specify the target port [80]
 	-c <port>     	Specify the callback port [81]
 	-C <value>    	Specify a cookie to set for the client
 	-H <file>     	Specify a file of HTTP headers for the client to send to the target
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## rebind Usage Example

Use interface eth0 (`-i eth0`) to conduct the rebind attack with the specified domain (`-d kali.local`):

```
root@kali:~# rebind -i eth0 -d kali.local

[+] Starting DNS server on port 53
[+] Starting attack Web server on port 80
[+] Starting callback Web server on port 81
[+] Starting proxy server on 192.168.1.202:664
[+] Services started and running!

> dns
[+] 192.168.1.202       kali.local.
[+] 192.168.1.202       www.kali.local.
[+] 192.168.1.202       ns1.kali.local.
[+] 192.168.1.202       ns2.kali.local.
```
