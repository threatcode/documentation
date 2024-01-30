---
Title: dnsmap
Homepage: https://github.com/resurrecting-open-source-projects/dnsmap
Repository: https://salsa.debian.org/pkg-security-team/dnsmap
Architectures: any
Version: 0.36-3
Metapackages: kali-linux-default kali-linux-everything kali-linux-large kali-tools-information-gathering kali-tools-vulnerability 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### dnsmap
 
  dnsmap scans a domain for common subdomains using a built-in or an external
  wordlist (if specified using -w option). The internal wordlist has around 1000
  words in English and Spanish as ns1, firewall servicios and smtp. So will be
  possible search for smtp.example.com inside example.com automatically. Results
  can be saved in CSV and human-readable format for further processing. dnsmap
  does NOT require root privileges to be run, and should NOT be run with such
  privileges for security reasons.
   
  dnsmap was originally released back in 2006 and was inspired by the fictional
  story "The Thief No One Saw" by Paul Craig, which can be found in the book
  "Stealing the Network - How to 0wn the Box".
   
  dnsmap is mainly meant to be used by pentesters during the information
  gathering/enumeration phase of infrastructure security assessments. During the
  enumeration stage, the security consultant would typically discover the target
  company's IP netblocks, domain names, phone numbers, etc.
   
  Subdomain brute-forcing is another technique that should be used in the
  enumeration stage, as it's especially useful when other domain enumeration
  techniques such as zone transfers don't work (I rarely see zone transfers being
  publicly allowed these days by the way).
   
  Fun things that can happen:
   
    1) Finding interesting remote access servers
       (e.g.: https:://extranet.example.com).
    2) Finding badly configured and/or unpatched servers
       (e.g.: test.example.com).
    3) Finding new domain names which will allow you to map
       non-obvious/hard-to-find netblocks of your target organization
       (registry lookups - aka whois is your friend).
    4) Sometimes you find that some bruteforced subdomains resolve to internal IP
       addresses (RFC 1918). This is great as sometimes they are real up-to-date
       "A" records which means that it is possible to enumerate internal servers
       of a target organization from the Internet by only using standard DNS
       resolving (as opposed to zone transfers for instance).
    5) Discover embedded devices configured using Dynamic DNS services
       (e.g.: IP Cameras). This method is an alternative to finding devices via
       Google hacking techniques.
   
  This package provides two possible commands: dnsmap and dnsmap-bulk.
   
  This program is useful for pentesters, ethical hackers and forensics experts.
  It also can be used for security tests.
 
 **Installed size:** `256 KB`  
 **How to install:** `sudo apt install dnsmap`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### dnsmap
 
 Scan for subdomains using bruteforcing techniques
 
 ```
 root@kali:~# man dnsmap
 dnsmap(1)      scan for subdomains using bruteforcing techniques     dnsmap(1)
 
 NAME
        dnsmap - scan for subdomains using bruteforcing techniques
 
 SYNOPSIS
        dnsmap <target-domain> [options]
 
 DESCRIPTION
        dnsmap  scans a domain for common subdomains using a built-in or an ex-
        ternal wordlist (if specified with -w option).  The  internal  wordlist
        has  around  1000 words in English and Spanish as ns1, firewall, servi-
        cios and smtp. So will be possible search for  smtp.example.com  inside
        example.com automatically.  Results can be saved in CSV and human-read-
        able format for further processing. dnsmap does NOT require root privi-
        leges  to  be run, and should NOT be run with such privileges for secu-
        rity reasons.
 
        dnsmap was originally released back in 2006 and  was  inspired  by  the
        fictional  story  "The  Thief  No  One Saw" by Paul Craig, which can be
        found in the book "Stealing the Network - How to 0wn the Box".
 
        dnsmap is mainly meant to be used by pentesters during the  information
        gathering/enumeration  phase  of  infrastructure  security assessments.
        During the enumeration stage, the security consultant  would  typically
        discover  the  target  company's IP netblocks, domain names, phone num-
        bers, etc.
 
        Subdomain bruteforcing is another technique that should be used in  the
        enumeration stage, as it's especially useful when other domain enumera-
        tion  techniques such as zone transfers don't work (is rare to see zone
        transfers being publicly allowed these days by the way).
 
        Fun things that can happen:
 
               1.  Finding interesting remote access servers (e.g.: https://ex-
                   tranet.example.com).
 
               2.  Finding badly configured  and/or  unpatched  servers  (e.g.:
                   test.example.com).
 
               3.  Finding new domain names which will allow you to map non-ob-
                   vious/hard-to-find  netblocks  of  your  target organization
                   (registry lookups - aka whois is your friend).
 
               4.  Sometimes you find that some bruteforced subdomains  resolve
                   to internal IP addresses (RFC 1918).  This is great as some-
                   times  they are real up-to-date "A" records which means that
                   it *is* possible to enumerate internal servers of  a  target
                   organization  from  the  Internet by only using standard DNS
                   resolving (as opposed to zone transfers for instance).
 
               5.  Discover embedded devices configured using Dynamic DNS  ser-
                   vices  (e.g.:  IP Cameras). This method is an alternative to
                   finding devices via Google hacking techniques.
 
 OPTIONS
        -w <wordlist-file>
               Use an external wordlist instead of the built-in  one.  You  can
               use   programs  as  crunch  or  cupp  to  generate  personalized
               wordlists.
 
        -r <regular-results-file>
               Save results to a plain text file. If a  file  name  isn't  sup-
               plied,  dnsmap will create an unique filename which includes the
               current          timestamp.          e.g.:          dnsmap_exam-
               ple_com_br_2019_11_15_214812.txt.  So,  you can provide a direc-
               tory name only, as -r /tmp.
 
        -c <csv-results-file>
               Save results in CSV format in a file. If a file name isn't  pro-
               vided,    dnsmap   will   create   something   as   dnsmap_exam-
               ple_com_br_2019_11_15_220114.csv. This is  a  similar  behaviour
               from -r option.
 
        -d <delay-millisecs>
               Limit   of  random  delay  in  milliseconds  between  successive
               queries. Delay value is a maximum random value. e.g. if you  en-
               ter 1000, each DNS request will be delayed a *maximum* of 1 sec-
               ond. By default, dnsmap uses a value of 10 milliseconds of maxi-
               mum  delay  between DNS lookups. It is recommended to use the -d
               (delay in milliseconds) option in cases where dnsmap  is  inter-
               fering  with  your  online  experience. i.e.: killing your band-
               width. If used, delay must be between 1 and 300000  milliseconds
               (5 minutes).
 
        -i <ips-to-ignore>
               IP addresses to ignore in the results (useful if you get obtain-
               ing  false positives). Use commas without spaces to separate the
               IP addresses. The maximum number of IPs to filter is 5. Example:
               203.0.113.10,198.51.199.65
 
 INTERNAL WORDLIST
        The built-in wordlist is defined in src/dnsmap.h file. If  needed,  see
        the file to know all words.
 
 EXAMPLES
        Subdomain bruteforcing using dnsmap's built-in wordlist:
 
            $ dnsmap example.com
 
        Subdomain bruteforcing using a user-supplied wordlist:
 
            $ dnsmap example.com -w wordlist.txt
 
        Subdomain  bruteforcing  using the built-in wordlist and saving the re-
        sults to /tmp/ :
 
            $ dnsmap example.com -r /tmp
 
        Example of subdomain bruteforcing using the built-in  wordlist,  saving
        the  results to /tmp/, and waiting a random maximum of 300 milliseconds
        between each request:
 
            $ dnsmap example.com -r /tmp/ -d 300
 
        Subdomain bruteforcing with 0.8 seconds delay, saving results in  regu-
        lar  and CSV format, filtering 2 user-provided IP and using a user-sup-
        plied wordlist:
 
            $ dnsmap example.com -d 800 -r /tmp/ -c /tmp/ -i 10.55.206.154,10.55.24.100 -w ./wordlist_TLAs.txt
 
 BUGS
        Currently, dnsmap does not yet support parallel scanning and hence take
        quite a long time.
 
        New bugs should be  reported  at  https://github.com/resurrecting-open-
        source-projects/dnsmap/issues
 
 SEE ALSO
        crunch(1), cupp(1), dnsmap-bulk(1)
 
 AUTHOR
        dnsmap  was  originally  written  by  "pagvac" in 2006. Currently it is
        maintained    by    volunteers,    inside    dnsmap     project,     at
        https://github.com/resurrecting-open-source-projects/dnsmap/
 
        This manpage was written by Joao Eriberto Mota Filho.
 
 dnsmap-0.36                       25 Feb 2021                        dnsmap(1)
 ```
 
 - - -
 
 ##### dnsmap-bulk
 
 Mass scan using dnsmap
 
 ```
 root@kali:~# man dnsmap-bulk
 dnsmap-bulk(1)              mass scan using dnsmap              dnsmap-bulk(1)
 
 NAME
        dnsmap-bulk - mass scan using dnsmap
 
 SYNOPSIS
        dnsmap-bulk <domains-file> [results-path]
 
 DESCRIPTION
        dnsmap-bulk  is used to bruteforce several target domains in bulk fash-
        ion. In other words, is possible get a list of domains from a  file  to
        scan multiple targets using dnsmap as backend.
 
        WARNING: using dnsmap-bulk, dnsmap will always use the default options,
        i.e. built-in wordlist, delay = 10 ms, never ignoring IPs.
 
 OPTIONS
        domain-file
               A file with domains to be scanned, one per line.
 
        results-path
               A  path  where the results will be saved. dnsmap will use the -r
               option to name files and will be created a file for each domain.
               This item is optional and if not supplied, dnsmap  won't  create
               files.
 
 EXAMPLE
        For bruteforcing a list of target domains in a bulk fashion, saving all
        results inside a directory:
 
            $ dnsmap-bulk domains.txt /tmp/results/
 
 SEE ALSO
        dnsmap(1)
 
 AUTHOR
        dnsmap-bulk was originally written by "pagvac" in 2006. Currently it is
        maintained     by     volunteers,    inside    dnsmap    project,    at
        https://github.com/resurrecting-open-source-projects/dnsmap/
 
        This manpage was written by Joao Eriberto Mota Filho.
 
 dnsmap-bulk-0.1                   18 Nov 2019                   dnsmap-bulk(1)
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## dnsmap Usage Example

Scan example.com using a wordlist (`-w /usr/share/wordlists/dnsmap.txt`):

```
root@kali:~# dnsmap example.com -w /usr/share/wordlists/dnsmap.txt
dnsmap 0.30 - DNS Network Mapper by pagvac (gnucitizen.org)

[+] searching (sub)domains for example.com using /usr/share/wordlists/dnsmap.txt
[+] using maximum random delay of 10 millisecond(s) between requests
```

## dnsmap-bulk Usage Example

Create a file containing domain names to scan (domains.txt) and pass it to dnsmap-bulk.sh:

```
root@kali:~# echo "example.com" >> domains.txt
root@kali:~# echo "example.org" >> domains.txt
root@kali:~# dnsmap-bulk.sh domains.txt
dnsmap 0.30 - DNS Network Mapper by pagvac (gnucitizen.org)

[+] searching (sub)domains for example.com using built-in wordlist
[+] using maximum random delay of 10 millisecond(s) between requests
```
