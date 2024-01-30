---
Title: sslscan
Homepage: https://github.com/rbsec/sslscan
Repository: https://gitlab.com/kalilinux/packages/sslscan
Architectures: any
Version: 2.1.2-0kali1
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-information-gathering kali-tools-vulnerability kali-tools-web 
Icon: images/sslscan-logo.svg
PackagesInfo: |
 ### sslscan
 
  SSLScan queries SSL services, such as HTTPS, in order to determine the ciphers
  that are supported. SSLScan is designed to be easy, lean and fast. The output
  includes preferred ciphers of the SSL service, the certificate and is in text
  and XML formats.
 
 **Installed size:** `4.65 MB`  
 **How to install:** `sudo apt install sslscan`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * zlib1g 
 {{< /spoiler >}}
 
 ##### sslscan
 
 Fast SSL/TLS scanner
 
 ```
 root@kali:~# sslscan -h
                    _
            ___ ___| |___  ___ __ _ _ __
           / __/ __| / __|/ __/ _` | '_ \
           \__ \__ \ \__ \ (_| (_| | | | |
           |___/___/_|___/\___\__,_|_| |_|
 
 
 		2.1.2-static
 		OpenSSL 3.0.12 24 Oct 2023
 
 
 Command:
   sslscan [options] [host:port | host]
 
 Options:
   --targets=<file>     A file containing a list of hosts to check.
                        Hosts can  be supplied  with ports (host:port)
   --sni-name=<name>    Hostname for SNI
   --ipv4, -4           Only use IPv4
   --ipv6, -6           Only use IPv6
 
   --show-certificate   Show full certificate information
   --show-client-cas    Show trusted CAs for TLS client auth
   --no-check-certificate  Don't warn about weak certificate algorithm or keys
   --ocsp               Request OCSP response from server
   --pk=<file>          A file containing the private key or a PKCS#12 file
                        containing a private key/certificate pair
   --pkpass=<password>  The password for the private  key or PKCS#12 file
   --certs=<file>       A file containing PEM/ASN1 formatted client certificates
 
   --ssl2               Only check if SSLv2 is enabled
   --ssl3               Only check if SSLv3 is enabled
   --tls10              Only check TLSv1.0 ciphers
   --tls11              Only check TLSv1.1 ciphers
   --tls12              Only check TLSv1.2 ciphers
   --tls13              Only check TLSv1.3 ciphers
   --tlsall             Only check TLS ciphers (all versions)
   --show-ciphers       Show supported client ciphers
   --show-cipher-ids    Show cipher ids
   --iana-names         Use IANA/RFC cipher names rather than OpenSSL ones
   --show-times         Show handhake times in milliseconds
 
   --no-cipher-details  Disable EC curve names and EDH/RSA key lengths output
   --no-ciphersuites    Do not check for supported ciphersuites
   --no-compression     Do not check for TLS compression (CRIME)
   --no-fallback        Do not check for TLS Fallback SCSV
   --no-groups          Do not enumerate key exchange groups
   --no-heartbleed      Do not check for OpenSSL Heartbleed (CVE-2014-0160)
   --no-renegotiation   Do not check for TLS renegotiation
   --show-sigs          Enumerate signature algorithms
 
   --starttls-ftp       STARTTLS setup for FTP
   --starttls-imap      STARTTLS setup for IMAP
   --starttls-irc       STARTTLS setup for IRC
   --starttls-ldap      STARTTLS setup for LDAP
   --starttls-mysql     STARTTLS setup for MYSQL
   --starttls-pop3      STARTTLS setup for POP3
   --starttls-psql      STARTTLS setup for PostgreSQL
   --starttls-smtp      STARTTLS setup for SMTP
   --starttls-xmpp      STARTTLS setup for XMPP
   --xmpp-server        Use a server-to-server XMPP handshake
   --rdp                Send RDP preamble before starting scan
 
   --bugs               Enable SSL implementation bug work-arounds
   --no-colour          Disable coloured output
   --sleep=<msec>       Pause between connection request. Default is disabled
   --timeout=<sec>      Set socket timeout. Default is 3s
   --connect-timeout=<sec>  Set connect timeout. Default is 75s
   --verbose            Display verbose output
   --version            Display the program version
   --xml=<file>         Output results to an XML file. Use - for STDOUT.
   --help               Display the help text you are now reading
 
 Example:
   sslscan 127.0.0.1
   sslscan [::1]
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
