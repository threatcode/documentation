---
Title: smbmap
Homepage: https://github.com/ShawnDEvans/smbmap
Repository: https://salsa.debian.org/pkg-security-team/smbmap
Architectures: all
Version: 1.9.2-1
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-information-gathering kali-tools-passwords 
Icon: images/smbmap-logo.svg
PackagesInfo: |
 ### smbmap
 
  SMBMap allows users to enumerate samba share drives across an entire domain.
  List share drives, drive permissions, share contents, upload/download
  functionality, file name auto-download pattern matching, and even execute
  remote commands. This tool was designed with pen testing in mind, and is
  intended to simplify searching for potentially sensitive data across large
  networks.
 
 **Installed size:** `111 KB`  
 **How to install:** `sudo apt install smbmap`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-impacket
 * python3-pyasn1
 * python3-termcolor
 {{< /spoiler >}}
 
 ##### smbmap
 
 SMB enumeration tool
 
 ```
 root@kali:~# smbmap -h
 usage: smbmap [-h] (-H HOST | --host-file FILE) [-u USERNAME]
               [-p PASSWORD | --prompt] [-s SHARE] [-d DOMAIN] [-P PORT] [-v]
               [--admin] [--no-banner] [--no-color] [--no-update]
               [--timeout SCAN_TIMEOUT] [-x COMMAND] [--mode CMDMODE]
               [-L | -r [PATH]] [-A PATTERN | -g FILE | --csv FILE]
               [--dir-only] [--no-write-check] [-q] [--depth DEPTH]
               [--exclude SHARE [SHARE ...]] [-F PATTERN] [--search-path PATH]
               [--search-timeout TIMEOUT] [--download PATH] [--upload SRC DST]
               [--delete PATH TO FILE] [--skip]
 
     ________  ___      ___  _______   ___      ___       __         _______
    /"       )|"  \    /"  ||   _  "\ |"  \    /"  |     /""\       |   __ "\
   (:   \___/  \   \  //   |(. |_)  :) \   \  //   |    /    \      (. |__) :)
    \___  \    /\  \/.    ||:     \/   /\   \/.    |   /' /\  \     |:  ____/
     __/  \   |: \.        |(|  _  \  |: \.        |  //  __'  \    (|  /
    /" \   :) |.  \    /:  ||: |_)  :)|.  \    /:  | /   /  \   \  /|__/ \
   (_______/  |___|\__/|___|(_______/ |___|\__/|___|(___/    \___)(_______)
  -----------------------------------------------------------------------------
      SMBMap - Samba Share Enumerator | Shawn Evans - ShawnDEvans@gmail.com
                      https://github.com/ShawnDEvans/smbmap
 
 options:
   -h, --help            show this help message and exit
 
 Main arguments:
   -H HOST               IP of host
   --host-file FILE      File containing a list of hosts
   -u USERNAME           Username, if omitted null session assumed
   -p PASSWORD           Password or NTLM hash
   --prompt              Prompt for a password
   -s SHARE              Specify a share (default C$), ex 'C$'
   -d DOMAIN             Domain name (default WORKGROUP)
   -P PORT               SMB port (default 445)
   -v                    Return the OS version of the remote host
   --admin               Just report if the user is an admin
   --no-banner           Removes the banner from the top of the output
   --no-color            Removes the color from output
   --no-update           Removes the "Working on it" message
   --timeout SCAN_TIMEOUT
                         Set port scan socket timeout. Default is .5 seconds
 
 Command Execution:
   Options for executing commands on the specified host
 
   -x COMMAND            Execute a command ex. 'ipconfig /all'
   --mode CMDMODE        Set the execution method, wmi or psexec, default wmi
 
 Shard drive Search:
   Options for searching/enumerating the share of the specified host(s)
 
   -L                    List all drives on the specified host, requires ADMIN
                         rights.
   -r [PATH]             Recursively list dirs and files (no share\path lists
                         the root of ALL shares), ex. 'email/backup'
   -A PATTERN            Define a file name pattern (regex) that auto downloads
                         a file on a match (requires -r), not case sensitive,
                         ex '(web|global).(asax|config)'
   -g FILE               Output to a file in a grep friendly format, used with
                         -r (otherwise it outputs nothing), ex -g grep_out.txt
   --csv FILE            Output to a CSV file, ex --csv shares.csv
   --dir-only            List only directories, ommit files.
   --no-write-check      Skip check to see if drive grants WRITE access.
   -q                    Quiet verbose output. Only shows shares you have READ
                         or WRITE on, and suppresses file listing when
                         performing a search (-A).
   --depth DEPTH         Traverse a directory tree to a specific depth. Default
                         is 5.
   --exclude SHARE [SHARE ...]
                         Exclude share(s) from searching and listing, ex.
                         --exclude ADMIN$ C$'
 
 File Content Search:
   Options for searching the content of files (must run as root), kind of experimental
 
   -F PATTERN            File content search, -F '[Pp]assword' (requires admin
                         access to execute commands, and PowerShell on victim
                         host)
   --search-path PATH    Specify drive/path to search (used with -F, default
                         C:\Users), ex 'D:\HR\'
   --search-timeout TIMEOUT
                         Specifcy a timeout (in seconds) before the file search
                         job gets killed. Default is 300 seconds.
 
 Filesystem interaction:
   Options for interacting with the specified host's filesystem
 
   --download PATH       Download a file from the remote system,
                         ex.'C$\temp\passwords.txt'
   --upload SRC DST      Upload a file to the remote system ex.
                         '/tmp/payload.exe C$\temp\payload.exe'
   --delete PATH TO FILE
                         Delete a remote file, ex. 'C$\temp\msf.exe'
   --skip                Skip delete file confirmation prompt
 
 Examples:
 
 $ smbmap -u jsmith -p password1 -d workgroup -H 192.168.0.1
 $ smbmap -u jsmith -p 'aad3b435b51404eeaad3b435b51404ee:da76f2c4c96028b7a6111aef4a50a94d' -H 172.16.0.20
 $ smbmap -u 'apadmin' -p 'asdf1234!' -d ACME -Hh 10.1.3.30 -x 'net group "Domain Admins" /domain'
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## smbmap Usage Examples

Check for shares on the specified host with the username and password provided:

```
root@kali:~# smbmap -u victim -p s3cr3t -H 192.168.86.61
[+] Finding open SMB ports....
[+] User SMB session establishd on 192.168.86.61...
[+] IP: 192.168.86.61:445   Name: win7-x86.lan
    Disk                                                    Permissions
    ----                                                    -----------
    ADMIN$                                              NO ACCESS
    C$                                                  NO ACCESS
    IPC$                                                NO ACCESS
    Users                                               READ ONLY
```
