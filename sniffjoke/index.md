---
Title: sniffjoke
Homepage: https://github.com/vecna/sniffjoke
Repository: https://gitlab.com/kalilinux/packages/sniffjoke
Architectures: any
Version: 0.4.1-1kali2
Metapackages: kali-linux-everything kali-linux-large kali-tools-sniffing-spoofing 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### sniffjoke
 
  SniffJoke is an application for Linux that handle
  transparently your TCP connection, delaying, modifyng and
  inject fake packets inside your transmission, make them
  almost impossible to be correctly readed by a passive
  wiretapping technology (IDS or sniffer).
 
 **Installed size:** `518 KB`  
 **How to install:** `sudo apt install sniffjoke`  
 
 {{< spoiler "Dependencies:" >}}
 * iptables
 * libc6 
 * libgcc-s1 
 * libstdc++6 
 * tcpdump
 {{< /spoiler >}}
 
 ##### sj-commit-results
 
 
 ```
 root@kali:~# sj-commit-results -h
 usage: /usr/bin/sj-commit-results options
 This script is part of SniffJoke autotest
 USUALLY - an user has not any needings in use this script
 
 OPTIONS:
    -l      target location to send remotely 
    -u      URL which commit to
            (both required)
 
 ```
 
 - - -
 
 ##### sj-iptcpopt-probe
 
 
 ```
 root@kali:~# sj-iptcpopt-probe -h
 usage: /usr/bin/sj-iptcpopt-probe options
 This script is part of SniffJoke autotest
 
 This script is invoked by sniffjoke-autotest and try the possibile
 combination of IP/TCP header options for the testing 'location'
 
 Is required a detailed test because different ISP will handle 
 differently these options, considering a packet acceptable or not
 by internal policy, router configuration and updating frequency
 
 by hand this script should accept these argument:
 
 OPTIONS:
    -h      show this message
    -w      working directory                                   (required)
             (eg: /tmp/home/, where sniffjoke-autotest is running)
    -u      testing URL                                         (required)
    -n      username to downgrade privileges
    -g      group to downgrade privileges
    -i      server IPv4 format 000.000.000.000                  (required)
    
 ```
 
 - - -
 
 ##### sniffjoke
 
 (unknown subject)
 
 ```
 root@kali:~# sniffjoke -h
 Usage: sniffjoke [OPTION]... :
  --location <name>	specify the network environment (suggested) [default: generic]
  --dir <name>		specify the base directory where the location reside [default: /usr/local/var/sniffjoke/]
 			[using both location and dir defaults, the configuration status will not be saved]
  --user <username>	downgrade priviledge to the specified user [default: nobody]
  --group <groupname>	downgrade priviledge to the specified group [default: nogroup]
  --no-tcp		disable tcp mangling [default: tcp mangled]
  --no-udp		disable udp mangling [default: udp mangled]
  --whitelist		inject evasion packets only in the specified ip addresses
  --blacklist		inject evasion packet in all session excluding the blacklisted ip address
  --start		if present, evasion i'ts activated immediatly [default: not present]
  --chain		enable chained hacking, powerful and entropic effects [default: disabled]
  --debug <level 0-5>	set verbosity level [default: 2]
 			0: suppress log, 1: common, 2: verbose, 3: debug, 4: session 5: packets
  --foreground		running in foreground [default:background]
  --admin <ip>[:port]	specify administration IP address [default: 127.0.0.1:8844]
  --force		force restart (usable when another sniffjoke service is running)
  --gw-mac-addr		specify default gateway mac address [default: is autodetected]
  --version		show sniffjoke version
  --help			show this help
 
 			http://www.delirandom.net/sniffjoke
 ```
 
 - - -
 
 ##### sniffjoke-autotest
 
 (unknown subject)
 
 ```
 root@kali:~# sniffjoke-autotest -h
 usage: /usr/bin/sniffjoke-autotest options
 
   This script runs plugins test along different destinations OS to determinate the 
 selection of plugins and options that correctly works in the current location. 
 
   Every workplace (office, home, freewifi) you use, neet to be setup as location.
 
   Having a location correctly configurated IS THE ONLY WAY to have SniffJoke working;
   technical details will be found in: 
 http://www.delirandom.net/sniffjoke/sniffjoke-locations
 
 OPTIONS:
    -h      show this message
    -l      location name                                       (required)
    -n      number of replicas to be passed for the single hack (default 1)
    -g      specify the group to privilege downgrade            (default: nogroup)
    -u      specify the user to privilege downgrade             (default: nobody)
 
 ```
 
 - - -
 
 ##### sniffjokectl
 
 (unknown subject)
 
 ```
 root@kali:~# sniffjokectl -h
 Usage: sniffjokectl [OPTIONS]... [COMMANDS]...
  --address <ip>[:port]	specify administration IP address [default: 127.0.0.1:8844]
  --version		show sniffjoke version
  --timeout		set milliseconds timeout when contacting SniffJoke service [default: 500]
  --help			show this help
 
 when sniffjoke is running, you should send commands with a command line argument:
  start			start sniffjoke hijacking/injection
  stop			pause sniffjoke
  quit			quit sniffjoke
  saveconf		dump configuration file
  stat			get statistics about sniffjoke configuration and network
  info			get statistics about sniffjoke active sessions
  ttlmap			show the mapped hop count for destination
  showport		show the running port-aggressivity configuration
  set start:end value	set the injection's strogness over selected port [not supported!]
 		need to be set in port-aggressivity.conf
  debug			[0-5] change the log debug level
 
 			http://www.delirandom.net/sniffjoke
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
