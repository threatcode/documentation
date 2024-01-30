---
Title: polenum
Homepage: https://github.com/Wh1t3Fox/polenum/
Repository: https://salsa.debian.org/pkg-security-team/polenum
Architectures: all
Version: 1.6.1-2
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-forensics kali-tools-information-gathering kali-tools-passwords kali-tools-respond kali-tools-vulnerability 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### polenum
 
  polenum is a Python script which uses the Impacket Library from CORE Security
  Technologies to extract the password policy information from a windows machine.
  This allows a non-windows (Linux, Mac OSX, BSD etc..) user to query the
  password policy of a remote windows box without the need to have access to a
  windows machine.
 
 **Installed size:** `26 KB`  
 **How to install:** `sudo apt install polenum`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-impacket
 {{< /spoiler >}}
 
 ##### polenum
 
 Extracts the password policy from a Windows system
 
 ```
 root@kali:~# polenum -h
 usage: polenum [-h] [--username USERNAME] [--password PASSWORD]
                [--domain DOMAIN] [--protocols [PROTOCOLS ...]]
                [enum4linux]
 
 positional arguments:
   enum4linux            username:password@IPaddress
 
 options:
   -h, --help            show this help message and exit
   --username USERNAME, -u USERNAME
                         The specified username
   --password PASSWORD, -p PASSWORD
                         The password of the user
   --domain DOMAIN, -d DOMAIN
                         The domain or IP
   --protocols [PROTOCOLS ...]
                         ['139/SMB', '445/SMB']
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## polenum Usage Example

Get the password policy of the system by logging in with the provided username and password (`victim:s3cr3t@192.168.1.200`) using SMB port 445 (`445/SMB`):

```
root@kali:~# polenum victim:s3cr3t@192.168.1.200 '445/SMB'

[+] Attaching to 192.168.1.200 using victim:s3cr3t

    [+] Trying protocol 445/SMB...

[+] Found domain(s):

    [+] WIN7-X86
    [+] Builtin

[+] Password Info for Domain: WIN7-X86

    [+] Minimum password length: None
    [+] Password history length: None
    [+] Maximum password age: Not Set
    [+] Password Complexity Flags: 000000

        [+] Domain Refuse Password Change: 0
        [+] Domain Password Store Cleartext: 0
        [+] Domain Password Lockout Admins: 0
        [+] Domain Password No Clear Change: 0
        [+] Domain Password No Anon Change: 0
        [+] Domain Password Complex: 0

    [+] Minimum password age: None
    [+] Reset Account Lockout Counter: 30 minutes
    [+] Locked Account Duration: 30 minutes
    [+] Account Lockout Threshold: None
    [+] Forced Log off Time: Not Set
```
