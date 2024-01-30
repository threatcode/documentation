---
Title: certipy-ad
Homepage: https://github.com/ly4k/Certipy
Repository: https://gitlab.com/kalilinux/packages/certipy-ad
Architectures: all
Version: 4.7.0-0kali3
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### certipy-ad
 
  Offensive tool for enumerating and abusing Active
  Directory Certificate Services (AD CS).
 
 **Installed size:** `538 KB`  
 **How to install:** `sudo apt install certipy-ad`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-asn1crypto
 * python3-cryptography 
 * python3-dnspython
 * python3-dsinternals
 * python3-impacket
 * python3-ldap3
 * python3-openssl
 * python3-pyasn1 
 * python3-pycryptodome
 * python3-requests
 * python3-requests-ntlm
 * python3-unicrypto
 {{< /spoiler >}}
 
 ##### certipy-ad
 
 
 ```
 root@kali:~# certipy-ad -h
 usage: certipy-ad [-v] [-h]
                   {account,auth,ca,cert,find,forge,ptt,relay,req,shadow,template}
                   ...
 
 Active Directory Certificate Services enumeration and abuse
 
 positional arguments:
   {account,auth,ca,cert,find,forge,ptt,relay,req,shadow,template}
                         Action
     account             Manage user and machine accounts
     auth                Authenticate using certificates
     ca                  Manage CA and certificates
     cert                Manage certificates and private keys
     find                Enumerate AD CS
     forge               Create Golden Certificates
     ptt                 Inject TGT for SSPI authentication
     relay               NTLM Relay to AD CS HTTP Endpoints
     req                 Request certificates
     shadow              Abuse Shadow Credentials for account takeover
     template            Manage certificate templates
 
 options:
   -v, --version         Show Certipy's version number and exit
   -h, --help            Show this help message and exit
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
