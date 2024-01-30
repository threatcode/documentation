---
Title: regripper
Homepage: https://github.com/keydet89/RegRipper3.0
Repository: https://salsa.debian.org/pkg-security-team/regripper
Architectures: all
Version: 3.0~git20221205.d588019+dfsg-1
Metapackages: kali-linux-everything kali-linux-large kali-tools-forensics kali-tools-respond kali-tools-windows-resources 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### regripper
 
  Regripper's CLI tool can be used to surgically extract, translate, and
  display information (both data and metadata) from Registry-formatted
  files via plugins in the form of Perl-scripts. It allows the analyst to
  select a hive-file to parse and a plugin or a profile, which is a list
  of plugins to run against the given hive. The results go to STDOUT and
  can be redirected to a file, that the analyst designates.
 
 **Installed size:** `1.05 MB`  
 **How to install:** `sudo apt install regripper`  
 
 {{< spoiler "Dependencies:" >}}
 * libparse-win32registry-perl
 * perl
 {{< /spoiler >}}
 
 ##### regripper
 
 Forensic analysis of Registry hives
 
 ```
 root@kali:~# regripper -h
 Rip v.3.0 - CLI RegRipper tool	
 Rip [-r Reg hive file] [-f profile] [-p plugin] [options]
 Parse Windows Registry files, using either a single module, or a profile.
 
 NOTE: This tool does NOT automatically process Registry transaction logs! The tool 
 does check to see if the hive is dirty, but does not automatically process the
 transaction logs.  If you need to incorporate transaction logs, please consider 
 using yarp + registryFlush.py, or rla.exe from Eric Zimmerman.
 
   -r [hive] .........Registry hive file to parse
   -d ................Check to see if the hive is dirty 
   -g ................Guess the hive file type 
   -a ................Automatically run hive-specific plugins 
   -aT ...............Automatically run hive-specific TLN plugins 
   -f [profile].......use the profile 
   -p [plugin]........use the plugin
   -l ................list all plugins
   -c ................Output plugin list in CSV format (use with -l)
   -s systemname......system name (TLN support)
   -u username........User name (TLN support)
   -uP ...............Update default profiles
   -h.................Help (print this information)
   
 Ex: C:\>rip -r c:\case\system -f system
     C:\>rip -r c:\case\ntuser.dat -p userassist
     C:\>rip -r c:\case\ntuser.dat -a
     C:\>rip -l -c
 
 All output goes to STDOUT; use redirection (ie, > or >>) to output to a file.
   
 copyright 2020 Quantum Analytics Research, LLC
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## Screenshots

```
regripper
```

![regripper](images/regripper.png)
