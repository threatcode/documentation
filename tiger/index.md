---
Title: tiger
Homepage: http://savannah.nongnu.org/projects/tiger/
Repository: https://git.savannah.nongnu.org/cgit/tiger.git
Architectures: any
Version: 1:3.2.4~rc1-3.2
Metapackages: kali-linux-everything kali-tools-identify 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### tiger
 
  TIGER, or the 'tiger' scripts, is a set of tools (Bourne shell scripts and C
  programs) which are used to perform a security audit of different operating
  systems components. The tools can be both run all at once to generate an
  audit report of the system and to detect elements that could be fixed
  when hardening it.
   
  TIGER has one primary goal: report ways the system's security can be
  compromised.
   
  Most of the tools are independent, but some of them rely on specialised
  external security tools such as John the Ripper, Chkroot and integrity check
  tools (like Tripwire, Integrit or Aide) to execute some tasks.
   
  The same checks are also configured by default to run periodically and
  detect deviations or unauthorised changes. This makes it possible to
  used them also as a host intrusion detection mechanism.
  This review mechanism relies on the use of the cron task scheduler and an
  email delivery system to report errors and deviations.
   
  This package provides all the security scripts and data files for Linux.
  A separate package is available providing the scripts for other operating
  systems so they can be run from a centralised repository.
   
  The Linux scripts incorporate specific checks targetting the Debian OS
  including: md5sums checks of installed files, location of files not belonging
  to packages, and analysis of local listening processes.
   
  Alternatives to TIGER available in Debian include lynis and ossec. If you are
  aiming for a small set of checks, try checksecurity, lsat or yasat.
 
 **Installed size:** `7.61 MB`  
 **How to install:** `sudo apt install tiger`  
 
 {{< spoiler "Dependencies:" >}}
 * binutils
 * bsdutils 
 * debconf  | debconf-2.0
 * debianutils 
 * libc6 
 * lsb-release
 * net-tools
 * ucf
 {{< /spoiler >}}
 
 ##### tiger
 
 UNIX Security Checker
 
 ```
 root@kali:~# tiger -h
 Tiger UN*X security checking system
    Developed by Texas A&M University, 1994
    Updated by the Advanced Research Corporation, 1999-2002
    Further updated by Javier Fernandez-Sanguino, 2001-2018
    Contributions by Francisco Manuel Garcia Claramonte, 2009-2010
    Covered by the GNU General Public License (GPL)
 
 Tiger, version 
 Usage: ./tiger [-vthqGSH]  [-B dir] [-l dir|@host] [-w dir] [-b dir] [-e|-E] [-c config] [-A arch] [-O os] [-R release]
 
        -v     Show the Tiger version.
 
        -t     Run in test mode.
 
        -h     Show usage (this help).
 
        -q     Supress messages to be as quiet as possible, only 
               security messages will be shown.
 
        -B name
               Specify  the directory where tiger is installed.  If
               not specified, '/usr/lib/tiger' is used.
 
        -l name
               Specify the name of the directory where Tiger  will
               write  the  security  report.  This defaults to    
               '/var/log/tiger'. The filename  of  the report will be of 
               the form 'security.report.host-name.date.time.'    
               If the directory  begins  with a @, the name will
               be interpreted as a tiger logging server.
 
        -w name
               Specify a directory to  use  for  creating  scratch
               files.  This defaults to '/var/lib/tiger/work'.
 
        -b name
               Specify  the directory which contains (or will con-
               tain) the binaries generated from  the  C  modules.
               If  the  systems  directories contain all the bina-
               ries, they will be used directly  from  there.   If
               not,  then  if  the  bindir  contains the binaries,
               these will be used.  If none are  found  in  either
               place,  then an attempt will be made to compile the
               C code and install the executables into the bindir.
 
        -c name
               Specify  an  alternate  name for the tigerrc control
               file.  The default is '/etc/tiger/tigerrc'.
 
        -e     This option will cause explanations to be  inserted
               into  the  security  report following each message.
               This can greatly increase the size of  the  report,
               as explanations may appear repeatedly.
 
        -E     This  option  indicates that a separate explanation
               report should be  created,  with  explanations  for
               each  type  of  message  only  appearing once.  The
               filename of the explanation report will be  of  the
               form 'explain.report.hostname.date.time.'
 
        -G     Generate the signatures (MD5 hashes and file permissions)
               for system binary files.
 
        -H     This option will format the report into HTML creat-
               ing local links to the problem descriptions.
 
        -S     This option indicates that a surface level check of
               the  configuration  files  of  any diskless clients
               served by this machine should  be  checked  at  the
               same  time.   The checks will not be as in depth as
               they would be if run on the client itself.
 
 Overrides for values detected  by the configuration system:
        -A arch
               Specify  an  alternate  architecture for tiger
 
        -O os
               Specify  an  alternate  operating system for tiger
 
        -R release
               Specify  an  alternate  operating system release  
               for tiger
 
 Report bugs at http://savannah.nongnu.org/projects/tiger
 ```
 
 - - -
 
 ##### tigercron
 
 Cron utility for Tiger UNIX Security Checker
 
 ```
 root@kali:~# tigercron -h
 Tiger, version 
 Usage: ./tiger [-vthqGSH]  [-B dir] [-l dir|@host] [-w dir] [-b dir] [-e|-E] [-c config] [-A arch] [-O os] [-R release]
 
        -v     Show the Tiger version.
 
        -t     Run in test mode.
 
        -h     Show usage (this help).
 
        -q     Supress messages to be as quiet as possible, only 
               security messages will be shown.
 
        -B name
               Specify  the directory where tiger is installed.  If
               not specified, '/usr/lib/tiger' is used.
 
        -l name
               Specify the name of the directory where Tiger  will
               write  the  security  report.  This defaults to    
               '/var/log/tiger'. The filename  of  the report will be of 
               the form 'security.report.host-name.date.time.'    
               If the directory  begins  with a @, the name will
               be interpreted as a tiger logging server.
 
        -w name
               Specify a directory to  use  for  creating  scratch
               files.  This defaults to '/var/lib/tiger/work'.
 
        -b name
               Specify  the directory which contains (or will con-
               tain) the binaries generated from  the  C  modules.
               If  the  systems  directories contain all the bina-
               ries, they will be used directly  from  there.   If
               not,  then  if  the  bindir  contains the binaries,
               these will be used.  If none are  found  in  either
               place,  then an attempt will be made to compile the
               C code and install the executables into the bindir.
 
        -c name
               Specify  an  alternate  name for the tigerrc control
               file.  The default is '/etc/tiger/tigerrc'.
 
        -e     This option will cause explanations to be  inserted
               into  the  security  report following each message.
               This can greatly increase the size of  the  report,
               as explanations may appear repeatedly.
 
        -E     This  option  indicates that a separate explanation
               report should be  created,  with  explanations  for
               each  type  of  message  only  appearing once.  The
               filename of the explanation report will be  of  the
               form 'explain.report.hostname.date.time.'
 
        -G     Generate the signatures (MD5 hashes and file permissions)
               for system binary files.
 
        -H     This option will format the report into HTML creat-
               ing local links to the problem descriptions.
 
        -S     This option indicates that a surface level check of
               the  configuration  files  of  any diskless clients
               served by this machine should  be  checked  at  the
               same  time.   The checks will not be as in depth as
               they would be if run on the client itself.
 
 Overrides for values detected  by the configuration system:
        -A arch
               Specify  an  alternate  architecture for tiger
 
        -O os
               Specify  an  alternate  operating system for tiger
 
        -R release
               Specify  an  alternate  operating system release  
               for tiger
 
 Report bugs at http://savannah.nongnu.org/projects/tiger
 ```
 
 - - -
 
 ##### tigexp
 
 UNIX Security Checker Explanation Generator
 
 ```
 root@kali:~# tigexp --help
 
 
 ```
 
 - - -
 
 ### tiger-otheros
 
  TIGER, or the 'tiger' scripts, is a set of tools (Bourne shell scripts and C
  programs) which are used to perform a security audit of different operating
  systems components. The tools can be both run all at once to generate an
  audit report of the system and to detect elements that could be fixed
  when hardening it. They can also be run periodically to compare the operating
  system status against a baseline and report deviations. In this way, they can
  be used also as a host intrusion detection mechanism.
   
  This package provides all the scripts for Unix-based operating systems (other
  than Linux) which are provided in the Tiger application upstream. They are
  separately packaged in Debian as most users do not need them to run Tiger.
   
  On the other hand, they might be useful for administrators that wish to run
  Tiger in hosts running different Unix variants in a distributed environment.
  Hosts can run the Tiger scripts through the network (e.g. NFS) and generate
  locally reports for analysis and intrusion detection.
 
 **Installed size:** `2.37 MB`  
 **How to install:** `sudo apt install tiger-otheros`  
 
 {{< spoiler "Dependencies:" >}}
 * tiger
 {{< /spoiler >}}
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
