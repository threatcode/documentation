---
Title: mitmproxy
Homepage: https://mitmproxy.org
Repository: https://gitlab.com/kalilinux/packages/mitmproxy
Architectures: all
Version: 10.1.5-0kali1
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-linux-nethunter kali-tools-sniffing-spoofing kali-tools-web 
Icon: images/mitmproxy-logo.svg
PackagesInfo: |
 ### mitmproxy
 
  mitmproxy is an interactive man-in-the-middle proxy for HTTP and HTTPS. It
  provides a console interface that allows traffic flows to be inspected and
  edited on the fly.
   
  Also shipped is mitmdump, the command-line version of mitmproxy, with
  the same functionality but without the frills. Think tcpdump for
  HTTP.
   
  Features:
   - intercept and modify HTTP and HTTPS requests and responses and modify them
     on the fly
   - save HTTP conversations for later replay and analysis
   - replay the client-side of an HTTP conversation
   - reverse proxy mode to forward traffic to a specified server
   - transparent proxy mode on OSX and Linux
   - make scripted changes to HTTP traffic using Python
   - SSL/TLS certificates for interception are generated on the fly
   - ...
   
  This package contains the python-pathod module (previously
  provided by other source package). The python-netlib module was also included
  but it has been dropped by upstream in version 1.0.
 
 **Installed size:** `3.75 MB`  
 **How to install:** `sudo apt install mitmproxy`  
 
 {{< spoiler "Dependencies:" >}}
 * dpkg 
 * fonts-font-awesome 
 * python3
 * python3-aioquic
 * python3-asgiref 
 * python3-brotli 
 * python3-certifi 
 * python3-cryptography 
 * python3-flask 
 * python3-h11
 * python3-h2 
 * python3-hyperframe 
 * python3-kaitaistruct 
 * python3-ldap3 
 * python3-mitmproxy-rs
 * python3-mitmproxy-wireguard
 * python3-msgpack 
 * python3-openssl 
 * python3-passlib 
 * python3-pkg-resources
 * python3-protobuf 
 * python3-publicsuffix2 
 * python3-pyparsing 
 * python3-pyperclip 
 * python3-ruamel.yaml 
 * python3-sortedcontainers 
 * python3-tornado 
 * python3-typing-extensions | python3-supported-min 
 * python3-urwid
 * python3-wsproto 
 * python3-zstandard
 {{< /spoiler >}}
 
 ##### mitmdump
 
 
 ```
 root@kali:~# mitmdump -h
 usage: mitmdump [options] [filter]
 
 positional arguments:
   filter_args           Filter expression, equivalent to setting both the
                         view_filter and save_stream_filter options.
 
 options:
   -h, --help            show this help message and exit
   --version             show version number and exit
   --options             Show all options and their default values
   --commands            Show all commands and their signatures
   --set option[=value]  Set an option. When the value is omitted, booleans are
                         set to true, strings and integers are set to None (if
                         permitted), and sequences are emptied. Boolean values
                         can be true, false or toggle. Sequences are set using
                         multiple invocations to set for the same option.
   -q, --quiet           Quiet.
   -v, --verbose         Increase log verbosity.
   --mode MODE, -m MODE  The proxy server type(s) to spawn. Can be passed
                         multiple times. Mitmproxy supports "regular" (HTTP),
                         "transparent", "socks5", "reverse:SPEC",
                         "upstream:SPEC", and "wireguard[:PATH]" proxy servers.
                         For reverse and upstream proxy modes, SPEC is host
                         specification in the form of "http[s]://host[:port]".
                         For WireGuard mode, PATH may point to a file
                         containing key material. If no such file exists, it
                         will be created on startup. You may append
                         `@listen_port` or `@listen_host:listen_port` to
                         override `listen_host` or `listen_port` for a specific
                         proxy mode. Features such as client playback will use
                         the first mode to determine which upstream server to
                         use. May be passed multiple times.
   --no-anticache
   --anticache           Strip out request headers that might cause the server
                         to return 304-not-modified.
   --no-showhost
   --showhost            Use the Host header to construct URLs for display.
   --rfile PATH, -r PATH
                         Read flows from file.
   --scripts SCRIPT, -s SCRIPT
                         Execute a script. May be passed multiple times.
   --stickycookie FILTER
                         Set sticky cookie filter. Matched against requests.
   --stickyauth FILTER   Set sticky auth filter. Matched against requests.
   --save-stream-file PATH, -w PATH
                         Stream flows to file as they arrive. Prefix path with
                         + to append. The full path can use python strftime()
                         formating, missing directories are created as needed.
                         A new file is opened every time the formatted string
                         changes.
   --no-anticomp
   --anticomp            Try to convince servers to send us un-compressed data.
   --flow-detail LEVEL   The display detail level for flows in mitmdump: 0
                         (quiet) to 4 (very verbose). 0: no output 1: shortened
                         request URL with response status code 2: full request
                         URL with response status code and HTTP headers 3: 2 +
                         truncated response content, content of WebSocket and
                         TCP messages 4: 3 + nothing is truncated
 
 Proxy Options:
   --listen-host HOST    Address to bind proxy server(s) to (may be overridden
                         for individual modes, see `mode`).
   --listen-port PORT, -p PORT
                         Port to bind proxy server(s) to (may be overridden for
                         individual modes, see `mode`). By default, the port is
                         mode-specific. The default regular HTTP proxy spawns
                         on port 8080.
   --no-server, -n
   --server              Start a proxy server. Enabled by default.
   --ignore-hosts HOST   Ignore host and forward all traffic without processing
                         it. In transparent mode, it is recommended to use an
                         IP address (range), not the hostname. In regular mode,
                         only SSL traffic is ignored and the hostname should be
                         used. The supplied value is interpreted as a regular
                         expression and matched on the ip or the hostname. May
                         be passed multiple times.
   --allow-hosts HOST    Opposite of --ignore-hosts. May be passed multiple
                         times.
   --tcp-hosts HOST      Generic TCP SSL proxy mode for all hosts that match
                         the pattern. Similar to --ignore-hosts, but SSL
                         connections are intercepted. The communication
                         contents are printed to the log in verbose mode. May
                         be passed multiple times.
   --upstream-auth USER:PASS
                         Add HTTP Basic authentication to upstream proxy and
                         reverse proxy requests. Format: username:password.
   --proxyauth SPEC      Require proxy authentication. Format: "username:pass",
                         "any" to accept any user/pass combination, "@path" to
                         use an Apache htpasswd file, or "ldap[s]:url_server_ld
                         ap[:port]:dn_auth:password:dn_subtree[?search_filter_k
                         ey=...]" for LDAP authentication.
   --no-rawtcp
   --rawtcp              Enable/disable raw TCP connections. TCP connections
                         are enabled by default.
   --no-http2
   --http2               Enable/disable HTTP/2 support. HTTP/2 support is
                         enabled by default.
 
 SSL:
   --certs SPEC          SSL certificates of the form "[domain=]path". The
                         domain may include a wildcard, and is equal to "*" if
                         not specified. The file at path is a certificate in
                         PEM format. If a private key is included in the PEM,
                         it is used, else the default key in the conf dir is
                         used. The PEM file should contain the full certificate
                         chain, with the leaf certificate as the first entry.
                         May be passed multiple times.
   --cert-passphrase PASS
                         Passphrase for decrypting the private key provided in
                         the --cert option. Note that passing cert_passphrase
                         on the command line makes your passphrase visible in
                         your system's process list. Specify it in config.yaml
                         to avoid this.
   --no-ssl-insecure
   --ssl-insecure, -k    Do not verify upstream server SSL/TLS certificates.
 
 Client Replay:
   --client-replay PATH, -C PATH
                         Replay client requests from a saved file. May be
                         passed multiple times.
 
 Server Replay:
   --server-replay PATH, -S PATH
                         Replay server responses from a saved file. May be
                         passed multiple times.
   --no-server-replay-kill-extra
   --server-replay-kill-extra
                         Kill extra requests during replay (for which no
                         replayable response was found).[Deprecated, prefer to
                         use server_replay_extra='kill']
   --server-replay-extra {forward,kill,204,400,404,500}
                         Behaviour for extra requests during replay for which
                         no replayable response was found. Setting a numeric
                         string value will return an empty HTTP response with
                         the respective status code.
   --no-server-replay-reuse
   --server-replay-reuse
                         Don't remove flows from server replay state after use.
                         This makes it possible to replay same response
                         multiple times.
   --no-server-replay-refresh
   --server-replay-refresh
                         Refresh server replay responses by adjusting date,
                         expires and last-modified headers, as well as
                         adjusting cookie expiration.
 
 Map Remote:
   --map-remote PATTERN, -M PATTERN
                         Map remote resources to another remote URL using a
                         pattern of the form "[/flow-filter]/url-
                         regex/replacement", where the separator can be any
                         character. May be passed multiple times.
 
 Map Local:
   --map-local PATTERN   Map remote resources to a local file using a pattern
                         of the form "[/flow-filter]/url-regex/file-or-
                         directory-path", where the separator can be any
                         character. May be passed multiple times.
 
 Modify Body:
   --modify-body PATTERN, -B PATTERN
                         Replacement pattern of the form "[/flow-
                         filter]/regex/[@]replacement", where the separator can
                         be any character. The @ allows to provide a file path
                         that is used to read the replacement string. May be
                         passed multiple times.
 
 Modify Headers:
   --modify-headers PATTERN, -H PATTERN
                         Header modify pattern of the form "[/flow-
                         filter]/header-name/[@]header-value", where the
                         separator can be any character. The @ allows to
                         provide a file path that is used to read the header
                         value string. An empty header-value removes existing
                         header-name headers. May be passed multiple times.
 
 ```
 
 - - -
 
 ##### mitmproxy
 
 
 ```
 root@kali:~# mitmproxy -h
 usage: mitmproxy [options]
 
 options:
   -h, --help            show this help message and exit
   --version             show version number and exit
   --options             Show all options and their default values
   --commands            Show all commands and their signatures
   --set option[=value]  Set an option. When the value is omitted, booleans are
                         set to true, strings and integers are set to None (if
                         permitted), and sequences are emptied. Boolean values
                         can be true, false or toggle. Sequences are set using
                         multiple invocations to set for the same option.
   -q, --quiet           Quiet.
   -v, --verbose         Increase log verbosity.
   --mode MODE, -m MODE  The proxy server type(s) to spawn. Can be passed
                         multiple times. Mitmproxy supports "regular" (HTTP),
                         "transparent", "socks5", "reverse:SPEC",
                         "upstream:SPEC", and "wireguard[:PATH]" proxy servers.
                         For reverse and upstream proxy modes, SPEC is host
                         specification in the form of "http[s]://host[:port]".
                         For WireGuard mode, PATH may point to a file
                         containing key material. If no such file exists, it
                         will be created on startup. You may append
                         `@listen_port` or `@listen_host:listen_port` to
                         override `listen_host` or `listen_port` for a specific
                         proxy mode. Features such as client playback will use
                         the first mode to determine which upstream server to
                         use. May be passed multiple times.
   --no-anticache
   --anticache           Strip out request headers that might cause the server
                         to return 304-not-modified.
   --no-showhost
   --showhost            Use the Host header to construct URLs for display.
   --rfile PATH, -r PATH
                         Read flows from file.
   --scripts SCRIPT, -s SCRIPT
                         Execute a script. May be passed multiple times.
   --stickycookie FILTER
                         Set sticky cookie filter. Matched against requests.
   --stickyauth FILTER   Set sticky auth filter. Matched against requests.
   --save-stream-file PATH, -w PATH
                         Stream flows to file as they arrive. Prefix path with
                         + to append. The full path can use python strftime()
                         formating, missing directories are created as needed.
                         A new file is opened every time the formatted string
                         changes.
   --no-anticomp
   --anticomp            Try to convince servers to send us un-compressed data.
   --console-layout {horizontal,single,vertical}
                         Console layout.
   --no-console-layout-headers
   --console-layout-headers
                         Show layout component headers
 
 Proxy Options:
   --listen-host HOST    Address to bind proxy server(s) to (may be overridden
                         for individual modes, see `mode`).
   --listen-port PORT, -p PORT
                         Port to bind proxy server(s) to (may be overridden for
                         individual modes, see `mode`). By default, the port is
                         mode-specific. The default regular HTTP proxy spawns
                         on port 8080.
   --no-server, -n
   --server              Start a proxy server. Enabled by default.
   --ignore-hosts HOST   Ignore host and forward all traffic without processing
                         it. In transparent mode, it is recommended to use an
                         IP address (range), not the hostname. In regular mode,
                         only SSL traffic is ignored and the hostname should be
                         used. The supplied value is interpreted as a regular
                         expression and matched on the ip or the hostname. May
                         be passed multiple times.
   --allow-hosts HOST    Opposite of --ignore-hosts. May be passed multiple
                         times.
   --tcp-hosts HOST      Generic TCP SSL proxy mode for all hosts that match
                         the pattern. Similar to --ignore-hosts, but SSL
                         connections are intercepted. The communication
                         contents are printed to the log in verbose mode. May
                         be passed multiple times.
   --upstream-auth USER:PASS
                         Add HTTP Basic authentication to upstream proxy and
                         reverse proxy requests. Format: username:password.
   --proxyauth SPEC      Require proxy authentication. Format: "username:pass",
                         "any" to accept any user/pass combination, "@path" to
                         use an Apache htpasswd file, or "ldap[s]:url_server_ld
                         ap[:port]:dn_auth:password:dn_subtree[?search_filter_k
                         ey=...]" for LDAP authentication.
   --no-rawtcp
   --rawtcp              Enable/disable raw TCP connections. TCP connections
                         are enabled by default.
   --no-http2
   --http2               Enable/disable HTTP/2 support. HTTP/2 support is
                         enabled by default.
 
 SSL:
   --certs SPEC          SSL certificates of the form "[domain=]path". The
                         domain may include a wildcard, and is equal to "*" if
                         not specified. The file at path is a certificate in
                         PEM format. If a private key is included in the PEM,
                         it is used, else the default key in the conf dir is
                         used. The PEM file should contain the full certificate
                         chain, with the leaf certificate as the first entry.
                         May be passed multiple times.
   --cert-passphrase PASS
                         Passphrase for decrypting the private key provided in
                         the --cert option. Note that passing cert_passphrase
                         on the command line makes your passphrase visible in
                         your system's process list. Specify it in config.yaml
                         to avoid this.
   --no-ssl-insecure
   --ssl-insecure, -k    Do not verify upstream server SSL/TLS certificates.
 
 Client Replay:
   --client-replay PATH, -C PATH
                         Replay client requests from a saved file. May be
                         passed multiple times.
 
 Server Replay:
   --server-replay PATH, -S PATH
                         Replay server responses from a saved file. May be
                         passed multiple times.
   --no-server-replay-kill-extra
   --server-replay-kill-extra
                         Kill extra requests during replay (for which no
                         replayable response was found).[Deprecated, prefer to
                         use server_replay_extra='kill']
   --server-replay-extra {forward,kill,204,400,404,500}
                         Behaviour for extra requests during replay for which
                         no replayable response was found. Setting a numeric
                         string value will return an empty HTTP response with
                         the respective status code.
   --no-server-replay-reuse
   --server-replay-reuse
                         Don't remove flows from server replay state after use.
                         This makes it possible to replay same response
                         multiple times.
   --no-server-replay-refresh
   --server-replay-refresh
                         Refresh server replay responses by adjusting date,
                         expires and last-modified headers, as well as
                         adjusting cookie expiration.
 
 Map Remote:
   --map-remote PATTERN, -M PATTERN
                         Map remote resources to another remote URL using a
                         pattern of the form "[/flow-filter]/url-
                         regex/replacement", where the separator can be any
                         character. May be passed multiple times.
 
 Map Local:
   --map-local PATTERN   Map remote resources to a local file using a pattern
                         of the form "[/flow-filter]/url-regex/file-or-
                         directory-path", where the separator can be any
                         character. May be passed multiple times.
 
 Modify Body:
   --modify-body PATTERN, -B PATTERN
                         Replacement pattern of the form "[/flow-
                         filter]/regex/[@]replacement", where the separator can
                         be any character. The @ allows to provide a file path
                         that is used to read the replacement string. May be
                         passed multiple times.
 
 Modify Headers:
   --modify-headers PATTERN, -H PATTERN
                         Header modify pattern of the form "[/flow-
                         filter]/header-name/[@]header-value", where the
                         separator can be any character. The @ allows to
                         provide a file path that is used to read the header
                         value string. An empty header-value removes existing
                         header-name headers. May be passed multiple times.
 
 Filters:
   See help in mitmproxy for filter expression syntax.
 
   --intercept FILTER    Intercept filter expression.
   --view-filter FILTER  Limit the view to matching flows.
 
 ```
 
 - - -
 
 ##### mitmweb
 
 
 ```
 root@kali:~# mitmweb -h
 usage: mitmweb [options]
 
 options:
   -h, --help            show this help message and exit
   --version             show version number and exit
   --options             Show all options and their default values
   --commands            Show all commands and their signatures
   --set option[=value]  Set an option. When the value is omitted, booleans are
                         set to true, strings and integers are set to None (if
                         permitted), and sequences are emptied. Boolean values
                         can be true, false or toggle. Sequences are set using
                         multiple invocations to set for the same option.
   -q, --quiet           Quiet.
   -v, --verbose         Increase log verbosity.
   --mode MODE, -m MODE  The proxy server type(s) to spawn. Can be passed
                         multiple times. Mitmproxy supports "regular" (HTTP),
                         "transparent", "socks5", "reverse:SPEC",
                         "upstream:SPEC", and "wireguard[:PATH]" proxy servers.
                         For reverse and upstream proxy modes, SPEC is host
                         specification in the form of "http[s]://host[:port]".
                         For WireGuard mode, PATH may point to a file
                         containing key material. If no such file exists, it
                         will be created on startup. You may append
                         `@listen_port` or `@listen_host:listen_port` to
                         override `listen_host` or `listen_port` for a specific
                         proxy mode. Features such as client playback will use
                         the first mode to determine which upstream server to
                         use. May be passed multiple times.
   --no-anticache
   --anticache           Strip out request headers that might cause the server
                         to return 304-not-modified.
   --no-showhost
   --showhost            Use the Host header to construct URLs for display.
   --rfile PATH, -r PATH
                         Read flows from file.
   --scripts SCRIPT, -s SCRIPT
                         Execute a script. May be passed multiple times.
   --stickycookie FILTER
                         Set sticky cookie filter. Matched against requests.
   --stickyauth FILTER   Set sticky auth filter. Matched against requests.
   --save-stream-file PATH, -w PATH
                         Stream flows to file as they arrive. Prefix path with
                         + to append. The full path can use python strftime()
                         formating, missing directories are created as needed.
                         A new file is opened every time the formatted string
                         changes.
   --no-anticomp
   --anticomp            Try to convince servers to send us un-compressed data.
 
 Mitmweb:
   --no-web-open-browser
   --web-open-browser    Start a browser.
   --web-port PORT       Web UI port.
   --web-host HOST       Web UI host.
 
 Proxy Options:
   --listen-host HOST    Address to bind proxy server(s) to (may be overridden
                         for individual modes, see `mode`).
   --listen-port PORT, -p PORT
                         Port to bind proxy server(s) to (may be overridden for
                         individual modes, see `mode`). By default, the port is
                         mode-specific. The default regular HTTP proxy spawns
                         on port 8080.
   --no-server, -n
   --server              Start a proxy server. Enabled by default.
   --ignore-hosts HOST   Ignore host and forward all traffic without processing
                         it. In transparent mode, it is recommended to use an
                         IP address (range), not the hostname. In regular mode,
                         only SSL traffic is ignored and the hostname should be
                         used. The supplied value is interpreted as a regular
                         expression and matched on the ip or the hostname. May
                         be passed multiple times.
   --allow-hosts HOST    Opposite of --ignore-hosts. May be passed multiple
                         times.
   --tcp-hosts HOST      Generic TCP SSL proxy mode for all hosts that match
                         the pattern. Similar to --ignore-hosts, but SSL
                         connections are intercepted. The communication
                         contents are printed to the log in verbose mode. May
                         be passed multiple times.
   --upstream-auth USER:PASS
                         Add HTTP Basic authentication to upstream proxy and
                         reverse proxy requests. Format: username:password.
   --proxyauth SPEC      Require proxy authentication. Format: "username:pass",
                         "any" to accept any user/pass combination, "@path" to
                         use an Apache htpasswd file, or "ldap[s]:url_server_ld
                         ap[:port]:dn_auth:password:dn_subtree[?search_filter_k
                         ey=...]" for LDAP authentication.
   --no-rawtcp
   --rawtcp              Enable/disable raw TCP connections. TCP connections
                         are enabled by default.
   --no-http2
   --http2               Enable/disable HTTP/2 support. HTTP/2 support is
                         enabled by default.
 
 SSL:
   --certs SPEC          SSL certificates of the form "[domain=]path". The
                         domain may include a wildcard, and is equal to "*" if
                         not specified. The file at path is a certificate in
                         PEM format. If a private key is included in the PEM,
                         it is used, else the default key in the conf dir is
                         used. The PEM file should contain the full certificate
                         chain, with the leaf certificate as the first entry.
                         May be passed multiple times.
   --cert-passphrase PASS
                         Passphrase for decrypting the private key provided in
                         the --cert option. Note that passing cert_passphrase
                         on the command line makes your passphrase visible in
                         your system's process list. Specify it in config.yaml
                         to avoid this.
   --no-ssl-insecure
   --ssl-insecure, -k    Do not verify upstream server SSL/TLS certificates.
 
 Client Replay:
   --client-replay PATH, -C PATH
                         Replay client requests from a saved file. May be
                         passed multiple times.
 
 Server Replay:
   --server-replay PATH, -S PATH
                         Replay server responses from a saved file. May be
                         passed multiple times.
   --no-server-replay-kill-extra
   --server-replay-kill-extra
                         Kill extra requests during replay (for which no
                         replayable response was found).[Deprecated, prefer to
                         use server_replay_extra='kill']
   --server-replay-extra {forward,kill,204,400,404,500}
                         Behaviour for extra requests during replay for which
                         no replayable response was found. Setting a numeric
                         string value will return an empty HTTP response with
                         the respective status code.
   --no-server-replay-reuse
   --server-replay-reuse
                         Don't remove flows from server replay state after use.
                         This makes it possible to replay same response
                         multiple times.
   --no-server-replay-refresh
   --server-replay-refresh
                         Refresh server replay responses by adjusting date,
                         expires and last-modified headers, as well as
                         adjusting cookie expiration.
 
 Map Remote:
   --map-remote PATTERN, -M PATTERN
                         Map remote resources to another remote URL using a
                         pattern of the form "[/flow-filter]/url-
                         regex/replacement", where the separator can be any
                         character. May be passed multiple times.
 
 Map Local:
   --map-local PATTERN   Map remote resources to a local file using a pattern
                         of the form "[/flow-filter]/url-regex/file-or-
                         directory-path", where the separator can be any
                         character. May be passed multiple times.
 
 Modify Body:
   --modify-body PATTERN, -B PATTERN
                         Replacement pattern of the form "[/flow-
                         filter]/regex/[@]replacement", where the separator can
                         be any character. The @ allows to provide a file path
                         that is used to read the replacement string. May be
                         passed multiple times.
 
 Modify Headers:
   --modify-headers PATTERN, -H PATTERN
                         Header modify pattern of the form "[/flow-
                         filter]/header-name/[@]header-value", where the
                         separator can be any character. The @ allows to
                         provide a file path that is used to read the header
                         value string. An empty header-value removes existing
                         header-name headers. May be passed multiple times.
 
 Filters:
   See help in mitmproxy for filter expression syntax.
 
   --intercept FILTER    Intercept filter expression.
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## mitmproxy Usage Example

Run mitmproxy listening (p) on port2139.

```
root@kali:~# mitmproxy -p 2139
```
