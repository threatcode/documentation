---
Title: sslsniff
Homepage: https://moxie.org/software/sslsniff/
Repository: https://salsa.debian.org/pkg-security-team/sslsniff
Architectures: any
Version: 0.8-9
Metapackages: kali-linux-everything kali-linux-large kali-tools-sniffing-spoofing kali-tools-web 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### sslsniff
 
  sslsniff is designed to create man-in-the-middle (MITM) attacks for
  SSL/TLS connections, and dynamically generates certs for the domains
  that are being accessed on the fly. The new certificates are constructed
  in a certificate chain that is signed by any certificate that is
  provided.
  sslsniff also supports other attacks like null-prefix or OCSP attacks to
  achieve silent interceptions of connections when possible.
 
 **Installed size:** `384 KB`  
 **How to install:** `sudo apt install sslsniff`  
 
 {{< spoiler "Dependencies:" >}}
 * libboost-filesystem1.74.0 
 * libboost-thread1.74.0 
 * libc6 
 * libgcc-s1 
 * liblog4cpp5v5 
 * libssl3 
 * libstdc++6 
 {{< /spoiler >}}
 
 ##### sslsniff
 
 SSL/TLS man-in-the-middle attack tool
 
 ```
 root@kali:~# sslsniff -h
 sslsniff: option requires an argument -- 'h'
 Usage: sslsniff [options]
 
 Modes:
 -a	Authority mode.  Specify a certificate that will act as a CA.
 -t	Targeted mode.  Specify a directory full of certificates to target.
 
 Required Options:
 -c <file|directory>	File containing CA cert/key (authority mode) or 
 			directory containing a collection of certs/keys
 			(targeted mode)
 -s <port>		Port to listen on for SSL interception.
 -w <file>		File to log to
 
 Optional Options:
 -u <updateLocation>	Loction of any Firefox XML update files.
 -m <certificateChain>	Location of any intermediary certificates.
 -h <port>		Port to listen on for HTTP interception (required for
 			fingerprinting).
 -f <ff,ie,safari,opera,ios>	Only intercept requests from the specified browser(s).
 -d			Deny OCSP requests for our certificates.
 -p			Only log HTTP POSTs
 -e <url>		Intercept Mozilla Addon Updates
 -j <sha256>		The sha256sum value of the addon to inject
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
