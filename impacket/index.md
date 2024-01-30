---
Title: impacket
Homepage: https://github.com/SecureAuthCorp/impacket
Repository: https://salsa.debian.org/python-team/packages/impacket
Architectures: all
Version: 0.11.0-1
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-exploitation kali-tools-forensics kali-tools-information-gathering kali-tools-passwords kali-tools-respond kali-tools-social-engineering kali-tools-top10 kali-tools-vulnerability kali-tools-web 
Icon: images/impacket-logo.svg
PackagesInfo: |
 ### python3-impacket
 
  Impacket  is a  collection  of Python3  classes  focused on  providing
  access  to network  packets.   Impacket allows  Python3 developers  to
  craft and decode network packets in simple and consistent manner.  It
  includes support for low-level protocols  such as IP, UDP and TCP, as
  well as higher-level protocols such as NMB and SMB.
   
  Impacket is highly  effective when used in conjunction  with a packet
  capture utility or package such as Pcapy.  Packets can be constructed
  from  scratch, as  well as  parsed from  raw data.   Furthermore, the
  object  oriented API  makes  it  simple to  work  with deep  protocol
  hierarchies.
 
 **Installed size:** `6.66 MB`  
 **How to install:** `sudo apt install python3-impacket`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-charset-normalizer
 * python3-flask
 * python3-future
 * python3-ldap3
 * python3-ldapdomaindump
 * python3-openssl 
 * python3-pkg-resources
 * python3-pyasn1 
 * python3-pycryptodome
 * python3-six
 {{< /spoiler >}}
 
 ##### impacket-netview
 
 
 ```
 root@kali:~# impacket-netview -h
 Impacket v0.11.0 - Copyright 2023 Fortra
 
 usage: netview.py [-h] [-user USER] [-users USERS] [-target TARGET]
                   [-targets TARGETS] [-noloop] [-delay DELAY]
                   [-max-connections MAX_CONNECTIONS] [-ts] [-debug]
                   [-hashes LMHASH:NTHASH] [-no-pass] [-k] [-aesKey hex key]
                   [-dc-ip ip address]
                   identity
 
 positional arguments:
   identity              [domain/]username[:password]
 
 options:
   -h, --help            show this help message and exit
   -user USER            Filter output by this user
   -users USERS          input file with list of users to filter to output for
   -target TARGET        target system to query info from. If not specified
                         script will run in domain mode.
   -targets TARGETS      input file with targets system to query info from (one
                         per line). If not specified script will run in domain
                         mode.
   -noloop               Stop after the first probe
   -delay DELAY          seconds delay between starting each batch probe
                         (default 10 seconds)
   -max-connections MAX_CONNECTIONS
                         Max amount of connections to keep opened (default
                         1000)
   -ts                   Adds timestamp to every logging output
   -debug                Turn DEBUG output ON
 
 authentication:
   -hashes LMHASH:NTHASH
                         NTLM hashes, format is LMHASH:NTHASH
   -no-pass              don't ask for password (useful for -k)
   -k                    Use Kerberos authentication. Grabs credentials from
                         ccache file (KRB5CCNAME) based on target parameters.
                         If valid credentials cannot be found, it will use the
                         ones specified in the command line
   -aesKey hex key       AES key to use for Kerberos Authentication (128 or 256
                         bits)
   -dc-ip ip address     IP Address of the domain controller. If ommited it use
                         the domain part (FQDN) specified in the target
                         parameter
 ```
 
 - - -
 
 ##### impacket-rpcdump
 
 
 ```
 root@kali:~# impacket-rpcdump -h
 Impacket v0.11.0 - Copyright 2023 Fortra
 
 usage: rpcdump.py [-h] [-debug] [-target-ip ip address]
                   [-port [destination port]] [-hashes LMHASH:NTHASH]
                   target
 
 Dumps the remote RPC enpoints information via epmapper.
 
 positional arguments:
   target                [[domain/]username[:password]@]<targetName or address>
 
 options:
   -h, --help            show this help message and exit
   -debug                Turn DEBUG output ON
 
 connection:
   -target-ip ip address
                         IP Address of the target machine. If ommited it will
                         use whatever was specified as target. This is useful
                         when target is the NetBIOS name and you cannot resolve
                         it
   -port [destination port]
                         Destination port to connect to RPC Endpoint Mapper
 
 authentication:
   -hashes LMHASH:NTHASH
                         NTLM hashes, format is LMHASH:NTHASH
 ```
 
 - - -
 
 ##### impacket-samrdump
 
 
 ```
 root@kali:~# impacket-samrdump -h
 Impacket v0.11.0 - Copyright 2023 Fortra
 
 usage: samrdump.py [-h] [-csv] [-ts] [-debug] [-dc-ip ip address]
                    [-target-ip ip address] [-port [destination port]]
                    [-hashes LMHASH:NTHASH] [-no-pass] [-k] [-aesKey hex key]
                    target
 
 This script downloads the list of users for the target system.
 
 positional arguments:
   target                [[domain/]username[:password]@]<targetName or address>
 
 options:
   -h, --help            show this help message and exit
   -csv                  Turn CSV output
   -ts                   Adds timestamp to every logging output
   -debug                Turn DEBUG output ON
 
 connection:
   -dc-ip ip address     IP Address of the domain controller. If ommited it use
                         the domain part (FQDN) specified in the target
                         parameter
   -target-ip ip address
                         IP Address of the target machine. If ommited it will
                         use whatever was specified as target. This is useful
                         when target is the NetBIOS name and you cannot resolve
                         it
   -port [destination port]
                         Destination port to connect to SMB Server
 
 authentication:
   -hashes LMHASH:NTHASH
                         NTLM hashes, format is LMHASH:NTHASH
   -no-pass              don't ask for password (useful for -k)
   -k                    Use Kerberos authentication. Grabs credentials from
                         ccache file (KRB5CCNAME) based on target parameters.
                         If valid credentials cannot be found, it will use the
                         ones specified in the command line
   -aesKey hex key       AES key to use for Kerberos Authentication (128 or 256
                         bits)
 ```
 
 - - -
 
 ##### impacket-secretsdump
 
 
 ```
 root@kali:~# impacket-secretsdump -h
 Impacket v0.11.0 - Copyright 2023 Fortra
 
 usage: secretsdump.py [-h] [-ts] [-debug] [-system SYSTEM] [-bootkey BOOTKEY]
                       [-security SECURITY] [-sam SAM] [-ntds NTDS]
                       [-resumefile RESUMEFILE] [-outputfile OUTPUTFILE]
                       [-use-vss] [-rodcNo RODCNO] [-rodcKey RODCKEY]
                       [-use-keylist]
                       [-exec-method [{smbexec,wmiexec,mmcexec}]]
                       [-just-dc-user USERNAME] [-ldapfilter LDAPFILTER]
                       [-just-dc] [-just-dc-ntlm] [-pwd-last-set]
                       [-user-status] [-history] [-hashes LMHASH:NTHASH]
                       [-no-pass] [-k] [-aesKey hex key] [-keytab KEYTAB]
                       [-dc-ip ip address] [-target-ip ip address]
                       target
 
 Performs various techniques to dump secrets from the remote machine without
 executing any agent there.
 
 positional arguments:
   target                [[domain/]username[:password]@]<targetName or address>
                         or LOCAL (if you want to parse local files)
 
 options:
   -h, --help            show this help message and exit
   -ts                   Adds timestamp to every logging output
   -debug                Turn DEBUG output ON
   -system SYSTEM        SYSTEM hive to parse
   -bootkey BOOTKEY      bootkey for SYSTEM hive
   -security SECURITY    SECURITY hive to parse
   -sam SAM              SAM hive to parse
   -ntds NTDS            NTDS.DIT file to parse
   -resumefile RESUMEFILE
                         resume file name to resume NTDS.DIT session dump (only
                         available to DRSUAPI approach). This file will also be
                         used to keep updating the session's state
   -outputfile OUTPUTFILE
                         base output filename. Extensions will be added for
                         sam, secrets, cached and ntds
   -use-vss              Use the VSS method instead of default DRSUAPI
   -rodcNo RODCNO        Number of the RODC krbtgt account (only avaiable for
                         Kerb-Key-List approach)
   -rodcKey RODCKEY      AES key of the Read Only Domain Controller (only
                         avaiable for Kerb-Key-List approach)
   -use-keylist          Use the Kerb-Key-List method instead of default
                         DRSUAPI
   -exec-method [{smbexec,wmiexec,mmcexec}]
                         Remote exec method to use at target (only when using
                         -use-vss). Default: smbexec
 
 display options:
   -just-dc-user USERNAME
                         Extract only NTDS.DIT data for the user specified.
                         Only available for DRSUAPI approach. Implies also
                         -just-dc switch
   -ldapfilter LDAPFILTER
                         Extract only NTDS.DIT data for specific users based on
                         an LDAP filter. Only available for DRSUAPI approach.
                         Implies also -just-dc switch
   -just-dc              Extract only NTDS.DIT data (NTLM hashes and Kerberos
                         keys)
   -just-dc-ntlm         Extract only NTDS.DIT data (NTLM hashes only)
   -pwd-last-set         Shows pwdLastSet attribute for each NTDS.DIT account.
                         Doesn't apply to -outputfile data
   -user-status          Display whether or not the user is disabled
   -history              Dump password history, and LSA secrets OldVal
 
 authentication:
   -hashes LMHASH:NTHASH
                         NTLM hashes, format is LMHASH:NTHASH
   -no-pass              don't ask for password (useful for -k)
   -k                    Use Kerberos authentication. Grabs credentials from
                         ccache file (KRB5CCNAME) based on target parameters.
                         If valid credentials cannot be found, it will use the
                         ones specified in the command line
   -aesKey hex key       AES key to use for Kerberos Authentication (128 or 256
                         bits)
   -keytab KEYTAB        Read keys for SPN from keytab file
 
 connection:
   -dc-ip ip address     IP Address of the domain controller. If ommited it use
                         the domain part (FQDN) specified in the target
                         parameter
   -target-ip ip address
                         IP Address of the target machine. If omitted it will
                         use whatever was specified as target. This is useful
                         when target is the NetBIOS name and you cannot resolve
                         it
 ```
 
 - - -
 
 ##### impacket-wmiexec
 
 
 ```
 root@kali:~# impacket-wmiexec -h
 Impacket v0.11.0 - Copyright 2023 Fortra
 
 usage: wmiexec.py [-h] [-share SHARE] [-nooutput] [-ts] [-silentcommand]
                   [-debug] [-codec CODEC] [-shell-type {cmd,powershell}]
                   [-com-version MAJOR_VERSION:MINOR_VERSION]
                   [-hashes LMHASH:NTHASH] [-no-pass] [-k] [-aesKey hex key]
                   [-dc-ip ip address] [-A authfile] [-keytab KEYTAB]
                   target [command ...]
 
 Executes a semi-interactive shell using Windows Management Instrumentation.
 
 positional arguments:
   target                [[domain/]username[:password]@]<targetName or address>
   command               command to execute at the target. If empty it will
                         launch a semi-interactive shell
 
 options:
   -h, --help            show this help message and exit
   -share SHARE          share where the output will be grabbed from (default
                         ADMIN$)
   -nooutput             whether or not to print the output (no SMB connection
                         created)
   -ts                   Adds timestamp to every logging output
   -silentcommand        does not execute cmd.exe to run given command (no
                         output)
   -debug                Turn DEBUG output ON
   -codec CODEC          Sets encoding used (codec) from the target's output
                         (default "utf-8"). If errors are detected, run
                         chcp.com at the target, map the result with https://do
                         cs.python.org/3/library/codecs.html#standard-encodings
                         and then execute wmiexec.py again with -codec and the
                         corresponding codec
   -shell-type {cmd,powershell}
                         choose a command processor for the semi-interactive
                         shell
   -com-version MAJOR_VERSION:MINOR_VERSION
                         DCOM version, format is MAJOR_VERSION:MINOR_VERSION
                         e.g. 5.7
 
 authentication:
   -hashes LMHASH:NTHASH
                         NTLM hashes, format is LMHASH:NTHASH
   -no-pass              don't ask for password (useful for -k)
   -k                    Use Kerberos authentication. Grabs credentials from
                         ccache file (KRB5CCNAME) based on target parameters.
                         If valid credentials cannot be found, it will use the
                         ones specified in the command line
   -aesKey hex key       AES key to use for Kerberos Authentication (128 or 256
                         bits)
   -dc-ip ip address     IP Address of the domain controller. If ommited it use
                         the domain part (FQDN) specified in the target
                         parameter
   -A authfile           smbclient/mount.cifs-style authentication file. See
                         smbclient man page's -A option.
   -keytab KEYTAB        Read keys for SPN from keytab file
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
