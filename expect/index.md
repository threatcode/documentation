---
Title: expect
Homepage: https://core.tcl.tk/expect/
Repository: https://salsa.debian.org/tcltk-team/expect
Architectures: any
Version: 5.45.4-2
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### expect
 
  Expect is a tool for automating interactive applications according to a script.
  Following the script, Expect knows what can be expected from a program and what
  the correct response should be. Expect is also useful for testing these same
  applications. And by adding Tk, you can also wrap interactive applications in
  X11 GUIs. An interpreted language provides branching and high-level control
  structures to direct the dialogue. In addition, the user can take control and
  interact directly when desired, afterward returning control to the script.
   
  This package contains the expect binary and several Expect based scripts.
 
 **Installed size:** `317 KB`  
 **How to install:** `sudo apt install expect`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libtcl8.6 
 * tcl-expect
 * tcl8.6
 {{< /spoiler >}}
 
 ##### autoexpect
 
 Generate an Expect script from watching a session
 
 ```
 root@kali:~# man autoexpect
 AUTOEXPECT(1)               General Commands Manual              AUTOEXPECT(1)
 
 NAME
        autoexpect - generate an Expect script from watching a session
 
 SYNOPSIS
        autoexpect [ args ] [ program args...  ]
 
 INTRODUCTION
        autoexpect  watches you interacting with another program and creates an
        Expect script that  reproduces  your  interactions.   For  straightline
        scripts,  autoexpect  saves  substantial  time  over writing scripts by
        hand.  Even if you are an Expect expert, you will find it convenient to
        use autoexpect to automate the more mindless parts of interactions.  It
        is much easier to cut/paste hunks of autoexpect scripts  together  than
        to write them from scratch.  And if you are a beginner, you may be able
        to  get  away  with learning nothing more about Expect than how to call
        autoexpect.
 
        The simplest way to use autoexpect is to call it from the command  line
        with no arguments.  For example:
 
             % autoexpect
 
        By  default,  autoexpect  spawns a shell for you.  Given a program name
        and arguments, autoexpect spawns that program.  For example:
 
             % autoexpect ftp ftp.cme.nist.gov
 
        Once your spawned program is running, interact normally.  When you have
        exited the shell (or program that you specified), autoexpect will  cre-
        ate a new script for you.  By default, autoexpect writes the new script
        to  "script.exp".  You can override this with the -f flag followed by a
        new script name.
 
        The following example runs "ftp ftp.cme.nist.gov" and  stores  the  re-
        sulting Expect script in the file "nist".
 
             % autoexpect -f nist ftp ftp.cme.nist.gov
 
        It  is  important  to  understand  that autoexpect does not guarantee a
        working script because it necessarily has to guess about certain things
        - and occasionally it guesses wrong.  However, it is usually very  easy
        to identify and fix these problems.  The typical problems are:
 
               o   Timing.   A  surprisingly large number of programs (rn, ksh,
                   zsh, telnet, etc.) and devices (e.g.,  modems)  ignore  key-
                   strokes  that  arrive  "too  quickly" after prompts.  If you
                   find your new script hanging up at one spot,  try  adding  a
                   short sleep just before the previous send.
 
                   You  can  force  this  behavior throughout by overriding the
                   variable "force_conservative" near the beginning of the gen-
                   erated script.  This "conservative"  mode  makes  autoexpect
                   automatically  pause  briefly (one tenth of a second) before
                   sending each character.  This pacifies every program I  know
                   of.
 
                   This conservative mode is useful if you just want to quickly
                   reassure  yourself  that  the problem is a timing one (or if
                   you really don't care about how fast the script runs).  This
                   same mode can be forced before script  generation  by  using
                   the -c flag.
 
                   Fortunately, these timing spots are rare.  For example, tel-
                   net  ignores  characters  only after entering its escape se-
                   quence.  Modems only  ignore  characters  immediately  after
                   connecting  to  them for the first time.  A few programs ex-
                   hibit this behavior all the time but typically have a switch
                   to disable it.  For example, rn's -T flag disables this  be-
                   havior.
 
                   The  following  example  starts  autoexpect  in conservative
                   mode.
 
                        autoexpect -c
 
                   The -C flag defines a key to toggle conservative mode.   The
                   following  example  starts  autoexpect  (in non-conservative
                   mode) with ^L as the toggle.  (Note that the ^L  is  entered
                   literally - i.e., enter a real control-L).
 
                        autoexpect -C ^L
 
                   The following example starts autoexpect in conservative mode
                   with ^L as the toggle.
 
                        autoexpect -c -C ^L
 
               o   Echoing.  Many program echo characters.  For example, if you
                   type "more" to a shell, what autoexpect actually sees is:
 
                        you typed 'm',
                        computer typed 'm',
                        you typed 'o',
                        computer typed 'o',
                        you typed 'r',
                        computer typed 'r',
                        ...
 
                   Without  specific knowledge of the program, it is impossible
                   to know if you are waiting to see each character echoed  be-
                   fore  typing  the next.  If autoexpect sees characters being
                   echoed, it assumes that it can send  them  all  as  a  group
                   rather  than  interleaving  them the way they originally ap-
                   peared.  This makes the script more pleasant to read.   How-
                   ever, it could conceivably be incorrect if you really had to
                   wait to see each character echoed.
 
               o   Change.   Autoexpect records every character from the inter-
                   action in the script.  This is desirable  because  it  gives
                   you  the  ability to make judgements about what is important
                   and what can be replaced with a pattern match.
 
                   On the other hand, if you use commands whose output  differs
                   from  run  to run, the generated scripts are not going to be
                   correct.  For example, the "date"  command  always  produces
                   different  output.   So using the date command while running
                   autoexpect is a sure way to produce a script that  will  re-
                   quire editing in order for it to work.
 
                   The  -p  flag  puts  autoexpect into "prompt mode".  In this
                   mode, autoexpect will only look for the  the  last  line  of
                   program  output - which is usually the prompt.  This handles
                   the date problem (see above) and most others.
 
                   The following example starts autoexpect in prompt mode.
 
                        autoexpect -p
 
                   The -P flag defines a key to toggle prompt mode.   The  fol-
                   lowing  example  starts autoexpect (in non-prompt mode) with
                   ^P as the toggle.  Note that the ^P is entered  literally  -
                   i.e., enter a real control-P.
 
                        autoexpect -P ^P
 
                   The  following example starts autoexpect in prompt mode with
                   ^P as the toggle.
 
                        autoexpect -p -P ^P
 
 OTHER FLAGS
        The -quiet flag disables informational messages produced by autoexpect.
 
        The -Q flag names a quote character which can be used to enter  charac-
        ters  that  autoexpect would otherwise consume because they are used as
        toggles.
 
        The following example shows a number of flags with quote used  to  pro-
        vide a way of entering the toggles literally.
 
             autoexpect -P ^P -C ^L -Q ^Q
 
 STYLE
        I  don't  know if there is a "style" for Expect programs but autoexpect
        should definitely not be held up as any model of style.   For  example,
        autoexpect  uses  features of Expect that are intended specifically for
        computer-generated scripting.  So don't try to faithfully write scripts
        that appear as if they were generated by autoexpect.  This is not  use-
        ful.
 
        On  the  other hand, autoexpect scripts do show some worthwhile things.
        For example, you can see how any string must be quoted in order to  use
        it in a Tcl script simply by running the strings through autoexpect.
 
 SEE ALSO
        "Exploring  Expect: A Tcl-Based Toolkit for Automating Interactive Pro-
        grams" by Don Libes, O'Reilly and Associates, January 1995.
 
 AUTHOR
        Don Libes, National Institute of Standards and Technology
 
        expect and autoexpect are in the public domain.  NIST and I  would  ap-
        preciate credit if these programs or parts of them are used.
 
                                  30 June 1995                    AUTOEXPECT(1)
 ```
 
 - - -
 
 ##### autopasswd
 
 
 ```
 root@kali:~# autopasswd -h
 spawn passwd -h
 Usage: passwd [options] [LOGIN]
 
 Options:
   -a, --all                     report password status on all accounts
   -d, --delete                  delete the password for the named account
   -e, --expire                  force expire the password for the named account
   -h, --help                    display this help message and exit
   -k, --keep-tokens             change password only if expired
   -i, --inactive INACTIVE       set password inactive after expiration
                                 to INACTIVE
   -l, --lock                    lock the password of the named account
   -n, --mindays MIN_DAYS        set minimum number of days before password
                                 change to MIN_DAYS
   -q, --quiet                   quiet mode
   -r, --repository REPOSITORY   change password in REPOSITORY repository
   -R, --root CHROOT_DIR         directory to chroot into
   -S, --status                  report password status on the named account
   -u, --unlock                  unlock the password of the named account
   -w, --warndays WARN_DAYS      set expiration warning days to WARN_DAYS
   -x, --maxdays MAX_DAYS        set maximum number of days before password
                                 change to MAX_DAYS
 
 ```
 
 - - -
 
 ##### cryptdir
 
 Encrypt/decrypt all files in a directory
 
 ```
 root@kali:~# cryptdir -h
 This example requires the mcrypt package.
 ```
 
 - - -
 
 ##### decryptdir
 
 Encrypt/decrypt all files in a directory
 
 ```
 root@kali:~# decryptdir -h
 This example requires the mcrypt package.
 ```
 
 - - -
 
 ##### dislocate
 
 Expect_disconnect and reconnect processes
 Disconnect and reconnect processes
 
 ```
 root@kali:~# dislocate -h
 bad flag "-h": must be -console, -ignore, -leaveopen, -noecho, -nottycopy, -nottyinit, -open, or -pty
     while executing
 "spawn -h"
     ("eval" body line 1)
     invoked from within
 "eval spawn $argv"
     (procedure "child" line 11)
     invoked from within
 "child $datearg $argv"
     invoked from within
 "if {$argc} {
     # initial creation occurs before fork because if we do it after
     # then either the child or the parent may have to spin retrying
  ..."
     (file "/usr/bin/dislocate" line 264)
 Killed
 ```
 
 - - -
 
 ##### expect
 
 Programmed dialogue with interactive programs, Version 5
 Programmed dialogue with interactive programs, Version 5
 
 ```
 root@kali:~# expect -h
 expect: invalid option -- 'h'
 usage: expect [-div] [-c cmds] [[-f] cmdfile] [args]
 ```
 
 - - -
 
 ##### expect_autoexpect
 
 Generate an Expect script from watching a session
 
 ```
 root@kali:~# man expect_autoexpect
 AUTOEXPECT(1)               General Commands Manual              AUTOEXPECT(1)
 
 NAME
        autoexpect - generate an Expect script from watching a session
 
 SYNOPSIS
        autoexpect [ args ] [ program args...  ]
 
 INTRODUCTION
        autoexpect  watches you interacting with another program and creates an
        Expect script that  reproduces  your  interactions.   For  straightline
        scripts,  autoexpect  saves  substantial  time  over writing scripts by
        hand.  Even if you are an Expect expert, you will find it convenient to
        use autoexpect to automate the more mindless parts of interactions.  It
        is much easier to cut/paste hunks of autoexpect scripts  together  than
        to write them from scratch.  And if you are a beginner, you may be able
        to  get  away  with learning nothing more about Expect than how to call
        autoexpect.
 
        The simplest way to use autoexpect is to call it from the command  line
        with no arguments.  For example:
 
             % autoexpect
 
        By  default,  autoexpect  spawns a shell for you.  Given a program name
        and arguments, autoexpect spawns that program.  For example:
 
             % autoexpect ftp ftp.cme.nist.gov
 
        Once your spawned program is running, interact normally.  When you have
        exited the shell (or program that you specified), autoexpect will  cre-
        ate a new script for you.  By default, autoexpect writes the new script
        to  "script.exp".  You can override this with the -f flag followed by a
        new script name.
 
        The following example runs "ftp ftp.cme.nist.gov" and  stores  the  re-
        sulting Expect script in the file "nist".
 
             % autoexpect -f nist ftp ftp.cme.nist.gov
 
        It  is  important  to  understand  that autoexpect does not guarantee a
        working script because it necessarily has to guess about certain things
        - and occasionally it guesses wrong.  However, it is usually very  easy
        to identify and fix these problems.  The typical problems are:
 
               o   Timing.   A  surprisingly large number of programs (rn, ksh,
                   zsh, telnet, etc.) and devices (e.g.,  modems)  ignore  key-
                   strokes  that  arrive  "too  quickly" after prompts.  If you
                   find your new script hanging up at one spot,  try  adding  a
                   short sleep just before the previous send.
 
                   You  can  force  this  behavior throughout by overriding the
                   variable "force_conservative" near the beginning of the gen-
                   erated script.  This "conservative"  mode  makes  autoexpect
                   automatically  pause  briefly (one tenth of a second) before
                   sending each character.  This pacifies every program I  know
                   of.
 
                   This conservative mode is useful if you just want to quickly
                   reassure  yourself  that  the problem is a timing one (or if
                   you really don't care about how fast the script runs).  This
                   same mode can be forced before script  generation  by  using
                   the -c flag.
 
                   Fortunately, these timing spots are rare.  For example, tel-
                   net  ignores  characters  only after entering its escape se-
                   quence.  Modems only  ignore  characters  immediately  after
                   connecting  to  them for the first time.  A few programs ex-
                   hibit this behavior all the time but typically have a switch
                   to disable it.  For example, rn's -T flag disables this  be-
                   havior.
 
                   The  following  example  starts  autoexpect  in conservative
                   mode.
 
                        autoexpect -c
 
                   The -C flag defines a key to toggle conservative mode.   The
                   following  example  starts  autoexpect  (in non-conservative
                   mode) with ^L as the toggle.  (Note that the ^L  is  entered
                   literally - i.e., enter a real control-L).
 
                        autoexpect -C ^L
 
                   The following example starts autoexpect in conservative mode
                   with ^L as the toggle.
 
                        autoexpect -c -C ^L
 
               o   Echoing.  Many program echo characters.  For example, if you
                   type "more" to a shell, what autoexpect actually sees is:
 
                        you typed 'm',
                        computer typed 'm',
                        you typed 'o',
                        computer typed 'o',
                        you typed 'r',
                        computer typed 'r',
                        ...
 
                   Without  specific knowledge of the program, it is impossible
                   to know if you are waiting to see each character echoed  be-
                   fore  typing  the next.  If autoexpect sees characters being
                   echoed, it assumes that it can send  them  all  as  a  group
                   rather  than  interleaving  them the way they originally ap-
                   peared.  This makes the script more pleasant to read.   How-
                   ever, it could conceivably be incorrect if you really had to
                   wait to see each character echoed.
 
               o   Change.   Autoexpect records every character from the inter-
                   action in the script.  This is desirable  because  it  gives
                   you  the  ability to make judgements about what is important
                   and what can be replaced with a pattern match.
 
                   On the other hand, if you use commands whose output  differs
                   from  run  to run, the generated scripts are not going to be
                   correct.  For example, the "date"  command  always  produces
                   different  output.   So using the date command while running
                   autoexpect is a sure way to produce a script that  will  re-
                   quire editing in order for it to work.
 
                   The  -p  flag  puts  autoexpect into "prompt mode".  In this
                   mode, autoexpect will only look for the  the  last  line  of
                   program  output - which is usually the prompt.  This handles
                   the date problem (see above) and most others.
 
                   The following example starts autoexpect in prompt mode.
 
                        autoexpect -p
 
                   The -P flag defines a key to toggle prompt mode.   The  fol-
                   lowing  example  starts autoexpect (in non-prompt mode) with
                   ^P as the toggle.  Note that the ^P is entered  literally  -
                   i.e., enter a real control-P.
 
                        autoexpect -P ^P
 
                   The  following example starts autoexpect in prompt mode with
                   ^P as the toggle.
 
                        autoexpect -p -P ^P
 
 OTHER FLAGS
        The -quiet flag disables informational messages produced by autoexpect.
 
        The -Q flag names a quote character which can be used to enter  charac-
        ters  that  autoexpect would otherwise consume because they are used as
        toggles.
 
        The following example shows a number of flags with quote used  to  pro-
        vide a way of entering the toggles literally.
 
             autoexpect -P ^P -C ^L -Q ^Q
 
 STYLE
        I  don't  know if there is a "style" for Expect programs but autoexpect
        should definitely not be held up as any model of style.   For  example,
        autoexpect  uses  features of Expect that are intended specifically for
        computer-generated scripting.  So don't try to faithfully write scripts
        that appear as if they were generated by autoexpect.  This is not  use-
        ful.
 
        On  the  other hand, autoexpect scripts do show some worthwhile things.
        For example, you can see how any string must be quoted in order to  use
        it in a Tcl script simply by running the strings through autoexpect.
 
 SEE ALSO
        "Exploring  Expect: A Tcl-Based Toolkit for Automating Interactive Pro-
        grams" by Don Libes, O'Reilly and Associates, January 1995.
 
 AUTHOR
        Don Libes, National Institute of Standards and Technology
 
        expect and autoexpect are in the public domain.  NIST and I  would  ap-
        preciate credit if these programs or parts of them are used.
 
                                  30 June 1995                    AUTOEXPECT(1)
 ```
 
 - - -
 
 ##### expect_autopasswd
 
 
 ```
 root@kali:~# expect_autopasswd -h
 spawn passwd -h
 Usage: passwd [options] [LOGIN]
 
 Options:
   -a, --all                     report password status on all accounts
   -d, --delete                  delete the password for the named account
   -e, --expire                  force expire the password for the named account
   -h, --help                    display this help message and exit
   -k, --keep-tokens             change password only if expired
   -i, --inactive INACTIVE       set password inactive after expiration
                                 to INACTIVE
   -l, --lock                    lock the password of the named account
   -n, --mindays MIN_DAYS        set minimum number of days before password
                                 change to MIN_DAYS
   -q, --quiet                   quiet mode
   -r, --repository REPOSITORY   change password in REPOSITORY repository
   -R, --root CHROOT_DIR         directory to chroot into
   -S, --status                  report password status on the named account
   -u, --unlock                  unlock the password of the named account
   -w, --warndays WARN_DAYS      set expiration warning days to WARN_DAYS
   -x, --maxdays MAX_DAYS        set maximum number of days before password
                                 change to MAX_DAYS
 
 ```
 
 - - -
 
 ##### expect_cryptdir
 
 Encrypt/decrypt all files in a directory
 
 ```
 root@kali:~# expect_cryptdir -h
 This example requires the mcrypt package.
 ```
 
 - - -
 
 ##### expect_decryptdir
 
 Encrypt/decrypt all files in a directory
 
 ```
 root@kali:~# expect_decryptdir -h
 This example requires the mcrypt package.
 ```
 
 - - -
 
 ##### expect_dislocate
 
 Disconnect and reconnect processes
 
 ```
 root@kali:~# expect_dislocate -h
 bad flag "-h": must be -console, -ignore, -leaveopen, -noecho, -nottycopy, -nottyinit, -open, or -pty
     while executing
 "spawn -h"
     ("eval" body line 1)
     invoked from within
 "eval spawn $argv"
     (procedure "child" line 11)
     invoked from within
 "child $datearg $argv"
     invoked from within
 "if {$argc} {
     # initial creation occurs before fork because if we do it after
     # then either the child or the parent may have to spin retrying
  ..."
     (file "/usr/bin/expect_dislocate" line 264)
 Killed
 ```
 
 - - -
 
 ##### expect_ftp-rfc
 
 
 ```
 root@kali:~# expect_ftp-rfc -h
 spawn ftp ftp.uu.net
 ```
 
 - - -
 
 ##### expect_kibitz
 
 Allow two people to interact with one shell
 
 ```
 root@kali:~# man expect_kibitz
 KIBITZ(1)                   General Commands Manual                  KIBITZ(1)
 
 NAME
        kibitz - allow two people to interact with one shell
 
 SYNOPSIS
        kibitz [ kibitz-args ] user [ program program-args...  ]
        kibitz [ kibitz-args ] user@host [ program program-args...  ]
 
 INTRODUCTION
        kibitz  allows  two (or more) people to interact with one shell (or any
        arbitrary program).  Uses include:
 
               o   A novice user can ask an expert user for help.   Using  kib-
                   itz,  the  expert  can see what the user is doing, and offer
                   advice or show how to do it right.
 
               o   By running kibitz and then starting  a  full-screen  editor,
                   people  may  carry out a conversation, retaining the ability
                   to scroll backwards, save the entire conversation,  or  even
                   edit it while in progress.
 
               o   People  can team up on games, document editing, or other co-
                   operative tasks where each person has  strengths  and  weak-
                   nesses that complement one another.
 
 USAGE
        To  start  kibitz,  user1  runs kibitz with the argument of the user to
        kibitz.  For example:
 
             kibitz user2
 
        kibitz starts a new shell (or another program, if given on the  command
        line),  while  prompting  user2 to run kibitz.  If user2 runs kibitz as
        directed, the keystrokes of both users become the input of  the  shell.
        Similarly, both users receive the output from the shell.
 
        To terminate kibitz it suffices to terminate the shell itself.  For ex-
        ample,  if either user types ^D (and the shell accepts this to be EOF),
        the shell terminates followed by kibitz.
 
        Normally, all characters are passed uninterpreted.  However, if the es-
        cape character (described when kibitz starts) is issued, the  user  may
        talk  directly to the kibitz interpreter.  Any Expect(1) or Tcl(3) com-
        mands may be given.  Also, job control may be used while in the  inter-
        preter, to, for example, suspend or restart kibitz.
 
        Various  processes  can  provide various effects.  For example, you can
        emulate a two-way write(1) session with the command:
 
             kibitz user2 sleep 1000000
 
 ARGUMENTS
        kibitz takes arguments, these should also be separated by whitespace.
 
        The -noproc flag runs kibitz with no  process  underneath.   Characters
        are  passed  to the other kibitz.  This is particularly useful for con-
        necting multiple interactive processes together.  In this mode, charac-
        ters are not echoed back to the typist.
 
        -noescape disables the escape character.
 
        -escape char sets the escape character.  The default  escape  character
        is ^].
 
        -silent  turns off informational messages describing what kibitz is do-
        ing to initiate a connection.
 
        -tty ttyname defines the tty to which the invitation should be sent.
 
        If you start kibitz to user2 on a remote computer,  kibitz  performs  a
        rlogin  to  the  remote  computer  with your current username. The flag
        -proxy username causes rlogin to use  username  for  the  remote  login
        (e.g. if your account on the remote computer has a different username).
        If the -proxy flag is not given, kibitz tries to determine your current
        username  by  (in that order) inspecting the environment variables USER
        and LOGNAME, then by using the commands whoami and logname.
 
        The arguments -noescape and -escape can also be  given  by  user2  when
        prompted to run kibitz.
 
 MORE THAN TWO USERS
        The  current  implementation  of kibitz explicitly understands only two
        users, however, it is nonetheless possible to have a  three  (or  more)
        -way  kibitz,  by kibitzing another kibitz.  For example, the following
        command runs kibitz with the current user, user2, and user3:
 
             % kibitz user2 kibitz user3
 
        Additional users may be added by simply appending  more  "kibitz  user"
        commands.
 
        The xkibitz script is similar to kibitz but supports the ability to add
        additional users (and drop them) dynamically.
 
 CAVEATS
        kibitz  assumes the 2nd user has the same terminal type and size as the
        1st user.  If this assumption is incorrect, graphical programs may dis-
        play oddly.
 
        kibitz handles character graphics, but cannot handle  bitmapped  graph-
        ics.  Thus,
 
             % xterm -e kibitz    will work
             % kibitz xterm       will not work
 
        However,  you can get the effect of the latter command by using xkibitz
        (see SEE ALSO below).  kibitz uses the  same  permissions  as  used  by
        rlogin,  rsh,  etc.   Thus,  you  can only kibitz to users at hosts for
        which you can rlogin.  Similarly, kibitz will prompt for a password  on
        the remote host if rlogin would.
 
        If  you  kibitz  to  users at remote hosts, kibitz needs to distinguish
        your prompt from other things that may precede it during login.   (Ide-
        ally,  the end of it is preferred but any part should suffice.)  If you
        have an unusual prompt, set the environment variable  EXPECT_PROMPT  to
        an egrep(1)-style regular expression.  Brackets should be preceded with
        one  backslash  in  ranges, and three backslashes for literal brackets.
        The default prompt r.e. is "($|%|#) ".
 
        kibitz requires the kibitz program on both hosts.  kibitz requires  ex-
        pect(1).
 
        By  comparison,  the  xkibitz script uses the X authorization mechanism
        for inter-host communication so it does not need  to  login,  recognize
        your  prompt,  or  require  kibitz on the remote host.  It does however
        need permission to access the other X servers.
 
 BUGS
        An early version of Sun's tmpfs had a bug in it that causes  kibitz  to
        blow  up.   If  kibitz reports "error flushing ...: Is a directory" ask
        Sun for patch #100174.
 
        If your Expect is not compiled with multiple-process support (i.e., you
        do not have a working select or poll), you will not be able to run kib-
        itz.
 
 ENVIRONMENT
        The environment variable SHELL is used to determine the shell to start,
        if no other program is given on the command line.
 
        If the environment variable EXPECT_PROMPT exists, it is taken as a reg-
        ular expression which matches the end of your login  prompt  (but  does
        not otherwise occur while logging in). See also CAVEATS above.
 
        If the environment variables USER or LOGNAME are defined, they are used
        to  determine  the current user name for a kibitz to a remote computer.
        See description of the -proxy option in ARGUMENTS above.
 
 SEE ALSO
        Tcl(3), libexpect(3), xkibitz(1)
        "Exploring Expect: A Tcl-Based Toolkit for Automating Interactive  Pro-
        grams" by Don Libes, O'Reilly and Associates, January 1995.
        "Kibitz  -  Connecting  Multiple Interactive Programs Together", by Don
        Libes, Software - Practice & Experience, John Wiley & Sons,  West  Sus-
        sex, England, Vol. 23, No. 5, May, 1993.
 
 AUTHOR
        Don Libes, National Institute of Standards and Technology
 
        kibitz  is in the public domain.  NIST and I would appreciate credit if
        this program or parts of it are used.
 
                                 19 October 1994                      KIBITZ(1)
 ```
 
 - - -
 
 ##### expect_lpunlock
 
 
 ```
 root@kali:~# expect_lpunlock -h
 spawn ed /etc/printcap
 ```
 
 - - -
 
 ##### expect_mkpasswd
 
 Generate new password, optionally apply it to a user
 
 ```
 root@kali:~# expect_mkpasswd -h
 3pLTp3!io
 ```
 
 - - -
 
 ##### expect_multixterm
 
 Drive multiple xterms separately or together
 
 ```
 root@kali:~# man expect_multixterm
 MULTIXTERM(1)               General Commands Manual              MULTIXTERM(1)
 
 NAME
        multixterm - drive multiple xterms separately or together
 
 SYNOPSIS
        multixterm [ args ]
 
 DESCRIPTION
        Multixterm creates multiple xterms that can be driven together or sepa-
        rately.
 
        In  its simplest form, multixterm is run with no arguments and commands
        are interactively entered in the first entry field.  Press  return  (or
        click  the  "new xterm" button) to create a new xterm running that com-
        mand.
 
        Keystrokes in the "stdin window" are redirected to all  xterms  started
        by  multixterm.   xterms may be driven separately simply by focusing on
        them.
 
        The stdin window must have the focus for keystrokes to be sent  to  the
        xterms.   When  it  has the focus, the color changes to aquamarine.  As
        characters are entered, the color changes to green for a second.   This
        provides feedback since characters are not echoed in the stdin window.
 
        Typing  in  the  stdin  window  while holding down the alt or meta keys
        sends an escape character before the typed characters.   This  provides
        support for programs such as emacs.
 
 ARGUMENTS
               -xa The  optional  -xa  argument  indicates arguments to pass to
                   xterm.
 
               -xc The optional -xc argument indicates a command to be  run  in
                   each  named xterm (see -xn).  With no -xc argument, the com-
                   mand is the current shell.
 
               -xd The optional -xd argument indicates a  directory  to  search
                   for  files  that will appear in the Files menu.  By default,
                   the directory is: ~/lib/multixterm
 
               -xf The optional -xf argument indicates a file  to  be  read  at
                   startup.  See FILES below for more info.
 
               -xn The  optional  -xn argument indicates a name for each xterm.
                   This name will also be substituted for any %n in the command
                   argument (see -xc).
 
               -xv The optional -xv flag puts multixterm into  a  verbose  mode
                   where it will describe some of the things it is doing inter-
                   nally.  The verbose output is not intended to be understand-
                   able to anyone but the author.
 
        Less  common  options may be changed by the startup file (see FILES be-
        low).
 
        All the usual X and wish flags are supported (i.e.,  -display,  -name).
        There are so many of them that to avoid colliding and make them easy to
        remember, all the multixterm flags begin with -x.
 
        If  any  arguments  do  not match the flags above, the remainder of the
        command line is made available for user processing.   By  default,  the
        remainder  is  used  as a list of xterm names in the style of -xn.  The
        default behavior may be changed using the .multixtermrc file  (see  DOT
        FILE below).
 
 EXAMPLE COMMAND LINE ARGUMENTS
        The  following command line starts up two xterms using ssh to the hosts
        bud and dexter.
 
             multixterm -xc "ssh %n" bud dexter
 
 FILES
        Command files may be used to drive or initialize multixterm.  The  File
        menu  may be used to invoke other files.  If files exist in the command
        file directory (see -xd above), they will  appear  in  the  File  menu.
        Files  may also be loaded by using File->Open.  Any filename is accept-
        able but the File->Open browser defaults to files with a .mxt suffix.
 
        Files are written in Tcl and may change any  variables  or  invoke  any
        procedures.   The  primary  variables  of interest are 'xtermCmd' which
        identifies the command (see -xc) and 'xtermNames' which is  a  list  of
        names  (see  -xn).  The procedure xtermStartAll, starts xterms for each
        name in the list.  Other variables and procedures may be discovered  by
        examining multixterm itself.
 
 EXAMPLE FILE
        The  following  file does the same thing as the earlier example command
        line:
 
             # start two xterms connected to bud and dexter
             set xtermCmd "ssh %n"
             set xtermNames {bud dexter}
             xtermStartAll
 
 DOT FILE
        At startup, multixterm reads ~/.multixtermrc if present.  This is simi-
        lar to the command files (see FILES above)  except  that  .multixtermrc
        may  not  call xtermStartAll.  Instead it is called implicitly, similar
        to the way that it is implicit in the command line use of -xn.
 
        The following example .multixtermrc file makes every xterm run  ssh  to
        the hosts named on the command line.
 
             set xtermCmd "ssh %n"
 
        Then multixterm could be called simply:
 
             multixterm bud dexter
 
        If  any command-line argument does not match a multixterm flag, the re-
        mainder of the command line is made available to .multixtermrc  in  the
        argv  variable.  If argv is non-empty when .multixtermrc returns, it is
        assigned to xtermNames unless xtermNames is non-empty  in  which  case,
        the content of argv is ignored.
 
        Commands  from  multixterm are evaluated early in the initialization of
        multixterm.  Anything that must be  done  late  in  the  initialization
        (such  as adding additional bindings to the user interface) may be done
        by putting the commands inside a procedure called "initLate".
 
 MENUS
        Except as otherwise noted, the menus are self-explanatory.  Some of the
        menus have dashed lines as the first entry.   Clicking  on  the  dashed
        lines will "tear off" the menus.
 
 USAGE SUGGESTION - ALIASES AND COMMAND FILES
        Aliases may be used to store lengthy command-line invocations.  Command
        files  can be also be used to store such invocations as well as provid-
        ing a convenient way to share configurations.
 
        Tcl is a general-purpose language.  Thus multixterm command  files  can
        be extremely flexible, such as loading hostnames from other programs or
        files  that may change from day-to-day.  In addition, command files can
        be used for other purposes.  For example, command files may be used  to
        prepared common canned interaction sequences.  For example, the command
        to send the same string to all xterms is:
 
            xtermSend "a particularly long string"
 
        The  File  menu  (torn-off)  makes canned sequences particularly conve-
        nient.  Interactions could also be bound to a mouse button,  keystroke,
        or added to a menu via the .multixtermrc file.
 
        The  following .multixtermrc causes tiny xterms to tile across and down
        the screen.  (You may have to adjust the parameters for  your  screen.)
        This can be very helpful when dealing with large numbers of xterms.
 
            set yPos 0
            set xPos 0
 
            trace variable xtermArgs r traceArgs
 
            proc traceArgs {args} {
                global xPos yPos
                set ::xtermArgs "-geometry 80x12+$xPos+$yPos -font 6x10"
                if {$xPos} {
                    set xPos 0
                    incr yPos 145
                    if {$yPos > 800} {set yPos 0}
                } else {
                    set xPos 500
                }
            }
 
        The  xtermArgs variable in the code above is the variable corresponding
        to the -xa argument.
 
        xterms can be also be created directly.   The  following  command  file
        creates three xterms overlapped horizontally:
 
            set xPos 0
            foreach name {bud dexter hotdog} {
                set ::xtermArgs "-geometry 80x12+$xPos+0 -font 6x10"
                set ::xtermNames $name
                xtermStartAll
                incr xPos 300
            }
 
 USAGE SUGGESTION - SELECTING HOSTS BY NICKNAME
        The  following  .multixtermrc  shows an example of changing the default
        handling of the arguments from hostnames to a filename containing host-
        names:
 
             set xtermNames [exec cat $argv]
 
        The following is a variation, retrieving the host  names  from  the  yp
        database:
 
             set xtermNames [exec ypcat $argv]
 
        The following hardcodes two sets of hosts, so that you can call multix-
        term with either "cluster1" or "cluster2":
 
             switch $argv {
                    cluster1 {
                        set xtermNames "bud dexter"
                    }
                    cluster2 {
                        set xtermNames "frank hotdog weiner"
                    }
                }
 
 COMPARE/CONTRAST
        It  is  worth  comparing  multixterm to xkibitz.  Multixterm connects a
        separate process to each xterm.  xkibitz connects the same  process  to
        each xterm.
 
 LIMITATIONS
        Multixterm  provides no way to remotely control scrollbars, resize, and
        most other window system related functions.
 
        Because xterm has no mechanism for propagating size information to  ex-
        ternal  processes,  particularly  for  character  graphic  applications
        (e.g., vi, emacs), you may have to manually  ensure  that  the  spawned
        process  behind  each  xterm has the correct size.  For example, if you
        create or set the xterm to a size, you may have  to  send  an  explicit
        stty  command with the correct size to the spawned process(es).  Alter-
        natively, you can add the correct size argument when an xterm  is  cre-
        ated (i.e., "-geometry 80x20").
 
        Multixterm  can  only  control  new  xterms  that multixterm itself has
        started.
 
        As a convenience, the File menu shows a limited number  of  files.   To
        show all the files, use File->Open.
 
 FILES
        $DOTDIR/.multixtermrc   initial command file
        ~/.multixtermrc         fallback command file
        ~/lib/multixterm/       default command file directory
 
 BUGS
        If  multixterm  is killed using an uncatchable kill, the xterms are not
        killed.  This appears to be a bug in xterm itself.
 
        Send/expect sequences can be done in multixterm  command  files.   How-
        ever, due to the richness of the possibilities, to document it properly
        would take more time than the author has at present.
 
 REQUIREMENTS
        Requires Expect 5.36.0 or later.
        Requires Tk 8.3.3 or later.
 
 VERSION
        This man page describes version 1.8 of multixterm.
 
        The   latest   version  of  multixterm  is  available  from  http://ex-
        pect.nist.gov/example/multixterm .  If your version of  Expect  and  Tk
        are  too old (see REQUIREMENTS above), download a new version of Expect
        from http://expect.nist.gov
 
 DATE
        April 30, 2002
 
 AUTHOR
        Don Libes <don@libes.com>
 
 LICENSE
        Multixterm is in the public domain; however the author would appreciate
        acknowledgement if multixterm or parts of it or ideas from it are used.
 
                                 16 August 2002                   MULTIXTERM(1)
 ```
 
 - - -
 
 ##### expect_passmass
 
 Change password on multiple machines
 
 ```
 root@kali:~# man expect_passmass
 PASSMASS(1)                 General Commands Manual                PASSMASS(1)
 
 NAME
        passmass - change password on multiple machines
 
 SYNOPSIS
        passmass [ host1 host2 host3 ...  ]
 
 INTRODUCTION
        Passmass changes a password on multiple machines.  If you have accounts
        on  several machines that do not share password databases, Passmass can
        help you keep them all in sync.  This, in turn, will make it easier  to
        change them more frequently.
 
        When Passmass runs, it asks you for the old and new passwords.  (If you
        are changing root passwords and have equivalencing, the old password is
        not used and may be omitted.)
 
        Passmass understands the "usual" conventions.  Additional arguments may
        be  used  for tuning.  They affect all hosts which follow until another
        argument overrides it.  For example, if you are  known  as  "libes"  on
        host1 and host2, but "don" on host3, you would say:
 
             passmass host1 host2 -user don host3
 
        Arguments are:
 
               -user
                   User  whose  password will be changed.  By default, the cur-
                   rent user is used.
 
               -rlogin
                   Use rlogin to access host.  (default)
 
               -slogin
                   Use slogin to access host.
 
               -ssh
                   Use ssh to access host.
 
               -telnet
                   Use telnet to access host.
 
               -program
 
                   Next argument is a program to run to set the password.   De-
                   fault  is "passwd".  Other common choices are "yppasswd" and
                   "set passwd" (e.g., VMS hosts).   A  program  name  such  as
                   "password  fred"  can  be used to create entries for new ac-
                   counts (when run as root).
 
               -prompt
                   Next argument is a prompt suffix pattern.  This  allows  the
                   script  to know when the shell is prompting.  The default is
                   "# " for root and "% " for non-root accounts.
 
               -timeout
                   Next argument is the number  of  seconds  to  wait  for  re-
                   sponses.   Default is 30 but some systems can be much slower
                   logging in.
 
               -su
 
                   Next argument is  1  or  0.   If  1,  you  are  additionally
                   prompted  for a root password which is used to su after log-
                   ging in.  root's password is changed rather than the user's.
                   This is useful for hosts which do not allow root to log in.
 
 HOW TO USE
        The best way to run Passmass is to put the command in a one-line  shell
        script  or alias.  Whenever you get a new account on a new machine, add
        the appropriate arguments to the command.  Then  run  it  whenever  you
        want to change your passwords on all the hosts.
 
 CAVEATS
        Using  the  same password on multiple hosts carries risks.  In particu-
        lar, if the password can be stolen, then all of your  accounts  are  at
        risk.  Thus, you should not use Passmass in situations where your pass-
        word  is  visible,  such as across a network which hackers are known to
        eavesdrop.
 
        On the other hand, if you have enough  accounts  with  different  pass-
        words,  you  may end up writing them down somewhere - and that can be a
        security problem.  Funny story: my  college  roommate  had  an  11"x13"
        piece of paper on which he had listed accounts and passwords all across
        the Internet.  This was several years worth of careful work and he car-
        ried it with him everywhere he went.  Well one day, he forgot to remove
        it  from  his jeans, and we found a perfectly blank sheet of paper when
        we took out the wash the following day!
 
 SEE ALSO
        "Exploring Expect: A Tcl-Based Toolkit for Automating Interactive  Pro-
        grams" by Don Libes, O'Reilly and Associates, January 1995.
 
 AUTHOR
        Don Libes, National Institute of Standards and Technology
 
                                 7 October 1993                     PASSMASS(1)
 ```
 
 - - -
 
 ##### expect_rftp
 
 
 ```
 root@kali:~# expect_rftp -h
 Once logged in, cd to the directory to be transferred and press:
 ~p to put the current directory from the local to the remote host
 ~g to get the current directory from the remote host to the local host
 ~l to list the current directory from the remote host
 spawn ftp -h
 ```
 
 - - -
 
 ##### expect_rlogin-cwd
 
 
 ```
 root@kali:~# expect_rlogin-cwd -h
 spawn rlogin -h
 rlogin: invalid option -- 'h'
 usage: rlogin [-8ELKd] [-e char] [-i user] [-l user] [-p port] host
 ```
 
 - - -
 
 ##### expect_timed-read
 
 
 
 - - -
 
 ##### expect_timed-run
 
 
 ```
 root@kali:~# expect_timed-run -h
 usage: spawn [spawn-args] program [program-args]
     while executing
 "spawn"
     ("eval" body line 1)
     invoked from within
 "eval spawn [lrange $argv 1 end]"
     (file "/usr/bin/expect_timed-run" line 12)
 ```
 
 - - -
 
 ##### expect_tknewsbiff
 
 Pop up a window when news appears
 
 ```
 root@kali:~# man expect_tknewsbiff
 TKNEWSBIFF(1)               General Commands Manual              TKNEWSBIFF(1)
 
 NAME
        tknewsbiff - pop up a window when news appears
 
 SYNOPSIS
        tknewsbiff [ server or config-file ]
 
 INTRODUCTION
        tknewsbiff  pops up a window when there is unread news in your favorite
        newsgroups and removes the window after you've read the news.  tknewsb-
        iff can optionally play a sound, start your newsreader, etc.
 
 SELECTING NEWSGROUPS
        By default, the configuration file ~/.tknewsbiff describes how tknewsb-
        iff behaves.  The syntax observes the usual Tcl rules -  however,  even
        if you don't know Tcl, all but the most esoteric configurations will be
        obvious.
 
        Each newsgroup (or set of newsgroups) to be watched is described by us-
        ing the "watch" command.  For example:
 
        watch dc.dining
        watch nist.*
        watch comp.unix.wizard  -threshold 3
        watch *.sources.*       -threshold 20
 
        For each newsgroup pattern, any newsgroup that matches it and which you
        are  subscribed  to (according to your newsrc file) is eligible for re-
        porting.  By default, tknewsbiff reports on the newsgroup if  there  is
        at least one unread article.  The "-threshold" flag changes the thresh-
        old  to  the following number.  For example, "-threshold 3" means there
        must be at least three articles unread before  tknewsbiff  will  report
        the newsgroup.
 
        If  no  watch commands are given (or no configuration file exists), all
        groups which are subscribed to are watched.
 
        To suppress newsgroups that would otherwise be reported, use  the  "ig-
        nore"  command.   For  example,  the  following  matches all comp.* and
        nist.* newgroups except for nist.posix or .d (discussion) groups:
 
        watch comp.*
        watch nist.*
        ignore nist.posix.*
        ignore *.d
 
        The flag "-new" describes a command to be executed when  the  newsgroup
        is  first  reported  as having unread news.  For example, the following
        lines invoke the UNIX command "play" to play a sound.
 
        watch dc.dining -new "exec play /usr/local/sounds/yumyum.au"
        watch rec.auto* -new "exec play /usr/local/sounds/vroom.au"
 
        You can cut down on the verbosity of actions  by  defining  procedures.
        For example, if you have many -new flags that all play sound files, you
        could  define  a sound procedure.  This would allow the -new specifica-
        tion to be much shorter.
 
        proc play {sound} {
             exec play /usr/local/sounds/$sound.au
        }
 
        watch dc.dining -new "play yumyum"
        watch rec.auto* -new "play vroom"
 
        As an aside, you can put an "&" at the end of an "exec" command to  get
        commands  to execute asynchronously.  However, it's probably not a good
        idea to do this when playing sound files anyway.
 
        "newsgroup" is a read-only variable which  contains  the  name  of  the
        newsgroup  that  is  being reported.  This is useful when the action is
        triggered by a pattern.  For example, the following line could run  the
        newsgroup name through a speech synthesizer:
 
        watch * -new {
             exec play herald.au
             exec speak "New news has arrived in $newsgroup."
        }
 
        The  flag  "-display" describes a command to be executed every time the
        newsgroup is reported as having unread news.  The special command "dis-
        play" is the default command.  It schedules $newsgroup to be written to
        tknewsbiff's display when it is rewritten.  For example, by  explicitly
        providing  a -display flag that omits the display command, you can dis-
        able the display of newsgroups that are already reported via -new.
 
        watch dc.dining -new {exec play yumyum.au} -display {}
 
        If you want to execute an action repeatedly and still display the news-
        group in the default manner, explicitly invoke the display command  via
        the -display flag.  For example:
 
        watch *security* -display {
             exec play red-alert.au
             display
        }
 
        Actions  associated  with the -new and -display flags are executed only
        once for each matching newsgroup.  The command executed is the one  as-
        sociated  with the first pattern in the configuration file that matches
        and observes the given threshold.
 
        Any command that is simply listed in the configuration file is executed
        each time before the update loop  in  tknewsbiff.   The  reserved  (but
        user-defined)  procedure "user" is run immediately after the newsgroups
        are scheduled to be written to the display and before they are actually
        written.
 
        For example, suppose unread articles appear in several rec.auto  groups
        and you play the same sound for each one.  To prevent playing the sound
        several  times  in  a row, make the -new command simply set a flag.  In
        the user procedure, play the sound if the flag is set (and  then  reset
        the flag).
 
        The  user  procedure  could  also  be used to start a newsreader.  This
        would avoid the possibility of starting multiple newsreaders  just  be-
        cause  multiple newsgroups contained unread articles.  (A check should,
        of course, be made to make sure that a newsreader is not  already  run-
        ning.)
 
 MORE VARIABLES
        The following example lines show variables that can affect the behavior
        of tknewsbiff
 
        set delay          120
        set server         news.nist.gov
        set server_timeout 60
        set newsrc         ~/.newsrc
        set width          40
        set height         20
        set active_file    /usr/news/lib/active
 
        tknewsbiff  alternates  between  checking  for unread news and sleeping
        (kind of like many undergraduates).  The "delay" variable describes how
        many seconds to sleep.
 
        The "server" variable  names  an  NNTP  news-server.   The  default  is
        "news".   The "server" variable is only used if the "active_file" vari-
        able is not set.
 
        The "server_timeout" variable describes how how many  seconds  to  wait
        for a response from the server before giving up.  -1 means wait forever
        or until the server itself times out.  The default is 60 seconds.
 
        The  "newsrc" variable describes the name of your .newsrc file.  By de-
        fault, tknewsbiff looks in your home directory for a  newsrc  file.   A
        server-specific  newsrc is used if found.  For example, if you have set
        server to "cubit.nist.gov", then  tknewsbiff  looks  for  ~/.newsrc-cu-
        bit.nist.gov.   (This is the Emacs gnus convention - which is very con-
        venient when you read news from multiple  servers.)   If  there  is  no
        server-specific newsrc, tknewsbiff uses ~/.newsrc.
 
        The  "width"  variable  describes the width that tknewsbiff will use to
        display information.  If any newsgroup names are long enough, they will
        be truncated so that the article counts can still be  shown.   You  can
        manually resize the window to see what was truncated.  However, if your
        configuration file sets the width variable, the window will be restored
        to  that  size the next time that tknewsbiff checks for unread news and
        updates its display.
 
        The "height" variable describes the maximum height that tknewsbiff will
        use to display information.  If fewer newsgroups are reported, tknewsb-
        iff will shrink the window appropriately.  You can manually resize  the
        window  but  if  your  configuration file sets the height variable, the
        window will be restored to that size  the  next  time  that  tknewsbiff
        checks for unread news and updates its display.
 
        The  "active_file" variable describes the name of the news active file.
        If set, the active file is read directly in preference  to  using  NNTP
        (even  if  the  "server" variable is set).  This is particularly useful
        for testing out new configuration files since you can edit a  fake  ac-
        tive file and then click button 2 to immediately see how tknewsbiff re-
        sponds (see BUTTONS below).
 
        If  the environment variable DOTDIR is set, then its value is used as a
        directory in which to find all dotfiles instead of from the home direc-
        tory.  In particular, this affects the  tknewsbiff  configuration  file
        and  the  .newsrc file (assuming the newsrc variable is not set explic-
        itly).
 
 WATCHING DIFFERENT NEWS SERVERS
        To watch multiple servers, run tknewsbiff multiple times.   (Since  you
        need  different .newsrc files and the servers have different newsgroups
        and article numbers anyway, there is no point in trying to do this in a
        single process.)
 
        You can point tknewsbiff at a different server with an appropriate  ar-
        gument.  The argument is tried both as a configuration file name and as
        a  suffix  to the string "~/.tknewsbiff-".  So if you want to watch the
        server "kidney", store  the  tknewsbiff  configuration  information  in
        ~/.tknewsbiff-kidney".   The  following two commands will both use that
        configuration file.
 
             tknewsbiff kidney
             tknewsbiff ~/.tknewsbiff-kidney
 
        In both cases, the actual server to contact is set by the value of  the
        server variable in the configuration file.
 
        If  no  configuration file is found, the argument is used as the server
        to contact.  This allows tknewsbiff to be run with no preparation what-
        soever.
 
        If the argument is the special keyword "active" (or ends in "/active"),
        it is used as the name of an active file.  This is in turn used to ini-
        tialize the variable "active_file" so that tknewsbiff  reads  from  the
        active file directly rather than using NNTP.
 
        Creating  your own active file is a convenient way of testing your con-
        figuration file.  For example, after running the following command, you
        can repeatedly edit your active file and trigger the update-now command
        (either by pressing button 2 or setting the delay variable very low) to
        see how tknewsbiff responds.
 
        The active file must follow the format of a real active file.  The for-
        mat is one newsgroup per line.  After the newsgroup name is the  number
        of  the highest article, the lowest article.  Lastly is the letter y or
        m.  m means the newsgroup is moderated.  y means posting is allowed.
 
 WINDOW
        When unread news is found, a window is popped up.  The window lists the
        names of the newsgroups and the number of unread articles in each  (un-
        less suppressed by the -display flag).  When there is no longer any un-
        read  news,  the  window  disappears (although the process continues to
        run).
 
 BUTTONS
        Button or key bindings may be assigned by bind commands.  Feel free  to
        change them.  The default bind commands are:
 
        bind .list <1> help
        bind .list <2> update-now
        bind .list <3> unmapwindow
 
        By default button 1 (left) is bound to "help".  The help command causes
        tknewsbiff to pop up a help window.
 
        By default, button 2 (middle) is bound to "update-now".  The update-now
        command  causes  tknewsbiff  to  immediately check for unread news.  If
        your news server is slow or maintains a  very  large  number  of  news-
        groups,  or  you  have a large number of patterns in your configuration
        file, tknewsbiff can take considerable time  before  actually  updating
        the window.
 
        By  default, button 3 (right) is bound to "unmapwindow".  The unmapwin-
        dow command causes tknewsbiff to remove the window from the display un-
        til the next time it finds unread news.  (The mapwindow command  causes
        tknewsbiff to restore the window.)
 
        As an example, here is a binding to pop up an xterm and run rn when you
        hold down the shift key and press button 1 in the listing window.
 
        bind .list <Shift-1> {
             exec xterm -e rn &
        }
 
        Here  is  a  similar  binding.  However it tells rn to look only at the
        newsgroup that is under the mouse when  you  pressed  it.   (The  "dis-
        play_list" variable is described later in this man page.)
 
        bind .list <Shift-1> {
             exec xterm -e rn [lindex $display_list [.list nearest %y]] &
        }
 
 OTHER COMMANDS AND VARIABLES
        Built-in  commands already mentioned are: watch, ignore, display, help,
        update-now, unmapwindow, and mapwindow.
 
        Any Tcl and Tk command can also be given.  In particular, the  list  of
        newsgroups  is stored in the list widget ".list", and the scroll bar is
        stored in the scrollbar widget ".scroll".  So for example, if you  want
        to  change  the foreground and background colors of the newsgroup list,
        you can say:
 
             .list config -bg honeydew1 -fg orchid2
 
        These can also be controlled by the X resource database as well.   How-
        ever,  the configuration file allows arbitrarily complex commands to be
        evaluated rather than simple assignments.
 
        Certain Tcl/Tk commands can  disrupt  proper  function  of  tknewsbiff.
        These will probably be obvious to anyone who knows enough to give these
        commands  in the first place.  As a simple example, the program assumes
        the font in the list box is of fixed width.  The newsgroups will likely
        not align if you use a variable-width font.
 
        The following variables are accessible and can  be  used  for  esoteric
        uses.  All other variables are private.  Private variables and commands
        begin with "_" so you don't need to worry about accidental collisions.
 
        The array "db" is a database which maintains information about read and
        unread  news.   db($newsgroup,hi)  is  the highest article that exists.
        db($newsgroup,seen) is the highest article that you have read.
 
        A number of lists maintain interesting information. "active_list" is  a
        list  of  known  newsgroups.   "seen_list" is a list of newsgroups that
        have been seen so  far  as  the  -new  and  -display  flags  are  being
        processed.   "previous_seen_list"  is "seen_list" from the previous cy-
        cle.  "ignore_list" is  the  list  of  newsgroup  patterns  to  ignore.
        "watch_list"  is  the  list  of  newsgroup  patterns  to  watch.  "dis-
        play_list" is the list of newsgroup will be displayed at the  next  op-
        portunity.
 
 UPDATING YOUR FILES
        tknewsbiff  automatically  rereads your configuration file each time it
        wakes up to check for unread news.  To force tknewsbiff to  reread  the
        file  immediately  (such  as  if you are testing a new configuration or
        have just modified your newsrc file), press button  2  in  the  display
        (see BUTTONS above).
 
 CAVEATS
        tknewsbiff  defines the number of unread articles as the highest exist-
        ing article minus the highest article that you've read.  So  if  you've
        read the last article in the newsgroup but no others, tknewsbiff thinks
        there  are  no  unread  articles.  (It's impossible to do any better by
        reading the active file and it would be very time consuming to do  this
        more  accurately via NNTP since servers provide no efficient way of re-
        porting their own holes in the newsgroups.)  Fortunately, this  defini-
        tion is considered a feature by most people.  It allows you to read ar-
        ticles  and  then  mark  them "unread" but not have tknewsbiff continue
        telling you that they are unread.
 
 UNWARRANTED CONCERNS
        Your news administrator may wonder if many people using tknewsbiff  se-
        verely  impact  an NNTP server.  In fact, the impact is negligible even
        when the delay is very low.  To gather all the  information  it  needs,
        tknewsbiff uses a single NNTP query - it just asks for the active file.
        The NNTP server does no computation, formatting, etc, it just sends the
        file.  All the interesting processing happens locally in the tknewsbiff
        program itself.
 
 BUGS
        The man page is longer than the program.
 
 SEE ALSO
        "Exploring  Expect: A Tcl-Based Toolkit for Automating Interactive Pro-
        grams" by Don Libes, O'Reilly and Associates, January 1995.
 
 AUTHOR
        Don Libes, National Institute of Standards and Technology
 
                                 1 January 1994                   TKNEWSBIFF(1)
 ```
 
 - - -
 
 ##### expect_tkpasswd
 
 
 
 - - -
 
 ##### expect_unbuffer
 
 Unbuffer output
 
 ```
 root@kali:~# expect_unbuffer -h
 bad flag "-h": must be -console, -ignore, -leaveopen, -noecho, -nottycopy, -nottyinit, -open, or -pty
     while executing
 "spawn -noecho -h"
     ("eval" body line 1)
     invoked from within
 "eval [list spawn -noecho] $argv"
     invoked from within
 "if {[string compare [lindex $argv 0] "-p"] == 0} {
     # pipeline
     set stty_init "-echo"
     eval [list spawn -noecho] [lrange $argv 1 end]
     clo..."
     (file "/usr/bin/expect_unbuffer" line 13)
 ```
 
 - - -
 
 ##### expect_weather
 
 
 ```
 root@kali:~# expect_weather -h
 spawn telnet rainmaker.wunderground.com 3000
 Trying 35.160.169.47...
 ```
 
 - - -
 
 ##### expect_xkibitz
 
 Allow multiple people to interact in an xterm
 
 ```
 root@kali:~# expect_xkibitz -h
 bad flag "-h": must be -console, -ignore, -leaveopen, -noecho, -nottycopy, -nottyinit, -open, or -pty
     while executing
 "spawn -noecho -h"
     ("eval" body line 1)
     invoked from within
 "eval spawn -noecho $argv"
     invoked from within
 "if {[llength $argv]>0} {
     eval spawn -noecho $argv
 } else {
     spawn -noecho $env(SHELL)
 }"
     (file "/usr/bin/expect_xkibitz" line 201)
 ```
 
 - - -
 
 ##### expect_xpstat
 
 
 
 - - -
 
 ##### ftp-rfc
 
 
 ```
 root@kali:~# ftp-rfc -h
 spawn ftp ftp.uu.net
 ```
 
 - - -
 
 ##### kibitz
 
 Allow two people to interact with one shell
 
 ```
 root@kali:~# man kibitz
 KIBITZ(1)                   General Commands Manual                  KIBITZ(1)
 
 NAME
        kibitz - allow two people to interact with one shell
 
 SYNOPSIS
        kibitz [ kibitz-args ] user [ program program-args...  ]
        kibitz [ kibitz-args ] user@host [ program program-args...  ]
 
 INTRODUCTION
        kibitz  allows  two (or more) people to interact with one shell (or any
        arbitrary program).  Uses include:
 
               o   A novice user can ask an expert user for help.   Using  kib-
                   itz,  the  expert  can see what the user is doing, and offer
                   advice or show how to do it right.
 
               o   By running kibitz and then starting  a  full-screen  editor,
                   people  may  carry out a conversation, retaining the ability
                   to scroll backwards, save the entire conversation,  or  even
                   edit it while in progress.
 
               o   People  can team up on games, document editing, or other co-
                   operative tasks where each person has  strengths  and  weak-
                   nesses that complement one another.
 
 USAGE
        To  start  kibitz,  user1  runs kibitz with the argument of the user to
        kibitz.  For example:
 
             kibitz user2
 
        kibitz starts a new shell (or another program, if given on the  command
        line),  while  prompting  user2 to run kibitz.  If user2 runs kibitz as
        directed, the keystrokes of both users become the input of  the  shell.
        Similarly, both users receive the output from the shell.
 
        To terminate kibitz it suffices to terminate the shell itself.  For ex-
        ample,  if either user types ^D (and the shell accepts this to be EOF),
        the shell terminates followed by kibitz.
 
        Normally, all characters are passed uninterpreted.  However, if the es-
        cape character (described when kibitz starts) is issued, the  user  may
        talk  directly to the kibitz interpreter.  Any Expect(1) or Tcl(3) com-
        mands may be given.  Also, job control may be used while in the  inter-
        preter, to, for example, suspend or restart kibitz.
 
        Various  processes  can  provide various effects.  For example, you can
        emulate a two-way write(1) session with the command:
 
             kibitz user2 sleep 1000000
 
 ARGUMENTS
        kibitz takes arguments, these should also be separated by whitespace.
 
        The -noproc flag runs kibitz with no  process  underneath.   Characters
        are  passed  to the other kibitz.  This is particularly useful for con-
        necting multiple interactive processes together.  In this mode, charac-
        ters are not echoed back to the typist.
 
        -noescape disables the escape character.
 
        -escape char sets the escape character.  The default  escape  character
        is ^].
 
        -silent  turns off informational messages describing what kibitz is do-
        ing to initiate a connection.
 
        -tty ttyname defines the tty to which the invitation should be sent.
 
        If you start kibitz to user2 on a remote computer,  kibitz  performs  a
        rlogin  to  the  remote  computer  with your current username. The flag
        -proxy username causes rlogin to use  username  for  the  remote  login
        (e.g. if your account on the remote computer has a different username).
        If the -proxy flag is not given, kibitz tries to determine your current
        username  by  (in that order) inspecting the environment variables USER
        and LOGNAME, then by using the commands whoami and logname.
 
        The arguments -noescape and -escape can also be  given  by  user2  when
        prompted to run kibitz.
 
 MORE THAN TWO USERS
        The  current  implementation  of kibitz explicitly understands only two
        users, however, it is nonetheless possible to have a  three  (or  more)
        -way  kibitz,  by kibitzing another kibitz.  For example, the following
        command runs kibitz with the current user, user2, and user3:
 
             % kibitz user2 kibitz user3
 
        Additional users may be added by simply appending  more  "kibitz  user"
        commands.
 
        The xkibitz script is similar to kibitz but supports the ability to add
        additional users (and drop them) dynamically.
 
 CAVEATS
        kibitz  assumes the 2nd user has the same terminal type and size as the
        1st user.  If this assumption is incorrect, graphical programs may dis-
        play oddly.
 
        kibitz handles character graphics, but cannot handle  bitmapped  graph-
        ics.  Thus,
 
             % xterm -e kibitz    will work
             % kibitz xterm       will not work
 
        However,  you can get the effect of the latter command by using xkibitz
        (see SEE ALSO below).  kibitz uses the  same  permissions  as  used  by
        rlogin,  rsh,  etc.   Thus,  you  can only kibitz to users at hosts for
        which you can rlogin.  Similarly, kibitz will prompt for a password  on
        the remote host if rlogin would.
 
        If  you  kibitz  to  users at remote hosts, kibitz needs to distinguish
        your prompt from other things that may precede it during login.   (Ide-
        ally,  the end of it is preferred but any part should suffice.)  If you
        have an unusual prompt, set the environment variable  EXPECT_PROMPT  to
        an egrep(1)-style regular expression.  Brackets should be preceded with
        one  backslash  in  ranges, and three backslashes for literal brackets.
        The default prompt r.e. is "($|%|#) ".
 
        kibitz requires the kibitz program on both hosts.  kibitz requires  ex-
        pect(1).
 
        By  comparison,  the  xkibitz script uses the X authorization mechanism
        for inter-host communication so it does not need  to  login,  recognize
        your  prompt,  or  require  kibitz on the remote host.  It does however
        need permission to access the other X servers.
 
 BUGS
        An early version of Sun's tmpfs had a bug in it that causes  kibitz  to
        blow  up.   If  kibitz reports "error flushing ...: Is a directory" ask
        Sun for patch #100174.
 
        If your Expect is not compiled with multiple-process support (i.e., you
        do not have a working select or poll), you will not be able to run kib-
        itz.
 
 ENVIRONMENT
        The environment variable SHELL is used to determine the shell to start,
        if no other program is given on the command line.
 
        If the environment variable EXPECT_PROMPT exists, it is taken as a reg-
        ular expression which matches the end of your login  prompt  (but  does
        not otherwise occur while logging in). See also CAVEATS above.
 
        If the environment variables USER or LOGNAME are defined, they are used
        to  determine  the current user name for a kibitz to a remote computer.
        See description of the -proxy option in ARGUMENTS above.
 
 SEE ALSO
        Tcl(3), libexpect(3), xkibitz(1)
        "Exploring Expect: A Tcl-Based Toolkit for Automating Interactive  Pro-
        grams" by Don Libes, O'Reilly and Associates, January 1995.
        "Kibitz  -  Connecting  Multiple Interactive Programs Together", by Don
        Libes, Software - Practice & Experience, John Wiley & Sons,  West  Sus-
        sex, England, Vol. 23, No. 5, May, 1993.
 
 AUTHOR
        Don Libes, National Institute of Standards and Technology
 
        kibitz  is in the public domain.  NIST and I would appreciate credit if
        this program or parts of it are used.
 
                                 19 October 1994                      KIBITZ(1)
 ```
 
 - - -
 
 ##### lpunlock
 
 
 ```
 root@kali:~# lpunlock -h
 spawn ed /etc/printcap
 ```
 
 - - -
 
 ##### multixterm
 
 Drive multiple xterms separately or together
 
 ```
 root@kali:~# man multixterm
 MULTIXTERM(1)               General Commands Manual              MULTIXTERM(1)
 
 NAME
        multixterm - drive multiple xterms separately or together
 
 SYNOPSIS
        multixterm [ args ]
 
 DESCRIPTION
        Multixterm creates multiple xterms that can be driven together or sepa-
        rately.
 
        In  its simplest form, multixterm is run with no arguments and commands
        are interactively entered in the first entry field.  Press  return  (or
        click  the  "new xterm" button) to create a new xterm running that com-
        mand.
 
        Keystrokes in the "stdin window" are redirected to all  xterms  started
        by  multixterm.   xterms may be driven separately simply by focusing on
        them.
 
        The stdin window must have the focus for keystrokes to be sent  to  the
        xterms.   When  it  has the focus, the color changes to aquamarine.  As
        characters are entered, the color changes to green for a second.   This
        provides feedback since characters are not echoed in the stdin window.
 
        Typing  in  the  stdin  window  while holding down the alt or meta keys
        sends an escape character before the typed characters.   This  provides
        support for programs such as emacs.
 
 ARGUMENTS
               -xa The  optional  -xa  argument  indicates arguments to pass to
                   xterm.
 
               -xc The optional -xc argument indicates a command to be  run  in
                   each  named xterm (see -xn).  With no -xc argument, the com-
                   mand is the current shell.
 
               -xd The optional -xd argument indicates a  directory  to  search
                   for  files  that will appear in the Files menu.  By default,
                   the directory is: ~/lib/multixterm
 
               -xf The optional -xf argument indicates a file  to  be  read  at
                   startup.  See FILES below for more info.
 
               -xn The  optional  -xn argument indicates a name for each xterm.
                   This name will also be substituted for any %n in the command
                   argument (see -xc).
 
               -xv The optional -xv flag puts multixterm into  a  verbose  mode
                   where it will describe some of the things it is doing inter-
                   nally.  The verbose output is not intended to be understand-
                   able to anyone but the author.
 
        Less  common  options may be changed by the startup file (see FILES be-
        low).
 
        All the usual X and wish flags are supported (i.e.,  -display,  -name).
        There are so many of them that to avoid colliding and make them easy to
        remember, all the multixterm flags begin with -x.
 
        If  any  arguments  do  not match the flags above, the remainder of the
        command line is made available for user processing.   By  default,  the
        remainder  is  used  as a list of xterm names in the style of -xn.  The
        default behavior may be changed using the .multixtermrc file  (see  DOT
        FILE below).
 
 EXAMPLE COMMAND LINE ARGUMENTS
        The  following command line starts up two xterms using ssh to the hosts
        bud and dexter.
 
             multixterm -xc "ssh %n" bud dexter
 
 FILES
        Command files may be used to drive or initialize multixterm.  The  File
        menu  may be used to invoke other files.  If files exist in the command
        file directory (see -xd above), they will  appear  in  the  File  menu.
        Files  may also be loaded by using File->Open.  Any filename is accept-
        able but the File->Open browser defaults to files with a .mxt suffix.
 
        Files are written in Tcl and may change any  variables  or  invoke  any
        procedures.   The  primary  variables  of interest are 'xtermCmd' which
        identifies the command (see -xc) and 'xtermNames' which is  a  list  of
        names  (see  -xn).  The procedure xtermStartAll, starts xterms for each
        name in the list.  Other variables and procedures may be discovered  by
        examining multixterm itself.
 
 EXAMPLE FILE
        The  following  file does the same thing as the earlier example command
        line:
 
             # start two xterms connected to bud and dexter
             set xtermCmd "ssh %n"
             set xtermNames {bud dexter}
             xtermStartAll
 
 DOT FILE
        At startup, multixterm reads ~/.multixtermrc if present.  This is simi-
        lar to the command files (see FILES above)  except  that  .multixtermrc
        may  not  call xtermStartAll.  Instead it is called implicitly, similar
        to the way that it is implicit in the command line use of -xn.
 
        The following example .multixtermrc file makes every xterm run  ssh  to
        the hosts named on the command line.
 
             set xtermCmd "ssh %n"
 
        Then multixterm could be called simply:
 
             multixterm bud dexter
 
        If  any command-line argument does not match a multixterm flag, the re-
        mainder of the command line is made available to .multixtermrc  in  the
        argv  variable.  If argv is non-empty when .multixtermrc returns, it is
        assigned to xtermNames unless xtermNames is non-empty  in  which  case,
        the content of argv is ignored.
 
        Commands  from  multixterm are evaluated early in the initialization of
        multixterm.  Anything that must be  done  late  in  the  initialization
        (such  as adding additional bindings to the user interface) may be done
        by putting the commands inside a procedure called "initLate".
 
 MENUS
        Except as otherwise noted, the menus are self-explanatory.  Some of the
        menus have dashed lines as the first entry.   Clicking  on  the  dashed
        lines will "tear off" the menus.
 
 USAGE SUGGESTION - ALIASES AND COMMAND FILES
        Aliases may be used to store lengthy command-line invocations.  Command
        files  can be also be used to store such invocations as well as provid-
        ing a convenient way to share configurations.
 
        Tcl is a general-purpose language.  Thus multixterm command  files  can
        be extremely flexible, such as loading hostnames from other programs or
        files  that may change from day-to-day.  In addition, command files can
        be used for other purposes.  For example, command files may be used  to
        prepared common canned interaction sequences.  For example, the command
        to send the same string to all xterms is:
 
            xtermSend "a particularly long string"
 
        The  File  menu  (torn-off)  makes canned sequences particularly conve-
        nient.  Interactions could also be bound to a mouse button,  keystroke,
        or added to a menu via the .multixtermrc file.
 
        The  following .multixtermrc causes tiny xterms to tile across and down
        the screen.  (You may have to adjust the parameters for  your  screen.)
        This can be very helpful when dealing with large numbers of xterms.
 
            set yPos 0
            set xPos 0
 
            trace variable xtermArgs r traceArgs
 
            proc traceArgs {args} {
                global xPos yPos
                set ::xtermArgs "-geometry 80x12+$xPos+$yPos -font 6x10"
                if {$xPos} {
                    set xPos 0
                    incr yPos 145
                    if {$yPos > 800} {set yPos 0}
                } else {
                    set xPos 500
                }
            }
 
        The  xtermArgs variable in the code above is the variable corresponding
        to the -xa argument.
 
        xterms can be also be created directly.   The  following  command  file
        creates three xterms overlapped horizontally:
 
            set xPos 0
            foreach name {bud dexter hotdog} {
                set ::xtermArgs "-geometry 80x12+$xPos+0 -font 6x10"
                set ::xtermNames $name
                xtermStartAll
                incr xPos 300
            }
 
 USAGE SUGGESTION - SELECTING HOSTS BY NICKNAME
        The  following  .multixtermrc  shows an example of changing the default
        handling of the arguments from hostnames to a filename containing host-
        names:
 
             set xtermNames [exec cat $argv]
 
        The following is a variation, retrieving the host  names  from  the  yp
        database:
 
             set xtermNames [exec ypcat $argv]
 
        The following hardcodes two sets of hosts, so that you can call multix-
        term with either "cluster1" or "cluster2":
 
             switch $argv {
                    cluster1 {
                        set xtermNames "bud dexter"
                    }
                    cluster2 {
                        set xtermNames "frank hotdog weiner"
                    }
                }
 
 COMPARE/CONTRAST
        It  is  worth  comparing  multixterm to xkibitz.  Multixterm connects a
        separate process to each xterm.  xkibitz connects the same  process  to
        each xterm.
 
 LIMITATIONS
        Multixterm  provides no way to remotely control scrollbars, resize, and
        most other window system related functions.
 
        Because xterm has no mechanism for propagating size information to  ex-
        ternal  processes,  particularly  for  character  graphic  applications
        (e.g., vi, emacs), you may have to manually  ensure  that  the  spawned
        process  behind  each  xterm has the correct size.  For example, if you
        create or set the xterm to a size, you may have  to  send  an  explicit
        stty  command with the correct size to the spawned process(es).  Alter-
        natively, you can add the correct size argument when an xterm  is  cre-
        ated (i.e., "-geometry 80x20").
 
        Multixterm  can  only  control  new  xterms  that multixterm itself has
        started.
 
        As a convenience, the File menu shows a limited number  of  files.   To
        show all the files, use File->Open.
 
 FILES
        $DOTDIR/.multixtermrc   initial command file
        ~/.multixtermrc         fallback command file
        ~/lib/multixterm/       default command file directory
 
 BUGS
        If  multixterm  is killed using an uncatchable kill, the xterms are not
        killed.  This appears to be a bug in xterm itself.
 
        Send/expect sequences can be done in multixterm  command  files.   How-
        ever, due to the richness of the possibilities, to document it properly
        would take more time than the author has at present.
 
 REQUIREMENTS
        Requires Expect 5.36.0 or later.
        Requires Tk 8.3.3 or later.
 
 VERSION
        This man page describes version 1.8 of multixterm.
 
        The   latest   version  of  multixterm  is  available  from  http://ex-
        pect.nist.gov/example/multixterm .  If your version of  Expect  and  Tk
        are  too old (see REQUIREMENTS above), download a new version of Expect
        from http://expect.nist.gov
 
 DATE
        April 30, 2002
 
 AUTHOR
        Don Libes <don@libes.com>
 
 LICENSE
        Multixterm is in the public domain; however the author would appreciate
        acknowledgement if multixterm or parts of it or ideas from it are used.
 
                                 16 August 2002                   MULTIXTERM(1)
 ```
 
 - - -
 
 ##### passmass
 
 Change password on multiple machines
 
 ```
 root@kali:~# man passmass
 PASSMASS(1)                 General Commands Manual                PASSMASS(1)
 
 NAME
        passmass - change password on multiple machines
 
 SYNOPSIS
        passmass [ host1 host2 host3 ...  ]
 
 INTRODUCTION
        Passmass changes a password on multiple machines.  If you have accounts
        on  several machines that do not share password databases, Passmass can
        help you keep them all in sync.  This, in turn, will make it easier  to
        change them more frequently.
 
        When Passmass runs, it asks you for the old and new passwords.  (If you
        are changing root passwords and have equivalencing, the old password is
        not used and may be omitted.)
 
        Passmass understands the "usual" conventions.  Additional arguments may
        be  used  for tuning.  They affect all hosts which follow until another
        argument overrides it.  For example, if you are  known  as  "libes"  on
        host1 and host2, but "don" on host3, you would say:
 
             passmass host1 host2 -user don host3
 
        Arguments are:
 
               -user
                   User  whose  password will be changed.  By default, the cur-
                   rent user is used.
 
               -rlogin
                   Use rlogin to access host.  (default)
 
               -slogin
                   Use slogin to access host.
 
               -ssh
                   Use ssh to access host.
 
               -telnet
                   Use telnet to access host.
 
               -program
 
                   Next argument is a program to run to set the password.   De-
                   fault  is "passwd".  Other common choices are "yppasswd" and
                   "set passwd" (e.g., VMS hosts).   A  program  name  such  as
                   "password  fred"  can  be used to create entries for new ac-
                   counts (when run as root).
 
               -prompt
                   Next argument is a prompt suffix pattern.  This  allows  the
                   script  to know when the shell is prompting.  The default is
                   "# " for root and "% " for non-root accounts.
 
               -timeout
                   Next argument is the number  of  seconds  to  wait  for  re-
                   sponses.   Default is 30 but some systems can be much slower
                   logging in.
 
               -su
 
                   Next argument is  1  or  0.   If  1,  you  are  additionally
                   prompted  for a root password which is used to su after log-
                   ging in.  root's password is changed rather than the user's.
                   This is useful for hosts which do not allow root to log in.
 
 HOW TO USE
        The best way to run Passmass is to put the command in a one-line  shell
        script  or alias.  Whenever you get a new account on a new machine, add
        the appropriate arguments to the command.  Then  run  it  whenever  you
        want to change your passwords on all the hosts.
 
 CAVEATS
        Using  the  same password on multiple hosts carries risks.  In particu-
        lar, if the password can be stolen, then all of your  accounts  are  at
        risk.  Thus, you should not use Passmass in situations where your pass-
        word  is  visible,  such as across a network which hackers are known to
        eavesdrop.
 
        On the other hand, if you have enough  accounts  with  different  pass-
        words,  you  may end up writing them down somewhere - and that can be a
        security problem.  Funny story: my  college  roommate  had  an  11"x13"
        piece of paper on which he had listed accounts and passwords all across
        the Internet.  This was several years worth of careful work and he car-
        ried it with him everywhere he went.  Well one day, he forgot to remove
        it  from  his jeans, and we found a perfectly blank sheet of paper when
        we took out the wash the following day!
 
 SEE ALSO
        "Exploring Expect: A Tcl-Based Toolkit for Automating Interactive  Pro-
        grams" by Don Libes, O'Reilly and Associates, January 1995.
 
 AUTHOR
        Don Libes, National Institute of Standards and Technology
 
                                 7 October 1993                     PASSMASS(1)
 ```
 
 - - -
 
 ##### rlogin-cwd
 
 
 ```
 root@kali:~# rlogin-cwd -h
 spawn rlogin -h
 rlogin: invalid option -- 'h'
 usage: rlogin [-8ELKd] [-e char] [-i user] [-l user] [-p port] host
 ```
 
 - - -
 
 ##### timed-read
 
 
 
 - - -
 
 ##### timed-run
 
 
 ```
 root@kali:~# timed-run -h
 usage: spawn [spawn-args] program [program-args]
     while executing
 "spawn"
     ("eval" body line 1)
     invoked from within
 "eval spawn [lrange $argv 1 end]"
     (file "/usr/bin/timed-run" line 12)
 ```
 
 - - -
 
 ##### tknewsbiff
 
 Pop up a window when news appears
 
 ```
 root@kali:~# man tknewsbiff
 TKNEWSBIFF(1)               General Commands Manual              TKNEWSBIFF(1)
 
 NAME
        tknewsbiff - pop up a window when news appears
 
 SYNOPSIS
        tknewsbiff [ server or config-file ]
 
 INTRODUCTION
        tknewsbiff  pops up a window when there is unread news in your favorite
        newsgroups and removes the window after you've read the news.  tknewsb-
        iff can optionally play a sound, start your newsreader, etc.
 
 SELECTING NEWSGROUPS
        By default, the configuration file ~/.tknewsbiff describes how tknewsb-
        iff behaves.  The syntax observes the usual Tcl rules -  however,  even
        if you don't know Tcl, all but the most esoteric configurations will be
        obvious.
 
        Each newsgroup (or set of newsgroups) to be watched is described by us-
        ing the "watch" command.  For example:
 
        watch dc.dining
        watch nist.*
        watch comp.unix.wizard  -threshold 3
        watch *.sources.*       -threshold 20
 
        For each newsgroup pattern, any newsgroup that matches it and which you
        are  subscribed  to (according to your newsrc file) is eligible for re-
        porting.  By default, tknewsbiff reports on the newsgroup if  there  is
        at least one unread article.  The "-threshold" flag changes the thresh-
        old  to  the following number.  For example, "-threshold 3" means there
        must be at least three articles unread before  tknewsbiff  will  report
        the newsgroup.
 
        If  no  watch commands are given (or no configuration file exists), all
        groups which are subscribed to are watched.
 
        To suppress newsgroups that would otherwise be reported, use  the  "ig-
        nore"  command.   For  example,  the  following  matches all comp.* and
        nist.* newgroups except for nist.posix or .d (discussion) groups:
 
        watch comp.*
        watch nist.*
        ignore nist.posix.*
        ignore *.d
 
        The flag "-new" describes a command to be executed when  the  newsgroup
        is  first  reported  as having unread news.  For example, the following
        lines invoke the UNIX command "play" to play a sound.
 
        watch dc.dining -new "exec play /usr/local/sounds/yumyum.au"
        watch rec.auto* -new "exec play /usr/local/sounds/vroom.au"
 
        You can cut down on the verbosity of actions  by  defining  procedures.
        For example, if you have many -new flags that all play sound files, you
        could  define  a sound procedure.  This would allow the -new specifica-
        tion to be much shorter.
 
        proc play {sound} {
             exec play /usr/local/sounds/$sound.au
        }
 
        watch dc.dining -new "play yumyum"
        watch rec.auto* -new "play vroom"
 
        As an aside, you can put an "&" at the end of an "exec" command to  get
        commands  to execute asynchronously.  However, it's probably not a good
        idea to do this when playing sound files anyway.
 
        "newsgroup" is a read-only variable which  contains  the  name  of  the
        newsgroup  that  is  being reported.  This is useful when the action is
        triggered by a pattern.  For example, the following line could run  the
        newsgroup name through a speech synthesizer:
 
        watch * -new {
             exec play herald.au
             exec speak "New news has arrived in $newsgroup."
        }
 
        The  flag  "-display" describes a command to be executed every time the
        newsgroup is reported as having unread news.  The special command "dis-
        play" is the default command.  It schedules $newsgroup to be written to
        tknewsbiff's display when it is rewritten.  For example, by  explicitly
        providing  a -display flag that omits the display command, you can dis-
        able the display of newsgroups that are already reported via -new.
 
        watch dc.dining -new {exec play yumyum.au} -display {}
 
        If you want to execute an action repeatedly and still display the news-
        group in the default manner, explicitly invoke the display command  via
        the -display flag.  For example:
 
        watch *security* -display {
             exec play red-alert.au
             display
        }
 
        Actions  associated  with the -new and -display flags are executed only
        once for each matching newsgroup.  The command executed is the one  as-
        sociated  with the first pattern in the configuration file that matches
        and observes the given threshold.
 
        Any command that is simply listed in the configuration file is executed
        each time before the update loop  in  tknewsbiff.   The  reserved  (but
        user-defined)  procedure "user" is run immediately after the newsgroups
        are scheduled to be written to the display and before they are actually
        written.
 
        For example, suppose unread articles appear in several rec.auto  groups
        and you play the same sound for each one.  To prevent playing the sound
        several  times  in  a row, make the -new command simply set a flag.  In
        the user procedure, play the sound if the flag is set (and  then  reset
        the flag).
 
        The  user  procedure  could  also  be used to start a newsreader.  This
        would avoid the possibility of starting multiple newsreaders  just  be-
        cause  multiple newsgroups contained unread articles.  (A check should,
        of course, be made to make sure that a newsreader is not  already  run-
        ning.)
 
 MORE VARIABLES
        The following example lines show variables that can affect the behavior
        of tknewsbiff
 
        set delay          120
        set server         news.nist.gov
        set server_timeout 60
        set newsrc         ~/.newsrc
        set width          40
        set height         20
        set active_file    /usr/news/lib/active
 
        tknewsbiff  alternates  between  checking  for unread news and sleeping
        (kind of like many undergraduates).  The "delay" variable describes how
        many seconds to sleep.
 
        The "server" variable  names  an  NNTP  news-server.   The  default  is
        "news".   The "server" variable is only used if the "active_file" vari-
        able is not set.
 
        The "server_timeout" variable describes how how many  seconds  to  wait
        for a response from the server before giving up.  -1 means wait forever
        or until the server itself times out.  The default is 60 seconds.
 
        The  "newsrc" variable describes the name of your .newsrc file.  By de-
        fault, tknewsbiff looks in your home directory for a  newsrc  file.   A
        server-specific  newsrc is used if found.  For example, if you have set
        server to "cubit.nist.gov", then  tknewsbiff  looks  for  ~/.newsrc-cu-
        bit.nist.gov.   (This is the Emacs gnus convention - which is very con-
        venient when you read news from multiple  servers.)   If  there  is  no
        server-specific newsrc, tknewsbiff uses ~/.newsrc.
 
        The  "width"  variable  describes the width that tknewsbiff will use to
        display information.  If any newsgroup names are long enough, they will
        be truncated so that the article counts can still be  shown.   You  can
        manually resize the window to see what was truncated.  However, if your
        configuration file sets the width variable, the window will be restored
        to  that  size the next time that tknewsbiff checks for unread news and
        updates its display.
 
        The "height" variable describes the maximum height that tknewsbiff will
        use to display information.  If fewer newsgroups are reported, tknewsb-
        iff will shrink the window appropriately.  You can manually resize  the
        window  but  if  your  configuration file sets the height variable, the
        window will be restored to that size  the  next  time  that  tknewsbiff
        checks for unread news and updates its display.
 
        The  "active_file" variable describes the name of the news active file.
        If set, the active file is read directly in preference  to  using  NNTP
        (even  if  the  "server" variable is set).  This is particularly useful
        for testing out new configuration files since you can edit a  fake  ac-
        tive file and then click button 2 to immediately see how tknewsbiff re-
        sponds (see BUTTONS below).
 
        If  the environment variable DOTDIR is set, then its value is used as a
        directory in which to find all dotfiles instead of from the home direc-
        tory.  In particular, this affects the  tknewsbiff  configuration  file
        and  the  .newsrc file (assuming the newsrc variable is not set explic-
        itly).
 
 WATCHING DIFFERENT NEWS SERVERS
        To watch multiple servers, run tknewsbiff multiple times.   (Since  you
        need  different .newsrc files and the servers have different newsgroups
        and article numbers anyway, there is no point in trying to do this in a
        single process.)
 
        You can point tknewsbiff at a different server with an appropriate  ar-
        gument.  The argument is tried both as a configuration file name and as
        a  suffix  to the string "~/.tknewsbiff-".  So if you want to watch the
        server "kidney", store  the  tknewsbiff  configuration  information  in
        ~/.tknewsbiff-kidney".   The  following two commands will both use that
        configuration file.
 
             tknewsbiff kidney
             tknewsbiff ~/.tknewsbiff-kidney
 
        In both cases, the actual server to contact is set by the value of  the
        server variable in the configuration file.
 
        If  no  configuration file is found, the argument is used as the server
        to contact.  This allows tknewsbiff to be run with no preparation what-
        soever.
 
        If the argument is the special keyword "active" (or ends in "/active"),
        it is used as the name of an active file.  This is in turn used to ini-
        tialize the variable "active_file" so that tknewsbiff  reads  from  the
        active file directly rather than using NNTP.
 
        Creating  your own active file is a convenient way of testing your con-
        figuration file.  For example, after running the following command, you
        can repeatedly edit your active file and trigger the update-now command
        (either by pressing button 2 or setting the delay variable very low) to
        see how tknewsbiff responds.
 
        The active file must follow the format of a real active file.  The for-
        mat is one newsgroup per line.  After the newsgroup name is the  number
        of  the highest article, the lowest article.  Lastly is the letter y or
        m.  m means the newsgroup is moderated.  y means posting is allowed.
 
 WINDOW
        When unread news is found, a window is popped up.  The window lists the
        names of the newsgroups and the number of unread articles in each  (un-
        less suppressed by the -display flag).  When there is no longer any un-
        read  news,  the  window  disappears (although the process continues to
        run).
 
 BUTTONS
        Button or key bindings may be assigned by bind commands.  Feel free  to
        change them.  The default bind commands are:
 
        bind .list <1> help
        bind .list <2> update-now
        bind .list <3> unmapwindow
 
        By default button 1 (left) is bound to "help".  The help command causes
        tknewsbiff to pop up a help window.
 
        By default, button 2 (middle) is bound to "update-now".  The update-now
        command  causes  tknewsbiff  to  immediately check for unread news.  If
        your news server is slow or maintains a  very  large  number  of  news-
        groups,  or  you  have a large number of patterns in your configuration
        file, tknewsbiff can take considerable time  before  actually  updating
        the window.
 
        By  default, button 3 (right) is bound to "unmapwindow".  The unmapwin-
        dow command causes tknewsbiff to remove the window from the display un-
        til the next time it finds unread news.  (The mapwindow command  causes
        tknewsbiff to restore the window.)
 
        As an example, here is a binding to pop up an xterm and run rn when you
        hold down the shift key and press button 1 in the listing window.
 
        bind .list <Shift-1> {
             exec xterm -e rn &
        }
 
        Here  is  a  similar  binding.  However it tells rn to look only at the
        newsgroup that is under the mouse when  you  pressed  it.   (The  "dis-
        play_list" variable is described later in this man page.)
 
        bind .list <Shift-1> {
             exec xterm -e rn [lindex $display_list [.list nearest %y]] &
        }
 
 OTHER COMMANDS AND VARIABLES
        Built-in  commands already mentioned are: watch, ignore, display, help,
        update-now, unmapwindow, and mapwindow.
 
        Any Tcl and Tk command can also be given.  In particular, the  list  of
        newsgroups  is stored in the list widget ".list", and the scroll bar is
        stored in the scrollbar widget ".scroll".  So for example, if you  want
        to  change  the foreground and background colors of the newsgroup list,
        you can say:
 
             .list config -bg honeydew1 -fg orchid2
 
        These can also be controlled by the X resource database as well.   How-
        ever,  the configuration file allows arbitrarily complex commands to be
        evaluated rather than simple assignments.
 
        Certain Tcl/Tk commands can  disrupt  proper  function  of  tknewsbiff.
        These will probably be obvious to anyone who knows enough to give these
        commands  in the first place.  As a simple example, the program assumes
        the font in the list box is of fixed width.  The newsgroups will likely
        not align if you use a variable-width font.
 
        The following variables are accessible and can  be  used  for  esoteric
        uses.  All other variables are private.  Private variables and commands
        begin with "_" so you don't need to worry about accidental collisions.
 
        The array "db" is a database which maintains information about read and
        unread  news.   db($newsgroup,hi)  is  the highest article that exists.
        db($newsgroup,seen) is the highest article that you have read.
 
        A number of lists maintain interesting information. "active_list" is  a
        list  of  known  newsgroups.   "seen_list" is a list of newsgroups that
        have been seen so  far  as  the  -new  and  -display  flags  are  being
        processed.   "previous_seen_list"  is "seen_list" from the previous cy-
        cle.  "ignore_list" is  the  list  of  newsgroup  patterns  to  ignore.
        "watch_list"  is  the  list  of  newsgroup  patterns  to  watch.  "dis-
        play_list" is the list of newsgroup will be displayed at the  next  op-
        portunity.
 
 UPDATING YOUR FILES
        tknewsbiff  automatically  rereads your configuration file each time it
        wakes up to check for unread news.  To force tknewsbiff to  reread  the
        file  immediately  (such  as  if you are testing a new configuration or
        have just modified your newsrc file), press button  2  in  the  display
        (see BUTTONS above).
 
 CAVEATS
        tknewsbiff  defines the number of unread articles as the highest exist-
        ing article minus the highest article that you've read.  So  if  you've
        read the last article in the newsgroup but no others, tknewsbiff thinks
        there  are  no  unread  articles.  (It's impossible to do any better by
        reading the active file and it would be very time consuming to do  this
        more  accurately via NNTP since servers provide no efficient way of re-
        porting their own holes in the newsgroups.)  Fortunately, this  defini-
        tion is considered a feature by most people.  It allows you to read ar-
        ticles  and  then  mark  them "unread" but not have tknewsbiff continue
        telling you that they are unread.
 
 UNWARRANTED CONCERNS
        Your news administrator may wonder if many people using tknewsbiff  se-
        verely  impact  an NNTP server.  In fact, the impact is negligible even
        when the delay is very low.  To gather all the  information  it  needs,
        tknewsbiff uses a single NNTP query - it just asks for the active file.
        The NNTP server does no computation, formatting, etc, it just sends the
        file.  All the interesting processing happens locally in the tknewsbiff
        program itself.
 
 BUGS
        The man page is longer than the program.
 
 SEE ALSO
        "Exploring  Expect: A Tcl-Based Toolkit for Automating Interactive Pro-
        grams" by Don Libes, O'Reilly and Associates, January 1995.
 
 AUTHOR
        Don Libes, National Institute of Standards and Technology
 
                                 1 January 1994                   TKNEWSBIFF(1)
 ```
 
 - - -
 
 ##### tkpasswd
 
 
 
 - - -
 
 ##### unbuffer
 
 Unbuffer output
 
 ```
 root@kali:~# unbuffer -h
 bad flag "-h": must be -console, -ignore, -leaveopen, -noecho, -nottycopy, -nottyinit, -open, or -pty
     while executing
 "spawn -noecho -h"
     ("eval" body line 1)
     invoked from within
 "eval [list spawn -noecho] $argv"
     invoked from within
 "if {[string compare [lindex $argv 0] "-p"] == 0} {
     # pipeline
     set stty_init "-echo"
     eval [list spawn -noecho] [lrange $argv 1 end]
     clo..."
     (file "/usr/bin/unbuffer" line 13)
 ```
 
 - - -
 
 ##### xkibitz
 
 Allow multiple people to interact in an xterm
 
 ```
 root@kali:~# xkibitz -h
 bad flag "-h": must be -console, -ignore, -leaveopen, -noecho, -nottycopy, -nottyinit, -open, or -pty
     while executing
 "spawn -noecho -h"
     ("eval" body line 1)
     invoked from within
 "eval spawn -noecho $argv"
     invoked from within
 "if {[llength $argv]>0} {
     eval spawn -noecho $argv
 } else {
     spawn -noecho $env(SHELL)
 }"
     (file "/usr/bin/xkibitz" line 201)
 ```
 
 - - -
 
 ##### xpstat
 
 
 
 - - -
 
 ### tcl-expect
 
  Expect is a tool for automating interactive applications according to a script.
  Following the script, Expect knows what can be expected from a program and what
  the correct response should be. Expect is also useful for testing these same
  applications. And by adding Tk, you can also wrap interactive applications in
  X11 GUIs. An interpreted language provides branching and high-level control
  structures to direct the dialogue. In addition, the user can take control and
  interact directly when desired, afterward returning control to the script.
   
  This package contains the library and Tcl package Expect.
 
 **Installed size:** `271 KB`  
 **How to install:** `sudo apt install tcl-expect`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libtcl8.6
 {{< /spoiler >}}
 
 
 - - -
 
 ### tcl-expect-dev
 
  Expect is a tool for automating interactive applications according to a script.
  Following the script, Expect knows what can be expected from a program and what
  the correct response should be. Expect is also useful for testing these same
  applications. And by adding Tk, you can also wrap interactive applications in
  X11 GUIs. An interpreted language provides branching and high-level control
  structures to direct the dialogue. In addition, the user can take control and
  interact directly when desired, afterward returning control to the script.
   
  This package contains the development files.
 
 **Installed size:** `118 KB`  
 **How to install:** `sudo apt install tcl-expect-dev`  
 
 {{< spoiler "Dependencies:" >}}
 * tcl-expect 
 * tcl8.6-dev
 {{< /spoiler >}}
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
