---
Title: faraday-agent-dispatcher
Homepage: https://github.com/infobyte/faraday_agent_dispatcher
Repository: https://gitlab.com/kalilinux/packages/faraday-agent-dispatcher
Architectures: all
Version: 2.4.0-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### faraday-agent-dispatcher
 
  This package contains Faraday Agents Dispatcher. It helps user develop
  integrations with Faraday written in any language.
   
  This package installs the library for Python 3.
 
 **Installed size:** `265 KB`  
 **How to install:** `sudo apt install faraday-agent-dispatcher`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-aiohttp
 * python3-click
 * python3-faraday-agent-parameters-types
 * python3-faraday-plugins
 * python3-gvm
 * python3-itsdangerous
 * python3-psutil
 * python3-requests
 * python3-syslog-rfc5424-formatter
 * python3-websockets
 * python3-yaml
 * python3-zapv2
 {{< /spoiler >}}
 
 ##### faraday-dispatcher
 
 
 ```
 root@kali:~# faraday-dispatcher -h
 Usage: faraday-dispatcher [OPTIONS] COMMAND [ARGS]...
 
 Options:
   -v, --version  Show the version and exit.
   -h, --help     Show this message and exit.
 
 Commands:
   config-wizard  faraday-dispatcher config_wizard
   run            faraday-dispatcher run
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
