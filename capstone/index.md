---
Title: capstone
Homepage: https://www.capstone-engine.org/
Repository: https://salsa.debian.org/pkg-security-team/capstone
Architectures: any
Version: 4.0.2-5
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-linux-nethunter kali-tools-forensics kali-tools-hardware kali-tools-post-exploitation kali-tools-respond kali-tools-reverse-engineering kali-tools-social-engineering 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### capstone-tool
 
  Capstone is a lightweight multi-platform, multi-architecture disassembly
  framework.
   
  This package contains cstool, a command-line tool to disassemble
  hexadecimal strings.
 
 **Installed size:** `6.41 MB`  
 **How to install:** `sudo apt install capstone-tool`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### cstool
 
 
 ```
 root@kali:~# cstool -h
 Cstool for Capstone Disassembler Engine v4.0.2
 
 Syntax: cstool [-d|-s|-u|-v] <arch+mode> <assembly-hexstring> [start-address-in-hex-format]
 
 The following <arch+mode> options are supported:
         x16:        16-bit mode (X86)
         x32:        32-bit mode (X86)
         x64:        64-bit mode (X86)
         x16att:     16-bit mode (X86) syntax-att
         x32att:     32-bit mode (X86) syntax-att
         x64att:     64-bit mode (X86) syntax-att
         arm:        arm
         armbe:      arm + big endian
         thumb:      thumb mode
         thumbbe:    thumb + big endian
         cortexm:    thumb + cortex-m extensions
         armv8:      arm v8
         thumbv8:    thumb v8
         arm64:      aarch64 mode
         arm64be:    aarch64 + big endian
         mips:       mips32 + little endian
         mipsbe:     mips32 + big endian
         mips64:     mips64 + little endian
         mips64be:   mips64 + big endian
         ppc32:      ppc32 + little endian
         ppc32be:    ppc32 + big endian
         ppc32qpx:   ppc32 + qpx + little endian
         ppc32beqpx: ppc32 + qpx + big endian
         ppc64:      ppc64 + little endian
         ppc64be:    ppc64 + big endian
         ppc64qpx:   ppc64 + qpx + little endian
         ppc64beqpx: ppc64 + qpx + big endian
         sparc:      sparc
         systemz:    systemz (s390x)
         xcore:      xcore
         m68k:       m68k + big endian
         m68k40:     m68k_040
         tms320c64x: TMS320C64x
         m6800:      M6800/2
         m6801:      M6801/3
         m6805:      M6805
         m6808:      M68HC08
         m6809:      M6809
         m6811:      M68HC11
         cpu12:      M68HC12/HCS12
         hd6301:     HD6301/3
         hd6309:     HD6309
         hcs08:      HCS08
         evm:        Ethereum Virtual Machine
 
 Extra options:
         -d show detailed information of the instructions
         -s decode in SKIPDATA mode
         -u show immediates as unsigned
         -v show version & Capstone core build info
 
 ```
 
 - - -
 
 ### libcapstone-dev
 
  Capstone is a lightweight multi-platform, multi-architecture disassembly
  framework.
   
  These are the development headers and libraries.
 
 **Installed size:** `7.87 MB`  
 **How to install:** `sudo apt install libcapstone-dev`  
 
 {{< spoiler "Dependencies:" >}}
 * libcapstone4 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libcapstone4
 
  Capstone is a lightweight multi-platform, multi-architecture disassembly
  framework.
   
  Features:
   - Support hardware architectures: ARM, ARM64 (aka ARMv8), Mips, PowerPC &
  Intel.
   - Clean/simple/lightweight/intuitive architecture-neutral API.
   - Provide details on disassembled instructions (called "decomposer" by some
  others).
   - Provide some semantics of the disassembled instruction, such as list of
  implicit registers read & written.
   - Implemented in pure C language, with bindings for Java, OCaml and Python
  ready to use and Ruby, C#, GO & Vala available on git repos.
   - Native support for Windows & *nix (with OS X, Linux, *BSD & Solaris
  confirmed).
   - Thread-safe by design.
   - Special support for embedding into firmware or OS kernel.
   - Distributed under the open source BSD license.
 
 **Installed size:** `6.38 MB`  
 **How to install:** `sudo apt install libcapstone4`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 
 - - -
 
 ### python3-capstone
 
  Capstone is a lightweight multi-platform, multi-architecture disassembly
  framework.
   
  These are the Python 3 bindings.
 
 **Installed size:** `518 KB`  
 **How to install:** `sudo apt install python3-capstone`  
 
 {{< spoiler "Dependencies:" >}}
 * libcapstone4
 * python3
 * python3-distutils
 {{< /spoiler >}}
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
