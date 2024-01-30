---
Title: sliver
Homepage: https://github.com/BishopFox/sliver
Repository: https://gitlab.com/kalilinux/packages/sliver
Architectures: amd64 arm64
Version: 1.5.41-0kali2
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### sliver
 
  This package contains a general purpose cross-platform implant framework that
  supports C2 over Mutual-TLS, HTTP(S), and DNS. Implants are dynamically
  compiled with unique X.509 certificates signed by a per-instance certificate
  authority generated when you first run the binary.
 
 **Installed size:** `195.43 MB`  
 **How to install:** `sudo apt install sliver`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### sliver-client
 
 
 ```
 root@kali:~# sliver-client -h
 Usage:
   sliver-client [flags]
   sliver-client [command]
 
 Available Commands:
   completion  Generate the autocompletion script for the specified shell
   help        Help about any command
   import      Import a client configuration file
   version     Print version and exit
 
 Flags:
   -h, --help   help for sliver-client
 
 Use "sliver-client [command] --help" for more information about a command.
 ```
 
 - - -
 
 ##### sliver-server
 
 
 ```
 root@kali:~# sliver-server -h
 Usage:
   sliver-server [flags]
   sliver-server [command]
 
 Available Commands:
   builder     Start the process as an external builder
   completion  Generate the autocompletion script for the specified shell
   daemon      Force start server in daemon mode
   export-ca   Export certificate authority
   help        Help about any command
   import-ca   Import certificate authority
   operator    Generate operator configuration files
   unpack      Unpack assets and exit
   version     Print version and exit
 
 Flags:
   -h, --help   help for sliver-server
 
 Use "sliver-server [command] --help" for more information about a command.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
