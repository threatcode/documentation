---
Title: pev
Homepage: https://pev.sourceforge.net
Repository: https://salsa.debian.org/debian/pev
Architectures: any
Version: 0.81-10
Metapackages: kali-linux-everything kali-linux-large kali-tools-forensics kali-tools-respond 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### pev
 
  pev is a tool to get information of PE32/PE32+
  executables (EXE, DLL, OCX etc) like  headers,
  sections, resources and more.
 
 **Installed size:** `1.57 MB`  
 **How to install:** `sudo apt install pev`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libssl3 
 {{< /spoiler >}}
 
 ##### ofs2rva
 
 Converts a PE raw file offset to relative virtual address
 
 ```
 root@kali:~# ofs2rva -h
 Usage: ofs2rva <offset> FILE
 Convert raw file offset to RVA
 
 Example: ofs2rva 0x1b9b8 calc.exe
 
 Options:
  -V, --version                          Show version.
  --help                                 Show this help.
 ```
 
 - - -
 
 ##### pedis
 
 Disassemble PE sections and functions
 
 ```
 root@kali:~# pedis --help
 Usage: pedis OPTIONS FILE
 Disassemble PE sections and functions (by default, until found a RET or LEAVE instruction)
 
 Example: pedis -r 0x4c4df putty.exe
 
 Options:
  --att                                  Set AT&T assembly syntax (default: Intel).
  -e, --entrypoint                       Disassemble the entire entrypoint function.
  -f, --format <xml|html|json|text|csv>  Change output format (default: text).
  -m, --mode <16|32|64>                  Disassembly mode (default: auto).
  -i <number>                            Number of instructions to disassemble.
  -n <number>                            Number of bytes to disassemble
  -o, --offset <offset>                  Disassemble at specified offset, either in decimal or hexadecimal format (prefixed with 0x).
  -r, --rva <rva>                        Disassemble at specified RVA, either in decimal or hexadecimal format (prefixed with 0x).
  -s, --section <section_name>           Disassemble en entire section given.
  -V, --version                          Show version.
  --help                                 Show this help.
 ```
 
 - - -
 
 ##### pehash
 
 Calculate hashes of PE pieces
 
 ```
 root@kali:~# pehash --help
 Usage: pehash OPTIONS FILE
 Calculate hashes of PE pieces
 
 Example: pehash -s '.text' winzip.exe
 
 Options:
  -f, --format <xml|html|json|text|csv> Change output format (default: text).
  -a, --all                             Hash file, sections and headers with md5, sha1, sha256, ssdeep and imphash.
  -c, --content                         Hash only the file content (default).
  -h, --header <dos|coff|optional>      Hash only the header with the specified name.
  -s, --section <section_name>          Hash only the section with the specified name.
  --section-index <section_index>       Hash only the section at the specified index (1..n).
  -V, --version                         Show version.
  --help                                Show this help.
 ```
 
 - - -
 
 ##### peldd
 
 Shows library dependencies for a given PE file
 
 ```
 root@kali:~# peldd --help
 Usage: peldd FILE
 Display PE library dependencies
 
 Example: peldd winzip.exe
 
 Options:
  -f, --format <xml|html|json|text|csv>  Change output format (default: text).
  -V, --version                          Show version.
  --help                                 Show help.
 ```
 
 - - -
 
 ##### pepack
 
 Check if a PE file is packed
 
 ```
 root@kali:~# pepack --help
 Usage: pepack FILE
 Search for packers in PE files
 
 Example: pepack putty.exe
 
 Options:
  -d, --database <file>                  Use database file (default: ./userdb.txt).
  -f, --format <xml|html|json|text|csv>  Change output format (default: text).
  -V, --version                          Show version.
  --help                                 Show this help.
 ```
 
 - - -
 
 ##### peres
 
 Analyze and extract PE file resources
 
 ```
 root@kali:~# peres -h
 Usage: peres OPTIONS FILE
 Show information about resource section and extract it
 
 Example: peres -a putty.exe
 
 Options:
  -a, --all                              Show all information, statistics and extract resources
  -f, --format <xml|html|json|text|csv>  change output format (default: text)
  -i, --info                             Show resources information
  -l, --list                             Show list view
  -s, --statistics                       Show resources statistics
  -x, --extract                          Extract resources
  -X, --named-extract                    Extract resources with path names
  -v, --file-version                     Show File Version from PE resource directory
  -V, --version                          Show version and exit
  --help                                 Show this help and exit
 ```
 
 - - -
 
 ##### pescan
 
 Identify suspicious characteristics in PE files
 
 ```
 root@kali:~# pescan --help
 Usage: pescan OPTIONS FILE
 Search for suspicious things in PE files
 
 Example: pescan putty.exe
 
 Options:
  -f, --format <xml|html|json|text|csv>  Change output format (default: text).
  -v, --verbose                          Show more information about found items.
  -V, --version                          Show version.
  --help                                 Show this help.
 ```
 
 - - -
 
 ##### pesec
 
 Check for protections in PE files
 
 ```
 root@kali:~# pesec --help
 Usage: pesec [OPTIONS] FILE
 Check for security features in PE files
 
 Example: pesec wordpad.exe
 
 Options:
  -f, --format <xml|html|json|text|csv>  Change output format (default: text)
  -c, --certoutform <text|pem>           Specifies the certificate output format (default: text).
  -o, --certout <filename>               Specifies the output filename to write certificates to (default: stdout).
  -V, --version                          Show version.
  --help                                 Show this help.
 ```
 
 - - -
 
 ##### pestr
 
 Search strings in PE files
 
 ```
 root@kali:~# pestr --help
 Usage: pestr OPTIONS FILE
 Search for strings in PE files
 
 Example: pestr acrobat.exe
 
 Options:
  -n, --min-length                       Set minimum string length (default: 4).
  -o, --offset                           Show string offset in file.
  -s, --section                          Show string section, if exists.
  -V, --version                          Show version.
  --help                                 Show this help.
 ```
 
 - - -
 
 ##### readpe
 
 Displays information about PE files
 
 ```
 root@kali:~# readpe --help
 Usage: readpe OPTIONS FILE
 Show PE file headers
 
 Example: readpe --header optional winzip.exe
 
 Options:
  -A, --all                              Full output (default).
  -H, --all-headers                      Show all PE headers.
  -S, --all-sections                     Show PE section headers.
  -f, --format <xml|html|json|text|csv>  Change output format (default: text).
  -d, --dirs                             Show data directories.
  -h, --header <dos|coff|optional>       Show specific header. It can be used multiple times.
  -i, --imports                          Show imported functions.
  -e, --exports                          Show exported functions.
  -V, --version                          Show version.
  --help                                 Show this help.
 ```
 
 - - -
 
 ##### rva2ofs
 
 Converts a PE relative virtual address to raw file offset
 
 ```
 root@kali:~# rva2ofs -h
 Usage: rva2ofs <rva> FILE
 Convert RVA to raw file offset
 
 Example: rva2ofs 0x12db cards.dll
 
 Options:
  -V, --version                          Show version.
  --help                                 Show this help.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
