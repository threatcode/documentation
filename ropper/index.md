---
Title: ropper
Homepage: https://scoding.de/ropper/
Repository: https://gitlab.com/kalilinux/packages/ropper
Architectures: all
Version: 1.13.8-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### ropper
 
  This package contains scripts that display info about files in different
  formats and find gadgets to build ROPs chains for different architectures
  (x86/x86_64, ARM/ARM64, MIPS, PowerPC). For disassembly ropper uses the
  Capstone Framework.
 
 **Installed size:** `402 KB`  
 **How to install:** `sudo apt install ropper`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-capstone 
 * python3-filebytes
 * python3-pkg-resources
 {{< /spoiler >}}
 
 ##### ropper
 
 
 ```
 root@kali:~# ropper -h
 usage: ropper [-h] [--help-examples] [-v] [--console] [-f <file> [<file> ...]]
               [-r] [-a <arch>] [--section <section>] [--string [<string>]]
               [--hex] [--asm [<asm> [H|S|R] ...]] [--disasm <opcode>]
               [--disassemble-address <address:length>] [-i] [-e] [--imagebase]
               [-c] [-s] [-S] [--imports] [--symbols] [--set <option>]
               [--unset <option>] [-I <imagebase>] [-p] [-j <reg>]
               [--stack-pivot] [--inst-count <n bytes>] [--search <regex>]
               [--quality <quality>] [--opcode <opcode>]
               [--instructions <instructions>] [--type <type>] [--detailed]
               [--all] [--cfg-only] [--chain <generator>] [-b <badbytes>]
               [--nocolor] [--clear-cache] [--no-load] [--analyse <quality>]
               [--semantic constraint] [--count-of-findings <count of gadgets>]
               [--single]
 
 You can use ropper to display information about binary files in different file formats
     and you can search for gadgets to build rop chains for different architectures
 
 supported filetypes:
   ELF
   PE
   Mach-O
   Raw
 
 supported architectures:
   x86 [x86]
   x86_64 [x86_64]
   MIPS [MIPS, MIPS64]
   ARM/Thumb [ARM, ARMTHUMB]
   ARM64 [ARM64]
   PowerPC [PPC, PPC64]
   SPARC [SPARC64]
 
 available rop chain generators:
   execve (execve[=<cmd>], default /bin/sh) [Linux x86, x86_64]
   mprotect  (mprotect address=0xdeadbeef size=0x10000) [Linux x86, x86_64]
   virtualprotect (virtualprotect address=0xdeadbeef) [Windows x86]
 
 options:
   -h, --help            show this help message and exit
   --help-examples       Print examples
   -v, --version         Print version
   --console             Starts interactive commandline
   -f <file> [<file> ...], --file <file> [<file> ...]
                         The file to load
   -r, --raw             Loads the file as raw file
   -a <arch>, --arch <arch>
                         The architecture of the loaded file
   --section <section>   The data of the this section should be printed
   --string [<string>]   Looks for the string <string> in all data sections
   --hex                 Prints the selected sections in a hex format
   --asm [<asm> [H|S|R] ...]
                         A string to assemble and a format of the output
                         (H=HEX, S=STRING, R=RAW, default: H)
   --disasm <opcode>     Opcode to disassemble (e.g. ffe4, 89c8c3, ...)
   --disassemble-address <address:length>
                         Disassembles instruction at address <address>
                         (0x12345678:L3). The count of instructions to
                         disassemble can be specified (0x....:L...)
   -i, --info            Shows file header [ELF/PE/Mach-O]
   -e                    Shows EntryPoint
   --imagebase           Shows ImageBase [ELF/PE/Mach-O]
   -c, --dllcharacteristics
                         Shows DllCharacteristics [PE]
   -s, --sections        Shows file sections [ELF/PE/Mach-O]
   -S, --segments        Shows file segments [ELF/Mach-O]
   --imports             Shows imports [ELF/PE]
   --symbols             Shows symbols [ELF]
   --set <option>        Sets options. Available options: aslr nx
   --unset <option>      Unsets options. Available options: aslr nx
   -I <imagebase>        Uses this imagebase for gadgets
   -p, --ppr             Searches for 'pop reg; pop reg; ret' instructions
                         [only x86/x86_64]
   -j <reg>, --jmp <reg>
                         Searches for 'jmp reg' instructions (-j reg[,reg...])
                         [only x86/x86_64]
   --stack-pivot         Prints all stack pivot gadgets
   --inst-count <n bytes>
                         Specifies the max count of instructions in a gadget
                         (default: 6)
   --search <regex>      Searches for gadgets
   --quality <quality>   The quality for gadgets which are found by search (1 =
                         best)
   --opcode <opcode>     Searches for opcodes (e.g. ffe4 or ffe? or ff??)
   --instructions <instructions>
                         Searches for instructions (e.g. "jmp esp", "pop eax;
                         ret")
   --type <type>         Sets the type of gadgets [rop, jop, sys, all]
                         (default: all)
   --detailed            Prints gadgets more detailed
   --all                 Does not remove duplicate gadgets
   --cfg-only            Filters out gadgets which fail the Microsoft CFG
                         check. Only for PE files which are compiled with CFG
                         check enabled (check DllCharachteristics) [PE]
   --chain <generator>   Generates a ropchain [generator parameter=value[
                         parameter=value]]
   -b <badbytes>, --badbytes <badbytes>
                         Set bytes which should not contains in gadgets
   --nocolor             Disables colored output
   --clear-cache         Clears the cache
   --no-load             Don't load the gadgets automatically when start the
                         console (--console)
   --analyse <quality>   just used for the implementation of semantic search
   --semantic constraint
                         semantic search for gadgets
   --count-of-findings <count of gadgets>
                         Max count of gadgets which will be printed with
                         semantic search (0 = undefined, default: 5)
   --single              No multiple processes are used for gadget scanning
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
