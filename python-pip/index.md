---
Title: python-pip
Homepage: https://pip.pypa.io/en/stable/
Repository: https://salsa.debian.org/python-team/packages/python-pip
Architectures: all
Version: 23.3+dfsg-1
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-linux-nethunter kali-tools-forensics kali-tools-respond 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### python3-pip
 
  pip is the Python package installer.  It integrates with virtualenv, doesn't
  do partial installs, can save package state for replaying, can install from
  non-egg sources, and can install from version control repositories.
   
  This is the Python 3 version of the package.
 
 **Installed size:** `6.67 MB`  
 **How to install:** `sudo apt install python3-pip`  
 
 {{< spoiler "Dependencies:" >}}
 * ca-certificates
 * python3
 * python3-distutils
 * python3-setuptools
 * python3-wheel
 {{< /spoiler >}}
 
 ##### pip
 
 A tool for installing and managing Python packages
 
 ```
 root@kali:~# pip -h
 
 Usage:   
   pip <command> [options]
 
 Commands:
   install                     Install packages.
   download                    Download packages.
   uninstall                   Uninstall packages.
   freeze                      Output installed packages in requirements format.
   inspect                     Inspect the python environment.
   list                        List installed packages.
   show                        Show information about installed packages.
   check                       Verify installed packages have compatible dependencies.
   config                      Manage local and global configuration.
   search                      Search PyPI for packages.
   cache                       Inspect and manage pip's wheel cache.
   index                       Inspect information available from package indexes.
   wheel                       Build wheels from your requirements.
   hash                        Compute hashes of package archives.
   completion                  A helper command used for command completion.
   debug                       Show information useful for debugging.
   help                        Show help for commands.
 
 General Options:
   -h, --help                  Show help.
   --debug                     Let unhandled exceptions propagate outside the
                               main subroutine, instead of logging them to
                               stderr.
   --isolated                  Run pip in an isolated mode, ignoring
                               environment variables and user configuration.
   --require-virtualenv        Allow pip to only run in a virtual environment;
                               exit with an error otherwise.
   --python <python>           Run pip with the specified Python interpreter.
   -v, --verbose               Give more output. Option is additive, and can be
                               used up to 3 times.
   -V, --version               Show version and exit.
   -q, --quiet                 Give less output. Option is additive, and can be
                               used up to 3 times (corresponding to WARNING,
                               ERROR, and CRITICAL logging levels).
   --log <path>                Path to a verbose appending log.
   --no-input                  Disable prompting for input.
   --keyring-provider <keyring_provider>
                               Enable the credential lookup via the keyring
                               library if user input is allowed. Specify which
                               mechanism to use [disabled, import, subprocess].
                               (default: disabled)
   --proxy <proxy>             Specify a proxy in the form
                               scheme://[user:passwd@]proxy.server:port.
   --retries <retries>         Maximum number of retries each connection should
                               attempt (default 5 times).
   --timeout <sec>             Set the socket timeout (default 15 seconds).
   --exists-action <action>    Default action when a path already exists:
                               (s)witch, (i)gnore, (w)ipe, (b)ackup, (a)bort.
   --trusted-host <hostname>   Mark this host or host:port pair as trusted,
                               even though it does not have valid or any HTTPS.
   --cert <path>               Path to PEM-encoded CA certificate bundle. If
                               provided, overrides the default. See 'SSL
                               Certificate Verification' in pip documentation
                               for more information.
   --client-cert <path>        Path to SSL client certificate, a single file
                               containing the private key and the certificate
                               in PEM format.
   --cache-dir <dir>           Store the cache data in <dir>.
   --no-cache-dir              Disable the cache.
   --disable-pip-version-check
                               Don't periodically check PyPI to determine
                               whether a new version of pip is available for
                               download. Implied with --no-index.
   --no-color                  Suppress colored output.
   --no-python-version-warning
                               Silence deprecation warnings for upcoming
                               unsupported Pythons.
   --use-feature <feature>     Enable new functionality, that may be backward
                               incompatible.
   --use-deprecated <feature>  Enable deprecated functionality, that will be
                               removed in the future.
 ```
 
 - - -
 
 ##### pip3
 
 A tool for installing and managing Python packages
 
 ```
 root@kali:~# pip3 -h
 
 Usage:   
   pip3 <command> [options]
 
 Commands:
   install                     Install packages.
   download                    Download packages.
   uninstall                   Uninstall packages.
   freeze                      Output installed packages in requirements format.
   inspect                     Inspect the python environment.
   list                        List installed packages.
   show                        Show information about installed packages.
   check                       Verify installed packages have compatible dependencies.
   config                      Manage local and global configuration.
   search                      Search PyPI for packages.
   cache                       Inspect and manage pip's wheel cache.
   index                       Inspect information available from package indexes.
   wheel                       Build wheels from your requirements.
   hash                        Compute hashes of package archives.
   completion                  A helper command used for command completion.
   debug                       Show information useful for debugging.
   help                        Show help for commands.
 
 General Options:
   -h, --help                  Show help.
   --debug                     Let unhandled exceptions propagate outside the
                               main subroutine, instead of logging them to
                               stderr.
   --isolated                  Run pip in an isolated mode, ignoring
                               environment variables and user configuration.
   --require-virtualenv        Allow pip to only run in a virtual environment;
                               exit with an error otherwise.
   --python <python>           Run pip with the specified Python interpreter.
   -v, --verbose               Give more output. Option is additive, and can be
                               used up to 3 times.
   -V, --version               Show version and exit.
   -q, --quiet                 Give less output. Option is additive, and can be
                               used up to 3 times (corresponding to WARNING,
                               ERROR, and CRITICAL logging levels).
   --log <path>                Path to a verbose appending log.
   --no-input                  Disable prompting for input.
   --keyring-provider <keyring_provider>
                               Enable the credential lookup via the keyring
                               library if user input is allowed. Specify which
                               mechanism to use [disabled, import, subprocess].
                               (default: disabled)
   --proxy <proxy>             Specify a proxy in the form
                               scheme://[user:passwd@]proxy.server:port.
   --retries <retries>         Maximum number of retries each connection should
                               attempt (default 5 times).
   --timeout <sec>             Set the socket timeout (default 15 seconds).
   --exists-action <action>    Default action when a path already exists:
                               (s)witch, (i)gnore, (w)ipe, (b)ackup, (a)bort.
   --trusted-host <hostname>   Mark this host or host:port pair as trusted,
                               even though it does not have valid or any HTTPS.
   --cert <path>               Path to PEM-encoded CA certificate bundle. If
                               provided, overrides the default. See 'SSL
                               Certificate Verification' in pip documentation
                               for more information.
   --client-cert <path>        Path to SSL client certificate, a single file
                               containing the private key and the certificate
                               in PEM format.
   --cache-dir <dir>           Store the cache data in <dir>.
   --no-cache-dir              Disable the cache.
   --disable-pip-version-check
                               Don't periodically check PyPI to determine
                               whether a new version of pip is available for
                               download. Implied with --no-index.
   --no-color                  Suppress colored output.
   --no-python-version-warning
                               Silence deprecation warnings for upcoming
                               unsupported Pythons.
   --use-feature <feature>     Enable new functionality, that may be backward
                               incompatible.
   --use-deprecated <feature>  Enable deprecated functionality, that will be
                               removed in the future.
 ```
 
 - - -
 
 ##### pip3.11
 
 
 ```
 root@kali:~# pip3.11 -h
 
 Usage:   
   pip3.11 <command> [options]
 
 Commands:
   install                     Install packages.
   download                    Download packages.
   uninstall                   Uninstall packages.
   freeze                      Output installed packages in requirements format.
   inspect                     Inspect the python environment.
   list                        List installed packages.
   show                        Show information about installed packages.
   check                       Verify installed packages have compatible dependencies.
   config                      Manage local and global configuration.
   search                      Search PyPI for packages.
   cache                       Inspect and manage pip's wheel cache.
   index                       Inspect information available from package indexes.
   wheel                       Build wheels from your requirements.
   hash                        Compute hashes of package archives.
   completion                  A helper command used for command completion.
   debug                       Show information useful for debugging.
   help                        Show help for commands.
 
 General Options:
   -h, --help                  Show help.
   --debug                     Let unhandled exceptions propagate outside the
                               main subroutine, instead of logging them to
                               stderr.
   --isolated                  Run pip in an isolated mode, ignoring
                               environment variables and user configuration.
   --require-virtualenv        Allow pip to only run in a virtual environment;
                               exit with an error otherwise.
   --python <python>           Run pip with the specified Python interpreter.
   -v, --verbose               Give more output. Option is additive, and can be
                               used up to 3 times.
   -V, --version               Show version and exit.
   -q, --quiet                 Give less output. Option is additive, and can be
                               used up to 3 times (corresponding to WARNING,
                               ERROR, and CRITICAL logging levels).
   --log <path>                Path to a verbose appending log.
   --no-input                  Disable prompting for input.
   --keyring-provider <keyring_provider>
                               Enable the credential lookup via the keyring
                               library if user input is allowed. Specify which
                               mechanism to use [disabled, import, subprocess].
                               (default: disabled)
   --proxy <proxy>             Specify a proxy in the form
                               scheme://[user:passwd@]proxy.server:port.
   --retries <retries>         Maximum number of retries each connection should
                               attempt (default 5 times).
   --timeout <sec>             Set the socket timeout (default 15 seconds).
   --exists-action <action>    Default action when a path already exists:
                               (s)witch, (i)gnore, (w)ipe, (b)ackup, (a)bort.
   --trusted-host <hostname>   Mark this host or host:port pair as trusted,
                               even though it does not have valid or any HTTPS.
   --cert <path>               Path to PEM-encoded CA certificate bundle. If
                               provided, overrides the default. See 'SSL
                               Certificate Verification' in pip documentation
                               for more information.
   --client-cert <path>        Path to SSL client certificate, a single file
                               containing the private key and the certificate
                               in PEM format.
   --cache-dir <dir>           Store the cache data in <dir>.
   --no-cache-dir              Disable the cache.
   --disable-pip-version-check
                               Don't periodically check PyPI to determine
                               whether a new version of pip is available for
                               download. Implied with --no-index.
   --no-color                  Suppress colored output.
   --no-python-version-warning
                               Silence deprecation warnings for upcoming
                               unsupported Pythons.
   --use-feature <feature>     Enable new functionality, that may be backward
                               incompatible.
   --use-deprecated <feature>  Enable deprecated functionality, that will be
                               removed in the future.
 ```
 
 - - -
 
 ### python3-pip-whl
 
  pip is the Python package installer.  It integrates with virtualenv, doesn't
  do partial installs, can save package state for replaying, can install from
  non-egg sources, and can install from version control repositories.
   
  This is the support package for the PEP 427 wheel version of the package,
  required for using pip inside a virtual environment.
 
 **Installed size:** `1.75 MB`  
 **How to install:** `sudo apt install python3-pip-whl`  
 
 {{< spoiler "Dependencies:" >}}
 * ca-certificates
 {{< /spoiler >}}
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
