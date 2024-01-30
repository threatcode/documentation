---
Title: wpscan
Homepage: https://wpscan.com/wordpress-security-scanner
Repository: https://gitlab.com/kalilinux/packages/wpscan
Architectures: all
Version: 3.8.25-0kali1
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-information-gathering kali-tools-vulnerability kali-tools-web 
Icon: images/wpscan-logo.svg
PackagesInfo: |
 ### wpscan
 
  WPScan scans remote WordPress installations to find security issues.
 
 **Installed size:** `394 KB`  
 **How to install:** `sudo apt install wpscan`  
 
 {{< spoiler "Dependencies:" >}}
 * curl
 * ruby
 * ruby-activesupport
 * ruby-cms-scanner 
 * ruby-yajl
 {{< /spoiler >}}
 
 ##### wpscan
 
 WordPress Security Scanner
 
 ```
 root@kali:~# wpscan -h
 _______________________________________________________________
          __          _______   _____
          \ \        / /  __ \ / ____|
           \ \  /\  / /| |__) | (___   ___  __ _ _ __ ®
            \ \/  \/ / |  ___/ \___ \ / __|/ _` | '_ \
             \  /\  /  | |     ____) | (__| (_| | | | |
              \/  \/   |_|    |_____/ \___|\__,_|_| |_|
 
          WordPress Security Scanner by the WPScan Team
                          Version 3.8.25
                                
        @_WPScan_, @ethicalhack3r, @erwan_lr, @firefart
 _______________________________________________________________
 
 Usage: wpscan [options]
         --url URL                                 The URL of the blog to scan
                                                   Allowed Protocols: http, https
                                                   Default Protocol if none provided: http
                                                   This option is mandatory unless update or help or hh or version is/are supplied
     -h, --help                                    Display the simple help and exit
         --hh                                      Display the full help and exit
         --version                                 Display the version and exit
     -v, --verbose                                 Verbose mode
         --[no-]banner                             Whether or not to display the banner
                                                   Default: true
     -o, --output FILE                             Output to FILE
     -f, --format FORMAT                           Output results in the format supplied
                                                   Available choices: cli-no-colour, cli-no-color, json, cli
         --detection-mode MODE                     Default: mixed
                                                   Available choices: mixed, passive, aggressive
         --user-agent, --ua VALUE
         --random-user-agent, --rua                Use a random user-agent for each scan
         --http-auth login:password
     -t, --max-threads VALUE                       The max threads to use
                                                   Default: 5
         --throttle MilliSeconds                   Milliseconds to wait before doing another web request. If used, the max threads will be set to 1.
         --request-timeout SECONDS                 The request timeout in seconds
                                                   Default: 60
         --connect-timeout SECONDS                 The connection timeout in seconds
                                                   Default: 30
         --disable-tls-checks                      Disables SSL/TLS certificate verification, and downgrade to TLS1.0+ (requires cURL 7.66 for the latter)
         --proxy protocol://IP:port                Supported protocols depend on the cURL installed
         --proxy-auth login:password
         --cookie-string COOKIE                    Cookie string to use in requests, format: cookie1=value1[; cookie2=value2]
         --cookie-jar FILE-PATH                    File to read and write cookies
                                                   Default: /tmp/wpscan/cookie_jar.txt
         --force                                   Do not check if the target is running WordPress or returns a 403
         --[no-]update                             Whether or not to update the Database
         --api-token TOKEN                         The WPScan API Token to display vulnerability data, available at https://wpscan.com/profile
         --wp-content-dir DIR                      The wp-content directory if custom or not detected, such as "wp-content"
         --wp-plugins-dir DIR                      The plugins directory if custom or not detected, such as "wp-content/plugins"
     -e, --enumerate [OPTS]                        Enumeration Process
                                                   Available Choices:
                                                    vp   Vulnerable plugins
                                                    ap   All plugins
                                                    p    Popular plugins
                                                    vt   Vulnerable themes
                                                    at   All themes
                                                    t    Popular themes
                                                    tt   Timthumbs
                                                    cb   Config backups
                                                    dbe  Db exports
                                                    u    User IDs range. e.g: u1-5
                                                         Range separator to use: '-'
                                                         Value if no argument supplied: 1-10
                                                    m    Media IDs range. e.g m1-15
                                                         Note: Permalink setting must be set to "Plain" for those to be detected
                                                         Range separator to use: '-'
                                                         Value if no argument supplied: 1-100
                                                   Separator to use between the values: ','
                                                   Default: All Plugins, Config Backups
                                                   Value if no argument supplied: vp,vt,tt,cb,dbe,u,m
                                                   Incompatible choices (only one of each group/s can be used):
                                                    - vp, ap, p
                                                    - vt, at, t
         --exclude-content-based REGEXP_OR_STRING  Exclude all responses matching the Regexp (case insensitive) during parts of the enumeration.
                                                   Both the headers and body are checked. Regexp delimiters are not required.
         --plugins-detection MODE                  Use the supplied mode to enumerate Plugins.
                                                   Default: passive
                                                   Available choices: mixed, passive, aggressive
         --plugins-version-detection MODE          Use the supplied mode to check plugins' versions.
                                                   Default: mixed
                                                   Available choices: mixed, passive, aggressive
         --exclude-usernames REGEXP_OR_STRING      Exclude usernames matching the Regexp/string (case insensitive). Regexp delimiters are not required.
     -P, --passwords FILE-PATH                     List of passwords to use during the password attack.
                                                   If no --username/s option supplied, user enumeration will be run.
     -U, --usernames LIST                          List of usernames to use during the password attack.
                                                   Examples: 'a1', 'a1,a2,a3', '/tmp/a.txt'
         --multicall-max-passwords MAX_PWD         Maximum number of passwords to send by request with XMLRPC multicall
                                                   Default: 500
         --password-attack ATTACK                  Force the supplied attack to be used rather than automatically determining one.
                                                   Multicall will only work against WP < 4.4
                                                   Available choices: wp-login, xmlrpc, xmlrpc-multicall
         --login-uri URI                           The URI of the login page if different from /wp-login.php
         --stealthy                                Alias for --random-user-agent --detection-mode passive --plugins-version-detection passive
 
 [!] To see full list of options use --hh.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## wpscan Usage Examples

Scan a target WordPress URL and enumerate any plugins that are installed:

```
root@kali:~# wpscan --url http://wordpress.local --enumerate p
_______________________________________________________________
        __          _______   _____
        \ \        / /  __ \ / ____|
         \ \  /\  / /| |__) | (___   ___  __ _ _ __
          \ \/  \/ / |  ___/ \___ \ / __|/ _` | '_ \
           \  /\  /  | |     ____) | (__| (_| | | | |
            \/  \/   |_|    |_____/ \___|\__,_|_| |_|

        WordPress Security Scanner by the WPScan Team
                       Version 2.6
          Sponsored by Sucuri - https://sucuri.net
   @_WPScan_, @ethicalhack3r, @erwan_lr, pvdl, @_FireFart_
_______________________________________________________________

[+] URL: http://wordpress.local/
[+] Started: Mon Jan 12 14:07:40 2015

[+] robots.txt available under: 'http://wordpress.local/robots.txt'
[+] Interesting entry from robots.txt: http://wordpress.local/search
[+] Interesting entry from robots.txt: http://wordpress.local/support/search.php
[+] Interesting entry from robots.txt: http://wordpress.local/extend/plugins/search.php
[+] Interesting entry from robots.txt: http://wordpress.local/plugins/search.php
[+] Interesting entry from robots.txt: http://wordpress.local/extend/themes/search.php
[+] Interesting entry from robots.txt: http://wordpress.local/themes/search.php
[+] Interesting entry from robots.txt: http://wordpress.local/support/rss
[+] Interesting entry from robots.txt: http://wordpress.local/archive/
[+] Interesting header: SERVER: nginx
[+] Interesting header: X-FRAME-OPTIONS: SAMEORIGIN
[+] Interesting header: X-NC: HIT lax 249
[+] XML-RPC Interface available under: http://wordpress.local/xmlrpc.php

[+] WordPress version 4.2-alpha-31168 identified from rss generator

[+] Enumerating installed plugins  ...

   Time: 00:00:35 <======================================================> (2166 / 2166) 100.00% Time: 00:00:35

[+] We found 2166 plugins:
[...]
```
