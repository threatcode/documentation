---
archived: "true"
Title: fake-hwclock
Homepage: 
Repository: https://git.einval.com/cgi-bin/gitweb.cgi?p=fake-hwclock.git
Architectures: all
Version: 0.12
Metapackages: kali-linux-arm kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### fake-hwclock
 
  Some machines don't have a working realtime clock (RTC) unit, or no
  driver for the hardware that does exist. fake-hwclock is a simple set
  of scripts to save the kernel's current clock periodically (including
  at shutdown) and restore it at boot so that the system clock keeps at
  least close to realtime. This will stop some of the problems that may
  be caused by a system believing it has travelled in time back to
  1970, such as needing to perform filesystem checks at every boot.
   
  On top of this, use of NTP is still recommended to deal with the fake
  clock "drifting" while the hardware is halted or rebooting.
 
 **Installed size:** `32 KB`  
 **How to install:** `sudo apt install fake-hwclock`  
 
 ##### fake-hwclock
 
 Control fake hardware clock
 
 ```
 root@kali:~# man fake-hwclock
 FAKE-HWCLOCK(8)             System Manager's Manual            FAKE-HWCLOCK(8)
 
 NAME
        fake-hwclock - Control fake hardware clock
 
 SYNOPSIS
        fake-hwclock [ command ] [ force ]
 
 BACKGROUND
        Many  embedded  Linux  systems do not have a functional hardware clock.
        Either they simply don't have a hardware clock at all or  they  have  a
        hardware  clock  but  it is not usable (e.g. because Linux doesn't know
        how to use it or because no battery is present).
 
        This can lead to time moving backwards to  some  default  value  (often
        1970)  when the system is rebooted. Since lots of software assumes that
        time only moves forward this is a bad thing. NTP can (and should  where
        practical)  be  used  to sync with an external timeserver but it is not
        available early in the boot process and may be  unavailable  for  other
        reasons.
 
        The design expectation of fake-hwclock is that it will be run very late
        at shutdown and very early at boot. This will ensure that  fsck  has  a
        vaguely  sensible  idea  of system time at boot and won't complain that
        the last-modified time in the filesystem is not hugely in the  past  or
        future. Some users may not worry about this too use case, in which case
        it is possible to modify the init system configuration to  move  things
        earlier/later as appropriate.
 
 DESCRIPTION
        fake-hwclock  sets and queries a fake "hardware clock" which stores the
        time in a file. This program may be run by the system administrator di-
        rectly  but  is  typically run by init (to load the time on startup and
        save it on shutdown) and cron (to save the time hourly).
 
        If no command is given then fake-hwclock acts as if  the  save  command
        was used.
 
 COMMANDS
        save   Save  the time to the file. As a sanity check, fake-hwclock will
               not move the saved clock backwards to a time/date  earlier  than
               its own release date. Use "force" to over-ride this check.
 
        load   Load  the time from the file. If force is specified fake-hwclock
               will move the clock either backwards or forwards.  Otherwise  it
               will only move it forwards.
 
 FILES
        /etc/fake-hwclock.data
               The file used to store the time
 
        /etc/init.d/fake-hwclock
               The init script used to run fake-hwclock on startup and shutdown
 
        /lib/systemd/system/fake-hwclock.service
               systemd service used to run fake-hwclock on startup and shutdown
 
        /etc/default/fake-hwclock
               Settings file for the init script.
 
        /etc/cron.hourly/fake-hwclock
               Cron job used to save the time hourly
 
 ENVIRONMENT VARIABLES
        FILE   set the file used by fake-hwclock
 
 RETURN VALUES
        1 is returned for invalid commands. 0 is returned in all other cases.
 
 BUGS
        This  approach  can  only  provide a crude approximation of what a real
        hardware clock provides. Use of NTP or another method to keep the  time
        in sync is strongly advised.
 
 Debian                          1 October 2014                 FAKE-HWCLOCK(8)
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
