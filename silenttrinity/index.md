---
Title: silenttrinity
Homepage: https://github.com/byt3bl33d3r/SILENTTRINITY
Repository: https://gitlab.com/kalilinux/packages/silenttrinity
Architectures: all
Version: 0.4.6dev~20200310-0kali3
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### silenttrinity
 
  This package contains a modern, asynchronous, multiplayer & multiserver
  C2/post-exploitation framework powered by Python 3 and .NETs DLR. It's the
  culmination of an extensive amount of research into using embedded third-party
   .NET scripting languages to dynamically call .NET API's, a technique the
  author coined as BYOI (Bring Your Own Interpreter). The aim of this tool and
  the BYOI concept is to shift the paradigm back to PowerShell style like
  attacks (as it offers much more flexibility over traditional C# tradecraft)
  only without using PowerShell in anyway.
   
  Some of the main features that distinguish SILENTTRINITY are:
     - Multi-User & Multi-Server - Supports multi-user collaboration.
       Additionally, the client can connect to and control multiple Teamservers.
     - Client and Teamserver Built in Python 3.7 - Latest and greatest features
       of the Python language are used, heavy use of Asyncio provides ludicrous
       speeds.
     - Real-time Updates and Communication - Use of Websockets allow for
       real-time communication and updates between the Client and Teamserver.
     - Focus on Usability with an Extremely Modern CLI - Powered by
       prompt-toolkit.
     - Dynamic Evaluation/Compilation Using .NET Scripting Languages - The
       SILENTTRINITY implant Naga, is somewhat unique as it uses embedded
       third-party .NET scripting languages (e.g. Boolang) to dynamically
       compile/evaluate tasks, this removes the need to compile tasks server
       side, allows for real-time editing of modules, provides greater
       flexibilty and stealth over traditional C# based payloads and makes
       everything much more light-weight.
     - ECDHE Encrypted C2 Communication - SILENTTRINITY uses Ephemeral Elliptic
       Curve Diffie-Hellman Key Exchange to encrypt all C2 traffic between the
       Teamserver and its implant.
     - Fully Modular - Listeners, Modules, Stagers and C2 Channels are fully
       modular allowing operators to easily build their own.
     - Extensive logging - Every action is logged to a file.
     - Future proof - HTTPS/HTTP listeners are built on Quart & Hypercorn which
       also support HTTP2 & Websockets.
 
 **Installed size:** `4.89 MB`  
 **How to install:** `sudo apt install silenttrinity`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-aiocmd
 * python3-aiofiles
 * python3-aiosqlite
 * python3-aiowinreg
 * python3-asciitree
 * python3-asn1crypto
 * python3-blinker
 * python3-certifi
 * python3-cffi
 * python3-chardet
 * python3-click
 * python3-cryptography 
 * python3-defusedxml
 * python3-docopt
 * python3-donut
 * python3-h11
 * python3-h2
 * python3-hpack
 * python3-hypercorn
 * python3-hyperframe
 * python3-idna
 * python3-itsdangerous
 * python3-jinja2
 * python3-ldap3
 * python3-markupsafe
 * python3-minidump
 * python3-minikerberos
 * python3-msldap
 * python3-multidict
 * python3-netifaces
 * python3-priority
 * python3-prompt-toolkit 
 * python3-pyasn1
 * python3-pycparser
 * python3-pypykatz
 * python3-quart
 * python3-requests
 * python3-six 
 * python3-sortedcontainers
 * python3-termcolor
 * python3-terminaltables
 * python3-toml
 * python3-typing-extensions
 * python3-urllib3
 * python3-wcwidth
 * python3-websockets
 * python3-wsproto
 {{< /spoiler >}}
 
 ##### silenttrinity
 
 
 ```
 root@kali:~# silenttrinity -h
 Usage: st [-h] [-v] (client|teamserver) [<args>...]
 
 options:
     -h, --help                   Show this help message and exit
     -v, --version                Show version
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
