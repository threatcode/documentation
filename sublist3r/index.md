---
Title: sublist3r
Homepage: https://github.com/aboul3la/Sublist3r
Repository: https://salsa.debian.org/pkg-security-team/sublist3r
Architectures: all
Version: 1.1-4
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### sublist3r
 
  This package contains a Python security tool designed to enumerate subdomains
  of websites using OSINT. It helps penetration testers and bug hunters collect
  and gather subdomains for the domain they are targeting over the network.
  Sublist3r enumerates subdomains using many search engines such as Google,
  Yahoo, Bing, Baidu, and Ask. Sublist3r also enumerates subdomains using
  Netcraft, Virustotal, ThreatCrowd, DNSdumpster, and ReverseDNS.
   
  Subbrute was integrated with Sublist3r to increase the possibility of finding
  more subdomains using bruteforce with an improved wordlist.
 
 **Installed size:** `1.85 MB`  
 **How to install:** `sudo apt install sublist3r`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3  | python3  | python3 
 * python3-dnspython
 * python3-requests
 {{< /spoiler >}}
 
 ##### sublist3r
 
 Tool designed to enumerate subdomains of websites using OSINT
 
 ```
 root@kali:~# sublist3r -h
 usage: sublist3r [-h] -d DOMAIN [-b [BRUTEFORCE]] [-p PORTS] [-v [VERBOSE]]
                  [-t THREADS] [-e ENGINES] [-o OUTPUT] [-n]
 
 OPTIONS:
   -h, --help            show this help message and exit
   -d DOMAIN, --domain DOMAIN
                         Domain name to enumerate it's subdomains
   -b [BRUTEFORCE], --bruteforce [BRUTEFORCE]
                         Enable the subbrute bruteforce module
   -p PORTS, --ports PORTS
                         Scan the found subdomains against specified tcp ports
   -v [VERBOSE], --verbose [VERBOSE]
                         Enable Verbosity and display results in realtime
   -t THREADS, --threads THREADS
                         Number of threads to use for subbrute bruteforce
   -e ENGINES, --engines ENGINES
                         Specify a comma-separated list of search engines
   -o OUTPUT, --output OUTPUT
                         Save the results to text file
   -n, --no-color        Output without color
 
 Example: python3 /usr/bin/sublist3r -d google.com
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## sublist3r Usage Examples

Search for subdomains of kali.org (`-d kali.org`) using the Bing search engine (`-e bing`) with 3 threads (`-t 3`).

```
root@kali:~# sublist3r -d kali.org -t 3 -e bing

                 ____        _     _ _     _   _____
                / ___| _   _| |__ | (_)___| |_|___ / _ __
                \___ \| | | | '_ \| | / __| __| |_ \| '__|
                 ___) | |_| | |_) | | \__ \ |_ ___) | |
                |____/ \__,_|_.__/|_|_|___/\__|____/|_|

                # Coded By Ahmed Aboul-Ela - @aboul3la

[-] Enumerating subdomains now for kali.org
[-] Searching now in Bing..
[-] Total Unique Subdomains Found: 19
www.kali.org
archive-3.kali.org
archive-4.kali.org
archive-5.kali.org
bugs.kali.org
cdimage.kali.org
docs.kali.org
ar.docs.kali.org
he.docs.kali.org
id.docs.kali.org
tr.docs.kali.org
forums.kali.org
git.kali.org
http.kali.org
images.kali.org
pkg.kali.org
repo.kali.org
security.kali.org
tools.kali.org
```
