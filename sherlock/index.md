---
Title: sherlock
Homepage: https://github.com/sherlock-project/sherlock
Repository: https://gitlab.com/kalilinux/packages/sherlock
Architectures: all
Version: 0.14.3+git20231006-0kali1
Metapackages: kali-linux-everything 
Icon: images/sherlock-logo.svg
PackagesInfo: |
 ### sherlock
 
  This package contains a tool to find usernames across social networks.
 
 **Installed size:** `163 KB`  
 **How to install:** `sudo apt install sherlock`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-certifi
 * python3-colorama
 * python3-openpyxl
 * python3-pandas
 * python3-requests
 * python3-requests-futures
 * python3-socks
 * python3-stem
 * python3-torrequest
 {{< /spoiler >}}
 
 ##### sherlock
 
 
 ```
 root@kali:~# sherlock -h
 usage: sherlock [-h] [--version] [--verbose] [--folderoutput FOLDEROUTPUT]
                 [--output OUTPUT] [--tor] [--unique-tor] [--csv] [--xlsx]
                 [--site SITE_NAME] [--proxy PROXY_URL] [--json JSON_FILE]
                 [--timeout TIMEOUT] [--print-all] [--print-found] [--no-color]
                 [--browse] [--local] [--nsfw]
                 USERNAMES [USERNAMES ...]
 
 Sherlock: Find Usernames Across Social Networks (Version 0.14.3)
 
 positional arguments:
   USERNAMES             One or more usernames to check with social networks.
                         Check similar usernames using {%} (replace to '_',
                         '-', '.').
 
 options:
   -h, --help            show this help message and exit
   --version             Display version information and dependencies.
   --verbose, -v, -d, --debug
                         Display extra debugging information and metrics.
   --folderoutput FOLDEROUTPUT, -fo FOLDEROUTPUT
                         If using multiple usernames, the output of the results
                         will be saved to this folder.
   --output OUTPUT, -o OUTPUT
                         If using single username, the output of the result
                         will be saved to this file.
   --tor, -t             Make requests over Tor; increases runtime; requires
                         Tor to be installed and in system path.
   --unique-tor, -u      Make requests over Tor with new Tor circuit after each
                         request; increases runtime; requires Tor to be
                         installed and in system path.
   --csv                 Create Comma-Separated Values (CSV) File.
   --xlsx                Create the standard file for the modern Microsoft
                         Excel spreadsheet (xslx).
   --site SITE_NAME      Limit analysis to just the listed sites. Add multiple
                         options to specify more than one site.
   --proxy PROXY_URL, -p PROXY_URL
                         Make requests over a proxy. e.g.
                         socks5://127.0.0.1:1080
   --json JSON_FILE, -j JSON_FILE
                         Load data from a JSON file or an online, valid, JSON
                         file.
   --timeout TIMEOUT     Time (in seconds) to wait for response to requests
                         (Default: 60)
   --print-all           Output sites where the username was not found.
   --print-found         Output sites where the username was found (also if
                         exported as file).
   --no-color            Don't color terminal output
   --browse, -b          Browse to all results on default browser.
   --local, -l           Force the use of the local data.json file.
   --nsfw                Include checking of NSFW sites from default list.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
