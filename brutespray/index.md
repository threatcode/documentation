---
Title: brutespray
Homepage: https://github.com/x90skysn3k/brutespray
Repository: https://salsa.debian.org/pkg-security-team/brutespray
Architectures: all
Version: 1.8.1-2
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### brutespray
 
  This Python script takes nmap GNMAP/XML output, newline separated JSON,
  Nexpose `XML Export` output or Nessus `.nessus` exports and automatically
  brute-forces services with default credentials using Medusa.
   
  BruteSpray can even find non-standard ports by using the -sV inside Nmap.
 
 **Installed size:** `118 KB`  
 **How to install:** `sudo apt install brutespray`  
 
 {{< spoiler "Dependencies:" >}}
 * medusa
 * python3
 {{< /spoiler >}}
 
 ##### brutespray
 
 Python bruteforce tool
 
 ```
 root@kali:~# brutespray -h
 usage: brutespray [-h] [-f FILE] [-o OUTPUT] [-s SERVICE] [-t THREADS]
                   [-T HOSTS] [-U USERLIST] [-P PASSLIST] [-C COMBO]
                   [-u USERNAME] [-p PASSWORD] [-c] [-i] [-m] [-q] [-v VERBOSE]
                   [-w DEBUG]
 
 Usage: python brutespray.py <OPTIONS> 
 
 options:
   -h, --help            show this help message and exit
 
 Menu Options:
   -f FILE, --file FILE  GNMAP, JSON or XML file to parse
   -o OUTPUT, --output OUTPUT
                         Directory containing successful attempts
   -s SERVICE, --service SERVICE
                         specify service to attack
   -t THREADS, --threads THREADS
                         number of medusa threads
   -T HOSTS, --hosts HOSTS
                         number of hosts to test concurrently
   -U USERLIST, --userlist USERLIST
                         reference a custom username file
   -P PASSLIST, --passlist PASSLIST
                         reference a custom password file
   -C COMBO, --combo COMBO
                         specify a combo input (host:user:password)
   -u USERNAME, --username USERNAME
                         specify a single username
   -p PASSWORD, --password PASSWORD
                         specify a single password
   -c, --continuous      keep brute-forcing after success
   -i, --interactive     interactive mode
   -m, --modules         dump a list of available modules to brute
   -q, --quiet           supress banner
   -v VERBOSE, --verbose VERBOSE
                         verbose output from medusa [0-6], default=5
   -w DEBUG, --debug DEBUG
                         debug error output from medusa [0-10], default=5
 
                               #@                           @/
                            @@@                               @@@
                         %@@@                                   @@@.
                       @@@@@                                     @@@@%
                      @@@@@                                       @@@@@
                     @@@@@@@                  @                  @@@@@@@
                     @(@@@@@@@%            @@@@@@@            &@@@@@@@@@
                     @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
                      @@*@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@ @@
                        @@@( @@@@@#@@@@@@@@@*@@@,@@@@@@@@@@@@@@@  @@@
                            @@@@@@ .@@@/@@@@@@@@@@@@@/@@@@ @@@@@@
                                   @@@   @@@@@@@@@@@   @@@
                                  @@@@*  ,@@@@@@@@@(  ,@@@@
                                  @@@@@@@@@@@@@@@@@@@@@@@@@
                                   @@@.@@@@@@@@@@@@@@@ @@@
                                     @@@@@@ @@@@@ @@@@@@
                                        @@@@@@@@@@@@@
                                        @@   @@@   @@
                                        @@ @@@@@@@ @@
                                          @@% @  @@
 
 
 
         ██████╗ ██████╗ ██╗   ██╗████████╗███████╗███████╗██████╗ ██████╗  █████╗ ██╗   ██╗
         ██╔══██╗██╔══██╗██║   ██║╚══██╔══╝██╔════╝██╔════╝██╔══██╗██╔══██╗██╔══██╗╚██╗ ██╔╝
         ██████╔╝██████╔╝██║   ██║   ██║   █████╗  ███████╗██████╔╝██████╔╝███████║ ╚████╔╝
         ██╔══██╗██╔══██╗██║   ██║   ██║   ██╔══╝  ╚════██║██╔═══╝ ██╔══██╗██╔══██║  ╚██╔╝
         ██████╔╝██║  ██║╚██████╔╝   ██║   ███████╗███████║██║     ██║  ██║██║  ██║   ██║
         ╚═════╝ ╚═╝  ╚═╝ ╚═════╝    ╚═╝   ╚══════╝╚══════╝╚═╝     ╚═╝  ╚═╝╚═╝  ╚═╝   ╚═╝
 
  brutespray.py v1.8.1
  Created by: Shane Young/@t1d3nio && Jacob Robles/@shellfail
  Inspired by: Leon Johnson/@sho-luv
  Credit to Medusa: JoMo-Kun / Foofus Networks <jmk@foofus.net>
 
 usage: brutespray [-h] [-f FILE] [-o OUTPUT] [-s SERVICE] [-t THREADS]
                   [-T HOSTS] [-U USERLIST] [-P PASSLIST] [-C COMBO]
                   [-u USERNAME] [-p PASSWORD] [-c] [-i] [-m] [-q] [-v VERBOSE]
                   [-w DEBUG]
 
 Usage: python brutespray.py <OPTIONS> 
 
 options:
   -h, --help            show this help message and exit
 
 Menu Options:
   -f FILE, --file FILE  GNMAP, JSON or XML file to parse
   -o OUTPUT, --output OUTPUT
                         Directory containing successful attempts
   -s SERVICE, --service SERVICE
                         specify service to attack
   -t THREADS, --threads THREADS
                         number of medusa threads
   -T HOSTS, --hosts HOSTS
                         number of hosts to test concurrently
   -U USERLIST, --userlist USERLIST
                         reference a custom username file
   -P PASSLIST, --passlist PASSLIST
                         reference a custom password file
   -C COMBO, --combo COMBO
                         specify a combo input (host:user:password)
   -u USERNAME, --username USERNAME
                         specify a single username
   -p PASSWORD, --password PASSWORD
                         specify a single password
   -c, --continuous      keep brute-forcing after success
   -i, --interactive     interactive mode
   -m, --modules         dump a list of available modules to brute
   -q, --quiet           supress banner
   -v VERBOSE, --verbose VERBOSE
                         verbose output from medusa [0-6], default=5
   -w DEBUG, --debug DEBUG
                         debug error output from medusa [0-10], default=5
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## brutespray Usage Examples

Attack all services in `nas.gnmap` with a specific user list (`unix_users.txt`) and password list (`password.lst`):

```
root@kali:~# brutespray --file nas.gnmap -U /usr/share/wordlists/metasploit/unix_users.txt -P /usr/share/wordlists/metasploit/password.lst --threads 3 --hosts 1

                              #@                           @/
                           @@@                               @@@
                        %@@@                                   @@@.
                      @@@@@                                     @@@@%
                     @@@@@                                       @@@@@
                    @@@@@@@                  @                  @@@@@@@
                    @(@@@@@@@%            @@@@@@@            &@@@@@@@@@
                    @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
                     @@*@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@ @@
                       @@@( @@@@@#@@@@@@@@@*@@@,@@@@@@@@@@@@@@@  @@@
                           @@@@@@ .@@@/@@@@@@@@@@@@@/@@@@ @@@@@@
                                  @@@   @@@@@@@@@@@   @@@
                                 @@@@*  ,@@@@@@@@@(  ,@@@@
                                 @@@@@@@@@@@@@@@@@@@@@@@@@
                                  @@@.@@@@@@@@@@@@@@@ @@@
                                    @@@@@@ @@@@@ @@@@@@
                                       @@@@@@@@@@@@@
                                       @@   @@@   @@
                                       @@ @@@@@@@ @@
                                         @@% @  @@



        ██████╗ ██████╗ ██╗   ██╗████████╗███████╗███████╗██████╗ ██████╗  █████╗ ██╗   ██╗
        ██╔══██╗██╔══██╗██║   ██║╚══██╔══╝██╔════╝██╔════╝██╔══██╗██╔══██╗██╔══██╗╚██╗ ██╔╝
        ██████╔╝██████╔╝██║   ██║   ██║   █████╗  ███████╗██████╔╝██████╔╝███████║ ╚████╔╝
        ██╔══██╗██╔══██╗██║   ██║   ██║   ██╔══╝  ╚════██║██╔═══╝ ██╔══██╗██╔══██║  ╚██╔╝
        ██████╔╝██║  ██║╚██████╔╝   ██║   ███████╗███████║██║     ██║  ██║██║  ██║   ██║
        ╚═════╝ ╚═╝  ╚═╝ ╚═════╝    ╚═╝   ╚══════╝╚══════╝╚═╝     ╚═╝  ╚═╝╚═╝  ╚═╝   ╚═╝



 brutespray.py v1.5.2
 Created by: Shane Young/@x90skysn3k && Jacob Robles/@shellfail
 Inspired by: Leon Johnson/@sho-luv
 Credit to Medusa: JoMo-Kun / Foofus Networks <jmk@foofus.net>

Starting to brute, please make sure to use the right amount of threads(-t) and parallel hosts(-T)...  \

Brute-Forcing...
Medusa v2.2 [http://www.foofus.net] (C) JoMo-Kun / Foofus Networks <jmk@foofus.net>

ACCOUNT CHECK: [mysql] Host: 192.168.86.4 (1 of 1, 0 complete) User: 4Dgifts (1 of 111, 0 complete) Password: !@#$%^& (1 of 88396 complete)
ACCOUNT CHECK: [mysql] Host: 192.168.86.4 (1 of 1, 0 complete) User: 4Dgifts (1 of 111, 0 complete) Password: !@#$% (2 of 88396 complete)
ACCOUNT CHECK: [mysql] Host: 192.168.86.4 (1 of 1, 0 complete) User: 4Dgifts (1 of 111, 0 complete) Password: !@#$%^ (3 of 88396 complete)
[...]
```

Interactive mode, brute forcing the FTP service only.

```
root@kali:~# brutespray -i -f nas.gnmap

                              #@                           @/
                           @@@                               @@@
                        %@@@                                   @@@.
                      @@@@@                                     @@@@%
                     @@@@@                                       @@@@@
                    @@@@@@@                  @                  @@@@@@@
                    @(@@@@@@@%            @@@@@@@            &@@@@@@@@@
                    @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
                     @@*@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@ @@
                       @@@( @@@@@#@@@@@@@@@*@@@,@@@@@@@@@@@@@@@  @@@
                           @@@@@@ .@@@/@@@@@@@@@@@@@/@@@@ @@@@@@
                                  @@@   @@@@@@@@@@@   @@@
                                 @@@@*  ,@@@@@@@@@(  ,@@@@
                                 @@@@@@@@@@@@@@@@@@@@@@@@@
                                  @@@.@@@@@@@@@@@@@@@ @@@
                                    @@@@@@ @@@@@ @@@@@@
                                       @@@@@@@@@@@@@
                                       @@   @@@   @@
                                       @@ @@@@@@@ @@
                                         @@% @  @@



        ██████╗ ██████╗ ██╗   ██╗████████╗███████╗███████╗██████╗ ██████╗  █████╗ ██╗   ██╗
        ██╔══██╗██╔══██╗██║   ██║╚══██╔══╝██╔════╝██╔════╝██╔══██╗██╔══██╗██╔══██╗╚██╗ ██╔╝
        ██████╔╝██████╔╝██║   ██║   ██║   █████╗  ███████╗██████╔╝██████╔╝███████║ ╚████╔╝
        ██╔══██╗██╔══██╗██║   ██║   ██║   ██╔══╝  ╚════██║██╔═══╝ ██╔══██╗██╔══██║  ╚██╔╝
        ██████╔╝██║  ██║╚██████╔╝   ██║   ███████╗███████║██║     ██║  ██║██║  ██║   ██║
        ╚═════╝ ╚═╝  ╚═╝ ╚═════╝    ╚═╝   ╚══════╝╚══════╝╚═╝     ╚═╝  ╚═╝╚═╝  ╚═╝   ╚═╝



 brutespray.py v1.5.2
 Created by: Shane Young/@x90skysn3k && Jacob Robles/@shellfail
 Inspired by: Leon Johnson/@sho-luv
 Credit to Medusa: JoMo-Kun / Foofus Networks <jmk@foofus.net>

Loading File: /

Welcome to interactive mode!


WARNING: Leaving an option blank will leave it empty and refer to default


Available services to brute-force:
Service: ftp on port 21 with 1 hosts
Service: ssh on port 22 with 1 hosts
Service: mysql on port 3306 with 1 hosts

Enter services you want to brute - default all (ssh,ftp,etc): ftp
Enter the number of parallel threads (default is 2): 4
Enter the number of parallel hosts to scan per service (default is 1): 1
Would you like to specify a wordlist? (y/n): y
Enter a userlist you would like to use: /usr/share/wordlists/metasploit/unix_users.txt
Enter a passlist you would like to use: /usr/share/wordlists/metasploit/password.lst
Would to specify a single username or password (y/n): n

Starting to brute, please make sure to use the right amount of threads(-t) and parallel hosts(-T)...  \

Brute-Forcing...
```
