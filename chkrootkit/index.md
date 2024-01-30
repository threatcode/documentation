---
Title: chkrootkit
Homepage: https://www.chkrootkit.org/
Repository: https://salsa.debian.org/pkg-security-team/chkrootkit
Architectures: any
Version: 0.58b-1
Metapackages: kali-linux-everything kali-linux-large kali-tools-forensics kali-tools-respond 
Icon: images/chkrootkit-logo.svg
PackagesInfo: |
 ### chkrootkit
 
  The chkrootkit security scanner searches for signs that the system is
  infected with a 'rootkit'. Rootkits are a form of malware that seek
  to exploit security flaws to grant unauthorised access to a
  computer or its services, generally for malicious purposes.
   
  chkrootkit can identify signs of over 70 different rootkits (see the
  project's website for a list).
   
  Please note that an automated tool like chkrootkit can never
  guarantee a system is uncompromised. Nor does every report always
  signify a genuine problem: human judgement and further investigation
  will always be needed to assure the security of your system.
 
 **Installed size:** `926 KB`  
 **How to install:** `sudo apt install chkrootkit`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### chklastlog
 
 Check lastlog file for deleted entries
 
 ```
 root@kali:~# man chklastlog
 CHKLASTLOG(8)               System Manager's Manual              CHKLASTLOG(8)
 
 NAME
        chklastlog - check lastlog file for deleted entries
 
 SYNOPSIS
        chklastlog looks for users whose login has been erased from the lastlog
        database.
 
 DESCRIPTION
        chklastlog reads all entries from /var/log/wtmp (a database of informa-
        tion about logins and logouts) and checks that every user found in this
        file  has an entry in /var/log/lastlog.  It lists any users with logins
        in wtmp but no lastlogin information. This may suggest the user account
        has been compromised and the attacker has tried to cover their tracks.
 
        chklastlog needs to be able to read /var/log/wtmp and  /var/log/lastlo-
        gin.   Normally these files are world-readable so no special privileges
        are required.
 
 FILES
        /var/log/wtmp
               database of logins and logouts.
 
        /var/log/lastlog
               database which contains info on the last login of each user.
 
 SEE ALSO
        wtmp(5), who(1), lastlog(8), last(1)
 
 LIMITATIONS
        wtmp may itself be incomplete because not all programmes  record  their
        activity using utmp logging. See wtmp(8).
 
        chklastlog  will  not  detect missing entries if the user has logged in
        after the lastlog entry was deleted.
 
        This program was originally designed to run on SunOS  4.x  systems.  On
        other systems the output is undefined.
 
                                  Oct 23, 2021                    CHKLASTLOG(8)
 ```
 
 - - -
 
 ##### chkrootkit
 
 Scan the system for signs of rootkits
 
 ```
 root@kali:~# chkrootkit -h
 Usage: /usr/sbin/chkrootkit [options] [test ...]
 Options:
         -h                show this help and exit
         -V                show version information and exit
         -l                show available tests and exit
         -d                debug
         -q                quiet mode
         -x                expert mode
         -e 'FILE1 FILE2'  exclude files/dirs from results. Must be followed by a space-separated list of files/dirs.
                           Read /usr/share/doc/chkrootkit/README.FALSE-POSITIVES first.
         -s REGEXP         filter results of sniffer test through 'grep -Ev REGEXP' to exclude expected
                           PACKET_SNIFFERs. Read /usr/share/doc/chkrootkit/README.FALSE-POSITIVES first.
         -r DIR            use DIR as the root directory
         -p DIR1:DIR2:DIRN path for the external commands used by chkrootkit
         -n                skip NFS mount points
         -T FSTYPE         skip mount points of the specified file system type
 ```
 
 - - -
 
 ##### chkrootkit-daily
 
 Run chkrootkit and report results
 
 ```
 root@kali:~# man chkrootkit-daily
 chkrootkit-daily(8)         System Manager's Manual        chkrootkit-daily(8)
 
 NAME
        chkrootkit-daily - Run chkrootkit and report results
 
 SYNOPSIS
        chkrootkit-daily
 
 DESCRIPTION
        chkrootkit-daily  runs  chkrootkit(8) and emails the results. It is in-
        tended to be run by the systemd(1) timer or as a cron(1) job every day.
 
 CONFIGURATION
        All options are set and documented in /etc/chkrootkit/chkrootkit.conf.
 
 AUTHOR
        chkrootkit-daily and this manual page were written by Richard Lewis for
        the Debian project. They may be used by others.
 
 SEE ALSO
        chkrootkit(8)
 
                                   2023-02-19               chkrootkit-daily(8)
 ```
 
 - - -
 
 ##### chkwtmp
 
 Check wtmp file deleted entries
 
 ```
 root@kali:~# man chkwtmp
 CHKWTMP(8)                  System Manager's Manual                 CHKWTMP(8)
 
 NAME
        chkwtmp - check wtmp file deleted entries
 
 SYNOPSIS
        chkwtmp looks for data deleted from wtmp
 
 DESCRIPTION
        chkwtmp  examines  the  file  /var/log/wtmp for entries which have been
        overwritten (containing only null-bytes). If such entries are found the
        program displays the timestamps of the entries  before  and  after  the
        deleted entry, providing an idea of when the entry was deleted.
 
        chkwtmp  needs to be able to read /var/log/wtmp.  Normally this file is
        world-readable so no special privileges are required.
 
 FILES
        /var/log/wtmp
               database of logins and logouts.
 
 SEE ALSO
        wtmp(4), who(1)
 
 LIMITATIONS
        An entry is recognized as overwritten if the time-information has  been
        overwritten with null-bytes.
 
        This  program  was  originally designed to run on SunOS 4.x systems. On
        other systems the output is undefined.
 
                                  Oct 23, 2021                       CHKWTMP(8)
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
