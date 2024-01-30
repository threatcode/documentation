---
Title: wig
Homepage: https://github.com/jekyc/wig
Repository: https://salsa.debian.org/pkg-security-team/wig
Architectures: all
Version: 0.6-2
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### wig
 
  This package contains a web application information gathering tool, which can
  identify numerous Content Management Systems and other administrative
  applications.
   
  The application fingerprinting is based on checksums and string matching of
  known files for different versions of CMSes. This results in a score being
  calculated for each detected CMS and its versions. Each detected CMS is
  displayed along with the most probable version(s) of it. The score calculation
  is based on weights and the amount of "hits" for a given checksum.
   
  wig also tries to guess the operating system on the server based on the
  'server' and 'x-powered-by' headers. A database containing known header values
  for different operating systems is included in wig, which allows wig to guess
  Microsoft Windows versions and Linux distribution and version.
 
 **Installed size:** `6.36 MB`  
 **How to install:** `sudo apt install wig`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 {{< /spoiler >}}
 
 ##### wig
 
 WebApp Information Gatherer
 
 ```
 root@kali:~# wig -h
 usage: wig [-h] [-l INPUT_FILE] [-q] [-n STOP_AFTER] [-a] [-m] [-u] [-d]
            [-t THREADS] [--no_cache_load] [--no_cache_save] [-N] [--verbosity]
            [--proxy PROXY] [-w OUTPUT_FILE]
            [url]
 
 WebApp Information Gatherer
 
 positional arguments:
   url              The url to scan e.g. http://example.com
 
 options:
   -h, --help       show this help message and exit
   -l INPUT_FILE    File with urls, one per line.
   -q               Set wig to not prompt for user input during run
   -n STOP_AFTER    Stop after this amount of CMSs have been detected. Default:
                    1
   -a               Do not stop after the first CMS is detected
   -m               Try harder to find a match without making more requests
   -u               User-agent to use in the requests
   -d               Disable the search for subdomains
   -t THREADS       Number of threads to use
   --no_cache_load  Do not load cached responses
   --no_cache_save  Do not save the cache for later use
   -N               Shortcut for --no_cache_load and --no_cache_save
   --verbosity, -v  Increase verbosity. Use multiple times for more info
   --proxy PROXY    Tunnel through a proxy (format: localhost:8080)
   -w OUTPUT_FILE   File to dump results into (JSON)
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
