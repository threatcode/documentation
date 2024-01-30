---
Title: mc
Homepage: https://www.midnight-commander.org
Repository: https://salsa.debian.org/debian/mc
Architectures: any all
Version: 3:4.8.29-2
Metapackages: kali-linux-everything kali-linux-large 
Icon: images/mc-logo.svg
PackagesInfo: |
 ### mc
 
  GNU Midnight Commander is a text-mode full-screen file manager. It
  uses a two panel interface and a subshell for command execution. It
  includes an internal editor with syntax highlighting and an internal
  viewer with support for binary files. Also included is Virtual
  Filesystem (VFS), that allows files on remote systems (e.g. FTP, SSH
  servers) and files inside archives to be manipulated like real files.
 
 **Installed size:** `1.45 MB`  
 **How to install:** `sudo apt install mc`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libext2fs2 
 * libglib2.0-0 
 * libgpm2 
 * libslang2 
 * libssh2-1 
 * mc-data 
 {{< /spoiler >}}
 
 ##### mc
 
 Visual shell for Unix-like systems.
 
 ```
 root@kali:~# mc -h
 Usage:
   mc [OPTION?] [this_dir] [other_panel_dir]
 
 
 GNU Midnight Commander 4.8.29
 
 
 Help Options:
   -h, --help                Show help options
   --help-all                Show all help options
   --help-terminal           Terminal options
   --help-color              Color options
 
 Application Options:
   -V, --version             Displays the current version
   -f, --datadir             Print data directory
   -F, --datadir-info        Print extended info about used data directories
   --configure-options       Print configure options
   -P, --printwd=<file>      Print last working directory to specified file
   -U, --subshell            Enables subshell support (default)
   -u, --nosubshell          Disables subshell support
   -l, --ftplog=<file>       Log ftp dialog to specified file
   -v, --view=<file>         Launches the file viewer on a file
   -e, --edit=<file> ...     Edit files
 
 
 Please send any bug reports (including the output of 'mc -V')
 as tickets at www.midnight-commander.org
 
 ```
 
 - - -
 
 ##### mcdiff
 
 Visual shell for Unix-like systems.
 
 ```
 root@kali:~# mcdiff -h
 Usage:
   mcdiff [OPTION?] file1 file2
 
 
 GNU Midnight Commander 4.8.29
 
 
 Help Options:
   -h, --help                Show help options
   --help-all                Show all help options
   --help-terminal           Terminal options
   --help-color              Color options
 
 Application Options:
   -V, --version             Displays the current version
   -f, --datadir             Print data directory
   -F, --datadir-info        Print extended info about used data directories
   --configure-options       Print configure options
   -P, --printwd=<file>      Print last working directory to specified file
   -U, --subshell            Enables subshell support (default)
   -u, --nosubshell          Disables subshell support
   -l, --ftplog=<file>       Log ftp dialog to specified file
   -v, --view=<file>         Launches the file viewer on a file
   -e, --edit=<file> ...     Edit files
 
 
 Please send any bug reports (including the output of 'mc -V')
 as tickets at www.midnight-commander.org
 
 ```
 
 - - -
 
 ##### mcedit
 
 Internal file editor of GNU Midnight Commander.
 
 ```
 root@kali:~# mcedit -h
 Usage:
   mcedit [OPTION?] [+lineno] file1[:lineno] [file2[:lineno]...]
 
 
 GNU Midnight Commander 4.8.29
 
 
 Help Options:
   -h, --help                Show help options
   --help-all                Show all help options
   --help-terminal           Terminal options
   --help-color              Color options
 
 Application Options:
   -V, --version             Displays the current version
   -f, --datadir             Print data directory
   -F, --datadir-info        Print extended info about used data directories
   --configure-options       Print configure options
   -P, --printwd=<file>      Print last working directory to specified file
   -U, --subshell            Enables subshell support (default)
   -u, --nosubshell          Disables subshell support
   -l, --ftplog=<file>       Log ftp dialog to specified file
   -v, --view=<file>         Launches the file viewer on a file
   -e, --edit=<file> ...     Edit files
 
 
 Please send any bug reports (including the output of 'mc -V')
 as tickets at www.midnight-commander.org
 
 ```
 
 - - -
 
 ##### mcview
 
 Internal file viewer of GNU Midnight Commander.
 
 ```
 root@kali:~# mcview -h
 Usage:
   mcview [OPTION?] file
 
 
 GNU Midnight Commander 4.8.29
 
 
 Help Options:
   -h, --help                Show help options
   --help-all                Show all help options
   --help-terminal           Terminal options
   --help-color              Color options
 
 Application Options:
   -V, --version             Displays the current version
   -f, --datadir             Print data directory
   -F, --datadir-info        Print extended info about used data directories
   --configure-options       Print configure options
   -P, --printwd=<file>      Print last working directory to specified file
   -U, --subshell            Enables subshell support (default)
   -u, --nosubshell          Disables subshell support
   -l, --ftplog=<file>       Log ftp dialog to specified file
   -v, --view=<file>         Launches the file viewer on a file
   -e, --edit=<file> ...     Edit files
 
 
 Please send any bug reports (including the output of 'mc -V')
 as tickets at www.midnight-commander.org
 
 ```
 
 - - -
 
 ### mc-data
 
  GNU Midnight Commander is a text-mode full-screen file manager. It
  uses a two panel interface and a subshell for command execution. It
  includes an internal editor with syntax highlighting and an internal
  viewer with support for binary files. Also included is Virtual
  Filesystem (VFS), that allows files on remote systems (e.g. FTP, SSH
  servers) and files inside archives to be manipulated like real files.
   
  This package provides architecture independent files
 
 **Installed size:** `6.06 MB`  
 **How to install:** `sudo apt install mc-data`  
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
