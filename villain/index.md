---
Title: villain
Homepage: https://github.com/t3l3machus/Villain
Repository: https://gitlab.com/kalilinux/packages/villain
Architectures: all
Version: 0.0~git20230808.d24a7eb-0kali1
Metapackages: kali-linux-everything 
Icon: images/villain-logo.svg
PackagesInfo: |
 ### villain
 
  Villain is a C2 framework that can handle multiple TCP socket & HoaxShell-based
  reverse shells, enhance their functionality with additional features and share
  them among connected sibling servers.
 
 **Installed size:** `300 KB`  
 **How to install:** `sudo apt install villain`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-netifaces
 * python3-pycryptodome
 * python3-pyperclip
 * python3-requests
 {{< /spoiler >}}
 
 ##### villain
 
 
 ```
 root@kali:~# villain -h
 usage: Villain.py [-h] [-p PORT] [-x HOAX_PORT] [-n NETCAT_PORT]
                   [-f FILE_SMUGGLER_PORT] [-i] [-c CERTFILE] [-k KEYFILE] [-q]
 
 options:
   -h, --help            show this help message and exit
   -p PORT, --port PORT  Team server port (default: 6501).
   -x HOAX_PORT, --hoax-port HOAX_PORT
                         HoaxShell server port (default: 8080 via http, 443 via
                         https).
   -n NETCAT_PORT, --netcat-port NETCAT_PORT
                         Netcat multi-listener port (default: 4443).
   -f FILE_SMUGGLER_PORT, --file-smuggler-port FILE_SMUGGLER_PORT
                         Http file smuggler server port (default: 8888).
   -i, --insecure        Allows any Villain client (sibling server) to connect
                         to your instance without prompting you for
                         verification.
   -c CERTFILE, --certfile CERTFILE
                         Path to your ssl certificate (for HoaxShell https
                         server).
   -k KEYFILE, --keyfile KEYFILE
                         Path to the private key for your certificate (for
                         HoaxShell https server).
   -q, --quiet           Do not print the banner on startup.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
