---
Title: evil-ssdp
Homepage: https://github.com/initstring/evil-ssdp
Repository: https://gitlab.com/kalilinux/packages/evil-ssdp
Architectures: all
Version: 0.8~beta-0kali2
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### evil-ssdp
 
  This tool responds to SSDP multicast discover requests, posing as a generic
  UPNP device on a local network. Your spoofed device will magically appear in
  Windows Explorer on machines in your local network. Users who are tempted to
  open the device are shown a configurable webpage.
 
 **Installed size:** `100 KB`  
 **How to install:** `sudo apt install evil-ssdp`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 {{< /spoiler >}}
 
 ##### evil-ssdp
 
 
 ```
 root@kali:~# evil-ssdp -h
 
 ___________     .__.__    _________ _________________ __________
 \_   _____/__  _|__|  |  /   _____//   _____/\______ \\______   \
  |    __)_\  \/ /  |  |  \_____  \ \_____  \  |    |  \|     ___/
  |        \\   /|  |  |__/        \/        \ |    `   \    |
 /_______  / \_/ |__|____/_______  /_______  //_______  /____|
         \/                      \/        \/         \/
 
 ...by initstring (gitlab.com/initstring)
 Additional contributors: Dwight Hohnstein
 
 usage: evil_ssdp.py [-h] [-p PORT] [-t TEMPLATE] [-s SMB] [-b] [-r REALM]
                     [-u URL] [-a]
                     interface
 
 positional arguments:
   interface             Network interface to listen on.
 
 options:
   -h, --help            show this help message and exit
   -p PORT, --port PORT  Port for HTTP server. Defaults to 8888.
   -t TEMPLATE, --template TEMPLATE
                         Name of a folder in the templates directory. Defaults
                         to "office365". This will determine xml and phishing
                         pages used.
   -s SMB, --smb SMB     IP address of your SMB server. Defalts to the primary
                         address of the "interface" provided.
   -b, --basic           Enable base64 authentication for templates and write
                         credentials to log file.
   -r REALM, --realm REALM
                         Realm when prompting target for authentication via
                         Basic Auth.
   -u URL, --url URL     Redirect to this URL. Works with templates that do a
                         POST for logon forms and with templates that include
                         the custom redirect JavaScript (see README for more
                         info).[example: -r https://google.com]
   -a, --analyze         Run in analyze mode. Will NOT respond to any SSDP
                         queries, but will still enable and run the web server
                         for testing.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
