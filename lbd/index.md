---
Title: lbd
Homepage: http://ge.mine.nu/code/
Repository: https://gitlab.com/kalilinux/packages/lbd
Architectures: all
Version: 0.4-1kali3
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-information-gathering kali-tools-web 
Icon: images/lbd-logo.svg
PackagesInfo: |
 ### lbd
 
  Checks if a given domain uses load-balancing.
 
 **Installed size:** `15 KB`  
 **How to install:** `sudo apt install lbd`  
 
 ##### lbd
 
 
 ```
 root@kali:~# lbd -h
 host: illegal option -- h
 Usage: host [-aCdilrTvVw] [-c class] [-N ndots] [-t type] [-W time]
             [-R number] [-m flag] [-p port] hostname [server]
        -a is equivalent to -v -t ANY
        -A is like -a but omits RRSIG, NSEC, NSEC3
        -c specifies query class for non-IN data
        -C compares SOA records on authoritative nameservers
        -d is equivalent to -v
        -l lists all hosts in a domain, using AXFR
        -m set memory debugging flag (trace|record|usage)
        -N changes the number of dots allowed before root lookup is done
        -p specifies the port on the server to query
        -r disables recursive processing
        -R specifies number of retries for UDP packets
        -s a SERVFAIL response should stop query
        -t specifies the query type
        -T enables TCP/IP mode
        -U enables UDP mode
        -v enables verbose output
        -V print version number and exit
        -w specifies to wait forever for a reply
        -W specifies how long to wait for a reply
        -4 use IPv4 query transport only
        -6 use IPv6 query transport only
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## Video

<script id="asciicast-32257" src="https://asciinema.org/a/32257.js" async type="text/javascript"></script>

## lbd Usage Example

Test to see if the target domain (`example.com`) is using a load balancer:

```
root@kali:~# lbd example.com

lbd - load balancing detector 0.1 - Checks if a given domain uses load-balancing.
Written by Stefan Behte (http://ge.mine.nu)
Proof-of-concept! Might give false positives.

Checking for DNS-Loadbalancing: NOT FOUND
Checking for HTTP-Loadbalancing [Server]:
ECS (sea/55ED)
ECS (sea/1C15)
FOUND
```
