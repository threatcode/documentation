---
Title: medusa
Homepage: http://foofus.net/?page_id=51
Repository: https://salsa.debian.org/pkg-security-team/medusa
Architectures: any
Version: 2.2-7
Metapackages: kali-linux-default kali-linux-everything kali-linux-large kali-tools-information-gathering kali-tools-passwords kali-tools-vulnerability kali-tools-web 
Icon: images/medusa-logo.svg
PackagesInfo: |
 ### medusa
 
  Medusa is intended to be a speedy, massively parallel, modular, login
  brute-forcer. The goal is to support as many services which allow remote
  authentication as possible. The author considers following items as some of
  the key features of this application:
       * Thread-based parallel testing. Brute-force testing can be
         performed against multiple hosts, users or passwords
         concurrently.
       * Flexible user input. Target information (host/user/password) can
         be specified in a variety of ways. For example, each item can be
         either a single entry or a file containing multiple entries.
         Additionally, a combination file format allows the user to
         refine their target listing.
       * Modular design. Each service module exists as an
         independent .mod file. This means that no modifications are
         necessary to the core application in order to extend the
         supported list of services for brute-forcing.
 
 **Installed size:** `794 KB`  
 **How to install:** `sudo apt install medusa`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libpq5
 * libssh2-1 
 * libssl3 
 * libsvn1 
 {{< /spoiler >}}
 
 ##### medusa
 
 Parallel Network Login Auditor
 
 ```
 root@kali:~# medusa -h
 Medusa v2.2 [http://www.foofus.net] (C) JoMo-Kun / Foofus Networks <jmk@foofus.net>
 
 
 Syntax: Medusa [-h host|-H file] [-u username|-U file] [-p password|-P file] [-C file] -M module [OPT]
   -h [TEXT]    : Target hostname or IP address
   -H [FILE]    : File containing target hostnames or IP addresses
   -u [TEXT]    : Username to test
   -U [FILE]    : File containing usernames to test
   -p [TEXT]    : Password to test
   -P [FILE]    : File containing passwords to test
   -C [FILE]    : File containing combo entries. See README for more information.
   -O [FILE]    : File to append log information to
   -e [n/s/ns]  : Additional password checks ([n] No Password, [s] Password = Username)
   -M [TEXT]    : Name of the module to execute (without the .mod extension)
   -m [TEXT]    : Parameter to pass to the module. This can be passed multiple times with a
                  different parameter each time and they will all be sent to the module (i.e.
                  -m Param1 -m Param2, etc.)
   -d           : Dump all known modules
   -n [NUM]     : Use for non-default TCP port number
   -s           : Enable SSL
   -g [NUM]     : Give up after trying to connect for NUM seconds (default 3)
   -r [NUM]     : Sleep NUM seconds between retry attempts (default 3)
   -R [NUM]     : Attempt NUM retries before giving up. The total number of attempts will be NUM + 1.
   -c [NUM]     : Time to wait in usec to verify socket is available (default 500 usec).
   -t [NUM]     : Total number of logins to be tested concurrently
   -T [NUM]     : Total number of hosts to be tested concurrently
   -L           : Parallelize logins using one username per thread. The default is to process 
                  the entire username before proceeding.
   -f           : Stop scanning host after first valid username/password found.
   -F           : Stop audit after first valid username/password found on any host.
   -b           : Suppress startup banner
   -q           : Display module's usage information
   -v [NUM]     : Verbose level [0 - 6 (more)]
   -w [NUM]     : Error debug level [0 - 10 (more)]
   -V           : Display version
   -Z [TEXT]    : Resume scan based on map of previous scan
 
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
