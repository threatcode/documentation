---
Title: de4dot
Homepage: https://github.com/0xd4d/de4dot
Repository: https://salsa.debian.org/pkg-security-team/de4dot
Architectures: all
Version: 3.1.41592.3405-2
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### de4dot
 
  de4dot is a .NET deobfuscator and unpacker. It will try its best to
  restore a packed and obfuscated assembly to almost the original
  assembly.
   
  Most of the obfuscation can be completely restored (eg. string
  encryption), but symbol renaming is impossible to restore since the
  original names aren't (usually) part of the obfuscated assembly.
 
 **Installed size:** `1.40 MB`  
 **How to install:** `sudo apt install de4dot`  
 
 {{< spoiler "Dependencies:" >}}
 * libdnlib2.1-cil 
 * libmono-corlib4.5-cil 
 * libmono-system-drawing4.0-cil 
 * libmono-system-runtime4.0-cil 
 * libmono-system-xml4.0-cil 
 * libmono-system4.0-cil 
 * mono-runtime 
 {{< /spoiler >}}
 
 ##### de4dot
 
 
 ```
 root@kali:~# de4dot -h
 
 de4dot v3.1.41592.3405 Copyright (C) 2011-2015 de4dot@gmail.com
 Latest version and source code: https://github.com/0xd4d/de4dot
 
 Some of the advanced options may be incompatible, causing a nice exception.
 With great power comes great responsibility.
 
 de4dot.exe <options> <file options>
 Options:
   -r DIR           Scan for .NET files in all subdirs
   -ro DIR          Output base dir for recursively found files
   -ru              Skip recursively found files with unsupported obfuscator
   -d               Detect obfuscators and exit
   --asm-path PATH  Add an assembly search path
   --dont-rename    Don't rename classes, methods, etc.
   --keep-names FLAGS
                    Don't rename n(amespaces), t(ypes), p(rops), e(vents), f(ields), m(ethods), a(rgs), g(enericparams), d(elegate fields). Can be combined, eg. efm
   --dont-create-params
                    Don't create method params when renaming
   --dont-restore-props
                    Don't restore properties/events
   --default-strtyp TYPE
                    Default string decrypter type
   --default-strtok METHOD
                    Default string decrypter method token or [type::][name][(args,...)]
   --no-cflow-deob  No control flow deobfuscation (NOT recommended)
   --only-cflow-deob
                    Only control flow deobfuscation
   --load-new-process
                    Load executed assemblies into a new process
   --keep-types     Keep obfuscator types, fields, methods
   --preserve-tokens
                    Preserve important tokens, #US, #Blob, extra sig data
   --preserve-table FLAGS
                    Preserve rids in table: tr (TypeRef), td (TypeDef), fd (Field), md (Method), pd (Param), mr (MemberRef), s (StandAloneSig), ed (Event), pr (Property), ts (TypeSpec), ms (MethodSpec), all (all previous tables). Use - to disable (eg. all,-pd). Can be combined: ed,fd,md
   --preserve-strings
                    Preserve #Strings heap offsets
   --preserve-us    Preserve #US heap offsets
   --preserve-blob  Preserve #Blob heap offsets
   --preserve-sig-data
                    Preserve extra data at the end of signatures
   --one-file       Deobfuscate one file at a time
   -v               Verbose
   -vv              Very verbose
   -h               Show this help message
   --help           Same as -h
 
 File options:
   -f FILE          Name of .NET file
   -o FILE          Name of output file
   -p TYPE          Obfuscator type (see below)
   --strtyp TYPE    String decrypter type
   --strtok METHOD  String decrypter method token or [type::][name][(args,...)]
 
 Deobfuscator options:
 Type un (Unknown)
   --un-name REGEX  Valid name regex pattern (^[a-zA-Z_<{$][a-zA-Z_0-9<>{}$.`-]*$)
 
 Type an (Agile.NET)
   --an-name REGEX  Valid name regex pattern (^[\u2E80-\u9FFFa-zA-Z_<{$][\u2E80-\u9FFFa-zA-Z_0-9<>{}$.`-]*$)
   --an-methods BOOL
                    Decrypt methods (True)
   --an-rsrc BOOL   Decrypt resources (True)
   --an-stack BOOL  Remove all StackFrameHelper code (True)
   --an-vm BOOL     Restore VM code (True)
   --an-initlocals BOOL
                    Set initlocals in method header (True)
 
 Type bl (Babel .NET)
   --bl-name REGEX  Valid name regex pattern (^[\u2E80-\u9FFFa-zA-Z_<{$][\u2E80-\u9FFFa-zA-Z_0-9<>{}$.`-]*$)
   --bl-inline BOOL Inline short methods (True)
   --bl-remove-inlined BOOL
                    Remove inlined methods (True)
   --bl-methods BOOL
                    Decrypt methods (True)
   --bl-rsrc BOOL   Decrypt resources (True)
   --bl-consts BOOL Decrypt constants and arrays (True)
   --bl-embedded BOOL
                    Dump embedded assemblies (True)
 
 Type cf (CodeFort)
   --cf-name REGEX  Valid name regex pattern (!^[a-zA-Z]{1,3}$&!^[_<>{}$.`-]$&^[\u2E80-\u9FFFa-zA-Z_<{$][\u2E80-\u9FFFa-zA-Z_0-9<>{}$.`-]*$)
   --cf-embedded BOOL
                    Dump embedded assemblies (True)
 
 Type cv (CodeVeil)
   --cv-name REGEX  Valid name regex pattern (!^[A-Za-z]{1,2}$&^[\u2E80-\u9FFFa-zA-Z_<{$][\u2E80-\u9FFFa-zA-Z_0-9<>{}$.`-]*$)
 
 Type cw (CodeWall)
   --cw-name REGEX  Valid name regex pattern (!^[0-9A-F]{32}$&!^[_<>{}$.`-]$&^[\u2E80-\u9FFFa-zA-Z_<{$][\u2E80-\u9FFFa-zA-Z_0-9<>{}$.`-]*$)
   --cw-embedded BOOL
                    Dump embedded assemblies (True)
   --cw-decrypt-main BOOL
                    Decrypt main embedded assembly (True)
 
 Type cr (Confuser)
   --cr-name REGEX  Valid name regex pattern (^[a-zA-Z_<{$][a-zA-Z_0-9<>{}$.`-]*$)
   --cr-antidb BOOL Remove anti debug code (True)
   --cr-antidump BOOL
                    Remove anti dump code (True)
   --cr-decrypt-main BOOL
                    Decrypt main embedded assembly (True)
 
 Type co (Crypto Obfuscator)
   --co-name REGEX  Valid name regex pattern (!^(get_|set_|add_|remove_)?[A-Z]{1,3}(?:`\d+)?$&!^(get_|set_|add_|remove_)?c[0-9a-f]{32}(?:`\d+)?$&^[\u2E80-\u9FFFa-zA-Z_<{$][\u2E80-\u9FFFa-zA-Z_0-9<>{}$.`-]*$)
   --co-tamper BOOL Remove tamper protection code (True)
   --co-consts BOOL Decrypt constants (True)
   --co-inline BOOL Inline short methods (True)
   --co-ldnull BOOL Restore ldnull instructions (True)
 
 Type ds (DeepSea)
   --ds-name REGEX  Valid name regex pattern (^[\u2E80-\u9FFFa-zA-Z_<{$][\u2E80-\u9FFFa-zA-Z_0-9<>{}$.`-]*$)
   --ds-inline BOOL Inline short methods (True)
   --ds-remove-inlined BOOL
                    Remove inlined methods (True)
   --ds-rsrc BOOL   Decrypt resources (True)
   --ds-embedded BOOL
                    Dump embedded assemblies (True)
   --ds-fields BOOL Restore fields (True)
   --ds-keys BOOL   Rename resource keys (True)
   --ds-casts BOOL  Deobfuscate casts (True)
 
 Type df (Dotfuscator)
   --df-name REGEX  Valid name regex pattern (!^(?:eval_)?[a-z][a-z0-9]{0,2}$&!^A_[0-9]+$&^[\u2E80-\u9FFFa-zA-Z_<{$][\u2E80-\u9FFFa-zA-Z_0-9<>{}$.`-]*$)
 
 Type dr3 (.NET Reactor)
   --dr3-name REGEX Valid name regex pattern (^[\u2E80-\u9FFFa-zA-Z_<{$][\u2E80-\u9FFFa-zA-Z_0-9<>{}$.`-]*$)
   --dr3-types BOOL Restore types (object -> real type) (True)
   --dr3-inline BOOL
                    Inline short methods (True)
   --dr3-remove-inlined BOOL
                    Remove inlined methods (True)
   --dr3-ns1 BOOL   Clear namespace if there's only one class in it (True)
   --dr3-sn BOOL    Remove anti strong name code (True)
 
 Type dr4 (.NET Reactor)
   --dr4-name REGEX Valid name regex pattern (^[\u2E80-\u9FFFa-zA-Z_<{$][\u2E80-\u9FFFa-zA-Z_0-9<>{}$.`-]*$)
   --dr4-methods BOOL
                    Decrypt methods (True)
   --dr4-bools BOOL Decrypt booleans (True)
   --dr4-types BOOL Restore types (object -> real type) (True)
   --dr4-inline BOOL
                    Inline short methods (True)
   --dr4-remove-inlined BOOL
                    Remove inlined methods (True)
   --dr4-embedded BOOL
                    Dump embedded assemblies (True)
   --dr4-rsrc BOOL  Decrypt resources (True)
   --dr4-ns1 BOOL   Clear namespace if there's only one class in it (True)
   --dr4-sn BOOL    Remove anti strong name code (True)
   --dr4-sname BOOL Rename short names (False)
 
 Type ef (Eazfuscator.NET)
   --ef-name REGEX  Valid name regex pattern (!^[a-zA-Z]$&!^#=&!^dje_.+_ejd$&^[\u2E80-\u9FFFa-zA-Z_<{$][\u2E80-\u9FFFa-zA-Z_0-9<>{}$.`-]*$)
 
 Type go (Goliath.NET)
   --go-name REGEX  Valid name regex pattern (!^[A-Za-z]{1,2}(?:`\d+)?$&^[\u2E80-\u9FFFa-zA-Z_<{$][\u2E80-\u9FFFa-zA-Z_0-9<>{}$.`-]*$)
   --go-inline BOOL Inline short methods (True)
   --go-remove-inlined BOOL
                    Remove inlined methods (True)
   --go-locals BOOL Restore locals (True)
   --go-ints BOOL   Decrypt integers (True)
   --go-arrays BOOL Decrypt arrays (True)
   --go-sn BOOL     Remove anti strong name code (True)
 
 Type il (ILProtector)
   --il-name REGEX  Valid name regex pattern (^[\u2E80-\u9FFFa-zA-Z_<{$][\u2E80-\u9FFFa-zA-Z_0-9<>{}$.`-]*$)
 
 Type mc (MaxtoCode)
   --mc-name REGEX  Valid name regex pattern (!^[oO01l]+$&!^[A-F0-9]{20,}$&^[\u2E80-\u9FFFa-zA-Z_<{$][\u2E80-\u9FFFa-zA-Z_0-9<>{}$.`-]*$)
   --mc-cp INT      String code page (936)
 
 Type mp (MPRESS)
   --mp-name REGEX  Valid name regex pattern (^[\u2E80-\u9FFFa-zA-Z_<{$][\u2E80-\u9FFFa-zA-Z_0-9<>{}$.`-]*$)
 
 Type rm (Rummage)
   --rm-name REGEX  Valid name regex pattern (!.)
 
 Type sk (Skater .NET)
   --sk-name REGEX  Valid name regex pattern (!`[^0-9]+&^[\u2E80-\u9FFFa-zA-Z_<{$][\u2E80-\u9FFFa-zA-Z_0-9<>{}$.`-]*$)
 
 Type sa (SmartAssembly)
   --sa-name REGEX  Valid name regex pattern (^[\u2E80-\u9FFFa-zA-Z_<{$][\u2E80-\u9FFFa-zA-Z_0-9<>{}$.`-]*$)
   --sa-error BOOL  Remove automated error reporting code (True)
   --sa-tamper BOOL Remove tamper protection code (True)
   --sa-memory BOOL Remove memory manager code (True)
 
 Type sn (Spices.Net)
   --sn-name REGEX  Valid name regex pattern (!^[a-zA-Z0-9]{1,2}$&^[\u2E80-\u9FFFa-zA-Z_<{$][\u2E80-\u9FFFa-zA-Z_0-9<>{}$.`-]*$)
   --sn-inline BOOL Inline short methods (True)
   --sn-remove-inlined BOOL
                    Remove inlined methods (True)
   --sn-ns1 BOOL    Clear namespace if there's only one class in it (True)
   --sn-rsrc BOOL   Restore resource names (True)
 
 Type xc (Xenocode)
   --xc-name REGEX  Valid name regex pattern (!^[oO01l]{4,}$&!^(get_|set_|add_|remove_|_)?[x_][a-f0-9]{16,}$&^[\u2E80-\u9FFFa-zA-Z_<{$][\u2E80-\u9FFFa-zA-Z_0-9<>{}$.`-]*$)
 
 String decrypter types
   none             Don't decrypt strings
   default          Use default string decrypter type (usually static)
   static           Use static string decrypter if available
   delegate         Use a delegate to call the real string decrypter
   emulate          Call real string decrypter and emulate certain instructions
 
 Multiple regexes can be used if separated by '&'.
 Use '!' if you want to invert the regex. Example: !^[a-z\d]{1,2}$&!^[A-Z]_\d+$&^[\w.]+$
 
 Examples:
 de4dot.exe -r c:\my\files -ro c:\my\output
 de4dot.exe file1 file2 file3
 de4dot.exe file1 -f file2 -o file2.out -f file3 -o file3.out
 de4dot.exe file1 --strtyp delegate --strtok 06000123
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
