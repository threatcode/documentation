---
Title: screen
Homepage: https://savannah.gnu.org/projects/screen
Repository: https://salsa.debian.org/debian/screen
Architectures: any
Version: 4.9.1-1
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-802-11 kali-tools-sniffing-spoofing kali-tools-wireless 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### screen
 
  GNU Screen is a terminal multiplexer that runs several separate "screens" on
  a single physical character-based terminal. Each virtual terminal emulates a
  DEC VT100 plus several ANSI X3.64 and ISO 2022 functions. Screen sessions
  can be detached and resumed later on a different terminal.
   
  Screen also supports a whole slew of other features, including configurable
  input and output translation, serial port support, configurable logging,
  and multi-user support.
 
 **Installed size:** `1003 KB`  
 **How to install:** `sudo apt install screen`  
 
 {{< spoiler "Dependencies:" >}}
 * debianutils 
 * libc6 
 * libcrypt1 
 * libpam0g 
 * libtinfo6 
 * libutempter0 
 {{< /spoiler >}}
 
 ##### screen
 
 Screen manager with VT100/ANSI terminal emulation
 
 ```
 root@kali:~# screen -h
 Use: screen [-opts] [cmd [args]]
  or: screen -r [host.tty]
 
 Options:
 -4            Resolve hostnames only to IPv4 addresses.
 -6            Resolve hostnames only to IPv6 addresses.
 -a            Force all capabilities into each window's termcap.
 -A -[r|R]     Adapt all windows to the new display width & height.
 -c file       Read configuration file instead of '.screenrc'.
 -d (-r)       Detach the elsewhere running screen (and reattach here).
 -dmS name     Start as daemon: Screen session in detached mode.
 -D (-r)       Detach and logout remote (and reattach here).
 -D -RR        Do whatever is needed to get a screen session.
 -e xy         Change command characters.
 -f            Flow control on, -fn = off, -fa = auto.
 -h lines      Set the size of the scrollback history buffer.
 -i            Interrupt output sooner when flow control is on.
 -l            Login mode on (update /var/run/utmp), -ln = off.
 -ls [match]   or
 -list         Do nothing, just list our SockDir [on possible matches].
 -L            Turn on output logging.
 -Logfile file Set logfile name.
 -m            ignore $STY variable, do create a new screen session.
 -O            Choose optimal output rather than exact vt100 emulation.
 -p window     Preselect the named window if it exists.
 -q            Quiet startup. Exits with non-zero return code if unsuccessful.
 -Q            Commands will send the response to the stdout of the querying process.
 -r [session]  Reattach to a detached screen process.
 -R            Reattach if possible, otherwise start a new session.
 -s shell      Shell to execute rather than $SHELL.
 -S sockname   Name this session <pid>.sockname instead of <pid>.<tty>.<host>.
 -t title      Set title. (window's name).
 -T term       Use term as $TERM for windows, rather than "screen".
 -U            Tell screen to use UTF-8 encoding.
 -v            Print "Screen version 4.09.01 (GNU) 20-Aug-23".
 -wipe [match] Do nothing, just clean up SockDir [on possible matches].
 -x            Attach to a not detached screen. (Multi display mode).
 -X            Execute <cmd> as a screen command in the specified session.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
