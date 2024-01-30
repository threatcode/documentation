---
Title: zsh
Homepage: https://www.zsh.org/
Repository: https://salsa.debian.org/debian/zsh
Architectures: any all
Version: 5.9-5
Metapackages: kali-linux-core kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-linux-nethunter kali-linux-wsl kali-tools-reporting 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### zsh
 
  Zsh is a UNIX command interpreter (shell) usable as an
  interactive login shell and as a shell script command
  processor. Of the standard shells, zsh most closely resembles
  ksh but includes many enhancements. Zsh has command-line editing,
  built-in spelling correction, programmable command completion,
  shell functions (with autoloading), a history mechanism, and a
  host of other features.
 
 **Installed size:** `2.40 MB`  
 **How to install:** `sudo apt install zsh`  
 
 {{< spoiler "Dependencies:" >}}
 * debianutils 
 * libc6 
 * libcap2 
 * libtinfo6 
 * zsh-common 
 {{< /spoiler >}}
 
 ##### rzsh
 
 The Z shell
 
 ```
 root@kali:~# rzsh --help
 Usage: rzsh [<options>] [<argument> ...]
 
 Special options:
   --help     show this message, then exit
   --version  show zsh version number, then exit
   -b         end option processing, like --
   -c         take first argument as a command to execute
   -o OPTION  set an option by name (see below)
 
 Normal options are named.  An option may be turned on by
 `-o OPTION', `--OPTION', `+o no_OPTION' or `+-no-OPTION'.  An
 option may be turned off by `-o no_OPTION', `--no-OPTION',
 `+o OPTION' or `+-OPTION'.  Options are listed below only in
 `--OPTION' or `--no-OPTION' form.
 
 Named options:
   --aliases
   --aliasfuncdef
   --allexport
   --alwayslastprompt
   --alwaystoend
   --appendcreate
   --appendhistory
   --autocd
   --autocontinue
   --autolist
   --automenu
   --autonamedirs
   --autoparamkeys
   --autoparamslash
   --autopushd
   --autoremoveslash
   --autoresume
   --badpattern
   --banghist
   --bareglobqual
   --bashautolist
   --bashrematch
   --beep
   --bgnice
   --braceccl
   --bsdecho
   --caseglob
   --casematch
   --casepaths
   --cbases
   --cdablevars
   --cdsilent
   --chasedots
   --chaselinks
   --checkjobs
   --checkrunningjobs
   --clobber
   --clobberempty
   --combiningchars
   --completealiases
   --completeinword
   --continueonerror
   --correct
   --correctall
   --cprecedences
   --cshjunkiehistory
   --cshjunkieloops
   --cshjunkiequotes
   --cshnullcmd
   --cshnullglob
   --debugbeforecmd
   --dvorak
   --emacs
   --equals
   --errexit
   --errreturn
   --evallineno
   --exec
   --extendedglob
   --extendedhistory
   --flowcontrol
   --forcefloat
   --functionargzero
   --glob
   --globalexport
   --globalrcs
   --globassign
   --globcomplete
   --globdots
   --globstarshort
   --globsubst
   --hashcmds
   --hashdirs
   --hashexecutablesonly
   --hashlistall
   --histallowclobber
   --histbeep
   --histexpiredupsfirst
   --histfcntllock
   --histfindnodups
   --histignorealldups
   --histignoredups
   --histignorespace
   --histlexwords
   --histnofunctions
   --histnostore
   --histreduceblanks
   --histsavebycopy
   --histsavenodups
   --histsubstpattern
   --histverify
   --hup
   --ignorebraces
   --ignoreclosebraces
   --ignoreeof
   --incappendhistory
   --incappendhistorytime
   --interactive
   --interactivecomments
   --ksharrays
   --kshautoload
   --kshglob
   --kshoptionprint
   --kshtypeset
   --kshzerosubscript
   --listambiguous
   --listbeep
   --listpacked
   --listrowsfirst
   --listtypes
   --localloops
   --localoptions
   --localpatterns
   --localtraps
   --login
   --longlistjobs
   --magicequalsubst
   --mailwarning
   --markdirs
   --menucomplete
   --monitor
   --multibyte
   --multifuncdef
   --multios
   --nomatch
   --notify
   --nullglob
   --numericglobsort
   --octalzeroes
   --overstrike
   --pathdirs
   --pathscript
   --pipefail
   --posixaliases
   --posixargzero
   --posixbuiltins
   --posixcd
   --posixidentifiers
   --posixjobs
   --posixstrings
   --posixtraps
   --printeightbit
   --printexitvalue
   --privileged
   --promptbang
   --promptcr
   --promptpercent
   --promptsp
   --promptsubst
   --pushdignoredups
   --pushdminus
   --pushdsilent
   --pushdtohome
   --rcexpandparam
   --rcquotes
   --rcs
   --recexact
   --rematchpcre
   --restricted
   --rmstarsilent
   --rmstarwait
   --sharehistory
   --shfileexpansion
   --shglob
   --shinstdin
   --shnullcmd
   --shoptionletters
   --shortloops
   --shortrepeat
   --shwordsplit
   --singlecommand
   --singlelinezle
   --sourcetrace
   --sunkeyboardhack
   --transientrprompt
   --trapsasync
   --typesetsilent
   --typesettounset
   --unset
   --verbose
   --vi
   --warncreateglobal
   --warnnestedvar
   --xtrace
   --zle
 
 Option aliases:
   --braceexpand            equivalent to --no-ignorebraces
   --dotglob                equivalent to --globdots
   --hashall                equivalent to --hashcmds
   --histappend             equivalent to --appendcreate
   --histexpand             equivalent to --badpattern
   --log                    equivalent to --no-histnofunctions
   --mailwarn               equivalent to --mailwarning
   --onecmd                 equivalent to --singlecommand
   --physical               equivalent to --cdsilent
   --promptvars             equivalent to --promptsubst
   --stdin                  equivalent to --shinstdin
   --trackall               equivalent to --hashcmds
 
 Option letters:
   -0    equivalent to --completeinword
   -1    equivalent to --printexitvalue
   -2    equivalent to --no-autoresume
   -3    equivalent to --no-nomatch
   -4    equivalent to --globdots
   -5    equivalent to --notify
   -6    equivalent to --beep
   -7    equivalent to --ignoreeof
   -8    equivalent to --markdirs
   -9    equivalent to --autocontinue
   -B    equivalent to --no-bashrematch
   -C    equivalent to --no-checkjobs
   -D    equivalent to --pushdtohome
   -E    equivalent to --pushdsilent
   -F    equivalent to --no-glob
   -G    equivalent to --nullglob
   -H    equivalent to --rmstarsilent
   -I    equivalent to --ignorebraces
   -J    equivalent to --appendhistory
   -K    equivalent to --no-badpattern
   -L    equivalent to --sunkeyboardhack
   -M    equivalent to --singlelinezle
   -N    equivalent to --autoparamslash
   -O    equivalent to --continueonerror
   -P    equivalent to --rcexpandparam
   -Q    equivalent to --pathdirs
   -R    equivalent to --longlistjobs
   -S    equivalent to --recexact
   -T    equivalent to --cbases
   -U    equivalent to --mailwarning
   -V    equivalent to --no-promptcr
   -W    equivalent to --autoremoveslash
   -X    equivalent to --listtypes
   -Y    equivalent to --menucomplete
   -Z    equivalent to --zle
   -a    equivalent to --allexport
   -d    equivalent to --no-globalrcs
   -e    equivalent to --errexit
   -f    equivalent to --no-rcs
   -g    equivalent to --histignorespace
   -h    equivalent to --histignoredups
   -i    equivalent to --interactive
   -k    equivalent to --interactivecomments
   -l    equivalent to --login
   -m    equivalent to --monitor
   -n    equivalent to --no-exec
   -p    equivalent to --privileged
   -r    equivalent to --restricted
   -s    equivalent to --shinstdin
   -t    equivalent to --singlecommand
   -u    equivalent to --no-unset
   -v    equivalent to --verbose
   -w    equivalent to --cdsilent
   -x    equivalent to --xtrace
   -y    equivalent to --shwordsplit
 ```
 
 - - -
 
 ##### zsh
 
 The Z shell
 
 ```
 root@kali:~# zsh --help
 Usage: zsh [<options>] [<argument> ...]
 
 Special options:
   --help     show this message, then exit
   --version  show zsh version number, then exit
   -b         end option processing, like --
   -c         take first argument as a command to execute
   -o OPTION  set an option by name (see below)
 
 Normal options are named.  An option may be turned on by
 `-o OPTION', `--OPTION', `+o no_OPTION' or `+-no-OPTION'.  An
 option may be turned off by `-o no_OPTION', `--no-OPTION',
 `+o OPTION' or `+-OPTION'.  Options are listed below only in
 `--OPTION' or `--no-OPTION' form.
 
 Named options:
   --aliases
   --aliasfuncdef
   --allexport
   --alwayslastprompt
   --alwaystoend
   --appendcreate
   --appendhistory
   --autocd
   --autocontinue
   --autolist
   --automenu
   --autonamedirs
   --autoparamkeys
   --autoparamslash
   --autopushd
   --autoremoveslash
   --autoresume
   --badpattern
   --banghist
   --bareglobqual
   --bashautolist
   --bashrematch
   --beep
   --bgnice
   --braceccl
   --bsdecho
   --caseglob
   --casematch
   --casepaths
   --cbases
   --cdablevars
   --cdsilent
   --chasedots
   --chaselinks
   --checkjobs
   --checkrunningjobs
   --clobber
   --clobberempty
   --combiningchars
   --completealiases
   --completeinword
   --continueonerror
   --correct
   --correctall
   --cprecedences
   --cshjunkiehistory
   --cshjunkieloops
   --cshjunkiequotes
   --cshnullcmd
   --cshnullglob
   --debugbeforecmd
   --dvorak
   --emacs
   --equals
   --errexit
   --errreturn
   --evallineno
   --exec
   --extendedglob
   --extendedhistory
   --flowcontrol
   --forcefloat
   --functionargzero
   --glob
   --globalexport
   --globalrcs
   --globassign
   --globcomplete
   --globdots
   --globstarshort
   --globsubst
   --hashcmds
   --hashdirs
   --hashexecutablesonly
   --hashlistall
   --histallowclobber
   --histbeep
   --histexpiredupsfirst
   --histfcntllock
   --histfindnodups
   --histignorealldups
   --histignoredups
   --histignorespace
   --histlexwords
   --histnofunctions
   --histnostore
   --histreduceblanks
   --histsavebycopy
   --histsavenodups
   --histsubstpattern
   --histverify
   --hup
   --ignorebraces
   --ignoreclosebraces
   --ignoreeof
   --incappendhistory
   --incappendhistorytime
   --interactive
   --interactivecomments
   --ksharrays
   --kshautoload
   --kshglob
   --kshoptionprint
   --kshtypeset
   --kshzerosubscript
   --listambiguous
   --listbeep
   --listpacked
   --listrowsfirst
   --listtypes
   --localloops
   --localoptions
   --localpatterns
   --localtraps
   --login
   --longlistjobs
   --magicequalsubst
   --mailwarning
   --markdirs
   --menucomplete
   --monitor
   --multibyte
   --multifuncdef
   --multios
   --nomatch
   --notify
   --nullglob
   --numericglobsort
   --octalzeroes
   --overstrike
   --pathdirs
   --pathscript
   --pipefail
   --posixaliases
   --posixargzero
   --posixbuiltins
   --posixcd
   --posixidentifiers
   --posixjobs
   --posixstrings
   --posixtraps
   --printeightbit
   --printexitvalue
   --privileged
   --promptbang
   --promptcr
   --promptpercent
   --promptsp
   --promptsubst
   --pushdignoredups
   --pushdminus
   --pushdsilent
   --pushdtohome
   --rcexpandparam
   --rcquotes
   --rcs
   --recexact
   --rematchpcre
   --restricted
   --rmstarsilent
   --rmstarwait
   --sharehistory
   --shfileexpansion
   --shglob
   --shinstdin
   --shnullcmd
   --shoptionletters
   --shortloops
   --shortrepeat
   --shwordsplit
   --singlecommand
   --singlelinezle
   --sourcetrace
   --sunkeyboardhack
   --transientrprompt
   --trapsasync
   --typesetsilent
   --typesettounset
   --unset
   --verbose
   --vi
   --warncreateglobal
   --warnnestedvar
   --xtrace
   --zle
 
 Option aliases:
   --braceexpand            equivalent to --no-ignorebraces
   --dotglob                equivalent to --globdots
   --hashall                equivalent to --hashcmds
   --histappend             equivalent to --appendcreate
   --histexpand             equivalent to --badpattern
   --log                    equivalent to --no-histnofunctions
   --mailwarn               equivalent to --mailwarning
   --onecmd                 equivalent to --singlecommand
   --physical               equivalent to --cdsilent
   --promptvars             equivalent to --promptsubst
   --stdin                  equivalent to --shinstdin
   --trackall               equivalent to --hashcmds
 
 Option letters:
   -0    equivalent to --completeinword
   -1    equivalent to --printexitvalue
   -2    equivalent to --no-autoresume
   -3    equivalent to --no-nomatch
   -4    equivalent to --globdots
   -5    equivalent to --notify
   -6    equivalent to --beep
   -7    equivalent to --ignoreeof
   -8    equivalent to --markdirs
   -9    equivalent to --autocontinue
   -B    equivalent to --no-bashrematch
   -C    equivalent to --no-checkjobs
   -D    equivalent to --pushdtohome
   -E    equivalent to --pushdsilent
   -F    equivalent to --no-glob
   -G    equivalent to --nullglob
   -H    equivalent to --rmstarsilent
   -I    equivalent to --ignorebraces
   -J    equivalent to --appendhistory
   -K    equivalent to --no-badpattern
   -L    equivalent to --sunkeyboardhack
   -M    equivalent to --singlelinezle
   -N    equivalent to --autoparamslash
   -O    equivalent to --continueonerror
   -P    equivalent to --rcexpandparam
   -Q    equivalent to --pathdirs
   -R    equivalent to --longlistjobs
   -S    equivalent to --recexact
   -T    equivalent to --cbases
   -U    equivalent to --mailwarning
   -V    equivalent to --no-promptcr
   -W    equivalent to --autoremoveslash
   -X    equivalent to --listtypes
   -Y    equivalent to --menucomplete
   -Z    equivalent to --zle
   -a    equivalent to --allexport
   -d    equivalent to --no-globalrcs
   -e    equivalent to --errexit
   -f    equivalent to --no-rcs
   -g    equivalent to --histignorespace
   -h    equivalent to --histignoredups
   -i    equivalent to --interactive
   -k    equivalent to --interactivecomments
   -l    equivalent to --login
   -m    equivalent to --monitor
   -n    equivalent to --no-exec
   -p    equivalent to --privileged
   -r    equivalent to --restricted
   -s    equivalent to --shinstdin
   -t    equivalent to --singlecommand
   -u    equivalent to --no-unset
   -v    equivalent to --verbose
   -w    equivalent to --cdsilent
   -x    equivalent to --xtrace
   -y    equivalent to --shwordsplit
 ```
 
 - - -
 
 ##### zsh5
 
 
 ```
 root@kali:~# zsh5 --help
 Usage: /bin/zsh [<options>] [<argument> ...]
 
 Special options:
   --help     show this message, then exit
   --version  show zsh version number, then exit
   -b         end option processing, like --
   -c         take first argument as a command to execute
   -o OPTION  set an option by name (see below)
 
 Normal options are named.  An option may be turned on by
 `-o OPTION', `--OPTION', `+o no_OPTION' or `+-no-OPTION'.  An
 option may be turned off by `-o no_OPTION', `--no-OPTION',
 `+o OPTION' or `+-OPTION'.  Options are listed below only in
 `--OPTION' or `--no-OPTION' form.
 
 Named options:
   --aliases
   --aliasfuncdef
   --allexport
   --alwayslastprompt
   --alwaystoend
   --appendcreate
   --appendhistory
   --autocd
   --autocontinue
   --autolist
   --automenu
   --autonamedirs
   --autoparamkeys
   --autoparamslash
   --autopushd
   --autoremoveslash
   --autoresume
   --badpattern
   --banghist
   --bareglobqual
   --bashautolist
   --bashrematch
   --beep
   --bgnice
   --braceccl
   --bsdecho
   --caseglob
   --casematch
   --casepaths
   --cbases
   --cdablevars
   --cdsilent
   --chasedots
   --chaselinks
   --checkjobs
   --checkrunningjobs
   --clobber
   --clobberempty
   --combiningchars
   --completealiases
   --completeinword
   --continueonerror
   --correct
   --correctall
   --cprecedences
   --cshjunkiehistory
   --cshjunkieloops
   --cshjunkiequotes
   --cshnullcmd
   --cshnullglob
   --debugbeforecmd
   --dvorak
   --emacs
   --equals
   --errexit
   --errreturn
   --evallineno
   --exec
   --extendedglob
   --extendedhistory
   --flowcontrol
   --forcefloat
   --functionargzero
   --glob
   --globalexport
   --globalrcs
   --globassign
   --globcomplete
   --globdots
   --globstarshort
   --globsubst
   --hashcmds
   --hashdirs
   --hashexecutablesonly
   --hashlistall
   --histallowclobber
   --histbeep
   --histexpiredupsfirst
   --histfcntllock
   --histfindnodups
   --histignorealldups
   --histignoredups
   --histignorespace
   --histlexwords
   --histnofunctions
   --histnostore
   --histreduceblanks
   --histsavebycopy
   --histsavenodups
   --histsubstpattern
   --histverify
   --hup
   --ignorebraces
   --ignoreclosebraces
   --ignoreeof
   --incappendhistory
   --incappendhistorytime
   --interactive
   --interactivecomments
   --ksharrays
   --kshautoload
   --kshglob
   --kshoptionprint
   --kshtypeset
   --kshzerosubscript
   --listambiguous
   --listbeep
   --listpacked
   --listrowsfirst
   --listtypes
   --localloops
   --localoptions
   --localpatterns
   --localtraps
   --login
   --longlistjobs
   --magicequalsubst
   --mailwarning
   --markdirs
   --menucomplete
   --monitor
   --multibyte
   --multifuncdef
   --multios
   --nomatch
   --notify
   --nullglob
   --numericglobsort
   --octalzeroes
   --overstrike
   --pathdirs
   --pathscript
   --pipefail
   --posixaliases
   --posixargzero
   --posixbuiltins
   --posixcd
   --posixidentifiers
   --posixjobs
   --posixstrings
   --posixtraps
   --printeightbit
   --printexitvalue
   --privileged
   --promptbang
   --promptcr
   --promptpercent
   --promptsp
   --promptsubst
   --pushdignoredups
   --pushdminus
   --pushdsilent
   --pushdtohome
   --rcexpandparam
   --rcquotes
   --rcs
   --recexact
   --rematchpcre
   --restricted
   --rmstarsilent
   --rmstarwait
   --sharehistory
   --shfileexpansion
   --shglob
   --shinstdin
   --shnullcmd
   --shoptionletters
   --shortloops
   --shortrepeat
   --shwordsplit
   --singlecommand
   --singlelinezle
   --sourcetrace
   --sunkeyboardhack
   --transientrprompt
   --trapsasync
   --typesetsilent
   --typesettounset
   --unset
   --verbose
   --vi
   --warncreateglobal
   --warnnestedvar
   --xtrace
   --zle
 
 Option aliases:
   --braceexpand            equivalent to --no-ignorebraces
   --dotglob                equivalent to --globdots
   --hashall                equivalent to --hashcmds
   --histappend             equivalent to --appendcreate
   --histexpand             equivalent to --badpattern
   --log                    equivalent to --no-histnofunctions
   --mailwarn               equivalent to --mailwarning
   --onecmd                 equivalent to --singlecommand
   --physical               equivalent to --cdsilent
   --promptvars             equivalent to --promptsubst
   --stdin                  equivalent to --shinstdin
   --trackall               equivalent to --hashcmds
 
 Option letters:
   -0    equivalent to --completeinword
   -1    equivalent to --printexitvalue
   -2    equivalent to --no-autoresume
   -3    equivalent to --no-nomatch
   -4    equivalent to --globdots
   -5    equivalent to --notify
   -6    equivalent to --beep
   -7    equivalent to --ignoreeof
   -8    equivalent to --markdirs
   -9    equivalent to --autocontinue
   -B    equivalent to --no-bashrematch
   -C    equivalent to --no-checkjobs
   -D    equivalent to --pushdtohome
   -E    equivalent to --pushdsilent
   -F    equivalent to --no-glob
   -G    equivalent to --nullglob
   -H    equivalent to --rmstarsilent
   -I    equivalent to --ignorebraces
   -J    equivalent to --appendhistory
   -K    equivalent to --no-badpattern
   -L    equivalent to --sunkeyboardhack
   -M    equivalent to --singlelinezle
   -N    equivalent to --autoparamslash
   -O    equivalent to --continueonerror
   -P    equivalent to --rcexpandparam
   -Q    equivalent to --pathdirs
   -R    equivalent to --longlistjobs
   -S    equivalent to --recexact
   -T    equivalent to --cbases
   -U    equivalent to --mailwarning
   -V    equivalent to --no-promptcr
   -W    equivalent to --autoremoveslash
   -X    equivalent to --listtypes
   -Y    equivalent to --menucomplete
   -Z    equivalent to --zle
   -a    equivalent to --allexport
   -d    equivalent to --no-globalrcs
   -e    equivalent to --errexit
   -f    equivalent to --no-rcs
   -g    equivalent to --histignorespace
   -h    equivalent to --histignoredups
   -i    equivalent to --interactive
   -k    equivalent to --interactivecomments
   -l    equivalent to --login
   -m    equivalent to --monitor
   -n    equivalent to --no-exec
   -p    equivalent to --privileged
   -r    equivalent to --restricted
   -s    equivalent to --shinstdin
   -t    equivalent to --singlecommand
   -u    equivalent to --no-unset
   -v    equivalent to --verbose
   -w    equivalent to --cdsilent
   -x    equivalent to --xtrace
   -y    equivalent to --shwordsplit
 ```
 
 - - -
 
 ### zsh-common
 
  Zsh is a UNIX command interpreter (shell) usable as an
  interactive login shell and as a shell script command
  processor. Of the standard shells, zsh most closely resembles
  ksh but includes many enhancements. Zsh has command-line editing,
  built-in spelling correction, programmable command completion,
  shell functions (with autoloading), a history mechanism, and a
  host of other features.
   
  This package contains the common zsh files shared by all
  architectures.
 
 **Installed size:** `16.03 MB`  
 **How to install:** `sudo apt install zsh-common`  
 
 
 - - -
 
 ### zsh-dev
 
  Zsh is a UNIX command interpreter (shell) usable as an
  interactive login shell and as a shell script command
  processor. Of the standard shells, zsh most closely resembles
  ksh but includes many enhancements. Zsh has command-line editing,
  built-in spelling correction, programmable command completion,
  shell functions (with autoloading), a history mechanism, and a
  host of other features.
   
  This package contains headers and scripts necessary to compile
  third-party modules.
 
 **Installed size:** `686 KB`  
 **How to install:** `sudo apt install zsh-dev`  
 
 {{< spoiler "Dependencies:" >}}
 * zsh-common 
 {{< /spoiler >}}
 
 
 - - -
 
 ### zsh-doc
 
  Zsh is a UNIX command interpreter (shell) usable as an
  interactive login shell and as a shell script command
  processor. Of the standard shells, zsh most closely resembles
  ksh but includes many enhancements. Zsh has command-line editing,
  built-in spelling correction, programmable command completion,
  shell functions (with autoloading), a history mechanism, and a
  host of other features.
   
  This contains the documentation in GNU info and HTML formats.
 
 **Installed size:** `5.93 MB`  
 **How to install:** `sudo apt install zsh-doc`  
 
 {{< spoiler "Dependencies:" >}}
 * zsh-common 
 {{< /spoiler >}}
 
 
 - - -
 
 ### zsh-static
 
  Zsh is a UNIX command interpreter (shell) usable as an
  interactive login shell and as a shell script command
  processor. Of the standard shells, zsh most closely resembles
  ksh but includes many enhancements. Zsh has command-line editing,
  built-in spelling correction, programmable command completion,
  shell functions (with autoloading), a history mechanism, and a
  host of other features.
   
  This is the statically-compiled version of the shell, i.e. it doesn't
  require any dynamically loaded libraries to be present and will work
  even if libraries zsh (in general) needs are broken on the system. So
  it's more robust in case of a broken system.
   
  It though also has a few limitations compared to the normal,
  dynamically linked, e.g. it can't use NSS related functionality which
  might result in minor imperfections like e.g. user names being shown
  in the prompt.
 
 **Installed size:** `2.60 MB`  
 **How to install:** `sudo apt install zsh-static`  
 
 {{< spoiler "Dependencies:" >}}
 * debianutils 
 {{< /spoiler >}}
 
 ##### zsh-static
 
 The Z shell
 
 ```
 root@kali:~# zsh-static --help
 Usage: zsh-static [<options>] [<argument> ...]
 
 Special options:
   --help     show this message, then exit
   --version  show zsh version number, then exit
   -b         end option processing, like --
   -c         take first argument as a command to execute
   -o OPTION  set an option by name (see below)
 
 Normal options are named.  An option may be turned on by
 `-o OPTION', `--OPTION', `+o no_OPTION' or `+-no-OPTION'.  An
 option may be turned off by `-o no_OPTION', `--no-OPTION',
 `+o OPTION' or `+-OPTION'.  Options are listed below only in
 `--OPTION' or `--no-OPTION' form.
 
 Named options:
   --aliases
   --aliasfuncdef
   --allexport
   --alwayslastprompt
   --alwaystoend
   --appendcreate
   --appendhistory
   --autocd
   --autocontinue
   --autolist
   --automenu
   --autonamedirs
   --autoparamkeys
   --autoparamslash
   --autopushd
   --autoremoveslash
   --autoresume
   --badpattern
   --banghist
   --bareglobqual
   --bashautolist
   --bashrematch
   --beep
   --bgnice
   --braceccl
   --bsdecho
   --caseglob
   --casematch
   --casepaths
   --cbases
   --cdablevars
   --cdsilent
   --chasedots
   --chaselinks
   --checkjobs
   --checkrunningjobs
   --clobber
   --clobberempty
   --combiningchars
   --completealiases
   --completeinword
   --continueonerror
   --correct
   --correctall
   --cprecedences
   --cshjunkiehistory
   --cshjunkieloops
   --cshjunkiequotes
   --cshnullcmd
   --cshnullglob
   --debugbeforecmd
   --dvorak
   --emacs
   --equals
   --errexit
   --errreturn
   --evallineno
   --exec
   --extendedglob
   --extendedhistory
   --flowcontrol
   --forcefloat
   --functionargzero
   --glob
   --globalexport
   --globalrcs
   --globassign
   --globcomplete
   --globdots
   --globstarshort
   --globsubst
   --hashcmds
   --hashdirs
   --hashexecutablesonly
   --hashlistall
   --histallowclobber
   --histbeep
   --histexpiredupsfirst
   --histfcntllock
   --histfindnodups
   --histignorealldups
   --histignoredups
   --histignorespace
   --histlexwords
   --histnofunctions
   --histnostore
   --histreduceblanks
   --histsavebycopy
   --histsavenodups
   --histsubstpattern
   --histverify
   --hup
   --ignorebraces
   --ignoreclosebraces
   --ignoreeof
   --incappendhistory
   --incappendhistorytime
   --interactive
   --interactivecomments
   --ksharrays
   --kshautoload
   --kshglob
   --kshoptionprint
   --kshtypeset
   --kshzerosubscript
   --listambiguous
   --listbeep
   --listpacked
   --listrowsfirst
   --listtypes
   --localloops
   --localoptions
   --localpatterns
   --localtraps
   --login
   --longlistjobs
   --magicequalsubst
   --mailwarning
   --markdirs
   --menucomplete
   --monitor
   --multibyte
   --multifuncdef
   --multios
   --nomatch
   --notify
   --nullglob
   --numericglobsort
   --octalzeroes
   --overstrike
   --pathdirs
   --pathscript
   --pipefail
   --posixaliases
   --posixargzero
   --posixbuiltins
   --posixcd
   --posixidentifiers
   --posixjobs
   --posixstrings
   --posixtraps
   --printeightbit
   --printexitvalue
   --privileged
   --promptbang
   --promptcr
   --promptpercent
   --promptsp
   --promptsubst
   --pushdignoredups
   --pushdminus
   --pushdsilent
   --pushdtohome
   --rcexpandparam
   --rcquotes
   --rcs
   --recexact
   --rematchpcre
   --restricted
   --rmstarsilent
   --rmstarwait
   --sharehistory
   --shfileexpansion
   --shglob
   --shinstdin
   --shnullcmd
   --shoptionletters
   --shortloops
   --shortrepeat
   --shwordsplit
   --singlecommand
   --singlelinezle
   --sourcetrace
   --sunkeyboardhack
   --transientrprompt
   --trapsasync
   --typesetsilent
   --typesettounset
   --unset
   --verbose
   --vi
   --warncreateglobal
   --warnnestedvar
   --xtrace
   --zle
 
 Option aliases:
   --braceexpand            equivalent to --no-ignorebraces
   --dotglob                equivalent to --globdots
   --hashall                equivalent to --hashcmds
   --histappend             equivalent to --appendcreate
   --histexpand             equivalent to --badpattern
   --log                    equivalent to --no-histnofunctions
   --mailwarn               equivalent to --mailwarning
   --onecmd                 equivalent to --singlecommand
   --physical               equivalent to --cdsilent
   --promptvars             equivalent to --promptsubst
   --stdin                  equivalent to --shinstdin
   --trackall               equivalent to --hashcmds
 
 Option letters:
   -0    equivalent to --completeinword
   -1    equivalent to --printexitvalue
   -2    equivalent to --no-autoresume
   -3    equivalent to --no-nomatch
   -4    equivalent to --globdots
   -5    equivalent to --notify
   -6    equivalent to --beep
   -7    equivalent to --ignoreeof
   -8    equivalent to --markdirs
   -9    equivalent to --autocontinue
   -B    equivalent to --no-bashrematch
   -C    equivalent to --no-checkjobs
   -D    equivalent to --pushdtohome
   -E    equivalent to --pushdsilent
   -F    equivalent to --no-glob
   -G    equivalent to --nullglob
   -H    equivalent to --rmstarsilent
   -I    equivalent to --ignorebraces
   -J    equivalent to --appendhistory
   -K    equivalent to --no-badpattern
   -L    equivalent to --sunkeyboardhack
   -M    equivalent to --singlelinezle
   -N    equivalent to --autoparamslash
   -O    equivalent to --continueonerror
   -P    equivalent to --rcexpandparam
   -Q    equivalent to --pathdirs
   -R    equivalent to --longlistjobs
   -S    equivalent to --recexact
   -T    equivalent to --cbases
   -U    equivalent to --mailwarning
   -V    equivalent to --no-promptcr
   -W    equivalent to --autoremoveslash
   -X    equivalent to --listtypes
   -Y    equivalent to --menucomplete
   -Z    equivalent to --zle
   -a    equivalent to --allexport
   -d    equivalent to --no-globalrcs
   -e    equivalent to --errexit
   -f    equivalent to --no-rcs
   -g    equivalent to --histignorespace
   -h    equivalent to --histignoredups
   -i    equivalent to --interactive
   -k    equivalent to --interactivecomments
   -l    equivalent to --login
   -m    equivalent to --monitor
   -n    equivalent to --no-exec
   -p    equivalent to --privileged
   -r    equivalent to --restricted
   -s    equivalent to --shinstdin
   -t    equivalent to --singlecommand
   -u    equivalent to --no-unset
   -v    equivalent to --verbose
   -w    equivalent to --cdsilent
   -x    equivalent to --xtrace
   -y    equivalent to --shwordsplit
 ```
 
 - - -
 
 ##### zsh5-static
 
 
 ```
 root@kali:~# zsh5-static --help
 Usage: /bin/zsh-static [<options>] [<argument> ...]
 
 Special options:
   --help     show this message, then exit
   --version  show zsh version number, then exit
   -b         end option processing, like --
   -c         take first argument as a command to execute
   -o OPTION  set an option by name (see below)
 
 Normal options are named.  An option may be turned on by
 `-o OPTION', `--OPTION', `+o no_OPTION' or `+-no-OPTION'.  An
 option may be turned off by `-o no_OPTION', `--no-OPTION',
 `+o OPTION' or `+-OPTION'.  Options are listed below only in
 `--OPTION' or `--no-OPTION' form.
 
 Named options:
   --aliases
   --aliasfuncdef
   --allexport
   --alwayslastprompt
   --alwaystoend
   --appendcreate
   --appendhistory
   --autocd
   --autocontinue
   --autolist
   --automenu
   --autonamedirs
   --autoparamkeys
   --autoparamslash
   --autopushd
   --autoremoveslash
   --autoresume
   --badpattern
   --banghist
   --bareglobqual
   --bashautolist
   --bashrematch
   --beep
   --bgnice
   --braceccl
   --bsdecho
   --caseglob
   --casematch
   --casepaths
   --cbases
   --cdablevars
   --cdsilent
   --chasedots
   --chaselinks
   --checkjobs
   --checkrunningjobs
   --clobber
   --clobberempty
   --combiningchars
   --completealiases
   --completeinword
   --continueonerror
   --correct
   --correctall
   --cprecedences
   --cshjunkiehistory
   --cshjunkieloops
   --cshjunkiequotes
   --cshnullcmd
   --cshnullglob
   --debugbeforecmd
   --dvorak
   --emacs
   --equals
   --errexit
   --errreturn
   --evallineno
   --exec
   --extendedglob
   --extendedhistory
   --flowcontrol
   --forcefloat
   --functionargzero
   --glob
   --globalexport
   --globalrcs
   --globassign
   --globcomplete
   --globdots
   --globstarshort
   --globsubst
   --hashcmds
   --hashdirs
   --hashexecutablesonly
   --hashlistall
   --histallowclobber
   --histbeep
   --histexpiredupsfirst
   --histfcntllock
   --histfindnodups
   --histignorealldups
   --histignoredups
   --histignorespace
   --histlexwords
   --histnofunctions
   --histnostore
   --histreduceblanks
   --histsavebycopy
   --histsavenodups
   --histsubstpattern
   --histverify
   --hup
   --ignorebraces
   --ignoreclosebraces
   --ignoreeof
   --incappendhistory
   --incappendhistorytime
   --interactive
   --interactivecomments
   --ksharrays
   --kshautoload
   --kshglob
   --kshoptionprint
   --kshtypeset
   --kshzerosubscript
   --listambiguous
   --listbeep
   --listpacked
   --listrowsfirst
   --listtypes
   --localloops
   --localoptions
   --localpatterns
   --localtraps
   --login
   --longlistjobs
   --magicequalsubst
   --mailwarning
   --markdirs
   --menucomplete
   --monitor
   --multibyte
   --multifuncdef
   --multios
   --nomatch
   --notify
   --nullglob
   --numericglobsort
   --octalzeroes
   --overstrike
   --pathdirs
   --pathscript
   --pipefail
   --posixaliases
   --posixargzero
   --posixbuiltins
   --posixcd
   --posixidentifiers
   --posixjobs
   --posixstrings
   --posixtraps
   --printeightbit
   --printexitvalue
   --privileged
   --promptbang
   --promptcr
   --promptpercent
   --promptsp
   --promptsubst
   --pushdignoredups
   --pushdminus
   --pushdsilent
   --pushdtohome
   --rcexpandparam
   --rcquotes
   --rcs
   --recexact
   --rematchpcre
   --restricted
   --rmstarsilent
   --rmstarwait
   --sharehistory
   --shfileexpansion
   --shglob
   --shinstdin
   --shnullcmd
   --shoptionletters
   --shortloops
   --shortrepeat
   --shwordsplit
   --singlecommand
   --singlelinezle
   --sourcetrace
   --sunkeyboardhack
   --transientrprompt
   --trapsasync
   --typesetsilent
   --typesettounset
   --unset
   --verbose
   --vi
   --warncreateglobal
   --warnnestedvar
   --xtrace
   --zle
 
 Option aliases:
   --braceexpand            equivalent to --no-ignorebraces
   --dotglob                equivalent to --globdots
   --hashall                equivalent to --hashcmds
   --histappend             equivalent to --appendcreate
   --histexpand             equivalent to --badpattern
   --log                    equivalent to --no-histnofunctions
   --mailwarn               equivalent to --mailwarning
   --onecmd                 equivalent to --singlecommand
   --physical               equivalent to --cdsilent
   --promptvars             equivalent to --promptsubst
   --stdin                  equivalent to --shinstdin
   --trackall               equivalent to --hashcmds
 
 Option letters:
   -0    equivalent to --completeinword
   -1    equivalent to --printexitvalue
   -2    equivalent to --no-autoresume
   -3    equivalent to --no-nomatch
   -4    equivalent to --globdots
   -5    equivalent to --notify
   -6    equivalent to --beep
   -7    equivalent to --ignoreeof
   -8    equivalent to --markdirs
   -9    equivalent to --autocontinue
   -B    equivalent to --no-bashrematch
   -C    equivalent to --no-checkjobs
   -D    equivalent to --pushdtohome
   -E    equivalent to --pushdsilent
   -F    equivalent to --no-glob
   -G    equivalent to --nullglob
   -H    equivalent to --rmstarsilent
   -I    equivalent to --ignorebraces
   -J    equivalent to --appendhistory
   -K    equivalent to --no-badpattern
   -L    equivalent to --sunkeyboardhack
   -M    equivalent to --singlelinezle
   -N    equivalent to --autoparamslash
   -O    equivalent to --continueonerror
   -P    equivalent to --rcexpandparam
   -Q    equivalent to --pathdirs
   -R    equivalent to --longlistjobs
   -S    equivalent to --recexact
   -T    equivalent to --cbases
   -U    equivalent to --mailwarning
   -V    equivalent to --no-promptcr
   -W    equivalent to --autoremoveslash
   -X    equivalent to --listtypes
   -Y    equivalent to --menucomplete
   -Z    equivalent to --zle
   -a    equivalent to --allexport
   -d    equivalent to --no-globalrcs
   -e    equivalent to --errexit
   -f    equivalent to --no-rcs
   -g    equivalent to --histignorespace
   -h    equivalent to --histignoredups
   -i    equivalent to --interactive
   -k    equivalent to --interactivecomments
   -l    equivalent to --login
   -m    equivalent to --monitor
   -n    equivalent to --no-exec
   -p    equivalent to --privileged
   -r    equivalent to --restricted
   -s    equivalent to --shinstdin
   -t    equivalent to --singlecommand
   -u    equivalent to --no-unset
   -v    equivalent to --verbose
   -w    equivalent to --cdsilent
   -x    equivalent to --xtrace
   -y    equivalent to --shwordsplit
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
