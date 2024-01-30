---
Title: hashrat
Homepage: http://www.cjpaget.co.uk/Code/Hashrat
Repository: https://salsa.debian.org/pkg-security-team/hashrat
Architectures: any
Version: 1.13-1
Metapackages: kali-linux-everything kali-tools-respond 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### hashrat
 
  Hashrat is a hash-generation utility that supports the md5, sha1, sha256,
  sha512, whirlpool, jh-244, jh256, jh-384 and jh-512 hash functions, and
  also the HMAC versions of those functions. It can output in 'traditional'
  format (same as md5sum and shasum and the like), or it's own format.
   
  Hashes can be output in octal, decimal, hexadecimal, uppercase hexadecimal
  or base64.
   
  Hashrat also supports directory recursion, hashing entire devices,
  generating a hash for an entire directory, operations in remote machines
  and several other features. It has a 'CGI' mode that can be used as a
  web-page to lookup hashes.
   
  This tool is useful in forensics investigations and network security.
 
 **Installed size:** `346 KB`  
 **How to install:** `sudo apt install hashrat`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### hashrat
 
 Hashing tool supporting several hashes and recursivity
 
 ```
 root@kali:~# hashrat --help
 Hashrat: version 1.12
 Author: Colum Paget
 Email: colums.projects@gmail.com
 Credits:
 	Thanks for bug reports/advice to: Stephan Hegel, Michael Shigorin <mike@altlinux.org> and Joao Eriberto Mota Filho <eriberto@debian.org>
 	Thanks to the people who invented the hash functions!
 	MD5: Ronald Rivest
 	Whirlpool: Vincent Rijmen, Paulo S. L. M. Barreto
 	JH: Hongjun Wu
 	SHA: The NSA (thanks, but please stop reading my email. It's kinda creepy.).
 
 	Special thanks to Professor Hongjun Wu for taking the time to confirm that his JH algorithm is free for use in GPL programs.
 	Special, special thanks to Joao Eriberto Mota Filho for doing a LOT of work to make hashrat debian ready!
 
 Usage:
     hashrat [options] [path to hash]...
 
     hashrat -c [options] [input file of hashes]...
 
 Options:
   --help          Print this help
   -help           Print this help
   -?              Print this help
   --version       Print program version
   -version        Print program version
   -md5            Use md5 hash algorithm
   -sha1           Use sha1 hash algorithm
   -sha256         Use sha256 hash algorithm
   -sha512         Use sha512 hash algorithm
   -whirl          Use whirlpool hash algorithm
   -whirlpool      Use whirlpool hash algorithm
   -jh224          Use jh-224 hash algorithm
   -jh256          Use jh-256 hash algorithm
   -jh384          Use jh-384 hash algorithm
   -jh512          Use jh-512 hash algorithm
   -hmac           HMAC using specified hash algorithm
   -8              Encode with octal instead of hex
   -10             Encode with decimal instead of hex
   -H              Encode with UPPERCASE hexadecimal
   -HEX            Encode with UPPERCASE hexadecimal
   -64             Encode with base64 instead of hex
   -base64         Encode with base64 instead of hex
   -i64            Encode with base64 with rearranged characters
   -p64            Encode with base64 with a-z,A-Z and _-, for best compatibility with 'allowed characters' in websites.
   -r64            Encode with base64 with a-z,A-Z and _-, rfc4648 compatible.
   -rfc4648        Encode with base64 with a-z,A-Z and _-, rfc4648 compatible.
   -x64            Encode with XXencode style base64.
   -u64            Encode with UUencode style base64.
   -g64            Encode with GEDCOM style base64.
   -a85            Encode with ASCII85.
   -z85            Encode with ZEROMQ variant of ASCII85.
   -t              Output hashes in traditional md5sum, shaXsum format
   -trad           Output hashes in traditional md5sum, shaXsum format
   -bsd            Output hashes in bsdsum format
   -tag            Output hashes in bsdsum format
   --tag           Output hashes in bsdsum format
   -r              Recurse into directories when hashing files
   -hid            Show hidden (starting with .) files
   -hidden         Show hidden (starting with .) files
   -f <listfile>   Hash files listed in <listfile>
   -i <patterns>   Only hash items matching a comma-seperated list of shell patterns
   -x <patterns>   Exclude items matching a comma-sepearted list of shell patterns
   -X <file>       Exclude items matching shell patters stored in <file>
   -name  <patterns> Only hash items matching a comma-seperated list of shell patterns (-name aka 'find')
   -mtime <days>   Only hash items <days> old. Has the same format as the find command, e.g. -10 is younger than ten days, +10 is older than ten, and 10 is ten days old
   -mmin  <mins>   Only hash items <min> minutes old. Has the same format as the find command, e.g. -10 is younger than ten mins, +10 is older than ten, and 10 is ten mins old
   -myear <years>  Only hash items <years> old. Has the same format as the find command, e.g. -10 is younger than ten years, +10 is older than ten, and 10 is ten years old
   -exec           In CHECK or MATCH mode only examine executable files.
   -dups           Search for duplicate files.
   -n <length>     Truncate hashes to <length> bytes
   -segment <length> Break hash up into segments of <length> chars seperated by '-'
   -c              CHECK hashes against list from file (or stdin)
   -cf             CHECK hashes against list but only show failures
   -C <dir>        Recursively CHECK directory against list of files on stdin 
   -Cf <dir>       Recursively CHECK directory against list but only show failures
   -m              MATCH files from a list read from stdin.
   -lm             Read hashes from stdin, upload them to a memcached server (requires the -memcached option).
   -memcached <server> Specify memcached server. (Overrides reading list from stdin if used with -m, -c or -cf).
   -mcd <server>   Specify memcached server. (Overrides reading list from stdin if used with -m, -c or -cf).
   -h <script>     Script to run when a file fails CHECK mode, or is found in MATCH mode.
   -hook <script>  Script to run when a file fails CHECK mode, or is found in FIND mode
   -color          Use ANSI color codes on output when checking hashes.
   -strict         Strict mode: when checking, check file mtime, owner, group, and inode as well as it's hash
   -S              Strict mode: when checking, check file mtime, owner, group, and inode as well as it's hash
   -d              dereference (follow) symlinks
   -fs             Stay on one file system
   -dir            DirMode: Read all files in directory and create one hash for them!
   -dirmode        DirMode: Read all files in directory and create one hash for them!
   -devmode        DevMode: read from a file EVEN OF IT'S A DEVNODE
   -lines          Read lines from stdin and hash each line independently.
   -rawlines       Read lines from stdin and hash each line independently, INCLUDING any trailing whitespace. (This is compatible with 'echo text | md5sum')
   -rl             Read lines from stdin and hash each line independently, INCLUDING any trailing whitespace. (This is compatible with 'echo text | md5sum')
   -cgi            Run in HTTP CGI mode
   -net            Treat 'file' arguments as either ssh or http URLs, and pull files over the network and then hash them (Allows hashing of files on remote machines).
                   URLs are in the format ssh://[username]:[password]@[host]:[port] or http://[username]:[password]@[host]:[port]..
   -idfile <path>  Path to an ssh private key file to use to authenticate INSTEAD OF A PASSWORD when pulling files via ssh.
   -xattr          Use eXtended file ATTRibutes. In hash mode, store hashes in the file attributes, in check mode compare against hashes stored in file attributes.
   -txattr         Use TRUSTED eXtended file ATTRibutes. In hash mode, store hashes in 'trusted' file attributes. 'trusted' attributes can only be read and written by root. Under freebsd this menas SYSTEM attributes.
   -attrs          comma-separated list of filesystem attribute names to be set to the value of the hash.
   -cache          Use hashes stored in 'user' xattr if they're younger than the mtime of the file. This speeds up outputting hashes.
   -u <types>      Update. In checking mode, update hashes for the files as you go. <types> is a comma-separated list of things to update, which can be 'xattr' 'memcached' or a file name. This will update these targets with the hash that was found at the time of checking.
   -hide-input     When reading data from stdin in linemode, set the terminal to not echo characters, thus hiding typed input.
   -star-input     When reading data from stdin in linemode replace characters with stars.
   -xsel           Update X11 clipboard and primary selections to the current hash. This works using Xterm command sequences. The xterm resource 'allowWindowOps' must be set to 'true' for this to work.
 
 
 Hashrat can also detect if it's being run under any of the following names (e.g., via symlinks)
 
   md5sum          run with '-trad -md5'
   shasum          run with '-trad -sha1'
   sha1sum         run with '-trad -sha1'
   sha256sum       run with '-trad -sha256'
   sha512sum       run with '-trad -sha512'
   jh224sum        run with '-trad -jh224'
   jh256sum        run with '-trad -jh256'
   jh384sum        run with '-trad -jh384'
   jh512sum        run with '-trad -jh512'
   whirlpoolsum    run with '-trad -whirl'
   hashrat.cgi     run in web-enabled 'cgi mode'
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
