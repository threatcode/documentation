---
Title: spiderfoot
Homepage: https://www.spiderfoot.net
Repository: https://gitlab.com/kalilinux/packages/spiderfoot
Architectures: all
Version: 4.0-0kali3
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-identify 
Icon: images/spiderfoot-logo.svg
PackagesInfo: |
 ### spiderfoot
 
  This package contains an open source intelligence (OSINT) automation tool. Its
  goal is to automate the process of gathering intelligence about a given
  target, which may be an IP address, domain name, hostname, network subnet,
  ASN, e-mail address or person's name.
   
  SpiderFoot can be used offensively, i.e. as part of a black-box penetration
  test to gather information about the target, or defensively to identify what
  information you or your organisation are freely providing for attackers to use
  against you.
 
 **Installed size:** `13.73 MB`  
 **How to install:** `sudo apt install spiderfoot`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-adblockparser
 * python3-bs4
 * python3-cherrypy-cors
 * python3-cherrypy3
 * python3-cryptography
 * python3-dnspython
 * python3-docx
 * python3-exifread
 * python3-gexf
 * python3-ipwhois
 * python3-lxml
 * python3-mako
 * python3-netaddr
 * python3-networkx
 * python3-openpyxl
 * python3-openssl
 * python3-phonenumbers
 * python3-pptx
 * python3-publicsuffixlist
 * python3-pypdf2
 * python3-requests
 * python3-secure 
 * python3-socks
 * python3-whois
 * python3-yaml
 {{< /spoiler >}}
 
 ##### spiderfoot
 
 
 ```
 root@kali:~# spiderfoot -h
 usage: sf.py [-h] [-d] [-l IP:port] [-m mod1,mod2,...] [-M] [-C scanID]
              [-s TARGET] [-t type1,type2,...]
              [-u {all,footprint,investigate,passive}] [-T] [-o {tab,csv,json}]
              [-H] [-n] [-r] [-S LENGTH] [-D DELIMITER] [-f]
              [-F type1,type2,...] [-x] [-q] [-V] [-max-threads MAX_THREADS]
 
 SpiderFoot 4.0.0: Open Source Intelligence Automation.
 
 options:
   -h, --help            show this help message and exit
   -d, --debug           Enable debug output.
   -l IP:port            IP and port to listen on.
   -m mod1,mod2,...      Modules to enable.
   -M, --modules         List available modules.
   -C scanID, --correlate scanID
                         Run correlation rules against a scan ID.
   -s TARGET             Target for the scan.
   -t type1,type2,...    Event types to collect (modules selected
                         automatically).
   -u {all,footprint,investigate,passive}
                         Select modules automatically by use case
   -T, --types           List available event types.
   -o {tab,csv,json}     Output format. Tab is default.
   -H                    Don't print field headers, just data.
   -n                    Strip newlines from data.
   -r                    Include the source data field in tab/csv output.
   -S LENGTH             Maximum data length to display. By default, all data
                         is shown.
   -D DELIMITER          Delimiter to use for CSV output. Default is ,.
   -f                    Filter out other event types that weren't requested
                         with -t.
   -F type1,type2,...    Show only a set of event types, comma-separated.
   -x                    STRICT MODE. Will only enable modules that can
                         directly consume your target, and if -t was specified
                         only those events will be consumed by modules. This
                         overrides -t and -m options.
   -q                    Disable logging. This will also hide errors!
   -V, --version         Display the version of SpiderFoot and exit.
   -max-threads MAX_THREADS
                         Max number of modules to run concurrently.
 ```
 
 - - -
 
 ##### spiderfoot-cli
 
 
 ```
 root@kali:~# spiderfoot-cli -h
 usage: sfcli.py [-h] [-d] [-s URL] [-u USER] [-p PASS] [-P PASSFILE] [-e FILE]
                 [-l FILE] [-n] [-o FILE] [-i] [-q] [-k] [-b]
 
 SpiderFoot: Open Source Intelligence Automation.
 
 options:
   -h, --help   show this help message and exit
   -d, --debug  Enable debug output.
   -s URL       Connect to SpiderFoot server on URL. By default, a connection
                to http://127.0.0.1:5001 will be attempted.
   -u USER      Username to authenticate to SpiderFoot server.
   -p PASS      Password to authenticate to SpiderFoot server. Consider using
                -P PASSFILE instead so that your password isn't visible in your
                shell history or in process lists!
   -P PASSFILE  File containing password to authenticate to SpiderFoot server.
                Ensure permissions on the file are set appropriately!
   -e FILE      Execute commands from FILE.
   -l FILE      Log command history to FILE. By default, history is stored to
                ~/.spiderfoot_history unless disabled with -n.
   -n           Disable history logging.
   -o FILE      Spool commands and output to FILE.
   -i           Allow insecure server connections when using SSL
   -q           Silent output, only errors reported.
   -k           Turn off color-coded output.
   -b, -v       Print the banner w/ version and exit.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
