---
Title: nfs-utils
Homepage: https://linux-nfs.org/
Repository: https://salsa.debian.org/kernel-team/nfs-utils
Architectures: any
Version: 1:2.6.4-2
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-information-gathering kali-tools-vulnerability 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### libnfsidmap-dev
 
  Contains the header files and documentation for libnfsidmap
  for use in developing applications that use the libnfsidmap library.
   
  libnfsidmap provides functions to map between NFSv4 names (which are
  of the form user@domain) and local uid's and gid's.
 
 **Installed size:** `110 KB`  
 **How to install:** `sudo apt install libnfsidmap-dev`  
 
 {{< spoiler "Dependencies:" >}}
 * libnfsidmap1 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libnfsidmap1
 
  libnfsidmap provides functions to map between NFSv4 names (which are
  of the form user@domain) and local uid's and gid's.
 
 **Installed size:** `277 KB`  
 **How to install:** `sudo apt install libnfsidmap1`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libldap-2.5-0 
 {{< /spoiler >}}
 
 
 - - -
 
 ### nfs-common
 
  Use this package on any machine that uses NFS, either as client or
  server.  Programs included: lockd, statd, showmount, nfsstat, gssd,
  idmapd and mount.nfs.
 
 **Installed size:** `1.09 MB`  
 **How to install:** `sudo apt install nfs-common`  
 
 {{< spoiler "Dependencies:" >}}
 * adduser
 * init-system-helpers 
 * keyutils
 * libc6 
 * libcap2 
 * libcom-err2 
 * libdevmapper1.02.1 
 * libevent-core-2.1-7 
 * libgssapi-krb5-2 
 * libkeyutils1 
 * libkrb5-3 
 * libmount1 
 * libnfsidmap1 
 * libtirpc3 
 * libwrap0 
 * python3
 * rpcbind
 * ucf
 {{< /spoiler >}}
 
 ##### blkmapd
 
 PNFS block layout mapping daemon
 
 ```
 root@kali:~# blkmapd -h
 Usage: blkmapd [-hdf]
 ```
 
 - - -
 
 ##### mount.nfs
 
 Mount a Network File System
 
 ```
 root@kali:~# mount.nfs -h
 usage: mount.nfs remotetarget dir [-rvVwfnsh] [-o nfsoptions]
 options:
 	-r		Mount file system readonly
 	-v		Verbose
 	-V		Print version
 	-w		Mount file system read-write
 	-f		Fake mount, do not actually mount
 	-n		Do not update /etc/mtab
 	-s		Tolerate sloppy mount options rather than fail
 	-h		Print this help
 	nfsoptions	Refer to mount.nfs(8) or nfs(5)
 
 ```
 
 - - -
 
 ##### mount.nfs4
 
 Mount.nfs (8)        - mount a Network File System
 
 ```
 root@kali:~# mount.nfs4 -h
 usage: mount.nfs4 remotetarget dir [-rvVwfnsh] [-o nfsoptions]
 options:
 	-r		Mount file system readonly
 	-v		Verbose
 	-V		Print version
 	-w		Mount file system read-write
 	-f		Fake mount, do not actually mount
 	-n		Do not update /etc/mtab
 	-s		Tolerate sloppy mount options rather than fail
 	-h		Print this help
 	nfsoptions	Refer to mount.nfs(8) or nfs(5)
 
 ```
 
 - - -
 
 ##### mountstats
 
 Displays various NFS client per-mount statistics
 
 ```
 root@kali:~# mountstats -h
 usage: mountstats [-h] {mountstats,nfsstat,iostat} ...
 
 positional arguments:
   {mountstats,nfsstat,iostat}
                         sub-command help
     mountstats          Display a combination of per-op RPC statistics, NFS
                         event counts, and NFS byte counts. This is the default
                         sub-command if no sub-command is given.
     nfsstat             Display nfsstat-like statistics.
     iostat              Display iostat-like statistics.
 
 options:
   -h, --help            show this help message and exit
 
 For specific sub-command help, run 'mountstats SUB-COMMAND -h|--help'
 ```
 
 - - -
 
 ##### nfsconf
 
 Query various NFS configuration settings
 
 ```
 root@kali:~# nfsconf -h
 nfsconf: invalid option -- 'h'
 Usage: nfsconf [-v] [--file filename.conf] ...
 Options:
  -v			Increase Verbosity
  --file filename.conf	Load this config file
      (Default config file: /etc/nfs.conf
  --modified "info"	Use "info" in file modified header
 Modes:
   --dump [outputfile]
       Outputs the configuration to the named file
   --get [--arg subsection] {section} {tag}
       Output one specific config value
   --entry [--arg subsection] {section} {tag}
       Output the uninterpreted config entry
   --isset [--arg subsection] {section} {tag}
       Return code indicates if config value is present
   --set [--arg subsection] {section} {tag} {value}
       Set and Write a config value
   --unset [--arg subsection] {section} {tag}
       Remove an existing config value
 ```
 
 - - -
 
 ##### nfsidmap
 
 The NFS idmapper upcall program
 
 ```
 root@kali:~# nfsidmap -h
 nfsidmap: Usage: nfsidmap [-vh] [-c || [-u|-g|-r key] || -d || -l || [-t timeout] key desc]
 ```
 
 - - -
 
 ##### nfsiostat
 
 Emulate iostat for NFS mount points using /proc/self/mountstats
 
 ```
 root@kali:~# nfsiostat -h
 Usage: nfsiostat [ <interval> [ <count> ] ] [ <options> ] [ <mount point> ]
 
  Sample iostat-like program to display NFS client per-mount' statistics.  The
 <interval> parameter specifies the amount of time in seconds between each
 report.  The first report contains statistics for the time since each file
 system was mounted.  Each subsequent report contains statistics collected
 during the interval since the previous report.  If the <count> parameter is
 specified, the value of <count> determines the number of reports generated at
 <interval> seconds apart.  If the interval parameter is specified without the
 <count> parameter, the command generates reports continuously. If one or more
 <mount point> names are specified, statistics for only these mount points will
 be displayed.  Otherwise, all NFS mount points on the client are listed.
 
 Options:
   --version             show program's version number and exit
   -h, --help            show this help message and exit
 
   Statistics Options:
     File I/O is displayed unless one of the following is specified:
 
     -a, --attr          displays statistics related to the attribute cache
     -d, --dir           displays statistics related to directory operations
     -p, --page          displays statistics related to the page cache
 
   Display Options:
     Options affecting display format:
 
     -s, --sort          Sort NFS mount points by ops/second
     -l LIST, --list=LIST
                         only print stats for first LIST mount points
 ```
 
 - - -
 
 ##### nfsstat
 
 List NFS statistics
 
 ```
 root@kali:~# nfsstat --help
 Usage: nfsstat [OPTION]...
 
   -m, --mounts		Show statistics on mounted NFS filesystems
   -c, --client		Show NFS client statistics
   -s, --server		Show NFS server statistics
   -2			Show NFS version 2 statistics
   -3			Show NFS version 3 statistics
   -4			Show NFS version 4 statistics
   -o [facility]		Show statistics on particular facilities.
      nfs		NFS protocol information
      rpc		General RPC information
      net		Network layer statistics
      fh			Usage information on the server's file handle cache
      io			Usage information on the server's io statistics
      ra			Usage information on the server's read ahead cache
      rc			Usage information on the server's request reply cache
      all		Select all of the above
   -v, --verbose, --all	Same as '-o all'
   -r, --rpc		Show RPC statistics
   -n, --nfs		Show NFS statistics
   -Z[#], --sleep[=#]	Collects stats until interrupted.
 			    Cumulative stats are then printed
           		    If # is provided, stats will be output every
 			    # seconds.
   -S, --since file	Shows difference between current stats and those in 'file'
   -l, --list		Prints stats in list format
   --version		Show program version
   --help		What you just did
 
 ```
 
 - - -
 
 ##### rpc.gssd
 
 RPCSEC_GSS daemon
 
 ```
 root@kali:~# rpc.gssd -h
 rpc.gssd: invalid option -- 'h'
 usage: rpc.gssd [-f] [-l] [-M] [-n] [-v] [-r] [-p pipefsdir] [-k keytab] [-d ccachedir] [-t timeout] [-R preferred realm] [-D] [-H] [-U upcall timeout] [-C]
 ```
 
 - - -
 
 ##### rpc.idmapd
 
 NFSv4 ID <-> Name Mapper
 
 ```
 root@kali:~# rpc.idmapd -h
 Usage: rpc.idmapd [-hfvCS] [-p path] [-c path]
 ```
 
 - - -
 
 ##### rpc.statd
 
 NSM service daemon
 
 ```
 root@kali:~# rpc.statd -h
 usage: rpc.statd [options]
       -h, -?, --help       Print this help screen.
       -F, --foreground     Foreground (no-daemon mode)
       -d, --no-syslog      Verbose logging to stderr.  Foreground mode only.
       -p, --port           Port to listen on
       -o, --outgoing-port  Port for outgoing connections
       -V, -v, --version    Display version information and exit.
       -n, --name           Specify a local hostname.
       -P                   State directory path.
       -N                   Run in notify only mode.
       -L, --no-notify      Do not perform any notification.
       -H                   Specify a high-availability callout program.
 ```
 
 - - -
 
 ##### rpc.svcgssd
 
 Server-side rpcsec_gss daemon
 
 ```
 root@kali:~# rpc.svcgssd -h
 rpc.svcgssd: invalid option -- 'h'
 usage: rpc.svcgssd [-n] [-f] [-v] [-r] [-i] [-p principal]
 ```
 
 - - -
 
 ##### rpcctl
 
 Displays SunRPC connection information
 
 ```
 root@kali:~# rpcctl -h
 usage: rpcctl [-h] {client,switch,xprt} ...
 
 options:
   -h, --help            show this help message and exit
 
 commands:
   {client,switch,xprt}
     client              Commands for rpc clients
     switch              Commands for xprt switches
     xprt                Commands for individual xprts
 ```
 
 - - -
 
 ##### rpcdebug
 
 Set and clear NFS and RPC kernel debug flags
 
 ```
 root@kali:~# rpcdebug -h
 usage: rpcdebug [-v] [-h] [-m module] [-s flags...|-c flags...]
        set or cancel debug flags.
        (use rpcdebug -vh to get a list of modules and valid flags)
 ```
 
 - - -
 
 ##### showmount
 
 Show mount information for an NFS server
 
 ```
 root@kali:~# showmount -h
 Usage: showmount [-adehv]
        [--all] [--directories] [--exports]
        [--no-headers] [--help] [--version] [host]
 ```
 
 - - -
 
 ##### sm-notify
 
 Send reboot notifications to NFS peers
 
 ```
 root@kali:~# sm-notify -h
 sm-notify: invalid option -- 'h'
 Usage: sm-notify -notify [-dfq] [-m max-retry-minutes] [-p srcport]
             [-P /path/to/state/directory] [-v my_host_name]
 ```
 
 - - -
 
 ##### start-statd
 
 
 
 - - -
 
 ##### umount.nfs
 
 Unmount a Network File System
 
 ```
 root@kali:~# umount.nfs -h
 usage: umount.nfs dir [-fvnrlh]
 options:
 	-f	force unmount
 	-v	verbose
 	-n	Do not update /etc/mtab
 	-r	remount
 	-l	lazy unmount
 	-h	print this help
 
 ```
 
 - - -
 
 ##### umount.nfs4
 
 Umount.nfs (8)       - unmount a Network File System
 
 ```
 root@kali:~# umount.nfs4 -h
 usage: umount.nfs4 dir [-fvnrlh]
 options:
 	-f	force unmount
 	-v	verbose
 	-n	Do not update /etc/mtab
 	-r	remount
 	-l	lazy unmount
 	-h	print this help
 
 ```
 
 - - -
 
 ### nfs-kernel-server
 
  The NFS kernel server is currently the recommended NFS server for use
  with Linux, featuring features such as NFSv3 and NFSv4, Kerberos
  support via GSS, and much more. It is also significantly faster and
  usually more reliable than the user-space NFS servers (from the
  unfs3 and nfs-user-server packages). However, it is more difficult to
  debug than the user-space servers, and has a slightly different
  feature set.
   
  This package contains the user-space support needed to use the
  NFS kernel server. Most administrators wishing to set up an NFS server
  would want to install this package.
 
 **Installed size:** `769 KB`  
 **How to install:** `sudo apt install nfs-kernel-server`  
 
 {{< spoiler "Dependencies:" >}}
 * keyutils
 * libblkid1 
 * libc6 
 * libcap2 
 * libevent-core-2.1-7 
 * libsqlite3-0 
 * libtirpc3 
 * libuuid1 
 * libwrap0 
 * libxml2 
 * netbase
 * nfs-common 
 * ucf
 {{< /spoiler >}}
 
 ##### exportfs
 
 Maintain table of exported NFS file systems
 
 ```
 root@kali:~# exportfs -h
 usage: exportfs [-adfhioruvs] [host:/path]
 ```
 
 - - -
 
 ##### fsidd
 
 
 
 - - -
 
 ##### nfsdcld
 
 NFSv4 Client Tracking Daemon
 
 ```
 root@kali:~# nfsdcld -h
 nfsdcld [ -hFd ] [ -p pipefsdir ] [ -s storagedir ]
 ```
 
 - - -
 
 ##### nfsdclddb
 
 Tool for manipulating the nfsdcld sqlite database
 
 ```
 root@kali:~# nfsdclddb -h
 usage: nfsdclddb [-h] [-p PATH] {fix-table-names,downgrade-schema,print} ...
 
 positional arguments:
   {fix-table-names,downgrade-schema,print}
                         sub-command help
     fix-table-names     fix invalid table names
     downgrade-schema    downgrade database schema
     print               print database info
 
 options:
   -h, --help            show this help message and exit
   -p PATH, --path PATH  path to the database (default:
                         /var/lib/nfs/nfsdcld/main.sqlite)
 ```
 
 - - -
 
 ##### nfsdclnts
 
 Print various nfs client information for knfsd server.
 
 ```
 root@kali:~# nfsdclnts -h
 usage: nfsdclnts [-h] [-t type] [--clientinfo] [--hostname] [-v] [-f  [...]]
                  [-q]
 
 Parse the nfsd states and clientinfo files.
 
 options:
   -h, --help            show this help message and exit
   -t type, --type type  Input the type that you want to be printed: open,
                         lock, deleg, layout, all
   --clientinfo          output clients information, --hostname is implied.
   --hostname            print hostname of client instead of its ip address.
                         Longer hostnames are truncated.
   -v, --verbose         Verbose operation, show debug messages.
   -f  [ ...], --file  [ ...]
                         pass client states file, provided that info file
                         resides in the same directory.
   -q, --quiet           don't print the header information
 ```
 
 - - -
 
 ##### nfsdcltrack
 
 NFSv4 Client Tracking Callout Program
 
 ```
 root@kali:~# nfsdcltrack -h
 Usage: nfsdcltrack [ -hfd ] [ -s dir ] < cmd > < arg >
 Where < cmd > is one of the following and takes the following < arg >:
     init
     create <nfs_client_id4>
     remove <nfs_client_id4>
     check  <nfs_client_id4>
     gracedone <epoch time>
 ```
 
 - - -
 
 ##### nfsref
 
 Manage NFS referrals
 
 ```
 root@kali:~# nfsref -h
 nfsref: invalid option -- 'h'
 Usage: nfsref [ -t type ] SUBCOMMAND [ ARGUMENTS ]
 
 SUBCOMMAND is one of:
 	add        Add a new junction
 	remove     Remove an existing junction
 	lookup     Enumerate a junction
 
 Use "nfsref SUBCOMMAND -?" for details.
 ```
 
 - - -
 
 ##### rpc.mountd
 
 NFS mount daemon
 
 ```
 root@kali:~# rpc.mountd -h
 Usage: rpc.mountd [-F|--foreground] [-h|--help] [-v|--version] [-d kind|--debug kind]
 	[-l|--log-auth] [-i|--cache-use-ipaddr] [-T|--ttl ttl]
 	[-o num|--descriptors num]
 	[-p|--port port] [-V version|--nfs-version version]
 	[-N version|--no-nfs-version version] [-n|--no-tcp]
 	[-H prog |--ha-callout prog] [-r |--reverse-lookup]
 	[-s|--state-directory-path path] [-g|--manage-gids]
 	[-t num|--num-threads=num] [-u|--no-udp]
 ```
 
 - - -
 
 ##### rpc.nfsd
 
 NFS server process
 
 ```
 root@kali:~# rpc.nfsd -h
 Usage:
 rpc.nfsd [-d|--debug] [-H hostname] [-p|-P|--port port]
    [-N|--no-nfs-version version] [-V|--nfs-version version]
    [-s|--syslog] [-t|--tcp] [-T|--no-tcp] [-u|--udp] [-U|--no-udp]
    [-r|--rdma=] [-G|--grace-time secs] [-L|--leasetime secs] nrservs
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
