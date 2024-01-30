---
Title: poshc2
Homepage: https://github.com/nettitude/PoshC2
Repository: https://gitlab.com/kalilinux/packages/poshc2
Architectures: all
Version: 7.4.0-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### poshc2
 
  This package contains a proxy aware C2 framework used to aid penetration
  testers with red teaming, post-exploitation and lateral movement.
   
  PoshC2 is primarily written in Python3 and follows a modular format to enable
  users to add their own modules and tools, allowing an extendible and flexible
  C2 framework. Out-of-the-box PoshC2 comes PowerShell/C# and Python3 implants
  with payloads written in PowerShell v2 and v4, C++ and C# source code, a
  variety of executables, DLLs and raw shellcode in addition to a Python3
  payload. These enable C2 functionality on a wide range of devices and
  operating systems, including Windows, *nix and OSX.
   
  Other notable features of PoshC2 include:
     - Consistent and Cross-Platform support using Docker.
     - Highly configurable payloads, including default beacon times, jitter,
       kill dates, user agents and more.
     - A large number of payloads generated out-of-the-box which are frequently
       updated and maintained to bypass common Anti-Virus products.
     - Auto-generated Apache Rewrite rules for use in a C2 proxy, protecting
       your C2 infrastructure and maintaining good operational security.
     - A modular format allowing users to create or edit C#, PowerShell or
       Python3 modules which can be run in-memory by the Implants.
     - Notifications on receiving a successful Implant, such as via text message
       or Pushover.
     - A comprehensive and maintained contextual help and an intelligent prompt
       with contextual auto-completion, history and suggestions.
     - Fully encrypted communications, protecting the confidentiality and
       integrity of the C2 traffic even when communicating over HTTP.
     - Client/Server format allowing multiple team members to utilise a single
       C2 server.
     - Extensive logging. Every action and response is timestamped and stored in
       a database with all relevant information such as user, host, implant
       number etc. In addition to this the C2 server output is directly logged
       to a separate file.
     - PowerShell-less implants that do not use System.Management.Automation.dll
       using C# or Python.
     - A free and open-source SOCKS Proxy by integrating with SharpSocks
 
 **Installed size:** `36.69 MB`  
 **How to install:** `sudo apt install poshc2`  
 
 {{< spoiler "Dependencies:" >}}
 * espeak
 * graphviz
 * mingw-w64
 * mingw-w64-common
 * mingw-w64-i686-dev
 * mingw-w64-tools
 * mingw-w64-x86-64-dev
 * mono-devel
 * postgresql
 * python3
 * python3-donut
 * python3-openssl
 * python3-pandas
 * python3-prompt-toolkit
 * python3-psycopg2
 * python3-pycryptodome
 * python3-yaml
 * sqlite3
 * vim | editor
 {{< /spoiler >}}
 
 ##### _posh-common
 
 
 
 - - -
 
 ##### fpc
 
 
 ```
 root@kali:~# fpc -h
 No PoshC2 project set, please run posh-project
 ```
 
 - - -
 
 ##### posh
 
 
 ```
 root@kali:~# posh -h
 PoshC2 current project file does not exist, please run posh-project
 ```
 
 - - -
 
 ##### posh-config
 
 
 ```
 root@kali:~# posh-config -h
 No PoshC2 project set, please run posh-project
 ```
 
 - - -
 
 ##### posh-cookie-decrypter
 
 
 ```
 root@kali:~# posh-cookie-decrypter -h
 PoshC2 current project file does not exist, please run posh-project
 ```
 
 - - -
 
 ##### posh-log
 
 
 ```
 root@kali:~# posh-log -h
 No PoshC2 project set, please run posh-project
 ```
 
 - - -
 
 ##### posh-project
 
 
 ```
 root@kali:~# posh-project -h
 [*] Usage: posh-project -n <new-project-name>
 [*] Usage: posh-project -s <project-to-switch-to>
 [*] Usage: posh-project -l (lists projects)
 [*] Usage: posh-project -d <project-to-delete>
 [*] Usage: posh-project -c (shows current project)
 [*] Usage: posh-project -g (quietly shows current project directory for scripting)
 ```
 
 - - -
 
 ##### posh-server
 
 
 ```
 root@kali:~# posh-server -h
 No PoshC2 project set, please run posh-project
 ```
 
 - - -
 
 ##### posh-service
 
 
 ```
 root@kali:~# posh-service -h
 No PoshC2 project set, please run posh-project
 ```
 
 - - -
 
 ##### posh-stop-service
 
 
 
 - - -
 
 ##### sharpsocks
 
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
