---
Title: eyewitness
Homepage: https://www.christophertruncer.com/eyewitness-triage-tool/
Repository: https://gitlab.com/kalilinux/packages/eyewitness
Architectures: amd64 arm64 i386
Version: 20230525.1+git20230720-0kali2
Metapackages: kali-linux-default kali-linux-everything kali-linux-large kali-tools-information-gathering kali-tools-reporting kali-tools-vulnerability kali-tools-web 
Icon: images/eyewitness-logo.svg
PackagesInfo: |
 ### eyewitness
 
  EyeWitness is designed to take screenshots of websites, provide some server
  header info, and identify default credentials if possible.
   
  Inspiration came from Tim Tomes's PeepingTom Script.
   
  EyeWitness is designed to run on Kali Linux. It will auto detect the file you
  give it with the -f flag as either being a text file with URLs on each new
  line, nmap xml output, or nessus xml output. The -t (timeout) flag is
  completely optional, and lets you provice the max time to wait when trying to
  render and screenshot a web page. The --open flag, which is optional, will open
  the URL in a new tab within Firefox.
 
 **Installed size:** `5.78 MB`  
 **How to install:** `sudo apt install eyewitness`  
 
 {{< spoiler "Dependencies:" >}}
 * links | www-browser
 * python3
 * python3-distutils
 * python3-fuzzywuzzy
 * python3-netaddr
 * python3-pyvirtualdisplay
 * python3-selenium 
 * xvfb
 {{< /spoiler >}}
 
 ##### eyewitness
 
 
 ```
 root@kali:~# eyewitness -h
 ################################################################################
 #                                  EyeWitness                                  #
 ################################################################################
 #           Red Siege Information Security - https://www.redsiege.com           #
 ################################################################################
 
 usage: EyeWitness.py [--web] [-f Filename] [-x Filename.xml]
                      [--single Single URL] [--no-dns] [--timeout Timeout]
                      [--jitter # of Seconds] [--delay # of Seconds]
                      [--threads # of Threads]
                      [--max-retries Max retries on a timeout]
                      [-d Directory Name] [--results Hosts Per Page]
                      [--no-prompt] [--user-agent User Agent]
                      [--difference Difference Threshold]
                      [--proxy-ip 127.0.0.1] [--proxy-port 8080]
                      [--proxy-type socks5] [--show-selenium] [--resolve]
                      [--add-http-ports ADD_HTTP_PORTS]
                      [--add-https-ports ADD_HTTPS_PORTS]
                      [--only-ports ONLY_PORTS] [--prepend-https]
                      [--selenium-log-path SELENIUM_LOG_PATH]
                      [--cookies key1=value1,key2=value2] [--resume ew.db]
 
 EyeWitness is a tool used to capture screenshots from a list of URLs
 
 Protocols:
   --web                 HTTP Screenshot using Selenium
 
 Input Options:
   -f Filename           Line-separated file containing URLs to capture
   -x Filename.xml       Nmap XML or .Nessus file
   --single Single URL   Single URL/Host to capture
   --no-dns              Skip DNS resolution when connecting to websites
 
 Timing Options:
   --timeout Timeout     Maximum number of seconds to wait while requesting a
                         web page (Default: 7)
   --jitter # of Seconds
                         Randomize URLs and add a random delay between requests
   --delay # of Seconds  Delay between the opening of the navigator and taking
                         the screenshot
   --threads # of Threads
                         Number of threads to use while using file based input
   --max-retries Max retries on a timeout
                         Max retries on timeouts
 
 Report Output Options:
   -d Directory Name     Directory name for report output
   --results Hosts Per Page
                         Number of Hosts per page of report
   --no-prompt           Don't prompt to open the report
 
 Web Options:
   --user-agent User Agent
                         User Agent to use for all requests
   --difference Difference Threshold
                         Difference threshold when determining if user agent
                         requests are close "enough" (Default: 50)
   --proxy-ip 127.0.0.1  IP of web proxy to go through
   --proxy-port 8080     Port of web proxy to go through
   --proxy-type socks5   Proxy type (socks5/http)
   --show-selenium       Show display for selenium
   --resolve             Resolve IP/Hostname for targets
   --add-http-ports ADD_HTTP_PORTS
                         Comma-separated additional port(s) to assume are http
                         (e.g. '8018,8028')
   --add-https-ports ADD_HTTPS_PORTS
                         Comma-separated additional port(s) to assume are https
                         (e.g. '8018,8028')
   --only-ports ONLY_PORTS
                         Comma-separated list of exclusive ports to use (e.g.
                         '80,8080')
   --prepend-https       Prepend http:// and https:// to URLs without either
   --selenium-log-path SELENIUM_LOG_PATH
                         Selenium geckodriver log path
   --cookies key1=value1,key2=value2
                         Additional cookies to add to the request
 
 Resume Options:
   --resume ew.db        Path to db file if you want to resume
 ```
 
 - - -
 
 ##### geckodriver
 
 
 ```
 root@kali:~# geckodriver -h
 geckodriver 0.33.0 (a80e5fd61076 2023-04-02 18:31 +0000) 
 WebDriver implementation for Firefox
 
 USAGE:
     geckodriver [OPTIONS]
 
 OPTIONS:
         --allow-hosts <ALLOW_HOSTS>...
             List of hostnames to allow. By default the value of --host is allowed, and in addition
             if that's a well known local address, other variations on well known local addresses are
             allowed. If --allow-hosts is provided only exactly those hosts are allowed.
 
         --allow-origins <ALLOW_ORIGINS>...
             List of request origins to allow. These must be formatted as scheme://host:port. By
             default any request with an origin header is rejected. If --allow-origins is provided
             then only exactly those origins are allowed.
 
         --android-storage <ANDROID_STORAGE>
             Selects storage location to be used for test data (deprecated). [possible values: auto,
             app, internal, sdcard]
 
     -b, --binary <BINARY>
             Path to the Firefox binary
 
         --connect-existing
             Connect to an existing Firefox instance
 
     -h, --help
             Prints this message
 
         --host <HOST>
             Host IP to use for WebDriver server [default: 127.0.0.1]
 
         --jsdebugger
             Attach browser toolbox debugger for Firefox
 
         --log <LEVEL>
             Set Gecko log level [possible values: fatal, error, warn, info, config, debug, trace]
 
         --log-no-truncate
             Disable truncation of long log lines
 
         --marionette-host <HOST>
             Host to use to connect to Gecko [default: 127.0.0.1]
 
         --marionette-port <PORT>
             Port to use to connect to Gecko [default: system-allocated port]
 
     -p, --port <PORT>
             Port to use for WebDriver server [default: 4444]
 
         --profile-root <PROFILE_ROOT>
             Directory in which to create profiles. Defaults to the system temporary directory.
 
     -v
             Log level verbosity (-v for debug and -vv for trace level)
 
     -V, --version
             Prints version and copying information
 
         --websocket-port <PORT>
             Port to use to connect to WebDriver BiDi [default: 9222]
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## eyewitness Usage Examples

Take a screenshot of each of the websites listed in the provided file using headless mode:

```
root@kali:~# cat urls.txt
https://www.kali.org
https://www.kali.org/docs
https://www.kali.org/tools
https://www.exploit-db.com
https://www.offsec.com

root@kali:~# eyewitness -f /root/urls.txt -d screens --headless

################################################################################
#                                  EyeWitness                                  #
################################################################################

Starting Web Requests (5 Hosts)
Attempting to screenshot https://www.kali.org
Attempting to screenshot https://www.kali.org/docs
Attempting to screenshot https://www.kali.org/tools
Attempting to screenshot https://www.exploit-db.com
Attempting to screenshot https://www.offsec.com
Finished in 14.1417660713 seconds

[*] Done! Report written in the /usr/share/eyewitness/screens folder!
Would you like to open the report now? [Y/n] Y
```
