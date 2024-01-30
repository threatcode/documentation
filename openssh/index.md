---
Title: openssh
Homepage: https://www.openssh.com/
Repository: https://salsa.debian.org/ssh-team/openssh
Architectures: any all
Version: 1:9.4p1-1
Metapackages: kali-linux-core kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-linux-nethunter kali-linux-wsl 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### openssh-client
 
  This is the portable version of OpenSSH, a free implementation of
  the Secure Shell protocol as specified by the IETF secsh working
  group.
   
  Ssh (Secure Shell) is a program for logging into a remote machine
  and for executing commands on a remote machine.
  It provides secure encrypted communications between two untrusted
  hosts over an insecure network. X11 connections and arbitrary TCP/IP
  ports can also be forwarded over the secure channel.
  It can be used to provide applications with a secure communication
  channel.
   
  This package provides the ssh, scp and sftp clients, the ssh-agent
  and ssh-add programs to make public key authentication more convenient,
  and the ssh-keygen, ssh-keyscan, ssh-copy-id and ssh-argv0 utilities.
   
  In some countries it may be illegal to use any encryption at all
  without a special permit.
   
  ssh replaces the insecure rsh, rcp and rlogin programs, which are
  obsolete for most purposes.
 
 **Installed size:** `5.67 MB`  
 **How to install:** `sudo apt install openssh-client`  
 
 {{< spoiler "Dependencies:" >}}
 * adduser
 * libc6 
 * libedit2 
 * libfido2-1 
 * libgssapi-krb5-2 
 * libselinux1 
 * libssl3 
 * passwd
 * zlib1g 
 {{< /spoiler >}}
 
 ##### scp
 
 OpenSSH secure file copy
 
 ```
 root@kali:~# scp -h
 scp: unknown option -- h
 usage: scp [-346ABCOpqRrsTv] [-c cipher] [-D sftp_server_path] [-F ssh_config]
            [-i identity_file] [-J destination] [-l limit] [-o ssh_option]
            [-P port] [-S program] [-X sftp_option] source ... target
 ```
 
 - - -
 
 ##### sftp
 
 OpenSSH secure file transfer
 
 ```
 root@kali:~# sftp --help
 unknown option -- -
 usage: sftp [-46AaCfNpqrv] [-B buffer_size] [-b batchfile] [-c cipher]
           [-D sftp_server_command] [-F ssh_config] [-i identity_file]
           [-J destination] [-l limit] [-o ssh_option] [-P port]
           [-R num_requests] [-S program] [-s subsystem | sftp_server]
           [-X sftp_option] destination
 ```
 
 - - -
 
 ##### slogin
 
 OpenSSH remote login client
 
 ```
 root@kali:~# slogin -h
 unknown option -- h
 usage: ssh [-46AaCfGgKkMNnqsTtVvXxYy] [-B bind_interface] [-b bind_address]
            [-c cipher_spec] [-D [bind_address:]port] [-E log_file]
            [-e escape_char] [-F configfile] [-I pkcs11] [-i identity_file]
            [-J destination] [-L address] [-l login_name] [-m mac_spec]
            [-O ctl_cmd] [-o option] [-P tag] [-p port] [-Q query_option]
            [-R address] [-S ctl_path] [-W host:port] [-w local_tun[:remote_tun]]
            destination [command [argument ...]]
 ```
 
 - - -
 
 ##### ssh
 
 OpenSSH remote login client
 
 ```
 root@kali:~# ssh -h
 unknown option -- h
 usage: ssh [-46AaCfGgKkMNnqsTtVvXxYy] [-B bind_interface] [-b bind_address]
            [-c cipher_spec] [-D [bind_address:]port] [-E log_file]
            [-e escape_char] [-F configfile] [-I pkcs11] [-i identity_file]
            [-J destination] [-L address] [-l login_name] [-m mac_spec]
            [-O ctl_cmd] [-o option] [-P tag] [-p port] [-Q query_option]
            [-R address] [-S ctl_path] [-W host:port] [-w local_tun[:remote_tun]]
            destination [command [argument ...]]
 ```
 
 - - -
 
 ##### ssh-add
 
 Adds private key identities to the OpenSSH authentication agent
 
 ```
 root@kali:~# man ssh-add
 SSH-ADD(1)                  General Commands Manual                 SSH-ADD(1)
 
 NAME
        ssh-add  --  adds  private key identities to the OpenSSH authentication
        agent
 
 SYNOPSIS
        ssh-add  [-cDdKkLlqvXx]   [-E   fingerprint_hash]   [-H   hostkey_file]
                [-h destination_constraint] [-S provider] [-t life] [file ...]
        ssh-add -s pkcs11
        ssh-add -e pkcs11
        ssh-add -T pubkey ...
 
 DESCRIPTION
        ssh-add  adds  private  key  identities  to  the  authentication agent,
        ssh-agent(1).   When  run  without  arguments,  it   adds   the   files
        ~/.ssh/id_rsa,  ~/.ssh/id_ecdsa, ~/.ssh/id_ecdsa_sk, ~/.ssh/id_ed25519,
        ~/.ssh/id_ed25519_sk, and ~/.ssh/id_dsa.  After loading a private  key,
        ssh-add will try to load corresponding certificate information from the
        filename obtained by appending -cert.pub to the name of the private key
        file.  Alternative file names can be given on the command line.
 
        If any file requires a passphrase, ssh-add asks for the passphrase from
        the user.  The passphrase is read from the user's tty.  ssh-add retries
        the last passphrase if multiple identity files are given.
 
        The authentication agent must be running and the SSH_AUTH_SOCK environ-
        ment variable must contain the name of its socket for ssh-add to work.
 
        The options are as follows:
 
        -c      Indicates  that added identities should be subject to confirma-
                tion before being used  for  authentication.   Confirmation  is
                performed  by  ssh-askpass(1).  Successful confirmation is sig-
                naled by a zero exit status from  ssh-askpass(1),  rather  than
                text entered into the requester.
 
        -D      Deletes all identities from the agent.
 
        -d      Instead  of  adding  identities,  removes  identities  from the
                agent.  If ssh-add has been run without arguments, the keys for
                the default identities  and  their  corresponding  certificates
                will  be  removed.  Otherwise, the argument list will be inter-
                preted as a list of paths to public key files to  specify  keys
                and  certificates  to  be removed from the agent.  If no public
                key is found at a given path,  ssh-add  will  append  .pub  and
                retry.   If the argument list consists of "-" then ssh-add will
                read public keys to be removed from standard input.
 
        -E fingerprint_hash
                Specifies the hash algorithm used when displaying  key  finger-
                prints.  Valid options are: "md5" and "sha256".  The default is
                "sha256".
 
        -e pkcs11
                Remove keys provided by the PKCS#11 shared library pkcs11.
 
        -H hostkey_file
                Specifies  a  known  hosts  file to look up hostkeys when using
                destination-constrained keys via the -h flag.  This option  may
                be  specified  multiple  times  to  allow  multiple files to be
                searched.  If no files are specified, ssh-add will use the  de-
                fault  ssh_config(5)  known  hosts  files:  ~/.ssh/known_hosts,
                ~/.ssh/known_hosts2,       /etc/ssh/ssh_known_hosts,        and
                /etc/ssh/ssh_known_hosts2.
 
        -h destination_constraint
                When adding keys, constrain them to be usable only through spe-
                cific hosts or to specific destinations.
 
                Destination constraints of the form `[user@]dest-hostname' per-
                mit  use  of the key only from the origin host (the one running
                ssh-agent(1)) to the listed  destination  host,  with  optional
                user name.
 
                Constraints  of the form `src-hostname>[user@]dst-hostname' al-
                low a key available on a  forwarded  ssh-agent(1)  to  be  used
                through  a  particular host (as specified by `src-hostname') to
                authenticate to a further host, specified by `dst-hostname'.
 
                Multiple destination constraints  may  be  added  when  loading
                keys.   When attempting authentication with a key that has des-
                tination constraints,  the  whole  connection  path,  including
                ssh-agent(1)  forwarding,  is  tested against those constraints
                and each hop must be permitted for the attempt to succeed.  For
                example, if key is forwarded to a remote host, `host-b', and is
                attempting authentication to another host, `host-c',  then  the
                operation  will  be  successful  only if `host-b' was permitted
                from the origin host and the subsequent `host-b>host-c' hop  is
                also permitted by destination constraints.
 
                Hosts are identified by their host keys, and are looked up from
                known  hosts  files by ssh-add.  Wildcards patterns may be used
                for hostnames and certificate host keys are supported.  By  de-
                fault, keys added by ssh-add are not destination constrained.
 
                Destination  constraints  were  added  in  OpenSSH release 8.9.
                Support in both the remote SSH client and  server  is  required
                when   using  destination-constrained  keys  over  a  forwarded
                ssh-agent(1) channel.
 
                It is also important to note that destination  constraints  can
                only be enforced by ssh-agent(1) when a key is used, or when it
                is  forwarded  by  a cooperating ssh(1).  Specifically, it does
                not prevent an attacker with access to a  remote  SSH_AUTH_SOCK
                from  forwarding it again and using it on a different host (but
                only to a permitted destination).
 
        -K      Load resident keys from a FIDO authenticator.
 
        -k      When loading keys into or deleting keys from the agent, process
                plain private keys only and skip certificates.
 
        -L      Lists public key parameters of all identities currently  repre-
                sented by the agent.
 
        -l      Lists  fingerprints  of all identities currently represented by
                the agent.
 
        -q      Be quiet after a successful operation.
 
        -S provider
                Specifies a path to a library that will  be  used  when  adding
                FIDO authenticator-hosted keys, overriding the default of using
                the internal USB HID support.
 
        -s pkcs11
                Add keys provided by the PKCS#11 shared library pkcs11.
 
        -T pubkey ...
                Tests whether the private keys that correspond to the specified
                pubkey  files  are  usable by performing sign and verify opera-
                tions on each.
 
        -t life
                Set a maximum lifetime when adding identities to an agent.  The
                lifetime may be specified in seconds or in a time format speci-
                fied in sshd_config(5).
 
        -v      Verbose mode.  Causes ssh-add to print debugging messages about
                its progress.  This is helpful in debugging problems.  Multiple
                -v options increase the verbosity.  The maximum is 3.
 
        -X      Unlock the agent.
 
        -x      Lock the agent with a password.
 
 ENVIRONMENT
        DISPLAY, SSH_ASKPASS and SSH_ASKPASS_REQUIRE
                If ssh-add needs a passphrase, it will read the passphrase from
                the current terminal if it was run from a terminal.  If ssh-add
                does not have a terminal associated with  it  but  DISPLAY  and
                SSH_ASKPASS  are  set, it will execute the program specified by
                SSH_ASKPASS (by default "ssh-askpass") and open an  X11  window
                to read the passphrase.  This is particularly useful when call-
                ing ssh-add from a .xsession or related script.
 
                SSH_ASKPASS_REQUIRE  allows  further control over the use of an
                askpass program.  If this  variable  is  set  to  "never"  then
                ssh-add  will  never  attempt  to  use  one.   If  it is set to
                "prefer", then ssh-add will prefer to use the  askpass  program
                instead  of the TTY when requesting passwords.  Finally, if the
                variable is set to "force", then the askpass  program  will  be
                used  for all passphrase input regardless of whether DISPLAY is
                set.
 
        SSH_AUTH_SOCK
                Identifies the path of a Unix-domain socket used to communicate
                with the agent.
 
        SSH_SK_PROVIDER
                Specifies a path to a library that will be  used  when  loading
                any  FIDO  authenticator-hosted keys, overriding the default of
                using the built-in USB HID support.
 
 FILES
        ~/.ssh/id_dsa
        ~/.ssh/id_ecdsa
        ~/.ssh/id_ecdsa_sk
        ~/.ssh/id_ed25519
        ~/.ssh/id_ed25519_sk
        ~/.ssh/id_rsa
                Contains the DSA, ECDSA, authenticator-hosted  ECDSA,  Ed25519,
                authenticator-hosted  Ed25519 or RSA authentication identity of
                the user.
 
        Identity files should not be readable by anyone  but  the  user.   Note
        that ssh-add ignores identity files if they are accessible by others.
 
 EXIT STATUS
        Exit status is 0 on success, 1 if the specified command fails, and 2 if
        ssh-add is unable to contact the authentication agent.
 
 SEE ALSO
        ssh(1), ssh-agent(1), ssh-askpass(1), ssh-keygen(1), sshd(8)
 
 AUTHORS
        OpenSSH  is a derivative of the original and free ssh 1.2.12 release by
        Tatu Ylonen.  Aaron Campbell, Bob Beck, Markus  Friedl,  Niels  Provos,
        Theo  de  Raadt and Dug Song removed many bugs, re-added newer features
        and created OpenSSH.  Markus Friedl contributed  the  support  for  SSH
        protocol versions 1.5 and 2.0.
 
 Debian                         February 4, 2022                     SSH-ADD(1)
 ```
 
 - - -
 
 ##### ssh-agent
 
 OpenSSH authentication agent
 
 ```
 root@kali:~# ssh-agent -h
 unknown option -- h
 usage: ssh-agent [-c | -s] [-Dd] [-a bind_address] [-E fingerprint_hash]
                  [-O option] [-P allowed_providers] [-t life]
        ssh-agent [-a bind_address] [-E fingerprint_hash] [-O option]
                  [-P allowed_providers] [-t life] command [arg ...]
        ssh-agent [-c | -s] -k
 ```
 
 - - -
 
 ##### ssh-argv0
 
 Replaces the old ssh command-name as hostname handling
 
 ```
 root@kali:~# man ssh-argv0
 SSH-ARGV0(1)                General Commands Manual               SSH-ARGV0(1)
 
 NAME
        ssh-argv0 -- replaces the old ssh command-name as hostname handling
 
 SYNOPSIS
        hostname | user@hostname [-l login_name] [command]
 
        hostname   |  user@hostname  [-afgknqstvxACNTX1246]  [-b  bind_address]
        [-c cipher_spec] [-e escape_char] [-i  identity_file]  [-l  login_name]
        [-m   mac_spec]   [-o   option]   [-p   port]   [-F   configfile]   [-L
        port:host:hostport] [-R port:host:hostport] [-D port] [command]
 
 DESCRIPTION
        ssh-argv0 replaces the old ssh command-name as hostname  handling.   If
        you  link  to  this  script  with a hostname then executing the link is
        equivalent to having executed ssh with that hostname  as  an  argument.
        All other arguments are passed to ssh and will be processed normally.
 
 OPTIONS
        See ssh(1).
 
 FILES
        See ssh(1).
 
 AUTHORS
        OpenSSH  is a derivative of the original and free ssh 1.2.12 release by
        Tatu Ylonen.  Aaron Campbell, Bob Beck, Markus  Friedl,  Niels  Provos,
        Theo  de  Raadt and Dug Song removed many bugs, re-added newer features
        and created OpenSSH.  Markus Friedl contributed  the  support  for  SSH
        protocol  versions  1.5  and  2.0.   Natalie Amery wrote this ssh-argv0
        script and the associated documentation.
 
 SEE ALSO
        ssh(1)
 
 Debian Project                 September 7, 2001                  SSH-ARGV0(1)
 ```
 
 - - -
 
 ##### ssh-copy-id
 
 Use locally available keys to authorise logins on a remote machine
 
 ```
 root@kali:~# ssh-copy-id --help
 Illegal option --
 Usage: /usr/bin/ssh-copy-id [-h|-?|-f|-n|-s|-x] [-i [identity_file]] [-p port] [-F alternative ssh_config file] [-t target_path] [[-o <ssh -o options>] ...] [user@]hostname
 	-f: force mode -- copy keys without trying to check if they are already installed
 	-n: dry run    -- no keys are actually copied
 	-s: use sftp   -- use sftp instead of executing remote-commands. Can be useful if the remote only allows sftp
 	-x: debug      -- enables -x in this shell, for debugging
 	-h|-?: print this help
 ```
 
 - - -
 
 ##### ssh-keygen
 
 OpenSSH authentication key utility
 
 ```
 root@kali:~# ssh-keygen --help
 unknown option -- -
 usage: ssh-keygen [-q] [-a rounds] [-b bits] [-C comment] [-f output_keyfile]
                   [-m format] [-N new_passphrase] [-O option]
                   [-t dsa | ecdsa | ecdsa-sk | ed25519 | ed25519-sk | rsa]
                   [-w provider] [-Z cipher]
        ssh-keygen -p [-a rounds] [-f keyfile] [-m format] [-N new_passphrase]
                    [-P old_passphrase] [-Z cipher]
        ssh-keygen -i [-f input_keyfile] [-m key_format]
        ssh-keygen -e [-f input_keyfile] [-m key_format]
        ssh-keygen -y [-f input_keyfile]
        ssh-keygen -c [-a rounds] [-C comment] [-f keyfile] [-P passphrase]
        ssh-keygen -l [-v] [-E fingerprint_hash] [-f input_keyfile]
        ssh-keygen -B [-f input_keyfile]
        ssh-keygen -D pkcs11
        ssh-keygen -F hostname [-lv] [-f known_hosts_file]
        ssh-keygen -H [-f known_hosts_file]
        ssh-keygen -K [-a rounds] [-w provider]
        ssh-keygen -R hostname [-f known_hosts_file]
        ssh-keygen -r hostname [-g] [-f input_keyfile]
        ssh-keygen -M generate [-O option] output_file
        ssh-keygen -M screen [-f input_file] [-O option] output_file
        ssh-keygen -I certificate_identity -s ca_key [-hU] [-D pkcs11_provider]
                   [-n principals] [-O option] [-V validity_interval]
                   [-z serial_number] file ...
        ssh-keygen -L [-f input_keyfile]
        ssh-keygen -A [-a rounds] [-f prefix_path]
        ssh-keygen -k -f krl_file [-u] [-s ca_public] [-z version_number]
                   file ...
        ssh-keygen -Q [-l] -f krl_file [file ...]
        ssh-keygen -Y find-principals -s signature_file -f allowed_signers_file
        ssh-keygen -Y match-principals -I signer_identity -f allowed_signers_file
        ssh-keygen -Y check-novalidate -n namespace -s signature_file
        ssh-keygen -Y sign -f key_file -n namespace file [-O option] ...
        ssh-keygen -Y verify -f allowed_signers_file -I signer_identity
                   -n namespace -s signature_file [-r krl_file] [-O option]
 ```
 
 - - -
 
 ##### ssh-keyscan
 
 Gather SSH public keys from servers
 
 ```
 root@kali:~# ssh-keyscan -h
 unknown option -- h
 usage: ssh-keyscan [-46cDHv] [-f file] [-O option] [-p port] [-T timeout]
                    [-t type] [host | addrlist namelist]
 ```
 
 - - -
 
 ### openssh-server
 
  This is the portable version of OpenSSH, a free implementation of
  the Secure Shell protocol as specified by the IETF secsh working
  group.
   
  Ssh (Secure Shell) is a program for logging into a remote machine
  and for executing commands on a remote machine.
  It provides secure encrypted communications between two untrusted
  hosts over an insecure network. X11 connections and arbitrary TCP/IP
  ports can also be forwarded over the secure channel.
  It can be used to provide applications with a secure communication
  channel.
   
  This package provides the sshd server.
   
  In some countries it may be illegal to use any encryption at all
  without a special permit.
   
  sshd replaces the insecure rshd program, which is obsolete for most
  purposes.
 
 **Installed size:** `1.90 MB`  
 **How to install:** `sudo apt install openssh-server`  
 
 {{< spoiler "Dependencies:" >}}
 * adduser
 * debconf  | debconf-2.0
 * init-system-helpers 
 * libaudit1 
 * libc6 
 * libcom-err2 
 * libcrypt1 
 * libgssapi-krb5-2 
 * libkrb5-3 
 * libpam-modules
 * libpam-runtime
 * libpam0g 
 * libselinux1 
 * libssl3 
 * libsystemd0
 * libwrap0 
 * lsb-base
 * openssh-client 
 * openssh-sftp-server
 * procps
 * runit-helper 
 * ucf
 * zlib1g 
 {{< /spoiler >}}
 
 ##### sshd
 
 OpenSSH daemon
 
 ```
 root@kali:~# sshd -h
 option requires an argument -- h
 OpenSSH_9.4p1 Debian-1, OpenSSL 3.0.11 19 Sep 2023
 usage: sshd [-46DdeGiqTtV] [-C connection_spec] [-c host_cert_file]
             [-E log_file] [-f config_file] [-g login_grace_time]
             [-h host_key_file] [-o option] [-p port] [-u len]
 ```
 
 - - -
 
 ### openssh-sftp-server
 
  This is the portable version of OpenSSH, a free implementation of
  the Secure Shell protocol as specified by the IETF secsh working
  group.
   
  Ssh (Secure Shell) is a program for logging into a remote machine
  and for executing commands on a remote machine.
  It provides secure encrypted communications between two untrusted
  hosts over an insecure network. X11 connections and arbitrary TCP/IP
  ports can also be forwarded over the secure channel.
  It can be used to provide applications with a secure communication
  channel.
   
  This package provides the SFTP server module for the SSH server. It
  is needed if you want to access your SSH server with SFTP. The SFTP
  server module also works with other SSH daemons like dropbear.
   
  OpenSSH's sftp and sftp-server implement revision 3 of the SSH filexfer
  protocol described in:
   
   http://www.openssh.com/txt/draft-ietf-secsh-filexfer-02.txt
   
  Newer versions of the draft will not be supported, though some features
  are individually implemented as extensions.
 
 **Installed size:** `217 KB`  
 **How to install:** `sudo apt install openssh-sftp-server`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * openssh-client 
 {{< /spoiler >}}
 
 
 - - -
 
 ### openssh-tests
 
  This package provides OpenSSH's regression test suite.  It is mainly
  intended for use with the autopkgtest system, though can also be run
  directly using /usr/lib/openssh/regress/run-tests.
 
 **Installed size:** `7.55 MB`  
 **How to install:** `sudo apt install openssh-tests`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libselinux1 
 * libssl3 
 * openssh-client 
 * openssh-server 
 * openssh-sftp-server 
 * openssl
 * putty-tools 
 * python3-twisted
 * zlib1g 
 {{< /spoiler >}}
 
 
 - - -
 
 ### ssh
 
  This metapackage is a convenient way to install both the OpenSSH client
  and the OpenSSH server. It provides nothing in and of itself, so you
  may remove it if nothing depends on it.
 
 **Installed size:** `172 KB`  
 **How to install:** `sudo apt install ssh`  
 
 {{< spoiler "Dependencies:" >}}
 * openssh-client 
 * openssh-server 
 {{< /spoiler >}}
 
 
 - - -
 
 ### ssh-askpass-gnome
 
  This has been split out of the main openssh-client package so that
  openssh-client does not need to depend on GTK+.
   
  You probably want the ssh-askpass package instead, but this is
  provided to add to your choice and/or confusion.
 
 **Installed size:** `209 KB`  
 **How to install:** `sudo apt install ssh-askpass-gnome`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libglib2.0-0 
 * libgtk-3-0 
 * openssh-client | ssh 
 {{< /spoiler >}}
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
