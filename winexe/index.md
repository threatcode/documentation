---
Title: winexe
Homepage: https://sourceforge.net/projects/winexe
Repository: https://gitlab.com/kalilinux/packages/winexe
Architectures: any
Version: 1.1~20140107-0kali18
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-passwords 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### winexe
 
  Winexe remotely executes commands on Windows NT/2000/XP/2003 systems from
  GNU/Linux (and possibly also from other Unices capable of building the Samba 4
  software package).
 
 **Installed size:** `157 KB`  
 **How to install:** `sudo apt install winexe`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libpopt0 
 * libtalloc2 
 * libtevent0 
 * samba-libs 
 {{< /spoiler >}}
 
 ##### winexe
 
 Execute a remote Windows command
 
 ```
 root@kali:~# winexe -h
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
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## winexe Usage Example

With the given credentials (`-U ‘Administrator%s3cr3t’`), connect to the remote server (`//192.168.1.225`), and execute the given command (`cmd.exe /c echo “this is running on windows”`):

```
root@kali:~# winexe -U 'Administrator%s3cr3t' //192.168.1.225 'cmd.exe /c echo "this is running on windows"'
"this is running on windows"
```
