---
Title: proxify
Homepage: https://github.com/projectdiscovery/proxify
Repository: https://gitlab.com/kalilinux/packages/proxify
Architectures: any
Version: 0.0.5-0kali3
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### proxify
 
  This package contains a Swiss Army Knife Proxy for rapid deployments. It
  supports multiple operations such as request/response dump, filtering and
  manipulation via DSL language, upstream HTTP/Socks5 proxy. Additionally a
  replay utility allows to import the dumped traffic (request/responses with
  correct domain name) into burp or any other proxy by simply setting the
  upstream proxy to proxify.
   
  Features
   * Intercept / Manipulate HTTP/HTTPS & NON-HTTTP traffic
   * Invisible & Thick clients traffic proxy support
   * TLS MITM support with client/server certificates
   * HTTP and SOCKS5 support for upstream proxy
   * Traffic Match/Filter and Replace DSL support
   * Full traffic dump to file (request/responses)
   * Native embedded DNS server
   * Plugin Support to decode specific protocols (e.g XMPP/SMTP/FTP/SSH/)
   * Proxify Traffic replay in Burp
 
 **Installed size:** `35.08 MB`  
 **How to install:** `sudo apt install proxify`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### mitmrelay
 
 
 ```
 root@kali:~# mitmrelay -h
 Usage of mitmrelay:
   -client-cert string
     	Relay => Server Cert File
   -client-key string
     	Relay => Server Key File
   -dns-addr string
     	Listen DNS Ip and port (ip:port) (default ":5353")
   -dns-mapping string
     	DNS A mapping (eg domain:ip,domain:ip,..)
   -http-addr string
     	HTTP Server Listen Address (default "127.0.0.1:49999")
   -output string
     	Output Folder (default "logs/")
   -protocol string
     	tcp or udp (default "tcp")
   -proxy-addr string
     	HTTP Proxy Address
   -relay value
     	listen_ip:listen_port => destination_ip:destination_port
   -request-match-replace-dsl string
     	Request Match-Replace DSL
   -resolver-addr string
     	Listen DNS Ip and port (ip:port)
   -response-match-replace-dsl string
     	Request Match-Replace DSL
   -server-cert string
     	Client => Relay Cert File
   -server-key string
     	Client => Relay Key File
   -timeout int
     	Connection Timeout In Seconds (default 180)
   -tls-client
     	Relay => Server should use tls
   -tls-server
     	Client => Relay should use tls
 ```
 
 - - -
 
 ##### proxify
 
 
 ```
 root@kali:~# proxify -h
 Swiss Army Knife Proxy for rapid deployments. Supports multiple operations such as request/response dump,filtering and manipulation via DSL language, upstream HTTP/Socks5 proxy
 
 Usage:
   proxify [flags]
 
 Flags:
 OUTPUT:
    -o, -output string  Output Directory to store HTTP proxy logs (default "logs")
    -dump-req           Dump only HTTP requests to output file
    -dump-resp          Dump only HTTP responses to output file
 FILTER:
    -req-fd, -request-dsl string                   Request Filter DSL
    -resp-fd, -response-dsl string                 Response Filter DSL
    -req-mrd, -request-match-replace-dsl string    Request Match-Replace DSL
    -resp-mrd, -response-match-replace-dsl string  Response Match-Replace DSL
 NETWORK:
    -ha, -http-addr string    Listening HTTP IP and Port address (ip:port) (default "127.0.0.1:8888")
    -sa, -socks-addr string   Listening SOCKS IP and Port address (ip:port) (default "127.0.0.1:10080")
    -da, -dns-addr string     Listening DNS IP and Port address (ip:port)
    -dm, -dns-mapping string  Domain to IP DNS mapping (eg domain:ip,domain:ip,..)
    -r, -resolver string      Custom DNS resolvers to use (ip:port)
 PROXY:
    -hp, -http-proxy string    Upstream HTTP Proxies (eg http://proxy-ip:proxy-port
    -sp, -socks5-proxy string  Upstream SOCKS5 Proxies (eg socks5://proxy-ip:proxy-port)
    -c int                     Number of requests before switching to the next upstream proxy (default 1)
 EXPORT:
    -elastic-address string    elasticsearch address (ip:port)
    -elastic-ssl               enable elasticsearch ssl
    -elastic-ssl-verification  enable elasticsearch ssl verification
    -elastic-username string   elasticsearch username
    -elastic-password string   elasticsearch password
    -elastic-index string      elasticsearch index name (default "proxify")
    -kafka-address string      address of kafka broker (ip:port)
    -kafka-topic string        kafka topic to publish messages on (default "proxify")
 CONFIGURATION:
    -config string        Directory for storing program information (default "/root/.config/proxify")
    -cert-cache-size int  Number of certificates to cache (default 256)
    -allow string         Allowed list of IP/CIDR's to be proxied
    -deny string          Denied list of IP/CIDR's to be proxied
 DEBUG:
    -silent         Silent
    -nc, -no-color  No Color (default true)
    -version        Version
    -v, -verbose    Verbose
 ```
 
 - - -
 
 ##### replay-proxify
 
 
 ```
 root@kali:~# replay-proxify -h
 Usage of replay-proxify:
   -burp-addr string
     	Burp HTTP Address (default "http://127.0.0.1:8080")
   -dns-addr string
     	DNS UDP Server Listen Address (default ":10000")
   -http-addr string
     	HTTP Server Listen Address (default ":80")
   -output string
     	Output Folder (default "db/")
   -proxy-addr string
     	HTTP Proxy Server Listen Address (default ":8081")
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
