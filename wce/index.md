---
Title: wce
Homepage: http://www.ampliasecurity.com/research.html
Repository: https://gitlab.com/kalilinux/packages/wce
Architectures: all
Version: 1.42-beta-0kali4
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-forensics kali-tools-respond kali-tools-windows-resources 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### wce
 
  Windows Credentials Editor (WCE) v1.3beta allows you to:
   
  NTLM authentication:
   
  * List logon sessions and add, change, list and delete associated credentials
  (e.g.: LM/NT hashes)
  * Perform pass-the-hash on Windows natively
  * Obtain NT/LM hashes from memory (from interactive logons, services, remote
  desktop connections, etc.) which can be used to authenticate to other systems.
  WCE can perform this task without injecting code, just by reading and
  decrypting information stored in Windows internal memory structures. It also
  has the capability to automatically switch to code injection when the
  aforementioned method cannot be performed.
 
 **Installed size:** `940 KB`  
 **How to install:** `sudo apt install wce`  
 
 {{< spoiler "Dependencies:" >}}
 * kali-defaults 
 {{< /spoiler >}}
 
 ##### wce
 
 
 ```
 root@kali:~# wce -h
 
 > wce ~ Windows Credentials Editor
 
 /usr/share/windows-resources/wce
 |-- README
 |-- getlsasrvaddr.exe
 |-- wce-universal.exe
 |-- wce32.exe
 `-- wce64.exe
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
