---
Title: dirsearch
Homepage: https://github.com/maurosoria/dirsearch
Repository: https://salsa.debian.org/pkg-security-team/dirsearch
Architectures: all
Version: 0.4.3-1
Metapackages: kali-linux-everything 
Icon: images/dirsearch-logo.svg
PackagesInfo: |
 ### dirsearch
 
  This package contains is a command-line tool designed to brute force
  directories and files in webservers.
   
  As a feature-rich tool, dirsearch gives users the opportunity to perform a
  complex web content discovering, with many vectors for the wordlist, high
  accuracy, impressive performance, advanced connection/request settings, modern
  brute-force techniques and nice output.
 
 **Installed size:** `447 KB`  
 **How to install:** `sudo apt install dirsearch`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-bs4
 * python3-certifi
 * python3-cffi
 * python3-chardet
 * python3-charset-normalizer
 * python3-colorama
 * python3-cryptography 
 * python3-defusedxml
 * python3-idna
 * python3-jinja2
 * python3-markupsafe
 * python3-ntlm-auth
 * python3-openssl
 * python3-pyparsing
 * python3-requests
 * python3-requests-ntlm
 * python3-socks
 * python3-urllib3
 {{< /spoiler >}}
 
 ##### dirsearch
 
 An advanced command-line tool designed to brute force directories and files in webservers
 
 ```
 root@kali:~# dirsearch -h
 Usage: dirsearch.py [-u|--url] target [-e|--extensions] extensions [options]
 
 Options:
   --version             show program's version number and exit
   -h, --help            show this help message and exit
 
   Mandatory:
     -u URL, --url=URL   Target URL(s), can use multiple flags
     -l PATH, --url-file=PATH
                         URL list file
     --stdin             Read URL(s) from STDIN
     --cidr=CIDR         Target CIDR
     --raw=PATH          Load raw HTTP request from file (use `--scheme` flag
                         to set the scheme)
     -s SESSION_FILE, --session=SESSION_FILE
                         Session file
     --config=PATH       Full path to config file, see 'config.ini' for example
                         (Default: config.ini)
 
   Dictionary Settings:
     -w WORDLISTS, --wordlists=WORDLISTS
                         Customize wordlists (separated by commas)
     -e EXTENSIONS, --extensions=EXTENSIONS
                         Extension list separated by commas (e.g. php,asp)
     -f, --force-extensions
                         Add extensions to the end of every wordlist entry. By
                         default dirsearch only replaces the %EXT% keyword with
                         extensions
     -O, --overwrite-extensions
                         Overwrite other extensions in the wordlist with your
                         extensions (selected via `-e`)
     --exclude-extensions=EXTENSIONS
                         Exclude extension list separated by commas (e.g.
                         asp,jsp)
     --remove-extensions
                         Remove extensions in all paths (e.g. admin.php ->
                         admin)
     --prefixes=PREFIXES
                         Add custom prefixes to all wordlist entries (separated
                         by commas)
     --suffixes=SUFFIXES
                         Add custom suffixes to all wordlist entries, ignore
                         directories (separated by commas)
     -U, --uppercase     Uppercase wordlist
     -L, --lowercase     Lowercase wordlist
     -C, --capital       Capital wordlist
 
   General Settings:
     -t THREADS, --threads=THREADS
                         Number of threads
     -r, --recursive     Brute-force recursively
     --deep-recursive    Perform recursive scan on every directory depth (e.g.
                         api/users -> api/)
     --force-recursive   Do recursive brute-force for every found path, not
                         only directories
     -R DEPTH, --max-recursion-depth=DEPTH
                         Maximum recursion depth
     --recursion-status=CODES
                         Valid status codes to perform recursive scan, support
                         ranges (separated by commas)
     --subdirs=SUBDIRS   Scan sub-directories of the given URL[s] (separated by
                         commas)
     --exclude-subdirs=SUBDIRS
                         Exclude the following subdirectories during recursive
                         scan (separated by commas)
     -i CODES, --include-status=CODES
                         Include status codes, separated by commas, support
                         ranges (e.g. 200,300-399)
     -x CODES, --exclude-status=CODES
                         Exclude status codes, separated by commas, support
                         ranges (e.g. 301,500-599)
     --exclude-sizes=SIZES
                         Exclude responses by sizes, separated by commas (e.g.
                         0B,4KB)
     --exclude-text=TEXTS
                         Exclude responses by text, can use multiple flags
     --exclude-regex=REGEX
                         Exclude responses by regular expression
     --exclude-redirect=STRING
                         Exclude responses if this regex (or text) matches
                         redirect URL (e.g. '/index.html')
     --exclude-response=PATH
                         Exclude responses similar to response of this page,
                         path as input (e.g. 404.html)
     --skip-on-status=CODES
                         Skip target whenever hit one of these status codes,
                         separated by commas, support ranges
     --min-response-size=LENGTH
                         Minimum response length
     --max-response-size=LENGTH
                         Maximum response length
     --max-time=SECONDS  Maximum runtime for the scan
     --exit-on-error     Exit whenever an error occurs
 
   Request Settings:
     -m METHOD, --http-method=METHOD
                         HTTP method (default: GET)
     -d DATA, --data=DATA
                         HTTP request data
     --data-file=PATH    File contains HTTP request data
     -H HEADERS, --header=HEADERS
                         HTTP request header, can use multiple flags
     --header-file=PATH  File contains HTTP request headers
     -F, --follow-redirects
                         Follow HTTP redirects
     --random-agent      Choose a random User-Agent for each request
     --auth=CREDENTIAL   Authentication credential (e.g. user:password or
                         bearer token)
     --auth-type=TYPE    Authentication type (basic, digest, bearer, ntlm, jwt,
                         oauth2)
     --cert-file=PATH    File contains client-side certificate
     --key-file=PATH     File contains client-side certificate private key
                         (unencrypted)
     --user-agent=USER_AGENT
     --cookie=COOKIE     
 
   Connection Settings:
     --timeout=TIMEOUT   Connection timeout
     --delay=DELAY       Delay between requests
     --proxy=PROXY       Proxy URL (HTTP/SOCKS), can use multiple flags
     --proxy-file=PATH   File contains proxy servers
     --proxy-auth=CREDENTIAL
                         Proxy authentication credential
     --replay-proxy=PROXY
                         Proxy to replay with found paths
     --tor               Use Tor network as proxy
     --scheme=SCHEME     Scheme for raw request or if there is no scheme in the
                         URL (Default: auto-detect)
     --max-rate=RATE     Max requests per second
     --retries=RETRIES   Number of retries for failed requests
     --ip=IP             Server IP address
 
   Advanced Settings:
     --crawl             Crawl for new paths in responses
 
   View Settings:
     --full-url          Full URLs in the output (enabled automatically in
                         quiet mode)
     --redirects-history
                         Show redirects history
     --no-color          No colored output
     -q, --quiet-mode    Quiet mode
 
   Output Settings:
     -o PATH, --output=PATH
                         Output file
     --format=FORMAT     Report format (Available: simple, plain, json, xml,
                         md, csv, html, sqlite)
     --log=PATH          Log file
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
