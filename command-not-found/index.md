---
Title: command-not-found
Homepage: 
Repository: https://gitlab.com/kalilinux/packages/command-not-found
Architectures: all
Version: 23.04.0-1+kali3
Metapackages: 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### command-not-found
 
  This package will install a handler for command_not_found that looks up
  programs not currently installed but available from the repositories.
 
 **Installed size:** `526 KB`  
 **How to install:** `sudo apt install command-not-found`  
 
 {{< spoiler "Dependencies:" >}}
 * apt-file 
 * lsb-release
 * python3
 * python3-apt
 {{< /spoiler >}}
 
 ##### command-not-found
 
 
 ```
 root@kali:~# command-not-found -h
 Usage: command-not-found [options] <command-name>
 
 Options:
   --version             show program's version number and exit
   -h, --help            show this help message and exit
   -d DATA_DIR, --data-dir=DATA_DIR
                         use this path to locate data fields
   --ignore-installed, --ignore-installed
                         ignore local binaries and display the available
                         packages
   --no-failure-msg      don't print '<command-name>: command not found'
 ```
 
 - - -
 
 ##### update-command-not-found
 
 Update the command-not-found cache
 
 ```
 root@kali:~# man update-command-not-found
 update-com...-not-found(8) Command not found helper update-com...-not-found(8)
 
 NAME
        update-command-not-found - update the command-not-found cache
 
 SYNOPSIS
        update-command-not-found [-h|--help|-n|--no-apt-file]
 
 DESCRIPTION
        update-command-not-found updates the cache (databases) for command-not-
        found  using the files in /var/cache/apt/apt-file, which are fetched by
        apt-file.
 
 OPTIONS
        -h or --help
               Print the help message
 
        -n or --no-apt-file
               Do not run apt-file update before updating the cache.
 
 AUTHOR
        command-not-found was written by Zygmunt Krynicki,  update-command-not-
        found was written by Julian Andres Klode <jak@debian.org>
 
        This  manual  page  was written by Julian Andres Klode <jak@debian.org>
        for the Debian project, but may be used by others.
 
 0.2.26-1                          2008-10-24        update-com...-not-found(8)
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
