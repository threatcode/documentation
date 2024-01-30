---
Title: passing-the-hash
Homepage: http://passing-the-hash.blogspot.fr
Repository: https://gitlab.com/kalilinux/packages/passing-the-hash
Architectures: any
Version: 0~2015.12.34
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-passwords 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### passing-the-hash
 
  This package contains modified versions of Curl, Iceweasel, FreeTDS, Samba 4,
  WinEXE and WMI. They are installed as executables starting with the "pth-"
  string.
 
 **Installed size:** `13.88 MB`  
 **How to install:** `sudo apt install passing-the-hash`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libcrypt1 
 * libgmp10 
 * libgnutls30 
 * libgssapi-krb5-2 
 * libhogweed6
 * libidn2-0 
 * libldap-2.5-0 
 * libnettle8
 * librtmp1 
 * libssl3 
 * samba-common-bin 
 * smbclient 
 * sqsh
 * winexe
 * zlib1g 
 {{< /spoiler >}}
 
 ##### pth-curl
 
 
 ```
 root@kali:~# pth-curl -h
 Usage: curl [options...] <url>
  -d, --data <data>          HTTP POST data
  -f, --fail                 Fail fast with no output on HTTP errors
  -h, --help <category>      Get help for commands
  -i, --include              Include protocol response headers in the output
  -o, --output <file>        Write to file instead of stdout
  -O, --remote-name          Write output to a file named as the remote file
  -s, --silent               Silent mode
  -T, --upload-file <file>   Transfer local FILE to destination
  -u, --user <user:password> Server user and password
  -A, --user-agent <name>    Send User-Agent <name> to server
  -v, --verbose              Make the operation more talkative
  -V, --version              Show version number and quit
 
 This is not the full help, this menu is stripped into categories.
 Use "--help category" to get an overview of all categories.
 For all options use the manual or "--help all".
 ```
 
 - - -
 
 ##### pth-net
 
 
 ```
 root@kali:~# pth-net -h
 Usage:
   Use 'net help rpc' to get more extensive information about 'net rpc' commands.
   Use 'net help rap' to get more extensive information about 'net rap' commands.
   Use 'net help ads' to get more extensive information about 'net ads' commands.
   Use 'net help file' to get more information about 'net file' commands.
   Use 'net help share' to get more information about 'net share' commands.
   Use 'net help session' to get more information about 'net session' commands.
   Use 'net help server' to get more information about 'net server' commands.
   Use 'net help domain' to get more information about 'net domain' commands.
   Use 'net help printq' to get more information about 'net printq' commands.
   Use 'net help user' to get more information about 'net user' commands.
   Use 'net help group' to get more information about 'net group' commands.
   Use 'net help groupmap' to get more information about 'net groupmap' commands.
   Use 'net help sam' to get more information about 'net sam' commands.
   Use 'net help validate' to get more information about 'net validate' commands.
   Use 'net help groupmember' to get more information about 'net groupmember' commands.
   Use 'net help admin' to get more information about 'net admin' commands.
   Use 'net help service' to get more information about 'net service' commands.
   Use 'net help password' to get more information about 'net password' commands.
   Use 'net help primarytrust' to get more extensive information about 'net primarytrust' commands.
   Use 'net help changetrustpw' to get more information about 'net changetrustpw'.
   net [options] changesecretpw
     Change the ADS domain member machine account password in secrets.tdb.
     Do NOT use this function unless you know what it does.
     Requires the -f flag to work.
   net -U user[%%password] [-W domain] setauthuser
     Set the auth user, password (and optionally domain
     Will prompt for password if not given.
   net setauthuser delete
     Delete the existing auth user settings.
   net getauthuser
     Get the current winbind auth user settings.
   Use 'net help time' to get more information about 'net time' commands.
   Use 'net help lookup' to get more information about 'net lookup' commands.
   Use 'net help g_lock' to get more information about 'net g_lock' commands.
   Use 'net help join' to get more information about 'net join'.
   Use 'net help offlinejoin' to get more information about 'net offlinejoin'.
   Use 'net help dom' to get more information about 'net dom' commands.
   Use 'net help cache' to get more information about 'net cache' commands.
   net getlocalsid
   net setlocalsid S-1-5-21-x-y-z
   net setdomainsid S-1-5-21-x-y-z
   net getdomainsid
   net maxrid
   Use 'net help idmap to get more information about 'net idmap' commands.
   Use 'net help status' to get more information about 'net status' commands.
   Use 'net help usershare to get more information about 'net usershare' commands.
   Use 'net help usersidlist' to get more information about 'net usersidlist'.
   Use 'net help conf' to get more information about 'net conf' commands.
   Use 'net help registry' to get more information about 'net registry' commands.
   Use 'net help eventlog' to get more information about 'net eventlog' commands.
   Use 'net help printing' to get more information about 'net printing' commands.
   Use 'net help serverid' to get more information about 'net serverid' commands.
   Use 'net help notify' to get more information about 'net notify' commands.
   Use 'net help tdb' to get more information about 'net tdb' commands.
   Use 'net help vfs' to get more information about 'net vfs' commands.
   Use 'net help help' to list usage information for 'net' commands.
 ```
 
 - - -
 
 ##### pth-rpcclient
 
 
 ```
 root@kali:~# pth-rpcclient --help
 Usage: rpcclient [OPTION...] BINDING-STRING|HOST
 Options:
   -c, --command=COMMANDS                       Execute semicolon separated cmds
   -I, --dest-ip=IP                             Specify destination IP address
   -p, --port=PORT                              Specify port number
 
 Help options:
   -?, --help                                   Show this help message
       --usage                                  Display brief usage message
 
 Common Samba options:
   -d, --debuglevel=DEBUGLEVEL                  Set debug level
       --debug-stdout                           Send debug output to standard
                                                output
   -s, --configfile=CONFIGFILE                  Use alternative configuration
                                                file
       --option=name=value                      Set smb.conf option from
                                                command line
   -l, --log-basename=LOGFILEBASE               Basename for log/debug files
       --leak-report                            enable talloc leak reporting on
                                                exit
       --leak-report-full                       enable full talloc leak
                                                reporting on exit
 
 Connection options:
   -R, --name-resolve=NAME-RESOLVE-ORDER        Use these name resolution
                                                services only
   -O, --socket-options=SOCKETOPTIONS           socket options to use
   -m, --max-protocol=MAXPROTOCOL               Set max protocol level
   -n, --netbiosname=NETBIOSNAME                Primary netbios name
       --netbios-scope=SCOPE                    Use this Netbios scope
   -W, --workgroup=WORKGROUP                    Set the workgroup name
       --realm=REALM                            Set the realm name
 
 Credential options:
   -U, --user=[DOMAIN/]USERNAME[%PASSWORD]      Set the network username
   -N, --no-pass                                Don't ask for a password
       --password=STRING                        Password
       --pw-nt-hash                             The supplied password is the NT
                                                hash
   -A, --authentication-file=FILE               Get the credentials from a file
   -P, --machine-pass                           Use stored machine account
                                                password
       --simple-bind-dn=DN                      DN to use for a simple bind
       --use-kerberos=desired|required|off      Use Kerberos authentication
       --use-krb5-ccache=CCACHE                 Credentials cache location for
                                                Kerberos
       --use-winbind-ccache                     Use the winbind ccache for
                                                authentication
       --client-protection=sign|encrypt|off     Configure used protection for
                                                client connections
 
 Deprecated legacy options:
   -k, --kerberos                               DEPRECATED: Migrate to
                                                --use-kerberos
 
 Version options:
   -V, --version                                Print version
 ```
 
 - - -
 
 ##### pth-smbclient
 
 
 ```
 root@kali:~# pth-smbclient --help
 Usage: smbclient [OPTIONS] service <password>
   -M, --message=HOST                           Send message
   -I, --ip-address=IP                          Use this IP to connect to
   -E, --stderr                                 Write messages to stderr
                                                instead of stdout
   -L, --list=HOST                              Get a list of shares available
                                                on a host
   -T, --tar=<c|x>IXFvgbNan                     Command line tar
   -D, --directory=DIR                          Start from directory
   -c, --command=STRING                         Execute semicolon separated
                                                commands
   -b, --send-buffer=BYTES                      Changes the transmit/send buffer
   -t, --timeout=SECONDS                        Changes the per-operation
                                                timeout
   -p, --port=PORT                              Port to connect to
   -g, --grepable                               Produce grepable output
   -q, --quiet                                  Suppress help message
   -B, --browse                                 Browse SMB servers using DNS
 
 Help options:
   -?, --help                                   Show this help message
       --usage                                  Display brief usage message
 
 Common Samba options:
   -d, --debuglevel=DEBUGLEVEL                  Set debug level
       --debug-stdout                           Send debug output to standard
                                                output
   -s, --configfile=CONFIGFILE                  Use alternative configuration
                                                file
       --option=name=value                      Set smb.conf option from
                                                command line
   -l, --log-basename=LOGFILEBASE               Basename for log/debug files
       --leak-report                            enable talloc leak reporting on
                                                exit
       --leak-report-full                       enable full talloc leak
                                                reporting on exit
 
 Connection options:
   -R, --name-resolve=NAME-RESOLVE-ORDER        Use these name resolution
                                                services only
   -O, --socket-options=SOCKETOPTIONS           socket options to use
   -m, --max-protocol=MAXPROTOCOL               Set max protocol level
   -n, --netbiosname=NETBIOSNAME                Primary netbios name
       --netbios-scope=SCOPE                    Use this Netbios scope
   -W, --workgroup=WORKGROUP                    Set the workgroup name
       --realm=REALM                            Set the realm name
 
 Credential options:
   -U, --user=[DOMAIN/]USERNAME[%PASSWORD]      Set the network username
   -N, --no-pass                                Don't ask for a password
       --password=STRING                        Password
       --pw-nt-hash                             The supplied password is the NT
                                                hash
   -A, --authentication-file=FILE               Get the credentials from a file
   -P, --machine-pass                           Use stored machine account
                                                password
       --simple-bind-dn=DN                      DN to use for a simple bind
       --use-kerberos=desired|required|off      Use Kerberos authentication
       --use-krb5-ccache=CCACHE                 Credentials cache location for
                                                Kerberos
       --use-winbind-ccache                     Use the winbind ccache for
                                                authentication
       --client-protection=sign|encrypt|off     Configure used protection for
                                                client connections
 
 Deprecated legacy options:
   -k, --kerberos                               DEPRECATED: Migrate to
                                                --use-kerberos
 
 Version options:
   -V, --version                                Print version
 ```
 
 - - -
 
 ##### pth-smbget
 
 
 ```
 root@kali:~# pth-smbget --help
 Usage: smbget [OPTION...]
   -a, --guest                                  Work as user guest
   -e, --encrypt                                Encrypt SMB transport
   -r, --resume                                 Automatically resume aborted
                                                files
   -u, --update                                 Download only when remote file
                                                is newer than local file or
                                                local file is missing
       --recursive                              Recursively download files
   -b, --blocksize=INT                          Change number of bytes in a
                                                block
   -o, --outputfile=STRING                      Write downloaded data to
                                                specified file
       --stdout                                 Write data to stdout
   -D, --dots                                   Show dots as progress indication
   -q, --quiet                                  Be quiet
   -v, --verbose                                Be verbose
       --limit-rate=INT                         Limit download speed to this
                                                many KB/s
 
 Help options:
   -?, --help                                   Show this help message
       --usage                                  Display brief usage message
 
 Common Samba options:
   -d, --debuglevel=DEBUGLEVEL                  Set debug level
       --debug-stdout                           Send debug output to standard
                                                output
   -s, --configfile=CONFIGFILE                  Use alternative configuration
                                                file
       --option=name=value                      Set smb.conf option from
                                                command line
   -l, --log-basename=LOGFILEBASE               Basename for log/debug files
       --leak-report                            enable talloc leak reporting on
                                                exit
       --leak-report-full                       enable full talloc leak
                                                reporting on exit
 
 Connection options:
   -R, --name-resolve=NAME-RESOLVE-ORDER        Use these name resolution
                                                services only
   -O, --socket-options=SOCKETOPTIONS           socket options to use
   -m, --max-protocol=MAXPROTOCOL               Set max protocol level
   -n, --netbiosname=NETBIOSNAME                Primary netbios name
       --netbios-scope=SCOPE                    Use this Netbios scope
   -W, --workgroup=WORKGROUP                    Set the workgroup name
       --realm=REALM                            Set the realm name
 
 Credential options:
   -U, --user=[DOMAIN/]USERNAME[%PASSWORD]      Set the network username
   -N, --no-pass                                Don't ask for a password
       --password=STRING                        Password
       --pw-nt-hash                             The supplied password is the NT
                                                hash
   -A, --authentication-file=FILE               Get the credentials from a file
   -P, --machine-pass                           Use stored machine account
                                                password
       --simple-bind-dn=DN                      DN to use for a simple bind
       --use-kerberos=desired|required|off      Use Kerberos authentication
       --use-krb5-ccache=CCACHE                 Credentials cache location for
                                                Kerberos
       --use-winbind-ccache                     Use the winbind ccache for
                                                authentication
       --client-protection=sign|encrypt|off     Configure used protection for
                                                client connections
 
 Deprecated legacy options:
   -k, --kerberos                               DEPRECATED: Migrate to
                                                --use-kerberos
 
 Version options:
   -V, --version                                Print version
 ```
 
 - - -
 
 ##### pth-sqsh
 
 
 ```
 root@kali:~# pth-sqsh --help
 Use: sqsh [-a count] [-A packet_size] [-b] [-B] [-c [cmdend]] [-C sql]
           [-d severity] [-D database] [-e] [-E editor] [-f severity]
           [-G TDS version] [-h] [-H hostname] [-i filename] [-I interfaces]
           [-J charset] [-k keywords] [-K keytab] [-l level|flags]
           [-L var=value] [-m style] [-n {on|off}] [-N appname] [-o filename]
           [-p] [-P [password]] [-Q query_timeout] [-r [sqshrc]]
           [-R principal] [-s colsep] [-S server] [-t [filter]]
           [-T login_timeout] [-U username] [-v] [-V [bcdimoqru]] [-w width]
           [-X] [-y directory] [-z language] [-Z [secmech]]
           [--appname        appname] [--clientapplname clientapplname]
           [--clienthostname clienthostname] [--clientname     clientname]
           [--hostname       hostname] [--help          ] [--version       ]
 
  -a  Max. # of errors before abort       -p  Display performance stats
  -A  Adjust TDS packet size              -P  Sybase password (NULL)
  -b  Suppress banner message on startup  -Q  Query timeout period in seconds
  -B  Turn off file buffering on startup  -r  Specify name of .sqshrc
  -c  Alias for the 'go' command          -R  Network security server principal
  -C  Send sql statement to server        -s  Alternate column separator (\t)
  -d  Min. severity level to display      -S  Name of Sybase server ($DSQUERY)
  -D  Change database context on startup  -t  Filter batches through program
  -e  Echo batch prior to executing       -T  Login timeout period in seconds
  -E  Replace default editor (vi)         -U  Name of Sybase user
  -f  Min. severity level for failure     -v  Display current version and exit
  -G  TDS version to use                  -V  Request network security services
  -h  Disable headers and footers         -w  Adjust result display width
  -H  Set the client hostname             -X  Enable client password encryption
  -i  Read input from file                -y  Override value of $SYBASE
  -I  Alternate interfaces file           -z  Alternate display language
  -J  Client character set                -Z  Network security mechanism
  -k  Specify alternate keywords file     --appname         Set application name
  -K  Network security keytab file (DCE)  --clientapplname  Set client appl name
  -l  Set debugging level                 --clienthostname  Set client host name
  -L  Set the value of a given variable   --clientname      Set client name
  -m  Set display mode                    --hostname        Set hostname
  -n  Set chained transaction mode        --help            Show help text only
  -N  Set application name (sqsh-3.0)     --version         Show version only
  -o  Direct all output to file          
 
 ```
 
 - - -
 
 ##### pth-winexe
 
 
 ```
 root@kali:~# pth-winexe -h
 Usage: winexe [OPTION]... //HOST COMMAND
 Options:
   -h, --help                                  Display help message
   -V, --version                               Display version number
   -U, --user=[DOMAIN/]USERNAME[%PASSWORD]     Set the network username
   -A, --authentication-file=FILE              Get the credentials from a file
   -N, --no-pass                               Do not ask for a password
   -k, --kerberos=STRING                       Use Kerberos, -k [yes|no]
   -d, --debuglevel=DEBUGLEVEL                 Set debug level
       --uninstall                             Uninstall winexe service after
                                               remote execution
       --reinstall                             Reinstall winexe service before
                                               remote execution
       --system                                Use SYSTEM account
       --profile                               Load user profile
       --convert                               Try to convert characters
                                               between local and remote
                                               code-pages
       --runas=[DOMAIN\]USERNAME%PASSWORD      Run as the given user (BEWARE:
                                               this password is sent in
                                               cleartext over the network!)
       --runas-file=FILE                       Run as user options defined in a
                                               file
       --interactive=0|1                       Desktop interaction: 0 -
                                               disallow, 1 - allow. If allow,
                                               also use the --system switch
                                               (Windows requirement). Vista
                                               does not support this option.
       --ostype=0|1|2                          OS type: 0 - 32-bit, 1 - 64-bit,
                                               2 - winexe will decide.
                                               Determines which version (32-bit
                                               or 64-bit) of service will be
                                               installed.
 ```
 
 - - -
 
 ##### pth-wmic
 
 
 ```
 root@kali:~# pth-wmic --help
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
 
 ##### pth-wmis
 
 
 ```
 root@kali:~# pth-wmis --help
 Usage: //host
 
 Example: wmis -U [domain/]adminuser%password //host cmd.exe /c dir c:\ > c:\windows\temp\output.txt 
 
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
