---
Title: caldera
Homepage: https://github.com/mitre/caldera
Repository: https://gitlab.com/kalilinux/packages/caldera
Architectures: all
Version: 4.2.0-0kali1
Metapackages: kali-linux-everything kali-linux-large 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### caldera
 
  This package contains a cyber security framework designed to easily automate
  adversary emulation, assist manual red-teams, and automate incident response.
 
 **Installed size:** `63.12 MB`  
 **How to install:** `sudo apt install caldera`  
 
 {{< spoiler "Dependencies:" >}}
 * adduser
 * git
 * golang-go
 * python3
 * python3-aioftp
 * python3-aiohttp 
 * python3-aiohttp-apispec 
 * python3-aiohttp-jinja2
 * python3-aiohttp-security
 * python3-aiohttp-session
 * python3-asyncssh
 * python3-cryptography
 * python3-cssselect2
 * python3-dnspython
 * python3-docker
 * python3-donut
 * python3-jinja2
 * python3-ldap3
 * python3-lxml
 * python3-markdown
 * python3-marshmallow
 * python3-myst-parser
 * python3-pathspec
 * python3-recommonmark
 * python3-reportlab
 * python3-sphinx
 * python3-sphinx-rtd-theme
 * python3-websockets
 * python3-yaml
 * sudo
 {{< /spoiler >}}
 
 ##### caldera
 
 
 ```
 root@kali:~# caldera -h
 usage: Welcome to the system [-h] [-E ENVIRONMENT]
                              [-l {DEBUG,INFO,WARNING,ERROR,CRITICAL}]
                              [--fresh] [-P PLUGINS] [--insecure]
 
 options:
   -h, --help            show this help message and exit
   -E ENVIRONMENT, --environment ENVIRONMENT
                         Select an env. file to use
   -l {DEBUG,INFO,WARNING,ERROR,CRITICAL}, --log {DEBUG,INFO,WARNING,ERROR,CRITICAL}
                         Set the logging level
   --fresh               remove object_store on start
   -P PLUGINS, --plugins PLUGINS
                         Start up with a single plugin
   --insecure            Start caldera with insecure default config values.
                         Equivalent to "-E default".
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
