---
Title: emailharvester
Homepage: https://github.com/maldevel/EmailHarvester
Repository: https://gitlab.com/kalilinux/packages/emailharvester
Architectures: all
Version: 1.3.2+git20191005-0kali2
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### emailharvester
 
  This package contains EmailHarvester, a tool to retrieve Domain email
  addresses from Search Engines. Features:
   * Retrieve Domain email addresses from popular Search engines (Google, Bing,
     Yahoo, ASK, Baidu, Dogpile, Exalead)
   * Export results to txt and xml files
   * Limit search results
   * Define your own User-Agent string
   * Use proxy server
   * Plugins system
   * Search in popular web sites using Search engines (Twitter, LinkedIn,
     Google+, Github, Instagram, Reddit, Youtube)
 
 **Installed size:** `69 KB`  
 **How to install:** `sudo apt install emailharvester`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-colorama
 * python3-requests
 * python3-termcolor
 * python3-validators
 {{< /spoiler >}}
 
 ##### emailharvester
 
 
 ```
 root@kali:~# emailharvester -h
 usage: EmailHarvester.py [-h] [-d DOMAIN] [-s FILE] [-e ENGINE] [-l LIMIT]
                          [-u USER-AGENT] [-x PROXY] [--noprint]
                          [-r EXCLUDED_PLUGINS] [-p]
 
  _____                   _  _   _   _                                _              
 |  ___|                 (_)| | | | | |                              | |             
 | |__  _ __ ___    __ _  _ | | | |_| |  __ _  _ __ __   __ ___  ___ | |_  ___  _ __ 
 |  __|| '_ ` _ \  / _` || || | |  _  | / _` || '__|\ \ / // _ \/ __|| __|/ _ \| '__|
 | |___| | | | | || (_| || || | | | | || (_| || |    \ V /|  __/\__ \| |_|  __/| |   
 \____/|_| |_| |_| \__,_||_||_| \_| |_/ \__,_||_|     \_/  \___||___/ \__|\___||_| 
 
     A tool to retrieve Domain email addresses from Search Engines | @maldevel
                                 Version: 1.3.2
 
 options:
   -h, --help            show this help message and exit
   -d DOMAIN, --domain DOMAIN
                         Domain to search.
   -s FILE, --save FILE  Save the results into a TXT and XML file (both).
   -e ENGINE, --engine ENGINE
                         Select search engine plugin(eg. '-e google').
   -l LIMIT, --limit LIMIT
                         Limit the number of results.
   -u USER-AGENT, --user-agent USER-AGENT
                         Set the User-Agent request header.
   -x PROXY, --proxy PROXY
                         Setup proxy server (eg. '-x http://127.0.0.1:8080')
   --noprint             EmailHarvester will print discovered emails to terminal. It is possible to tell EmailHarvester not to print results to terminal with this option.
   -r EXCLUDED_PLUGINS, --exclude EXCLUDED_PLUGINS
                         Plugins to exclude when you choose 'all' for search engine (eg. '-r google,twitter')
   -p, --list-plugins    List all available plugins.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
