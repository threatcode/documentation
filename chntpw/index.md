---
Title: chntpw
Homepage: http://pogostick.net/~pnh/ntpasswd/
Repository: https://salsa.debian.org/debian/chntpw
Architectures: any
Version: 140201-1
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-passwords 
Icon: images/chntpw-logo.svg
PackagesInfo: |
 ### chntpw
 
  This little program provides a way to view information and
  change user passwords in a Windows NT/2000 user database file.
  Old passwords need not be known since they are overwritten.
  In addition it also contains a simple registry editor
  (same size data writes) and an hex-editor which enables you to
  fiddle around with bits and bytes in the file as you wish.
   
  If you want GNU/Linux bootdisks for offline password recovery
  you can add this utility to custom image disks or use those provided
  at the tools homepage.
 
 **Installed size:** `486 KB`  
 **How to install:** `sudo apt install chntpw`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### chntpw
 
 Utility to overwrite passwords of Windows systems
 
 ```
 root@kali:~# chntpw -h
 chntpw: change password of a user in a Windows SAM file,
 or invoke registry editor. Should handle both 32 and 64 bit windows and
 all version from NT3.x to Win8.1
 chntpw [OPTIONS] <samfile> [systemfile] [securityfile] [otherreghive] [...]
  -h          This message
  -u <user>   Username or RID (0x3e9 for example) to interactively edit
  -l          list all users in SAM file and exit
  -i          Interactive Menu system
  -e          Registry editor. Now with full write support!
  -d          Enter buffer debugger instead (hex editor), 
  -v          Be a little more verbose (for debuging)
  -L          For scripts, write names of changed files to /tmp/changed
  -N          No allocation mode. Only same length overwrites possible (very safe mode)
  -E          No expand mode, do not expand hive file (safe mode)
 
 Usernames can be given as name or RID (in hex with 0x first)
 
 See readme file on how to get to the registry files, and what they are.
 Source/binary freely distributable under GPL v2 license. See README for details.
 NOTE: This program is somewhat hackish! You are on your own!
 ```
 
 - - -
 
 ##### reged
 
 Utility to export/import and edit a Windows registry hives
 
 ```
 root@kali:~# reged -h
 reged version 0.1 140201, (c) Petter N Hagen
 
 Modes:
 -x <registryhivefile> <prefixstring> <key> <output.reg>
    Xport. Where <prefixstring> for example is HKEY_LOCAL_MACHINE\SOFTWARE
    <key> is key to dump (recursively), \ or \\ means all keys in hive
    Only one .reg and one hive file supported at the same time
 -I <registryhivefile> <prefixstring> <input.reg>
    Import from .reg file. Where <prefixstring> for example is HKEY_LOCAL_MACHINE\SOFTWARE
    Only one .reg and one hive file supported at the same time
 -e <registryhive> ...
    Interactive edit one or more of registry files
 
 Options:
 -L : Log changed filenames to /tmp/changed, also auto-saves
 -C : Auto-save (commit) changed hives without asking
 -N : No allocate mode, only allow edit of existing values with same size
 -E : No expand mode, do not expand hive file (safe mode)
 -t : Debug trace of allocated blocks
 -v : Some more verbose messages
 ```
 
 - - -
 
 ##### sampasswd
 
 Reset passwords of users in the SAM user database
 
 ```
 root@kali:~# sampasswd -h
 sampasswd version 0.2 140201, (c) Petter N Hagen
 sampasswd  [-r|-l] [-H] -u <user> <samhive>
 Reset password or list users in SAM database
 Mode:
    -r = reset users password
    -l = list users in sam
 Parameters:
    <user> can be given as a username or a RID in hex with 0x in front
    Example:
    -r -u theboss -> resets password of user named 'theboss' if found
    -r -u 0x3ea -> resets password for user with RID 0x3ea (hex)
    -r -a -> Reset password of all users in administrators group (0x220)
    -r -f -> Reset password of admin user with lowest RID
             not counting built-in admin (0x1f4) unless it is the only admin
    Usernames with international characters usually fails to be found,
    please use RID number instead
    If success, there will be no output, and exit code is 0
 Options:
    -H : For list: Human readable listing (default is parsable table)
    -H : For reset: Will output confirmation message if success
    -N : No allocate mode, only allow edit of existing values with same size
    -E : No expand mode, do not expand hive file (safe mode)
    -t : Debug trace of allocated blocks
    -v : Some more verbose messages/debug
 ```
 
 - - -
 
 ##### samunlock
 
 Unlock users in the SAM user database
 
 ```
 root@kali:~# samunlock -h
 samunlock version 0.1 141018, (c) Adrian Gibanel
 samunlock  [-U|-l] [-H] -u <user> <samhive>
 Unlock user or list users in SAM database
 Mode:
    -U = Unlock user
    -l = list users in sam
 Parameters:
    <user> can be given as a username or a RID in hex with 0x in front
    Example:
    -U -u theboss -> Unlocks user named 'theboss' if found
    -U -u 0x3ea -> Unlocks user with RID 0x3ea (hex)
    -U -f -> Unlocks admin user with lowest RID
             not counting built-in admin (0x1f4) unless it is the only admin
    Usernames with international characters usually fails to be found,
    please use RID number instead
    If success, there will be no output, and exit code is 0
 Options:
    -H : For list: Human readable listing (default is parsable table)
    -H : For unlock: Will output confirmation message if success
    -N : No allocate mode, only allow edit of existing values with same size
    -E : No expand mode, do not expand hive file (safe mode)
    -t : Debug trace of allocated blocks
    -v : Some more verbose messages/debug
 ```
 
 - - -
 
 ##### samusrgrp
 
 Add or remove users from groups in SAM database files
 
 ```
 root@kali:~# samusrgrp -h
 samusrgrp version 0.2 140201, (c) Petter N Hagen
 samusrgrp  [-a|-r] -u <user> -g <groupid> <samhive>
 Add or remove a (local) user to/from a group
 Mode:   -a = add user to group
    -r = remove user from group
    -l = list groups
    -L = list groups and also their members
    -s = Print machine SID
 Parameters:
    <user> can be given as a username or a RID in hex with 0x in front
    <group> is the group number, in hex with 0x in front
    Example:
    -a -u theboss -g 0x220 -> add user named 'theboss' group hex 220 (administrators)
    -a -u 0x3ea -g 0x221 -> add user with RID (hex) 3ea group hex 221 (users)
    -r -u 0x3ff -g 0x220 -> remove user RID 0x3ff from grp 0x220
    Usernames with international characters usually fails to be found,
    please use RID number instead
    If success, there will be no output, and exit code is 0
    Also, success if user already in (or not in if -r) the group
 Options:
    -H : Human readable output, else parsable
    -N : No allocate mode, only allow edit of existing values with same size
    -E : No expand mode, do not expand hive file (safe mode)
    -t : Debug trace of allocated blocks
    -v : Some more verbose messages/debug
 Multi call binary, if program is named:
   samusrtogrp -- Assume -a mode: Add a user into a group
   samusrfromgrp -- Assume -r mode: Remove user from a group
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
