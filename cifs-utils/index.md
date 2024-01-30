---
Title: cifs-utils
Homepage: https://www.samba.org/~jlayton/cifs-utils/
Repository: https://salsa.debian.org/samba-team/cifs-utils
Architectures: linux-any
Version: 2:7.0-2
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### cifs-utils
 
  The SMB/CIFS protocol provides support for cross-platform file sharing with
  Microsoft Windows, OS X, and other Unix systems.
   
  This package provides utilities for managing mounts of CIFS network
  file systems.
 
 **Installed size:** `317 KB`  
 **How to install:** `sudo apt install cifs-utils`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libcap-ng0 
 * libgssapi-krb5-2 
 * libkeyutils1 
 * libkrb5-3 
 * libpam0g 
 * libtalloc2 
 * libwbclient0 
 * python3
 {{< /spoiler >}}
 
 ##### cifs.idmap
 
 Userspace helper for mapping ids for Common Internet File System (CIFS)
 
 ```
 root@kali:~# cifs.idmap -h
 Usage: cifs.idmap [-h] [-v] [-t timeout] key_serial
 ```
 
 - - -
 
 ##### cifs.upcall
 
 Userspace upcall helper for Common Internet File System (CIFS)
 
 ```
 root@kali:~# man cifs.upcall
 CIFS.UPCALL(8)                                                  CIFS.UPCALL(8)
 
 NAME
        cifs.upcall  -  Userspace upcall helper for Common Internet File System
        (CIFS)
 
 SYNOPSIS
           cifs.upcall [--trust-dns|-t] [--version|-v] [--legacy-uid|-l]
                  [--krb5conf=/path/to/krb5.conf|-k         /path/to/krb5.conf]
                  [--keytab=/path/to/keytab|-K   /path/to/keytab]  [--expire|-e
                  nsecs] {keyid}
 
 DESCRIPTION
        This tool is part of the cifs-utils suite.
 
        cifs.upcall is a userspace helper program for  the  linux  CIFS  client
        filesystem.  There  are  a  number of activities that the kernel cannot
        easily do itself. This program is a callout  program  that  does  these
        things for the kernel and then returns the result.
 
        cifs.upcall  is  generally intended to be run when the kernel calls re-
        quest-key(8) for a particular key type. While it can  be  run  directly
        from the command-line, it's not generally intended to be run that way.
 
 OPTIONS
        -c     This option is deprecated and is currently ignored.
 
        --no-env-probe|-E
               Normally,  cifs.upcall will probe the environment variable space
               of the process that initiated the upcall in order to  fetch  the
               value  of  $KRB5CCNAME. This can assist the program with finding
               credential caches in non-default locations. If  this  option  is
               set,  then  the  program  won't do this and will rely on finding
               credcaches in the default locations specified in krb5.conf. Note
               that this is never performed when the  uid  is  0.  The  default
               credcache  location is always used when the uid is 0, regardless
               of the environment variable setting in the process.
 
        --krb5conf|-k=/path/to/krb5.conf
               This option allows administrators to set an  alternate  location
               for the krb5.conf file that cifs.upcall will use.
 
        --keytab=|-K=/path/to/keytab
               This option allows administrators to specify a keytab file to be
               used.  When  a user has no credential cache already established,
               cifs.upcall will attempt to use this keytab to acquire them. The
               default is the system-wide keytab /etc/krb5.keytab.
 
        --trust-dns|-t
               With krb5 upcalls, the name used as the host portion of the ser-
               vice principal defaults to the hostname portion of the UNC. This
               option allows the upcall program to reverse resolve the  network
               address of the server in order to get the hostname.
 
               This  is  less secure than not trusting DNS. When using this op-
               tion, it's possible that an attacker could get  control  of  DNS
               and  trick  the  client  into  mounting a different server alto-
               gether. It's preferable to instead add server principals to  the
               KDC  for  every  possible  hostname,  but this option exists for
               cases where that isn't possible. The default is to not trust re-
               verse hostname lookups in this fashion.
 
        --legacy-uid|-l
               Traditionally, the kernel has sent only a single uid=  parameter
               to  the  upcall  for  the SPNEGO upcall that's used to determine
               what user's credential cache to use.  This parameter is affected
               by the uid= mount option, which also governs  the  ownership  of
               files on the mount.
 
               Newer  kernels  send  a  creduid= option as well, which contains
               what uid it thinks actually owns the credentials that it's look-
               ing for. At mount time, this is generally set to the real uid of
               the user doing the mount. For multisession mounts, it's  set  to
               the  fsuid  of  the  mount  user.  Set  this  option if you want
               cifs.upcall to use the older uid= parameter instead of the  cre-
               duid= parameter.
 
        --expire|-e
               Override  default  timeout  value (600 seconds) for dns_resolver
               key.
 
        --version|-v
               Print version number and exit.
 
 ENVIRONMENT VARIABLES
        GSS_USE_PROXY="yes"
               Enable usage of gssproxy for credential retrieval. This includes
               keytab based client initiation as well as (Resource Based)  Con-
               strained Delegation.  See gssproxy-mech(8).
 
 CONFIGURATION FOR KEYCTL
        cifs.upcall  is  designed  to  be  called  from  the kernel via the re-
        quest-key callout program. This requires that request-key be told where
        and how to call this program.  The current cifs.upcall program  handles
        two different key types:
 
        cifs.spnego
               This keytype is for retrieving kerberos session keys
 
        dns_resolver
               This key type is for resolving hostnames into IP addresses. Sup-
               port for this key type may eventually be deprecated (see below).
 
               To  make this program useful for CIFS, you'll need to set up en-
               tries for them in request-key.conf(5). Here's an example  of  an
               entry for each key type:
 
                  #OPERATION  TYPE           D C PROGRAM ARG1 ARG2...
                  #=========  =============  = = ================================
                  create      cifs.spnego    * * /usr/sbin/cifs.upcall %k
                  create      dns_resolver   * * /usr/sbin/cifs.upcall %k
 
               See request-key.conf(5) for more info on each field.
 
               The  keyutils  package has also started including a dns_resolver
               handling program as well that  is  preferred  over  the  one  in
               cifs.upcall.  If  you  are  using a keyutils version equal to or
               greater than 1.5, you should use key.dns_resolver to handle  the
               dns_resolver  keytype  instead  of  cifs.upcall. See key.dns_re-
               solver(8) for more info.
 
 SEE ALSO
        request-key.conf(5), mount.cifs(8), key.dns_resolver(8)
 
 AUTHOR
        Igor Mammedov wrote the cifs.upcall program.
 
        Jeff Layton authored this manpage.
 
        The maintainer of the Linux CIFS VFS is Steve French.
 
        The Linux CIFS Mailing list is the preferred place to ask questions re-
        garding these programs.
 
                                                                 CIFS.UPCALL(8)
 ```
 
 - - -
 
 ##### cifscreds
 
 Manage NTLM credentials in kernel keyring
 
 ```
 root@kali:~# cifscreds -h
 cifscreds: invalid option -- 'h'
 Usage:
 	cifscreds add [-u username] [-d] <host|domain>
 	cifscreds clear [-u username] [-d] <host|domain>
 	cifscreds clearall 
 	cifscreds update [-u username] [-d] <host|domain>
 
 ```
 
 - - -
 
 ##### getcifsacl
 
 Userspace helper to display an ACL in a security descriptor for Common Internet File System (CIFS)
 
 ```
 root@kali:~# getcifsacl --help
 getcifsacl: invalid option -- '-'
 getcifsacl: Display CIFS/NTFS ACL in a security descriptor of a file object
 Usage: getcifsacl [option] <file_name1> [<file_name2>,<file_name3>,...]
 Valid options:
 	-h	Display this help text
 
 	-v	Version of the program
 
 	-R 	recurse into subdirectories
 
 	-r	Display raw values of the ACE fields
 
 Refer to getcifsacl(1) manpage for details
 ```
 
 - - -
 
 ##### mount.cifs
 
 Mount using the Common Internet File System (CIFS)
 
 ```
 root@kali:~# mount.cifs -h
 
 Usage:  mount.cifs <remotetarget> <dir> -o <options>
 
 Mount the remote target, specified as a UNC name, to a local directory.
 
 Options:
 	user=<arg>
 	pass=<arg>
 	dom=<arg>
 
 Less commonly used options:
 	credentials=<filename>,guest,perm,noperm,setuids,nosetuids,rw,ro,
 	sep=<char>,iocharset=<codepage>,suid,nosuid,exec,noexec,serverino,
 	noserverino,mapchars,nomapchars,nolock,servernetbiosname=<SRV_RFC1001NAME>
 	cache=<strict|none|loose>,nounix,cifsacl,sec=<authentication mechanism>,
 	sign,seal,fsc,snapshot=<token|time>,nosharesock,persistenthandles,
 	resilienthandles,rdma,vers=<smb_dialect>,cruid
 
 Options not needed for servers supporting CIFS Unix extensions
 	(e.g. unneeded for mounts to most Samba versions):
 	uid=<uid>,gid=<gid>,dir_mode=<mode>,file_mode=<mode>,sfu,
 	mfsymlinks,idsfromsid
 
 Rarely used options:
 	port=<tcpport>,rsize=<size>,wsize=<size>,unc=<unc_name>,ip=<ip_address>,
 	dev,nodev,nouser_xattr,netbiosname=<OUR_RFC1001NAME>,hard,soft,intr,
 	nointr,ignorecase,noposixpaths,noacl,prefixpath=<path>,nobrl,
 	echo_interval=<seconds>,actimeo=<seconds>,max_credits=<credits>,
 	bsize=<size>
 
 Options are described in more detail in the manual page
 	man 8 mount.cifs
 
 To display the version number of the mount helper:
 	mount.cifs -V
 ```
 
 - - -
 
 ##### mount.smb3
 
 Mount using the Common Internet File System (CIFS)
 
 ```
 root@kali:~# mount.smb3 -h
 
 Usage:  mount.smb3 <remotetarget> <dir> -o <options>
 
 Mount the remote target, specified as a UNC name, to a local directory.
 
 Options:
 	user=<arg>
 	pass=<arg>
 	dom=<arg>
 
 Less commonly used options:
 	credentials=<filename>,guest,perm,noperm,setuids,nosetuids,rw,ro,
 	sep=<char>,iocharset=<codepage>,suid,nosuid,exec,noexec,serverino,
 	noserverino,mapchars,nomapchars,nolock,servernetbiosname=<SRV_RFC1001NAME>
 	cache=<strict|none|loose>,nounix,cifsacl,sec=<authentication mechanism>,
 	sign,seal,fsc,snapshot=<token|time>,nosharesock,persistenthandles,
 	resilienthandles,rdma,vers=<smb_dialect>,cruid
 
 Options not needed for servers supporting CIFS Unix extensions
 	(e.g. unneeded for mounts to most Samba versions):
 	uid=<uid>,gid=<gid>,dir_mode=<mode>,file_mode=<mode>,sfu,
 	mfsymlinks,idsfromsid
 
 Rarely used options:
 	port=<tcpport>,rsize=<size>,wsize=<size>,unc=<unc_name>,ip=<ip_address>,
 	dev,nodev,nouser_xattr,netbiosname=<OUR_RFC1001NAME>,hard,soft,intr,
 	nointr,ignorecase,noposixpaths,noacl,prefixpath=<path>,nobrl,
 	echo_interval=<seconds>,actimeo=<seconds>,max_credits=<credits>,
 	bsize=<size>
 
 Options are described in more detail in the manual page
 	man 8 mount.smb3
 
 To display the version number of the mount helper:
 	mount.smb3 -V
 ```
 
 - - -
 
 ##### setcifsacl
 
 Userspace helper to alter components of a security descriptor for Common Internet File System (CIFS)
 
 ```
 root@kali:~# setcifsacl -h
 setcifsacl: Alter components of CIFS/NTFS security descriptor of a file object
 Usage: setcifsacl option [<list_of_ACEs>|<SID>] <file_name>
 Valid options:
 	-v	Version of the program
 	-U	Used in combination with -a, -D, -M, -S in order to 
 		apply the actions to SALC (aUdit ACL); if not specified, 
 		the actions apply to DACL
 
 	-a	Add ACE(s), separated by a comma, to an ACL
 	setcifsacl -a "ACL:Administrator:ALLOWED/0x0/FULL" <file_name>
 
 	-A	Add ACE(s) and reorder, separated by a comma, to an ACL
 	setcifsacl -A "ACL:Administrator:ALLOWED/0x0/FULL" <file_name>
 
 	-D	Delete ACE(s), separated by a comma, from an ACL
 	setcifsacl -D "ACL:Administrator:DENIED/0x0/D" <file_name>
 
 	-M	Modify ACE(s), separated by a comma, in an ACL
 	setcifsacl -M "ACL:user1:ALLOWED/0x0/0x1e01ff" <file_name>
 
 	-S	Replace existing ACL with ACE(s), separated by a comma
 	setcifsacl -S "ACL:Administrator:ALLOWED/0x0/D" <file_name>
 
 	-o	Set owner using specified SID (name or raw format)
 	setcifsacl -o "Administrator" <file_name>
 
 	-g	Set group using specified SID (name or raw format)
 	setcifsacl -g "Administrators" <file_name>
 
 Refer to setcifsacl(1) manpage for details
 ```
 
 - - -
 
 ##### smb2-quota
 
 Userspace helper to display quota information for the Linux SMB client file system (CIFS)
 
 ```
 root@kali:~# smb2-quota -h
 usage: smb2-quota [-h] [-t] [-c] [-l] <filename>
 
 Please specify an action to perform.
 
 positional arguments:
   <filename>     filename on a share
 
 options:
   -h, --help     show this help message and exit
   -t, --tabular  print quota information in tabular format
   -c, --csv      print quota information in csv format
   -l, --list     print quota information in list format
 ```
 
 - - -
 
 ##### smbinfo
 
 Userspace helper to display SMB-specific file information for the Linux SMB client file system (CIFS)
 
 ```
 root@kali:~# smbinfo -h
 usage: smbinfo [-h] [-V]
                {fileaccessinfo,filealigninfo,fileallinfo,filebasicinfo,fileeainfo,filefsfullsizeinfo,fileinternalinfo,filemodeinfo,filepositioninfo,filestandardinfo,filestreaminfo,fsctl-getobjid,getcompression,setcompression,list-snapshots,quota,secdesc,keys}
                ...
 
 Display SMB-specific file information using cifs IOCTL
 
 positional arguments:
   {fileaccessinfo,filealigninfo,fileallinfo,filebasicinfo,fileeainfo,filefsfullsizeinfo,fileinternalinfo,filemodeinfo,filepositioninfo,filestandardinfo,filestreaminfo,fsctl-getobjid,getcompression,setcompression,list-snapshots,quota,secdesc,keys}
                         sub-commands help
     fileaccessinfo      Prints FileAccessInfo for a cifs file
     filealigninfo       Prints FileAlignInfo for a cifs file
     fileallinfo         Prints FileAllInfo for a cifs file
     filebasicinfo       Prints FileBasicInfo for a cifs file
     fileeainfo          Prints FileEAInfo for a cifs file
     filefsfullsizeinfo  Prints FileFsFullSizeInfo for a cifs file
     fileinternalinfo    Prints FileInternalInfo for a cifs file
     filemodeinfo        Prints FileModeInfo for a cifs file
     filepositioninfo    Prints FilePositionInfo for a cifs file
     filestandardinfo    Prints FileStandardInfo for a cifs file
     filestreaminfo      Prints FileStreamInfo for a cifs file
     fsctl-getobjid      Prints the objectid of the file and GUID of the
                         underlying volume.
     getcompression      Prints the compression setting for the file
     setcompression      Sets the compression level for the file
     list-snapshots      List the previous versions of the volume that backs
                         this file
     quota               Prints the quota for a cifs file
     secdesc             Prints the security descriptor for a cifs file
     keys                Prints the decryption information needed to view
                         encrypted network traces
 
 options:
   -h, --help            show this help message and exit
   -V, --verbose         verbose output
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
