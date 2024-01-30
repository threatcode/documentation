---
Title: changeme
Homepage: https://github.com/ztgrace/changeme
Repository: https://salsa.debian.org/pkg-security-team/changeme
Architectures: all
Version: 1.2.3-3
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### changeme
 
  This package contains a default credential scanner. Commercial vulnerability
  scanners miss common default credentials. Getting default credentials added to
  commercial scanners is often difficult and slow. changeme is designed to be
  simple to add new credentials without having to write any code or modules.
   
  changeme keeps credential data separate from code. All credentials are stored
  in yaml files so they can be both easily read by humans and processed by
  changeme. Credential files can be created by using the ./changeme.py --mkcred
  tool and answering a few questions.
   
  changeme supports the http/https, MSSQL, MySQL, Postgres, ssh and ssh w/key
  protocols. Use ./changeme.py --dump to output all of the currently available
  credentials.
 
 **Installed size:** `313 KB`  
 **How to install:** `sudo apt install changeme`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-cerberus
 * python3-jinja2
 * python3-libnmap
 * python3-logutils
 * python3-lxml
 * python3-memcache
 * python3-netaddr
 * python3-nose
 * python3-paramiko
 * python3-psycopg2
 * python3-pymongo
 * python3-pyodbc
 * python3-pysnmp4
 * python3-redis
 * python3-requests
 * python3-selenium
 * python3-shodan
 * python3-sqlalchemy
 * python3-tabulate
 * python3-yaml
 {{< /spoiler >}}
 
 ##### changeme
 
 Default Credential Scanner
 
 ```
 root@kali:~# changeme -h
 
  #####################################################
 #       _                                             #
 #   ___| |__   __ _ _ __   __ _  ___ _ __ ___   ___   #
 #  / __| '_ \ / _` | '_ \ / _` |/ _ \ '_ ` _ \ / _ \  #
 # | (__| | | | (_| | | | | (_| |  __/ | | | | |  __/  #
 #  \___|_| |_|\__,_|_| |_|\__, |\___|_| |_| |_|\___|  #
 #                         |___/                       #
 #  v1.2.3                                             #
 #  Default Credential Scanner by @ztgrace             #
  #####################################################
     
 usage: changeme.py [-h] [--all] [--category CATEGORY] [--contributors]
                    [--debug] [--delay DELAY] [--dump] [--dryrun]
                    [--fingerprint] [--fresh] [--log LOG] [--mkcred]
                    [--name NAME] [--noversion] [--proxy PROXY]
                    [--output OUTPUT] [--oa] [--protocols PROTOCOLS]
                    [--portoverride] [--redishost REDISHOST]
                    [--redisport REDISPORT] [--resume]
                    [--shodan_query SHODAN_QUERY] [--shodan_key SHODAN_KEY]
                    [--ssl] [--threads THREADS] [--timeout TIMEOUT]
                    [--useragent USERAGENT] [--validate] [--verbose]
                    target
 
 Default credential scanner v1.2.3
 
 positional arguments:
   target                Target to scan. Can be IP, subnet, hostname, nmap xml
                         file, text file or proto://host:port
 
 options:
   -h, --help            show this help message and exit
   --all, -a             Scan for all protocols
   --category CATEGORY, -c CATEGORY
                         Category of default creds to scan for
   --contributors        Display cred file contributors
   --debug, -d           Debug output
   --delay DELAY, -dl DELAY
                         Specify a delay in milliseconds to avoid 429 status
                         codes default=500
   --dump                Print all of the loaded credentials
   --dryrun              Print urls to be scan, but don't scan them
   --fingerprint, -f     Fingerprint targets, but don't check creds
   --fresh               Flush any previous scans and start fresh
   --log LOG, -l LOG     Write logs to logfile
   --mkcred              Make cred file
   --name NAME, -n NAME  Narrow testing to the supplied credential name
   --noversion           Don't perform a version check
   --proxy PROXY, -p PROXY
                         HTTP(S) Proxy
   --output OUTPUT, -o OUTPUT
                         Name of result file. File extension determines type
                         (csv, html, json).
   --oa                  Output results files in csv, html and json formats
   --protocols PROTOCOLS
                         Comma separated list of protocols to test:
                         http,ssh,ssh_key. Defaults to http.
   --portoverride        Scan all protocols on all specified ports
   --redishost REDISHOST
                         Redis server
   --redisport REDISPORT
                         Redis server
   --resume, -r          Resume previous scan
   --shodan_query SHODAN_QUERY, -q SHODAN_QUERY
                         Shodan query
   --shodan_key SHODAN_KEY, -k SHODAN_KEY
                         Shodan API key
   --ssl                 Force cred to SSL and fall back to non-SSL if an
                         SSLError occurs
   --threads THREADS, -t THREADS
                         Number of threads, default=10
   --timeout TIMEOUT     Timeout in seconds for a request, default=10
   --useragent USERAGENT, -ua USERAGENT
                         User agent string to use
   --validate            Validate creds files
   --verbose, -v         Verbose output
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
