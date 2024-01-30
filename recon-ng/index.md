---
Title: recon-ng
Homepage: https://github.com/lanmaster53/recon-ng
Repository: https://salsa.debian.org/pkg-security-team/recon-ng
Architectures: all
Version: 5.1.2-1
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-linux-nethunter kali-tools-information-gathering 
Icon: images/recon-ng-logo.svg
PackagesInfo: |
 ### recon-ng
 
  Recon-ng is a full-featured Web Reconnaissance framework written in Python.
  Complete with independent modules, database interaction, built in convenience
  functions, interactive help, and command completion, Recon-ng provides a
  powerful environment in which open source web-based reconnaissance can be
  conducted quickly and thoroughly.
   
  Recon-ng has a look and feel similar to the Metasploit Framework, reducing the
  learning curve for leveraging the framework. However, it is quite different.
  Recon-ng is not intended to compete with existing frameworks, as it is designed
  exclusively for web-based open source reconnaissance. If you want to exploit,
  use the Metasploit Framework. If you want to Social Engineer, use the Social
  Engineer Toolkit.
 
 **Installed size:** `272 KB`  
 **How to install:** `sudo apt install recon-ng`  
 
 {{< spoiler "Dependencies:" >}}
 * libjs-jquery
 * libjs-skeleton
 * node-normalize.css
 * python3
 * python3-dicttoxml
 * python3-dnspython
 * python3-flasgger
 * python3-flask
 * python3-flask-restful
 * python3-lxml
 * python3-mechanize
 * python3-redis
 * python3-requests
 * python3-rq
 * python3-unicodecsv
 * python3-xlsxwriter
 * python3-yaml
 {{< /spoiler >}}
 
 ##### recon-cli
 
 Allow the use of recon-ng from the command line
 
 ```
 root@kali:~# recon-cli -h
 usage: recon-cli [-h] [-w workspace] [-C command] [-c command] [-G]
                  [-g name=value] [-M] [-m module] [-O] [-o name=value] [-x]
                  [--no-version] [--no-analytics] [--no-marketplace]
                  [--stealth] [--version] [--analytics]
 
 recon-cli - Tim Tomes (@lanmaster53)
 
 options:
   -h, --help        show this help message and exit
   -w workspace      load/create a workspace
   -C command        runs a command at the global context
   -c command        runs a command at the module context (pre-run)
   -G                show available global options
   -g name=value     set a global option (can be used more than once)
   -M                show modules
   -m module         specify the module
   -O                show available module options
   -o name=value     set a module option (can be used more than once)
   -x                run the module
   --no-version      disable version check. Already disabled by default in
                     Debian
   --no-analytics    disable analytics reporting. Already disabled by default
                     in Debian
   --no-marketplace  disable remote module management
   --stealth         disable all passive requests (--no-*)
   --version         displays the current version
   --analytics       enable analytics reporting. Send analytics to google
 ```
 
 - - -
 
 ##### recon-ng
 
 Web Reconnaissance framework
 
 ```
 root@kali:~# recon-ng -h
 usage: recon-ng [-h] [-w workspace] [-r filename] [--no-version]
                 [--no-analytics] [--no-marketplace] [--stealth] [--accessible]
                 [--version]
 
 recon-ng - Tim Tomes (@lanmaster53)
 
 options:
   -h, --help        show this help message and exit
   -w workspace      load/create a workspace
   -r filename       load commands from a resource file
   --no-version      disable version check. Already disabled by default in
                     Debian
   --no-analytics    disable analytics reporting. Already disabled by default
                     in Debian
   --no-marketplace  disable remote module management
   --stealth         disable all passive requests (--no-*)
   --accessible      Use accessible outputs when available
   --version         displays the current version
 ```
 
 - - -
 
 ##### recon-web
 
 Web-based user interface for Recon-ng.
 
 ```
 root@kali:~# recon-web -h
 *************************************************************************
  * Welcome to Recon-web, the analytics and reporting engine for Recon-ng!
  * This is a web-based user interface. Open the URL below in your browser to begin.
  * Recon-web includes the Recon-API, which can be accessed via the `/api/` URL.
 *************************************************************************
 [*] Marketplace disabled.
 [*] Version check disabled.
  * Workspace initialized: default
 usage: recon-web [-h] [--host HOST] [--port PORT]
 
 options:
   -h, --help   show this help message and exit
   --host HOST  IP address to listen on
   --port PORT  port to bind the web server to
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## recon-ng Usage Example

Search for results on xssed.com (`use recon/domains-vulnerabilities/xssed`) for the target domain (`set SOURCE cisco.com`):

```
root@kali:~# recon-ng

    _/_/_/    _/_/_/_/    _/_/_/    _/_/_/    _/      _/            _/      _/    _/_/_/
   _/    _/  _/        _/        _/      _/  _/_/    _/            _/_/    _/  _/
  _/_/_/    _/_/_/    _/        _/      _/  _/  _/  _/  _/_/_/_/  _/  _/  _/  _/  _/_/_/
 _/    _/  _/        _/        _/      _/  _/    _/_/            _/    _/_/  _/      _/
_/    _/  _/_/_/_/    _/_/_/    _/_/_/    _/      _/            _/      _/    _/_/_/


                                          /\
                                         / \\ /\
        Sponsored by...           /\  /\/  \\V  \/\
                                 / \\/ // \\\\\ \\ \/\
                                // // BLACK HILLS \/ \\
                               www.blackhillsinfosec.com

                      [recon-ng v4.9.4, Tim Tomes (@LaNMaSteR53)]

[76] Recon modules
[8]  Reporting modules
[2]  Import modules
[2]  Exploitation modules
[2]  Discovery modules

[recon-ng][default] > use recon/domains-vulnerabilities/xssed
[recon-ng][default][xssed] > set SOURCE cisco.com
SOURCE => cisco.com
[recon-ng][default][xssed] > run

---------
CISCO.COM
---------
[*] Category: Redirect
[*] Example: http://www.cisco.com/survey/exit.html?http://xssed.com/
[*] Host: www.cisco.com
[*] Publish_Date: 2012-02-16 00:00:00
[*] Reference: http://xssed.com/mirror/76478/
[*] Status: unfixed
[*] --------------------------------------------------
[*] Category: XSS
[*] Example: http://developer.cisco.com/web/webdialer/wikidocs?p_p_id=1_WAR_wikinavigationportlet_INSTANCE_veD7&p<br>_p_lifecycle=0&p_p_state=normal&p_p_mode=view&p_p_col_id=column-1&p_p_col_count=1&p_r_p_185834411_no<br>deId=803209&p_r_p_185834411_title=%22%3E%3Ch1%3ECross-Site%20Scripting%20@matiaslonigro%3C/h1%3E%3Cs<br>cript%3Ealert%28/xss/%29%3C/script%3E
[*] Host: developer.cisco.com
[*] Publish_Date: 2012-02-13 00:00:00
[*] Reference: http://xssed.com/mirror/76294/
[*] Status: unfixed
[...]
```
