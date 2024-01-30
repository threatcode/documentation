---
Title: php-defaults
Homepage: 
Repository: https://salsa.debian.org/php-team/php-defaults
Architectures: all
Version: 93
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-labs kali-linux-large kali-linux-nethunter kali-tools-exploitation kali-tools-forensics kali-tools-respond kali-tools-social-engineering kali-tools-web 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### libapache2-mod-php
 
  This package provides the PHP module for the Apache 2 webserver.
   
  PHP (recursive acronym for PHP: Hypertext Preprocessor) is a widely-used
  open source general-purpose scripting language that is especially suited
  for web development and can be embedded into HTML.
   
  This package is a dependency package, which depends on latest stable
  PHP version (currently 8.2).
 
 **Installed size:** `14 KB`  
 **How to install:** `sudo apt install libapache2-mod-php`  
 
 {{< spoiler "Dependencies:" >}}
 * libapache2-mod-php8.2
 {{< /spoiler >}}
 
 
 - - -
 
 ### libphp-embed
 
  This package provides the library /usr/lib/libphp.so which can
  be used by application developers to embed PHP scripting functionality.
   
  PHP (recursive acronym for PHP: Hypertext Preprocessor) is a widely-used
  open source general-purpose scripting language that is especially suited
  for web development and can be embedded into HTML.
   
  This package is a dependency package, which depends on latest stable
  PHP version (currently 8.2).
 
 **Installed size:** `10 KB`  
 **How to install:** `sudo apt install libphp-embed`  
 
 {{< spoiler "Dependencies:" >}}
 * libphp8.2-embed
 {{< /spoiler >}}
 
 
 - - -
 
 ### php
 
  PHP (recursive acronym for PHP: Hypertext Preprocessor) is a widely-used
  open source general-purpose scripting language that is especially suited
  for web development and can be embedded into HTML.
   
  This package is a dependency package, which depends on latest stable
  PHP version (currently 8.2).
 
 **Installed size:** `10 KB`  
 **How to install:** `sudo apt install php`  
 
 {{< spoiler "Dependencies:" >}}
 * php8.2
 {{< /spoiler >}}
 
 
 - - -
 
 ### php-all-dev
 
  This package is a dependency package used as a build dependency for other
  packages to avoid hardcoded dependencies on specific PHP development
  packages.
 
 **Installed size:** `10 KB`  
 **How to install:** `sudo apt install php-all-dev`  
 
 {{< spoiler "Dependencies:" >}}
 * php8.2-dev
 * php8.2-json
 * php8.2-mbstring
 * php8.2-xml
 {{< /spoiler >}}
 
 
 - - -
 
 ### php-bcmath
 
  This package provides a Bcmath module for PHP.
   
  PHP (recursive acronym for PHP: Hypertext Preprocessor) is a widely-used
  open source general-purpose scripting language that is especially suited
  for web development and can be embedded into HTML.
   
  This package is a dependency package, which depends on Debian's default
  PHP version (currently 8.2).
 
 **Installed size:** `10 KB`  
 **How to install:** `sudo apt install php-bcmath`  
 
 {{< spoiler "Dependencies:" >}}
 * php-common
 * php8.2-bcmath
 {{< /spoiler >}}
 
 
 - - -
 
 ### php-bz2
 
  This package provides a bzip2 module for PHP.
   
  PHP (recursive acronym for PHP: Hypertext Preprocessor) is a widely-used
  open source general-purpose scripting language that is especially suited
  for web development and can be embedded into HTML.
   
  This package is a dependency package, which depends on Debian's default
  PHP version (currently 8.2).
 
 **Installed size:** `10 KB`  
 **How to install:** `sudo apt install php-bz2`  
 
 {{< spoiler "Dependencies:" >}}
 * php-common
 * php8.2-bz2
 {{< /spoiler >}}
 
 
 - - -
 
 ### php-cgi
 
  This package provides the /usr/lib/cgi-bin/php CGI interpreter built
  for use in Apache 2 with mod_actions, or any other CGI httpd that
  supports a similar mechanism.  Note that MOST users probably
  want the php-fpm package that provide FastCGI support.
   
  PHP (recursive acronym for PHP: Hypertext Preprocessor) is a widely-used
  open source general-purpose scripting language that is especially suited
  for web development and can be embedded into HTML.
   
  This package is a dependency package, which depends on latest stable
  PHP version (currently 8.2).
 
 **Installed size:** `20 KB`  
 **How to install:** `sudo apt install php-cgi`  
 
 {{< spoiler "Dependencies:" >}}
 * php8.2-cgi
 {{< /spoiler >}}
 
 ##### php-cgi.default
 
 PHP Command Line Interface 'CLI'
 
 ```
 root@kali:~# php-cgi.default -h
 Usage: php-cgi [-q] [-h] [-s] [-v] [-i] [-f <file>]
        php-cgi <file> [args...]
   -a               Run interactively
   -b <address:port>|<port> Bind Path for external FASTCGI Server mode
   -C               Do not chdir to the script's directory
   -c <path>|<file> Look for php.ini file in this directory
   -n               No php.ini file will be used
   -d foo[=bar]     Define INI entry foo with value 'bar'
   -e               Generate extended information for debugger/profiler
   -f <file>        Parse <file>.  Implies `-q'
   -h               This help
   -i               PHP information
   -l               Syntax check only (lint)
   -m               Show compiled in modules
   -q               Quiet-mode.  Suppress HTTP Header output.
   -s               Display colour syntax highlighted source.
   -v               Version number
   -w               Display source with stripped comments and whitespace.
   -z <file>        Load Zend extension <file>.
   -T <count>       Measure execution time of script repeated <count> times.
 ```
 
 - - -
 
 ### php-cli
 
  This package provides the /usr/bin/php command interpreter, useful for
  testing PHP scripts from a shell or performing general shell scripting tasks.
   
  PHP (recursive acronym for PHP: Hypertext Preprocessor) is a widely-used
  open source general-purpose scripting language that is especially suited
  for web development and can be embedded into HTML.
   
  This package is a dependency package, which depends on latest stable
  PHP version (currently 8.2).
 
 **Installed size:** `21 KB`  
 **How to install:** `sudo apt install php-cli`  
 
 {{< spoiler "Dependencies:" >}}
 * php8.2-cli
 {{< /spoiler >}}
 
 ##### phar.default
 
 PHAR (PHP archive) command line tool
 
 ```
 root@kali:~# man phar.default
 PHAR(1)                          User Commands                         PHAR(1)
 
 NAME
        phar, phar.phar - PHAR (PHP archive) command line tool
 
 SYNOPSIS
        phar <command> [options] ...
 
 DESCRIPTION
        The PHAR file format provides a way to put entire PHP applications into
        a  single  file called a "phar" (PHP Archive) for easy distribution and
        installation.
 
        With the phar command you can create, update or extract PHP archives.
 
        Commands: add compress delete extract help help-list info list meta-del
        meta-get meta-set pack sign stub-get stub-set tree version
 
 add command
        Add entries to a PHAR package.
 
        Required arguments:
 
        -f file        Specifies the phar file to work on.
 
        ...            Any number of input files and directories. If -i  is  in
                       use  then  ONLY files and matching the given regular ex-
                       pression are being packed. If -x  is  given  then  files
                       matching that regular expression are NOT being packed.
 
        Optional arguments:
 
        -a alias       Provide an alias name for the phar file.
 
        -c algo        Compression algorithm (see COMPRESSION )
 
        -i regex       Specifies a regular expression for input files.
 
        -l level       Number  of  preceding  subdirectories to strip from file
                       entries
 
        -x regex       Regular expression for input files to exclude.
 
 compress command
        Compress or uncompress all files or a selected entry.
 
        Required arguments:
 
        -c algo        Compression algorithm (see COMPRESSION )
 
        -f file        Specifies the phar file to work on.
 
        Optional arguments:
 
        -e entry       Name of entry to work on (must include PHAR internal di-
                       rectory name if any).
 
 delete command
        Delete entry from a PHAR archive
 
        Required arguments:
 
        -e entry       Name of entry to work on (must include PHAR internal di-
                       rectory name if any).
 
        -f file        Specifies the phar file to work on.
 
 extract command
        Extract a PHAR package to a directory.
 
        Required arguments:
 
        -f file        Specifies the phar file to work on.
 
        Optional arguments:
 
        -i regex       Specifies a regular expression for input files.
 
        -x regex       Regular expression for input files to exclude.
 
        ...            Directory to extract to (defaults to '.').
 
 help command
        This help or help for a selected command.
 
        Optional arguments:
 
        ...            Optional command to retrieve help for.
 
 help-list command
        Lists available commands.
 
 info command
        Get information about a PHAR package.
 
        By using -k it is possible to return a single value.
 
        Required arguments:
 
        -f file        Specifies the phar file to work on.
 
        Optional arguments:
 
        -k index       Subscription index to work on.
 
 list command
        List contents of a PHAR archive.
 
        Required arguments:
 
        -f file        Specifies the phar file to work on.
 
        Optional arguments:
 
        -i regex       Specifies a regular expression for input files.
 
        -x regex       Regular expression for input files to exclude.
 
 meta-del command
        Delete meta information of a PHAR entry or a PHAR package.
 
        If -k is given then the metadata is expected to be  an  array  and  the
        given index is being deleted.
 
        If something was deleted the return value is 0 otherwise it is 1.
 
        Required arguments:
 
        -f file        Specifies the phar file to work on.
 
        Optional arguments:
 
        -e entry       Name of entry to work on (must include PHAR internal di-
                       rectory name if any).
 
        -k index       Subscription index to work on.
 
 meta-get command
        Get  meta  information  of a PHAR entry or a PHAR package in serialized
        from. If no output file is specified for meta data then stdout is being
        used.  You can also specify a particular index using -k. In  that  case
        the  metadata is expected to be an array and the value of the given in-
        dex is returned using echo rather than using serialize. If  that  index
        does not exist or no meta data is present then the return value is 1.
 
        Required arguments:
 
        -f file        Specifies the phar file to work on.
 
        Optional arguments:
 
        -e entry       Name of entry to work on (must include PHAR internal di-
                       rectory name if any).
 
        -k index       Subscription index to work on.
 
 meta-set command
        Set meta data of a PHAR entry or a PHAR package using serialized input.
        If  no  input file is specified for meta data then stdin is being used.
        You can also specify a particular index using  -k.  In  that  case  the
        metadata is expected to be an array and the value of the given index is
        being set.  If the metadata is not present or empty a new array will be
        created.   If  the metadata is present and a flat value then the return
        value is 1. Also using -k the input is been taken directly rather  then
        being serialized.
 
        Required arguments:
 
        -f file        Specifies the phar file to work on.
 
        -m meta        Meta data to store with entry (serialized php data).
 
        Optional arguments:
 
        -e entry       Name of entry to work on (must include PHAR internal di-
                       rectory name if any).
 
        -k index       Subscription index to work on.
 
 pack command
        Pack files into a PHAR archive.
 
        When  using  -s  <stub>,  then the stub file is being excluded from the
        list of input files/dirs.To create an archive that contains PEAR  class
        PHP_Archive then point -p argument to PHP/Archive.php.
 
        Required arguments:
 
        -f file        Specifies the phar file to work on.
 
        ...            Any  number  of input files and directories. If -i is in
                       use then ONLY files and matching the given  regular  ex-
                       pression  are  being  packed.  If -x is given then files
                       matching that regular expression are NOT being packed.
 
        Optional arguments:
 
        -a alias       Provide an alias name for the phar file.
 
        -b bang        Hash-bang   line   to   start    the    archive    (e.g.
                       #!/usr/bin/php).  The hash mark itself '#!' and the new-
                       line character are optional.
 
        -c algo        Compression algorithm (see COMPRESSION )
 
        -h hash        Selects the hash algorithm (see HASH )
 
        -i regex       Specifies a regular expression for input files.
 
        -l level       Number  of  preceding  subdirectories to strip from file
                       entries
 
        -p loader      Location of  PHP_Archive  class  file  (pear  list-files
                       PHP_Archive).You  can  use '0' or '1' to locate it auto-
                       matically using the mentioned pear command.  When  using
                       '0'  the  command does not error out when the class file
                       cannot be located.  This  switch  also  adds  some  code
                       around  the  stub  so that class PHP_Archive gets regis-
                       tered as phar:// stream wrapper if  necessary.  And  fi-
                       nally  this  switch will add the file phar.inc from this
                       package and load it to ensure class Phar is present.
 
        -s stub        Select the stub file.
 
        -x regex       Regular expression for input files to exclude.
 
        -y key         Private key for OpenSSL signing.
 
 sign command
        Set signature hash algorithm.
 
        Required arguments:
 
        -f file        Specifies the phar file to work on.
 
        -h hash        Selects the hash algorithm (see HASH )
 
        Optional arguments:
 
        -y key         Private key for OpenSSL signing.
 
 stub-get command
        Get the stub of a PHAR file. If no output file  is  specified  as  stub
        then stdout is being used.
 
        Required arguments:
 
        -f file        Specifies the phar file to work on.
 
        Optional arguments:
 
        -s stub        Select the stub file.
 
 stub-set command
        Set the stub of a PHAR file. If no input file is specified as stub then
        stdin is being used.
 
        Required arguments:
 
        -f file        Specifies the phar file to work on.
 
        Optional arguments:
 
        -b bang        Hash-bang    line    to    start   the   archive   (e.g.
                       #!/usr/bin/php).  The hash mark itself '#!' and the new-
                       line character are optional.
 
        -p loader      Location of  PHP_Archive  class  file  (pear  list-files
                       PHP_Archive).You  can  use '0' or '1' to locate it auto-
                       matically using the mentioned pear command.  When  using
                       '0'  the  command does not error out when the class file
                       cannot be located.  This  switch  also  adds  some  code
                       around  the  stub  so that class PHP_Archive gets regis-
                       tered as phar:// stream wrapper if  necessary.  And  fi-
                       nally  this  switch will add the file phar.inc from this
                       package and load it to ensure class Phar is present.
 
        -s stub        Select the stub file.
 
 tree command
        Get a directory tree for a PHAR archive.
 
        Required arguments:
 
        -f file        Specifies the phar file to work on.
 
        Optional arguments:
 
        -i regex       Specifies a regular expression for input files.
 
        -x regex       Regular expression for input files to exclude.
 
 version command
        Get information about the PHAR environment and the tool version.
 
 COMPRESSION
        Algorithms:
 
        0              No compression
 
        none           No compression
 
        auto           Automatically select compression algorithm
 
        gz             GZip compression
 
        gzip           GZip compression
 
        bz2            BZip2 compression
 
        bzip2          BZip2 compression
 
 HASH
        Algorithms:
 
        md5            MD5
 
        sha1           SHA1
 
        sha256         SHA256
 
        sha512         SHA512
 
        openssl        OpenSSL using SHA-1
 
        openssl_sha256 OpenSSL using SHA-256
 
        openssl_sha512 OpenSSL using SHA-512
 
 SEE ALSO
        For a more or less complete description of PHAR look here:
        http://php.net/phar
 
 BUGS
        You can view the list of known bugs or report any new bug you found at:
        https://github.com/php/php-src/issues
 
 AUTHORS
        The PHP Group: Thies C. Arntzen, Stig Bakken, Andi Gutmans, Rasmus Ler-
        dorf, Sam Ruby, Sascha Schumann, Zeev  Suraski,  Jim  Winstead,  Andrei
        Zmievski.
 
        Work for the PHP archive was done by Gregory Beaver, Marcus Boerger.
 
        A List of active developers can be found here:
        http://www.php.net/credits.php
 
        And last but not least PHP was developed with the help of a huge amount
        of contributors all around the world.
 
 VERSION INFORMATION
        This manpage describes phar, version 8.2.10.
 
 COPYRIGHT
        Copyright (C) The PHP Group
 
        This source file is subject to version 3.01 of the PHP license, that is
        bundled with this package in the file LICENSE, and is available through
        the world-wide-web at the following url:
        https://www.php.net/license/3_01.txt
 
        If  you did not receive a copy of the PHP license and are unable to ob-
        tain  it  through  the  world-wide-web,  please  send  a  note  to  li-
        cense@php.net so we can mail you a copy immediately.
 
 The PHP Group                        2022                              PHAR(1)
 ```
 
 - - -
 
 ##### phar.phar.default
 
 PHAR (PHP archive) command line tool
 
 ```
 root@kali:~# man phar.phar.default
 PHAR(1)                          User Commands                         PHAR(1)
 
 NAME
        phar, phar.phar - PHAR (PHP archive) command line tool
 
 SYNOPSIS
        phar <command> [options] ...
 
 DESCRIPTION
        The PHAR file format provides a way to put entire PHP applications into
        a  single  file called a "phar" (PHP Archive) for easy distribution and
        installation.
 
        With the phar command you can create, update or extract PHP archives.
 
        Commands: add compress delete extract help help-list info list meta-del
        meta-get meta-set pack sign stub-get stub-set tree version
 
 add command
        Add entries to a PHAR package.
 
        Required arguments:
 
        -f file        Specifies the phar file to work on.
 
        ...            Any number of input files and directories. If -i  is  in
                       use  then  ONLY files and matching the given regular ex-
                       pression are being packed. If -x  is  given  then  files
                       matching that regular expression are NOT being packed.
 
        Optional arguments:
 
        -a alias       Provide an alias name for the phar file.
 
        -c algo        Compression algorithm (see COMPRESSION )
 
        -i regex       Specifies a regular expression for input files.
 
        -l level       Number  of  preceding  subdirectories to strip from file
                       entries
 
        -x regex       Regular expression for input files to exclude.
 
 compress command
        Compress or uncompress all files or a selected entry.
 
        Required arguments:
 
        -c algo        Compression algorithm (see COMPRESSION )
 
        -f file        Specifies the phar file to work on.
 
        Optional arguments:
 
        -e entry       Name of entry to work on (must include PHAR internal di-
                       rectory name if any).
 
 delete command
        Delete entry from a PHAR archive
 
        Required arguments:
 
        -e entry       Name of entry to work on (must include PHAR internal di-
                       rectory name if any).
 
        -f file        Specifies the phar file to work on.
 
 extract command
        Extract a PHAR package to a directory.
 
        Required arguments:
 
        -f file        Specifies the phar file to work on.
 
        Optional arguments:
 
        -i regex       Specifies a regular expression for input files.
 
        -x regex       Regular expression for input files to exclude.
 
        ...            Directory to extract to (defaults to '.').
 
 help command
        This help or help for a selected command.
 
        Optional arguments:
 
        ...            Optional command to retrieve help for.
 
 help-list command
        Lists available commands.
 
 info command
        Get information about a PHAR package.
 
        By using -k it is possible to return a single value.
 
        Required arguments:
 
        -f file        Specifies the phar file to work on.
 
        Optional arguments:
 
        -k index       Subscription index to work on.
 
 list command
        List contents of a PHAR archive.
 
        Required arguments:
 
        -f file        Specifies the phar file to work on.
 
        Optional arguments:
 
        -i regex       Specifies a regular expression for input files.
 
        -x regex       Regular expression for input files to exclude.
 
 meta-del command
        Delete meta information of a PHAR entry or a PHAR package.
 
        If -k is given then the metadata is expected to be  an  array  and  the
        given index is being deleted.
 
        If something was deleted the return value is 0 otherwise it is 1.
 
        Required arguments:
 
        -f file        Specifies the phar file to work on.
 
        Optional arguments:
 
        -e entry       Name of entry to work on (must include PHAR internal di-
                       rectory name if any).
 
        -k index       Subscription index to work on.
 
 meta-get command
        Get  meta  information  of a PHAR entry or a PHAR package in serialized
        from. If no output file is specified for meta data then stdout is being
        used.  You can also specify a particular index using -k. In  that  case
        the  metadata is expected to be an array and the value of the given in-
        dex is returned using echo rather than using serialize. If  that  index
        does not exist or no meta data is present then the return value is 1.
 
        Required arguments:
 
        -f file        Specifies the phar file to work on.
 
        Optional arguments:
 
        -e entry       Name of entry to work on (must include PHAR internal di-
                       rectory name if any).
 
        -k index       Subscription index to work on.
 
 meta-set command
        Set meta data of a PHAR entry or a PHAR package using serialized input.
        If  no  input file is specified for meta data then stdin is being used.
        You can also specify a particular index using  -k.  In  that  case  the
        metadata is expected to be an array and the value of the given index is
        being set.  If the metadata is not present or empty a new array will be
        created.   If  the metadata is present and a flat value then the return
        value is 1. Also using -k the input is been taken directly rather  then
        being serialized.
 
        Required arguments:
 
        -f file        Specifies the phar file to work on.
 
        -m meta        Meta data to store with entry (serialized php data).
 
        Optional arguments:
 
        -e entry       Name of entry to work on (must include PHAR internal di-
                       rectory name if any).
 
        -k index       Subscription index to work on.
 
 pack command
        Pack files into a PHAR archive.
 
        When  using  -s  <stub>,  then the stub file is being excluded from the
        list of input files/dirs.To create an archive that contains PEAR  class
        PHP_Archive then point -p argument to PHP/Archive.php.
 
        Required arguments:
 
        -f file        Specifies the phar file to work on.
 
        ...            Any  number  of input files and directories. If -i is in
                       use then ONLY files and matching the given  regular  ex-
                       pression  are  being  packed.  If -x is given then files
                       matching that regular expression are NOT being packed.
 
        Optional arguments:
 
        -a alias       Provide an alias name for the phar file.
 
        -b bang        Hash-bang   line   to   start    the    archive    (e.g.
                       #!/usr/bin/php).  The hash mark itself '#!' and the new-
                       line character are optional.
 
        -c algo        Compression algorithm (see COMPRESSION )
 
        -h hash        Selects the hash algorithm (see HASH )
 
        -i regex       Specifies a regular expression for input files.
 
        -l level       Number  of  preceding  subdirectories to strip from file
                       entries
 
        -p loader      Location of  PHP_Archive  class  file  (pear  list-files
                       PHP_Archive).You  can  use '0' or '1' to locate it auto-
                       matically using the mentioned pear command.  When  using
                       '0'  the  command does not error out when the class file
                       cannot be located.  This  switch  also  adds  some  code
                       around  the  stub  so that class PHP_Archive gets regis-
                       tered as phar:// stream wrapper if  necessary.  And  fi-
                       nally  this  switch will add the file phar.inc from this
                       package and load it to ensure class Phar is present.
 
        -s stub        Select the stub file.
 
        -x regex       Regular expression for input files to exclude.
 
        -y key         Private key for OpenSSL signing.
 
 sign command
        Set signature hash algorithm.
 
        Required arguments:
 
        -f file        Specifies the phar file to work on.
 
        -h hash        Selects the hash algorithm (see HASH )
 
        Optional arguments:
 
        -y key         Private key for OpenSSL signing.
 
 stub-get command
        Get the stub of a PHAR file. If no output file  is  specified  as  stub
        then stdout is being used.
 
        Required arguments:
 
        -f file        Specifies the phar file to work on.
 
        Optional arguments:
 
        -s stub        Select the stub file.
 
 stub-set command
        Set the stub of a PHAR file. If no input file is specified as stub then
        stdin is being used.
 
        Required arguments:
 
        -f file        Specifies the phar file to work on.
 
        Optional arguments:
 
        -b bang        Hash-bang    line    to    start   the   archive   (e.g.
                       #!/usr/bin/php).  The hash mark itself '#!' and the new-
                       line character are optional.
 
        -p loader      Location of  PHP_Archive  class  file  (pear  list-files
                       PHP_Archive).You  can  use '0' or '1' to locate it auto-
                       matically using the mentioned pear command.  When  using
                       '0'  the  command does not error out when the class file
                       cannot be located.  This  switch  also  adds  some  code
                       around  the  stub  so that class PHP_Archive gets regis-
                       tered as phar:// stream wrapper if  necessary.  And  fi-
                       nally  this  switch will add the file phar.inc from this
                       package and load it to ensure class Phar is present.
 
        -s stub        Select the stub file.
 
 tree command
        Get a directory tree for a PHAR archive.
 
        Required arguments:
 
        -f file        Specifies the phar file to work on.
 
        Optional arguments:
 
        -i regex       Specifies a regular expression for input files.
 
        -x regex       Regular expression for input files to exclude.
 
 version command
        Get information about the PHAR environment and the tool version.
 
 COMPRESSION
        Algorithms:
 
        0              No compression
 
        none           No compression
 
        auto           Automatically select compression algorithm
 
        gz             GZip compression
 
        gzip           GZip compression
 
        bz2            BZip2 compression
 
        bzip2          BZip2 compression
 
 HASH
        Algorithms:
 
        md5            MD5
 
        sha1           SHA1
 
        sha256         SHA256
 
        sha512         SHA512
 
        openssl        OpenSSL using SHA-1
 
        openssl_sha256 OpenSSL using SHA-256
 
        openssl_sha512 OpenSSL using SHA-512
 
 SEE ALSO
        For a more or less complete description of PHAR look here:
        http://php.net/phar
 
 BUGS
        You can view the list of known bugs or report any new bug you found at:
        https://github.com/php/php-src/issues
 
 AUTHORS
        The PHP Group: Thies C. Arntzen, Stig Bakken, Andi Gutmans, Rasmus Ler-
        dorf, Sam Ruby, Sascha Schumann, Zeev  Suraski,  Jim  Winstead,  Andrei
        Zmievski.
 
        Work for the PHP archive was done by Gregory Beaver, Marcus Boerger.
 
        A List of active developers can be found here:
        http://www.php.net/credits.php
 
        And last but not least PHP was developed with the help of a huge amount
        of contributors all around the world.
 
 VERSION INFORMATION
        This manpage describes phar, version 8.2.10.
 
 COPYRIGHT
        Copyright (C) The PHP Group
 
        This source file is subject to version 3.01 of the PHP license, that is
        bundled with this package in the file LICENSE, and is available through
        the world-wide-web at the following url:
        https://www.php.net/license/3_01.txt
 
        If  you did not receive a copy of the PHP license and are unable to ob-
        tain  it  through  the  world-wide-web,  please  send  a  note  to  li-
        cense@php.net so we can mail you a copy immediately.
 
 The PHP Group                        2022                              PHAR(1)
 ```
 
 - - -
 
 ##### php.default
 
 PHP Command Line Interface 'CLI'
 
 ```
 root@kali:~# php.default -h
 Usage: php [options] [-f] <file> [--] [args...]
    php [options] -r <code> [--] [args...]
    php [options] [-B <begin_code>] -R <code> [-E <end_code>] [--] [args...]
    php [options] [-B <begin_code>] -F <file> [-E <end_code>] [--] [args...]
    php [options] -S <addr>:<port> [-t docroot] [router]
    php [options] -- [args...]
    php [options] -a
 
   -a               Run as interactive shell (requires readline extension)
   -c <path>|<file> Look for php.ini file in this directory
   -n               No configuration (ini) files will be used
   -d foo[=bar]     Define INI entry foo with value 'bar'
   -e               Generate extended information for debugger/profiler
   -f <file>        Parse and execute <file>.
   -h               This help
   -i               PHP information
   -l               Syntax check only (lint)
   -m               Show compiled in modules
   -r <code>        Run PHP <code> without using script tags <?..?>
   -B <begin_code>  Run PHP <begin_code> before processing input lines
   -R <code>        Run PHP <code> for every input line
   -F <file>        Parse and execute <file> for every input line
   -E <end_code>    Run PHP <end_code> after processing all input lines
   -H               Hide any passed arguments from external tools.
   -S <addr>:<port> Run with built-in web server.
   -t <docroot>     Specify document root <docroot> for built-in web server.
   -s               Output HTML syntax highlighted source.
   -v               Version number
   -w               Output source with stripped comments and whitespace.
   -z <file>        Load Zend extension <file>.
 
   args...          Arguments passed to script. Use -- args when first argument
                    starts with - or script is read from stdin
 
   --ini            Show configuration file names
 
   --rf <name>      Show information about function <name>.
   --rc <name>      Show information about class <name>.
   --re <name>      Show information about extension <name>.
   --rz <name>      Show information about Zend extension <name>.
   --ri <name>      Show configuration for extension <name>.
 
 ```
 
 - - -
 
 ### php-common
 
  This package contains common utilities shared among all packaged PHP
  versions.
   
  PHP (recursive acronym for PHP: Hypertext Preprocessor) is a widely-used
  open source general-purpose scripting language that is especially suited
  for web development and can be embedded into HTML.
 
 **Installed size:** `70 KB`  
 **How to install:** `sudo apt install php-common`  
 
 {{< spoiler "Dependencies:" >}}
 * psmisc 
 {{< /spoiler >}}
 
 ##### phpdismod
 
 
 ```
 root@kali:~# phpdismod -h
 usage: phpdismod [ -v ALL|php_version ] [ -s ALL|sapi_name ] module_name [ module_name_2 ]
 ```
 
 - - -
 
 ##### phpenmod
 
 
 ```
 root@kali:~# phpenmod -h
 usage: phpenmod [ -v ALL|php_version ] [ -s ALL|sapi_name ] module_name [ module_name_2 ]
 ```
 
 - - -
 
 ##### phpquery
 
 
 ```
 root@kali:~# phpquery -h
 usage: phpquery [ -d ] [ -q ] -v version_name -s sapi_name [ -m module_name ] [ -M ] [ -S ] [ -V ]
 ```
 
 - - -
 
 ### php-curl
 
  This package provides a CURL module for PHP.
   
  PHP (recursive acronym for PHP: Hypertext Preprocessor) is a widely-used
  open source general-purpose scripting language that is especially suited
  for web development and can be embedded into HTML.
   
  This package is a dependency package, which depends on Debian's default
  PHP version (currently 8.2).
 
 **Installed size:** `10 KB`  
 **How to install:** `sudo apt install php-curl`  
 
 {{< spoiler "Dependencies:" >}}
 * php-common
 * php8.2-curl
 {{< /spoiler >}}
 
 
 - - -
 
 ### php-dev
 
  Headers and other PHP needed for compiling additional modules.
   
  PHP (recursive acronym for PHP: Hypertext Preprocessor) is a widely-used
  open source general-purpose scripting language that is especially suited
  for web development and can be embedded into HTML.
   
  This package is a dependency package, which depends on latest stable
  PHP version (currently 8.2).
 
 **Installed size:** `19 KB`  
 **How to install:** `sudo apt install php-dev`  
 
 {{< spoiler "Dependencies:" >}}
 * php8.2-dev
 {{< /spoiler >}}
 
 ##### php-config.default
 
 Get information about PHP configuration and compile options
 
 ```
 root@kali:~# php-config.default -h
 Usage: /usr/bin/php-config.default [OPTION]
 Options:
   --prefix            [/usr]
   --includes          [-I/usr/include/php/20220829 -I/usr/include/php/20220829/main -I/usr/include/php/20220829/TSRM -I/usr/include/php/20220829/Zend -I/usr/include/php/20220829/ext -I/usr/include/php/20220829/ext/date/lib ]
   --ldflags           [-L/usr/lib/php/20220829 ]
   --libs              [-lcrypt   -lrt -lm  -lxml2 -lssl -lcrypto -lpcre2-8 -lz -lsodium -largon2 -lrt -ldl -lcrypt ]
   --extension-dir     [/usr/lib/php/20220829]
   --include-dir       [/usr/include/php/20220829]
   --man-dir           [/usr/share/man]
   --php-binary        [/usr/bin/php8.2]
   --php-sapis         [apache2handler cgi cli fpm phpdbg ]
   --phpapi            [20220829]
   --ini-path          [/etc/php/8.2/cli]
   --ini-dir           [/etc/php/8.2/cli/conf.d]
   --configure-options [--includedir=/usr/include --mandir=/usr/share/man --infodir=/usr/share/info --disable-option-checking --disable-silent-rules --libdir=/usr/lib/x86_64-linux-gnu --libexecdir=/usr/lib/x86_64-linux-gnu --disable-maintainer-mode --disable-dependency-tracking --prefix=/usr --enable-cli --disable-cgi --disable-phpdbg --with-config-file-path=/etc/php/8.2/cli --with-config-file-scan-dir=/etc/php/8.2/cli/conf.d --build=x86_64-linux-gnu --host=x86_64-linux-gnu --config-cache --cache-file=/tmp/buildd/nonexistent/config.cache --libdir=${prefix}/lib/php --libexecdir=${prefix}/lib/php --datadir=${prefix}/share/php/8.2 --program-suffix=8.2 --sysconfdir=/etc --localstatedir=/var --mandir=/usr/share/man --disable-all --disable-debug --disable-rpath --disable-static --enable-dtrace --with-pic --with-layout=GNU --without-pear --enable-filter --with-openssl --with-password-argon2=/usr --with-external-pcre --enable-hash --with-mhash=/usr --with-libxml --enable-session --with-sodium --with-system-tzdata --with-zlib=/usr --with-zlib-dir=/usr --enable-pcntl --with-libedit=shared,/usr build_alias=x86_64-linux-gnu host_alias=x86_64-linux-gnu CFLAGS=-g -O2 -fstack-protector-strong -fstack-clash-protection -Wformat -Werror=format-security -fcf-protection -O2 -Wall -pedantic -fsigned-char -fno-strict-aliasing -DOPENSSL_SUPPRESS_DEPRECATED -g]
   --version           [8.2.10]
   --vernum            [80210]
 ```
 
 - - -
 
 ##### phpize.default
 
 Prepare a PHP extension for compiling
 
 ```
 root@kali:~# phpize.default --help
 Usage: /usr/bin/phpize.default [--clean|--help|--version|-v]
 ```
 
 - - -
 
 ### php-enchant
 
  This package provides a Enchant module for PHP.
   
  PHP (recursive acronym for PHP: Hypertext Preprocessor) is a widely-used
  open source general-purpose scripting language that is especially suited
  for web development and can be embedded into HTML.
   
  This package is a dependency package, which depends on Debian's default
  PHP version (currently 8.2).
 
 **Installed size:** `10 KB`  
 **How to install:** `sudo apt install php-enchant`  
 
 {{< spoiler "Dependencies:" >}}
 * php-common
 * php8.2-enchant
 {{< /spoiler >}}
 
 
 - - -
 
 ### php-fpm
 
  This package provides the Fast Process Manager interpreter that runs
  as a daemon and receives Fast/CGI requests.
   
  PHP (recursive acronym for PHP: Hypertext Preprocessor) is a widely-used
  open source general-purpose scripting language that is especially suited
  for web development and can be embedded into HTML.
   
  This package is a dependency package, which depends on latest stable
  PHP version (currently 8.2).
 
 **Installed size:** `10 KB`  
 **How to install:** `sudo apt install php-fpm`  
 
 {{< spoiler "Dependencies:" >}}
 * php8.2-fpm
 {{< /spoiler >}}
 
 
 - - -
 
 ### php-gd
 
  This package provides a GD module for PHP.
   
  PHP (recursive acronym for PHP: Hypertext Preprocessor) is a widely-used
  open source general-purpose scripting language that is especially suited
  for web development and can be embedded into HTML.
   
  This package is a dependency package, which depends on Debian's default
  PHP version (currently 8.2).
 
 **Installed size:** `10 KB`  
 **How to install:** `sudo apt install php-gd`  
 
 {{< spoiler "Dependencies:" >}}
 * php-common
 * php8.2-gd
 {{< /spoiler >}}
 
 
 - - -
 
 ### php-gmp
 
  This package provides a GMP module for PHP.
   
  PHP (recursive acronym for PHP: Hypertext Preprocessor) is a widely-used
  open source general-purpose scripting language that is especially suited
  for web development and can be embedded into HTML.
   
  This package is a dependency package, which depends on Debian's default
  PHP version (currently 8.2).
 
 **Installed size:** `10 KB`  
 **How to install:** `sudo apt install php-gmp`  
 
 {{< spoiler "Dependencies:" >}}
 * php-common
 * php8.2-gmp
 {{< /spoiler >}}
 
 
 - - -
 
 ### php-imap
 
  This package provides a IMAP module for PHP.
   
  PHP (recursive acronym for PHP: Hypertext Preprocessor) is a widely-used
  open source general-purpose scripting language that is especially suited
  for web development and can be embedded into HTML.
   
  This package is a dependency package, which depends on Debian's default
  PHP version (currently 8.2).
 
 **Installed size:** `10 KB`  
 **How to install:** `sudo apt install php-imap`  
 
 {{< spoiler "Dependencies:" >}}
 * php-common
 * php8.2-imap
 {{< /spoiler >}}
 
 
 - - -
 
 ### php-interbase
 
  This package provides a Interbase module for PHP.
   
  PHP (recursive acronym for PHP: Hypertext Preprocessor) is a widely-used
  open source general-purpose scripting language that is especially suited
  for web development and can be embedded into HTML.
   
  This package is a dependency package, which depends on Debian's default
  PHP version (currently 8.2).
 
 **Installed size:** `10 KB`  
 **How to install:** `sudo apt install php-interbase`  
 
 {{< spoiler "Dependencies:" >}}
 * php-common
 * php8.2-interbase
 {{< /spoiler >}}
 
 
 - - -
 
 ### php-intl
 
  This package provides a Internationalisation module for PHP.
   
  PHP (recursive acronym for PHP: Hypertext Preprocessor) is a widely-used
  open source general-purpose scripting language that is especially suited
  for web development and can be embedded into HTML.
   
  This package is a dependency package, which depends on Debian's default
  PHP version (currently 8.2).
 
 **Installed size:** `10 KB`  
 **How to install:** `sudo apt install php-intl`  
 
 {{< spoiler "Dependencies:" >}}
 * php-common
 * php8.2-intl
 {{< /spoiler >}}
 
 
 - - -
 
 ### php-json
 
  This package provides a JSON module for PHP.
   
  PHP (recursive acronym for PHP: Hypertext Preprocessor) is a widely-used
  open source general-purpose scripting language that is especially suited
  for web development and can be embedded into HTML.
   
  This package is a dependency package, which depends on Debian's default
  PHP version (currently 8.2).
 
 **Installed size:** `10 KB`  
 **How to install:** `sudo apt install php-json`  
 
 {{< spoiler "Dependencies:" >}}
 * php-common
 * php8.2-json
 {{< /spoiler >}}
 
 
 - - -
 
 ### php-ldap
 
  This package provides a LDAP module for PHP.
   
  PHP (recursive acronym for PHP: Hypertext Preprocessor) is a widely-used
  open source general-purpose scripting language that is especially suited
  for web development and can be embedded into HTML.
   
  This package is a dependency package, which depends on Debian's default
  PHP version (currently 8.2).
 
 **Installed size:** `10 KB`  
 **How to install:** `sudo apt install php-ldap`  
 
 {{< spoiler "Dependencies:" >}}
 * php-common
 * php8.2-ldap
 {{< /spoiler >}}
 
 
 - - -
 
 ### php-mbstring
 
  This package provides a MBSTRING module for PHP.
   
  PHP (recursive acronym for PHP: Hypertext Preprocessor) is a widely-used
  open source general-purpose scripting language that is especially suited
  for web development and can be embedded into HTML.
   
  This package is a dependency package, which depends on Debian's default
  PHP version (currently 8.2).
 
 **Installed size:** `10 KB`  
 **How to install:** `sudo apt install php-mbstring`  
 
 {{< spoiler "Dependencies:" >}}
 * php-common
 * php8.2-mbstring
 {{< /spoiler >}}
 
 
 - - -
 
 ### php-mysql
 
  This package provides a MySQL module for PHP.
   
  PHP (recursive acronym for PHP: Hypertext Preprocessor) is a widely-used
  open source general-purpose scripting language that is especially suited
  for web development and can be embedded into HTML.
   
  This package is a dependency package, which depends on Debian's default
  PHP version (currently 8.2).
 
 **Installed size:** `10 KB`  
 **How to install:** `sudo apt install php-mysql`  
 
 {{< spoiler "Dependencies:" >}}
 * php-common
 * php8.2-mysql
 {{< /spoiler >}}
 
 
 - - -
 
 ### php-odbc
 
  This package provides a ODBC module for PHP.
   
  PHP (recursive acronym for PHP: Hypertext Preprocessor) is a widely-used
  open source general-purpose scripting language that is especially suited
  for web development and can be embedded into HTML.
   
  This package is a dependency package, which depends on Debian's default
  PHP version (currently 8.2).
 
 **Installed size:** `10 KB`  
 **How to install:** `sudo apt install php-odbc`  
 
 {{< spoiler "Dependencies:" >}}
 * php-common
 * php8.2-odbc
 {{< /spoiler >}}
 
 
 - - -
 
 ### php-pgsql
 
  This package provides a PostgreSQL module for PHP.
   
  PHP (recursive acronym for PHP: Hypertext Preprocessor) is a widely-used
  open source general-purpose scripting language that is especially suited
  for web development and can be embedded into HTML.
   
  This package is a dependency package, which depends on Debian's default
  PHP version (currently 8.2).
 
 **Installed size:** `10 KB`  
 **How to install:** `sudo apt install php-pgsql`  
 
 {{< spoiler "Dependencies:" >}}
 * php-common
 * php8.2-pgsql
 {{< /spoiler >}}
 
 
 - - -
 
 ### php-phpdbg
 
  This package provides the /usr/bin/phpdbg command interpreter, useful for
  stepthrough debugging of PHP code.
   
  PHP (recursive acronym for PHP: Hypertext Preprocessor) is a widely-used
  open source general-purpose scripting language that is especially suited
  for web development and can be embedded into HTML.
   
  This package is a dependency package, which depends on latest stable
  PHP version (currently 8.2).
 
 **Installed size:** `17 KB`  
 **How to install:** `sudo apt install php-phpdbg`  
 
 {{< spoiler "Dependencies:" >}}
 * php8.2-phpdbg
 {{< /spoiler >}}
 
 ##### phpdbg.default
 
 The interactive PHP debugger
 
 ```
 root@kali:~# phpdbg.default -h
 
 phpdbg is a lightweight, powerful and easy to use debugging platform for
 PHP5.4+
 It supports the following commands:
 
 Information
   list      list PHP source
   info      displays information on the debug session
   print     show opcodes
   frame     select a stack frame and print a stack frame summary
   generator show active generators or select a generator frame
   back      shows the current backtrace
   help      provide help on a topic
 
 Starting and Stopping Execution
   exec      set execution context
   stdin     set executing script from stdin
   run       attempt execution
   step      continue execution until other line is reached
   continue  continue execution
   until     continue execution up to the given location
   next      continue execution up to the given location and halt on the first
 line after it
   finish    continue up to end of the current execution frame
   leave     continue up to end of the current execution frame and halt after
 the calling instruction
   break     set a breakpoint at the specified target
   watch     set a watchpoint on $variable
   clear     clear one or all breakpoints
   clean     clean the execution environment
 
 Miscellaneous
   set       set the phpdbg configuration
   source    execute a phpdbginit script
   register  register a phpdbginit function as a command alias
   sh        shell a command
   ev        evaluate some code
   quit      exit phpdbg
 
 Type help <command> or (help alias) to get detailed help on any of the above
 ---Type <return> to continue or q <return> to quit---
 ```
 
 - - -
 
 ### php-pspell
 
  This package provides a pspell module for PHP.
   
  PHP (recursive acronym for PHP: Hypertext Preprocessor) is a widely-used
  open source general-purpose scripting language that is especially suited
  for web development and can be embedded into HTML.
   
  This package is a dependency package, which depends on Debian's default
  PHP version (currently 8.2).
 
 **Installed size:** `10 KB`  
 **How to install:** `sudo apt install php-pspell`  
 
 {{< spoiler "Dependencies:" >}}
 * php-common
 * php8.2-pspell
 {{< /spoiler >}}
 
 
 - - -
 
 ### php-readline
 
  This package provides a readline module for PHP.
   
  PHP (recursive acronym for PHP: Hypertext Preprocessor) is a widely-used
  open source general-purpose scripting language that is especially suited
  for web development and can be embedded into HTML.
   
  This package is a dependency package, which depends on Debian's default
  PHP version (currently 8.2).
 
 **Installed size:** `10 KB`  
 **How to install:** `sudo apt install php-readline`  
 
 {{< spoiler "Dependencies:" >}}
 * php-common
 * php8.2-readline
 {{< /spoiler >}}
 
 
 - - -
 
 ### php-snmp
 
  This package provides a SNMP module for PHP.
   
  PHP (recursive acronym for PHP: Hypertext Preprocessor) is a widely-used
  open source general-purpose scripting language that is especially suited
  for web development and can be embedded into HTML.
   
  This package is a dependency package, which depends on Debian's default
  PHP version (currently 8.2).
 
 **Installed size:** `10 KB`  
 **How to install:** `sudo apt install php-snmp`  
 
 {{< spoiler "Dependencies:" >}}
 * php-common
 * php8.2-snmp
 {{< /spoiler >}}
 
 
 - - -
 
 ### php-soap
 
  This package provides a SOAP module for PHP.
   
  PHP (recursive acronym for PHP: Hypertext Preprocessor) is a widely-used
  open source general-purpose scripting language that is especially suited
  for web development and can be embedded into HTML.
   
  This package is a dependency package, which depends on Debian's default
  PHP version (currently 8.2).
 
 **Installed size:** `10 KB`  
 **How to install:** `sudo apt install php-soap`  
 
 {{< spoiler "Dependencies:" >}}
 * php-common
 * php8.2-soap
 {{< /spoiler >}}
 
 
 - - -
 
 ### php-sqlite3
 
  This package provides a SQLite3 module for PHP.
   
  PHP (recursive acronym for PHP: Hypertext Preprocessor) is a widely-used
  open source general-purpose scripting language that is especially suited
  for web development and can be embedded into HTML.
   
  This package is a dependency package, which depends on Debian's default
  PHP version (currently 8.2).
 
 **Installed size:** `10 KB`  
 **How to install:** `sudo apt install php-sqlite3`  
 
 {{< spoiler "Dependencies:" >}}
 * php-common
 * php8.2-sqlite3
 {{< /spoiler >}}
 
 
 - - -
 
 ### php-sybase
 
  This package provides a Sybase module for PHP.
   
  PHP (recursive acronym for PHP: Hypertext Preprocessor) is a widely-used
  open source general-purpose scripting language that is especially suited
  for web development and can be embedded into HTML.
   
  This package is a dependency package, which depends on Debian's default
  PHP version (currently 8.2).
 
 **Installed size:** `10 KB`  
 **How to install:** `sudo apt install php-sybase`  
 
 {{< spoiler "Dependencies:" >}}
 * php-common
 * php8.2-sybase
 {{< /spoiler >}}
 
 
 - - -
 
 ### php-tidy
 
  This package provides a tidy module for PHP.
   
  PHP (recursive acronym for PHP: Hypertext Preprocessor) is a widely-used
  open source general-purpose scripting language that is especially suited
  for web development and can be embedded into HTML.
   
  This package is a dependency package, which depends on Debian's default
  PHP version (currently 8.2).
 
 **Installed size:** `10 KB`  
 **How to install:** `sudo apt install php-tidy`  
 
 {{< spoiler "Dependencies:" >}}
 * php-common
 * php8.2-tidy
 {{< /spoiler >}}
 
 
 - - -
 
 ### php-xml
 
  This package provides a DOM, SimpleXML, WDDX, XML, and XSL module for PHP.
   
  PHP (recursive acronym for PHP: Hypertext Preprocessor) is a widely-used
  open source general-purpose scripting language that is especially suited
  for web development and can be embedded into HTML.
   
  This package is a dependency package, which depends on Debian's default
  PHP version (currently 8.2).
 
 **Installed size:** `10 KB`  
 **How to install:** `sudo apt install php-xml`  
 
 {{< spoiler "Dependencies:" >}}
 * php-common
 * php8.2-xml
 {{< /spoiler >}}
 
 
 - - -
 
 ### php-zip
 
  This package provides a Zip module for PHP.
   
  PHP (recursive acronym for PHP: Hypertext Preprocessor) is a widely-used
  open source general-purpose scripting language that is especially suited
  for web development and can be embedded into HTML.
   
  This package is a dependency package, which depends on Debian's default
  PHP version (currently 8.2).
 
 **Installed size:** `10 KB`  
 **How to install:** `sudo apt install php-zip`  
 
 {{< spoiler "Dependencies:" >}}
 * php-common
 * php8.2-zip
 {{< /spoiler >}}
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
