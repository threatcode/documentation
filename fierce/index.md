---
Title: fierce
Homepage: https://github.com/mschwager/fierce
Repository: https://salsa.debian.org/pkg-security-team/fierce
Architectures: all
Version: 1.5.0-1
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-information-gathering 
Icon: images/fierce-logo.svg
PackagesInfo: |
 ### fierce
 
  Fierce is a semi-lightweight scanner that helps locate non-contiguous
  IP space and hostnames against specified domains. It's really meant as
  a pre-cursor to nmap, unicornscan, nessus, nikto, etc, since all of
  those require that you already know what IP space you are looking for.
  This does not perform exploitation and does not scan the whole internet
  indiscriminately. It is meant specifically to locate likely targets both
  inside and outside a corporate network.
   
  Because it uses DNS primarily you will often find mis-configured networks
  that leak internal address space. That's especially useful in targeted malware.
  Originally written by RSnake along with others at http://ha.ckers.org/.
  This is simply a conversion to Python 3 to simplify and modernize the codebase.
 
 **Installed size:** `238 KB`  
 **How to install:** `sudo apt install fierce`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-dnspython
 {{< /spoiler >}}
 
 ##### fierce
 
 DNS scanner that helps locate non-contiguous IP space and hostnames against specified domains.
 
 ```
 root@kali:~# fierce -h
 usage: fierce [-h] [--domain DOMAIN] [--connect] [--wide]
               [--traverse TRAVERSE] [--search SEARCH [SEARCH ...]]
               [--range RANGE] [--delay DELAY]
               [--subdomains SUBDOMAINS [SUBDOMAINS ...] | --subdomain-file
               SUBDOMAIN_FILE] [--dns-servers DNS_SERVERS [DNS_SERVERS ...] |
               --dns-file DNS_FILE] [--tcp]
 
         A DNS reconnaissance tool for locating non-contiguous IP space.
         
 
 options:
   -h, --help            show this help message and exit
   --domain DOMAIN       domain name to test
   --connect             attempt HTTP connection to non-RFC 1918 hosts
   --wide                scan entire class c of discovered records
   --traverse TRAVERSE   scan IPs near discovered records, this won't enter adjacent class c's
   --search SEARCH [SEARCH ...]
                         filter on these domains when expanding lookup
   --range RANGE         scan an internal IP range, use cidr notation
   --delay DELAY         time to wait between lookups
   --subdomains SUBDOMAINS [SUBDOMAINS ...]
                         use these subdomains
   --subdomain-file SUBDOMAIN_FILE
                         use subdomains specified in this file (one per line)
   --dns-servers DNS_SERVERS [DNS_SERVERS ...]
                         use these dns servers for reverse lookups
   --dns-file DNS_FILE   use dns servers specified in this file for reverse lookups (one per line)
   --tcp                 use TCP instead of UDP
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## fierce Usage Example

Run a default scan against the target domain (`-dns example.com`):

```
root@kali:~# fierce -dns example.com
DNS Servers for example.com:
    b.iana-servers.net
    a.iana-servers.net

Trying zone transfer first...
    Testing b.iana-servers.net
        Request timed out or transfer not allowed.
    Testing a.iana-servers.net
        Request timed out or transfer not allowed.

Unsuccessful in zone transfer (it was worth a shot)
Okay, trying the good old fashioned way... brute force

Checking for wildcard DNS...
Nope. Good.
Now performing 2280 test(s)...
```
