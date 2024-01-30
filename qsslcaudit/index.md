---
Title: qsslcaudit
Homepage: https://github.com/gremwell/qsslcaudit
Repository: https://gitlab.com/kalilinux/packages/qsslcaudit
Architectures: any
Version: 0.8.3-0kali1
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-information-gathering kali-tools-web 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### qsslcaudit
 
  This tool can be used to determine if an application that uses TLS/SSL for its
  data transfers does this in a secure way.
 
 **Installed size:** `1.08 MB`  
 **How to install:** `sudo apt install qsslcaudit`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libcrypto++8 
 * libgcc-s1 
 * libgnutls30 
 * libqt5core5a 
 * libqt5network5 
 * libstdc++6 
 * libunsafessl1.0.2
 {{< /spoiler >}}
 
 ##### qsslcaudit
 
 
 ```
 root@kali:~# qsslcaudit -h
 Usage: qsslcaudit [options]
 A tool to test SSL clients behavior
 
 SSL client tests:
 	1: (certs) custom certificate trust
 	   certificate trust test with user-supplied certificate
 	2: (certs) self-signed certificate for target domain trust
 	   certificate trust test with self-signed certificate for user-supplied common name
 	3: (certs) self-signed certificate for invalid domain trust
 	   certificate trust test with self-signed certificate for www.example.com
 	4: (certs) custom certificate for target domain trust
 	   certificate trust test with user-supplied common name signed by user-supplied certificate
 	5: (certs) custom certificate for invalid domain trust
 	   certificate trust test with www.example.com common name signed by user-supplied certificate
 	6: (certs) certificate for target domain signed by custom CA trust
 	   certificate trust test with user-supplied common name signed by user-supplied CA certificate
 	7: (certs) certificate for invalid domain signed by custom CA trust
 	   certificate trust test with www.example.com common name signed by user-supplied CA certificate
 	8: (protos) SSLv2 protocol support
 	   test for SSLv2 protocol support
 	9: (protos) SSLv3 protocol support
 	   test for SSLv3 protocol support
 	10: (ciphers) SSLv3 protocol and EXPORT grade ciphers support
 	   test for SSLv3 protocol and EXPORT grade ciphers support
 	11: (ciphers) SSLv3 protocol and LOW grade ciphers support
 	   test for SSLv3 protocol and LOW grade ciphers support
 	12: (ciphers) SSLv3 protocol and MEDIUM grade ciphers support
 	   test for SSLv3 protocol and MEDIUM grade ciphers support
 	13: (protos) TLS 1.0 protocol support
 	   test for TLS 1.0 protocol support
 	14: (ciphers) TLS 1.0 protocol and EXPORT grade ciphers support
 	   test for TLS 1.0 protocol and EXPORT grade ciphers support
 	15: (ciphers) TLS 1.0 protocol and LOW grade ciphers support
 	   test for TLS 1.0 protocol and LOW grade ciphers support
 	16: (ciphers) TLS 1.0 protocol and MEDIUM grade ciphers support
 	   test for TLS 1.0 protocol and MEDIUM grade ciphers support
 	17: (ciphers) TLS 1.1 protocol and EXPORT grade ciphers support
 	   test for TLS 1.1 protocol and EXPORT grade ciphers support
 	18: (ciphers) TLS 1.1 protocol and LOW grade ciphers support
 	   test for TLS 1.1 protocol and LOW grade ciphers support
 	19: (ciphers) TLS 1.1 protocol and MEDIUM grade ciphers support
 	   test for TLS 1.1 protocol and MEDIUM grade ciphers support
 	20: (ciphers) TLS 1.2 protocol and EXPORT grade ciphers support
 	   test for TLS 1.2 protocol and EXPORT grade ciphers support
 	21: (ciphers) TLS 1.2 protocol and LOW grade ciphers support
 	   test for TLS 1.2 protocol and LOW grade ciphers support
 	22: (ciphers) TLS 1.2 protocol and MEDIUM grade ciphers support
 	   test for TLS 1.2 protocol and MEDIUM grade ciphers support
 	23: (ciphers) DTLS 1.0 protocol and EXPORT grade ciphers support
 	   test for DTLS 1.0 protocol and EXPORT grade ciphers support
 	24: (ciphers) DTLS 1.0 protocol and LOW grade ciphers support
 	   test for DTLS 1.0 protocol and LOW grade ciphers support
 	25: (ciphers) DTLS 1.0 protocol and MEDIUM grade ciphers support
 	   test for DTLS 1.0 protocol and MEDIUM grade ciphers support
 	26: (ciphers) DTLS 1.2 protocol and EXPORT grade ciphers support
 	   test for DTLS 1.2 protocol and EXPORT grade ciphers support
 	27: (ciphers) DTLS 1.2 protocol and LOW grade ciphers support
 	   test for DTLS 1.2 protocol and LOW grade ciphers support
 	28: (ciphers) DTLS 1.2 protocol and MEDIUM grade ciphers support
 	   test for DTLS 1.2 protocol and MEDIUM grade ciphers support
 	29: (certs) CVE-2020-0601 ECC cert trust
 	   test for trusting certificate signed by private key with custom curve
 
 
 Options:
   -h, --help                      Displays help on commandline options.
   --help-all                      Displays help including Qt specific options.
   -v, --version                   Displays version information.
   -l, --listen-address <0.0.0.0>  listen on <address>
   -p, --listen-port <8443>        bind to <port>
   --user-cn <example.com>         common name (CN) to suggest to client
   --server <https://example.com>  grab certificate information from <server>
   --user-cert <~/host.cert>       path to file containing custom certificate
                                   (or chain of certificates)
   --user-key <~/host.key>         path to file containing custom private key
   --user-ca-cert <~/ca.cert>      path to file containing custom certificate
                                   usable as CA
   --user-ca-key <~/ca.key>        path to file containing custom private key
                                   for CA certificate
   --selected-tests <1,3,5>        comma-separated list of tests (id) to execute
   --forward <127.0.0.1:6666>      forward connection to upstream proxy
   --show-ciphers                  show ciphers provided by loaded openssl
                                   library
   --starttls <ftp|smtp|xmpp>      exchange specific STARTTLS messages before
                                   starting secure connection
   --loop-tests                    infinitely repeat selected tests (use Ctrl-C
                                   to kill the tool)
   -w, --wait-data-timeout <5000>  wait for incoming data <ms> milliseconds
                                   before emitting error
   --output-xml <qsslcaudit.xml>   save results in XML
   --pid-file </tmp/qs.pid>        create a pidfile once initialized
   --dtls                          use DTLS protocol over UDP
   --double-first-test             execute the first test two times and ignore
                                   its client fingerprint
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
