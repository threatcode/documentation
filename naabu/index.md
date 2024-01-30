---
Title: naabu
Homepage: https://github.com/projectdiscovery/naabu
Repository: https://gitlab.com/kalilinux/packages/naabu
Architectures: any
Version: 2.0.5-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### naabu
 
  This package contains a port scanning tool written in Go that allows you to
  enumerate valid ports for hosts in a fast and reliable manner. It is a really
  simple tool that does fast SYN/CONNECT scans on the host/list of hosts and
  lists all ports that return a reply.
  Main features are:
    * Fast And Simple SYN/CONNECT probe based scanning.
    * Optimized for ease of use and lightweight on resources
    * Automatic handling of duplicate hosts between multiple subdomains
    * NMAP Integration for service discovery
    * Piped input / output support for integrating in workflows
    * Multiple Output formats supported (JSON, File, Stdout)
    * Multiple input support including HOST/IP/CIDR notation
 
 **Installed size:** `11.44 MB`  
 **How to install:** `sudo apt install naabu`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libpcap0.8 
 {{< /spoiler >}}
 
 ##### naabu
 
 
 ```
 root@kali:~# naabu -h
 Naabu is a port scanning tool written in Go that allows you to enumerate open ports for hosts in a fast and reliable manner.
 
 Usage:
   naabu [flags]
 
 Flags:
 INPUT:
    -host string                Host to scan ports for
    -list, -l string            File containing list of hosts to scan ports
    -exclude-hosts, -eh string  Specifies a comma-separated list of targets to be excluded from the scan (ip, cidr)
    -exclude-file, -ef string   Specifies a newline-delimited file with targets to be excluded from the scan (ip, cidr)
 PORT:
    -port, -p string            Ports to scan (80, 80,443, 100-200
    -top-ports, -tp string      Top Ports to scan (default top 100)
    -exclude-ports, -ep string  Ports to exclude from scan
    -ports-file, -pf string     File containing ports to scan for
    -exclude-cdn, -ec           Skip full port scans for CDNs (only checks for 80,443)
 RATE-LIMIT:
    -c int     General internal worker threads (default 25)
    -rate int  Rate of port scan probe request (default 1000)
 OUTPUT:
    -o, -output string  File to write output to (optional)
    -json               Write output in JSON lines Format
 CONFIGURATION:
    -scan-all-ips          Scan all the ips
    -scan-type, -s string  Port scan type (SYN/CONNECT) (default "s")
    -source-ip string      Source Ip
    -interface-list, -il   List available interfaces and public ip
    -interface, -i string  Network Interface to use for port scan
    -nmap                  Invoke nmap scan on targets (nmap must be installed) - Deprecated
    -nmap-cli string       nmap command to run on found results (example: -nmap-cli 'nmap -sV')
    -r string              Custom resolvers to use to resolve DNS names (comma separated or from file)
 OPTIMIZATION:
    -retries int       Number of retries for the port scan probe (default 3)
    -timeout int       Millisecond to wait before timing out (default 1000)
    -warm-up-time int  Time in seconds between scan phases (default 2)
    -ping              Use ping probes for verification of host
    -verify            Validate the ports again with TCP verification
 DEBUG:
    -debug          Enable debugging information
    -v              Show Verbose output
    -no-color, -nc  Don't Use colors in output
    -silent         Show found ports only in output
    -version        Show version of naabu
    -stats          Display stats of the running scan
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
