---
Title: nishang
Homepage: https://github.com/samratashok/nishang
Repository: https://gitlab.com/kalilinux/packages/nishang
Architectures: all
Version: 0.7.6+git20210724.414ee11-0kali1
Metapackages: kali-linux-everything kali-linux-large kali-linux-nethunter kali-tools-post-exploitation kali-tools-web 
Icon: images/nishang-logo.svg
PackagesInfo: |
 ### nishang
 
  Nishang is a framework and collection of scripts and payloads which enables
  usage of PowerShell for offensive security and post exploitation during
  Penetration Tests. The scripts are written on the basis of requirement by the
  author during real Penetration Tests.
 
 **Installed size:** `6.41 MB`  
 **How to install:** `sudo apt install nishang`  
 
 {{< spoiler "Dependencies:" >}}
 * kali-defaults
 {{< /spoiler >}}
 
 ##### nishang
 
 
 ```
 root@kali:~# nishang -h
 
 > nishang ~ Collection of PowerShell scripts and payloads
 
 /usr/share/nishang
 |-- ActiveDirectory
 |-- Antak-WebShell
 |-- Backdoors
 |-- Bypass
 |-- Client
 |-- Escalation
 |-- Execution
 |-- Gather
 |-- MITM
 |-- Misc
 |-- Pivot
 |-- Prasadhak
 |-- Scan
 |-- Shells
 |-- Utility
 |-- nishang.psm1
 `-- powerpreter
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## nishang Usage Example

```
root@kali:~# ls -l /usr/share/nishang/
total 48
drwxr-xr-x 2 root root 4096 Jun  4 11:15 Antak-WebShell
drwxr-xr-x 2 root root 4096 Jun  4 11:15 Backdoors
drwxr-xr-x 2 root root 4096 Jun  4 11:15 Escalation
drwxr-xr-x 2 root root 4096 Jun  4 11:15 Execution
drwxr-xr-x 2 root root 4096 Jun  4 11:15 Gather
drwxr-xr-x 2 root root 4096 Jun  4 11:15 Misc
-rw-r--r-- 1 root root  495 Jun  4 11:14 nishang.psm1
drwxr-xr-x 2 root root 4096 Jun  4 11:15 Pivot
drwxr-xr-x 2 root root 4096 Jun  4 11:15 powerpreter
drwxr-xr-x 2 root root 4096 Jun  4 11:15 Prasadhak
drwxr-xr-x 2 root root 4096 Jun  4 11:15 Scan
drwxr-xr-x 2 root root 4096 Jun  4 11:15 Utility
```
