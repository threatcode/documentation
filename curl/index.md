---
Title: curl
Homepage: https://curl.se/
Repository: https://salsa.debian.org/debian/curl
Architectures: any all
Version: 8.4.0-2
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-labs kali-linux-large kali-linux-nethunter kali-linux-wsl kali-tools-802-11 kali-tools-bluetooth kali-tools-database kali-tools-detect kali-tools-exploitation kali-tools-forensics kali-tools-fuzzing kali-tools-identify kali-tools-information-gathering kali-tools-passwords kali-tools-post-exploitation kali-tools-protect kali-tools-reporting kali-tools-respond kali-tools-reverse-engineering kali-tools-sdr kali-tools-sniffing-spoofing kali-tools-social-engineering kali-tools-top10 kali-tools-vulnerability kali-tools-web kali-tools-windows-resources kali-tools-wireless 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### curl
 
  curl is a command line tool for transferring data with URL syntax, supporting
  DICT, FILE, FTP, FTPS, GOPHER, HTTP, HTTPS, IMAP, IMAPS, LDAP, LDAPS, POP3,
  POP3S, RTMP, RTSP, SCP, SFTP, SMTP, SMTPS, TELNET and TFTP.
   
  curl supports SSL certificates, HTTP POST, HTTP PUT, FTP uploading, HTTP form
  based upload, proxies, cookies, user+password authentication (Basic, Digest,
  NTLM, Negotiate, kerberos...), file transfer resume, proxy tunneling and a
  busload of other useful tricks.
 
 **Installed size:** `505 KB`  
 **How to install:** `sudo apt install curl`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libcurl4 
 * zlib1g 
 {{< /spoiler >}}
 
 ##### curl
 
 Transfer a URL
 
 ```
 root@kali:~# curl -h
 Usage: curl [options...] <url>
  -d, --data <data>          HTTP POST data
  -f, --fail                 Fail fast with no output on HTTP errors
  -h, --help <category>      Get help for commands
  -i, --include              Include protocol response headers in the output
  -o, --output <file>        Write to file instead of stdout
  -O, --remote-name          Write output to a file named as the remote file
  -s, --silent               Silent mode
  -T, --upload-file <file>   Transfer local FILE to destination
  -u, --user <user:password> Server user and password
  -A, --user-agent <name>    Send User-Agent <name> to server
  -v, --verbose              Make the operation more talkative
  -V, --version              Show version number and quit
 
 This is not the full help, this menu is stripped into categories.
 Use "--help category" to get an overview of all categories.
 For all options use the manual or "--help all".
 ```
 
 - - -
 
 ### libcurl3-gnutls
 
  libcurl is an easy-to-use client-side URL transfer library, supporting DICT,
  FILE, FTP, FTPS, GOPHER, HTTP, HTTPS, IMAP, IMAPS, LDAP, LDAPS, POP3, POP3S,
  RTMP, RTSP, SCP, SFTP, SMTP, SMTPS, TELNET and TFTP.
   
  libcurl supports SSL certificates, HTTP POST, HTTP PUT, FTP uploading, HTTP
  form based upload, proxies, cookies, user+password authentication (Basic,
  Digest, NTLM, Negotiate, Kerberos), file transfer resume, http proxy tunneling
  and more!
   
  libcurl is free, thread-safe, IPv6 compatible, feature rich, well supported,
  fast, thoroughly documented and is already used by many known, big and
  successful companies and numerous applications.
   
  SSL support is provided by GnuTLS.
 
 **Installed size:** `892 KB`  
 **How to install:** `sudo apt install libcurl3-gnutls`  
 
 {{< spoiler "Dependencies:" >}}
 * libbrotli1 
 * libc6 
 * libgnutls30 
 * libgssapi-krb5-2 
 * libidn2-0 
 * libldap-2.5-0 
 * libnettle8
 * libnghttp2-14 
 * libpsl5 
 * librtmp1 
 * libssh2-1 
 * libzstd1 
 * zlib1g 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libcurl4
 
  libcurl is an easy-to-use client-side URL transfer library, supporting DICT,
  FILE, FTP, FTPS, GOPHER, HTTP, HTTPS, IMAP, IMAPS, LDAP, LDAPS, POP3, POP3S,
  RTMP, RTSP, SCP, SFTP, SMTP, SMTPS, TELNET and TFTP.
   
  libcurl supports SSL certificates, HTTP POST, HTTP PUT, FTP uploading, HTTP
  form based upload, proxies, cookies, user+password authentication (Basic,
  Digest, NTLM, Negotiate, Kerberos), file transfer resume, http proxy tunneling
  and more!
   
  libcurl is free, thread-safe, IPv6 compatible, feature rich, well supported,
  fast, thoroughly documented and is already used by many known, big and
  successful companies and numerous applications.
   
  SSL support is provided by OpenSSL.
 
 **Installed size:** `904 KB`  
 **How to install:** `sudo apt install libcurl4`  
 
 {{< spoiler "Dependencies:" >}}
 * libbrotli1 
 * libc6 
 * libgssapi-krb5-2 
 * libidn2-0 
 * libldap-2.5-0 
 * libnghttp2-14 
 * libpsl5 
 * librtmp1 
 * libssh2-1 
 * libssl3 
 * libzstd1 
 * zlib1g 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libcurl4-doc
 
  libcurl is an easy-to-use client-side URL transfer library, supporting DICT,
  FILE, FTP, FTPS, GOPHER, HTTP, HTTPS, IMAP, IMAPS, LDAP, LDAPS, POP3, POP3S,
  RTMP, RTSP, SCP, SFTP, SMTP, SMTPS, TELNET and TFTP.
   
  libcurl supports SSL certificates, HTTP POST, HTTP PUT, FTP uploading, HTTP
  form based upload, proxies, cookies, user+password authentication (Basic,
  Digest, NTLM, Negotiate, Kerberos), file transfer resume, http proxy tunneling
  and more!
   
  libcurl is free, thread-safe, IPv6 compatible, feature rich, well supported,
  fast, thoroughly documented and is already used by many known, big and
  successful companies and numerous applications.
   
  This package provides the documentation files for libcurl.
 
 **Installed size:** `1.99 MB`  
 **How to install:** `sudo apt install libcurl4-doc`  
 
 
 - - -
 
 ### libcurl4-gnutls-dev
 
  libcurl is an easy-to-use client-side URL transfer library, supporting DICT,
  FILE, FTP, FTPS, GOPHER, HTTP, HTTPS, IMAP, IMAPS, LDAP, LDAPS, POP3, POP3S,
  RTMP, RTSP, SCP, SFTP, SMTP, SMTPS, TELNET and TFTP.
   
  libcurl supports SSL certificates, HTTP POST, HTTP PUT, FTP uploading, HTTP
  form based upload, proxies, cookies, user+password authentication (Basic,
  Digest, NTLM, Negotiate, Kerberos), file transfer resume, http proxy tunneling
  and more!
   
  libcurl is free, thread-safe, IPv6 compatible, feature rich, well supported,
  fast, thoroughly documented and is already used by many known, big and
  successful companies and numerous applications.
   
  This package provides the development files (ie. includes, static library,
  manual pages) that allow one to build software which uses libcurl.
   
  SSL support is provided by GnuTLS.
 
 **Installed size:** `1.83 MB`  
 **How to install:** `sudo apt install libcurl4-gnutls-dev`  
 
 {{< spoiler "Dependencies:" >}}
 * libcurl3-gnutls 
 {{< /spoiler >}}
 
 ##### curl-config
 
 Get information about a libcurl installation
 
 ```
 root@kali:~# curl-config --help
 Usage: curl-config [OPTION]
 
 Available values for OPTION include:
 
   --built-shared says 'yes' if libcurl was built shared
   --ca        ca bundle install path
   --cc        compiler
   --cflags    pre-processor and compiler flags
   --checkfor [version] check for (lib)curl of the specified version
   --configure the arguments given to configure when building curl
   --features  newline separated list of enabled features
   --help      display this help and exit
   --libs      library linking information
   --prefix    curl install prefix
   --protocols newline separated list of enabled protocols
   --ssl-backends output the SSL backends libcurl was built to support
   --static-libs static libcurl library linking information
   --version   output version information
   --vernum    output the version information as a number (hexadecimal)
 ```
 
 - - -
 
 ### libcurl4-openssl-dev
 
  libcurl is an easy-to-use client-side URL transfer library, supporting DICT,
  FILE, FTP, FTPS, GOPHER, HTTP, HTTPS, IMAP, IMAPS, LDAP, LDAPS, POP3, POP3S,
  RTMP, RTSP, SCP, SFTP, SMTP, SMTPS, TELNET and TFTP.
   
  libcurl supports SSL certificates, HTTP POST, HTTP PUT, FTP uploading, HTTP
  form based upload, proxies, cookies, user+password authentication (Basic,
  Digest, NTLM, Negotiate, Kerberos), file transfer resume, http proxy tunneling
  and more!
   
  libcurl is free, thread-safe, IPv6 compatible, feature rich, well supported,
  fast, thoroughly documented and is already used by many known, big and
  successful companies and numerous applications.
   
  This package provides the development files (ie. includes, static library,
  manual pages) that allow one to build software which uses libcurl.
   
  SSL support is provided by OpenSSL.
 
 **Installed size:** `1.86 MB`  
 **How to install:** `sudo apt install libcurl4-openssl-dev`  
 
 {{< spoiler "Dependencies:" >}}
 * libcurl4 
 {{< /spoiler >}}
 
 ##### curl-config
 
 Get information about a libcurl installation
 
 ```
 root@kali:~# curl-config --help
 Usage: curl-config [OPTION]
 
 Available values for OPTION include:
 
   --built-shared says 'yes' if libcurl was built shared
   --ca        ca bundle install path
   --cc        compiler
   --cflags    pre-processor and compiler flags
   --checkfor [version] check for (lib)curl of the specified version
   --configure the arguments given to configure when building curl
   --features  newline separated list of enabled features
   --help      display this help and exit
   --libs      library linking information
   --prefix    curl install prefix
   --protocols newline separated list of enabled protocols
   --ssl-backends output the SSL backends libcurl was built to support
   --static-libs static libcurl library linking information
   --version   output version information
   --vernum    output the version information as a number (hexadecimal)
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
