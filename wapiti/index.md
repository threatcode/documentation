---
Title: wapiti
Homepage: https://wapiti.sourceforge.net/
Repository: https://salsa.debian.org/pkg-security-team/wapiti
Architectures: all
Version: 3.0.4+dfsg-2
Metapackages: kali-linux-default kali-linux-everything kali-linux-large kali-tools-identify kali-tools-information-gathering kali-tools-vulnerability kali-tools-web 
Icon: images/wapiti-logo.svg
PackagesInfo: |
 ### wapiti
 
  Wapiti allows you to audit the security of your web applications.
  It performs "black-box" scans, i.e. it does not study the source code of the
  application but will scan the web pages of the deployed web applications,
  looking for scripts and forms where it can inject data.
  Once it gets this list, Wapiti acts like a fuzzer, injecting payloads to see
  if a script is vulnerable.
   
  Wapiti can detect the following vulnerabilities:
   - Database Injection (PHP/ASP/JSP SQL Injections and XPath Injections)
   - Cross Site Scripting (XSS) reflected and permanent
   - File disclosure detection (local and remote include, require, fopen,
     readfile...)
   - Command Execution detection (eval(), system(), passtru()...)
   - XXE (Xml eXternal Entity) injection
   - CRLF Injection
   - Search for potentially dangerous files on the server (thank to the Nikto db)
   - Bypass of weak htaccess configurations
   - Search for copies (backup) of scripts on the server
   - Shellshock
   - DirBuster like
   - Server Side Request Forgery (through use of an external Wapiti website)
 
 **Installed size:** `1.54 MB`  
 **How to install:** `sudo apt install wapiti`  
 
 {{< spoiler "Dependencies:" >}}
 * libjs-jquery
 * python3
 * python3-bs4 
 * python3-importlib-metadata
 * python3-mako 
 * python3-markupsafe
 * python3-requests
 * python3-six 
 * python3-socks
 * python3-tld
 * python3-yaswfp
 {{< /spoiler >}}
 
 ##### wapiti
 
 A web application vulnerability scanner in Python
 
 ```
 root@kali:~# wapiti -h
 
      __    __            _ _   _ _____
     / / /\ \ \__ _ _ __ (_) |_(_)___ /
     \ \/  \/ / _` | '_ \| | __| | |_ \
      \  /\  / (_| | |_) | | |_| |___) |
       \/  \/ \__,_| .__/|_|\__|_|____/
                   |_|                 
 Wapiti-3.0.4 (wapiti.sourceforge.io)
 usage: wapiti [-h] [-u URL] [--scope {page,folder,domain,url,punk}]
               [-m MODULES_LIST] [--list-modules] [--update] [-l LEVEL]
               [-p PROXY_URL] [--tor] [-a CREDENTIALS]
               [--auth-type {basic,digest,kerberos,ntlm,post}] [-c COOKIE_FILE]
               [--skip-crawl] [--resume-crawl] [--flush-attacks]
               [--flush-session] [--store-session PATH] [--store-config PATH]
               [-s URL] [-x URL] [-r PARAMETER] [--skip PARAMETER] [-d DEPTH]
               [--max-links-per-page MAX] [--max-files-per-dir MAX]
               [--max-scan-time SECONDS] [--max-attack-time SECONDS]
               [--max-parameters MAX] [-S FORCE] [-t SECONDS] [-H HEADER]
               [-A AGENT] [--verify-ssl {0,1}] [--color] [-v LEVEL] [-f FORMAT]
               [-o OUPUT_PATH] [--external-endpoint EXTERNAL_ENDPOINT_URL]
               [--internal-endpoint INTERNAL_ENDPOINT_URL]
               [--endpoint ENDPOINT_URL] [--no-bugreport] [--version]
 
 Wapiti-3.0.4: Web application vulnerability scanner
 
 options:
   -h, --help            show this help message and exit
   -u URL, --url URL     The base URL used to define the scan scope (default
                         scope is folder)
   --scope {page,folder,domain,url,punk}
                         Set scan scope
   -m MODULES_LIST, --module MODULES_LIST
                         List of modules to load
   --list-modules        List Wapiti attack modules and exit
   --update              Update Wapiti attack modules and exit
   -l LEVEL, --level LEVEL
                         Set attack level
   -p PROXY_URL, --proxy PROXY_URL
                         Set the HTTP(S) proxy to use. Supported: http(s) and
                         socks proxies
   --tor                 Use Tor listener (127.0.0.1:9050)
   -a CREDENTIALS, --auth-cred CREDENTIALS
                         Set HTTP authentication credentials
   --auth-type {basic,digest,kerberos,ntlm,post}
                         Set the authentication type to use
   -c COOKIE_FILE, --cookie COOKIE_FILE
                         Set a JSON cookie file to use
   --skip-crawl          Don't resume the scanning process, attack URLs scanned
                         during a previous session
   --resume-crawl        Resume the scanning process (if stopped) even if some
                         attacks were previously performed
   --flush-attacks       Flush attack history and vulnerabilities for the
                         current session
   --flush-session       Flush everything that was previously found for this
                         target (crawled URLs, vulns, etc)
   --store-session PATH  Directory where to store attack history and session
                         data.
   --store-config PATH   Directory where to store configuration databases.
   -s URL, --start URL   Adds an url to start scan with
   -x URL, --exclude URL
                         Adds an url to exclude from the scan
   -r PARAMETER, --remove PARAMETER
                         Remove this parameter from urls
   --skip PARAMETER      Skip attacking given parameter(s)
   -d DEPTH, --depth DEPTH
                         Set how deep the scanner should explore the website
   --max-links-per-page MAX
                         Set how many (in-scope) links the scanner should
                         extract for each page
   --max-files-per-dir MAX
                         Set how many pages the scanner should explore per
                         directory
   --max-scan-time SECONDS
                         Set how many seconds you want the scan to last (floats
                         accepted)
   --max-attack-time SECONDS
                         Set how many seconds you want each attack module to
                         last (floats accepted)
   --max-parameters MAX  URLs and forms having more than MAX input parameters
                         will be erased before attack.
   -S FORCE, --scan-force FORCE
                         Easy way to reduce the number of scanned and attacked
                         URLs. Possible values: paranoid, sneaky, polite,
                         normal, aggressive, insane
   -t SECONDS, --timeout SECONDS
                         Set timeout for requests
   -H HEADER, --header HEADER
                         Set a custom header to use for every requests
   -A AGENT, --user-agent AGENT
                         Set a custom user-agent to use for every requests
   --verify-ssl {0,1}    Set SSL check (default is no check)
   --color               Colorize output
   -v LEVEL, --verbose LEVEL
                         Set verbosity level (0: quiet, 1: normal, 2: verbose)
   -f FORMAT, --format FORMAT
                         Set output format. Supported: json, html (default),
                         txt, xml
   -o OUPUT_PATH, --output OUPUT_PATH
                         Output file or folder
   --external-endpoint EXTERNAL_ENDPOINT_URL
                         Url serving as endpoint for target
   --internal-endpoint INTERNAL_ENDPOINT_URL
                         Url serving as endpoint for attacker
   --endpoint ENDPOINT_URL
                         Url serving as endpoint for both attacker and target
   --no-bugreport        Don't send automatic bug report when an attack module
                         fails
   --version             Show program's version number and exit
 ```
 
 - - -
 
 ##### wapiti-getcookie
 
 A Wapiti utility to fetch cookies from a webpage and store them in the Wapiti JSON format.
 
 ```
 root@kali:~# wapiti-getcookie -h
 usage: wapiti-getcookie [-h] -u URL -c COOKIE [-p PROXY] [--tor]
                         [-a CREDENTIALS]
                         [--auth-type {basic,digest,kerberos,ntlm}] [-d DATA]
                         [-A AGENT] [-H HEADER]
 
 Wapiti-getcookie: An utility to grab cookies from a webpage
 
 options:
   -h, --help            show this help message and exit
   -u URL, --url URL     First page to fetch for cookies
   -c COOKIE, --cookie COOKIE
                         Cookie file in Wapiti JSON format where cookies will
                         be stored
   -p PROXY, --proxy PROXY
                         Address of the proxy server to use
   --tor                 Use Tor listener (127.0.0.1:9050)
   -a CREDENTIALS, --auth-cred CREDENTIALS
                         Set HTTP authentication credentials
   --auth-type {basic,digest,kerberos,ntlm}
                         Set the authentication type to use
   -d DATA, --data DATA  Data to send to the form with POST
   -A AGENT, --user-agent AGENT
                         Set a custom user-agent to use for every requests
   -H HEADER, --header HEADER
                         Set a custom header to use for every requests
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
