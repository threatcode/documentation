---
Title: python-virtualenv
Homepage: https://virtualenv.pypa.io/
Repository: https://salsa.debian.org/python-team/packages/python-virtualenv
Architectures: all
Version: 20.24.6+ds-2
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### python3-virtualenv
 
  virtualenv is a tool to create isolated Python environments, each invokable
  with its own Python executable.  Each instance can have different sets of
  modules, installable via pip.  Virtual Python instances can also be created
  without root access.
   
  Since Python 3.3, a subset of it has been integrated into the standard library
  under the venv module (python3-venv in Debian).  The venv module does not
  offer all features of this library, to name just a few more prominent ones:
   
   * is slower (by not having the app-data seed method),
   * is not as extendable,
   * cannot create virtual environments for arbitrarily installed Python
     versions (and automatically discover these),
   * does not have as rich programmatic API (describe virtual environments
     without creating them).
   
  This is the Python 3 version of the library.  It includes the command line
  script.
 
 **Installed size:** `356 KB`  
 **How to install:** `sudo apt install python3-virtualenv`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-distlib 
 * python3-filelock
 * python3-importlib-metadata  | python3-supported-min 
 * python3-pip-whl
 * python3-platformdirs 
 * python3-setuptools-whl
 * python3-setuptools-whl  | python3-distutils
 * python3-wheel-whl
 {{< /spoiler >}}
 
 ##### virtualenv
 
 Python virtual environment creator
 
 ```
 root@kali:~# virtualenv -h
 usage: virtualenv [--version] [--with-traceback] [-v | -q] [--read-only-app-data] [--app-data APP_DATA] [--reset-app-data] [--upgrade-embed-wheels] [--discovery {builtin}] [-p py] [--try-first-with py_exe]
                   [--creator {builtin,cpython3-posix,venv}] [--seeder {app-data,pip}] [--no-seed] [--activators comma_sep_list] [--clear] [--no-vcs-ignore] [--system-site-packages] [--symlinks | --copies] [--no-download | --download]
                   [--extra-search-dir d [d ...]] [--pip version] [--setuptools version] [--wheel version] [--no-pip] [--no-setuptools] [--no-wheel] [--no-periodic-update] [--symlink-app-data] [--prompt prompt] [-h]
                   dest
 
 options:
   --version                     display the version of the virtualenv package and its location, then exit
   --with-traceback              on failure also display the stacktrace internals of virtualenv (default: False)
   --read-only-app-data          use app data folder in read-only mode (write operations will fail with error) (default: False)
   --app-data APP_DATA           a data folder used as cache by the virtualenv (default: /root/.local/share/virtualenv)
   --reset-app-data              start with empty app data folder (default: False)
   --upgrade-embed-wheels        trigger a manual update of the embedded wheels (default: False)
   -h, --help                    show this help message and exit
 
 verbosity:
   verbosity = verbose - quiet, default INFO, mapping => CRITICAL=0, ERROR=1, WARNING=2, INFO=3, DEBUG=4, NOTSET=5
 
   -v, --verbose                 increase verbosity (default: 2)
   -q, --quiet                   decrease verbosity (default: 0)
 
 discovery:
   discover and provide a target interpreter
 
   --discovery {builtin}         interpreter discovery method (default: builtin)
   -p py, --python py            interpreter based on what to create environment (path/identifier) - by default use the interpreter where the tool is installed - first found wins (default: [])
   --try-first-with py_exe       try first these interpreters before starting the discovery (default: [])
 
 creator:
   options for creator builtin
 
   --creator {builtin,cpython3-posix,venv}
                                 create environment via (builtin = cpython3-posix) (default: builtin)
   dest                          directory to create virtualenv at
   --clear                       remove the destination directory if exist before starting (will overwrite files otherwise) (default: False)
   --no-vcs-ignore               don't create VCS ignore directive in the destination directory (default: False)
   --system-site-packages        give the virtual environment access to the system site-packages dir (default: False)
   --symlinks                    try to use symlinks rather than copies, when symlinks are not the default for the platform (default: True)
   --copies, --always-copy       try to use copies rather than symlinks, even when symlinks are the default for the platform (default: False)
 
 seeder:
   options for seeder app-data
 
   --seeder {app-data,pip}       seed packages install method (default: app-data)
   --no-seed, --without-pip      do not install seed packages (default: False)
   --no-download, --never-download
                                 pass to disable download of the latest pip/setuptools/wheel from PyPI (default: True)
   --download                    pass to enable download of the latest pip/setuptools/wheel from PyPI (default: False)
   --extra-search-dir d [d ...]  a path containing wheels to extend the internal wheel list (can be set 1+ times) (default: [])
   --pip version                 version of pip to install as seed: embed, bundle, none or exact version (default: bundle)
   --setuptools version          version of setuptools to install as seed: embed, bundle, none or exact version (default: bundle)
   --wheel version               version of wheel to install as seed: embed, bundle, none or exact version (default: bundle)
   --no-pip                      do not install pip (default: False)
   --no-setuptools               do not install setuptools (default: False)
   --no-wheel                    do not install wheel (default: False)
   --no-periodic-update          disable the periodic (once every 14 days) update of the embedded wheels (default: True)
   --symlink-app-data            symlink the python packages from the app-data folder (requires seed pip>=19.3) (default: False)
 
 activators:
   options for activation scripts
 
   --activators comma_sep_list   activators to generate - default is all supported (default: bash,cshell,fish,nushell,powershell,python)
   --prompt prompt               provides an alternative prompt prefix for this environment (value of . means name of the current working directory) (default: None)
 
 config file /root/.config/virtualenv/virtualenv.ini missing (change via env var VIRTUALENV_CONFIG_FILE)
 ```
 
 - - -
 
 ### virtualenv
 
  The virtualenv utility creates virtual Python instances, each invokable with
  its own Python executable.  Each instance can have different sets of modules,
  installable via pip.  Virtual Python instances can also be created without
  root access.
   
  This is a dependency package and may be safely removed.
 
 **Installed size:** `13 KB`  
 **How to install:** `sudo apt install virtualenv`  
 
 {{< spoiler "Dependencies:" >}}
 * python3-virtualenv
 {{< /spoiler >}}
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
