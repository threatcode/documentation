---
Title: sudo
Homepage: https://www.sudo.ws/
Repository: https://salsa.debian.org/sudo-team/sudo
Architectures: any all
Version: 1.9.14p2-1
Metapackages: kali-linux-core kali-linux-default kali-linux-everything kali-linux-headless kali-linux-labs kali-linux-large kali-linux-nethunter kali-linux-wsl kali-tools-identify kali-tools-post-exploitation kali-tools-reporting kali-tools-social-engineering kali-tools-vulnerability 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### libnss-sudo
 
  This empty package provides the basic configuration needed to enable the
  `sudoers` NSS service.
 
 **Installed size:** `687 KB`  
 **How to install:** `sudo apt install libnss-sudo`  
 
 
 - - -
 
 ### sudo
 
  Sudo is a program designed to allow a sysadmin to give limited root
  privileges to users and log root activity.  The basic philosophy is to give
  as few privileges as possible but still allow people to get their work done.
   
  This version is built with minimal shared library dependencies, use the
  sudo-ldap package instead if you need LDAP support for sudoers.
 
 **Installed size:** `6.07 MB`  
 **How to install:** `sudo apt install sudo`  
 
 {{< spoiler "Dependencies:" >}}
 * init-system-helpers 
 * libaudit1 
 * libc6 
 * libpam-modules
 * libpam0g 
 * libselinux1 
 * zlib1g 
 {{< /spoiler >}}
 
 ##### cvtsudoers
 
 Convert between sudoers file formats
 
 ```
 root@kali:~# cvtsudoers -h
 cvtsudoers - convert between sudoers file formats
 
 usage: cvtsudoers [-ehMpV] [-b dn] [-c conf_file ] [-d deftypes] [-f output_format] [-i input_format] [-I increment] [-m filter] [-o output_file] [-O start_point] [-P padding] [-s sections] [input_file]
 
 Options:
   -b, --base=dn              the base DN for sudo LDAP queries
   -c, --config=conf_file     the path to the configuration file
   -d, --defaults=deftypes    only convert Defaults of the specified types
   -e, --expand-aliases       expand aliases when converting
   -f, --output-format=format set output format: JSON, LDIF or sudoers
   -i, --input-format=format  set input format: LDIF or sudoers
   -I, --increment=num        amount to increase each sudoOrder by
   -h, --help                 display help message and exit
   -m, --match=filter         only convert entries that match the filter
   -M, --match-local          match filter uses passwd and group databases
   -o, --output=output_file   write converted sudoers to output_file
   -O, --order-start=num      starting point for first sudoOrder
   -p, --prune-matches        prune non-matching users, groups and hosts
   -P, --padding=num          base padding for sudoOrder increment
   -s, --suppress=sections    suppress output of certain sections
   -V, --version              display version information and exit
 ```
 
 - - -
 
 ##### cvtsudoers
 
 Convert between sudoers file formats
 
 ```
 root@kali:~# cvtsudoers -h
 cvtsudoers - convert between sudoers file formats
 
 usage: cvtsudoers [-ehMpV] [-b dn] [-c conf_file ] [-d deftypes] [-f output_format] [-i input_format] [-I increment] [-m filter] [-o output_file] [-O start_point] [-P padding] [-s sections] [input_file]
 
 Options:
   -b, --base=dn              the base DN for sudo LDAP queries
   -c, --config=conf_file     the path to the configuration file
   -d, --defaults=deftypes    only convert Defaults of the specified types
   -e, --expand-aliases       expand aliases when converting
   -f, --output-format=format set output format: JSON, LDIF or sudoers
   -i, --input-format=format  set input format: LDIF or sudoers
   -I, --increment=num        amount to increase each sudoOrder by
   -h, --help                 display help message and exit
   -m, --match=filter         only convert entries that match the filter
   -M, --match-local          match filter uses passwd and group databases
   -o, --output=output_file   write converted sudoers to output_file
   -O, --order-start=num      starting point for first sudoOrder
   -p, --prune-matches        prune non-matching users, groups and hosts
   -P, --padding=num          base padding for sudoOrder increment
   -s, --suppress=sections    suppress output of certain sections
   -V, --version              display version information and exit
 ```
 
 - - -
 
 ##### sudo
 
 Execute a command as another user
 
 ```
 root@kali:~# sudo -h
 sudo - execute a command as another user
 
 usage: sudo -h | -K | -k | -V
 usage: sudo -v [-ABkNnS] [-g group] [-h host] [-p prompt] [-u user]
 usage: sudo -l [-ABkNnS] [-g group] [-h host] [-p prompt] [-U user]
             [-u user] [command [arg ...]]
 usage: sudo [-ABbEHkNnPS] [-r role] [-t type] [-C num] [-D directory]
             [-g group] [-h host] [-p prompt] [-R directory] [-T timeout]
             [-u user] [VAR=value] [-i | -s] [command [arg ...]]
 usage: sudo -e [-ABkNnS] [-r role] [-t type] [-C num] [-D directory]
             [-g group] [-h host] [-p prompt] [-R directory] [-T timeout]
             [-u user] file ...
 
 Options:
   -A, --askpass                 use a helper program for password prompting
   -b, --background              run command in the background
   -B, --bell                    ring bell when prompting
   -C, --close-from=num          close all file descriptors >= num
   -D, --chdir=directory         change the working directory before running
                                 command
   -E, --preserve-env            preserve user environment when running command
       --preserve-env=list       preserve specific environment variables
   -e, --edit                    edit files instead of running a command
   -g, --group=group             run command as the specified group name or ID
   -H, --set-home                set HOME variable to target user's home dir
   -h, --help                    display help message and exit
   -h, --host=host               run command on host (if supported by plugin)
   -i, --login                   run login shell as the target user; a command
                                 may also be specified
   -K, --remove-timestamp        remove timestamp file completely
   -k, --reset-timestamp         invalidate timestamp file
   -l, --list                    list user's privileges or check a specific
                                 command; use twice for longer format
   -n, --non-interactive         non-interactive mode, no prompts are used
   -P, --preserve-groups         preserve group vector instead of setting to
                                 target's
   -p, --prompt=prompt           use the specified password prompt
   -R, --chroot=directory        change the root directory before running command
   -r, --role=role               create SELinux security context with specified
                                 role
   -S, --stdin                   read password from standard input
   -s, --shell                   run shell as the target user; a command may
                                 also be specified
   -t, --type=type               create SELinux security context with specified
                                 type
   -T, --command-timeout=timeout terminate command after the specified time limit
   -U, --other-user=user         in list mode, display privileges for user
   -u, --user=user               run command (or edit file) as specified user
                                 name or ID
   -V, --version                 display version information and exit
   -v, --validate                update user's timestamp without running a
                                 command
   --                            stop processing command line arguments
 ```
 
 - - -
 
 ##### sudo
 
 Execute a command as another user
 
 ```
 root@kali:~# sudo -h
 sudo - execute a command as another user
 
 usage: sudo -h | -K | -k | -V
 usage: sudo -v [-ABkNnS] [-g group] [-h host] [-p prompt] [-u user]
 usage: sudo -l [-ABkNnS] [-g group] [-h host] [-p prompt] [-U user]
             [-u user] [command [arg ...]]
 usage: sudo [-ABbEHkNnPS] [-r role] [-t type] [-C num] [-D directory]
             [-g group] [-h host] [-p prompt] [-R directory] [-T timeout]
             [-u user] [VAR=value] [-i | -s] [command [arg ...]]
 usage: sudo -e [-ABkNnS] [-r role] [-t type] [-C num] [-D directory]
             [-g group] [-h host] [-p prompt] [-R directory] [-T timeout]
             [-u user] file ...
 
 Options:
   -A, --askpass                 use a helper program for password prompting
   -b, --background              run command in the background
   -B, --bell                    ring bell when prompting
   -C, --close-from=num          close all file descriptors >= num
   -D, --chdir=directory         change the working directory before running
                                 command
   -E, --preserve-env            preserve user environment when running command
       --preserve-env=list       preserve specific environment variables
   -e, --edit                    edit files instead of running a command
   -g, --group=group             run command as the specified group name or ID
   -H, --set-home                set HOME variable to target user's home dir
   -h, --help                    display help message and exit
   -h, --host=host               run command on host (if supported by plugin)
   -i, --login                   run login shell as the target user; a command
                                 may also be specified
   -K, --remove-timestamp        remove timestamp file completely
   -k, --reset-timestamp         invalidate timestamp file
   -l, --list                    list user's privileges or check a specific
                                 command; use twice for longer format
   -n, --non-interactive         non-interactive mode, no prompts are used
   -P, --preserve-groups         preserve group vector instead of setting to
                                 target's
   -p, --prompt=prompt           use the specified password prompt
   -R, --chroot=directory        change the root directory before running command
   -r, --role=role               create SELinux security context with specified
                                 role
   -S, --stdin                   read password from standard input
   -s, --shell                   run shell as the target user; a command may
                                 also be specified
   -t, --type=type               create SELinux security context with specified
                                 type
   -T, --command-timeout=timeout terminate command after the specified time limit
   -U, --other-user=user         in list mode, display privileges for user
   -u, --user=user               run command (or edit file) as specified user
                                 name or ID
   -V, --version                 display version information and exit
   -v, --validate                update user's timestamp without running a
                                 command
   --                            stop processing command line arguments
 ```
 
 - - -
 
 ##### sudo_logsrvd
 
 Sudo event and I/O log server
 
 ```
 root@kali:~# sudo_logsrvd -h
 sudo_logsrvd - sudo log server
 
 
 Options:
   -f, --file            path to configuration file
   -h, --help            display help message and exit
   -n, --no-fork         do not fork, run in the foreground
   -R, --random-drop     percent chance connections will drop
   -V, --version         display version information and exit
 
 ```
 
 - - -
 
 ##### sudo_logsrvd
 
 Sudo event and I/O log server
 
 ```
 root@kali:~# sudo_logsrvd -h
 sudo_logsrvd - sudo log server
 
 
 Options:
   -f, --file            path to configuration file
   -h, --help            display help message and exit
   -n, --no-fork         do not fork, run in the foreground
   -R, --random-drop     percent chance connections will drop
   -V, --version         display version information and exit
 
 ```
 
 - - -
 
 ##### sudo_sendlog
 
 Send sudo I/O log to log server
 
 ```
 root@kali:~# sudo_sendlog --help
 sudo_sendlog - send sudo I/O log to remote server
 
 
 Options:
       --help            display help message and exit
   -A, --accept          only send an accept event (no I/O)
   -h, --host            host to send logs to
   -i, --iolog_id        remote ID of I/O log to be resumed
   -p, --port            port to use when connecting to host
   -r, --restart         restart previous I/O log transfer
   -R, --reject          reject the command with the given reason
   -s, --stop-after        stop transfer after reaching this time
   -t, --test            test audit server by sending selected I/O log n times in parallel
   -V, --version         display version information and exit
 
 ```
 
 - - -
 
 ##### sudo_sendlog
 
 Send sudo I/O log to log server
 
 ```
 root@kali:~# sudo_sendlog --help
 sudo_sendlog - send sudo I/O log to remote server
 
 
 Options:
       --help            display help message and exit
   -A, --accept          only send an accept event (no I/O)
   -h, --host            host to send logs to
   -i, --iolog_id        remote ID of I/O log to be resumed
   -p, --port            port to use when connecting to host
   -r, --restart         restart previous I/O log transfer
   -R, --reject          reject the command with the given reason
   -s, --stop-after        stop transfer after reaching this time
   -t, --test            test audit server by sending selected I/O log n times in parallel
   -V, --version         display version information and exit
 
 ```
 
 - - -
 
 ##### sudoedit
 
 Execute a command as another user
 
 ```
 root@kali:~# sudoedit -h
 sudoedit - edit files as another user
 
 usage: sudoedit -h | -V
 usage: sudoedit [-ABkNnS] [-r role] [-t type] [-C num] [-D directory]
                 [-g group] [-h host] [-p prompt] [-R directory] [-T timeout]
                 [-u user] file ...
 
 Options:
   -A, --askpass                 use a helper program for password prompting
   -B, --bell                    ring bell when prompting
   -C, --close-from=num          close all file descriptors >= num
   -D, --chdir=directory         change the working directory before running
                                 command
   -g, --group=group             run command as the specified group name or ID
   -h, --help                    display help message and exit
   -h, --host=host               run command on host (if supported by plugin)
   -k, --reset-timestamp         invalidate timestamp file
   -n, --non-interactive         non-interactive mode, no prompts are used
   -p, --prompt=prompt           use the specified password prompt
   -R, --chroot=directory        change the root directory before running command
   -r, --role=role               create SELinux security context with specified
                                 role
   -S, --stdin                   read password from standard input
   -t, --type=type               create SELinux security context with specified
                                 type
   -T, --command-timeout=timeout terminate command after the specified time limit
   -u, --user=user               run command (or edit file) as specified user
                                 name or ID
   -V, --version                 display version information and exit
   --                            stop processing command line arguments
 ```
 
 - - -
 
 ##### sudoedit
 
 Execute a command as another user
 
 ```
 root@kali:~# sudoedit -h
 sudoedit - edit files as another user
 
 usage: sudoedit -h | -V
 usage: sudoedit [-ABkNnS] [-r role] [-t type] [-C num] [-D directory]
                 [-g group] [-h host] [-p prompt] [-R directory] [-T timeout]
                 [-u user] file ...
 
 Options:
   -A, --askpass                 use a helper program for password prompting
   -B, --bell                    ring bell when prompting
   -C, --close-from=num          close all file descriptors >= num
   -D, --chdir=directory         change the working directory before running
                                 command
   -g, --group=group             run command as the specified group name or ID
   -h, --help                    display help message and exit
   -h, --host=host               run command on host (if supported by plugin)
   -k, --reset-timestamp         invalidate timestamp file
   -n, --non-interactive         non-interactive mode, no prompts are used
   -p, --prompt=prompt           use the specified password prompt
   -R, --chroot=directory        change the root directory before running command
   -r, --role=role               create SELinux security context with specified
                                 role
   -S, --stdin                   read password from standard input
   -t, --type=type               create SELinux security context with specified
                                 type
   -T, --command-timeout=timeout terminate command after the specified time limit
   -u, --user=user               run command (or edit file) as specified user
                                 name or ID
   -V, --version                 display version information and exit
   --                            stop processing command line arguments
 ```
 
 - - -
 
 ##### sudoreplay
 
 Replay sudo session logs
 
 ```
 root@kali:~# sudoreplay -h
 sudoreplay - replay sudo session logs
 
 usage: sudoreplay [-hnRS] [-d dir] [-m num] [-s num] ID
 usage: sudoreplay [-h] [-d dir] -l [search expression]
 
 Options:
   -d, --directory=dir    specify directory for session logs
   -f, --filter=filter    specify which I/O type(s) to display
   -h, --help             display help message and exit
   -l, --list             list available session IDs, with optional expression
   -m, --max-wait=num     max number of seconds to wait between events
   -n, --non-interactive  no prompts, session is sent to the standard output
   -R, --no-resize        do not attempt to re-size the terminal
   -S, --suspend-wait     wait while the command was suspended
   -s, --speed=num        speed up or slow down output
   -V, --version          display version information and exit
 ```
 
 - - -
 
 ##### sudoreplay
 
 Replay sudo session logs
 
 ```
 root@kali:~# sudoreplay -h
 sudoreplay - replay sudo session logs
 
 usage: sudoreplay [-hnRS] [-d dir] [-m num] [-s num] ID
 usage: sudoreplay [-h] [-d dir] -l [search expression]
 
 Options:
   -d, --directory=dir    specify directory for session logs
   -f, --filter=filter    specify which I/O type(s) to display
   -h, --help             display help message and exit
   -l, --list             list available session IDs, with optional expression
   -m, --max-wait=num     max number of seconds to wait between events
   -n, --non-interactive  no prompts, session is sent to the standard output
   -R, --no-resize        do not attempt to re-size the terminal
   -S, --suspend-wait     wait while the command was suspended
   -s, --speed=num        speed up or slow down output
   -V, --version          display version information and exit
 ```
 
 - - -
 
 ##### visudo
 
 Edit the sudoers file
 
 ```
 root@kali:~# visudo -h
 visudo - safely edit the sudoers file
 
 usage: visudo [-chqsV] [[-f] sudoers ]
 
 Options:
   -c, --check              check-only mode
   -f, --file=sudoers       specify sudoers file location
   -h, --help               display help message and exit
   -I, --no-includes        do not edit include files
   -q, --quiet              less verbose (quiet) syntax error messages
   -s, --strict             strict syntax checking
   -V, --version            display version information and exit
 
 ```
 
 - - -
 
 ##### visudo
 
 Edit the sudoers file
 
 ```
 root@kali:~# visudo -h
 visudo - safely edit the sudoers file
 
 usage: visudo [-chqsV] [[-f] sudoers ]
 
 Options:
   -c, --check              check-only mode
   -f, --file=sudoers       specify sudoers file location
   -h, --help               display help message and exit
   -I, --no-includes        do not edit include files
   -q, --quiet              less verbose (quiet) syntax error messages
   -s, --strict             strict syntax checking
   -V, --version            display version information and exit
 
 ```
 
 - - -
 
 ### sudo-ldap
 
  Sudo is a program designed to allow a sysadmin to give limited root
  privileges to users and log root activity.  The basic philosophy is to give
  as few privileges as possible but still allow people to get their work done.
   
  This version is built with LDAP support, which allows an equivalent of the
  sudoers database to be distributed via LDAP.  Authentication is still
  performed via pam.
 
 **Installed size:** `6.15 MB`  
 **How to install:** `sudo apt install sudo-ldap`  
 
 {{< spoiler "Dependencies:" >}}
 * init-system-helpers 
 * libaudit1 
 * libc6 
 * libldap-2.5-0 
 * libnss-sudo
 * libpam-modules
 * libpam0g 
 * libselinux1 
 * zlib1g 
 {{< /spoiler >}}
 
 ##### cvtsudoers
 
 Convert between sudoers file formats
 
 ```
 root@kali:~# cvtsudoers -h
 cvtsudoers - convert between sudoers file formats
 
 usage: cvtsudoers [-ehMpV] [-b dn] [-c conf_file ] [-d deftypes] [-f output_format] [-i input_format] [-I increment] [-m filter] [-o output_file] [-O start_point] [-P padding] [-s sections] [input_file]
 
 Options:
   -b, --base=dn              the base DN for sudo LDAP queries
   -c, --config=conf_file     the path to the configuration file
   -d, --defaults=deftypes    only convert Defaults of the specified types
   -e, --expand-aliases       expand aliases when converting
   -f, --output-format=format set output format: JSON, LDIF or sudoers
   -i, --input-format=format  set input format: LDIF or sudoers
   -I, --increment=num        amount to increase each sudoOrder by
   -h, --help                 display help message and exit
   -m, --match=filter         only convert entries that match the filter
   -M, --match-local          match filter uses passwd and group databases
   -o, --output=output_file   write converted sudoers to output_file
   -O, --order-start=num      starting point for first sudoOrder
   -p, --prune-matches        prune non-matching users, groups and hosts
   -P, --padding=num          base padding for sudoOrder increment
   -s, --suppress=sections    suppress output of certain sections
   -V, --version              display version information and exit
 ```
 
 - - -
 
 ##### sudo
 
 Execute a command as another user
 
 ```
 root@kali:~# sudo -h
 sudo - execute a command as another user
 
 usage: sudo -h | -K | -k | -V
 usage: sudo -v [-ABkNnS] [-g group] [-h host] [-p prompt] [-u user]
 usage: sudo -l [-ABkNnS] [-g group] [-h host] [-p prompt] [-U user]
             [-u user] [command [arg ...]]
 usage: sudo [-ABbEHkNnPS] [-r role] [-t type] [-C num] [-D directory]
             [-g group] [-h host] [-p prompt] [-R directory] [-T timeout]
             [-u user] [VAR=value] [-i | -s] [command [arg ...]]
 usage: sudo -e [-ABkNnS] [-r role] [-t type] [-C num] [-D directory]
             [-g group] [-h host] [-p prompt] [-R directory] [-T timeout]
             [-u user] file ...
 
 Options:
   -A, --askpass                 use a helper program for password prompting
   -b, --background              run command in the background
   -B, --bell                    ring bell when prompting
   -C, --close-from=num          close all file descriptors >= num
   -D, --chdir=directory         change the working directory before running
                                 command
   -E, --preserve-env            preserve user environment when running command
       --preserve-env=list       preserve specific environment variables
   -e, --edit                    edit files instead of running a command
   -g, --group=group             run command as the specified group name or ID
   -H, --set-home                set HOME variable to target user's home dir
   -h, --help                    display help message and exit
   -h, --host=host               run command on host (if supported by plugin)
   -i, --login                   run login shell as the target user; a command
                                 may also be specified
   -K, --remove-timestamp        remove timestamp file completely
   -k, --reset-timestamp         invalidate timestamp file
   -l, --list                    list user's privileges or check a specific
                                 command; use twice for longer format
   -n, --non-interactive         non-interactive mode, no prompts are used
   -P, --preserve-groups         preserve group vector instead of setting to
                                 target's
   -p, --prompt=prompt           use the specified password prompt
   -R, --chroot=directory        change the root directory before running command
   -r, --role=role               create SELinux security context with specified
                                 role
   -S, --stdin                   read password from standard input
   -s, --shell                   run shell as the target user; a command may
                                 also be specified
   -t, --type=type               create SELinux security context with specified
                                 type
   -T, --command-timeout=timeout terminate command after the specified time limit
   -U, --other-user=user         in list mode, display privileges for user
   -u, --user=user               run command (or edit file) as specified user
                                 name or ID
   -V, --version                 display version information and exit
   -v, --validate                update user's timestamp without running a
                                 command
   --                            stop processing command line arguments
 ```
 
 - - -
 
 ##### sudo_logsrvd
 
 Sudo event and I/O log server
 
 ```
 root@kali:~# sudo_logsrvd -h
 sudo_logsrvd - sudo log server
 
 
 Options:
   -f, --file            path to configuration file
   -h, --help            display help message and exit
   -n, --no-fork         do not fork, run in the foreground
   -R, --random-drop     percent chance connections will drop
   -V, --version         display version information and exit
 
 ```
 
 - - -
 
 ##### sudo_sendlog
 
 Send sudo I/O log to log server
 
 ```
 root@kali:~# sudo_sendlog --help
 sudo_sendlog - send sudo I/O log to remote server
 
 
 Options:
       --help            display help message and exit
   -A, --accept          only send an accept event (no I/O)
   -h, --host            host to send logs to
   -i, --iolog_id        remote ID of I/O log to be resumed
   -p, --port            port to use when connecting to host
   -r, --restart         restart previous I/O log transfer
   -R, --reject          reject the command with the given reason
   -s, --stop-after        stop transfer after reaching this time
   -t, --test            test audit server by sending selected I/O log n times in parallel
   -V, --version         display version information and exit
 
 ```
 
 - - -
 
 ##### sudoedit
 
 Execute a command as another user
 
 ```
 root@kali:~# sudoedit -h
 sudoedit - edit files as another user
 
 usage: sudoedit -h | -V
 usage: sudoedit [-ABkNnS] [-r role] [-t type] [-C num] [-D directory]
                 [-g group] [-h host] [-p prompt] [-R directory] [-T timeout]
                 [-u user] file ...
 
 Options:
   -A, --askpass                 use a helper program for password prompting
   -B, --bell                    ring bell when prompting
   -C, --close-from=num          close all file descriptors >= num
   -D, --chdir=directory         change the working directory before running
                                 command
   -g, --group=group             run command as the specified group name or ID
   -h, --help                    display help message and exit
   -h, --host=host               run command on host (if supported by plugin)
   -k, --reset-timestamp         invalidate timestamp file
   -n, --non-interactive         non-interactive mode, no prompts are used
   -p, --prompt=prompt           use the specified password prompt
   -R, --chroot=directory        change the root directory before running command
   -r, --role=role               create SELinux security context with specified
                                 role
   -S, --stdin                   read password from standard input
   -t, --type=type               create SELinux security context with specified
                                 type
   -T, --command-timeout=timeout terminate command after the specified time limit
   -u, --user=user               run command (or edit file) as specified user
                                 name or ID
   -V, --version                 display version information and exit
   --                            stop processing command line arguments
 ```
 
 - - -
 
 ##### sudoreplay
 
 Replay sudo session logs
 
 ```
 root@kali:~# sudoreplay -h
 sudoreplay - replay sudo session logs
 
 usage: sudoreplay [-hnRS] [-d dir] [-m num] [-s num] ID
 usage: sudoreplay [-h] [-d dir] -l [search expression]
 
 Options:
   -d, --directory=dir    specify directory for session logs
   -f, --filter=filter    specify which I/O type(s) to display
   -h, --help             display help message and exit
   -l, --list             list available session IDs, with optional expression
   -m, --max-wait=num     max number of seconds to wait between events
   -n, --non-interactive  no prompts, session is sent to the standard output
   -R, --no-resize        do not attempt to re-size the terminal
   -S, --suspend-wait     wait while the command was suspended
   -s, --speed=num        speed up or slow down output
   -V, --version          display version information and exit
 ```
 
 - - -
 
 ##### visudo
 
 Edit the sudoers file
 
 ```
 root@kali:~# visudo -h
 visudo - safely edit the sudoers file
 
 usage: visudo [-chqsV] [[-f] sudoers ]
 
 Options:
   -c, --check              check-only mode
   -f, --file=sudoers       specify sudoers file location
   -h, --help               display help message and exit
   -I, --no-includes        do not edit include files
   -q, --quiet              less verbose (quiet) syntax error messages
   -s, --strict             strict syntax checking
   -V, --version            display version information and exit
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
