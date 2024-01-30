---
Title: wafw00f
Homepage: https://github.com/sandrogauci/wafw00f
Repository: https://salsa.debian.org/pkg-security-team/wafw00f
Architectures: all
Version: 2.2.0-1
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-information-gathering kali-tools-vulnerability kali-tools-web 
Icon: images/wafw00f-logo.svg
PackagesInfo: |
 ### wafw00f
 
  This package identifies and fingerprints Web Application Firewall (WAF)
  products using the following logic:
   
   - Sends a _normal_ HTTP request and analyses the response; this identifies a
     number of WAF solutions.
   - If that is not successful, it sends a number of (potentially malicious)
     HTTP requests and uses simple logic to deduce which WAF it is.
   - If that is also not successful, it analyses the responses previously
     returned and uses another simple algorithm to guess if a WAF or security
     solution is actively responding to the attacks.
 
 **Installed size:** `240 KB`  
 **How to install:** `sudo apt install wafw00f`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-pluginbase
 * python3-requests
 {{< /spoiler >}}
 
 ##### wafw00f
 
 Identify and fingerprint Web Application Firewall products
 
 ```
 root@kali:~# wafw00f -h
 Usage: wafw00f url1 [url2 [url3 ... ]]
 example: wafw00f http://www.victim.org/
 
 Options:
   -h, --help            show this help message and exit
   -v, --verbose         Enable verbosity, multiple -v options increase
                         verbosity
   -a, --findall         Find all WAFs which match the signatures, do not stop
                         testing on the first one
   -r, --noredirect      Do not follow redirections given by 3xx responses
   -t TEST, --test=TEST  Test for one specific WAF
   -o OUTPUT, --output=OUTPUT
                         Write output to csv, json or text file depending on
                         file extension. For stdout, specify - as filename.
   -f FORMAT, --format=FORMAT
                         Force output format to csv, json or text.
   -i INPUT, --input-file=INPUT
                         Read targets from a file. Input format can be csv,
                         json or text. For csv and json, a `url` column name or
                         element is required.
   -l, --list            List all WAFs that WAFW00F is able to detect
   -p PROXY, --proxy=PROXY
                         Use an HTTP proxy to perform requests, examples:
                         http://hostname:8080, socks5://hostname:1080,
                         http://user:pass@hostname:8080
   -V, --version         Print out the current version of WafW00f and exit.
   -H HEADERS, --headers=HEADERS
                         Pass custom headers via a text file to overwrite the
                         default header set.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
