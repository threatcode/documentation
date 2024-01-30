---
Title: vim
Homepage: https://www.vim.org/
Repository: https://salsa.debian.org/vim-team/vim
Architectures: any all
Version: 2:9.0.2116-1
Metapackages: kali-linux-core kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-linux-nethunter kali-linux-wsl 
Icon: images/vim-logo.svg
PackagesInfo: |
 ### vim
 
  Vim is an almost compatible version of the UNIX editor Vi.
   
  Many new features have been added: multi level undo, syntax
  highlighting, command line history, on-line help, filename
  completion, block operations, folding, Unicode support, etc.
   
  This package contains a version of vim compiled with a rather
  standard set of features.  This package does not provide a GUI
  version of Vim.  See the other vim-* packages if you need more
  (or less).
 
 **Installed size:** `3.65 MB`  
 **How to install:** `sudo apt install vim`  
 
 {{< spoiler "Dependencies:" >}}
 * libacl1 
 * libc6 
 * libgpm2 
 * libselinux1 
 * libsodium23 
 * libtinfo6 
 * vim-common 
 * vim-runtime 
 {{< /spoiler >}}
 
 ##### vim.basic
 
 
 ```
 root@kali:~# vim.basic -h
 VIM - Vi IMproved 9.0 (2022 Jun 28, compiled Nov 20 2023 16:05:25)
 
 Usage: vim [arguments] [file ..]       edit specified file(s)
    or: vim [arguments] -               read text from stdin
    or: vim [arguments] -t tag          edit file where tag is defined
    or: vim [arguments] -q [errorfile]  edit file with first error
 
 Arguments:
    --			Only file names after this
    -v			Vi mode (like "vi")
    -e			Ex mode (like "ex")
    -E			Improved Ex mode
    -s			Silent (batch) mode (only for "ex")
    -d			Diff mode (like "vimdiff")
    -y			Easy mode (like "evim", modeless)
    -R			Readonly mode (like "view")
    -Z			Restricted mode (like "rvim")
    -m			Modifications (writing files) not allowed
    -M			Modifications in text not allowed
    -b			Binary mode
    -l			Lisp mode
    -C			Compatible with Vi: 'compatible'
    -N			Not fully Vi compatible: 'nocompatible'
    -V[N][fname]		Be verbose [level N] [log messages to fname]
    -D			Debugging mode
    -n			No swap file, use memory only
    -r			List swap files and exit
    -r (with file name)	Recover crashed session
    -L			Same as -r
    -A			Start in Arabic mode
    -H			Start in Hebrew mode
    -T <terminal>	Set terminal type to <terminal>
    --not-a-term		Skip warning for input/output not being a terminal
    --ttyfail		Exit if input or output is not a terminal
    -u <vimrc>		Use <vimrc> instead of any .vimrc
    --noplugin		Don't load plugin scripts
    -p[N]		Open N tab pages (default: one for each file)
    -o[N]		Open N windows (default: one for each file)
    -O[N]		Like -o but split vertically
    +			Start at end of file
    +<lnum>		Start at line <lnum>
    --cmd <command>	Execute <command> before loading any vimrc file
    -c <command>		Execute <command> after loading the first file
    -S <session>		Source file <session> after loading the first file
    -s <scriptin>	Read Normal mode commands from file <scriptin>
    -w <scriptout>	Append all typed commands to file <scriptout>
    -W <scriptout>	Write all typed commands to file <scriptout>
    -x			Edit encrypted files
    --startuptime <file>	Write startup timing messages to <file>
    --log <file>		Start logging to <file> early
    -i <viminfo>		Use <viminfo> instead of .viminfo
    --clean		'nocompatible', Vim defaults, no plugins, no viminfo
    -h  or  --help	Print Help (this message) and exit
    --version		Print version information and exit
 ```
 
 - - -
 
 ### vim-athena
 
  This is a transitional package to install the vim-motif package.  You may
  remove this package if nothing depends on it.
 
 **Installed size:** `79 KB`  
 **How to install:** `sudo apt install vim-athena`  
 
 {{< spoiler "Dependencies:" >}}
 * vim-motif
 {{< /spoiler >}}
 
 
 - - -
 
 ### vim-common
 
  Vim is an almost compatible version of the UNIX editor Vi.
   
  This package contains files shared by all non GUI-enabled vim variants
  available in Debian.  Examples of such shared files are: manpages and
  configuration files.
 
 **Installed size:** `1.48 MB`  
 **How to install:** `sudo apt install vim-common`  
 
 ##### helpztags
 
 Generate the help tags file for directory
 
 ```
 root@kali:~# man helpztags
 HELPZTAGS(1)                     User Commands                    HELPZTAGS(1)
 
 NAME
        helpztags - generate the help tags file for directory
 
 SYNOPSIS
        helpztags DIRS...
 
 DESCRIPTION
        helpztags scans given directories for *.txt and *.txt.gz files.  Each
        file is scanned for tags used in vim help files. For each directory
        proper tags file is generated.
 
        There should be at least one directory given. In other case program
        exits with error.
 
 AUTHORS
        Written by Jakub Turski and Artur R. Czechowski based on idea contained
        in vim sources for its :helptags command.
 
 REPORTING BUGS
        Please use a Debian reportbug command or procedure described at
        http://bugs.debian.org/.
 
 SEE ALSO
        Read :help helptags in vim for detailed information about helptags.
 
 vim 9.0                           August 2010                     HELPZTAGS(1)
 ```
 
 - - -
 
 ### vim-doc
 
  Vim is an almost compatible version of the UNIX editor Vi.
   
  This package contains the HTML version of the online documentation.  It is
  built from the runtime/doc directory of the source tree.
 
 **Installed size:** `14.69 MB`  
 **How to install:** `sudo apt install vim-doc`  
 
 
 - - -
 
 ### vim-gtk3
 
  Vim is an almost compatible version of the UNIX editor Vi.
   
  Many new features have been added: multi level undo, syntax
  highlighting, command line history, on-line help, filename
  completion, block operations, folding, Unicode support, etc.
   
  This package contains a version of vim compiled with a GTK3 GUI
  and support for scripting with Lua, Perl, Python 3, Ruby, and Tcl.
 
 **Installed size:** `4.46 MB`  
 **How to install:** `sudo apt install vim-gtk3`  
 
 {{< spoiler "Dependencies:" >}}
 * libacl1 
 * libc6 
 * libcairo2 
 * libcanberra0 
 * libgdk-pixbuf-2.0-0 
 * libglib2.0-0 
 * libgpm2 
 * libgtk-3-0 
 * libice6 
 * liblua5.1-0
 * libpango-1.0-0 
 * libpangocairo-1.0-0 
 * libperl5.36 
 * libpython3.11 
 * libruby3.1 
 * libselinux1 
 * libsm6
 * libsodium23 
 * libtcl8.6 
 * libtinfo6 
 * libx11-6
 * libxt6
 * vim-common 
 * vim-gui-common 
 * vim-runtime 
 {{< /spoiler >}}
 
 ##### vim.gtk3
 
 
 ```
 root@kali:~# vim.gtk3 -h
 VIM - Vi IMproved 9.0 (2022 Jun 28, compiled Nov 20 2023 16:05:25)
 
 Usage: vim [arguments] [file ..]       edit specified file(s)
    or: vim [arguments] -               read text from stdin
    or: vim [arguments] -t tag          edit file where tag is defined
    or: vim [arguments] -q [errorfile]  edit file with first error
 
 Arguments:
    --			Only file names after this
    -g			Run using GUI (like "gvim")
    -f  or  --nofork	Foreground: Don't fork when starting GUI
    -v			Vi mode (like "vi")
    -e			Ex mode (like "ex")
    -E			Improved Ex mode
    -s			Silent (batch) mode (only for "ex")
    -d			Diff mode (like "vimdiff")
    -y			Easy mode (like "evim", modeless)
    -R			Readonly mode (like "view")
    -Z			Restricted mode (like "rvim")
    -m			Modifications (writing files) not allowed
    -M			Modifications in text not allowed
    -b			Binary mode
    -l			Lisp mode
    -C			Compatible with Vi: 'compatible'
    -N			Not fully Vi compatible: 'nocompatible'
    -V[N][fname]		Be verbose [level N] [log messages to fname]
    -D			Debugging mode
    -n			No swap file, use memory only
    -r			List swap files and exit
    -r (with file name)	Recover crashed session
    -L			Same as -r
    -A			Start in Arabic mode
    -H			Start in Hebrew mode
    -T <terminal>	Set terminal type to <terminal>
    --not-a-term		Skip warning for input/output not being a terminal
    --gui-dialog-file {fname}  For testing: write dialog text
    --ttyfail		Exit if input or output is not a terminal
    -u <vimrc>		Use <vimrc> instead of any .vimrc
    -U <gvimrc>		Use <gvimrc> instead of any .gvimrc
    --noplugin		Don't load plugin scripts
    -p[N]		Open N tab pages (default: one for each file)
    -o[N]		Open N windows (default: one for each file)
    -O[N]		Like -o but split vertically
    +			Start at end of file
    +<lnum>		Start at line <lnum>
    --cmd <command>	Execute <command> before loading any vimrc file
    -c <command>		Execute <command> after loading the first file
    -S <session>		Source file <session> after loading the first file
    -s <scriptin>	Read Normal mode commands from file <scriptin>
    -w <scriptout>	Append all typed commands to file <scriptout>
    -W <scriptout>	Write all typed commands to file <scriptout>
    -x			Edit encrypted files
    -X			Do not connect to X server
    --remote <files>	Edit <files> in a Vim server if possible
    --remote-silent <files>  Same, don't complain if there is no server
    --remote-wait <files>  As --remote but wait for files to have been edited
    --remote-wait-silent <files>  Same, don't complain if there is no server
    --remote-tab[-wait][-silent] <files>  As --remote but use tab page per file
    --remote-send <keys>	Send <keys> to a Vim server and exit
    --remote-expr <expr>	Evaluate <expr> in a Vim server and print result
    --serverlist		List available Vim server names and exit
    --servername <name>	Send to/become the Vim server <name>
    --startuptime <file>	Write startup timing messages to <file>
    --log <file>		Start logging to <file> early
    -i <viminfo>		Use <viminfo> instead of .viminfo
    --clean		'nocompatible', Vim defaults, no plugins, no viminfo
    -h  or  --help	Print Help (this message) and exit
    --version		Print version information and exit
 
 Arguments recognised by gvim (GTK+ version):
    -background <color>	Use <color> for the background (also: -bg)
    -foreground <color>	Use <color> for normal text (also: -fg)
    -font <font>		Use <font> for normal text (also: -fn)
    -geometry <geom>	Use <geom> for initial geometry (also: -geom)
    -iconic		Start Vim iconified
    -reverse		Use reverse video (also: -rv)
    -display <display>	Run Vim on <display> (also: --display)
    --role <role>	Set a unique role to identify the main window
    --socketid <xid>	Open Vim inside another GTK widget
    --echo-wid		Make gvim echo the Window ID on stdout
 ```
 
 - - -
 
 ### vim-gui-common
 
  Vim is an almost compatible version of the UNIX editor Vi.
   
  This package contains files shared by all GUI-enabled vim
  variants available in Debian.  Examples of such shared files are:
  gvimtutor, icons, and desktop environments settings.
 
 **Installed size:** `235 KB`  
 **How to install:** `sudo apt install vim-gui-common`  
 
 ##### gvimtutor
 
 The Vim tutor
 
 ```
 root@kali:~# man gvimtutor
 VIMTUTOR(1)                 General Commands Manual                VIMTUTOR(1)
 
 NAME
        vimtutor - the Vim tutor
 
 SYNOPSIS
        vimtutor [-g] [language]
 
 DESCRIPTION
        Vimtutor starts the Vim tutor.  It copies the tutor file first, so that
        it can be modified without changing the original file.
 
        The  Vimtutor  is  useful for people that want to learn their first Vim
        commands.
 
        The optional argument -g starts vimtutor with gvim rather than vim,  if
        the  GUI  version  of vim is available, or falls back to Vim if gvim is
        not found.
 
        The optional [language] argument is the two-letter name of a  language,
        like "it" or "es".  If the [language] argument is missing, the language
        of  the  current  locale  will be used.  If a tutor in this language is
        available, it will be used.  Otherwise  the  English  version  will  be
        used.
 
        Vim is always started in Vi compatible mode.
 
 FILES
        /usr/share/vim/vim90/tutor/tutor[.language]
                       The Vimtutor text file(s).
 
        /usr/share/vim/vim90/tutor/tutor.vim
                       The Vim script used to copy the Vimtutor text file.
 
 AUTHOR
        The  Vimtutor  was  originally  written for Vi by Michael C. Pierce and
        Robert K. Ware, Colorado  School  of  Mines  using  ideas  supplied  by
        Charles  Smith,  Colorado  State  University.  E-mail: bware@mines.col-
        orado.edu (now invalid).
        It was modified for Vim by Bram Moolenaar.  For the names of the trans-
        lators see the tutor files.
 
 SEE ALSO
        vim(1)
 
                                  2001 April 2                      VIMTUTOR(1)
 ```
 
 - - -
 
 ### vim-motif
 
  Vim is an almost compatible version of the UNIX editor Vi.
   
  Many new features have been added: multi level undo, syntax
  highlighting, command line history, on-line help, filename
  completion, block operations, folding, Unicode support, etc.
   
  This package contains a version of vim compiled with a Motif GUI
  and support for scripting with Lua, Perl, Python 3, and Tcl.
 
 **Installed size:** `4.51 MB`  
 **How to install:** `sudo apt install vim-motif`  
 
 {{< spoiler "Dependencies:" >}}
 * libacl1 
 * libc6 
 * libcanberra0 
 * libgpm2 
 * libice6 
 * liblua5.1-0
 * libperl5.36 
 * libpython3.11 
 * libruby3.1 
 * libselinux1 
 * libsm6
 * libsodium23 
 * libtcl8.6 
 * libtinfo6 
 * libx11-6
 * libxm4 
 * libxt6
 * vim-common 
 * vim-gui-common 
 * vim-runtime 
 {{< /spoiler >}}
 
 ##### vim.motif
 
 
 ```
 root@kali:~# vim.motif -h
 VIM - Vi IMproved 9.0 (2022 Jun 28, compiled Nov 20 2023 16:05:25)
 
 Usage: vim [arguments] [file ..]       edit specified file(s)
    or: vim [arguments] -               read text from stdin
    or: vim [arguments] -t tag          edit file where tag is defined
    or: vim [arguments] -q [errorfile]  edit file with first error
 
 Arguments:
    --			Only file names after this
    -g			Run using GUI (like "gvim")
    -f  or  --nofork	Foreground: Don't fork when starting GUI
    -v			Vi mode (like "vi")
    -e			Ex mode (like "ex")
    -E			Improved Ex mode
    -s			Silent (batch) mode (only for "ex")
    -d			Diff mode (like "vimdiff")
    -y			Easy mode (like "evim", modeless)
    -R			Readonly mode (like "view")
    -Z			Restricted mode (like "rvim")
    -m			Modifications (writing files) not allowed
    -M			Modifications in text not allowed
    -b			Binary mode
    -l			Lisp mode
    -C			Compatible with Vi: 'compatible'
    -N			Not fully Vi compatible: 'nocompatible'
    -V[N][fname]		Be verbose [level N] [log messages to fname]
    -D			Debugging mode
    -n			No swap file, use memory only
    -r			List swap files and exit
    -r (with file name)	Recover crashed session
    -L			Same as -r
    -A			Start in Arabic mode
    -H			Start in Hebrew mode
    -T <terminal>	Set terminal type to <terminal>
    --not-a-term		Skip warning for input/output not being a terminal
    --gui-dialog-file {fname}  For testing: write dialog text
    --ttyfail		Exit if input or output is not a terminal
    -u <vimrc>		Use <vimrc> instead of any .vimrc
    -U <gvimrc>		Use <gvimrc> instead of any .gvimrc
    --noplugin		Don't load plugin scripts
    -p[N]		Open N tab pages (default: one for each file)
    -o[N]		Open N windows (default: one for each file)
    -O[N]		Like -o but split vertically
    +			Start at end of file
    +<lnum>		Start at line <lnum>
    --cmd <command>	Execute <command> before loading any vimrc file
    -c <command>		Execute <command> after loading the first file
    -S <session>		Source file <session> after loading the first file
    -s <scriptin>	Read Normal mode commands from file <scriptin>
    -w <scriptout>	Append all typed commands to file <scriptout>
    -W <scriptout>	Write all typed commands to file <scriptout>
    -x			Edit encrypted files
    -display <display>	Connect Vim to this particular X-server
    -X			Do not connect to X server
    --remote <files>	Edit <files> in a Vim server if possible
    --remote-silent <files>  Same, don't complain if there is no server
    --remote-wait <files>  As --remote but wait for files to have been edited
    --remote-wait-silent <files>  Same, don't complain if there is no server
    --remote-tab[-wait][-silent] <files>  As --remote but use tab page per file
    --remote-send <keys>	Send <keys> to a Vim server and exit
    --remote-expr <expr>	Evaluate <expr> in a Vim server and print result
    --serverlist		List available Vim server names and exit
    --servername <name>	Send to/become the Vim server <name>
    --startuptime <file>	Write startup timing messages to <file>
    --log <file>		Start logging to <file> early
    -i <viminfo>		Use <viminfo> instead of .viminfo
    --clean		'nocompatible', Vim defaults, no plugins, no viminfo
    -h  or  --help	Print Help (this message) and exit
    --version		Print version information and exit
 
 Arguments recognised by gvim (Motif version):
    -display <display>	Run Vim on <display>
    -iconic		Start Vim iconified
    -background <color>	Use <color> for the background (also: -bg)
    -foreground <color>	Use <color> for normal text (also: -fg)
    -font <font>		Use <font> for normal text (also: -fn)
    -boldfont <font>	Use <font> for bold text
    -italicfont <font>	Use <font> for italic text
    -geometry <geom>	Use <geom> for initial geometry (also: -geom)
    -borderwidth <width>	Use a border width of <width> (also: -bw)
    -scrollbarwidth <width>  Use a scrollbar width of <width> (also: -sw)
    -reverse		Use reverse video (also: -rv)
    +reverse		Don't use reverse video (also: +rv)
    -xrm <resource>	Set the specified resource
 ```
 
 - - -
 
 ### vim-nox
 
  Vim is an almost compatible version of the UNIX editor Vi.
   
  Many new features have been added: multi level undo, syntax
  highlighting, command line history, on-line help, filename
  completion, block operations, folding, Unicode support, etc.
   
  This package contains a version of vim compiled with support for
  scripting with Lua, Perl, Python 3, Ruby, and Tcl but no GUI.
 
 **Installed size:** `4.15 MB`  
 **How to install:** `sudo apt install vim-nox`  
 
 {{< spoiler "Dependencies:" >}}
 * libacl1 
 * libc6 
 * libgpm2 
 * liblua5.1-0
 * libperl5.36 
 * libpython3.11 
 * libruby3.1 
 * libselinux1 
 * libsodium23 
 * libtcl8.6 
 * libtinfo6 
 * vim-common 
 * vim-runtime 
 {{< /spoiler >}}
 
 ##### vim.nox
 
 
 ```
 root@kali:~# vim.nox -h
 VIM - Vi IMproved 9.0 (2022 Jun 28, compiled Nov 20 2023 16:05:25)
 
 Usage: vim [arguments] [file ..]       edit specified file(s)
    or: vim [arguments] -               read text from stdin
    or: vim [arguments] -t tag          edit file where tag is defined
    or: vim [arguments] -q [errorfile]  edit file with first error
 
 Arguments:
    --			Only file names after this
    -v			Vi mode (like "vi")
    -e			Ex mode (like "ex")
    -E			Improved Ex mode
    -s			Silent (batch) mode (only for "ex")
    -d			Diff mode (like "vimdiff")
    -y			Easy mode (like "evim", modeless)
    -R			Readonly mode (like "view")
    -Z			Restricted mode (like "rvim")
    -m			Modifications (writing files) not allowed
    -M			Modifications in text not allowed
    -b			Binary mode
    -l			Lisp mode
    -C			Compatible with Vi: 'compatible'
    -N			Not fully Vi compatible: 'nocompatible'
    -V[N][fname]		Be verbose [level N] [log messages to fname]
    -D			Debugging mode
    -n			No swap file, use memory only
    -r			List swap files and exit
    -r (with file name)	Recover crashed session
    -L			Same as -r
    -A			Start in Arabic mode
    -H			Start in Hebrew mode
    -T <terminal>	Set terminal type to <terminal>
    --not-a-term		Skip warning for input/output not being a terminal
    --ttyfail		Exit if input or output is not a terminal
    -u <vimrc>		Use <vimrc> instead of any .vimrc
    --noplugin		Don't load plugin scripts
    -p[N]		Open N tab pages (default: one for each file)
    -o[N]		Open N windows (default: one for each file)
    -O[N]		Like -o but split vertically
    +			Start at end of file
    +<lnum>		Start at line <lnum>
    --cmd <command>	Execute <command> before loading any vimrc file
    -c <command>		Execute <command> after loading the first file
    -S <session>		Source file <session> after loading the first file
    -s <scriptin>	Read Normal mode commands from file <scriptin>
    -w <scriptout>	Append all typed commands to file <scriptout>
    -W <scriptout>	Write all typed commands to file <scriptout>
    -x			Edit encrypted files
    --startuptime <file>	Write startup timing messages to <file>
    --log <file>		Start logging to <file> early
    -i <viminfo>		Use <viminfo> instead of .viminfo
    --clean		'nocompatible', Vim defaults, no plugins, no viminfo
    -h  or  --help	Print Help (this message) and exit
    --version		Print version information and exit
 ```
 
 - - -
 
 ### vim-runtime
 
  Vim is an almost compatible version of the UNIX editor Vi.
   
  This package contains vimtutor and the architecture independent runtime
  files, used, if available, by all vim variants available in Debian.
  Example of such runtime files are: online documentation, rules for
  language-specific syntax highlighting and indentation, color schemes,
  and standard plugins.
 
 **Installed size:** `35.15 MB`  
 **How to install:** `sudo apt install vim-runtime`  
 
 ##### vimtutor
 
 The Vim tutor
 
 ```
 root@kali:~# man vimtutor
 VIMTUTOR(1)                 General Commands Manual                VIMTUTOR(1)
 
 NAME
        vimtutor - the Vim tutor
 
 SYNOPSIS
        vimtutor [-g] [language]
 
 DESCRIPTION
        Vimtutor starts the Vim tutor.  It copies the tutor file first, so that
        it can be modified without changing the original file.
 
        The  Vimtutor  is  useful for people that want to learn their first Vim
        commands.
 
        The optional argument -g starts vimtutor with gvim rather than vim,  if
        the  GUI  version  of vim is available, or falls back to Vim if gvim is
        not found.
 
        The optional [language] argument is the two-letter name of a  language,
        like "it" or "es".  If the [language] argument is missing, the language
        of  the  current  locale  will be used.  If a tutor in this language is
        available, it will be used.  Otherwise  the  English  version  will  be
        used.
 
        Vim is always started in Vi compatible mode.
 
 FILES
        /usr/share/vim/vim90/tutor/tutor[.language]
                       The Vimtutor text file(s).
 
        /usr/share/vim/vim90/tutor/tutor.vim
                       The Vim script used to copy the Vimtutor text file.
 
 AUTHOR
        The  Vimtutor  was  originally  written for Vi by Michael C. Pierce and
        Robert K. Ware, Colorado  School  of  Mines  using  ideas  supplied  by
        Charles  Smith,  Colorado  State  University.  E-mail: bware@mines.col-
        orado.edu (now invalid).
        It was modified for Vim by Bram Moolenaar.  For the names of the trans-
        lators see the tutor files.
 
 SEE ALSO
        vim(1)
 
                                  2001 April 2                      VIMTUTOR(1)
 ```
 
 - - -
 
 ### vim-tiny
 
  Vim is an almost compatible version of the UNIX editor Vi.
   
  This package contains a minimal version of Vim compiled with no GUI and
  a small subset of features. This package's sole purpose is to provide
  the vi binary for base installations.
   
  If a vim binary is wanted, try one of the following more featureful
  packages: vim, vim-nox, vim-motif, or vim-gtk3.
 
 **Installed size:** `1.68 MB`  
 **How to install:** `sudo apt install vim-tiny`  
 
 {{< spoiler "Dependencies:" >}}
 * libacl1 
 * libc6 
 * libselinux1 
 * libtinfo6 
 * vim-common 
 {{< /spoiler >}}
 
 ##### vim.tiny
 
 
 ```
 root@kali:~# vim.tiny -h
 VIM - Vi IMproved 9.0 (2022 Jun 28, compiled Nov 20 2023 16:05:25)
 
 Usage: vim [arguments] [file ..]       edit specified file(s)
    or: vim [arguments] -               read text from stdin
    or: vim [arguments] -t tag          edit file where tag is defined
 
 Arguments:
    --			Only file names after this
    -v			Vi mode (like "vi")
    -e			Ex mode (like "ex")
    -E			Improved Ex mode
    -s			Silent (batch) mode (only for "ex")
    -y			Easy mode (like "evim", modeless)
    -R			Readonly mode (like "view")
    -Z			Restricted mode (like "rvim")
    -m			Modifications (writing files) not allowed
    -M			Modifications in text not allowed
    -b			Binary mode
    -l			Lisp mode
    -C			Compatible with Vi: 'compatible'
    -N			Not fully Vi compatible: 'nocompatible'
    -V[N][fname]		Be verbose [level N] [log messages to fname]
    -n			No swap file, use memory only
    -r			List swap files and exit
    -r (with file name)	Recover crashed session
    -L			Same as -r
    -T <terminal>	Set terminal type to <terminal>
    --not-a-term		Skip warning for input/output not being a terminal
    --ttyfail		Exit if input or output is not a terminal
    -u <vimrc>		Use <vimrc> instead of any .vimrc
    --noplugin		Don't load plugin scripts
    -p[N]		Open N tab pages (default: one for each file)
    -o[N]		Open N windows (default: one for each file)
    -O[N]		Like -o but split vertically
    +			Start at end of file
    +<lnum>		Start at line <lnum>
    --cmd <command>	Execute <command> before loading any vimrc file
    -c <command>		Execute <command> after loading the first file
    -S <session>		Source file <session> after loading the first file
    -s <scriptin>	Read Normal mode commands from file <scriptin>
    -w <scriptout>	Append all typed commands to file <scriptout>
    -W <scriptout>	Write all typed commands to file <scriptout>
    --clean		'nocompatible', Vim defaults, no plugins, no viminfo
    -h  or  --help	Print Help (this message) and exit
    --version		Print version information and exit
 ```
 
 - - -
 
 ### xxd
 
  xxd creates a hex dump of a given file or standard input.  It can also convert
  a hex dump back to its original binary form.
 
 **Installed size:** `147 KB`  
 **How to install:** `sudo apt install xxd`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### xxd
 
 Make a hex dump or do the reverse.
 
 ```
 root@kali:~# xxd -h
 Usage:
        xxd [options] [infile [outfile]]
     or
        xxd -r [-s [-]offset] [-c cols] [-ps] [infile [outfile]]
 Options:
     -a          toggle autoskip: A single '*' replaces nul-lines. Default off.
     -b          binary digit dump (incompatible with -ps,-i). Default hex.
     -C          capitalize variable names in C include file style (-i).
     -c cols     format <cols> octets per line. Default 16 (-i: 12, -ps: 30).
     -E          show characters in EBCDIC. Default ASCII.
     -e          little-endian dump (incompatible with -ps,-i,-r).
     -g bytes    number of octets per group in normal output. Default 2 (-e: 4).
     -h          print this summary.
     -i          output in C include file style.
     -l len      stop after <len> octets.
     -n name     set the variable name used in C include output (-i).
     -o off      add <off> to the displayed file position.
     -ps         output in postscript plain hexdump style.
     -r          reverse operation: convert (or patch) hexdump into binary.
     -r -s off   revert with <off> added to file positions found in hexdump.
     -d          show offset in decimal instead of hex.
     -s [+][-]seek  start at <seek> bytes abs. (or +: rel.) infile offset.
     -u          use upper case hex letters.
     -R when     colorize the output; <when> can be 'always', 'auto' or 'never'. Default: 'auto'.
     -v          show version: "xxd 2023-10-25 by Juergen Weigert et al.".
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
