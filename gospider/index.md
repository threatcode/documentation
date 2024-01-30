---
Title: gospider
Homepage: https://github.com/jaeles-project/gospider
Repository: https://gitlab.com/kalilinux/packages/gospider
Architectures: any
Version: 1.1.0-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### gospider
 
  This package contains a Fast web spider written in Go. The features are:
     - Fast web crawling
     - Brute force and parse sitemap.xml
     - Parse robots.txt
     - Generate and verify link from JavaScript files
     - Link Finder
     - Find AWS-S3 from response source
     - Find subdomains from response source
     - Get URLs from Wayback Machine, Common Crawl, Virus Total, Alien Vault
     - Format output easy to Grep
     - Support Burp input
     - Crawl multiple sites in parallel
     - Random mobile/web User-AgentShowcases
 
 **Installed size:** `11.18 MB`  
 **How to install:** `sudo apt install gospider`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### gospider
 
 
 ```
 root@kali:~# gospider -h
 A Simple Web Spider - v1.1.0 by @theblackturtle
 
 Usage:
   gospider [flags]
 
 Flags:
   -s, --site string            Site to crawl
   -S, --sites string           Site list to crawl
   -p, --proxy string           Proxy (Ex: http://127.0.0.1:8080)
   -o, --output string          Output folder
   -u, --user-agent string      User Agent to use
                                	web: random web user-agent
                                	mobi: random mobile user-agent
                                	or you can set your special user-agent (default "web")
       --cookie string          Cookie to use (testA=a; testB=b)
   -H, --header stringArray     Header to use (Use multiple flag to set multiple header)
       --burp string            Load headers and cookie from burp raw http request
       --blacklist string       Blacklist URL Regex
   -t, --threads int            Number of threads (Run sites in parallel) (default 1)
   -c, --concurrent int         The number of the maximum allowed concurrent requests of the matching domains (default 5)
   -d, --depth int              MaxDepth limits the recursion depth of visited URLs. (Set it to 0 for infinite recursion) (default 1)
   -k, --delay int              Delay is the duration to wait before creating a new request to the matching domains (second)
   -K, --random-delay int       RandomDelay is the extra randomized duration to wait added to Delay before creating a new request (second)
   -m, --timeout int            Request timeout (second) (default 10)
       --sitemap                Try to crawl sitemap.xml
       --robots                 Try to crawl robots.txt (default true)
   -a, --other-source           Find URLs from 3rd party (Archive.org, CommonCrawl.org, VirusTotal.com)
   -w, --include-subs           Include subdomains crawled from 3rd party. Default is main domain
   -r, --include-other-source   Also include other-source's urls (still crawl and request)
       --debug                  Turn on debug mode
   -v, --verbose                Turn on verbose
       --no-redirect            Disable redirect
       --version                Check version
   -h, --help                   help for gospider
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
