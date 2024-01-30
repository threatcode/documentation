---
Title: curlftpfs
Homepage: http://curlftpfs.sourceforge.net
Repository: http://anonscm.debian.org/viewvc/collab-maint/deb-maint/curlftpfs/trunk/
Architectures: any
Version: 0.9.2-9
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### curlftpfs
 
  CurlFtpFS is a tool to mount FTP hosts as local directories. It connects
  to a FTP server and maps its directory structure to the local filesystem.
   
  Based on FUSE (filesystem in userspace) and the cURL library, CurlFtpFS
  has some features that distinguish it over other FTP filesystems:
   * support for SSLv3 and TLSv1
   * connecting through tunneling HTTP proxies
   * automatic reconnection if the server times out
   * conversion of absolute symlinks to point back into the FTP filesystem
 
 **Installed size:** `83 KB`  
 **How to install:** `sudo apt install curlftpfs`  
 
 {{< spoiler "Dependencies:" >}}
 * fuse
 * libc6 
 * libcurl3-gnutls 
 * libfuse2 
 * libglib2.0-0 
 {{< /spoiler >}}
 
 ##### curlftpfs
 
 Mount a ftp host as a local directory
 
 ```
 root@kali:~# curlftpfs -h
 usage: curlftpfs <ftphost> <mountpoint>
 
 CurlFtpFS options:
     -o opt,[opt...]        ftp options
     -v   --verbose         make libcurl print verbose debug
     -h   --help            print help
     -V   --version         print version
 
 FTP options:
     ftpfs_debug         print some debugging information
     transform_symlinks  prepend mountpoint to absolute symlink targets
     disable_epsv        use PASV, without trying EPSV first (default)
     enable_epsv         try EPSV before reverting to PASV
     skip_pasv_ip        skip the IP address for PASV
     ftp_port=STR        use PORT with address instead of PASV
     disable_eprt        use PORT, without trying EPRT first
     ftp_method          [multicwd/singlecwd] Control CWD usage
     custom_list=STR     Command used to list files. Defaults to "LIST -a"
     tcp_nodelay         use the TCP_NODELAY option
     connect_timeout=N   maximum time allowed for connection in seconds
     ssl                 enable SSL/TLS for both control and data connections
     ssl_control         enable SSL/TLS only for control connection
     ssl_try             try SSL/TLS first but connect anyway
     no_verify_hostname  does not verify the hostname (SSL)
     no_verify_peer      does not verify the peer (SSL)
     cert=STR            client certificate file (SSL)
     cert_type=STR       certificate file type (DER/PEM/ENG) (SSL)
     key=STR             private key file name (SSL)
     key_type=STR        private key file type (DER/PEM/ENG) (SSL)
     pass=STR            pass phrase for the private key (SSL)
     engine=STR          crypto engine to use (SSL)
     cacert=STR          file with CA certificates to verify the peer (SSL)
     capath=STR          CA directory to verify peer against (SSL)
     ciphers=STR         SSL ciphers to use (SSL)
     interface=STR       specify network interface/address to use
     krb4=STR            enable krb4 with specified security level
     proxy=STR           use host:port HTTP proxy
     proxytunnel         operate through a HTTP proxy tunnel (using CONNECT)
     proxy_anyauth       pick "any" proxy authentication method
     proxy_basic         use Basic authentication on the proxy
     proxy_digest        use Digest authentication on the proxy
     proxy_ntlm          use NTLM authentication on the proxy
     httpproxy           use a HTTP proxy (default)
     socks4              use a SOCKS4 proxy
     socks5              use a SOCKS5 proxy
     user=STR            set server user and password
     proxy_user=STR      set proxy user and password
     tlsv1               use TLSv1 (SSL)
     sslv3               use SSLv3 (SSL)
     ipv4                resolve name to IPv4 address
     ipv6                resolve name to IPv6 address
     utf8                try to transfer file list with utf-8 encoding
     codepage=STR        set the codepage the server uses
     iocharset=STR       set the charset used by the client
 
 CurlFtpFS cache options:  
     cache=yes|no              enable/disable cache (default: yes)
     cache_timeout=SECS        set timeout for stat, dir, link at once
                               default is 10 seconds
     cache_stat_timeout=SECS   set stat timeout
     cache_dir_timeout=SECS    set dir timeout
     cache_link_timeout=SECS   set link timeout
 
 FUSE options:
     -d   -o debug          enable debug output (implies -f)
     -f                     foreground operation
     -s                     disable multi-threaded operation
 
     -o allow_other         allow access to other users
     -o allow_root          allow access to root
     -o auto_unmount        auto unmount on process termination
     -o nonempty            allow mounts over non-empty file/dir
     -o default_permissions enable permission checking by kernel
     -o fsname=NAME         set filesystem name
     -o subtype=NAME        set filesystem type
     -o large_read          issue large read requests (2.4 only)
     -o max_read=N          set maximum size of read requests
 
     -o hard_remove         immediate removal (don't hide files)
     -o use_ino             let filesystem set inode numbers
     -o readdir_ino         try to fill in d_ino in readdir
     -o direct_io           use direct I/O
     -o kernel_cache        cache files in kernel
     -o [no]auto_cache      enable caching based on modification times (off)
     -o umask=M             set file permissions (octal)
     -o uid=N               set file owner
     -o gid=N               set file group
     -o entry_timeout=T     cache timeout for names (1.0s)
     -o negative_timeout=T  cache timeout for deleted names (0.0s)
     -o attr_timeout=T      cache timeout for attributes (1.0s)
     -o ac_attr_timeout=T   auto cache timeout for attributes (attr_timeout)
     -o noforget            never forget cached inodes
     -o remember=T          remember cached inodes for T seconds (0s)
     -o nopath              don't supply path if not necessary
     -o intr                allow requests to be interrupted
     -o intr_signal=NUM     signal to send on interrupt (10)
     -o modules=M1[:M2...]  names of modules to push onto filesystem stack
 
     -o max_write=N         set maximum size of write requests
     -o max_readahead=N     set maximum readahead
     -o max_background=N    set number of maximum background requests
     -o congestion_threshold=N  set kernel's congestion threshold
     -o async_read          perform reads asynchronously (default)
     -o sync_read           perform reads synchronously
     -o atomic_o_trunc      enable atomic open+truncate support
     -o big_writes          enable larger than 4kB writes
     -o no_remote_lock      disable remote file locking
     -o no_remote_flock     disable remote file locking (BSD)
     -o no_remote_posix_lock disable remove file locking (POSIX)
     -o [no_]splice_write   use splice to write to the fuse device
     -o [no_]splice_move    move data while splicing to the fuse device
     -o [no_]splice_read    use splice to read from the fuse device
 
 Module options:
 
 [iconv]
     -o from_code=CHARSET   original encoding of file names (default: UTF-8)
     -o to_code=CHARSET	    new encoding of the file names (default: ANSI_X3.4-1968)
 
 [subdir]
     -o subdir=DIR	    prepend this directory to all paths (mandatory)
     -o [no]rellinks	    transform absolute symlinks to relative
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
