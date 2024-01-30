---
Title: powersploit
Homepage: https://github.com/PowerShellMafia/PowerSploit
Repository: https://gitlab.com/kalilinux/packages/powersploit
Architectures: all
Version: 3.0.0+git20200817.d943001-0kali1
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-post-exploitation 
Icon: images/powersploit-logo.svg
PackagesInfo: |
 ### powersploit
 
  PowerSploit is a series of Microsoft PowerShell scripts
  that can be used in post-exploitation scenarios during
  authorized penetration tests.
 
 **Installed size:** `5.46 MB`  
 **How to install:** `sudo apt install powersploit`  
 
 {{< spoiler "Dependencies:" >}}
 * kali-defaults 
 {{< /spoiler >}}
 
 ##### powersploit
 
 
 ```
 root@kali:~# powersploit -h
 
 > powersploit ~ PowerShell Post-Exploitation Framework
 
 /usr/share/windows-resources/powersploit
 |-- AntivirusBypass
 |-- CodeExecution
 |-- Exfiltration
 |-- Mayhem
 |-- Persistence
 |-- PowerSploit.psd1
 |-- PowerSploit.psm1
 |-- Privesc
 |-- README.md
 |-- Recon
 |-- ScriptModification
 `-- Tests
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## PowerSploit Usage Example

```
root@kali:~# ls -l /usr/share/powersploit/
total 52
drwxr-xr-x 2 root root 4096 Feb 11 15:10 AntivirusBypass
drwxr-xr-x 3 root root 4096 Feb 11 15:10 CodeExecution
drwxr-xr-x 2 root root 4096 Feb 11 15:10 Exfiltration
drwxr-xr-x 2 root root 4096 Feb 11 15:10 Persistence
drwxr-xr-x 2 root root 4096 Feb 11 15:10 PETools
-rw-r--r-- 1 root root 3542 Jun 11  2013 PowerSploit.psd1
-rw-r--r-- 1 root root   89 Jun 11  2013 PowerSploit.psm1
-rw-r--r-- 1 root root 8900 Jun 11  2013 README.md
drwxr-xr-x 3 root root 4096 Feb 11 15:10 Recon
drwxr-xr-x 2 root root 4096 Feb 11 15:10 ReverseEngineering
drwxr-xr-x 2 root root 4096 Feb 11 15:10 ScriptModification
```
