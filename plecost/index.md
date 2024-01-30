---
archived: "true"
Title: plecost
Homepage: https://github.com/iniqua/plecost
Repository: https://gitlab.com/kalilinux/packages/plecost
Architectures: all
Version: 1.1.2-0kali1
Metapackages: kali-linux-everything kali-linux-large kali-tools-web 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### plecost
 
  Wordpress finger printer tool, plecost search and retrieve
  information about the plugins versions installed in
  Wordpress systems. It can analyze a single URL or perform
  an analysis based on the results indexed by Google.
  Additionally displays CVE code associated with each plugin,
  if there.
   
  Plecost retrieves the information contained on Web sites
  supported by Wordpress, and also allows a search on the
  results indexed by Google.
 
 **Installed size:** `5.86 MB`  
 **How to install:** `sudo apt install plecost`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-aiohttp
 * python3-lxml
 * python3-termcolor
 {{< /spoiler >}}
 
 ##### plecost
 
 
 ```
 root@kali:~# plecost -h
 usage: plecost [-h] [-v] [-o OUTPUT_FILE] [--hostname HOSTNAME] [-np] [-nc]
                [-nv] [-f] [-j] [-w WORDLIST] [-l] [-c CONCURRENCY] [-nb]
                [--update-cve] [--update-plugins] [--update-all] [-sp]
                [-vp SHOW_PLUGIN_CVES] [--cve CVE_DETAILS]
                [TARGET ...]
 
 Plecost: Wordpress finger printer tool
 
 positional arguments:
   TARGET
 
 options:
   -h, --help            show this help message and exit
   -v, --verbosity       verbosity level: -v, -vv, -vvv.
   -o OUTPUT_FILE        report file with extension: xml|json
 
 scanner options:
   --hostname HOSTNAME   set custom hostname for the HTTP request
   -np, --no-plugins     do not try to find plugins versions
   -nc, --no-check-wordpress
                         do not check Wordpress connectivity
   -nv, --no-wordpress-version
                         do not check Wordpress version
   -f, --force-scan      force to scan even although not wordpress installation detected
   -j, --jackass-modes   jackass mode: unlimited connections to remote host
 
 wordlist options:
   -w WORDLIST, --wordlist WORDLIST
                         set custom word list. Default 200 most common
   -l, --list-wordlist   list embedded available word list
 
 advanced options:
   -c CONCURRENCY, --concurrency CONCURRENCY
                         number of parallel processes.
   -nb                   don't display banner
 
 update options:
   --update-cve          Update CVE database.
   --update-plugins      Update plugins.
   --update-all          Update CVE, plugins, and core.
 
 database search:
   -sp, --show-plugins   display plugins in database
   -vp SHOW_PLUGIN_CVES, --plugin-cves SHOW_PLUGIN_CVES
                         display CVEs for plugin
   --cve CVE_DETAILS     display details of CVE
 
 Examples:
 
     * Scan target using default 50 most common plugins:
         plecost TARGET
     * Update plugin list
         plecost --update-plugins
     * Update vulnerability database:
         plecost --update-cve
     * List available word lists:
         plecost -l
     * Use embedded 1000 most common word list:
         plecost -w plugin_list_1000.txt TARGET
         or: plecost -w plugin_list_1000 TARGET
     * Scan, using 10 concurrent network connections:
         plecost -w plugin_list_1000.txt --concurrency 10 TARGET
     * Scan using verbose mode and generate xml report:
         plecost -w plugin_list_1000.txt --concurrency 10 -o report.xml TARGET
     * Scan using verbose mode and generate json report:
         plecost -vvv --concurrency 10 -o report.json TARGET
     * Not show banner, and only test wordpress connectivity, without plugin or wordpress testing:
         plecost -v -np -nc -nv TARGET
     * Update CVE database:
         plecost --update-cve
     * Update plugins list:
         plecost --update-plugins
     * List plugins with associated vulnerabilities in local database:
         plecost --show-plugins
     
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## plecost Usage Example

Use 100 plugins (`-n 100`), sleep for 10 seconds between probes (`-s 10`) but no more than 15 (`-M 15`) and use the plugin list (`-i /usr/share/plecost/wp_plugin_list.txt`) to scan the given URL (`192.168.1.202/wordpress`):

```
root@kali:~# plecost -n 100 -s 10 -M 15 -i /usr/share/plecost/wp_plugin_list.txt 192.168.1.202/wordpress
[*] Num of checks set to: 100

-------------------------------------------------
[*] Input plugin list set to: /usr/share/plecost/wp_plugin_list.txt
[*] Min sleep time set to: 10
[*] Max sleep time set to: 15
-------------------------------------------------

==> Results for: 192.168.1.202/wordpress <==

[i] Wordpress version found:  3.9.1
[i] Wordpress last public version: 3.9.1


[*] Search for installed plugins


[i] Plugin found: akismet
    |_Latest version:  2.4.0
    |_ Installed version: 3.0.0
    |_CVE list:
    |___CVE-2009-2334: (http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2009-2334)
    |___CVE-2007-2714: (http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2007-2714)
    |___CVE-2006-4743: (http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2006-4743)
    |___CVE-2009-2334: (http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2009-2334)
    |___CVE-2007-2714: (http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2007-2714)
    |___CVE-2006-4743: (http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2006-4743)
```
