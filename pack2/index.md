---
Title: pack2
Homepage: https://github.com/hops/pack2
Repository: https://gitlab.com/kalilinux/packages/pack2
Architectures: any
Version: 0.1.0~git20200929.da4b245-0kali4
Metapackages: kali-linux-everything kali-linux-large kali-tools-passwords 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### pack2
 
  This package contains a replacement for iphelix's PACK. This is a work in
  progress. Not all features are available and while being similar some will
  differ slightly.
   
  PACK was developed in order to aid in a password cracking competition "Crack
  Me If You Can" that occurred during Defcon 2010. The goal of this toolkit is
  to aid in preparation for the "better than bruteforce" password attacks by
  analyzing common ways that people create passwords. After the analysis stage,
  the statistical database can be used to generate attack masks for tools such
  as oclHashcat.
   
  NOTE: This tool itself can not crack passwords, but helps other tools crack
  more passwords faster.
 
 **Installed size:** `897 KB`  
 **How to install:** `sudo apt install pack2`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libgcc-s1 
 {{< /spoiler >}}
 
 ##### pack2
 
 
 ```
 root@kali:~# pack2 -h
 pack2 0.1.0
 
 USAGE:
     pack2 <SUBCOMMAND>
 
 FLAGS:
     -h, --help       Prints help information
     -V, --version    Prints version information
 
 SUBCOMMANDS:
     cgrams        Splits each line on the charset boundry
     filtermask    Filters a wordlist by a given mask
     help          Prints this message or the help of the given subcommand(s)
     statsgen      Generates statistics from a [input] and writes masks to <output> stats are written to stderr
     unhex         Decodes $HEX[] encoded lines
 ```
 
 - - -
 
 ##### pack200
 
 Packages a JAR file into a compressed pack200 file for web deployment.
 
 ```
 root@kali:~# pack200 -h
 
 Warning: The pack200 tool is deprecated, and is planned for removal in a future JDK release.
 
 Usage:  pack200 [-opt... | --option=value]... x.pack[.gz] y.jar
 
 Packing Options
   -r, --repack                    repack or normalize a jar, suitable for 
                                   signing with jarsigner
   -g, --no-gzip                   output a plain pack file, suitable to be
                                   compressed with a file compression utility
   --gzip                          (default) post compress the pack output
                                   with gzip
   -G, --strip-debug               remove debugging attributes (SourceFile,
                                   LineNumberTable, LocalVariableTable
                                   and LocalVariableTypeTable) while packing
   -O, --no-keep-file-order        do not transmit file ordering information
   --keep-file-order               (default) preserve input file ordering
   -S{N}, --segment-limit={N}      limit segment sizes (default unlimited)
   -E{N}, --effort={N}             packing effort (default N=5)
   -H{h}, --deflate-hint={h}       transmit deflate hint: true, false,
                                   or keep (default)
   -m{V}, --modification-time={V}  transmit modtimes: latest or keep (default)
   -P{F}, --pass-file={F}          transmit the given input element(s) unchanged
   -U{a}, --unknown-attribute={a}  unknown attribute action: error, strip,
                                   or pass (default)
   -C{N}={L}, --class-attribute={N}={L}  (user-defined attribute)
   -F{N}={L}, --field-attribute={N}={L}  (user-defined attribute)
   -M{N}={L}, --method-attribute={N}={L} (user-defined attribute)
   -D{N}={L}, --code-attribute={N}={L}   (user-defined attribute)
   -f{F}, --config-file={F}        read file F for Pack200.Packer properties
   -v, --verbose                   increase program verbosity
   -q, --quiet                     set verbosity to lowest level
   -l{F}, --log-file={F}           output to the given log file, 
                                   or '-' for System.out
   -?, -h, --help                  print this help message
   -V, --version                   print program version
   -J{X}                           pass option X to underlying Java VM
 
 Notes:
   The -P, -C, -F, -M, and -D options accumulate.
   Example attribute definition:  -C SourceFile=RUH .
   Config. file properties are defined by the Pack200 API.
   For meaning of -S, -E, -H-, -m, -U values, see Pack200 API.
   Layout definitions (like RUH) are defined by JSR 200.
 
 Repacking mode updates the JAR file with a pack/unpack cycle:
     pack200 [-r|--repack] [-opt | --option=value]... [repackedy.jar] y.jar
 
 
 Exit Status:
   0 if successful, >0 if an error occurred
 
 Warning: The pack200 tool is deprecated, and is planned for removal in a future JDK release.
 
 ```
 
 - - -
 
 ##### unpack200
 
 Transforms a packed file produced by pack200(1) into a JAR file for web deployment.
 
 ```
 root@kali:~# unpack200 -h
 
 Warning: The unpack200 tool is deprecated, and is planned for removal in a future JDK release.
 
 Usage:  unpack200 [-opt... | --option=value]... x.pack[.gz] y.jar
 
 Unpacking Options
   -H{h}, --deflate-hint={h}     override transmitted deflate hint:
                                 true, false, or keep (default)
   -r, --remove-pack-file        remove input file after unpacking
   -v, --verbose                 increase program verbosity
   -q, --quiet                   set verbosity to lowest level
   -l{F}, --log-file={F}         output to the given log file,
                                 or '-' for standard output (default)
   -?, -h, --help                print this help message
   -V, --version                 print program version
 
 Exit Status:
   0 if successful, >0 if an error occurred
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
