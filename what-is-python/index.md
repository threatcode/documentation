---
Title: what-is-python
Homepage: 
Repository: 
Architectures: all
Version: 14
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### python-dev-is-python3
 
  Starting with the Debian 11 (bullseye) and Ubuntu 20.04 LTS (focal)
  releases, all python packages use explicit python3 or python2
  interpreter and do not use unversioned /usr/bin/python-config at all.
  Some third-party code is now predominantly python3 based, yet may use
  /usr/bin/python-config.
   
  This is a convenience package which ships a symlink to point
  /usr/bin/python-config script at the current default python3. It may
  improve compatibility with other modern systems, whilst breaking some
  obsolete or 3rd-party software.
   
  No packages may declare dependencies on this package.
 
 **Installed size:** `13 KB`  
 **How to install:** `sudo apt install python-dev-is-python3`  
 
 {{< spoiler "Dependencies:" >}}
 * python-is-python3 
 * python3-dev
 {{< /spoiler >}}
 
 ##### pdb
 
 The Python debugger
 
 ```
 root@kali:~# pdb -h
 usage: pdb.py [-c command] ... [-m module | pyfile] [arg] ...
 
 Debug the Python program given by pyfile. Alternatively,
 an executable module or package to debug can be specified using
 the -m switch.
 
 Initial commands are read from .pdbrc files in your home directory
 and in the current directory, if they exist.  Commands supplied with
 -c are executed after commands from .pdbrc files.
 
 To let the script run until an exception occurs, use "-c continue".
 To let the script run up to a given line X in the debugged file, use
 "-c 'until X'".
 ```
 
 - - -
 
 ##### python-config
 
 Output build options for python C/C++ extensions or embedding
 
 ```
 root@kali:~# python-config --help
 Usage: /usr/bin/python-config --prefix|--exec-prefix|--includes|--libs|--cflags|--ldflags|--extension-suffix|--help|--abiflags|--configdir|--embed
 ```
 
 - - -
 
 ### python-is-python3
 
  Starting with the Debian 11 (bullseye) and Ubuntu 20.04 LTS (focal)
  releases, all python packages use explicit python3 or python2
  interpreter and do not use unversioned /usr/bin/python at all. Some
  third-party code is now predominantly python3 based, yet may use
  /usr/bin/python.
   
  This is a convenience package which ships a symlink to point
  the /usr/bin/python interpreter at the current default python3. It may
  improve compatibility with other modern systems, whilst breaking some
  obsolete or 3rd-party software.
   
  No packages may declare dependencies on this package.
 
 **Installed size:** `15 KB`  
 **How to install:** `sudo apt install python-is-python3`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 {{< /spoiler >}}
 
 ##### pydoc
 
 The Python documentation tool
 
 ```
 root@kali:~# pydoc -h
 pydoc - the Python documentation tool
 
 pydoc <name> ...
     Show text documentation on something.  <name> may be the name of a
     Python keyword, topic, function, module, or package, or a dotted
     reference to a class or function within a module or module in a
     package.  If <name> contains a '/', it is used as the path to a
     Python source file to document. If name is 'keywords', 'topics',
     or 'modules', a listing of these things is displayed.
 
 pydoc -k <keyword>
     Search for a keyword in the synopsis lines of all available modules.
 
 pydoc -n <hostname>
     Start an HTTP server with the given hostname (default: localhost).
 
 pydoc -p <port>
     Start an HTTP server on the given port on the local machine.  Port
     number 0 can be used to get an arbitrary unused port.
 
 pydoc -b
     Start an HTTP server on an arbitrary unused port and open a web browser
     to interactively browse documentation.  This option can be used in
     combination with -n and/or -p.
 
 pydoc -w <name> ...
     Write out the HTML documentation for a module to a file in the current
     directory.  If <name> contains a '/', it is treated as a filename; if
     it names a directory, documentation is written for all the contents.
 
 ```
 
 - - -
 
 ##### python
 
 An interpreted, interactive, object-oriented programming language
 
 ```
 root@kali:~# python -h
 usage: python [option] ... [-c cmd | -m mod | file | -] [arg] ...
 Options (and corresponding environment variables):
 -b     : issue warnings about str(bytes_instance), str(bytearray_instance)
          and comparing bytes/bytearray with str. (-bb: issue errors)
 -B     : don't write .pyc files on import; also PYTHONDONTWRITEBYTECODE=x
 -c cmd : program passed in as string (terminates option list)
 -d     : turn on parser debugging output (for experts only, only works on
          debug builds); also PYTHONDEBUG=x
 -E     : ignore PYTHON* environment variables (such as PYTHONPATH)
 -h     : print this help message and exit (also -? or --help)
 -i     : inspect interactively after running script; forces a prompt even
          if stdin does not appear to be a terminal; also PYTHONINSPECT=x
 -I     : isolate Python from the user's environment (implies -E and -s)
 -m mod : run library module as a script (terminates option list)
 -O     : remove assert and __debug__-dependent statements; add .opt-1 before
          .pyc extension; also PYTHONOPTIMIZE=x
 -OO    : do -O changes and also discard docstrings; add .opt-2 before
          .pyc extension
 -P     : don't prepend a potentially unsafe path to sys.path; also PYTHONSAFEPATH
 -q     : don't print version and copyright messages on interactive startup
 -s     : don't add user site directory to sys.path; also PYTHONNOUSERSITE
 -S     : don't imply 'import site' on initialization
 -u     : force the stdout and stderr streams to be unbuffered;
          this option has no effect on stdin; also PYTHONUNBUFFERED=x
 -v     : verbose (trace import statements); also PYTHONVERBOSE=x
          can be supplied multiple times to increase verbosity
 -V     : print the Python version number and exit (also --version)
          when given twice, print more information about the build
 -W arg : warning control; arg is action:message:category:module:lineno
          also PYTHONWARNINGS=arg
 -x     : skip first line of source, allowing use of non-Unix forms of #!cmd
 -X opt : set implementation-specific option
 --check-hash-based-pycs always|default|never:
          control how Python invalidates hash-based .pyc files
 --help-env      : print help about Python environment variables and exit
 --help-xoptions : print help about implementation-specific -X options and exit
 --help-all      : print complete help information and exit
 Arguments:
 file   : program read from script file
 -      : program read from stdin (default; interactive mode if a tty)
 arg ...: arguments passed to program in sys.argv[1:]
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
