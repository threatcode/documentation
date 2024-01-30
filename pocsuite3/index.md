---
Title: pocsuite3
Homepage: https://pocsuite.org
Repository: https://salsa.debian.org/pkg-security-team/pocsuite3
Architectures: all
Version: 1.9.6-1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### pocsuite3
 
  Pocsuite3 is an open-sourced remote vulnerability testing and proof-of-concept
  development framework developed by the Knownsec 404 Team. It comes with a
  powerful proof-of-concept engine, many nice features for the ultimate
  penetration testers and security researchers.
 
 **Installed size:** `662 KB`  
 **How to install:** `sudo apt install pocsuite3`  
 
 {{< spoiler "Dependencies:" >}}
 * binutils
 * nasm
 * python3
 * python3-chardet
 * python3-colorama
 * python3-colorlog
 * python3-fake-factory
 * python3-openssl
 * python3-prettytable
 * python3-pycryptodome
 * python3-requests
 * python3-requests-toolbelt
 * python3-scapy
 * python3-socks
 * python3-termcolor
 * python3-urllib3
 {{< /spoiler >}}
 
 ##### poc-console
 
 Console mode of pocsuite3.
 
 ```
 root@kali:~# man poc-console
 POC-CONSOLE(1)              General Commands Manual             POC-CONSOLE(1)
 
 NAME
        poc-console - console mode of pocsuite3.
 
 Legal Disclaimer
        poc-console is part of pocsuite3. Usage of pocsuite3 for attacking tar-
        gets  without  prior mutual consent is illegal.  pocsuite3 is for secu-
        rity testing purposes only.
 
 SYNOPSIS
        poc-console
 
 DESCRIPTION
        poc-console is the console mode of pocsuite3.  pocsuite3  is  an  open-
        sourced  remote  vulnerability testing and proof-of-concept development
        framework developed by the Knownsec 404 Team. It comes with a  powerful
        proof-of-concept  engine,  many nice features for the ultimate penetra-
        tion testers and security researchers.
 
 OPTIONS
        poc-console do not have command line options. To see a list  of  avail-
        able commands, enter help at the console prompt.
 
 SEE ALSO
        The full documentation for pocsuite3 is maintained at:
        https://github.com/knownsec/pocsuite3/blob/master/docs/USAGE.md
 
 VERSION
        This manual page documents pocsuite3 version 1.9.6
 
 AUTHOR
        (c) 2014-2022 by Knownsec 404 Team
        <404-team@knownsec.com>
 
        This  program  is  free software; you may redistribute and/or modify it
        under the terms of the GNU General Public License as published  by  the
        Free  Software Foundation; Version 2 with the clarifications and excep-
        tions described below. This guarantees your right to use,  modify,  and
        redistribute this software under certain conditions. If you wish to em-
        bed pocsuite3 technology into proprietary software, we sell alternative
        licenses (contact 404-team@knownsec.com).
 
        Manual page started by Tian Qiao <abcnsxyz@gmail.com>
 
 Manual page for poc-console        July 2022                    POC-CONSOLE(1)
 ```
 
 - - -
 
 ##### pocsuite
 
 Open-sourced remote vulnerability testing framework.
 
 ```
 root@kali:~# pocsuite -h
 
 ,------.                        ,--. ,--.       ,----.   {1.9.6-1e20bb5}
 |  .--. ',---. ,---.,---.,--.,--`--,-'  '-.,---.'.-.  |
 |  '--' | .-. | .--(  .-'|  ||  ,--'-.  .-| .-. : .' <
 |  | --'' '-' \ `--.-'  `'  ''  |  | |  | \   --/'-'  |
 `--'     `---' `---`----' `----'`--' `--'  `----`----'   https://pocsuite.org
 usage: pocsuite [options]
 
 options:
   -h, --help            show this help message and exit
   --version             Show program's version number and exit
   --update              Update Pocsuite3
   -n, --new             Create a PoC template
   -v {0,1,2,3,4,5,6}    Verbosity level: 0-6 (default 1)
 
 Target:
   At least one of these options has to be provided to define the target(s)
 
   -u URL [URL ...], --url URL [URL ...]
                         Target URL/CIDR (e.g.
                         "http://www.site.com/vuln.php?id=1")
   -f URL_FILE, --file URL_FILE
                         Scan multiple targets given in a textual file (one per
                         line)
   -p PORTS, --ports PORTS
                         add additional port to each target (e.g. 8080,8443)
   -r POC [POC ...]      Load PoC file from local or remote from seebug website
   -k POC_KEYWORD        Filter PoC by keyword, e.g. ecshop
   -c CONFIGFILE         Load options from a configuration INI file
 
 Mode:
   Pocsuite running mode options
 
   --verify              Run poc with verify mode
   --attack              Run poc with attack mode
   --shell               Run poc with shell mode
 
 Request:
   Network request options
 
   --cookie COOKIE       HTTP Cookie header value
   --host HOST           HTTP Host header value
   --referer REFERER     HTTP Referer header value
   --user-agent AGENT    HTTP User-Agent header value (default random)
   --proxy PROXY         Use a proxy to connect to the target URL
                         (protocol://host:port)
   --proxy-cred PROXY_CRED
                         Proxy authentication credentials (name:password)
   --timeout TIMEOUT     Seconds to wait before timeout connection (default 10)
   --retry RETRY         Time out retrials times (default 0)
   --delay DELAY         Delay between two request of one thread
   --headers HEADERS     Extra headers (e.g. "key1: value1\nkey2: value2")
 
 Account:
   Account options
 
   --ceye-token CEYE_TOKEN
                         CEye token
   --oob-server OOB_SERVER
                         Interactsh server to use (default "interact.sh")
   --oob-token OOB_TOKEN
                         Authentication token to connect protected interactsh
                         server
   --seebug-token SEEBUG_TOKEN
                         Seebug token
   --zoomeye-token ZOOMEYE_TOKEN
                         ZoomEye token
   --shodan-token SHODAN_TOKEN
                         Shodan token
   --fofa-user FOFA_USER
                         Fofa user
   --fofa-token FOFA_TOKEN
                         Fofa token
   --quake-token QUAKE_TOKEN
                         Quake token
   --hunter-token HUNTER_TOKEN
                         Hunter token
   --censys-uid CENSYS_UID
                         Censys uid
   --censys-secret CENSYS_SECRET
                         Censys secret
 
 Modules:
   Modules options
 
   --dork DORK           Zoomeye dork used for search
   --dork-zoomeye DORK_ZOOMEYE
                         Zoomeye dork used for search
   --dork-shodan DORK_SHODAN
                         Shodan dork used for search
   --dork-fofa DORK_FOFA
                         Fofa dork used for search
   --dork-quake DORK_QUAKE
                         Quake dork used for search
   --dork-hunter DORK_HUNTER
                         Hunter dork used for search
   --dork-censys DORK_CENSYS
                         Censys dork used for search
   --max-page MAX_PAGE   Max page used in search API
   --search-type SEARCH_TYPE
                         search type used in search API, web or host
   --vul-keyword VUL_KEYWORD
                         Seebug keyword used for search
   --ssv-id SSVID        Seebug SSVID number for target PoC
   --lhost CONNECT_BACK_HOST
                         Connect back host for target PoC in shell mode
   --lport CONNECT_BACK_PORT
                         Connect back port for target PoC in shell mode
   --tls                 Enable TLS listener in shell mode
   --comparison          Compare popular web search engines
   --dork-b64            Whether dork is in base64 format
 
 Optimization:
   Optimization options
 
   -o OUTPUT_PATH, --output OUTPUT_PATH
                         Output file to write (JSON Lines format)
   --plugins PLUGINS     Load plugins to execute
   --pocs-path POCS_PATH
                         User defined poc scripts path
   --threads THREADS     Max number of concurrent network requests (default
                         150)
   --batch BATCH         Automatically choose defaut choice without asking
   --requires            Check install_requires
   --quiet               Activate quiet mode, working without logger
   --ppt                 Hiden sensitive information when published to the
                         network
   --pcap                use scapy capture flow
   --rule                export suricata rules, default export reqeust and
                         response
   --rule-req            only export request rule
   --rule-filename RULE_FILENAME
                         Specify the name of the export rule file
 
 Poc options:
   definition options for PoC
 
   --options             Show all definition options
 
 [*] shutting down at 10:13:21
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
