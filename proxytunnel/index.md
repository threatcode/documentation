---
Title: proxytunnel
Homepage: https://proxytunnel.sourceforge.io/
Repository: https://salsa.debian.org/pkg-security-team/proxytunnel
Architectures: any
Version: 1.11.1-1
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-post-exploitation kali-tools-web 
Icon: images/proxytunnel-logo.svg
PackagesInfo: |
 ### proxytunnel
 
  Proxytunnel creates tunnels through HTTP(S) proxies for any TCP based
  protocol. It comes in handy when one sits behind a firewall that allows for
  HTTP(S) traffic only.
   
  The program connects stdin and stdout to an origin server somewhere in the
  Internet through an industry standard HTTP or HTTPS proxy. It was originally
  written as an extension to SSH, to be used to SSH to a box at home.
   
  It's possible to use proxytunnel along with other applications as well,
  by running it from inetd or as daemon listing on a local port to be
  forwarded through the tunnel.
 
 **Installed size:** `97 KB`  
 **How to install:** `sudo apt install proxytunnel`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libssl3 
 {{< /spoiler >}}
 
 ##### proxytunnel
 
 Program to tunnel a connection through a standard HTTPS proxy
 
 ```
 root@kali:~# proxytunnel -h
 proxytunnel 1.11.1 Copyright 2001-2023 Proxytunnel Project
 Usage: proxytunnel [OPTIONS]...
 Build generic tunnels through HTTPS proxies using HTTP authentication
 
 Standard options:
  -i, --inetd                Run from inetd (default: off)
  -a, --standalone=INT       Run as standalone daemon on specified port
  -p, --proxy=STRING         Local proxy host:port combination
  -r, --remproxy=STRING      Remote proxy host:port combination (using 2 proxies)
  -d, --dest=STRING          Destination host:port combination
  -e, --encrypt              SSL encrypt data between local proxy and destination
  -E, --encrypt-proxy        SSL encrypt data between client and local proxy
  -X, --encrypt-remproxy     SSL encrypt data between local and remote proxy
 
 Additional options for specific features:
  -W, --wa-bug-29744         Workaround ASF Bugzilla 29744: if SSL is active stop
                             using it after CONNECT (might not work on all setups; see
                             /usr/share/doc/proxytunnel/README.Debian.gz)
  -B, --buggy-encrypt-proxy  Equivalent to -E -W, provided for backwards
                             compatibility
  -L                         Enforce TLSv1 connection (legacy)
  -T, --no-ssl3              Do not connect using SSLv3
  -z, --no-check-certificate Don't verify server SSL certificate
  -C, --cacert=STRING        Path to trusted CA certificate or directory
  -4, --ipv4                 Enforce IPv4 connection to local proxy
  -6, --ipv6                 Enforce IPv6 connection to local proxy
  -F, --passfile=STRING      File with credentials for proxy authentication
  -P, --proxyauth=STRING     Proxy auth credentials user:pass combination
  -R, --remproxyauth=STRING  Remote proxy auth credentials user:pass combination
  -N, --ntlm                 Use NTLM based authentication
  -t, --domain=STRING        NTLM domain (default: autodetect)
  -H, --header=STRING        Add additional HTTP headers to send to proxy
  -o STRING                  Send custom Host Header
  -x, --proctitle=STRING     Use a different process title
 
 Miscellaneous options:
  -v, --verbose              Turn on verbosity
  -q, --quiet                Suppress messages
  -h, --help                 Print help and exit
  -V, --version              Print version and exit
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
