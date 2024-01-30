---
Title: zonedb
Homepage: https://github.com/zonedb/zonedb
Repository: https://gitlab.com/kalilinux/packages/zonedb
Architectures: any all
Version: 1.0.3170-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### golang-github-zonedb-zonedb-dev
 
  This package provides a free, open-source database
  (http://opendatacommons.org/licenses/odbl/1.0/) containing a list and
  associated metadata of public DNS zones
  (http://en.wikipedia.org/wiki/DNS_zone) (domain name extensions). It attempts
  to be exhaustive, including current, retired, and withdrawn top-level domains
  and subdomains.
   
  This package is the library package (source code).
 
 **Installed size:** `793 KB`  
 **How to install:** `sudo apt install golang-github-zonedb-zonedb-dev`  
 
 {{< spoiler "Dependencies:" >}}
 * golang-github-miekg-dns-dev
 * golang-github-puerkitobio-goquery-dev
 * golang-github-wsxiaoys-terminal-dev
 * golang-golang-x-net-dev
 * golang-golang-x-text-dev
 {{< /spoiler >}}
 
 
 - - -
 
 ### zonedb
 
  This package provides a free, open-source database
  (http://opendatacommons.org/licenses/odbl/1.0/) containing a list and
  associated metadata of public DNS zones
  (http://en.wikipedia.org/wiki/DNS_zone) (domain name extensions). It attempts
  to be exhaustive, including current, retired, and withdrawn top-level domains
  and subdomains.
 
 **Installed size:** `14.86 MB`  
 **How to install:** `sudo apt install zonedb`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### zonedb
 
 
 ```
 root@kali:~# zonedb -h
 Usage: zonedb [arguments] <command>
 
 Available arguments: 
   -add-languages string
     	add BCP 47 language tags to zones (comma-delimited)
   -add-locations string
     	add locations to zones (comma-delimited)
   -add-rdap-url string
     	add RDAP URL to zones
   -add-tags string
     	add tags to zones (comma-delimited)
   -c int
     	number of concurrent connections (default 32)
   -dir string
     	data directory (location of zones.txt and metadata dir) (default "/var/lib/zonedb")
   -exclude-tags string
     	exclude working zones with tags (comma-delimited)
   -generate-go
     	generate Go source code to specified directory
   -grep string
     	filter working zones by regular expression across all metadata
   -guess-languages
     	guess BCP 47 languages for zones
   -list
     	list working zones
   -list-locations
     	list locations in working zones
   -list-tags
     	list tags in working zones
   -list-wildcards
     	list zones with wildcarded DNS
   -ps
     	check against Public Suffix List
   -remove-locations string
     	remove locations from zones (comma-delimited)
   -remove-tags string
     	remove tags from zones (comma-delimited)
   -set-info-url string
     	set zone(s) info URLs
   -tags string
     	filter working zones by tags (comma-delimited)
   -tlds
     	work on top-level domains only
   -update
     	update all (root zone, whois, IANA data, IDN tables)
   -update-iana
     	query IANA for metadata
   -update-idn
     	query IANA for IDN tables
   -update-info-url
     	update zone(s) info URLs
   -update-ns
     	update name servers
   -update-rdap
     	query IANA for RDAP URLs
   -update-root
     	retrieve updates to the root zone file
   -update-ruby-whois
     	query Ruby Whois for whois servers
   -update-whois
     	query whois-servers.net for whois servers
   -update-wildcards
     	update wildcard IPs
   -v	enable verbose logging
   -verify-ns
     	verify name servers
   -verify-whois
     	verify whois servers
   -w	write zones.txt and metadata
   -x string
     	filter working zones by regular expression
   -zones string
     	select specific working zones (comma-delimited)
 
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
