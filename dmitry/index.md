---
Title: dmitry
Homepage: https://mor-pah.net/software/dmitry-deepmagic-information-gathering-tool/
Repository: 
Architectures: any
Version: 1.3a-2
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-information-gathering 
Icon: images/dmitry-logo.svg
PackagesInfo: |
 ### dmitry
 
  DMitry is a UNIX/(GNU)Linux command line application written in C.
  DMitry can find possible subdomains, email addresses, uptime information,
  perform tcp port scan, whois lookups, and more.
 
 **Installed size:** `49 KB`  
 **How to install:** `sudo apt install dmitry`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### dmitry
 
 Deepmagic Information Gathering Tool
 
 ```
 root@kali:~# dmitry -h
 Deepmagic Information Gathering Tool
 "There be some deep magic going on"
 
 Usage: dmitry [-winsepfb] [-t 0-9] [-o %host.txt] host
   -o	 Save output to %host.txt or to file specified by -o file
   -i	 Perform a whois lookup on the IP address of a host
   -w	 Perform a whois lookup on the domain name of a host
   -n	 Retrieve Netcraft.com information on a host
   -s	 Perform a search for possible subdomains
   -e	 Perform a search for possible email addresses
   -p	 Perform a TCP port scan on a host
 * -f	 Perform a TCP port scan on a host showing output reporting filtered ports
 * -b	 Read in the banner received from the scanned port
 * -t 0-9 Set the TTL in seconds when scanning a TCP port ( Default 2 )
 *Requires the -p flagged to be passed
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## Video

<script id="asciicast-31154" src="https://asciinema.org/a/31154.js" async type="text/javascript"></script>

## dmitry Usage Example

Run a domain whois lookup (`w`), an IP whois lookup (`i`), retrieve Netcraft info (`n`), search for subdomains (`s`), search for email addresses (`e`), do a TCP port scan (`p`), and save the output to example.txt (`o`) for the domain `example.com`:

```
root@kali:~# dmitry -winsepo example.txt example.com
Deepmagic Information Gathering Tool
"There be some deep magic going on"

Writing output to 'example.txt'

HostIP:93.184.216.119
HostName:example.com

Gathered Inet-whois information for 93.184.216.119
---------------------------------
```
