---
Title: subversion
Homepage: http://subversion.apache.org/
Repository: https://salsa.debian.org/jamessan/subversion
Architectures: any all
Version: 1.14.2-5
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-802-11 kali-tools-information-gathering kali-tools-passwords kali-tools-top10 kali-tools-vulnerability kali-tools-web kali-tools-wireless 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### libapache2-mod-svn
 
  This package provides the mod_dav_svn and mod_authz_svn modules for
  the Apache 2.4 web server.  These modules provide Apache Subversion's WebDAV
  server backend, to serve repositories over the http and https
  protocols.  See the 'subversion' package for more information.
 
 **Installed size:** `406 KB`  
 **How to install:** `sudo apt install libapache2-mod-svn`  
 
 {{< spoiler "Dependencies:" >}}
 * apache2-api-20120211
 * apache2-bin 
 * libc6 
 * libsvn1 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libsvn-dev
 
  This package contains the symlinks, headers, and object files needed
  to compile and link programs which use libsvn1, the Apache Subversion
  libraries.  This package is needed only in order to compile software
  that uses libsvn1.
 
 **Installed size:** `1.91 MB`  
 **How to install:** `sudo apt install libsvn-dev`  
 
 {{< spoiler "Dependencies:" >}}
 * libapr1-dev
 * libaprutil1-dev
 * libsvn1 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libsvn-doc
 
  This package contains development (API) documentation for libsvn1, the
  Apache Subversion libraries.  See the 'libsvn1' package for more information.
 
 **Installed size:** `26.03 MB`  
 **How to install:** `sudo apt install libsvn-doc`  
 
 
 - - -
 
 ### libsvn-java
 
  This is a set of Java classes which provide the functionality of
  libsvn, the Apache Subversion libraries.  It is useful if you want to,
  for example, write a Java class that manipulates a Subversion repository
  or working copy.  See the 'subversion' package for more information.
 
 **Installed size:** `1.24 MB`  
 **How to install:** `sudo apt install libsvn-java`  
 
 {{< spoiler "Dependencies:" >}}
 * libapr1 
 * libc6 
 * libgcc-s1 
 * libstdc++6 
 * libsvn1 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libsvn-perl
 
  This is a set of Perl interfaces to libsvn, the Apache Subversion libraries.
  It is useful if you want to, for example, write a Perl script that
  manipulates a Subversion repository or working copy.  See the
  'subversion' package for more information.
 
 **Installed size:** `5.08 MB`  
 **How to install:** `sudo apt install libsvn-perl`  
 
 {{< spoiler "Dependencies:" >}}
 * libapr1 
 * libc6 
 * libsvn1 
 * perl 
 * perlapi-5.36.0
 {{< /spoiler >}}
 
 
 - - -
 
 ### libsvn1
 
  This package includes shared libraries to manipulate Apache Subversion
  (svn) repositories and working copies.  See the 'subversion' package for
  more information.
 
 **Installed size:** `4.21 MB`  
 **How to install:** `sudo apt install libsvn1`  
 
 {{< spoiler "Dependencies:" >}}
 * libapr1 
 * libaprutil1 
 * libc6 
 * libdb5.3
 * libexpat1 
 * liblz4-1 
 * libsasl2-2 
 * libserf-1-1 
 * libsqlite3-0 
 * libutf8proc3 
 * zlib1g 
 {{< /spoiler >}}
 
 
 - - -
 
 ### python3-subversion
 
  This is a set of Python3 interfaces to libsvn, the Apache Subversion
  libraries.  It is useful if you want to, for example, write a Python3
  script that manipulates a Subversion repository or working copy.  See
  the 'subversion' package for more information.
 
 **Installed size:** `5.08 MB`  
 **How to install:** `sudo apt install python3-subversion`  
 
 {{< spoiler "Dependencies:" >}}
 * libapr1 
 * libc6 
 * libsvn1 
 * python3
 * python3 
 {{< /spoiler >}}
 
 
 - - -
 
 ### ruby-svn
 
  This is a set of Ruby interfaces to libsvn, the Apache Subversion libraries.
  It is useful if you want to, for example, write a Ruby script that
  manipulates a Subversion repository or working copy.  See the
  'subversion' package for more information.
 
 **Installed size:** `2.71 MB`  
 **How to install:** `sudo apt install ruby-svn`  
 
 {{< spoiler "Dependencies:" >}}
 * libapr1 
 * libc6 
 * libruby3.1 
 * libsvn1 
 * ruby
 {{< /spoiler >}}
 
 
 - - -
 
 ### subversion
 
  Apache Subversion, also known as svn, is a centralised version control
  system.  Version control systems allow many individuals (who may be
  distributed geographically) to collaborate on a set of files (source
  code, websites, etc).  Subversion began with a CVS paradigm and
  supports all the major features of CVS, but has evolved to support
  many features that CVS users often wish they had.
   
  This package includes the Subversion client (svn, svnsync), repository
  administration tools (svnadmin, svnlook) and a network server (svnserve).
 
 **Installed size:** `4.72 MB`  
 **How to install:** `sudo apt install subversion`  
 
 {{< spoiler "Dependencies:" >}}
 * libapr1 
 * libaprutil1 
 * libc6 
 * libsvn1 
 {{< /spoiler >}}
 
 ##### svn
 
 Subversion command line client tool
 
 ```
 root@kali:~# svn -h
 usage: svn <subcommand> [options] [args]
 Subversion command-line client.
 Type 'svn help <subcommand>' for help on a specific subcommand.
 Type 'svn --version' to see the program version and RA modules,
      'svn --version --verbose' to see dependency versions as well,
      'svn --version --quiet' to see just the version number.
 
 Most subcommands take file and/or directory arguments, recursing
 on the directories.  If no arguments are supplied to such a
 command, it recurses on the current directory (inclusive) by default.
 
 Available subcommands:
    add
    auth
    blame (praise, annotate, ann)
    cat
    changelist (cl)
    checkout (co)
    cleanup
    commit (ci)
    copy (cp)
    delete (del, remove, rm)
    diff (di)
    export
    help (?, h)
    import
    info
    list (ls)
    lock
    log
    merge
    mergeinfo
    mkdir
    move (mv, rename, ren)
    patch
    propdel (pdel, pd)
    propedit (pedit, pe)
    propget (pget, pg)
    proplist (plist, pl)
    propset (pset, ps)
    relocate
    resolve
    resolved
    revert
    status (stat, st)
    switch (sw)
    unlock
    update (up)
    upgrade
 
 Subversion is a tool for version control.
 For additional information, see http://subversion.apache.org/
 ```
 
 - - -
 
 ##### svnadmin
 
 Subversion repository administration tool
 
 ```
 root@kali:~# svnadmin -h
 general usage: svnadmin SUBCOMMAND REPOS_PATH  [ARGS & OPTIONS ...]
 Subversion repository administration tool.
 Type 'svnadmin help <subcommand>' for help on a specific subcommand.
 Type 'svnadmin --version' to see the program version and FS modules.
 
 Available subcommands:
    build-repcache
    crashtest
    create
    delrevprop
    deltify
    dump
    dump-revprops
    freeze
    help (?, h)
    hotcopy
    info
    list-dblogs
    list-unused-dblogs
    load
    load-revprops
    lock
    lslocks
    lstxns
    pack
    recover
    rev-size
    rmlocks
    rmtxns
    setlog
    setrevprop
    setuuid
    unlock
    upgrade
    verify
 
 ```
 
 - - -
 
 ##### svnauthz
 
 
 ```
 root@kali:~# svnauthz -h
 general usage: svnauthz SUBCOMMAND TARGET [ARGS & OPTIONS ...]
                svnauthz-validate TARGET
 
 If the command name starts with 'svnauthz-validate', runs in
 pre-1.8 compatibility mode: run the 'validate' subcommand on TARGET.
 
 Type 'svnauthz help <subcommand>' for help on a specific subcommand.
 Type 'svnauthz --version' to see the program version.
 
 Available subcommands:
    help (?, h)
    validate
    accessof
 
 ```
 
 - - -
 
 ##### svnauthz-validate
 
 
 
 - - -
 
 ##### svnbench
 
 
 ```
 root@kali:~# svnbench -h
 usage: svnbench <subcommand> [options] [args]
 Subversion benchmarking tool.
 Type 'svnbench help <subcommand>' for help on a specific subcommand.
 Type 'svnbench --version' to see the program version and RA modules
   or 'svnbench --version --quiet' to see just the version number.
 
 Most subcommands take file and/or directory arguments, recursing
 on the directories.  If no arguments are supplied to such a
 command, it recurses on the current directory (inclusive) by default.
 
 Available subcommands:
    help (?, h)
    null-blame
    null-export
    null-list (ls)
    null-log
    null-info
 
 Subversion is a tool for version control.
 For additional information, see http://subversion.apache.org/
 ```
 
 - - -
 
 ##### svndumpfilter
 
 Filter a subversion repository 'dumpfile'.
 
 ```
 root@kali:~# svndumpfilter -h
 general usage: svndumpfilter SUBCOMMAND [ARGS & OPTIONS ...]
 Subversion repository dump filtering tool.
 Type 'svndumpfilter help <subcommand>' for help on a specific subcommand.
 Type 'svndumpfilter --version' to see the program version.
 
 Available subcommands:
    exclude
    include
    help (?, h)
 
 ```
 
 - - -
 
 ##### svnfsfs
 
 
 ```
 root@kali:~# svnfsfs -h
 general usage: svnfsfs SUBCOMMAND REPOS_PATH  [ARGS & OPTIONS ...]
 Subversion FSFS repository manipulation tool.
 Type 'svnfsfs help <subcommand>' for help on a specific subcommand.
 Type 'svnfsfs --version' to see the program version.
 
 Available subcommands:
    help (?, h)
    dump-index
    load-index
    stats
 
 ```
 
 - - -
 
 ##### svnlook
 
 Subversion repository examination tool
 
 ```
 root@kali:~# svnlook -h
 general usage: svnlook SUBCOMMAND REPOS_PATH [ARGS & OPTIONS ...]
 Subversion repository inspection tool.
 Type 'svnlook help <subcommand>' for help on a specific subcommand.
 Type 'svnlook --version' to see the program version and FS modules.
 Note: any subcommand which takes the '--revision' and '--transaction'
       options will, if invoked without one of those options, act on
       the repository's youngest revision.
 
 Available subcommands:
    author
    cat
    changed
    date
    diff
    dirs-changed
    filesize
    help (?, h)
    history
    info
    lock
    log
    propget (pget, pg)
    proplist (plist, pl)
    tree
    uuid
    youngest
 
 ```
 
 - - -
 
 ##### svnmucc
 
 Multiple URL Command Client for Subversion
 
 ```
 root@kali:~# svnmucc -h
 usage: svnmucc ACTION...
 Subversion multiple URL command client.
 Type 'svnmucc --version' to see the program version and RA modules.
 
   Perform one or more Subversion repository URL-based ACTIONs, committing
   the result as a (single) new revision.
 
 Actions:
   cp REV SRC-URL DST-URL : copy SRC-URL@REV to DST-URL
   mkdir URL              : create new directory URL
   mv SRC-URL DST-URL     : move SRC-URL to DST-URL
   rm URL                 : delete URL
   put SRC-FILE URL       : add or modify file URL with contents copied from
                            SRC-FILE (use "-" to read from standard input)
   propset NAME VALUE URL : set property NAME on URL to VALUE
   propsetf NAME FILE URL : set property NAME on URL to value read from FILE
   propdel NAME URL       : delete property NAME from URL
 
 Valid options:
   -h, -? [--help]        : display this text
   -m [--message] ARG     : use ARG as a log message
   -F [--file] ARG        : read log message from file ARG
   -u [--username] ARG    : commit the changes as username ARG
   -p [--password] ARG    : use ARG as the password
   --password-from-stdin  : read password from stdin
   -U [--root-url] ARG    : interpret all action URLs relative to ARG
   -r [--revision] ARG    : use revision ARG as baseline for changes
   --with-revprop ARG     : set revision property in the following format:
                                NAME[=VALUE]
   --non-interactive      : do no interactive prompting (default is to
                            prompt only if standard input is a terminal)
   --force-interactive    : do interactive prompting even if standard
                            input is not a terminal
   --trust-server-cert    : deprecated;
                            same as --trust-server-cert-failures=unknown-ca
   --trust-server-cert-failures ARG
                            with --non-interactive, accept SSL server
                            certificates with failures; ARG is comma-separated
                            list of 'unknown-ca' (Unknown Authority),
                            'cn-mismatch' (Hostname mismatch), 'expired'
                            (Expired certificate),'not-yet-valid' (Not yet
                            valid certificate) and 'other' (all other not
                            separately classified certificate errors).
   -X [--extra-args] ARG  : append arguments from file ARG (one per line;
                            use "-" to read from standard input)
   --config-dir ARG       : use ARG to override the config directory
   --config-option ARG    : use ARG to override a configuration option
   --no-auth-cache        : do not cache authentication tokens
   --version              : print version information
 ```
 
 - - -
 
 ##### svnrdump
 
 Subversion remote repository dumper and loader
 
 ```
 root@kali:~# svnrdump -h
 general usage: svnrdump SUBCOMMAND URL [-r LOWER[:UPPER]]
 Subversion remote repository dump and load tool.
 Type 'svnrdump help <subcommand>' for help on a specific subcommand.
 Type 'svnrdump --version' to see the program version and RA modules.
 
 Available subcommands:
    dump
    load
    help (?, h)
 
 ```
 
 - - -
 
 ##### svnserve
 
 Server for the 'svn' repository access method
 
 ```
 root@kali:~# svnserve -h
 usage: svnserve [-d | -i | -t | -X] [options]
 Subversion repository server.
 Type 'svnserve --version' to see the program version.
 
 Valid options:
   -d [--daemon]            : daemon mode
   -i [--inetd]             : inetd mode
   -t [--tunnel]            : tunnel mode
   -X [--listen-once]       : listen-once mode (useful for debugging)
   -r [--root] ARG          : root of directory to serve
   -R [--read-only]         : force read only, overriding repository config file
   --config-file ARG        : read configuration from file ARG
   --listen-port ARG        : listen port. The default port is 3690.
                              [mode: daemon, listen-once]
   --listen-host ARG        : listen hostname or IP address
                              By default svnserve listens on all addresses.
                              [mode: daemon, listen-once]
   -6 [--prefer-ipv6]       : prefer IPv6 when resolving the listen hostname
                              [IPv4 is preferred by default. Using IPv4 and IPv6
                              at the same time is not supported in daemon mode.
                              Use inetd mode or tunnel mode if you need this.]
   -c [--compression] ARG   : compression level to use for network transmissions
                              [0 .. no compression, 5 .. default, 
                               9 .. maximum compression]
   -M [--memory-cache-size] ARG : size of the extra in-memory cache in MB used to
                              minimize redundant operations.
                              Default is 16.
                              0 switches to dynamically sized caches.
                              [used for FSFS and FSX repositories only]
   --cache-txdeltas ARG     : enable or disable caching of deltas between older
                              revisions.
                              Default is yes.
                              [used for FSFS and FSX repositories only]
   --cache-fulltexts ARG    : enable or disable caching of file contents
                              Default is yes.
                              [used for FSFS and FSX repositories only]
   --cache-revprops ARG     : enable or disable caching of revision properties.
                              Consult the documentation before activating this.
                              Default is no.
                              [used for FSFS and FSX repositories only]
   --cache-nodeprops ARG    : enable or disable caching of node properties
                              Default is yes.
                              [used for FSFS repositories only]
   --client-speed ARG       : Optimize network handling based on the assumption
                              that most clients are connected with a bitrate of
                              ARG Mbit/s.
                              Default is 0 (optimizations disabled).
   --block-read ARG         : Parse and cache all data found in block instead
                              of just the requested item.
                              Default is no.
                              [used for FSFS repositories in 1.9 format only]
   -T [--threads]           : use threads instead of fork [mode: daemon]
   --min-threads ARG        : Minimum number of server threads, even if idle.
                              Capped to max-threads; minimum value is 0.
                              Default is 1.
                              [used only with --threads]
   --max-threads ARG        : Maximum number of server threads, even if there
                              are more connections.  Minimum value is 1.
                              Default is 256.
                              [used only with --threads]
   --max-request-size ARG   : Maximum acceptable size of a client request in MB.
                              This implicitly limits the length of paths and
                              property values that can be sent to the server.
                              Also the peak memory usage for protocol handling
                              per server thread or sub-process.
                              0 disables the size check; default is 16.
   --max-response-size ARG  : Maximum acceptable server response size in MB.
                              Longer responses get truncated and return an
                              error.  This limits the server load e.g. when
                              checking out at the wrong path level.
                              Default is 0 (disabled).
   --foreground             : run in foreground (useful for debugging)
                              [mode: daemon]
   --single-thread          : handle one connection at a time in the parent
                              process (useful for debugging)
   --log-file ARG           : svnserve log file
   --pid-file ARG           : write server process ID to file ARG
                              [mode: daemon, listen-once]
   --tunnel-user ARG        : tunnel username (default is current uid's name)
                              [mode: tunnel]
   -h [--help]              : display this help
   --virtual-host           : virtual host mode (look for repo in directory
                              of provided hostname)
   --version                : show program version information
   -q [--quiet]             : no progress (only errors) to stderr
 
 ```
 
 - - -
 
 ##### svnsync
 
 Subversion repository synchronization tool
 
 ```
 root@kali:~# svnsync -h
 general usage: svnsync SUBCOMMAND DEST_URL  [ARGS & OPTIONS ...]
 Subversion repository replication tool.
 Type 'svnsync help <subcommand>' for help on a specific subcommand.
 Type 'svnsync --version' to see the program version and RA modules.
 
 Available subcommands:
    initialize (init)
    synchronize (sync)
    copy-revprops
    info
    help (?, h)
 
 ```
 
 - - -
 
 ##### svnversion
 
 Produce a compact version identifier for a working copy.
 
 ```
 root@kali:~# svnversion -h
 usage: svnversion [OPTIONS] [WC_PATH [TRAIL_URL]]
 Subversion working copy identification tool.
 Type 'svnversion --version' to see the program version.
 
   Produce a compact version identifier for the working copy path
   WC_PATH.  TRAIL_URL is the trailing portion of the URL used to
   determine if WC_PATH itself is switched (detection of switches
   within WC_PATH does not rely on TRAIL_URL).  The version identifier
   is written to standard output.  For example:
 
     $ svnversion . /repos/svn/trunk
     4168
 
   The version identifier will be a single number if the working
   copy is single revision, unmodified, not switched and with
   a URL that matches the TRAIL_URL argument.  If the working
   copy is unusual the version identifier will be more complex:
 
    4123:4168     mixed revision working copy
    4168M         modified working copy
    4123S         switched working copy
    4123P         partial working copy, from a sparse checkout
    4123:4168MS   mixed revision, modified, switched working copy
 
   If WC_PATH is an unversioned path, the program will output
   'Unversioned directory' or 'Unversioned file'.  If WC_PATH is
   an added or copied or moved path, the program will output
   'Uncommitted local addition, copy or move'.
 
   If invoked without arguments WC_PATH will be the current directory.
 
 Valid options:
   -n [--no-newline]        : do not output the trailing newline
   -c [--committed]         : last changed rather than current revisions
   -h [--help]              : display this help
   --version                : show program version information
   -q [--quiet]             : no progress (only errors) to stderr
 
 ```
 
 - - -
 
 ### subversion-tools
 
  This package includes miscellaneous tools for use with Apache Subversion
  clients and servers:
   * svn-backup-dumps: Incremental dumpfile-based backup script
   * svn-bisect: Bisect revisions to find a regression
   * svn-clean: Remove unversioned files from a working copy
   * svn-hot-backup: Backup script, primarily for BDB repositories
   * svn_apply_autoprops: Apply property settings from
     .subversion/config file to an existing repository
   * svn_load_dirs: Sophisticated replacement for 'svn import'
   * svnwrap: Set umask to 002 before calling svn or svnserve
   * fsfs-access-map: Convert strace output into FSFS access map
   * several example hook scripts: commit-access-control, commit-email,
     log-police, mailer, svnperms, verify-po
   
  NOTE that some of these scripts are unsupported by upstream, and may
  change radically or disappear in future releases.  Some of these
  scripts require packages on the Recommends list.
 
 **Installed size:** `1.02 MB`  
 **How to install:** `sudo apt install subversion-tools`  
 
 {{< spoiler "Dependencies:" >}}
 * libapr1 
 * libc6 
 * libsvn1 
 * subversion
 {{< /spoiler >}}
 
 ##### fsfs-access-map
 
 
 ```
 root@kali:~# fsfs-access-map -h
 fsfs-access-map <file>
 
 Reads strace of some FSFS-based tool from <file>, prints some stats
 and writes a cluster access map to 'access.bmp' the current folder.
 Each pixel corresponds to one 64kB cluster and every line to a rev
 or packed rev file in the repository.  Turquoise and green indicate
 1 and 2 hits, yellow to read-ish colors for up to 20, shares of
 for up to 100 and black for > 200 hits.
 
 A typical strace invocation looks like this:
 strace -e trace=open,close,read,lseek -o strace.txt svn log ...
 ```
 
 - - -
 
 ##### fsfs-stats
 
 
 ```
 root@kali:~# fsfs-stats -h
 stats: usage: svnfsfs stats REPOS_PATH
 
 Write object size statistics to console.
 
 Valid options:
   -M [--memory-cache-size] ARG : size of the extra in-memory cache in MB used to
                              minimize redundant operations. Default: 16.
 
 ```
 
 - - -
 
 ##### svn-backup-dumps
 
 Create dumpfiles to backup a subversion repository.
 
 ```
 root@kali:~# svn-backup-dumps -h
 Usage: svn-backup-dumps.py [options] repospath dumpdir
 
 Options:
   --version             show program's version number and exit
   -h, --help            show this help message and exit
   -b                    compress the dump using python bzip2 library.
   -i                    perform incremental relative to last dump.
   --deltas              pass --deltas to svnadmin dump.
   -c CNT                count of revisions per dumpfile.
   -o                    overwrite files.
   -O                    overwrite all files.
   -q                    quiet.
   -r REV                revision number for single rev dump.
   -t TRANSFER           transfer dumps to another machine (s.a. --help-
                         transfer).
   -z                    compress the dump using python gzip library.
   --bzip2-path=BZIP2_PATH
                         compress the dump using bzip2 custom command.
   --gzip-path=GZIP_PATH
                         compress the dump using gzip custom command.
   --svnadmin-path=SVNADMIN_PATH
                         svnadmin command path.
   --svnlook-path=SVNLOOK_PATH
                         svnlook command path.
   --help-transfer       shows detailed help for the transfer option.
 ```
 
 - - -
 
 ##### svn-bisect
 
 Bisect Subversion revisions to find a regression
 
 ```
 root@kali:~# svn-bisect -h
 Usage:
   /usr/bin/svn-bisect start [good_rev [bad_rev]]
   /usr/bin/svn-bisect good [revision]
   /usr/bin/svn-bisect bad [revision]
   /usr/bin/svn-bisect run {command}
   /usr/bin/svn-bisect status
   /usr/bin/svn-bisect reset
 ```
 
 - - -
 
 ##### svn-clean
 
 Wipes out unversioned files from Subversion working copy
 
 ```
 root@kali:~# svn-clean -h
 Usage:
     svn-clean [options] [directory or file ...]
 
 Options:
     -e, --exclude
             A regular expression for filenames to be exluded. For example,
             the following command will skip files ending in ".zip":
 
                     svn-clean --exclude '\.zip$'
 
             Multiple exclude patterns can be specified. If at least one
             matches, then the file is skipped. For example, the following
             command will skip files ending in ".jpg" or ".png":
 
                     svn-clean --exclude '\.jpg$' --exclude '\.png$'
 
             The following command will skip the entire "build" subdirectory:
 
                     svn-clean --exclude '^build(/|$)'
 
     -f, --force
             Files to which you do not have delete access (if running under
             VMS) or write access (if running under another OS) will not be
             deleted unless you use this option.
 
     -N, --non-recursive
             Do not search recursively for unversioned files and directories.
             Unversioned directories will still be deleted along with all
             their contents.
 
     -q, --quiet
             Do not print progress info. In particular, do not print a
             message each time a file is examined, giving the name of the
             file, and indicating whether "rmdir" or "unlink" is used to
             remove it, or that it's skipped.
 
     -p, --print
             Do not delete anything. Instead, print the name of every file
             and directory that would have been deleted.
 
     -?, -h, --help
             Prints a brief help message and exits.
 
     --man   Prints the manual page and exits.
 
 ```
 
 - - -
 
 ##### svn-hot-backup
 
 Perform a "hot" backup of a Berkeley DB repository.
 
 ```
 root@kali:~# svn-hot-backup -h
 USAGE: svn-hot-backup [OPTIONS] REPOS_PATH BACKUP_PATH
 
 Create a backup of the repository at REPOS_PATH in a subdirectory of
 the BACKUP_PATH location, named after the youngest revision.
 
 Options:
   --archive-type=FMT Create an archive of the backup. FMT can be one of:
                        bz2  : Creates a bzip2 compressed tar file.
                        gz   : Creates a gzip compressed tar file.
                        zip  : Creates a compressed zip file.
                        zip64: Creates a zip64 file (can be > 2GB).
   --num-backups=N    Number of prior backups to keep around (0 to keep all).
   --verify           Verify the backup.
   --help      -h     Print this help message and exit.
 
 ```
 
 - - -
 
 ##### svn-mergeinfo-normalizer
 
 
 ```
 root@kali:~# svn-mergeinfo-normalizer -h
 usage: svn-mergeinfo-normalizer <subcommand> [options] [args]
 Subversion mergeinfo normalization and reduction tool.
 Type 'svn-mergeinfo-normalizer help <subcommand>' for help on a specific
 subcommand.  Type 'svn-mergeinfo-normalizer --version' to see the program
 version and RA modules or 'svn-mergeinfo-normalizer --version --quiet'
 to see just the version number.
 
 Most subcommands take file and/or directory arguments, recursing
 on the directories.  If no arguments are supplied to such a
 command, it recurses on the current directory (inclusive) by default.
 
 Available subcommands:
    help (?, h)
    analyze (analyse)
    normalize
    remove-branches
 
 Subversion is a tool for version control.
 For additional information, see http://subversion.apache.org/
 ```
 
 - - -
 
 ##### svn-populate-node-origins-index
 
 
 
 - - -
 
 ##### svn-vendor
 
 
 ```
 root@kali:~# svn-vendor -h
 usage: svn-vendor [-h] [--auto | --detect FILE | --apply FILE] [--save FILE]
                   [--config OPT VALUE]
                   wcdir importdir
 
 Prepare a working copy for SVN vendor import.
 
 positional arguments:
   wcdir               Path to working copy (destination of import)
   importdir           Path to imported sources (source of import)
 
 options:
   -h, --help          show this help message and exit
   --auto              Automatic mode: detect moves, apply them and copy
                       sources
   --detect FILE       Semi-automatic mode: detect moves and save them to FILE
   --apply FILE        Semi-automatic mode: apply the moves from FILE and copy
                       the sources
   --save FILE         Automatic mode: save moves to FILE after detection, then
                       proceed to apply the changes
   --config OPT VALUE  Set configuration option OPT to VALUE
 ```
 
 - - -
 
 ##### svn_apply_autoprops
 
 
 ```
 root@kali:~# svn_apply_autoprops -h
 This script reads the auto-properties defined in the file
 '/root/.subversion/config'
 and applies them recursively to all the files and directories in the
 current working copy.  It may behave differently than the Subversion
 command line; where the subversion command line may only apply a single
 matching auto-property to a single pathname, this script will apply all
 matching lines to a single pathname.
 
 Usage:
   svn_apply_autoprops [options] [WC_PATH]
 where WC_PATH is the path to a working copy.
 If WC_PATH is not specified, '.' is assumed.
 
 Valid options are:
   --help, -h         : Print this help text.
   --config ARG       : Read the Subversion config file at path ARG
                        instead of '/root/.subversion/config'.
 
 ```
 
 - - -
 
 ##### svn_load_dirs
 
 Load directories into a Subversion repository
 
 ```
 root@kali:~# svn_load_dirs -h
 Unknown option: h
 usage: /usr/bin/svn_load_dirs [options] svn_url svn_import_dir [dir_v1 [dir_v2 [..]]]
   svn_url        is the file:// or http:// URL of the svn repository
   svn_import_dir is the path relative to svn_url where to load dirs
   dir_v1 ..      list dirs to import otherwise read from stdin
 options are
   -no_user_input don't ask yes/no questions and assume yes answer
   -no_auto_exe   don't set svn:executable for executable files
   -p filename    table listing properties to apply to matching files
   -svn_username  username to perform commits as
   -svn_password  password to supply to svn commit
   -t tag_dir     create a tag copy in tag_dir, relative to svn_url
   -v             increase program verbosity, multiple -v's allowed
   -wc path       use the already checked-out working copy at path
                  instead of checkout out a fresh working copy
   -glob_ignores  List of filename patterns to ignore (as in svn's
                  global-ignores config option)
   -message       Final commit message
 ```
 
 - - -
 
 ##### svnraisetreeconflict
 
 
 ```
 root@kali:~# svnraisetreeconflict -h
 usage: svnraisetreeconflict [OPTIONS] WC_PATH NODE_KIND OPERATION ACTION REASON REPOS_URL1 PATH_IN_REPOS1 PEG_REV1 NODE_KIND1 REPOS_URL2 PATH_IN_REPOS2 PEG_REV2 NODE_KIND2
 
   Mark the working-copy node WC_PATH as being the victim of a tree conflict.
 
   WC_PATH's parent directory must be a working copy, otherwise a
   tree conflict cannot be raised.
 
 Valid options:
   -h [--help]              : display this help
   --version                : show program version information
 
 Valid enum argument values:
   NODE_KIND, NODE_KIND1, NODE_KIND2:
     none file dir unknown
   OPERATION:
     update switch merge
   ACTION (what svn tried to do):
     edit delete add
   REASON (what local change made svn fail):
     edited deleted missing obstructed added
   REPOS_URL1, REPOS_URL2:
     The URL of the repository itself, e.g.: file://usr/repos
   PATH_IN_REPOS1, PATH_IN_REPOS2:
     The complete path of the node in the repository, e.g.: sub/dir/foo
   PEG_REV1, PEG_REV2:
     The revision number at which the given path is relevant.
 
 Example:
   svnraisetreeconflict ./foo file update delete deleted file://usr/repos sub/dir/foo 1 file file://usr/repos sub/dir/foo 3 none
 
 ```
 
 - - -
 
 ##### svnwrap
 
 Umask wrapper for subversion client commands
 
 ```
 root@kali:~# svnwrap -h
 Usage: svnwrap {program} [args...]
 Valid programs: svn svnlook svnserve svnadmin svnversion
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
