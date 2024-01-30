---
Title: wmi
Homepage: 
Repository: https://gitlab.com/kalilinux/packages/wmi
Architectures: any
Version: 1.3.16-0kali8
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### wmi-client
 
  This DCOM/WMI client implementation is based on Samba4
  sources. It uses RPC/DCOM mechanisms to interact with WMI
  services on Windows 2000/XP/2003 machines.
   
  This package contains the command line client to perform
  remote command execution on Windows systems.
 
 **Installed size:** `9.06 MB`  
 **How to install:** `sudo apt install wmi-client`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libcrypt1 
 {{< /spoiler >}}
 
 ##### wmic
 
 
 ```
 root@kali:~# wmic --help
 Usage: //host query
 
 Example: wmic -U [domain/]adminuser%password //host "select * from Win32_ComputerSystem"
   --namespace=STRING                          WMI namespace, default to
                                               root\cimv2
   --delimiter=STRING                          delimiter to use when querying
                                               multiple values, default to '|'
 
 Help options:
   -?, --help                                  Show this help message
   --usage                                     Display brief usage message
 
 Common samba options:
   -d, --debuglevel=DEBUGLEVEL                 Set debug level
   --debug-stderr                              Send debug output to STDERR
   -s, --configfile=CONFIGFILE                 Use alternative configuration
                                               file
   --option=name=value                         Set smb.conf option from command
                                               line
   -l, --log-basename=LOGFILEBASE              Basename for log/debug files
   --leak-report                               enable talloc leak reporting on
                                               exit
   --leak-report-full                          enable full talloc leak
                                               reporting on exit
 
 Connection options:
   -R, --name-resolve=NAME-RESOLVE-ORDER       Use these name resolution
                                               services only
   -O, --socket-options=SOCKETOPTIONS          socket options to use
   -n, --netbiosname=NETBIOSNAME               Primary netbios name
   -W, --workgroup=WORKGROUP                   Set the workgroup name
   --realm=REALM                               Set the realm name
   -i, --scope=SCOPE                           Use this Netbios scope
   -m, --maxprotocol=MAXPROTOCOL               Set max protocol level
 
 Authentication options:
   -U, --user=[DOMAIN\]USERNAME[%PASSWORD]     Set the network username
   -N, --no-pass                               Don't ask for a password
   --password=STRING                           Password
   -A, --authentication-file=FILE              Get the credentials from a file
   -S, --signing=on|off|required               Set the client signing state
   -P, --machine-pass                          Use stored machine account
                                               password (implies -k)
   --simple-bind-dn=STRING                     DN to use for a simple bind
   -k, --kerberos=STRING                       Use Kerberos
   --use-security-mechanisms=STRING            Restricted list of
                                               authentication mechanisms
                                               available for use with this
                                               authentication
 
 Common samba options:
   -V, --version                               Print version
 ```
 
 - - -
 
 ##### wmis
 
 
 ```
 root@kali:~# wmis --help
 Usage: //host
 
 Example: wmis -U [domain/]adminuser%password //host
 
 Help options:
   -?, --help                                  Show this help message
   --usage                                     Display brief usage message
 
 Common samba options:
   -d, --debuglevel=DEBUGLEVEL                 Set debug level
   --debug-stderr                              Send debug output to STDERR
   -s, --configfile=CONFIGFILE                 Use alternative configuration
                                               file
   --option=name=value                         Set smb.conf option from command
                                               line
   -l, --log-basename=LOGFILEBASE              Basename for log/debug files
   --leak-report                               enable talloc leak reporting on
                                               exit
   --leak-report-full                          enable full talloc leak
                                               reporting on exit
 
 Connection options:
   -R, --name-resolve=NAME-RESOLVE-ORDER       Use these name resolution
                                               services only
   -O, --socket-options=SOCKETOPTIONS          socket options to use
   -n, --netbiosname=NETBIOSNAME               Primary netbios name
   -W, --workgroup=WORKGROUP                   Set the workgroup name
   --realm=REALM                               Set the realm name
   -i, --scope=SCOPE                           Use this Netbios scope
   -m, --maxprotocol=MAXPROTOCOL               Set max protocol level
 
 Authentication options:
   -U, --user=[DOMAIN\]USERNAME[%PASSWORD]     Set the network username
   -N, --no-pass                               Don't ask for a password
   --password=STRING                           Password
   -A, --authentication-file=FILE              Get the credentials from a file
   -S, --signing=on|off|required               Set the client signing state
   -P, --machine-pass                          Use stored machine account
                                               password (implies -k)
   --simple-bind-dn=STRING                     DN to use for a simple bind
   -k, --kerberos=STRING                       Use Kerberos
   --use-security-mechanisms=STRING            Restricted list of
                                               authentication mechanisms
                                               available for use with this
                                               authentication
 
 Common samba options:
   -V, --version                               Print version
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
