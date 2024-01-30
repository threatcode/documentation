---
Title: odat
Homepage: https://github.com/quentinhardy/odat
Repository: https://gitlab.com/kalilinux/packages/odat
Architectures: i386 amd64
Version: 5.1.1-0kali2
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### odat
 
  This package contains the ODAT (Oracle Database Attacking Tool), an open source
  penetration testing tool that tests the security of Oracle Databases remotely.
   
  Usage examples of ODAT:
    * You have an Oracle database listening remotely and want to find valid SIDs
      and credentials in order to connect to the database
    * You have a valid Oracle account on a database and want to escalate your
      privileges to become DBA or SYSDBA
    * You have a Oracle account and you want to execute system commands (e.g.
      reverse shell) in order to move forward on the operating system hosting
      the database
 
 **Installed size:** `511 KB`  
 **How to install:** `sudo apt install odat`  
 
 {{< spoiler "Dependencies:" >}}
 * oracle-instantclient-basic 
 * oracle-instantclient-devel 
 * python3
 * python3-argcomplete
 * python3-colorlog
 * python3-cx-oracle
 * python3-libnmap
 * python3-passlib
 * python3-pycryptodome
 * python3-scapy
 * python3-termcolor
 {{< /spoiler >}}
 
 ##### odat
 
 
 ```
 root@kali:~# odat -h
 usage: odat.py [-h] [--version]
                {all,tnscmd,tnspoison,sidguesser,snguesser,passwordguesser,utlhttp,httpuritype,utltcp,ctxsys,externaltable,dbmsxslprocessor,dbmsadvisor,utlfile,dbmsscheduler,java,passwordstealer,oradbg,dbmslob,stealremotepwds,userlikepwd,smb,privesc,cve,search,unwrapper,clean}
                ...
 
             _  __   _  ___ 
            / \|  \ / \|_ _|
           ( o ) o ) o || | 
            \_/|__/|_n_||_| 
 -------------------------------------------
   _        __           _           ___ 
  / \      |  \         / \         |_ _|
 ( o )       o )         o |         | | 
  \_/racle |__/atabase |_n_|ttacking |_|ool 
 -------------------------------------------
 
 By Quentin Hardy (quentin.hardy@protonmail.com or quentin.hardy@bt.com)
 
 positional arguments:
   {all,tnscmd,tnspoison,sidguesser,snguesser,passwordguesser,utlhttp,httpuritype,utltcp,ctxsys,externaltable,dbmsxslprocessor,dbmsadvisor,utlfile,dbmsscheduler,java,passwordstealer,oradbg,dbmslob,stealremotepwds,userlikepwd,smb,privesc,cve,search,unwrapper,clean}
                       
                       Choose a main command
     all               to run all modules in order to know what it is possible to do
     tnscmd            to communicate with the TNS listener
     tnspoison         to exploit TNS poisoning attack (SID required)
     sidguesser        to know valid SIDs
     snguesser         to know valid Service Name(s)
     passwordguesser   to know valid credentials
     utlhttp           to send HTTP requests or to scan ports
     httpuritype       to send HTTP requests or to scan ports
     utltcp            to scan ports
     ctxsys            to read files
     externaltable     to read files or to execute system commands/scripts
     dbmsxslprocessor  to upload files
     dbmsadvisor       to upload files
     utlfile           to download/upload/delete files
     dbmsscheduler     to execute system commands without a standard output
     java              to execute system commands
     passwordstealer   to get hashed Oracle passwords
     oradbg            to execute a bin or script
     dbmslob           to download files
     stealremotepwds   to steal hashed passwords thanks an authentication sniffing (CVE-2012-3137)
     userlikepwd       to try each Oracle username stored in the DB like the corresponding pwd
     smb               to capture the SMB authentication
     privesc           to gain elevated access
     cve               to exploit a CVE
     search            to search in databases, tables and columns
     unwrapper         to unwrap PL/SQL source code (no for 9i version)
     clean             clean traces and logs
 
 options:
   -h, --help          show this help message and exit
   --version           show program's version number and exit
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
