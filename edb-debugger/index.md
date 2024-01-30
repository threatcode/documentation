---
Title: edb-debugger
Homepage: https://github.com/eteran/edb-debugger
Repository: https://salsa.debian.org/debian/edb-debugger
Architectures: amd64 i386
Version: 1.3.0-2.1
Metapackages: kali-linux-everything kali-linux-large kali-tools-forensics kali-tools-respond kali-tools-reverse-engineering 
Icon: images/edb-debugger-logo.svg
PackagesInfo: |
 ### edb-debugger
 
  edb is a graphical cross platform x86/x86-64 debugger.
  It was inspired by Ollydbg, but aims to function on x86
  and x86-64 as well as multiple OS's. Linux is the only
  officially supported platform at the moment, but FreeBSD,
  OpenBSD, OSX and Windows ports are underway with varying
  degrees of functionality.
 
 **Installed size:** `1.64 MB`  
 **How to install:** `sudo apt install edb-debugger`  
 
 {{< spoiler "Dependencies:" >}}
 * edb-debugger-plugins
 * libc6 
 * libcapstone4 
 * libcgraph6
 * libdouble-conversion3 
 * libgcc-s1 
 * libgvc6
 * libqt5core5a 
 * libqt5gui5  | libqt5gui5-gles 
 * libqt5svg5 
 * libqt5widgets5 
 * libqt5xml5 
 * libqt5xmlpatterns5 
 * libstdc++6 
 {{< /spoiler >}}
 
 ##### edb
 
 Graphical debugger and disassembler for executables
 
 ```
 root@kali:~# man edb
 EDB(1)                                                                  EDB(1)
 
 NAME
        edb - graphical debugger and disassembler for executables
 
 SYNOPSIS
         edb [OPTION]... [TARGET]
 
 DESCRIPTION
        edb (Evan's Debugger) is a modular and modern disassembler and debugger
        for  binary  ELF files based on ptrace API and the capstone disassembly
        library.
 
        --help Show usage and exit.
 
        --symbols <file>
               generate symbols map for file <file>
 
        --attach <pid>
               attach the process of PID <pid> to debugger
 
        --run <program> [args...]
               open <program> in debugger with optional [args...]
 
        --version
               show version string and exit.
 
        --dump-version
               show version and exit.
 
 EXAMPLE
        edb --symbols /lib/libc.so.6 > libc.so.6.map
 
             Will generate symbols for libc and save it in a text file. It's useful if you store this map files in the symbols directory configured in edb's preferences.
 
        for i in $(ls /lib); do edb --symbols $i > $(basename $i).map; done
 
              Useful to generate maps for all libs you have in /lib.
 
        edb --run /bin/ls
 
              Will open the ls program binary in debugger.
 
        edb --attach 1720
 
             Attach the process of PID 1720 to debugger.
 
 AUTHOR
        Written by Evan Teran <evan.teran@gmail.com>
 
 REPORTING BUGS
        Report   any   bugs   or   requests   for   features   via    BTS    on
        https://github.com/eteran/edb-debugger/issues
 
 COPYRIGHT
        Copyright   (C)  2008  CodeF00.  Licensed  GPLv2:  GNU  GPL  version  2
        <http://www.gnu.org/licenses/old-licenses/gpl-2.0.txt>.  This  is  free
        software:  you are free to change and redistribute it. There is NO WAR-
        RANTY, to the extent permitted by law.
 
                                  December 2011                          EDB(1)
 ```
 
 - - -
 
 ### edb-debugger-plugins
 
  edb is a graphical cross platform x86/x86-64 debugger.
  It was inspired by Ollydbg, but aims to function on x86
  and x86-64 as well as multiple OS's. Linux is the only
  officially supported platform at the moment, but FreeBSD,
  OpenBSD, OSX and Windows ports are underway with varying
  degrees of functionality.
   
  This package provides the plugins that used by edb.
 
 **Installed size:** `2.66 MB`  
 **How to install:** `sudo apt install edb-debugger-plugins`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libcapstone4 
 * libgcc-s1 
 * libqt5core5a 
 * libqt5gui5  | libqt5gui5-gles 
 * libqt5network5 
 * libqt5widgets5 
 * libqt5xml5 
 * libqt5xmlpatterns5 
 * libstdc++6 
 {{< /spoiler >}}
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## Screenshots

```
edb
```

![edb-debugger](images/edb-debugger.png)
