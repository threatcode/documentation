---
Title: python-defaults
Homepage: https://www.python.org/
Repository: https://salsa.debian.org/cpython-team/python-defaults
Architectures: any all
Version: 2.7.18-3
Metapackages: kali-linux-nethunter 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### libpython-all-dbg
 
  The package currently depends on libpython2.7-dbg, in the
  future, dependencies on jython (Python2 for a JVM) and ironpython (Python2
  for Mono) may be added.
   
  This package is a dependency package used as a build dependency for other
  packages to avoid hardcoded dependencies on specific Python2 debug packages.
 
 **Installed size:** `7 KB`  
 **How to install:** `sudo apt install libpython-all-dbg`  
 
 {{< spoiler "Dependencies:" >}}
 * libpython2-dbg 
 * libpython2.7-dbg
 {{< /spoiler >}}
 
 
 - - -
 
 ### libpython-all-dev
 
  The package currently depends on libpython2.7-dev, in the
  future, dependencies on jython (Python2 for a JVM) and ironpython (Python2
  for Mono) may be added.
   
  This package is a dependency package used as a build dependency for other
  packages to avoid hardcoded dependencies on specific Python2 development
  packages.
 
 **Installed size:** `6 KB`  
 **How to install:** `sudo apt install libpython-all-dev`  
 
 {{< spoiler "Dependencies:" >}}
 * libpython2-dev 
 * libpython2.7-dev
 {{< /spoiler >}}
 
 
 - - -
 
 ### libpython2-dbg
 
  Python2 interpreter configured with --pydebug. Dynamically loaded modules
  are searched in /usr/lib/python2.7/lib-dynload/debug first.
 
 **Installed size:** `43 KB`  
 **How to install:** `sudo apt install libpython2-dbg`  
 
 {{< spoiler "Dependencies:" >}}
 * libpython2.7-dbg 
 {{< /spoiler >}}
 
 ##### x86_64-linux-gnu-python2-dbg-config
 
 Output build options for python C/C++ extensions or embedding
 
 ```
 root@kali:~# x86_64-linux-gnu-python2-dbg-config --help
 Usage: /usr/bin/x86_64-linux-gnu-python2-dbg-config --prefix|--exec-prefix|--includes|--libs|--cflags|--ldflags|--extension-suffix|--help|--configdir
 ```
 
 - - -
 
 ### libpython2-dev
 
  Header files, a static library and development tools for building
  Python2 modules, extending the Python2 interpreter or embedding Python2
  in applications.
   
  This package is a dependency package, which depends on Debian's Python2
  version (currently v2.7).
 
 **Installed size:** `43 KB`  
 **How to install:** `sudo apt install libpython2-dev`  
 
 {{< spoiler "Dependencies:" >}}
 * libpython2.7-dev 
 {{< /spoiler >}}
 
 ##### x86_64-linux-gnu-python2-config
 
 Output build options for python C/C++ extensions or embedding
 
 ```
 root@kali:~# x86_64-linux-gnu-python2-config --help
 Usage: /usr/bin/x86_64-linux-gnu-python2-config --prefix|--exec-prefix|--includes|--libs|--cflags|--ldflags|--extension-suffix|--help|--configdir
 ```
 
 - - -
 
 ### libpython2-stdlib
 
  Python2, the high-level, interactive object oriented language,
  includes an extensive class library with lots of goodies for
  network programming, system administration, sounds and graphics.
   
  This package is a dependency package, which depends on Debian's Python2
  version (currently v2.7).
 
 **Installed size:** `38 KB`  
 **How to install:** `sudo apt install libpython2-stdlib`  
 
 {{< spoiler "Dependencies:" >}}
 * libpython2.7-stdlib 
 {{< /spoiler >}}
 
 
 - - -
 
 ### python-all
 
  The package currently depends on python2.7, in the future,
  dependencies on jython (Python2 for a JVM) and ironpython (Python2 for Mono)
  may be added.
   
  This package is a dependency package used as a build dependency for other
  packages to avoid hardcoded dependencies on specific Python2 runtimes.
 
 **Installed size:** `6 KB`  
 **How to install:** `sudo apt install python-all`  
 
 {{< spoiler "Dependencies:" >}}
 * python2 
 * python2.7 
 {{< /spoiler >}}
 
 
 - - -
 
 ### python-all-dbg
 
  The package currently depends on python2.7-dbg, in the
  future, dependencies on jython (Python for a JVM) and ironpython (Python2
  for Mono) may be added.
   
  This package is a dependency package used as a build dependency for other
  packages to avoid hardcoded dependencies on specific Python2 debug packages.
 
 **Installed size:** `6 KB`  
 **How to install:** `sudo apt install python-all-dbg`  
 
 {{< spoiler "Dependencies:" >}}
 * libpython-all-dbg 
 * python-all 
 * python2 
 * python2-dbg 
 * python2.7-dbg 
 {{< /spoiler >}}
 
 
 - - -
 
 ### python-all-dev
 
  The package currently depends on python2.7-dev, in the
  future, dependencies on jython (Python2 for a JVM) and ironpython (Python2
  for Mono) may be added.
   
  This package is a dependency package used as a build dependency for other
  packages to avoid hardcoded dependencies on specific Python2 development
  packages.
 
 **Installed size:** `6 KB`  
 **How to install:** `sudo apt install python-all-dev`  
 
 {{< spoiler "Dependencies:" >}}
 * libpython-all-dev 
 * python-all 
 * python2 
 * python2-dev 
 * python2.7-dev 
 {{< /spoiler >}}
 
 
 - - -
 
 ### python2
 
  Python2, the high-level, interactive object oriented language,
  includes an extensive class library with lots of goodies for
  network programming, system administration, sounds and graphics.
   
  This package is a dependency package, which depends on Debian's Python2
  version (currently v2.7).
 
 **Installed size:** `69 KB`  
 **How to install:** `sudo apt install python2`  
 
 {{< spoiler "Dependencies:" >}}
 * libpython2-stdlib 
 * python2-minimal 
 * python2.7 
 {{< /spoiler >}}
 
 ##### pdb2
 
 The Python debugger
 
 ```
 root@kali:~# pdb2 -h
 usage: pdb.py scriptfile [arg] ...
 ```
 
 - - -
 
 ##### pydoc2
 
 The Python documentation tool
 
 ```
 root@kali:~# pydoc2 -h
 pydoc - the Python documentation tool
 
 pydoc2 <name> ...
     Show text documentation on something.  <name> may be the name of a
     Python keyword, topic, function, module, or package, or a dotted
     reference to a class or function within a module or module in a
     package.  If <name> contains a '/', it is used as the path to a
     Python source file to document. If name is 'keywords', 'topics',
     or 'modules', a listing of these things is displayed.
 
 pydoc2 -k <keyword>
     Search for a keyword in the synopsis lines of all available modules.
 
 pydoc2 -p <port>
     Start an HTTP server on the given port on the local machine.  Port
     number 0 can be used to get an arbitrary unused port.
 
 pydoc2 -g
     Pop up a graphical interface for finding and serving documentation.
 
 pydoc2 -w <name> ...
     Write out the HTML documentation for a module to a file in the current
     directory.  If <name> contains a '/', it is treated as a filename; if
     it names a directory, documentation is written for all the contents.
 
 ```
 
 - - -
 
 ##### pygettext2
 
 Python equivalent of xgettext(1)
 
 ```
 root@kali:~# pygettext2 -h
 pygettext -- Python equivalent of xgettext(1)
 
 Many systems (Solaris, Linux, Gnu) provide extensive tools that ease the
 internationalization of C programs. Most of these tools are independent of
 the programming language and can be used from within Python programs.
 Martin von Loewis' work[1] helps considerably in this regard.
 
 There's one problem though; xgettext is the program that scans source code
 looking for message strings, but it groks only C (or C++). Python
 introduces a few wrinkles, such as dual quoting characters, triple quoted
 strings, and raw strings. xgettext understands none of this.
 
 Enter pygettext, which uses Python's standard tokenize module to scan
 Python source code, generating .pot files identical to what GNU xgettext[2]
 generates for C and C++ code. From there, the standard GNU tools can be
 used.
 
 A word about marking Python strings as candidates for translation. GNU
 xgettext recognizes the following keywords: gettext, dgettext, dcgettext,
 and gettext_noop. But those can be a lot of text to include all over your
 code. C and C++ have a trick: they use the C preprocessor. Most
 internationalized C source includes a #define for gettext() to _() so that
 what has to be written in the source is much less. Thus these are both
 translatable strings:
 
     gettext("Translatable String")
     _("Translatable String")
 
 Python of course has no preprocessor so this doesn't work so well.  Thus,
 pygettext searches only for _() by default, but see the -k/--keyword flag
 below for how to augment this.
 
  [1] http://www.python.org/workshops/1997-10/proceedings/loewis.html
  [2] http://www.gnu.org/software/gettext/gettext.html
 
 NOTE: pygettext attempts to be option and feature compatible with GNU
 xgettext where ever possible. However some options are still missing or are
 not fully implemented. Also, xgettext's use of command line switches with
 option arguments is broken, and in these cases, pygettext just defines
 additional switches.
 
 Usage: pygettext [options] inputfile ...
 
 Options:
 
     -a
     --extract-all
         Extract all strings.
 
     -d name
     --default-domain=name
         Rename the default output file from messages.pot to name.pot.
 
     -E
     --escape
         Replace non-ASCII characters with octal escape sequences.
 
     -D
     --docstrings
         Extract module, class, method, and function docstrings.  These do
         not need to be wrapped in _() markers, and in fact cannot be for
         Python to consider them docstrings. (See also the -X option).
 
     -h
     --help
         Print this help message and exit.
 
     -k word
     --keyword=word
         Keywords to look for in addition to the default set, which are:
         _
 
         You can have multiple -k flags on the command line.
 
     -K
     --no-default-keywords
         Disable the default set of keywords (see above).  Any keywords
         explicitly added with the -k/--keyword option are still recognized.
 
     --no-location
         Do not write filename/lineno location comments.
 
     -n
     --add-location
         Write filename/lineno location comments indicating where each
         extracted string is found in the source.  These lines appear before
         each msgid.  The style of comments is controlled by the -S/--style
         option.  This is the default.
 
     -o filename
     --output=filename
         Rename the default output file from messages.pot to filename.  If
         filename is `-' then the output is sent to standard out.
 
     -p dir
     --output-dir=dir
         Output files will be placed in directory dir.
 
     -S stylename
     --style stylename
         Specify which style to use for location comments.  Two styles are
         supported:
 
         Solaris  # File: filename, line: line-number
         GNU      #: filename:line
 
         The style name is case insensitive.  GNU style is the default.
 
     -v
     --verbose
         Print the names of the files being processed.
 
     -V
     --version
         Print the version of pygettext and exit.
 
     -w columns
     --width=columns
         Set width of output to columns.
 
     -x filename
     --exclude-file=filename
         Specify a file that contains a list of strings that are not be
         extracted from the input files.  Each string to be excluded must
         appear on a line by itself in the file.
 
     -X filename
     --no-docstrings=filename
         Specify a file that contains a list of files (one per line) that
         should not have their docstrings extracted.  This is only useful in
         conjunction with the -D option above.
 
 If `inputfile' is -, standard input is read.
 
 ```
 
 - - -
 
 ### python2-dbg
 
  Python2 interpreter configured with --pydebug. Dynamically loaded modules are
  searched in /usr/lib/python2.7/lib-dynload/debug first.
 
 **Installed size:** `20 KB`  
 **How to install:** `sudo apt install python2-dbg`  
 
 {{< spoiler "Dependencies:" >}}
 * libpython2-dbg 
 * python2 
 * python2.7-dbg 
 {{< /spoiler >}}
 
 ##### python2-dbg
 
 An interpreted, interactive, object-oriented programming language
 
 ```
 root@kali:~# python2-dbg -h
 usage: python2-dbg [option] ... [-c cmd | -m mod | file | -] [arg] ...
 Options and arguments (and corresponding environment variables):
 -b     : issue warnings about comparing bytearray with unicode
          (-bb: issue errors)
 -B     : don't write .py[co] files on import; also PYTHONDONTWRITEBYTECODE=x
 -c cmd : program passed in as string (terminates option list)
 -d     : debug output from parser; also PYTHONDEBUG=x
 -E     : ignore PYTHON* environment variables (such as PYTHONPATH)
 -h     : print this help message and exit (also --help)
 -i     : inspect interactively after running script; forces a prompt even
          if stdin does not appear to be a terminal; also PYTHONINSPECT=x
 -m mod : run library module as a script (terminates option list)
 -O     : optimize generated bytecode slightly; also PYTHONOPTIMIZE=x
 -OO    : remove doc-strings in addition to the -O optimizations
 -R     : use a pseudo-random salt to make hash() values of various types be
          unpredictable between separate invocations of the interpreter, as
          a defense against denial-of-service attacks
 -Q arg : division options: -Qold (default), -Qwarn, -Qwarnall, -Qnew
 -s     : don't add user site directory to sys.path; also PYTHONNOUSERSITE
 -S     : don't imply 'import site' on initialization
 -t     : issue warnings about inconsistent tab usage (-tt: issue errors)
 -u     : unbuffered binary stdout and stderr; also PYTHONUNBUFFERED=x
          see man page for details on internal buffering relating to '-u'
 -v     : verbose (trace import statements); also PYTHONVERBOSE=x
          can be supplied multiple times to increase verbosity
 -V     : print the Python version number and exit (also --version)
 -W arg : warning control; arg is action:message:category:module:lineno
          also PYTHONWARNINGS=arg
 -x     : skip first line of source, allowing use of non-Unix forms of #!cmd
 -3     : warn about Python 3.x incompatibilities that 2to3 cannot trivially fix
 file   : program read from script file
 -      : program read from stdin (default; interactive mode if a tty)
 arg ...: arguments passed to program in sys.argv[1:]
 
 Other environment variables:
 PYTHONSTARTUP: file executed on interactive startup (no default)
 PYTHONPATH   : ':'-separated list of directories prefixed to the
                default module search path.  The result is sys.path.
 PYTHONHOME   : alternate <prefix> directory (or <prefix>:<exec_prefix>).
                The default module search path uses <prefix>/pythonX.X.
 PYTHONCASEOK : ignore case in 'import' statements (Windows).
 PYTHONIOENCODING: Encoding[:errors] used for stdin/stdout/stderr.
 PYTHONHASHSEED: if this variable is set to 'random', the effect is the same
    as specifying the -R option: a random value is used to seed the hashes of
    str, bytes and datetime objects.  It can also be set to an integer
    in the range [0,4294967295] to get hash values with a predictable seed.
 ```
 
 - - -
 
 ##### python2-dbg-config
 
 Output build options for python C/C++ extensions or embedding
 
 ```
 root@kali:~# python2-dbg-config --help
 Usage: /usr/bin/python2-dbg-config --prefix|--exec-prefix|--includes|--libs|--cflags|--ldflags|--extension-suffix|--help|--configdir
 ```
 
 - - -
 
 ### python2-dev
 
  Header files, a static library and development tools for building
  Python2 modules, extending the Python2 interpreter or embedding Python2
  in applications.
   
  This package is a dependency package, which depends on Debian's Python2
  version (currently v2.7).
 
 **Installed size:** `15 KB`  
 **How to install:** `sudo apt install python2-dev`  
 
 {{< spoiler "Dependencies:" >}}
 * libpython2-dev 
 * python2 
 * python2.7-dev 
 {{< /spoiler >}}
 
 ##### python2-config
 
 Output build options for python C/C++ extensions or embedding
 
 ```
 root@kali:~# python2-config --help
 Usage: /usr/bin/python2-config --prefix|--exec-prefix|--includes|--libs|--cflags|--ldflags|--extension-suffix|--help|--configdir
 ```
 
 - - -
 
 ### python2-doc
 
  This is the official set of documentation for the interactive high-level
  object-oriented language Python2 (v2.7). All documents are provided
  in HTML format, some in info format. The package consists of nine documents:
   
    * Tutorial
    * Python Library Reference
    * Macintosh Module Reference
    * Python Language Reference
    * Extending and Embedding Python
    * Python/C API Reference
    * Installing Python Modules
    * Documenting Python
    * Distributing Python Modules
   
  This package is a dependency package, which depends on Debian's Python2
  version (currently v2.7).
 
 **Installed size:** `41 KB`  
 **How to install:** `sudo apt install python2-doc`  
 
 {{< spoiler "Dependencies:" >}}
 * python2.7-doc 
 {{< /spoiler >}}
 
 
 - - -
 
 ### python2-minimal
 
  This package contains the interpreter and some essential modules.  It's used
  in the boot process for some basic tasks.
  See /usr/share/doc/python2.7-minimal/README.Debian for a list of the modules
  contained in this package.
 
 **Installed size:** `105 KB`  
 **How to install:** `sudo apt install python2-minimal`  
 
 {{< spoiler "Dependencies:" >}}
 * dpkg 
 * python2.7-minimal 
 {{< /spoiler >}}
 
 ##### pyclean
 
 Removes .pyc and .pyo files
 
 ```
 root@kali:~# pyclean -h
 Usage: pyclean [-p PACKAGE] [DIR_OR_FILE]
 
 Options:
   --version             show program's version number and exit
   -h, --help            show this help message and exit
   -v, --verbose         turn verbose more one
   -q, --quiet           be quiet
   -p PACKAGE, --package=PACKAGE
                         specify Debian package name to clean
 ```
 
 - - -
 
 ##### pycompile
 
 Byte compile Python source files
 
 ```
 root@kali:~# pycompile -h
 Usage: pycompile [-V [X.Y][-][A.B]] DIR_OR_FILE [-X REGEXPR]
        pycompile -p PACKAGE
 
 Options:
   --version             show program's version number and exit
   -h, --help            show this help message and exit
   -v, --verbose         turn verbose mode on
   -q, --quiet           be quiet
   -f, --force           force rebuild even if timestamps are up-to-date
   -O                    byte-compile to .pyo files
   -p PACKAGE, --package=PACKAGE
                         specify Debian package name whose files should be
                         bytecompiled
   -V VRANGE             force private modules to be bytecompiled with Python
                         version from given range, regardless of the default
                         Python version in the system. If there are no other
                         options, bytecompile all public modules for installed
                         Python versions that match given range.  VERSION_RANGE
                         examples: '2.5' (version 2.5 only), '2.5-' (version
                         2.5 or newer), '2.5-2.7' (version 2.5 or 2.6), '-3.0'
                         (all supported 2.X versions)
   -X REGEXPR, --exclude=REGEXPR
                         exclude items that match given REGEXPR. You may use
                         this option multiple times to build up a list of
                         things to exclude.
 ```
 
 - - -
 
 ##### python2
 
 An interpreted, interactive, object-oriented programming language
 
 ```
 root@kali:~# python2 -h
 usage: python2 [option] ... [-c cmd | -m mod | file | -] [arg] ...
 Options and arguments (and corresponding environment variables):
 -b     : issue warnings about comparing bytearray with unicode
          (-bb: issue errors)
 -B     : don't write .py[co] files on import; also PYTHONDONTWRITEBYTECODE=x
 -c cmd : program passed in as string (terminates option list)
 -d     : debug output from parser; also PYTHONDEBUG=x
 -E     : ignore PYTHON* environment variables (such as PYTHONPATH)
 -h     : print this help message and exit (also --help)
 -i     : inspect interactively after running script; forces a prompt even
          if stdin does not appear to be a terminal; also PYTHONINSPECT=x
 -m mod : run library module as a script (terminates option list)
 -O     : optimize generated bytecode slightly; also PYTHONOPTIMIZE=x
 -OO    : remove doc-strings in addition to the -O optimizations
 -R     : use a pseudo-random salt to make hash() values of various types be
          unpredictable between separate invocations of the interpreter, as
          a defense against denial-of-service attacks
 -Q arg : division options: -Qold (default), -Qwarn, -Qwarnall, -Qnew
 -s     : don't add user site directory to sys.path; also PYTHONNOUSERSITE
 -S     : don't imply 'import site' on initialization
 -t     : issue warnings about inconsistent tab usage (-tt: issue errors)
 -u     : unbuffered binary stdout and stderr; also PYTHONUNBUFFERED=x
          see man page for details on internal buffering relating to '-u'
 -v     : verbose (trace import statements); also PYTHONVERBOSE=x
          can be supplied multiple times to increase verbosity
 -V     : print the Python version number and exit (also --version)
 -W arg : warning control; arg is action:message:category:module:lineno
          also PYTHONWARNINGS=arg
 -x     : skip first line of source, allowing use of non-Unix forms of #!cmd
 -3     : warn about Python 3.x incompatibilities that 2to3 cannot trivially fix
 file   : program read from script file
 -      : program read from stdin (default; interactive mode if a tty)
 arg ...: arguments passed to program in sys.argv[1:]
 
 Other environment variables:
 PYTHONSTARTUP: file executed on interactive startup (no default)
 PYTHONPATH   : ':'-separated list of directories prefixed to the
                default module search path.  The result is sys.path.
 PYTHONHOME   : alternate <prefix> directory (or <prefix>:<exec_prefix>).
                The default module search path uses <prefix>/pythonX.X.
 PYTHONCASEOK : ignore case in 'import' statements (Windows).
 PYTHONIOENCODING: Encoding[:errors] used for stdin/stdout/stderr.
 PYTHONHASHSEED: if this variable is set to 'random', the effect is the same
    as specifying the -R option: a random value is used to seed the hashes of
    str, bytes and datetime objects.  It can also be set to an integer
    in the range [0,4294967295] to get hash values with a predictable seed.
 ```
 
 - - -
 
 ##### pyversions
 
 Print python version information
 
 ```
 root@kali:~# pyversions -h
 Usage: [-v] [-h] [-d|--default] [-s|--supported] [-i|--installed] [-r|--requested <version string>|<control file>]
 
 Options:
   -h, --help       show this help message and exit
   -d, --default    print the default python version
   -s, --supported  print the supported python versions
   -r, --requested  print the python versions requested by a build; the
                    argument is either the name of a control file or the value
                    of the X(S)-Python-Version attribute
   -i, --installed  print the installed supported python versions
   -v, --version    print just the version number(s)
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
