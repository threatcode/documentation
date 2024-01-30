---
Title: sprayingtoolkit
Homepage: https://github.com/byt3bl33d3r/SprayingToolkit
Repository: https://gitlab.com/kalilinux/packages/sprayingtoolkit
Architectures: all
Version: 0.0~git20201009.68f295d-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### sprayingtoolkit
 
  A set of Python scripts/utilities that tries to make password spraying attacks
  against Lync/S4B & OWA a lot quicker, less painful and more efficient.
 
 **Installed size:** `79 KB`  
 **How to install:** `sudo apt install sprayingtoolkit`  
 
 {{< spoiler "Dependencies:" >}}
 * kali-defaults
 * mitmproxy
 * python3
 * python3-boto3
 * python3-docopt
 * python3-imapclient
 * python3-lxml
 * python3-requests
 * python3-requests-ntlm
 * python3-termcolor
 * python3-urllib3
 {{< /spoiler >}}
 
 ##### atomizer
 
 
 ```
 root@kali:~# atomizer -h
 Usage:
     atomizer (lync|owa|imap) <target> <password> <userfile> [--targetPort PORT] [--threads THREADS] [--debug]
     atomizer (lync|owa|imap) <target> <passwordfile> <userfile> --interval <TIME> [--gchat <URL>] [--slack <URL>] [--targetPort PORT][--threads THREADS] [--debug]
     atomizer (lync|owa|imap) <target> --csvfile CSVFILE [--user-row-name NAME] [--pass-row-name NAME] [--targetPort PORT] [--threads THREADS] [--debug]
     atomizer (lync|owa|imap) <target> --user-as-pass USERFILE [--targetPort PORT] [--threads THREADS] [--debug]
     atomizer (lync|owa|imap) <target> --recon [--debug]
     atomizer -h | --help
     atomizer -v | --version
 
 Arguments:
     target         target domain or url
     password       password to spray
     userfile       file containing usernames (one per line)
     passwordfile   file containing passwords (one per line)
 
 Options:
     -h, --help               show this screen
     -v, --version            show version
     -c, --csvfile CSVFILE    csv file containing usernames and passwords
     -i, --interval TIME      spray at the specified interval [format: "H:M:S"]
     -t, --threads THREADS    number of concurrent threads to use [default: 3]
     -d, --debug              enable debug output
     -p, --targetPort PORT    target port of the IMAP server (IMAP only) [default: 993]
     --recon                  only collect info, don't password spray
     --gchat URL              gchat webhook url for notification
     --slack URL              slack webhook url for notification
     --user-row-name NAME     username row title in CSV file [default: Email Address]
     --pass-row-name NAME     password row title in CSV file [default: Password]
     --user-as-pass USERFILE  use the usernames in the specified file as the password (one per line)
 ```
 
 - - -
 
 ##### spindrift
 
 
 ```
 root@kali:~# spindrift -h
 Usage:
     spindrift [<file>] [--target TARGET | --domain DOMAIN] [--format FORMAT]
 
 Arguments:
     file    file containing names, can also read from stdin
 
 Options:
     --target TARGET   optional domain or url to retrieve the internal domain name from OWA
     --domain DOMAIN   manually specify the domain to append to each username
     --format FORMAT   username format [default: {f}{last}]
 ```
 
 - - -
 
 ##### sprayingtoolkit
 
 
 ```
 root@kali:~# sprayingtoolkit -h
 
 > sprayingtoolkit ~ Scripts to make password spraying attacks against Lync/S4B, OWA & O365
 
 /usr/share/sprayingtoolkit
 |-- aerosol.py
 |-- atomizer.py
 |-- core
 |-- spindrift.py
 `-- vaporizer.py
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
