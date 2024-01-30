---
Title: theharvester
Homepage: https://github.com/laramies/theHarvester
Repository: https://gitlab.com/kalilinux/packages/theharvester
Architectures: all
Version: 4.4.4-0kali2
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-information-gathering kali-tools-vulnerability 
Icon: images/theharvester-logo.svg
PackagesInfo: |
 ### theharvester
 
  The package contains a tool for gathering subdomain names, e-mail addresses,
  virtual hosts, open ports/ banners, and employee names from different public
  sources (search engines, pgp key servers).
 
 **Installed size:** `1.79 MB`  
 **How to install:** `sudo apt install theharvester`  
 
 {{< spoiler "Dependencies:" >}}
 * kali-defaults
 * python3
 * python3-aiodns 
 * python3-aiofiles
 * python3-aiohttp 
 * python3-aiomultiprocess 
 * python3-aiosqlite 
 * python3-bs4 
 * python3-censys 
 * python3-certifi 
 * python3-dateutil
 * python3-dnspython 
 * python3-fastapi 
 * python3-lxml 
 * python3-netaddr 
 * python3-pyppeteer 
 * python3-requests 
 * python3-retrying 
 * python3-shodan 
 * python3-slowapi
 * python3-starlette
 * python3-ujson
 * python3-uvicorn
 * python3-uvloop 
 * python3-yaml 
 {{< /spoiler >}}
 
 ##### restfulHarvest
 
 
 ```
 root@kali:~# restfulHarvest -h
 usage: restfulHarvest [-h] [-H HOST] [-p PORT] [-l LOG_LEVEL] [-r]
 
 options:
   -h, --help            show this help message and exit
   -H HOST, --host HOST  IP address to listen on default is 127.0.0.1
   -p PORT, --port PORT  Port to bind the web server to, default is 5000
   -l LOG_LEVEL, --log-level LOG_LEVEL
                         Set logging level, default is info but
                         [critical|error|warning|info|debug|trace] can be set
   -r, --reload          Enable automatic reload used during development of the
                         api
 ```
 
 - - -
 
 ##### theHarvester
 
 
 ```
 root@kali:~# theHarvester -h
 *******************************************************************
 *  _   _                                            _             *
 * | |_| |__   ___    /\  /\__ _ _ ____   _____  ___| |_ ___ _ __  *
 * | __|  _ \ / _ \  / /_/ / _` | '__\ \ / / _ \/ __| __/ _ \ '__| *
 * | |_| | | |  __/ / __  / (_| | |   \ V /  __/\__ \ ||  __/ |    *
 *  \__|_| |_|\___| \/ /_/ \__,_|_|    \_/ \___||___/\__\___|_|    *
 *                                                                 *
 * theHarvester 4.4.4                                              *
 * Coded by Christian Martorella                                   *
 * Edge-Security Research                                          *
 * cmartorella@edge-security.com                                   *
 *                                                                 *
 *******************************************************************
 usage: theHarvester [-h] -d DOMAIN [-l LIMIT] [-S START] [-p] [-s]
                     [--screenshot SCREENSHOT] [-v] [-e DNS_SERVER] [-t]
                     [-r [DNS_RESOLVE]] [-n] [-c] [-f FILENAME] [-b SOURCE]
 
 theHarvester is used to gather open source intelligence (OSINT) on a company
 or domain.
 
 options:
   -h, --help            show this help message and exit
   -d DOMAIN, --domain DOMAIN
                         Company name or domain to search.
   -l LIMIT, --limit LIMIT
                         Limit the number of search results, default=500.
   -S START, --start START
                         Start with result number X, default=0.
   -p, --proxies         Use proxies for requests, enter proxies in
                         proxies.yaml.
   -s, --shodan          Use Shodan to query discovered hosts.
   --screenshot SCREENSHOT
                         Take screenshots of resolved domains specify output
                         directory: --screenshot output_directory
   -v, --virtual-host    Verify host name via DNS resolution and search for
                         virtual hosts.
   -e DNS_SERVER, --dns-server DNS_SERVER
                         DNS server to use for lookup.
   -t, --take-over       Check for takeovers.
   -r [DNS_RESOLVE], --dns-resolve [DNS_RESOLVE]
                         Perform DNS resolution on subdomains with a resolver
                         list or passed in resolvers, default False.
   -n, --dns-lookup      Enable DNS server lookup, default False.
   -c, --dns-brute       Perform a DNS brute force on the domain.
   -f FILENAME, --filename FILENAME
                         Save the results to an XML and JSON file.
   -b SOURCE, --source SOURCE
                         anubis, baidu, bevigil, binaryedge, bing, bingapi,
                         bufferoverun, brave, censys, certspotter, criminalip,
                         crtsh, dnsdumpster, duckduckgo, fullhunt, github-code,
                         hackertarget, hunter, hunterhow, intelx, netlas,
                         onyphe, otx, pentesttools, projectdiscovery, rapiddns,
                         rocketreach, securityTrails, sitedossier,
                         subdomaincenter, subdomainfinderc99, threatminer,
                         tomba, urlscan, virustotal, yahoo, zoomeye
 ```
 
 - - -
 
 ##### theharvester
 
 
 ```
 root@kali:~# theharvester -h
 ┏━(Message from Kali developers)
 ┃
 ┃ The command theharvester is deprecated. Please use theHarvester instead.
 ┃
 ┗━
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## theharvester Usage Example

Search from email addresses from a domain (`-d kali.org`), limiting the results to 500 (`-l 500`), using DuckDuckGo (`-b duckduckgo`):

```
root@kali:~# theHarvester -d kali.org -l 500 -b duckduckgo
*******************************************************************
*  _   _                                            _             *
* | |_| |__   ___    /\  /\__ _ _ ____   _____  ___| |_ ___ _ __  *
* | __|  _ \ / _ \  / /_/ / _` | '__\ \ / / _ \/ __| __/ _ \ '__| *
* | |_| | | |  __/ / __  / (_| | |   \ V /  __/\__ \ ||  __/ |    *
*  \__|_| |_|\___| \/ /_/ \__,_|_|    \_/ \___||___/\__\___|_|    *
*                                                                 *
* theHarvester 4.4.3                                              *
* Coded by Christian Martorella                                   *
* Edge-Security Research                                          *
* cmartorella@edge-security.com                                   *
*                                                                 *
*******************************************************************

[*] Target: kali.org

[*] Searching Duckduckgo.

[*] No IPs found.

[*] No emails found.

[*] Hosts found: 14
---------------------
[...]

```
