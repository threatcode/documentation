---
Title: httpx-toolkit
Homepage: https://github.com/projectdiscovery/httpx
Repository: https://gitlab.com/kalilinux/packages/httpx-toolkit
Architectures: any
Version: 1.1.5-0kali2
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### httpx-toolkit
 
  This package contains the httpX toolkit developed by ProjectDiscovery. It's a
  fast and multi-purpose HTTP toolkit allow to run multiple probers using
  retryablehttp library, it is designed to maintain the result reliability with
  increased threads.
   
  Features
   * Simple and modular code base making it easy to contribute.
   * Fast And fully configurable flags to probe multiple elements.
   * Supports multiple HTTP based probings.
   * Smart auto fallback from https to http as default.
   * Supports hosts, URLs and CIDR as input.
   * Handles edge cases doing retries, backoffs etc for handling WAFs.
   
  This tool is packaged as 'httpx-toolkit' to avoid confusion and conflicts
  with the package python3-httpx that provides a script /usr/bin/httpx.
 
 **Installed size:** `11.47 MB`  
 **How to install:** `sudo apt install httpx-toolkit`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### httpx-toolkit
 
 
 ```
 root@kali:~# httpx-toolkit -h
 httpx is a fast and multi-purpose HTTP toolkit allow to run multiple probers using retryablehttp library.
 
 Usage:
   httpx-toolkit [flags]
 
 Flags:
 INPUT:
    -l, -list string  Input file containing list of hosts to process
    -request string   File containing raw request
 PROBES:
    -sc, -status-code     Display Status Code
    -td, -tech-detect     Display wappalyzer based technology detection
    -cl, -content-length  Display Content-Length
    -server, -web-server  Display Server header
    -ct, -content-type    Display Content-Type header
    -lc, -line-count      Display Response body line count
    -wc, -word-count      Display Response body word count
    -rt, -response-time   Display the response time
    -title                Display page title
    -location             Display Location header
    -method               Display Request method
    -websocket            Display server using websocket
    -ip                   Display Host IP
    -cname                Display Host cname
    -cdn                  Display if CDN in use
    -probe                Display probe status
 MATCHERS:
    -mc, -match-code string         Match response with given status code (-mc 200,302)
    -ml, -match-length string       Match response with given content length (-ml 100,102)
    -ms, -match-string string       Match response with given string
    -mr, -match-regex string        Match response with specific regex
    -er, -extract-regex string      Display response content with matched regex
    -mlc, -match-line-count string  Match Response body line count
    -mwc, -match-word-count string  Match Response body word count
    -mfc, -match-favicon string[]   Match response with specific favicon
 FILTERS:
    -fc, -filter-code string         Filter response with given status code (-fc 403,401)
    -fl, -filter-length string       Filter response with given content length (-fl 23,33)
    -fs, -filter-string string       Filter response with specific string
    -fe, -filter-regex string        Filter response with specific regex
    -flc, -filter-line-count string  Filter Response body line count
    -fwc, -filter-word-count string  Filter Response body word count
    -ffc, -filter-favicon string[]   Filter response with specific favicon
 RATE-LIMIT:
    -t, -threads int      Number of threads (default 50)
    -rl, -rate-limit int  Maximum requests to send per second (default 150)
 MISCELLANEOUS:
    -favicon             Probes for favicon ("favicon.ico" as path) and display phythonic hash
    -tls-grab            Perform TLS(SSL) data grabbing
    -tls-probe           Send HTTP probes on the extracted TLS domains
    -csp-probe           Send HTTP probes on the extracted CSP domains
    -pipeline            HTTP1.1 Pipeline probe
    -http2               HTTP2 probe
    -vhost               VHOST Probe
    -p, -ports string[]  Port to scan (nmap syntax: eg 1,2-10,11)
    -path string         File or comma separated paths to request
    -paths string        File or comma separated paths to request (deprecated)
 OUTPUT:
    -o, -output string                file to write output results
    -sr, -store-response              store http response to output directory
    -srd, -store-response-dir string  store http response to custom directory
    -csv                              store output in CSV format
    -json                             store output in JSONL(ines) format
    -irr, -include-response           include http request/response in JSON output (-json only)
    -include-chain                    include redirect http chain in JSON output (-json only)
    -store-chain                      include http redirect chain in responses (-sr only)
 CONFIGURATIONS:
    -r, -resolvers string[]       List of custom resolvers (file or comma separated)
    -allow string[]               Allowed list of IP/CIDR's to process (file or comma separated)
    -deny string[]                Denied list of IP/CIDR's to process (file or comma separated)
    -random-agent                 Enable Random User-Agent to use (default true)
    -H, -header string[]          Custom Header to send with request
    -http-proxy, -proxy string    HTTP Proxy, eg http://127.0.0.1:8080
    -unsafe                       Send raw requests skipping golang normalization
    -resume                       Resume scan using resume.cfg
    -fr, -follow-redirects        Follow HTTP redirects
    -maxr, -max-redirects int     Max number of redirects to follow per host (default 10)
    -fhr, -follow-host-redirects  Follow redirects on the same host
    -vhost-input                  Get a list of vhosts as input
    -x string                     Request methods to use, use 'all' to probe all HTTP methods
    -body string                  Post body to include in HTTP request
    -s, -stream                   Stream mode - start elaborating input targets without sorting
    -sd, -skip-dedupe             Disable dedupe input items (only used with stream mode)
    -pa, -probe-all-ips           Probe all the ips associated with same host
    -ldp, -leave-default-ports    Leave default HTTP/HTTPS ports (eg. http://host:80 - https//host:443
 DEBUG:
    -silent         Silent mode
    -v, -verbose    Verbose mode
    -version        Display version
    -nc, -no-color  Disable color in output
    -debug          Debug mode
    -debug-req      Show all sent requests
    -debug-resp     Show all received responses
    -stats          Display scan statistic
 OPTIMIZATIONS:
    -nf, -no-fallback                  Display both probbed protocol (HTTPS and HTTP)
    -nfs, -no-fallback-scheme          Probe with input protocol scheme
    -maxhr, -max-host-error int        Max error count per host before skipping remaining path/s (default 30)
    -ec, -exclude-cdn                  Skip full port scans for CDNs (only checks for 80,443)
    -retries int                       Number of retries
    -timeout int                       Timeout in seconds (default 5)
    -rsts, -response-size-to-save int  Max response size to save in bytes (default 2147483647)
    -rstr, -response-size-to-read int  Max response size to read in bytes (default 2147483647)
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
