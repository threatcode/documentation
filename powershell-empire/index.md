---
Title: powershell-empire
Homepage: https://github.com/BC-SECURITY/Empire
Repository: https://gitlab.com/kalilinux/packages/powershell-empire
Architectures: all
Version: 5.4.2-0kali5
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large 
Icon: images/powershell-empire-logo.svg
PackagesInfo: |
 ### powershell-empire
 
  This package contains a post-exploitation framework that includes a
  pure-PowerShell2.0 Windows agent, and a pure Python Linux/OS X agent.
  It is the merge of the previous PowerShell Empire and Python EmPyre projects.
  The framework offers cryptologically-secure communications and a flexible
  architecture. On the PowerShell side, Empire implements the ability to run
  PowerShell agents without needing powershell.exe, rapidly deployable
  post-exploitation modules ranging from key loggers to Mimikatz, and adaptable
  communications to evade network detection, all wrapped up in a
  usability-focused framework.
 
 **Installed size:** `156.97 MB`  
 **How to install:** `sudo apt install powershell-empire`  
 
 {{< spoiler "Dependencies:" >}}
 * default-mysql-server
 * python3
 * python3-aiofiles
 * python3-bcrypt
 * python3-cryptography
 * python3-docopt
 * python3-donut 
 * python3-dropbox
 * python3-fastapi
 * python3-flask
 * python3-flask-socketio
 * python3-humanize
 * python3-jinja2
 * python3-jose
 * python3-jq
 * python3-macholib
 * python3-multipart
 * python3-netifaces
 * python3-openssl
 * python3-packaging
 * python3-passlib
 * python3-prompt-toolkit
 * python3-pycryptodome
 * python3-pydantic
 * python3-pydispatch
 * python3-pyinstaller
 * python3-pymysql
 * python3-pyparsing
 * python3-pyperclip
 * python3-pyvnc
 * python3-requests
 * python3-secretsocks
 * python3-setuptools
 * python3-simplejson
 * python3-socketio 
 * python3-sqlalchemy
 * python3-sqlalchemy-utc
 * python3-terminaltables
 * python3-tk
 * python3-urllib3
 * python3-uvicorn
 * python3-websocket
 * python3-websockets
 * python3-websockify
 * python3-xlrd
 * python3-xlutils
 * python3-yaml
 * python3-zlib-wrapper
 * starkiller 
 {{< /spoiler >}}
 
 ##### powershell-empire
 
 
 ```
 root@kali:~# powershell-empire -h
 usage: empire.py [-h] {server,client} ...
 
 positional arguments:
   {server,client}
     server         Launch Empire Server
     client         Launch Empire CLI
 
 options:
   -h, --help       show this help message and exit
 ```
 
 - - -
 
 ##### starkiller
 
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
