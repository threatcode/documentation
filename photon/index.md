---
Title: photon
Homepage: https://github.com/s0md3v/Photon
Repository: https://gitlab.com/kalilinux/packages/photon
Architectures: all
Version: 1.3.0-0kali1
Metapackages: kali-linux-everything kali-linux-large 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### photon
 
  This package includes a fast and flexible crawler designed for open source
  intelligence (OSINT).
   
  Photon can extract the following data while crawling:
   - URLs (in-scope & out-of-scope)
   - URLs with parameters (example.com/gallery.php?id=2)
   - Intel (emails, social media accounts, amazon buckets etc.)
   - Files (pdf, png, xml etc.)
   - Secret keys (auth/API keys & hashes)
   - JavaScript files & Endpoints present in them
   - Strings matching custom regex pattern
   - Subdomains & DNS related data
   
  The extracted information is saved in an organized manner or can be exported
  as json.
 
 **Installed size:** `60 KB`  
 **How to install:** `sudo apt install photon`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-requests
 * python3-socks
 * python3-tld
 * python3-urllib3
 {{< /spoiler >}}
 
 ##### photon
 
 
 ```
 root@kali:~# photon -h
       ____  __          __
      / __ \/ /_  ____  / /_____  ____
     / /_/ / __ \/ __ \/ __/ __ \/ __ \
    / ____/ / / / /_/ / /_/ /_/ / / / /
   /_/   /_/ /_/\____/\__/\____/_/ /_/ v1.2.2
 
 usage: photon.py [-h] [-u ROOT] [-c COOK] [-r REGEX] [-e {csv,json}]
                  [-o OUTPUT] [-l LEVEL] [-t THREADS] [-d DELAY] [-v]
                  [-s SEEDS [SEEDS ...]] [--stdout STD]
                  [--user-agent USER_AGENT] [--exclude EXCLUDE]
                  [--timeout TIMEOUT] [--clone] [--headers] [--dns] [--keys]
                  [--only-urls] [--wayback]
 
 options:
   -h, --help            show this help message and exit
   -u ROOT, --url ROOT   root url
   -c COOK, --cookie COOK
                         cookie
   -r REGEX, --regex REGEX
                         regex pattern
   -e {csv,json}, --export {csv,json}
                         export format
   -o OUTPUT, --output OUTPUT
                         output directory
   -l LEVEL, --level LEVEL
                         levels to crawl
   -t THREADS, --threads THREADS
                         number of threads
   -d DELAY, --delay DELAY
                         delay between requests
   -v, --verbose         verbose output
   -s SEEDS [SEEDS ...], --seeds SEEDS [SEEDS ...]
                         additional seed URLs
   --stdout STD          send variables to stdout
   --user-agent USER_AGENT
                         custom user agent(s)
   --exclude EXCLUDE     exclude URLs matching this regex
   --timeout TIMEOUT     http request timeout
   --clone               clone the website locally
   --headers             add headers
   --dns                 enumerate subdomains and DNS data
   --keys                find secret keys
   --only-urls           only extract URLs
   --wayback             fetch URLs from archive.org as seeds
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
