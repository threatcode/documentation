---
Title: certgraph
Homepage: https://github.com/lanrat/certgraph
Repository: https://gitlab.com/kalilinux/packages/certgraph
Architectures: any
Version: 20180911-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### certgraph
 
  This package contains a tool to crawl the graph of certificate Alternate
  Names. CertGraph crawls SSL certificates creating a directed graph where each
  domain is a node and the certificate alternative names for that domain's
  certificate are the edges to other domain nodes. New domains are printed as
  they are found. In Detailed mode upon completion the Graph's adjacency list is
  printed.
   
  Crawling defaults to collecting certificate by connecting over TCP, however
  there are multiple drivers that can search Certificate Transparency logs.
   
  This tool was designed to be used for host name enumeration via SSL
  certificates, but it can also show you a "chain" of trust between domains and
  the certificates that re-used between them.
 
 **Installed size:** `6.37 MB`  
 **How to install:** `sudo apt install certgraph`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### certgraph
 
 
 ```
 root@kali:~# certgraph -h
 Usage of certgraph: [OPTION]... HOST...
 	https://github.com/lanrat/certgraph
 OPTIONS:
   -cdn
     	include certificates from CDNs
   -ct-expired
     	include expired certificates in certificate transparency search
   -ct-subdomains
     	include sub-domains in certificate transparency search
   -depth uint
     	maximum BFS depth to go (default 5)
   -details
     	print details about the domains crawled
   -dns
     	check for DNS records to determine if domain is registered
   -driver string
     	driver to use [crtsh, google, http, smtp] (default "http")
   -json
     	print the graph as json, can be used for graph in web UI
   -parallel uint
     	number of certificates to retrieve in parallel (default 10)
   -sanscap int
     	maximum number of uniq TLD+1 domains in certificate to include, 0 has no limit (default 80)
   -save string
     	save certs to folder in PEM format
   -timeout uint
     	tcp timeout in seconds (default 10)
   -tldplus1
     	for every domain found, add tldPlus1 of the domain's parent
   -updatepsl
     	Update the default Public Suffix List
   -verbose
     	verbose logging
   -version
     	print version and exit
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
