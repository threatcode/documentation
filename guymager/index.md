---
Title: guymager
Homepage: https://guymager.sourceforge.net/
Repository: https://salsa.debian.org/pkg-security-team/guymager
Architectures: any
Version: 0.8.13-2
Metapackages: kali-linux-default kali-linux-everything kali-linux-large kali-tools-forensics kali-tools-respond 
Icon: images/guymager-logo.svg
PackagesInfo: |
 ### guymager
 
  The forensic imager contained in this package, guymager, was designed to
  support different image file formats, to be most user-friendly and to run
  really fast. It has a high speed multi-threaded engine using parallel
  compression for best performance on multi-processor and hyper-threading
  machines.
 
 **Installed size:** `1021 KB`  
 **How to install:** `sudo apt install guymager`  
 
 {{< spoiler "Dependencies:" >}}
 * hdparm
 * libc6 
 * libewf2 
 * libgcc-s1 
 * libguytools2 
 * libparted0 | libparted
 * libqt5core5a 
 * libqt5dbus5 
 * libqt5gui5  | libqt5gui5-gles 
 * libqt5widgets5 
 * libstdc++6 
 * smartmontools
 * zlib1g 
 {{< /spoiler >}}
 
 ##### guymager
 
 A forensic acquisition program
 
 ```
 root@kali:~# man guymager
 guymager(1)                 General Commands Manual                guymager(1)
 
 0.8.13-1" "guymager manual pages"
 
 NAME
        guymager - a forensic acquisition program
 
 SYNOPSIS
        guymager [log=log_file] [cfg=configuration_file] [options]
 
 DESCRIPTION
        Guymager  is a Qt-based forensic imager. It is capable of producing im-
        age files in EWF, AFF and dd format. Its main  strenghs  are  the  easy
        user  interface,  the  high  imaging speed and the extended acquisition
        info file.
 
        The internal structure is based on separate threads for  reading,  hash
        calculation  (MD5 and SHA256), writing and includes a parallelised com-
        pression engine, thus making full  usage  of  multi-processor  and  hy-
        per-threading machines.
 
        Guymager should be run with root privileges, as other users do not have
        access to physical devices normally.
 
 OPTIONS
        log=log_file
               By default, guymager uses /var/log/guymager.log as its log file.
               This option allows for specifying a different file.
 
        cfg=configuration_file
               The  default  configuration  file is /etc/guymager/guymager.cfg.
               This option allows for specifying  a  different  file.  Guymager
               creates  a template configuration file when the option -cfg=tem-
               plate.cfg is given.
 
        All other configuration options may be specified on  the  command  line
        and/or  in the configuration file. See /etc/guymager/guymager.cfg for a
        description of all possible options. In case an option is specified  in
        the  configuration file and on the command line, the command line domi-
        nates.
 
 EXIT CODES
        Guymager normally returns an exit code of 0. Exit code 1 means that
        Guymager terminated because the AutoExit function became active. All
        other exit codes are related to internal Guymager or Qt errors.
 
 EXAMPLES
        Write all log entries to ./my.log:
               guymager log=my.log
 
        Create a template configuration file
               guymager cfg=template.cfg
 
        Read the configuration from my.cfg and use 4 threads for parallelised
        compression:
               guymager cfg=my.cfg CompressionThreads=4
 
        See /etc/guymager/guymager.cfg for details  about  option  Compression-
        Threads and all other options as well.
 
 AUTHOR
        Guy Voncken (develop (at) faert.net)
 
 version 0.8.13-2                  2022-12-31                       guymager(1)
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## Screenshots

```
guymager
```

![guymager](images/guymager.png)
