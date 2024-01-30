---
Title: ivre
Homepage: https://ivre.rocks
Repository: https://gitlab.com/kalilinux/packages/ivre
Architectures: all
Version: 0.9.20-0kali2
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### ivre
 
  This package contains IVRE (Instrument de veille sur les réseaux extérieurs) or
  DRUNK (Dynamic Recon of UNKnown networks), a network recon framework,
  including tools for passive recon (flow analytics relying on Bro, Argus,
  Nfdump, fingerprint analytics based on Bro and p0f and active recon.
   
  IVRE uses Nmap to run scans, can use ZMap as a pre-scanner; IVRE can also
  import XML output from Nmap and Masscan.
 
 **Installed size:** `15.31 MB`  
 **How to install:** `sudo apt install ivre`  
 
 {{< spoiler "Dependencies:" >}}
 * libjs-sphinxdoc
 * python3
 * python3-bottle
 * python3-cryptography
 * python3-dbus
 * python3-future
 * python3-matplotlib
 * python3-mysqldb
 * python3-openssl
 * python3-pil
 * python3-psycopg2
 * python3-pymongo
 * python3-sqlalchemy
 * python3-tinydb
 {{< /spoiler >}}
 
 ##### ivre
 
 
 ```
 root@kali:~# ivre -h
 IVRE - Network recon framework
 Copyright 2011 - 2023 Pierre LALET <pierre@droids-corp.org>
 Version 0.9.20+kali
 
 Python 3.11.6 (main, Oct  8 2023, 05:06:43) [GCC 13.2.0]
 
 Linux kali 6.5.0-kali3-amd64 #1 SMP PREEMPT_DYNAMIC Debian 6.5.6-1kali1 (2023-10-09) x86_64
 
 Dependencies:
     MySQLdb: 1.4.6
     OpenSSL: 23.2.0
     PIL: 10.0.0
     bottle: 0.12.25
     cryptography: 38.0.4
     dbus: 1.3.2
     krbV: *missing*
     matplotlib: 3.6.3
     psycopg2: 2.9.9 (dt dec pq3 ext lo64)
     pycurl: PycURL/7.45.2 libcurl/8.4.0 GnuTLS/3.8.1 zlib/1.2.13 brotli/1.1.0 zstd/1.5.5 libidn2/2.3.4 libpsl/0.21.2 (+libidn2/2.3.4) libssh2/1.11.0 nghttp2/1.58.0 librtmp/2.3 OpenLDAP/2.5.13
     pymongo: 3.11.0
     sqlalchemy: 1.4.47
     tinydb: 3.15.2
 
 usage: ivre [COMMAND]
 
 available commands:
   airodump2db
   arp2db
   auditdom
   db2view
   flow2db
   flowcli
   getmoduli
   getwebdata
   httpd
   ipcalc
   ipdata
   iphost
   ipinfo
   localscan
   macdata
   macinfo
   p0f2db
   passiverecon2db
   passivereconworker
   plotdb
   runscans
   runscansagent
   runscansagentdb
   scan2db
   scancli
   scanstatus
   sort
   version
   view
   weblog2db
   zeek2db
 
 Try ivre help [COMMAND]
 
 ```
 
 - - -
 
 ### ivre-doc
 
  This package contains the documentation for IVRE (Instrument de veille sur les
  réseaux extérieurs) or DRUNK (Dynamic Recon of UNKnown networks), a network
  recon framework, including tools for passive recon (flow analytics relying on
  Bro, Argus, Nfdump, fingerprint analytics based on Bro and p0f and active
  recon.
   
  IVRE uses Nmap to run scans, can use ZMap as a pre-scanner; IVRE
  can also import XML output from Nmap and Masscan.
 
 **Installed size:** `8.55 MB`  
 **How to install:** `sudo apt install ivre-doc`  
 
 {{< spoiler "Dependencies:" >}}
 * libjs-sphinxdoc 
 * sphinx-rtd-theme-common 
 {{< /spoiler >}}
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
