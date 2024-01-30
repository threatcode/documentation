---
Title: bloodhound.py
Homepage: https://github.com/fox-it/BloodHound.py
Repository: https://gitlab.com/kalilinux/packages/bloodhound.py
Architectures: all
Version: 1.6.1-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### bloodhound.py
 
  This package contains a Python based ingestor for BloodHound, based on
  Impacket.
  BloodHound.py currently has the following limitations:
     * Supports most, but not all BloodHound (SharpHound) features. Primary
       missing features are GPO local groups and some differences in session
       resolution between BloodHound and SharpHound.
     * Kerberos authentication support is not yet complete, but can be used from
       the updatedkerberos branch.
   
  This package installs the library for Python 3.
 
 **Installed size:** `331 KB`  
 **How to install:** `sudo apt install bloodhound.py`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-dnspython
 * python3-future
 * python3-impacket
 * python3-ldap3
 * python3-pyasn1 
 {{< /spoiler >}}
 
 ##### bloodhound-python
 
 
 ```
 root@kali:~# bloodhound-python -h
 usage: bloodhound-python [-h] [-c COLLECTIONMETHOD] [-d DOMAIN] [-v]
                          [-u USERNAME] [-p PASSWORD] [-k] [--hashes HASHES]
                          [-no-pass] [-aesKey hex key]
                          [--auth-method {auto,ntlm,kerberos}] [-ns NAMESERVER]
                          [--dns-tcp] [--dns-timeout DNS_TIMEOUT] [-dc HOST]
                          [-gc HOST] [-w WORKERS] [--exclude-dcs]
                          [--disable-pooling] [--disable-autogc] [--zip]
                          [--computerfile COMPUTERFILE] [--cachefile CACHEFILE]
 
 Python based ingestor for BloodHound
 For help or reporting issues, visit https://github.com/Fox-IT/BloodHound.py
 
 options:
   -h, --help            show this help message and exit
   -c COLLECTIONMETHOD, --collectionmethod COLLECTIONMETHOD
                         Which information to collect. Supported: Group,
                         LocalAdmin, Session, Trusts, Default (all previous),
                         DCOnly (no computer connections), DCOM, RDP,PSRemote,
                         LoggedOn, Container, ObjectProps, ACL, All (all except
                         LoggedOn). You can specify more than one by separating
                         them with a comma. (default: Default)
   -d DOMAIN, --domain DOMAIN
                         Domain to query.
   -v                    Enable verbose output
 
 authentication options:
   Specify one or more authentication options. 
   By default Kerberos authentication is used and NTLM is used as fallback. 
   Kerberos tickets are automatically requested if a password or hashes are specified.
 
   -u USERNAME, --username USERNAME
                         Username. Format: username[@domain]; If the domain is
                         unspecified, the current domain is used.
   -p PASSWORD, --password PASSWORD
                         Password
   -k, --kerberos        Use kerberos
   --hashes HASHES       LM:NLTM hashes
   -no-pass              don't ask for password (useful for -k)
   -aesKey hex key       AES key to use for Kerberos Authentication (128 or 256
                         bits)
   --auth-method {auto,ntlm,kerberos}
                         Authentication methods. Force Kerberos or NTLM only or
                         use auto for Kerberos with NTLM fallback
 
 collection options:
   -ns NAMESERVER, --nameserver NAMESERVER
                         Alternative name server to use for queries
   --dns-tcp             Use TCP instead of UDP for DNS queries
   --dns-timeout DNS_TIMEOUT
                         DNS query timeout in seconds (default: 3)
   -dc HOST, --domain-controller HOST
                         Override which DC to query (hostname)
   -gc HOST, --global-catalog HOST
                         Override which GC to query (hostname)
   -w WORKERS, --workers WORKERS
                         Number of workers for computer enumeration (default:
                         10)
   --exclude-dcs         Skip DCs during computer enumeration
   --disable-pooling     Don't use subprocesses for ACL parsing (only for
                         debugging purposes)
   --disable-autogc      Don't automatically select a Global Catalog (use only
                         if it gives errors)
   --zip                 Compress the JSON output files into a zip archive
   --computerfile COMPUTERFILE
                         File containing computer FQDNs to use as allowlist for
                         any computer based methods
   --cachefile CACHEFILE
                         Cache file (experimental)
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
