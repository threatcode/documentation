---
Title: parsero
Homepage: https://github.com/behindthefirewalls/Parsero
Repository: https://gitlab.com/kalilinux/packages/parsero
Architectures: all
Version: 0.81~git20140929-0kali1
Metapackages: kali-linux-everything 
Icon: images/parsero-logo.svg
PackagesInfo: |
 ### parsero
 
  Parsero is a free script written in Python which reads the Robots.txt file of
  a web server and looks at the Disallow entries. The Disallow entries tell the
  search engines what directories or files hosted on a web server mustn't be
  indexed. For example, "Disallow: /portal/login" means that the content on
  www.example.com/portal/login it's not allowed to be indexed by crawlers like
  Google, Bing, Yahoo... This is the way the administrator have to not share
  sensitive or private information with the search engines.
 
 **Installed size:** `20 KB`  
 **How to install:** `sudo apt install parsero`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-bs4
 * python3-urllib3
 {{< /spoiler >}}
 
 ##### parsero
 
 
 ```
 root@kali:~# parsero -h
 usage: parsero [-h] [-u URL] [-o] [-sb] [-f FILE]
 
 options:
   -h, --help  show this help message and exit
   -u URL      Type the URL which will be analyzed
   -o          Show only the "HTTP 200" status code
   -sb         Search in Bing indexed Disallows
   -f FILE     Scan a list of domains from a list
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## Video

<script id="asciicast-31995" src="https://asciinema.org/a/31995.js" async type="text/javascript"></script>

## parsero Usage Example

Search for results from a website (`-u www.bing.com`) using Bing indexed Disallows (`-sb`):

````
root@kali:~# parsero -u www.bing.com -sb

____
| _ \ __ _ _ __ ___ ___ _ __ ___
| |_) / _` | '__/ __|/ _ \ '__/ _ \
| __/ (_| | | \__ \ __/ | | (_) |
|_| \__,_|_| |___/\___|_| \___/

Starting Parsero v0.75 (https://github.com/behindthefirewalls/Parsero) at 06/09/14 12:48:25
Parsero scan report for www.bing.com
http://www.bing.com/travel/secure 301 Moved Permanently
http://www.bing.com/travel/flight/flightSearchAction 301 Moved Permanently
http://www.bing.com/travel/css 301 Moved Permanently
http://www.bing.com/results 404 Not Found
http://www.bing.com/spbasic 404 Not Found
http://www.bing.com/entities/search 302 Found
http://www.bing.com/translator/? 200 OK
http://www.bing.com/Proxy.ashx 404 Not Found
http://www.bing.com/images/search? 200 OK
http://www.bing.com/travel/hotel/hotelSearch 301 Moved Permanently
http://www.bing.com/static/ 404 Not Found
http://www.bing.com/offers/proxy/dealsserver/api/log 405 Method Not Allowed
http://www.bing.com/shenghuo 301 Moved Permanently
http://www.bing.com/widget/render 200 OK
````
