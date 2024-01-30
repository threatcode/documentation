---
Title: python-ldapdomaindump
Homepage: https://github.com/dirkjanm/ldapdomaindump
Repository: https://salsa.debian.org/python-team/packages/python-ldapdomaindump
Architectures: all
Version: 0.9.4-1
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-exploitation kali-tools-forensics kali-tools-information-gathering kali-tools-passwords kali-tools-respond kali-tools-social-engineering kali-tools-top10 kali-tools-vulnerability kali-tools-web 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### python3-ldapdomaindump
 
  This package contains an Active Directory information dumper via LDAP. In an
  Active Directory domain, a lot of interesting information can be retrieved via
  LDAP by any authenticated user (or machine). This makes LDAP an interesting
  protocol for gathering information in the recon phase of a pentest of an
  internal network. A problem is that data from LDAP often is not available in
  an easy to read format.
   
  ldapdomaindump is a tool which aims to solve this problem, by collecting and
  parsing information available via LDAP and outputting it in a human readable
  HTML format, as well as machine readable json and csv/tsv/greppable files.
   
  This package installs the library for Python 3.
 
 **Installed size:** `85 KB`  
 **How to install:** `sudo apt install python3-ldapdomaindump`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-dnspython
 * python3-future
 * python3-ldap3
 {{< /spoiler >}}
 
 ##### ldapdomaindump
 
 
 ```
 root@kali:~# ldapdomaindump -h
 usage: ldapdomaindump [-h] [-u USERNAME] [-p PASSWORD] [-at {NTLM,SIMPLE}]
                       [-o DIRECTORY] [--no-html] [--no-json] [--no-grep]
                       [--grouped-json] [-d DELIMITER] [-r] [-n DNS_SERVER]
                       [-m]
                       HOSTNAME
 
 Domain information dumper via LDAP. Dumps users/computers/groups and
 OS/membership information to HTML/JSON/greppable output.
 
 Required options:
   HOSTNAME              Hostname/ip or ldap://host:port connection string to
                         connect to (use ldaps:// to use SSL)
 
 Main options:
   -h, --help            show this help message and exit
   -u USERNAME, --user USERNAME
                         DOMAIN\username for authentication, leave empty for
                         anonymous authentication
   -p PASSWORD, --password PASSWORD
                         Password or LM:NTLM hash, will prompt if not specified
   -at {NTLM,SIMPLE}, --authtype {NTLM,SIMPLE}
                         Authentication type (NTLM or SIMPLE, default: NTLM)
 
 Output options:
   -o DIRECTORY, --outdir DIRECTORY
                         Directory in which the dump will be saved (default:
                         current)
   --no-html             Disable HTML output
   --no-json             Disable JSON output
   --no-grep             Disable Greppable output
   --grouped-json        Also write json files for grouped files (default:
                         disabled)
   -d DELIMITER, --delimiter DELIMITER
                         Field delimiter for greppable output (default: tab)
 
 Misc options:
   -r, --resolve         Resolve computer hostnames (might take a while and
                         cause high traffic on large networks)
   -n DNS_SERVER, --dns-server DNS_SERVER
                         Use custom DNS resolver instead of system DNS (try a
                         domain controller IP)
   -m, --minimal         Only query minimal set of attributes to limit memmory
                         usage
 ```
 
 - - -
 
 ##### ldd2bloodhound
 
 
 ```
 root@kali:~# ldd2bloodhound -h
 usage: ldd2bloodhound [-h] [-d] FILENAME [FILENAME ...]
 
 LDAPDomainDump to BloodHound CSV converter utility. Supports
 users/computers/trusts conversion.
 
 positional arguments:
   FILENAME     The ldapdomaindump json files to load. Required files:
                domain_users.json and domain_groups.json
 
 options:
   -h, --help   show this help message and exit
   -d, --debug  Enable debug logger
 ```
 
 - - -
 
 ##### ldd2pretty
 
 
 ```
 root@kali:~# ldd2pretty -h
 usage: ldd2pretty [-h] [-d DIRECTORY]
 
 LDAPDomainDump to pretty output like enum4linux.
 
 options:
   -h, --help            show this help message and exit
   -d DIRECTORY, --directory DIRECTORY
                         The ldapdomaindump directory where the json files are
                         saved. Required files: domain_users.json,
                         domain_groups.json and domain_policy.json
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
