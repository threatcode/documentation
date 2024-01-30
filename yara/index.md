---
Title: yara
Homepage: https://virustotal.github.io/yara/
Repository: https://salsa.debian.org/pkg-security-team/yara
Architectures: any all
Version: 4.4.0-1
Metapackages: kali-linux-everything kali-tools-forensics kali-tools-respond 
Icon: images/yara-logo.svg
PackagesInfo: |
 ### libyara-dev
 
  YARA is a tool aimed at helping malware researchers to identify and
  classify malware samples. With YARA, it is possible to create
  descriptions of malware families based on textual or binary patterns
  contained in samples of those families. Each description consists of
  a set of strings and a Boolean expression which determines its logic.
   
  Complex and powerful rules can be created by using binary strings with
  wild-cards, case-insensitive text strings, special operators, regular
  expressions and many other features.
   
  This package provides development libraries and headers.
 
 **Installed size:** `1.34 MB`  
 **How to install:** `sudo apt install libyara-dev`  
 
 {{< spoiler "Dependencies:" >}}
 * libjansson-dev
 * libmagic-dev
 * libssl-dev
 * libyara10 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libyara10
 
  YARA is a tool aimed at helping malware researchers to identify and
  classify malware samples. With YARA, it is possible to create
  descriptions of malware families based on textual or binary patterns
  contained in samples of those families. Each description consists of
  a set of strings and a Boolean expression which determines its logic.
   
  Complex and powerful rules can be created by using binary strings with
  wild-cards, case-insensitive text strings, special operators, regular
  expressions and many other features.
   
  This package provides a shared library.
 
 **Installed size:** `612 KB`  
 **How to install:** `sudo apt install libyara10`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libjansson4 
 * libmagic1 
 * libssl3 
 {{< /spoiler >}}
 
 
 - - -
 
 ### yara
 
  YARA is a tool aimed at helping malware researchers to identify and
  classify malware samples. With YARA, it is possible to create
  descriptions of malware families based on textual or binary patterns
  contained in samples of those families. Each description consists of
  a set of strings and a Boolean expression which determines its logic.
   
  Complex and powerful rules can be created by using binary strings with
  wild-cards, case-insensitive text strings, special operators, regular
  expressions and many other features.
 
 **Installed size:** `86 KB`  
 **How to install:** `sudo apt install yara`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libyara10 
 {{< /spoiler >}}
 
 ##### yara
 
 Find files matching patterns and rules written in a special-purpose language.
 
 ```
 root@kali:~# yara -h
 YARA 4.4.0, the pattern matching swiss army knife.
 Usage: yara [OPTION]... [NAMESPACE:]RULES_FILE... FILE | DIR | PID
 
 Mandatory arguments to long options are mandatory for short options too.
 
        --atom-quality-table=FILE           path to a file with the atom quality table
   -C,  --compiled-rules                    load compiled rules
   -c,  --count                             print only number of matches
   -E,  --strict-escape                     warn on unknown escape sequences
   -d,  --define=VAR=VALUE                  define external variable
   -q,  --disable-console-logs              disable printing console log messages
        --fail-on-warnings                  fail on warnings
   -f,  --fast-scan                         fast matching mode
   -h,  --help                              show this help and exit
   -i,  --identifier=IDENTIFIER             print only rules named IDENTIFIER
        --max-process-memory-chunk=NUMBER   set maximum chunk size while reading process memory (default=1073741824)
   -l,  --max-rules=NUMBER                  abort scanning after matching a NUMBER of rules
        --max-strings-per-rule=NUMBER       set maximum number of strings per rule (default=10000)
   -x,  --module-data=MODULE=FILE           pass FILE's content as extra data to MODULE
   -n,  --negate                            print only not satisfied rules (negate)
   -N,  --no-follow-symlinks                do not follow symlinks when scanning
   -w,  --no-warnings                       disable warnings
   -m,  --print-meta                        print metadata
   -D,  --print-module-data                 print module data
   -M,  --module-names                      show module names
   -e,  --print-namespace                   print rules' namespace
   -S,  --print-stats                       print rules' statistics
   -s,  --print-strings                     print matching strings
   -L,  --print-string-length               print length of matched strings
   -X,  --print-xor-key                     print xor key and plaintext of matched strings
   -g,  --print-tags                        print tags
   -r,  --recursive                         recursively search directories
        --scan-list                         scan files listed in FILE, one per line
   -z,  --skip-larger=NUMBER                skip files larger than the given size when scanning a directory
   -k,  --stack-size=SLOTS                  set maximum stack size (default=16384)
   -t,  --tag=TAG                           print only rules tagged as TAG
   -p,  --threads=NUMBER                    use the specified NUMBER of threads to scan a directory
   -a,  --timeout=SECONDS                   abort scanning after the given number of SECONDS
   -v,  --version                           show version information
 
 Send bug reports and suggestions to: vmalvarez@virustotal.com.
 ```
 
 - - -
 
 ##### yarac
 
 Compile rules to yara
 
 ```
 root@kali:~# yarac -h
 Usage: yarac [OPTION]... [NAMESPACE:]SOURCE_FILE... OUTPUT_FILE
 
        --atom-quality-table=FILE        path to a file with the atom quality table
   -d,  --define=VAR=VALUE               define external variable
        --fail-on-warnings               fail on warnings
   -h,  --help                           show this help and exit
   -E,  --strict-escape                  warn on unknown escape sequences
        --max-strings-per-rule=NUMBER    set maximum number of strings per rule (default=10000)
   -w,  --no-warnings                    disable warnings
   -v,  --version                        show version information
 
 Send bug reports and suggestions to: vmalvarez@virustotal.com
 ```
 
 - - -
 
 ### yara-doc
 
  YARA is a tool aimed at helping malware researchers to identify and
  classify malware samples. With YARA, it is possible to create
  descriptions of malware families based on textual or binary patterns
  contained in samples of those families. Each description consists of
  a set of strings and a Boolean expression which determines its logic.
   
  Complex and powerful rules can be created by using binary strings with
  wild-cards, case-insensitive text strings, special operators, regular
  expressions and many other features.
   
  This package contains the documentation in HTML format.
 
 **Installed size:** `1.41 MB`  
 **How to install:** `sudo apt install yara-doc`  
 
 {{< spoiler "Dependencies:" >}}
 * libjs-sphinxdoc 
 {{< /spoiler >}}
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
