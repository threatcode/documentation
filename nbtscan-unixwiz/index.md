---
Title: nbtscan-unixwiz
Homepage: http://unixwiz.net/tools/nbtscan.html
Repository: https://gitlab.com/kalilinux/packages/nbtscan-unixwiz
Architectures: any
Version: 1.0.35-0kali2
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### nbtscan-unixwiz
 
  This package contains a command-line tool that scans for open NETBIOS
  nameservers on a local or remote TCP/IP network, and this is a first step in
  finding of open shares. It is based on the functionality of the standard
  Windows tool nbtstat, but it operates on a range of addresses instead of just
  one.
 
 **Installed size:** `45 KB`  
 **How to install:** `sudo apt install nbtscan-unixwiz`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### nbtscan-unixwiz
 
 
 ```
 root@kali:~# nbtscan-unixwiz -h
 nbtscan-unixwiz: invalid option -- 'h'
 nbtscan 1.0.35 - 2008-04-08 - http://www.unixwiz.net/tools/
 
 usage: nbtscan-unixwiz [options] target [targets...]
 
    Targets are lists of IP addresses, DNS names, or address
    ranges. Ranges can be in /nbits notation ("192.168.12.0/24")
    or with a range in the last octet ("192.168.12.64-97")
 
    -V        show Version information
    -f        show Full NBT resource record responses (recommended)
    -H        generate HTTP headers
    -v        turn on more Verbose debugging
    -n        No looking up inverse names of IP addresses responding
    -p <n>    bind to UDP Port <n> (default=0)
    -m        include MAC address in response (implied by '-f')
    -T <n>    Timeout the no-responses in <n> seconds (default=2 secs)
    -w <n>    Wait <n> msecs after each write (default=10 ms)
    -t <n>    Try each address <n> tries (default=1)
    -P        generate results in perl hashref format
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## Video

<script type="text/javascript" src="https://asciinema.org/a/104243.js" id="asciicast-104243" async></script>

## nbtscan-unixwiz Usage Examples

Scan a range of IP addresses (`192.168.0.100-110`) without doing inverse name lookups (`-n`):

```
root@kali:~# nbtscan-unixwiz -n 192.168.0.100-110
192.168.0.105   WORKGROUP\RETROPIE              SHARING
*timeout (normal end of scan)
```


Scan a single IP address (`192.168.0.38`) and show Full NBT resource record responses (`-f`):

```
root@kali:~# nbtscan-unixwiz -f 192.168.0.38
192.168.0.38    WORKGROUP\DOOKOSSEL             SHARING
  DOOKOSSEL      <00> UNIQUE Workstation Service
  DOOKOSSEL      <03> UNIQUE Messenger Service<3>
  DOOKOSSEL      <20> UNIQUE File Server Service
  ..__MSBROWSE__.<01> GROUP  Master Browser
  WORKGROUP      <00> GROUP  Domain Name
  WORKGROUP      <1d> UNIQUE Master Browser
  WORKGROUP      <1e> GROUP  Browser Service Elections
  00:00:00:00:00:00   ETHER
```
