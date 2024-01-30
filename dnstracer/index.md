---
Title: dnstracer
Homepage: http://www.mavetju.org/unix/dnstracer.php
Repository: https://salsa.debian.org/creekorful/dnstracer
Architectures: any
Version: 1.9-7
Metapackages: kali-linux-everything kali-linux-large kali-tools-information-gathering 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### dnstracer
 
  dnstracer determines where a given Domain Name Server (DNS) gets its
  information from for a given hostname, and follows the chain of DNS
  servers back to the authoritative answer.
 
 **Installed size:** `61 KB`  
 **How to install:** `sudo apt install dnstracer`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### dnstracer
 
 Trace a chain of DNS servers to the source
 
 ```
 root@kali:~# dnstracer -h
 dnstracer: invalid option -- 'h'
 DNSTRACER version 1.8.1 - (c) Edwin Groothuis - http://www.mavetju.org
 Usage: dnstracer [options] [host]
 	-c: disable local caching, default enabled
 	-C: enable negative caching, default disabled
 	-o: enable overview of received answers, default disabled
 	-q <querytype>: query-type to use for the DNS requests, default A
 	-r <retries>: amount of retries for DNS requests, default 3
 	-s <server>: use this server for the initial request, default localhost
 	             If . is specified, A.ROOT-SERVERS.NET will be used.
 	-t <maximum timeout>: Limit time to wait per try
 	-v: verbose
 	-S <ip address>: use this source address.
 	-4: don't query IPv6 servers
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## dnstracer Usage Example

Scan a domain (`example.com`), retry up to 3 times (`-r 3`), and display verbose output (`-v`):

```
root@kali:~# dnstracer -r 3 -v example.com
Tracing to example.com[a] via 192.168.1.1, maximum of 3 retries
192.168.1.1 (192.168.1.1) IP HEADER
- Destination address:  192.168.1.1
DNS HEADER (send)
```
