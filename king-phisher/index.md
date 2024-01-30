---
archived: "true"
Title: king-phisher
Homepage: https://github.com/securestate/king-phisher
Repository: https://gitlab.com/kalilinux/packages/king-phisher
Architectures: all
Version: 1.15.0+git20220130-0kali1
Metapackages: kali-linux-default kali-linux-everything kali-linux-large 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### king-phisher
 
  This package contains is a tool for testing and promoting user awareness by
  simulating real world phishing attacks. It features an easy to use, yet very
  flexible architecture allowing full control over both emails and server
  content. King Phisher can be used to run campaigns ranging from simple
  awareness training to more complicated scenarios in which user aware content
  is served for harvesting credentials.
 
 **Installed size:** `66.04 MB`  
 **How to install:** `sudo apt install king-phisher`  
 
 {{< spoiler "Dependencies:" >}}
 * adduser
 * fonts-font-awesome
 * fonts-lato
 * gir1.2-gtk-3.0
 * gir1.2-gtksource-3.0
 * gir1.2-vte-2.91
 * gir1.2-webkit2-4.0
 * gobject-introspection
 * libjs-jquery
 * libjs-underscore
 * postgresql
 * pwgen
 * python3
 * python3-advancedhttpserver 
 * python3-alembic 
 * python3-asn1crypto
 * python3-blinker 
 * python3-boltons 
 * python3-cairo-dev
 * python3-cryptography
 * python3-dateutil 
 * python3-dnspython 
 * python3-ecdsa 
 * python3-email-validator
 * python3-geoip2 
 * python3-geojson 
 * python3-gi
 * python3-gi-cairo
 * python3-graphene 
 * python3-graphene-sqlalchemy 
 * python3-graphql-core 
 * python3-graphql-relay 
 * python3-icalendar 
 * python3-jinja2 
 * python3-jsonschema 
 * python3-markdown
 * python3-markupsafe 
 * python3-matplotlib 
 * python3-msgpack 
 * python3-numpy
 * python3-pampy
 * python3-paramiko 
 * python3-pluginbase 
 * python3-psycopg2 
 * python3-pyotp 
 * python3-requests 
 * python3-requests-file 
 * python3-rule-engine
 * python3-six 
 * python3-smoke-zephyr 
 * python3-sqlalchemy 
 * python3-termcolor 
 * python3-tz 
 * python3-tzlocal 
 * python3-websocket 
 * python3-xlsxwriter 
 * python3-yaml 
 {{< /spoiler >}}
 
 ##### king-phisher-client
 
 
 ```
 root@kali:~# king-phisher-client -h
 usage: KingPhisher [-h] [-v] [-L {DEBUG,INFO,WARNING,ERROR,FATAL}]
                    [--logger LOGGER] [--gc-debug-leak] [--gc-debug-stats]
                    [-c CONFIG_FILE] [--no-plugins] [--no-style]
 
 King Phisher Client GUI
 
 options:
   -h, --help            show this help message and exit
   -v, --version         show program's version number and exit
 
 logging options:
   -L {DEBUG,INFO,WARNING,ERROR,FATAL}, --log {DEBUG,INFO,WARNING,ERROR,FATAL}
                         set the logging level
   --logger LOGGER       specify the root logger
 
 garbage collector options:
   --gc-debug-leak       set the DEBUG_LEAK flag
   --gc-debug-stats      set the DEBUG_STATS flag
 
 client specific options:
   -c CONFIG_FILE, --config CONFIG_FILE
                         specify a configuration file to use
   --no-plugins          disable all plugins
   --no-style            disable interface styling
 ```
 
 - - -
 
 ##### king-phisher-server
 
 
 ```
 root@kali:~# king-phisher-server -h
 usage: KingPhisherServer [-h] [-v] [-L {DEBUG,INFO,WARNING,ERROR,FATAL}]
                          [--logger LOGGER] [--gc-debug-leak]
                          [--gc-debug-stats] [-f] [--verify-config]
                          config_file
 
 King Phisher Server
 
 options:
   -h, --help            show this help message and exit
   -v, --version         show program's version number and exit
 
 logging options:
   -L {DEBUG,INFO,WARNING,ERROR,FATAL}, --log {DEBUG,INFO,WARNING,ERROR,FATAL}
                         set the logging level
   --logger LOGGER       specify the root logger
 
 garbage collector options:
   --gc-debug-leak       set the DEBUG_LEAK flag
   --gc-debug-stats      set the DEBUG_STATS flag
 
 server specific options:
   -f, --foreground      run in the foreground (do not fork)
   --verify-config       verify the configuration and exit
   config_file           configuration file to use
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
