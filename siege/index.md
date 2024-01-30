---
Title: siege
Homepage: http://www.joedog.org/JoeDog/Siege
Repository: https://salsa.debian.org/debian/siege
Architectures: any
Version: 4.0.7-1
Metapackages: kali-linux-everything kali-linux-large kali-tools-vulnerability kali-tools-web 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### siege
 
  Siege is an regression test and benchmark utility. It can stress test a single
  URL with a user defined number of simulated users, or it can read many URLs
  into memory and stress them simultaneously. The program reports the total
  number of hits recorded, bytes transferred, response time, concurrency, and
  return status. Siege supports HTTP/1.0 and 1.1 protocols, the GET and POST
  directives, cookies, transaction logging, and basic authentication. Its
  features are configurable on a per user basis.
   
  Note: this package contains siege with HTTPS support turned on, thus it
  obsoletes siege-ssl package now.
 
 **Installed size:** `280 KB`  
 **How to install:** `sudo apt install siege`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libssl3 
 * zlib1g 
 {{< /spoiler >}}
 
 ##### bombardment
 
 Run siege with an ever-increasing number of users
 
 ```
 root@kali:~# bombardment --help
 
 usage:
 bombardment [urlfile] [inital # of clients] [inc value] [# of inc] [delay]
 
 
 ```
 
 - - -
 
 ##### siege
 
 An HTTP/FTP load tester and benchmarking utility.
 
 ```
 root@kali:~# siege -h
 Usage: siege [options]
        siege [options] URL
        siege -g URL
 Options:
   -V, --version             VERSION, prints the version number.
   -h, --help                HELP, prints this section.
   -C, --config              CONFIGURATION, show the current config.
   -v, --verbose             VERBOSE, prints notification to screen.
   -q, --quiet               QUIET turns verbose off and suppresses output.
   -g, --get                 GET, pull down HTTP headers and display the
                             transaction. Great for application debugging.
   -p, --print               PRINT, like GET only it prints the entire page.
   -c, --concurrent=NUM      CONCURRENT users, default is 10
   -r, --reps=NUM            REPS, number of times to run the test.
   -t, --time=NUMm           TIMED testing where "m" is modifier S, M, or H
                             ex: --time=1H, one hour test.
   -d, --delay=NUM           Time DELAY, random delay before each request
   -b, --benchmark           BENCHMARK: no delays between requests.
   -i, --internet            INTERNET user simulation, hits URLs randomly.
   -f, --file=FILE           FILE, select a specific URLS FILE.
   -R, --rc=FILE             RC, specify an siegerc file
   -l, --log[=FILE]          LOG to FILE. If FILE is not specified, the
                             default is used: /var/log/siege.log
   -m, --mark="text"         MARK, mark the log file with a string.
                             between .001 and NUM. (NOT COUNTED IN STATS)
   -H, --header="text"       Add a header to request (can be many)
   -A, --user-agent="text"   Sets User-Agent in request
   -T, --content-type="text" Sets Content-Type in request
   -j, --json-output         JSON OUTPUT, print final stats to stdout as JSON
       --no-parser           NO PARSER, turn off the HTML page parser
       --no-follow           NO FOLLOW, do not follow HTTP redirects
 
 Copyright (C) 2018 by Jeffrey Fulmer, et al.
 This is free software; see the source for copying conditions.
 There is NO warranty; not even for MERCHANTABILITY or FITNESS
 FOR A PARTICULAR PURPOSE.
 
 ```
 
 - - -
 
 ##### siege.config
 
 Builds a siege.conf template in the user's home directory.
 
 ```
 root@kali:~# siege.config -h
 siege.config
 usage: siege.config [no arguments]
 ----------------------------------
 Resource file already install as /root/.siege/siege.conf
 Use your favorite editor to change  your configuration by
 editing the values in that file or remove it and run this
 program again.
 
 ```
 
 - - -
 
 ##### siege2csv
 
 Run siege with an ever-increasing number of users
 
 ```
 root@kali:~# man siege2csv
 BOMBARDMENT(1)                     siege2csv                    BOMBARDMENT(1)
 
 NAME
        bombardment - Run siege with an ever-increasing number of users
 
    SYNOPSIS
        bombardment [urlfile] [clients] [increment] [trials] [delay]
        bombardment urls.txt 5 10 20 1
 
 DESCRIPTION
        bombardment is part of the siege distribution. It calls siege with an
        initial number of clients. When that run finishes, it immediately calls
        siege again with that number of clients plus the increment.  It does
        this the number of times specified in the fourth argument.
 
 OPTIONS
        urlfile
            The name of the file containing one or more URLs for siege to test.
 
        clients
            The initial number of clients to be used on the first run.
 
        increment
            The number of clients to add to each ensuing run.
 
        trials
            The number of times to run siege.
 
        delay
            The is the amount of time, in seconds, that each client will wait
            between requests.  The siege default is overridden by bombardment
 
 SEE ALSO
        siege(1), siege2csv(1)
 
 AUTHOR
        Written by Peter Hutnick, et al.
 
 JoeDog                            2020-07-10                    BOMBARDMENT(1)
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
