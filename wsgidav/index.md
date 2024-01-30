---
Title: wsgidav
Homepage: https://github.com/mar10/wsgidav
Repository: https://gitlab.com/kalilinux/packages/wsgidav
Architectures: all
Version: 4.3.0-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### python-wsgidav-doc
 
  This package contains a generic and extendable WebDAV server written in Python
  and based on WSGI.
   
  This is the common documentation package.
 
 **Installed size:** `386.24 MB`  
 **How to install:** `sudo apt install python-wsgidav-doc`  
 
 {{< spoiler "Dependencies:" >}}
 * libjs-sphinxdoc 
 {{< /spoiler >}}
 
 
 - - -
 
 ### python3-wsgidav
 
  This package contains a generic and extendable WebDAV server written in Python
  and based on WSGI.
   
  This package installs the library for Python 3.
 
 **Installed size:** `615 KB`  
 **How to install:** `sudo apt install python3-wsgidav`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-cheroot
 * python3-defusedxml
 * python3-jinja2
 * python3-json5
 * python3-yaml
 {{< /spoiler >}}
 
 ##### wsgidav
 
 
 ```
 root@kali:~# wsgidav -h
 usage: wsgidav [-h] [-p PORT] [-H HOST] [-r ROOT_PATH]
                [--auth {anonymous,nt,pam-login}]
                [--server {cheroot,ext-wsgiutils,gevent,gunicorn,paste,uvicorn,wsgiref}]
                [--ssl-adapter {builtin,pyopenssl}] [-v | -q]
                [-c CONFIG_FILE | --no-config] [--browse] [-V]
 
 Run a WEBDAV server to share file system folders.
 
 Examples:
 
   Share filesystem folder '/temp' for anonymous access (no config file used):
     wsgidav --port=80 --host=0.0.0.0 --root=/temp --auth=anonymous
 
   Run using a specific configuration file:
     wsgidav --port=80 --host=0.0.0.0 --config=~/my_wsgidav.yaml
 
   If no config file is specified, the application will look for a file named
   'wsgidav.yaml' in the current directory.
   See
     https://wsgidav.readthedocs.io/en/latest/user_guide_configure.html
   for some explanation of the configuration file format.
   
 
 options:
   -h, --help            show this help message and exit
   -p PORT, --port PORT  port to serve on (default: 8080)
   -H HOST, --host HOST  host to serve from (default: localhost). 'localhost' is only accessible from the local computer. Use 0.0.0.0 to make your application public
   -r ROOT_PATH, --root ROOT_PATH
                         path to a file system folder to publish as share '/'.
   --auth {anonymous,nt,pam-login}
                         quick configuration of a domain controller when no config file is used
   --server {cheroot,ext-wsgiutils,gevent,gunicorn,paste,uvicorn,wsgiref}
                         type of pre-installed WSGI server to use (default: cheroot).
   --ssl-adapter {builtin,pyopenssl}
                         used by 'cheroot' server if SSL certificates are configured (default: builtin).
   -v, --verbose         increment verbosity by one (default: 3, range: 0..5)
   -q, --quiet           decrement verbosity by one
   -c CONFIG_FILE, --config CONFIG_FILE
                         configuration file (default: ('wsgidav.yaml', 'wsgidav.json') in current directory)
   --no-config           do not try to load default ('wsgidav.yaml', 'wsgidav.json')
   --browse              open browser on start
   -V, --version         print version info and exit (may be combined with --verbose)
 
 Licensed under the MIT license.
 See https://github.com/mar10/wsgidav for additional information.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
