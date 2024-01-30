---
Title: arjun
Homepage: https://github.com/s0md3v/Arjun
Repository: https://salsa.debian.org/pkg-security-team/arjun
Architectures: all
Version: 2.2.1-2
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### arjun
 
  This package can find query parameters for URL endpoints.
   
  Web applications use parameters (or queries) to accept user input, take the
  following example into consideration.
   
     http://api.example.com/v1/userinfo?id=751634589
   
  This URL seems to load user information for a specific user id, but what if
  there exists a parameter named admin which when set to True makes the endpoint
  provide more information about the user?
  This is what Arjun does, it finds valid HTTP parameters with a huge default
  dictionary of 25,890 parameter names.
  It takes less than 10 seconds to go through this huge list while making just
  50-60 requests to the target.
   
  Some features:
    - Supports GET/POST/POST-JSON/POST-XML requests;
    - Automatically handles rate limits and timeouts;
    - Export results to: BurpSuite, text or JSON file;
    - Import targets from: BurpSuite, text file or a raw request file;
    - Can passively extract parameters from JS or 3 external sources.
   
  Arjun is useful for penetration testing (PENTEST) and network security
  analysis, serving as OSINT.
 
 **Installed size:** `345 KB`  
 **How to install:** `sudo apt install arjun`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-dicttoxml
 * python3-requests
 {{< /spoiler >}}
 
 ##### arjun
 
 HTTP parameter discovery suite
 
 ```
 root@kali:~# arjun -h
 usage: arjun [-h] [-u URL] [-o JSON_FILE] [-oT TEXT_FILE] [-oB [BURP_PORT]]
              [-d DELAY] [-t THREADS] [-w WORDLIST] [-m METHOD]
              [-i [IMPORT_FILE]] [-T TIMEOUT] [-c CHUNKS] [-q]
              [--headers [HEADERS]] [--passive [PASSIVE]] [--stable]
              [--include INCLUDE] [--disable-redirects]
 
 options:
   -h, --help            show this help message and exit
   -u URL                Target URL
   -o JSON_FILE, -oJ JSON_FILE
                         Path for json output file.
   -oT TEXT_FILE         Path for text output file.
   -oB [BURP_PORT]       Port for output to Burp Suite Proxy. Default port is
                         8080.
   -d DELAY              Delay between requests in seconds. (default: 0)
   -t THREADS            Number of concurrent threads. (default: 5)
   -w WORDLIST           Wordlist file path. (default: {arjundir}/db/large.txt)
   -m METHOD             Request method to use: GET/POST/XML/JSON/HEADERS.
                         (default: GET)
   -i [IMPORT_FILE]      Import target URLs from file.
   -T TIMEOUT            HTTP request timeout in seconds. (default: 15)
   -c CHUNKS             Chunk size. The number of parameters to be sent at
                         once
   -q                    Quiet mode. No output.
   --headers [HEADERS]   Add headers. Separate multiple headers with a new
                         line.
   --passive [PASSIVE]   Collect parameter names from passive sources like
                         wayback, commoncrawl and otx.
   --stable              Prefer stability over speed.
   --include INCLUDE     Include this data in every request.
   --disable-redirects   disable redirects
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
