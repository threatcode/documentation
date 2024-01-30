---
Title: cloud-enum
Homepage: https://github.com/initstring/cloud_enum
Repository: https://salsa.debian.org/pkg-security-team/cloud-enum
Architectures: all
Version: 0.7-3
Metapackages: kali-linux-everything kali-linux-large 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### cloud-enum
 
  cloud_enum enumerates public resources matching user requested keywords in
  public clouds:
   Amazon Web Services:
     Open S3 Buckets
     Protected S3 Buckets
   Microsoft Azure:
     Storage Accounts
     Open Blob Storage Containers
     Hosted Databases
     Virtual Machines
     Web Apps
   Google Cloud Platform:
     Open GCP Buckets
     Protected GCP Buckets
     Google App Engine sites
   
  This program is useful for penetration testing (PENTEST) and network security
  analysis serving as OSINT.
 
 **Installed size:** `79 KB`  
 **How to install:** `sudo apt install cloud-enum`  
 
 {{< spoiler "Dependencies:" >}}
 * bind9-host | host
 * python3
 * python3-dnspython
 * python3-requests
 * python3-requests-futures
 {{< /spoiler >}}
 
 ##### cloud_enum
 
 Enumerates public resources matching user requested keyword
 
 ```
 root@kali:~# cloud_enum -h
 usage: cloud_enum [-h] (-k KEYWORD | -kf KEYFILE) [-m MUTATIONS] [-b BRUTE]
                   [-t THREADS] [-ns NAMESERVER] [-l LOGFILE] [-f FORMAT]
                   [--disable-aws] [--disable-azure] [--disable-gcp] [-qs]
 
 Multi-cloud enumeration utility. All hail OSINT!
 
 options:
   -h, --help            show this help message and exit
   -k KEYWORD, --keyword KEYWORD
                         Keyword. Can use argument multiple times.
   -kf KEYFILE, --keyfile KEYFILE
                         Input file with a single keyword per line.
   -m MUTATIONS, --mutations MUTATIONS
                         Mutations. Default: /usr/lib/cloud-
                         enum/enum_tools/fuzz.txt
   -b BRUTE, --brute BRUTE
                         List to brute-force Azure container names. Default:
                         /usr/lib/cloud-enum/enum_tools/fuzz.txt
   -t THREADS, --threads THREADS
                         Threads for HTTP brute-force. Default = 5
   -ns NAMESERVER, --nameserver NAMESERVER
                         DNS server to use in brute-force.
   -l LOGFILE, --logfile LOGFILE
                         Appends found items to specified file.
   -f FORMAT, --format FORMAT
                         Format for log file (text,json,csv) - default: text
   --disable-aws         Disable Amazon checks.
   --disable-azure       Disable Azure checks.
   --disable-gcp         Disable Google checks.
   -qs, --quickscan      Disable all mutations and second-level scans
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
