---
Title: glibc
Homepage: https://www.gnu.org/software/libc/libc.html
Repository: https://salsa.debian.org/glibc-team/glibc
Architectures: any all
Version: 2.37-12
Metapackages: kali-linux-core kali-linux-default kali-linux-everything kali-linux-headless kali-linux-labs kali-linux-large kali-linux-nethunter kali-linux-wsl kali-tools-802-11 kali-tools-bluetooth kali-tools-crypto-stego kali-tools-database kali-tools-detect kali-tools-exploitation kali-tools-forensics kali-tools-fuzzing kali-tools-gpu kali-tools-hardware kali-tools-identify kali-tools-information-gathering kali-tools-passwords kali-tools-post-exploitation kali-tools-protect kali-tools-recover kali-tools-reporting kali-tools-respond kali-tools-reverse-engineering kali-tools-rfid kali-tools-sdr kali-tools-sniffing-spoofing kali-tools-social-engineering kali-tools-top10 kali-tools-voip kali-tools-vulnerability kali-tools-web kali-tools-windows-resources kali-tools-wireless 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### glibc-doc
 
  Contains man pages for libpthread functions and the complete GNU C Library
  ChangeLog.  The GNU C Library Reference manual has been moved into
  glibc-doc-reference for licensing reasons.
 
 **Installed size:** `3.41 MB`  
 **How to install:** `sudo apt install glibc-doc`  
 
 
 - - -
 
 ### glibc-source
 
  This package contains the sources and patches which are needed to
  build glibc.
 
 **Installed size:** `20.79 MB`  
 **How to install:** `sudo apt install glibc-source`  
 
 
 - - -
 
 ### libc-bin
 
  This package contains utility programs related to the GNU C Library.
   
   * getconf: query system configuration variables
   * getent: get entries from administrative databases
   * iconv, iconvconfig: convert between character encodings
   * ldd, ldconfig: print/configure shared library dependencies
   * locale, localedef: show/generate locale definitions
   * tzselect, zdump, zic: select/dump/compile time zones
 
 **Installed size:** `1.97 MB`  
 **How to install:** `sudo apt install libc-bin`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### getconf
 
 Query system configuration variables
 
 ```
 root@kali:~# getconf --help
 Usage: getconf [-v SPEC] VAR
   or:  getconf [-v SPEC] PATH_VAR PATH
 
 Get the configuration value for variable VAR, or for variable PATH_VAR
 for path PATH.  If SPEC is given, give values for compilation
 environment SPEC.
 
 For bug reporting instructions, please see:
 <http://www.debian.org/Bugs/>.
 ```
 
 - - -
 
 ##### getent
 
 Get entries from Name Service Switch libraries
 
 ```
 root@kali:~# getent --help
 Usage: getent [OPTION...] database [key ...]
 Get entries from administrative database.
 
   -A, --no-addrconfig        do not filter out unsupported IPv4/IPv6 addresses
                              (with ahosts*)
   -i, --no-idn               disable IDN encoding
   -s, --service=CONFIG       Service configuration to be used
   -?, --help                 Give this help list
       --usage                Give a short usage message
   -V, --version              Print program version
 
 Mandatory or optional arguments to long options are also mandatory or optional
 for any corresponding short options.
 
 Supported databases:
 ahosts ahostsv4 ahostsv6 aliases ethers group gshadow hosts initgroups
 netgroup networks passwd protocols rpc services shadow
 
 For bug reporting instructions, please see:
 <http://www.debian.org/Bugs/>.
 ```
 
 - - -
 
 ##### iconv
 
 Convert text from one character encoding to another
 Perform character set conversion
 
 ```
 root@kali:~# iconv --help
 Usage: iconv [OPTION...] [FILE...]
 Convert encoding of given files from one encoding to another.
 
  Input/Output format specification:
   -f, --from-code=NAME       encoding of original text
   -t, --to-code=NAME         encoding for output
 
  Information:
   -l, --list                 list all known coded character sets
 
  Output control:
   -c                         omit invalid characters from output
   -o, --output=FILE          output file
   -s, --silent               suppress warnings
       --verbose              print progress information
 
   -?, --help                 Give this help list
       --usage                Give a short usage message
   -V, --version              Print program version
 
 Mandatory or optional arguments to long options are also mandatory or optional
 for any corresponding short options.
 
 For bug reporting instructions, please see:
 <http://www.debian.org/Bugs/>.
 ```
 
 - - -
 
 ##### iconvconfig
 
 Create iconv module configuration cache
 
 ```
 root@kali:~# iconvconfig --help
 Usage: iconvconfig [OPTION...] [DIR...]
 Create fastloading iconv module configuration file.
 
       --nostdlib             Do not search standard directories, only those on
                              the command line
   -o, --output=FILE          Put output in FILE instead of installed location
                              (--prefix does not apply to FILE)
       --prefix=PATH          Prefix used for all file accesses
   -?, --help                 Give this help list
       --usage                Give a short usage message
   -V, --version              Print program version
 
 Mandatory or optional arguments to long options are also mandatory or optional
 for any corresponding short options.
 
 For bug reporting instructions, please see:
 <http://www.debian.org/Bugs/>.
 ```
 
 - - -
 
 ##### ld.so
 
 Dynamic linker/loader
 
 ```
 root@kali:~# ld.so --help
 Usage: ld.so [OPTION]... EXECUTABLE-FILE [ARGS-FOR-PROGRAM...]
 You have invoked 'ld.so', the program interpreter for dynamically-linked
 ELF programs.  Usually, the program interpreter is invoked automatically
 when a dynamically-linked executable is started.
 
 You may invoke the program interpreter program directly from the command
 line to load and run an ELF executable file; this is like executing that
 file itself, but always uses the program interpreter you invoked,
 instead of the program interpreter specified in the executable file you
 run.  Invoking the program interpreter directly provides access to
 additional diagnostics, and changing the dynamic linker behavior without
 setting environment variables (which would be inherited by subprocesses).
 
   --list                list all dependencies and how they are resolved
   --verify              verify that given object really is a dynamically linked
                         object we can handle
   --inhibit-cache       Do not use /etc/ld.so.cache
   --library-path PATH   use given PATH instead of content of the environment
                         variable LD_LIBRARY_PATH
   --glibc-hwcaps-prepend LIST
                         search glibc-hwcaps subdirectories in LIST
   --glibc-hwcaps-mask LIST
                         only search built-in subdirectories if in LIST
   --inhibit-rpath LIST  ignore RUNPATH and RPATH information in object names
                         in LIST
   --audit LIST          use objects named in LIST as auditors
   --preload LIST        preload objects named in LIST
   --argv0 STRING        set argv[0] to STRING before running
   --list-tunables       list all tunables with minimum and maximum values
   --list-diagnostics    list diagnostics information
   --help                display this help and exit
   --version             output version information and exit
 
 This program interpreter self-identifies as: /lib64/ld-linux-x86-64.so.2
 
 Shared library search path:
   (libraries located via /etc/ld.so.cache)
   /lib/x86_64-linux-gnu (system search path)
   /usr/lib/x86_64-linux-gnu (system search path)
   /lib (system search path)
   /usr/lib (system search path)
 
 Subdirectories of glibc-hwcaps directories, in priority order:
   x86-64-v4
   x86-64-v3
   x86-64-v2 (supported, searched)
 ```
 
 - - -
 
 ##### ldconfig
 
 Configure dynamic linker run-time bindings
 
 ```
 root@kali:~# ldconfig --help
 Usage: ldconfig [OPTION...]
 Configure Dynamic Linker Run Time Bindings.
 
   -c, --format=FORMAT        Format to use: new (default), old, or compat
   -C CACHE                   Use CACHE as cache file
   -f CONF                    Use CONF as configuration file
   -i, --ignore-aux-cache     Ignore auxiliary cache file
   -l                         Manually link individual libraries.
   -n                         Only process directories specified on the command
                              line.  Don't build cache.
   -N                         Don't build cache
   -p, --print-cache          Print cache
   -r ROOT                    Change to and use ROOT as root directory
   -v, --verbose              Generate verbose messages
   -X                         Don't update symbolic links
   -?, --help                 Give this help list
       --usage                Give a short usage message
   -V, --version              Print program version
 
 Mandatory or optional arguments to long options are also mandatory or optional
 for any corresponding short options.
 
 For bug reporting instructions, please see:
 <http://www.debian.org/Bugs/>.
 ```
 
 - - -
 
 ##### ldd
 
 Print shared object dependencies
 
 ```
 root@kali:~# ldd --help
 Usage: ldd [OPTION]... FILE...
       --help              print this help and exit
       --version           print version information and exit
   -d, --data-relocs       process data relocations
   -r, --function-relocs   process data and function relocations
   -u, --unused            print unused direct dependencies
   -v, --verbose           print all information
 
 For bug reporting instructions, please see:
 <http://www.debian.org/Bugs/>.
 ```
 
 - - -
 
 ##### locale
 
 Get locale-specific information
 Describes a locale definition file
 Description of multilanguage support
 
 ```
 root@kali:~# locale --help
 Usage: locale [OPTION...] NAME
   or:  locale [OPTION...] [-a|-m]
 Get locale-specific information.
 
  System information:
   -a, --all-locales          Write names of available locales
   -m, --charmaps             Write names of available charmaps
 
  Modify output format:
   -c, --category-name        Write names of selected categories
   -k, --keyword-name         Write names of selected keywords
   -v, --verbose              Print more information
 
   -?, --help                 Give this help list
       --usage                Give a short usage message
   -V, --version              Print program version
 
 For bug reporting instructions, please see:
 <http://www.debian.org/Bugs/>.
 ```
 
 - - -
 
 ##### localedef
 
 Compile locale definition files
 
 ```
 root@kali:~# localedef --help
 Usage: localedef [OPTION...] NAME
   or:  localedef [OPTION...] [--add-to-archive|--delete-from-archive] FILE...
   or:  localedef [OPTION...] --list-archive [FILE]
 Compile locale specification
 
  Input Files:
   -f, --charmap=FILE         Symbolic character names defined in FILE
   -i, --inputfile=FILE       Source definitions are found in FILE
   -u, --repertoire-map=FILE  FILE contains mapping from symbolic names to UCS4
                              values
 
  Output control:
   -c, --force                Create output even if warning messages were issued
                             
       --no-hard-links        Do not create hard links between installed
                              locales
       --no-warnings=<warnings>   Comma-separated list of warnings to disable;
                              supported warnings are: ascii, intcurrsym
       --posix                Strictly conform to POSIX
       --prefix=PATH          Optional output file prefix
       --quiet                Suppress warnings and information messages
   -v, --verbose              Print more messages
       --warnings=<warnings>  Comma-separated list of warnings to enable;
                              supported warnings are: ascii, intcurrsym
 
  Archive control:
       --add-to-archive       Add locales named by parameters to archive
   -A, --alias-file=FILE      locale.alias file to consult when making archive
       --big-endian           Generate big-endian output
       --delete-from-archive  Remove locales named by parameters from archive
       --list-archive         List content of archive
       --little-endian        Generate little-endian output
       --no-archive           Don't add new data to archive
       --replace              Replace existing archive content
 
   -?, --help                 Give this help list
       --usage                Give a short usage message
   -V, --version              Print program version
 
 Mandatory or optional arguments to long options are also mandatory or optional
 for any corresponding short options.
 
 System's directory for character maps : /usr/share/i18n/charmaps
 		       repertoire maps: /usr/share/i18n/repertoiremaps
 		       locale path    : /usr/lib/locale:/usr/share/i18n
 For bug reporting instructions, please see:
 <http://www.debian.org/Bugs/>.
 ```
 
 - - -
 
 ##### pldd
 
 Display dynamic shared objects linked into a process
 
 ```
 root@kali:~# pldd --help
 Usage: pldd [OPTION...] PID
 List dynamic shared objects loaded into process.
 
   -?, --help                 Give this help list
       --usage                Give a short usage message
   -V, --version              Print program version
 
 For bug reporting instructions, please see:
 <http://www.debian.org/Bugs/>.
 ```
 
 - - -
 
 ##### tzselect
 
 View timezones
 Select a timezone
 
 ```
 root@kali:~# tzselect --help
 Usage: tzselect [--version] [--help] [-c COORD] [-n LIMIT]
 Select a timezone interactively.
 
 Options:
 
   -c COORD
     Instead of asking for continent and then country and then city,
     ask for selection from time zones whose largest cities
     are closest to the location with geographical coordinates COORD.
     COORD should use ISO 6709 notation, for example, '-c +4852+00220'
     for Paris (in degrees and minutes, North and East), or
     '-c -35-058' for Buenos Aires (in degrees, South and West).
 
   -n LIMIT
     Display at most LIMIT locations when -c is used (default 10).
 
   --version
     Output version information.
 
   --help
     Output this help.
 
 Report bugs to <http://www.debian.org/Bugs/>.
 ```
 
 - - -
 
 ##### zdump
 
 Timezone dumper
 
 ```
 root@kali:~# zdump --help
 zdump: usage: zdump OPTIONS TIMEZONE ...
 Options include:
   -c [L,]U   Start at year L (default -500), end before year U (default 2500)
   -t [L,]U   Start at time L, end before time U (in seconds since 1970)
   -i         List transitions briefly (format is experimental)
   -v         List transitions verbosely
   -V         List transitions a bit less verbosely
   --help     Output this help
   --version  Output version info
 
 Report bugs to <http://www.debian.org/Bugs/>.
 ```
 
 - - -
 
 ##### zic
 
 Timezone compiler
 
 ```
 root@kali:~# zic --help
 zic: usage is zic [ --version ] [ --help ] [ -v ] \
 	[ -b {slim|fat} ] [ -d directory ] [ -l localtime ] [ -L leapseconds ] \
 	[ -p posixrules ] [ -r '[@lo][/@hi]' ] [ -t localtime-link ] \
 	[ filename ... ]
 
 Report bugs to <http://www.debian.org/Bugs/>.
 ```
 
 - - -
 
 ### libc-dev-bin
 
  This package contains utility programs related to the GNU C Library
  development package.
   
   * gencat: generate message catalogs
 
 **Installed size:** `92 KB`  
 **How to install:** `sudo apt install libc-dev-bin`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### gencat
 
 Generate message catalog
 
 ```
 root@kali:~# gencat --help
 Usage: gencat [OPTION...] -o OUTPUT-FILE [INPUT-FILE]...
   or:  gencat [OPTION...] [OUTPUT-FILE [INPUT-FILE]...]
 Generate message catalog.
 
   -H, --header=NAME          Create C header file NAME containing symbol
                              definitions
       --new                  Do not use existing catalog, force new output file
                             
   -o, --output=NAME          Write output to file NAME
   -?, --help                 Give this help list
       --usage                Give a short usage message
   -V, --version              Print program version
 
 Mandatory or optional arguments to long options are also mandatory or optional
 for any corresponding short options.
 
 If INPUT-FILE is -, input is read from standard input.  If OUTPUT-FILE
 is -, output is written to standard output.
 
 For bug reporting instructions, please see:
 <http://www.debian.org/Bugs/>.
 ```
 
 - - -
 
 ### libc-devtools
 
  This package contains development tools shipped by the GNU C
  Library.
   
   * memusage, memusagestat: profile a program's memory usage
   * mtrace: interpret the malloc trace log
   * sotruss: trace shared library calls
   * sprof: display shared object profiling data
 
 **Installed size:** `136 KB`  
 **How to install:** `sudo apt install libc-devtools`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libgd3 
 {{< /spoiler >}}
 
 ##### memusage
 
 Profile memory usage of a program
 
 ```
 root@kali:~# memusage --help
 Usage: memusage [OPTION]... PROGRAM [PROGRAMOPTION]...
 Profile memory usage of PROGRAM.
 
    -n,--progname=NAME     Name of the program file to profile
    -p,--png=FILE          Generate PNG graphic and store it in FILE
    -d,--data=FILE         Generate binary data file and store it in FILE
    -u,--unbuffered        Don't buffer output
    -b,--buffer=SIZE       Collect SIZE entries before writing them out
       --no-timer          Don't collect additional information through timer
    -m,--mmap              Also trace mmap & friends
 
    -?,--help              Print this help and exit
       --usage             Give a short usage message
    -V,--version           Print version information and exit
 
  The following options only apply when generating graphical output:
    -t,--time-based        Make graph linear in time
    -T,--total             Also draw graph of total memory use
       --title=STRING      Use STRING as title of the graph
    -x,--x-size=SIZE       Make graphic SIZE pixels wide
    -y,--y-size=SIZE       Make graphic SIZE pixels high
 
 Mandatory arguments to long options are also mandatory for any corresponding
 short options.
 
 
 For bug reporting instructions, please see:
 <http://www.debian.org/Bugs/>.
 ```
 
 - - -
 
 ##### memusagestat
 
 Generate graphic from memory profiling data
 
 ```
 root@kali:~# memusagestat --help
 Usage: memusagestat [OPTION...] DATAFILE [OUTFILE]
 Generate graphic from memory profiling data
 
   -o, --output=FILE          Name output file
   -s, --string=STRING        Title string used in output graphic
   -t, --time                 Generate output linear to time (default is linear
                              to number of function calls)
   -T, --total                Also draw graph for total memory consumption
   -x, --x-size=VALUE         Make output graphic VALUE pixels wide
   -y, --y-size=VALUE         Make output graphic VALUE pixels high
   -?, --help                 Give this help list
       --usage                Give a short usage message
   -V, --version              Print program version
 
 Mandatory or optional arguments to long options are also mandatory or optional
 for any corresponding short options.
 
 For bug reporting instructions, please see:
 <http://www.debian.org/Bugs/>.
 ```
 
 - - -
 
 ##### mtrace
 
 Interpret the malloc trace log
 Malloc tracing
 
 ```
 root@kali:~# mtrace --help
 Usage: mtrace [OPTION]... [Binary] MtraceData
   --help       print this help, then exit
   --version    print version number, then exit
 
 For bug reporting instructions, please see:
 <http://www.debian.org/Bugs/>.
 ```
 
 - - -
 
 ##### sotruss
 
 Trace shared library calls through PLT
 
 ```
 root@kali:~# sotruss --help
 Usage: sotruss [OPTION...] [--] EXECUTABLE [EXECUTABLE-OPTION...]
   -F, --from FROMLIST     Trace calls from objects on FROMLIST
   -T, --to TOLIST         Trace calls to objects on TOLIST
 
   -e, --exit              Also show exits from the function calls
   -f, --follow            Trace child processes
   -o, --output FILENAME   Write output to FILENAME (or FILENAME. in case
 			  -f is also used) instead of standard error
 
   -?, --help              Give this help list
       --usage             Give a short usage message
       --version           Print program version
 
 Mandatory arguments to long options are also mandatory for any corresponding
 short options.
 
 For bug reporting instructions, please see:
 <http://www.debian.org/Bugs/>.
 ```
 
 - - -
 
 ##### sprof
 
 Read and display shared object profiling data
 
 ```
 root@kali:~# sprof --help
 Usage: sprof [OPTION...] SHOBJ [PROFDATA]
 Read and display shared object profiling data.
 
  Output selection:
   -c, --call-pairs           print list of count paths and their number of use
   -p, --flat-profile         generate flat profile with counts and ticks
   -q, --graph                generate call graph
 
   -?, --help                 Give this help list
       --usage                Give a short usage message
   -V, --version              Print program version
 
 For bug reporting instructions, please see:
 <http://www.debian.org/Bugs/>.
 ```
 
 - - -
 
 ### libc-l10n
 
  This package contains the translation files for the GNU C library and
  utility programs.
 
 **Installed size:** `4.32 MB`  
 **How to install:** `sudo apt install libc-l10n`  
 
 
 - - -
 
 ### libc0.3
 
 
 **Installed size:** ` KB`  
 **How to install:** `sudo apt install libc0.3`  
 
 
 - - -
 
 ### libc0.3-dev
 
 
 **Installed size:** ` KB`  
 **How to install:** `sudo apt install libc0.3-dev`  
 
 
 - - -
 
 ### libc6
 
  Contains the standard libraries that are used by nearly all programs on
  the system. This package includes shared versions of the standard C library
  and the standard math library, as well as many others.
 
 **Installed size:** `12.68 MB`  
 **How to install:** `sudo apt install libc6`  
 
 {{< spoiler "Dependencies:" >}}
 * libgcc-s1
 {{< /spoiler >}}
 
 
 - - -
 
 ### libc6-amd64
 
 
 **Installed size:** ` KB`  
 **How to install:** `sudo apt install libc6-amd64`  
 
 
 - - -
 
 ### libc6-dbg
 
  This package contains the detached debugging symbols for the GNU C
  library.
 
 **Installed size:** `10.74 MB`  
 **How to install:** `sudo apt install libc6-dbg`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libc6-dev
 
  Contains the symlinks, headers, and object files needed to compile
  and link programs which use the standard C library.
 
 **Installed size:** `11.76 MB`  
 **How to install:** `sudo apt install libc6-dev`  
 
 {{< spoiler "Dependencies:" >}}
 * libc-dev-bin 
 * libc6 
 * libcrypt-dev
 * libnsl-dev
 * linux-libc-dev
 * rpcsvc-proto
 {{< /spoiler >}}
 
 
 - - -
 
 ### libc6-dev-i386
 
  Contains the symlinks and object files needed to compile and link programs
  which use the standard C library. This is the 32bit version of the
  library, meant for AMD64 systems.
 
 **Installed size:** `6.66 MB`  
 **How to install:** `sudo apt install libc6-dev-i386`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6-dev 
 * libc6-i386 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libc6-dev-x32
 
  Contains the symlinks and object files needed to compile and link programs
  which use the standard C library. This is the X32 ABI version of the
  library, meant for amd64 systems.
 
 **Installed size:** `7.50 MB`  
 **How to install:** `sudo apt install libc6-dev-x32`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6-dev 
 * libc6-dev-i386 
 * libc6-x32 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libc6-i386
 
  This package includes shared versions of the standard C
  library and the standard math library, as well as many others.
  This is the 32bit version of the library, meant for AMD64 systems.
 
 **Installed size:** `11.60 MB`  
 **How to install:** `sudo apt install libc6-i386`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libc6-mips32
 
 
 **Installed size:** ` KB`  
 **How to install:** `sudo apt install libc6-mips32`  
 
 
 - - -
 
 ### libc6-mips64
 
 
 **Installed size:** ` KB`  
 **How to install:** `sudo apt install libc6-mips64`  
 
 
 - - -
 
 ### libc6-mipsn32
 
 
 **Installed size:** ` KB`  
 **How to install:** `sudo apt install libc6-mipsn32`  
 
 
 - - -
 
 ### libc6-powerpc
 
 
 **Installed size:** ` KB`  
 **How to install:** `sudo apt install libc6-powerpc`  
 
 
 - - -
 
 ### libc6-ppc64
 
 
 **Installed size:** ` KB`  
 **How to install:** `sudo apt install libc6-ppc64`  
 
 
 - - -
 
 ### libc6-s390
 
 
 **Installed size:** ` KB`  
 **How to install:** `sudo apt install libc6-s390`  
 
 
 - - -
 
 ### libc6-sparc
 
 
 **Installed size:** ` KB`  
 **How to install:** `sudo apt install libc6-sparc`  
 
 
 - - -
 
 ### libc6-sparc64
 
 
 **Installed size:** ` KB`  
 **How to install:** `sudo apt install libc6-sparc64`  
 
 
 - - -
 
 ### libc6-x32
 
  This package includes shared versions of the standard C library and the
  standard math library, as well as many others. This is the X32 ABI version
  of the library, meant for AMD64 systems.
 
 **Installed size:** `11.27 MB`  
 **How to install:** `sudo apt install libc6-x32`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libc6.1
 
 
 **Installed size:** ` KB`  
 **How to install:** `sudo apt install libc6.1`  
 
 
 - - -
 
 ### libc6.1-dev
 
 
 **Installed size:** ` KB`  
 **How to install:** `sudo apt install libc6.1-dev`  
 
 
 - - -
 
 ### locales
 
  Machine-readable data files, shared objects and programs used by the
  C library for localization (l10n) and internationalization (i18n) support.
   
  This package contains tools to generate locale definitions from source
  files (included in this package). It allows you to customize which
  definitions actually get generated. This is a space-saver over how this
  package used to be, with all locales generated by default. This created
  a package that unpacked to an excess of 30 megs.
 
 **Installed size:** `15.48 MB`  
 **How to install:** `sudo apt install locales`  
 
 {{< spoiler "Dependencies:" >}}
 * debconf  | debconf-2.0
 * libc-bin 
 * libc-l10n 
 {{< /spoiler >}}
 
 ##### locale-gen
 
 Generate localisation files from templates
 
 ```
 root@kali:~# locale-gen -h
 Generating locales (this might take a while)...
   en_US.UTF-8... done
 Generation complete.
 ```
 
 - - -
 
 ##### update-locale
 
 Modify global locale settings
 
 ```
 root@kali:~# update-locale -h
 Usage: update-locale [OPTIONS] [LANG=locale] [LC_NUMERIC=locale] ...
 Options:
    --help              display this message and exit
    --reset             ignore variables defined in the locale file
    --locale-file=FILE  file containing locale variables
                        (Default: /etc/locale.conf)
    --no-checks         do not perform sanity checks on locale variables
 ```
 
 - - -
 
 ##### validlocale
 
 Test if a given locale is available
 
 ```
 root@kali:~# man validlocale
 validlocale(8)                                                  validlocale(8)
 
 NAME
        validlocale - Test if a given locale is available
 
 SYNTAX
        validlocale <locale>
 
 DESCRIPTION
        Test  if  the locale given as argument is a valid locale.  If it isn't,
        print on stdout the string to add to /etc/locale.gen to make locale-gen
        generate the locale (if it exists at all).
 
 FILES
        /usr/sbin/validlocale
        /usr/share/i18n/SUPPORTED
 
 ENVIRONMENT VARIABLES
        DEFAULTCHARSET
               Which charset to assume if the given locale is missing from  the
               list of supported locales.
 
 EXAMPLES
        If you give a valid locale as parameter, it outputs a string specifying
        this on stderr:
 
               % validlocale C
               locale 'C' valid and available
 
        When  given a invalid (not generated or just nonexistent), it outputs a
        string on stderr telling that this is an invalid locale, and  a  string
        to stdout with the string to add to /etc/locale.gen to have this locale
        generated:
 
               % validlocale de_AU@euro
               locale 'de_AU@euro' not available
               de_AU@euro ISO-8859-15
 
 AUTHORS
        Petter Reinholdtsen <pere@hungry.com>
 
 SEE ALSO
        locale-gen(8), localedef(1), locale(1)
 
 Petter Reinholdtsen                   0.1                       validlocale(8)
 ```
 
 - - -
 
 ### locales-all
 
  This package contains the precompiled locale data for all supported locales.
  A better alternative is to install the locales package and only select
  desired locales, but it can be useful on a low-memory machine because some
  locale files take a lot of memory to be compiled.
 
 **Installed size:** `222.30 MB`  
 **How to install:** `sudo apt install locales-all`  
 
 {{< spoiler "Dependencies:" >}}
 * libc-l10n 
 {{< /spoiler >}}
 
 
 - - -
 
 ### nscd
 
  A daemon which handles passwd, group and host lookups
  for running programs and caches the results for the next
  query. You should install this package only if you use
  slow services like LDAP, NIS or NIS+.
 
 **Installed size:** `246 KB`  
 **How to install:** `sudo apt install nscd`  
 
 {{< spoiler "Dependencies:" >}}
 * init-system-helpers 
 * libaudit1 
 * libc6 
 * libcap2 
 * libselinux1 
 {{< /spoiler >}}
 
 ##### nscd
 
 Name service caching daemon
 
 ```
 root@kali:~# nscd --help
 Usage: nscd [OPTION...]
 Name Service Cache Daemon.
 
   -d, --debug                Do not fork and display messages on the current
                              tty
   -f, --config-file=NAME     Read configuration data from NAME
   -F, --foreground           Do not fork, but otherwise behave like a daemon
   -g, --statistics           Print current configuration statistics
   -i, --invalidate=TABLE     Invalidate the specified cache
   -K, --shutdown             Shut the server down
   -p, --print=NAME           Print contents of the offline cache file NAME
   -t, --nthreads=NUMBER      Start NUMBER threads
   -?, --help                 Give this help list
       --usage                Give a short usage message
   -V, --version              Print program version
 
 Mandatory or optional arguments to long options are also mandatory or optional
 for any corresponding short options.
 
 Supported tables:
 passwd group hosts services netgroup
 
 For bug reporting instructions, please see:
 <http://www.debian.org/Bugs/>.
 ```
 
 - - -
 
 ##### nscd
 
 Name service caching daemon
 
 ```
 root@kali:~# nscd --help
 Usage: nscd [OPTION...]
 Name Service Cache Daemon.
 
   -d, --debug                Do not fork and display messages on the current
                              tty
   -f, --config-file=NAME     Read configuration data from NAME
   -F, --foreground           Do not fork, but otherwise behave like a daemon
   -g, --statistics           Print current configuration statistics
   -i, --invalidate=TABLE     Invalidate the specified cache
   -K, --shutdown             Shut the server down
   -p, --print=NAME           Print contents of the offline cache file NAME
   -t, --nthreads=NUMBER      Start NUMBER threads
   -?, --help                 Give this help list
       --usage                Give a short usage message
   -V, --version              Print program version
 
 Mandatory or optional arguments to long options are also mandatory or optional
 for any corresponding short options.
 
 Supported tables:
 passwd group hosts services netgroup
 
 For bug reporting instructions, please see:
 <http://www.debian.org/Bugs/>.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
