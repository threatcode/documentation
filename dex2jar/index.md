---
Title: dex2jar
Homepage: https://github.com/pxb1988/dex2jar/tree/2.x
Repository: https://gitlab.com/kalilinux/packages/dex2jar
Architectures: all
Version: 2.1~nightly-28-0kali2
Metapackages: kali-linux-everything kali-linux-large kali-tools-reverse-engineering 
Icon: images/dex2jar-logo.svg
PackagesInfo: |
 ### dex2jar
 
  dex2jar contains 4 compments:
   
  dex-reader is designed to read the Dalvik Executable
  (.dex/.odex) format. It has a light weight API similar
  with ASM. An example here
  dex-translator is designed to do the convert job. It reads
  the dex instruction to dex-ir format, after some optimize,
  convert to ASM format.
  dex-ir used by dex-translator, is designed to represent
  the dex instruction
  dex-tools tools to work with .class files.
 
 **Installed size:** `5.80 MB`  
 **How to install:** `sudo apt install dex2jar`  
 
 {{< spoiler "Dependencies:" >}}
 * default-jre
 {{< /spoiler >}}
 
 ##### d2j-apk-sign
 
 
 ```
 root@kali:~# d2j-apk-sign -h
 d2j-apk-sign -- Sign an android apk file use a test certificate.
 usage: d2j-apk-sign [options] <apk>
 options:
  -f,--force                   force overwrite
  -h,--help                    Print this help message
  -o,--output <out-apk-file>   output .apk file, default is $current_dir/[apk-nam
                               e]-signed.apk
  -t,--tiny                    use tiny sign
 version: 2.1-SNAPSHOT
 ```
 
 - - -
 
 ##### d2j-asm-verify
 
 
 ```
 root@kali:~# d2j-asm-verify -h
 d2j-asm-verify -- Verify .class in jar
 usage: d2j-asm-verify [options] <jar0> [jar1 ... jarN]
 options:
  -d,--detail   Print detail error message
  -h,--help     Print this help message
 version: 2.1-SNAPSHOT
 ```
 
 - - -
 
 ##### d2j-baksmali
 
 
 ```
 root@kali:~# d2j-baksmali -h
 d2j-baksmali -- disassembles and/or dumps a dex file
 usage: d2j-baksmali [options] <dex>
 options:
  -b,--no-debug-info            [not impl] don't write out debug info (.local, .p
                                aram, .line, etc.)
  -f,--force                    force overwrite
  -h,--help                     Print this help message
  -l,--use-locals               output the .locals directive with the number of n
                                on-parameter registers, rather than the .register
  -o,--output <out>             output dir of .smali files, default is $current_d
                                ir/[jar-name]-out/
  -p,--no-parameter-registers   use the v<n> syntax instead of the p<n> syntax fo
                                r registers mapped to method parameters
 version: 2.1-SNAPSHOT
 online help: https://sourceforge.net/p/dex2jar/wiki/Smali
 ```
 
 - - -
 
 ##### d2j-class-version-switch
 
 
 ```
 root@kali:~# d2j-class-version-switch -h
 Usage: clz-version-switch version old.jar new.jar
 ```
 
 - - -
 
 ##### d2j-decrypt-string
 
 
 ```
 root@kali:~# d2j-decrypt-string -h
 d2j-decrypt-string -- Decrypt in class file
 usage: d2j-decrypt-string [options] <jar>
 options:
  -cp,--classpath <cp>                 add extra lib to classpath
  -d,--delete                          delete the method which can decrypt the st
                                       ings
  -da,--deep-analyze                   use dex2jar IR to static analyze and find 
                                       more values like byte[]
  -f,--force                           force overwrite
  -h,--help                            Print this help message
  -m,--methods <cfg>                   a file contain a list of methods, each lin
                                       e like: La/b;->decrypt(III)Ljava/lang/Stri
                                       ng;
  -mn,--decrypt-method-name <name>     the owner of the method which can decrypt 
                                       the stings, the method's signature must be
                                        static (parameter-type)Ljava/lang/String;
                                       . Please use -pt,--parameter-type to set t
                                       he argument descrypt.
  -mo,--decrypt-method-owner <owner>   the owner of the method which can decrypt 
                                       the stings, example: java.lang.String
  -o,--output <out>                    output of .jar files, default is $current_
                                       dir/[jar-name]-decrypted.jar
  -pd,--parameters-descriptor <type>   the descriptor for the method which can de
                                       crypt the stings, example1: Ljava/lang/Str
                                       ing; example2: III, default is Ljava/lang/
                                       String;
  -t,--arg-types <type>                comma-separated list of types:boolean,byte
                                       ,short,char,int,long,float,double,string. 
                                       Default is string
  -v,--verbose                         show more on output
 version: 2.1-SNAPSHOT
 online help: 
 https://sourceforge.net/p/dex2jar/wiki/DecryptStrings
 https://bitbucket.org/pxb1988/dex2jar/wiki/DecryptStrings
 ```
 
 - - -
 
 ##### d2j-dex-recompute-checksum
 
 
 ```
 root@kali:~# d2j-dex-recompute-checksum -h
 d2j-dex-recompute-checksum -- recompute crc and sha1 of dex.
 usage: d2j-dex-recompute-checksum [options] dex
 options:
  -f,--force                   force overwrite
  -h,--help                    Print this help message
  -o,--output <out-dex-file>   output .dex file, default is [dex-name]-rechecksum
                               .dex
 version: 2.1-SNAPSHOT
 ```
 
 - - -
 
 ##### d2j-dex-weaver
 
 
 ```
 root@kali:~# d2j-dex-weaver -h
 d2j-dex-weaver -- replace invoke in dex
 usage: d2j-dex-weaver [options] dex
 options:
  -c,--config <config>         config file
  -h,--help                    Print this help message
  -o,--output <out-dex-file>   output .dex file
  -s,--stub-dex <stub>         stub dex
 version: 2.1-SNAPSHOT
 online help: https://sourceforge.net/p/dex2jar/wiki/DexWeaver
 ```
 
 - - -
 
 ##### d2j-dex2jar
 
 
 ```
 root@kali:~# d2j-dex2jar -h
 d2j-dex2jar -- convert dex to jar
 usage: d2j-dex2jar [options] <file0> [file1 ... fileN]
 options:
  --skip-exceptions            skip-exceptions
  -d,--debug-info              translate debug info
  -e,--exception-file <file>   detail exception file, default is $current_dir/[fi
                               le-name]-error.zip
  -f,--force                   force overwrite
  -h,--help                    Print this help message
  -n,--not-handle-exception    not handle any exceptions thrown by dex2jar
  -nc,--no-code
  -o,--output <out-jar-file>   output .jar file, default is $current_dir/[file-na
                               me]-dex2jar.jar
  -os,--optmize-synchronized   optimize-synchronized
  -p,--print-ir                print ir to System.out
  -r,--reuse-reg               reuse register while generate java .class file
  -s                           same with --topological-sort/-ts
  -ts,--topological-sort       sort block by topological, that will generate more
                                readable code, default enabled
 version: reader-2.1-SNAPSHOT, translator-2.1-SNAPSHOT, ir-2.1-SNAPSHOT
 ```
 
 - - -
 
 ##### d2j-dex2smali
 
 
 ```
 root@kali:~# d2j-dex2smali -h
 d2j-baksmali -- disassembles and/or dumps a dex file
 usage: d2j-baksmali [options] <dex>
 options:
  -b,--no-debug-info            [not impl] don't write out debug info (.local, .p
                                aram, .line, etc.)
  -f,--force                    force overwrite
  -h,--help                     Print this help message
  -l,--use-locals               output the .locals directive with the number of n
                                on-parameter registers, rather than the .register
  -o,--output <out>             output dir of .smali files, default is $current_d
                                ir/[jar-name]-out/
  -p,--no-parameter-registers   use the v<n> syntax instead of the p<n> syntax fo
                                r registers mapped to method parameters
 version: 2.1-SNAPSHOT
 online help: https://sourceforge.net/p/dex2jar/wiki/Smali
 ```
 
 - - -
 
 ##### d2j-jar-access
 
 
 ```
 root@kali:~# d2j-jar-access -h
 d2j-jar-access -- add or remove class/method/field access in jar file
 usage: d2j-jar-access [options] <jar>
 options:
  -ac,--add-class-access <ACC>       add access from class
  -af,--add-field-access <ACC>       add access from field
  -am,--add-method-access <ACC>      add access from method
  -f,--force                         force overwrite
  -h,--help                          Print this help message
  -o,--output <out-dir>              output dir of .j files, default is $current_
                                     dir/[jar-name]-access.jar
  -rc,--remove-class-access <ACC>    remove access from class
  -rd,--remove-debug                 remove debug info
  -rf,--remove-field-access <ACC>    remove access from field
  -rm,--remove-method-access <ACC>   remove access from method
 version: 2.1-SNAPSHOT
 ```
 
 - - -
 
 ##### d2j-jar-weaver
 
 
 ```
 root@kali:~# d2j-jar-weaver -h
 d2j-jar-weaver -- replace invoke in jar
 usage: d2j-jar-weaver [options] jar
 options:
  -c,--config <config>         config file
  -h,--help                    Print this help message
  -o,--output <out-jar-file>   output .jar file
  -s,--stub-jar <stub>         stub jar
 version: 2.1-SNAPSHOT
 online help: https://sourceforge.net/p/dex2jar/wiki/JarWeaver
 ```
 
 - - -
 
 ##### d2j-jar2dex
 
 
 ```
 root@kali:~# d2j-jar2dex -h
 d2j-jar2dex -- Convert jar to dex by invoking dx.
 usage: d2j-jar2dex [options] <dir>
 options:
  -f,--force                   force overwrite
  -h,--help                    Print this help message
  -o,--output <out-dex-file>   output .dex file, default is $current_dir/[jar-nam
                               e]-jar2dex.dex
 version: 2.1-SNAPSHOT
 ```
 
 - - -
 
 ##### d2j-jar2jasmin
 
 
 ```
 root@kali:~# d2j-jar2jasmin -h
 d2j-jar2jasmin -- Disassemble .class in jar file to jasmin file
 usage: d2j-jar2jasmin [options] <jar>
 options:
  -d,--debug              disassemble debug info
  -e,--encoding <enc>     encoding for .j files, default is UTF-8
  -f,--force              force overwrite
  -h,--help               Print this help message
  -o,--output <out-dir>   output dir of .j files, default is $current_dir/[jar-na
                          me]-jar2jasmin/
 version: 2.1-SNAPSHOT
 online help: https://sourceforge.net/p/dex2jar/wiki/Jasmin
 ```
 
 - - -
 
 ##### d2j-jasmin2jar
 
 
 ```
 root@kali:~# d2j-jasmin2jar -h
 d2j-jasmin2jar -- Assemble .j files to .class file
 usage: d2j-jasmin2jar [options] <jar>
 options:
  --no-compute-max
  -cv,--class-version <arg>       default .class version, [1~9], default 6 for JA
                                  VA6
  -d,--dump                       dump to stdout
  -e,--encoding <enc>             encoding for .j files, default is UTF-8
  -f,--force                      force overwrite
  -g,--autogenerate-linenumbers   autogenerate-linenumbers
  -h,--help                       Print this help message
  -o,--output <out-jar-file>      output .jar file, default is $current_dir/[jar-
                                  name]-jasmin2jar.jar
 version: 2.1-SNAPSHOT
 online help: https://sourceforge.net/p/dex2jar/wiki/Jasmin
 ```
 
 - - -
 
 ##### d2j-smali
 
 
 ```
 root@kali:~# d2j-smali -h
 d2j-smali -- assembles a set of smali files into a dex file
 usage: d2j-smali [options] [--] [<smali-file>|folder]*
 options:
  --                             read smali from stdin
  -a,--api-level <API_LEVEL>     [not impl] The numeric api-level of the file to 
                                 generate, e.g. 14 for ICS. If not specified, it 
                                 defaults to 14 (ICS).
  -h,--help                      Print this help message
  -o,--output <FILE>             the name of the dex file that will be written. T
                                 he default is out.dex
  -v,--version                   prints the version then exits
  -x,--allow-odex-instructions   [not impl] allow odex instructions to be compile
                                 d into the dex file. Only a few instructions are
                                  supported - the ones that can exist in a dead c
                                 ode path and not cause dalvik to reject the clas
                                 s
 version: 2.1-SNAPSHOT
 online help: https://sourceforge.net/p/dex2jar/wiki/Smali
 ```
 
 - - -
 
 ##### d2j-std-apk
 
 
 ```
 root@kali:~# d2j-std-apk -h
 d2j-std-zip -- clean up apk to standard zip
 usage: d2j-std-zip [options] <zip>
 options:
  -h,--help           Print this help message
  -o,--output <out>   The output file
 version: 2.1-SNAPSHOT
 ```
 
 - - -
 
 ##### d2j_invoke
 
 
 ```
 root@kali:~# d2j_invoke --help
 Usage: java [options] <mainclass> [args...]
            (to execute a class)
    or  java [options] -jar <jarfile> [args...]
            (to execute a jar file)
    or  java [options] -m <module>[/<mainclass>] [args...]
        java [options] --module <module>[/<mainclass>] [args...]
            (to execute the main class in a module)
    or  java [options] <sourcefile> [args]
            (to execute a single source-file program)
 
  Arguments following the main class, source file, -jar <jarfile>,
  -m or --module <module>/<mainclass> are passed as the arguments to
  main class.
 
  where options include:
 
     -zero	  to select the "zero" VM
     -dcevm	  to select the "dcevm" VM
     -cp <class search path of directories and zip/jar files>
     -classpath <class search path of directories and zip/jar files>
     --class-path <class search path of directories and zip/jar files>
                   A : separated list of directories, JAR archives,
                   and ZIP archives to search for class files.
     -p <module path>
     --module-path <module path>...
                   A : separated list of directories, each directory
                   is a directory of modules.
     --upgrade-module-path <module path>...
                   A : separated list of directories, each directory
                   is a directory of modules that replace upgradeable
                   modules in the runtime image
     --add-modules <module name>[,<module name>...]
                   root modules to resolve in addition to the initial module.
                   <module name> can also be ALL-DEFAULT, ALL-SYSTEM,
                   ALL-MODULE-PATH.
     --enable-native-access <module name>[,<module name>...]
                   modules that are permitted to perform restricted native operations.
                   <module name> can also be ALL-UNNAMED.
     --list-modules
                   list observable modules and exit
     -d <module name>
     --describe-module <module name>
                   describe a module and exit
     --dry-run     create VM and load main class but do not execute main method.
                   The --dry-run option may be useful for validating the
                   command-line options such as the module system configuration.
     --validate-modules
                   validate all modules and exit
                   The --validate-modules option may be useful for finding
                   conflicts and other errors with modules on the module path.
     -D<name>=<value>
                   set a system property
     -verbose:[class|module|gc|jni]
                   enable verbose output for the given subsystem
     -version      print product version to the error stream and exit
     --version     print product version to the output stream and exit
     -showversion  print product version to the error stream and continue
     --show-version
                   print product version to the output stream and continue
     --show-module-resolution
                   show module resolution output during startup
     -? -h -help
                   print this help message to the error stream
     --help        print this help message to the output stream
     -X            print help on extra options to the error stream
     --help-extra  print help on extra options to the output stream
     -ea[:<packagename>...|:<classname>]
     -enableassertions[:<packagename>...|:<classname>]
                   enable assertions with specified granularity
     -da[:<packagename>...|:<classname>]
     -disableassertions[:<packagename>...|:<classname>]
                   disable assertions with specified granularity
     -esa | -enablesystemassertions
                   enable system assertions
     -dsa | -disablesystemassertions
                   disable system assertions
     -agentlib:<libname>[=<options>]
                   load native agent library <libname>, e.g. -agentlib:jdwp
                   see also -agentlib:jdwp=help
     -agentpath:<pathname>[=<options>]
                   load native agent library by full pathname
     -javaagent:<jarpath>[=<options>]
                   load Java programming language agent, see java.lang.instrument
     -splash:<imagepath>
                   show splash screen with specified image
                   HiDPI scaled images are automatically supported and used
                   if available. The unscaled image filename, e.g. image.ext,
                   should always be passed as the argument to the -splash option.
                   The most appropriate scaled image provided will be picked up
                   automatically.
                   See the SplashScreen API documentation for more information
     @argument files
                   one or more argument files containing options
     -disable-@files
                   prevent further argument file expansion
     --enable-preview
                   allow classes to depend on preview features of this release
 To specify an argument for a long option, you can use --<name>=<value> or
 --<name> <value>.
 
 ```
 
 - - -
 
 ##### dex-tools
 
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## d2j-dex2jar Usage Example

```
root@kali:~# d2j-dex2jar /usr/share/metasploit-framework/data/android/apk/classes.dex
dex2jar /usr/share/metasploit-framework/data/android/apk/classes.dex -> classes-dex2jar.jar
```

## d2j-jar-remap

```
root@kali:~# d2j-jar-remap -h
d2j-jar-remap -- rename package/class/method/field name in a jar
usage: d2j-jar-remap [options] jar
options:
 -c,--config <config>    config file for remap, this is REQUIRED
 -f,--force              force overwrite
 -h,--help               Print this help message
 -o,--output <out-jar>   output .jar file, default is $current_dir/[jar-name]-re
                         map.jar
version: 0.0.9.15
online help: https://code.google.com/p/dex2jar/wiki/DeObfuscateJarWithDexTool
```

## dex2jar

```
root@kali:~# dex2jar
this cmd is deprecated, use the d2j-dex2jar if possible
dex2jar version: translator-0.0.9.15
dex2jar file1.dexORapk file2.dexORapk ...
```

## d2j-dex-dump

```
root@kali:~# d2j-dex-dump -h
Dump in.dexORapk out.dump.jar
```

## d2j-init-deobf

```
root@kali:~# d2j-init-deobf -h
d2j-init-deobf -- generate an init config file for deObfuscate a jar
usage: d2j-init-deobf [options] <jar>
options:
 -f,--force                force overwrite
 -h,--help                 Print this help message
 -max,--max-length <MAX>   do the rename if the length > MIN, default is 40
 -min,--min-length <MIN>   do the rename if the length < MIN, default is 2
 -o,--output <out-file>    output .jar file, default is $current_dir/[file-name]
                           -deobf-init.txt
version: 0.0.9.15
```
