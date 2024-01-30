---
Title: python-faraday
Homepage: https://faradaysec.com
Repository: https://gitlab.com/kalilinux/packages/python-faraday
Architectures: all
Version: 4.6.2-0kali1
Metapackages: kali-linux-default kali-linux-everything kali-linux-large kali-tools-reporting 
Icon: images/python-faraday-logo.svg
PackagesInfo: |
 ### faraday
 
  Faraday introduces a new concept (IPE) Integrated Penetration-Test Environment
  a multiuser Penetration test IDE. Designed for distribution, indexation and
  analysis of the generated data during the process of a security audit.
   
  The main purpose of Faraday is to re-use the available tools in the community
  to take advantage of them in a multiuser way.
   
  This package no longer contains the GTK client like the upstream repo.
 
 **Installed size:** `33.23 MB`  
 **How to install:** `sudo apt install faraday`  
 
 {{< spoiler "Dependencies:" >}}
 * curl
 * gir1.2-gtk-3.0
 * gir1.2-vte-2.91
 * pgcli
 * postgresql
 * python3
 * python3-alembic
 * python3-apispec
 * python3-apispec-webframeworks
 * python3-autobahn
 * python3-bcrypt
 * python3-bidict
 * python3-bleach
 * python3-click
 * python3-colorama
 * python3-cryptography 
 * python3-cvss
 * python3-dateutil
 * python3-distro
 * python3-distutils
 * python3-email-validator
 * python3-faraday-agent-parameters-types 
 * python3-faraday-plugins 
 * python3-filedepot
 * python3-filteralchemy 
 * python3-flask 
 * python3-flask-classful 
 * python3-flask-kvsession
 * python3-flask-limiter 
 * python3-flask-login
 * python3-flask-mail
 * python3-flask-principal
 * python3-flask-socketio 
 * python3-flask-sqlalchemy 
 * python3-flaskext.wtf
 * python3-jwt
 * python3-marshmallow 
 * python3-marshmallow-sqlalchemy 
 * python3-nplusone 
 * python3-openssl
 * python3-pil
 * python3-psycopg2
 * python3-pyasn1
 * python3-pyotp
 * python3-requests
 * python3-service-identity
 * python3-simplekv
 * python3-sqlalchemy-schemadisplay
 * python3-syslog-rfc5424-formatter
 * python3-tornado
 * python3-tqdm
 * python3-twisted
 * python3-webargs 
 * python3-werkzeug
 * python3-wtforms
 * python3-yaml
 * sudo
 * xdg-utils
 * zsh | zsh-beta
 {{< /spoiler >}}
 
 ##### faraday
 
 Kali script to start and stop faraday-server and faraday-client
 
 ```
 root@kali:~# faraday -h
 >>> Start faraday.service
 ```
 
 - - -
 
 ##### faraday-manage
 
 Helper to manage Faraday's database, users...
 
 ```
 root@kali:~# faraday-manage -h
 Usage: faraday-manage [OPTIONS] COMMAND [ARGS]...
 
 Options:
   -h, --help  Show this message and exit.
 
 Commands:
   add-custom-field                Custom field wizard
   change-password                 Changes the password of a user
   create-superuser                Create ADMIN user for Faraday application
   create-tables                   Create database tables.
   database-schema                 Create a PNG image with Faraday model...
   delete-custom-field             Custom field delete wizard
   generate-nginx-config           Generate nginx config
   import-vulnerability-templates  Import Vulnerability templates
   initdb                          Create Faraday DB in Postgresql, also...
   list-plugins                    List Available Plugins
   migrate                         Migrates database schema.
   openapi-swagger                 Creates Faraday Swagger config file
   rename-user                     Change username
   settings                        Manage settings
   show-urls                       Show all URLs in Faraday Server API
   sql-shell                       Open a SQL Shell connected to...
 ```
 
 - - -
 
 ##### faraday-server
 
 Faraday server's launcher
 
 ```
 root@kali:~# faraday-server -h
 usage: faraday-server [-h] [--debug] [--port PORT]
                       [--websocket_port WEBSOCKET_PORT]
                       [--bind_address BIND_ADDRESS] [-v]
 
 options:
   -h, --help            show this help message and exit
   --debug               run Faraday Server in debug mode
   --port PORT           Overides server.ini port configuration
   --websocket_port WEBSOCKET_PORT
                         Overides server.ini websocket port configuration
   --bind_address BIND_ADDRESS
                         Overides server.ini bind_address configuration
   -v, --version         show program's version number and exit
 ```
 
 - - -
 
 ##### python-faraday
 
 
 ```
 root@kali:~# python-faraday -h
 >>> Start faraday.service
 ```
 
 - - -
 
 ### python-faraday
 
  Faraday introduces a new concept (IPE) Integrated Penetration-Test Environment
  a multiuser Penetration test IDE. Designed for distribution, indexation and
  analysis of the generated data during the process of a security audit.
   
  The main purpose of Faraday is to re-use the available tools in the community
  to take advantage of them in a multiuser way.
   
  This package is a transitional package. It can be remove safely.
 
 **Installed size:** `32 KB`  
 **How to install:** `sudo apt install python-faraday`  
 
 {{< spoiler "Dependencies:" >}}
 * faraday
 {{< /spoiler >}}
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## Screenshots

![python-faraday](images/faraday-01-main.png)

## Faraday Usage Examples

Faraday is a GUI application that consists of a ZSH terminal and a sidebar with details about your workspaces and hosts.

When Faraday supports the command you are running, it will automatically detect it and import the results. In the example below, the original nmap command that was entered was `nmap -A 192.168.0.7`, which Faraday converted on the fly.

```
>>> WELCOME TO FARADAY
[+] Current Workspace: dev1
[+] API: OK
[faraday](dev1) kali#  nmap -oX /root/.faraday/data/devel1_Nmap_output-3.46164772371.xml -A 192.168.0.7 2>&1 | tee -a tmp.tu0ldZUG2JgzuHvLOjBYEzBx3Bu7O

Starting Nmap 7.40 ( https://nmap.org ) at 2017-03-07 13:46 MST
Nmap scan report for pi-hole (192.168.0.7)
Host is up (0.0011s latency).
Not shown: 995 closed ports
PORT    STATE SERVICE    VERSION
22/tcp  open  ssh        OpenSSH 6.7p1 Raspbian 5+deb8u3 (protocol 2.0)
| ssh-hostkey:
|   1024 f7:5d:7c:e2:c5:46:32:19:08:e9:4b:79:5e:80:1c:83 (DSA)
|   2048 3c:f9:1d:ce:03:0f:2e:d2:17:05:77:af:81:54:32:fc (RSA)
|_  256 ea:20:d1:e0:e1:89:2c:65:9e:0d:d0:d0:e9:8b:9b:28 (ECDSA)
53/tcp  open  domain     dnsmasq 2.72
| dns-nsid:
|_  bind.version: dnsmasq-2.72
80/tcp  open  http       lighttpd 1.4.35
|_http-server-header: lighttpd/1.4.35
|_http-title: Welcome page
110/tcp open  tcpwrapped
143/tcp open  tcpwrapped
Device type: general purpose
Running: Linux 2.4.X|3.X
OS CPE: cpe:/o:linux:linux_kernel:2.4.37 cpe:/o:linux:linux_kernel:3.2
OS details: DD-WRT v24-sp2 (Linux 2.4.37), Linux 3.2
Network Distance: 2 hops
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

TRACEROUTE (using port 80/tcp)
HOP RTT     ADDRESS
1   0.27 ms 172.16.206.2
2   0.21 ms pi-hole (192.168.0.7)

OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 18.41 seconds
[faraday](devel1) kali#
```

Once the nmap scan is finished, double-clicking on the host under the `Hosts` tab will bring up details about the host, its services, and any vulnerabilities that were detected.

![python-faraday](images/faraday-02-host.png)

The excellent dirb utility is also supported by Faraday by default:

```
[faraday](devel1) kali#  dirb http://192.168.0.23/commix-testbed -w 2>&1 | tee -a tmp.qNejUxvvrPpbGPVEfwf8OZOuM1F1E

-----------------
DIRB v2.22
By The Dark Raver
-----------------

START_TIME: Tue Mar  7 13:58:52 2017
URL_BASE: http://192.168.0.23/commix-testbed/
WORDLIST_FILES: /usr/share/dirb/wordlists/common.txt
OPTION: Not Stoping on warning messages

-----------------

GENERATED WORDS: 4612

---- Scanning URL: http://192.168.0.23/commix-testbed/ ----
==> DIRECTORY: http://192.168.0.23/commix-testbed/css/
==> DIRECTORY: http://192.168.0.23/commix-testbed/fonts/
==> DIRECTORY: http://192.168.0.23/commix-testbed/img/
+ http://192.168.0.23/commix-testbed/index.php (CODE:200|SIZE:14346)
==> DIRECTORY: http://192.168.0.23/commix-testbed/js/
==> DIRECTORY: http://192.168.0.23/commix-testbed/readme/

---- Entering directory: http://192.168.0.23/commix-testbed/css/ ----
(!) WARNING: Directory IS LISTABLE. No need to scan it.
    (Use mode '-w' if you want to scan it anyway)

---- Entering directory: http://192.168.0.23/commix-testbed/fonts/ ----
(!) WARNING: Directory IS LISTABLE. No need to scan it.
    (Use mode '-w' if you want to scan it anyway)

---- Entering directory: http://192.168.0.23/commix-testbed/img/ ----
(!) WARNING: Directory IS LISTABLE. No need to scan it.
    (Use mode '-w' if you want to scan it anyway)

---- Entering directory: http://192.168.0.23/commix-testbed/js/ ----
(!) WARNING: Directory IS LISTABLE. No need to scan it.
    (Use mode '-w' if you want to scan it anyway)

---- Entering directory: http://192.168.0.23/commix-testbed/readme/ ----
(!) WARNING: Directory IS LISTABLE. No need to scan it.
    (Use mode '-w' if you want to scan it anyway)

-----------------
END_TIME: Tue Mar  7 14:04:24 2017
DOWNLOADED: 27672 - FOUND: 1
```

When the scan is finished, double-clicking on the host will bring up its details, including the directories that dirb detected.

![python-faraday](images/faraday-03-vuln.png)

Take a look in the `/usr/share/python-faraday/plugins/repo` directory to see what other applications Faraday supports.

```
root@kali:/usr/share/python-faraday/plugins/repo# ls
acunetix  dnsrecon      listurl       netsparker     retina          wapiti
amap      dnswalk       maltego       nexpose        reverseraider   wcscan
appscan   fierce        masscan       nexpose-full   sentinel        webfuzzer
arachni   fruitywifi    medusa        nikto          skipfish        whois
arp-scan  ftp           metagoofil    nmap           sqlmap          wpscan
beef      goohost       metasploit    openvas        sshdefaultscan  x1
burp      hping3        metasploiton  pasteanalyzer  sslcheck        zap
dig       hydra         ndiff         peepingtom     telnet
dirb      impact        nessus        ping           theharvester
dnsenum   __init__.py   netcat        propecia       traceroute
dnsmap    __init__.pyc  netdiscover   qualysguard    w3af
```

Faraday also includes a full-featured web interface that provides you, your team, and any other interested parties with an immense amount of information.

![python-faraday](images/faraday-04-web.png)
