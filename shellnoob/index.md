---
Title: shellnoob
Homepage: https://github.com/reyammer/shellnoob
Repository: https://gitlab.com/kalilinux/packages/shellnoob
Architectures: amd64 armel armhf i386
Version: 2.1+git20170425-0kali4
Metapackages: kali-linux-everything kali-tools-exploitation 
Icon: images/shellnoob-logo.svg
PackagesInfo: |
 ### shellnoob
 
  Features:
      * convert shellcode between different formats and sources. Formats
       currently supported: asm, bin, hex, obj, exe, C, Python, ruby, pretty,
       safeasm, completec, shellstorm. (All details in the "Formats description"
       section.)
      * interactive asm-to-opcode conversion (and viceversa) mode. This is
        useful when you cannot use specific bytes in the shellcode and you want
        to figure out if a specific assembly instruction will cause problems.
      * support for both ATT & Intel syntax. Check the --intel switch.
      * support for 32 and 64 bits (when playing on x86_64 machine). Check
        the --64 switch.
      * resolve syscall numbers, constants, and error numbers
      * portable and easily deployable (it only relies on gcc/as/objdump and
        Python) And it just one self-contained Python script!
      * in-place development: you run ShellNoob directly on the target
        architecture
      * built-in support for Linux/x86, Linux/x86_64, Linux/ARM, FreeBSD/x86,
        FreeBSD/x86_64.
      * "*prepend breakpoint*" option. Check the -c switch.
      * read from stdin / write to stdout support (use "-" as filename)
      * uber cheap debugging: check the --to-strace and --to-gdb option!
      * Use ShellNoob as a Python module in your scripts! Check the "ShellNoob
        as a library" section.
      * Verbose mode shows the low-level steps of the conversion: useful to
        debug / understand / learn
      * Extra plugins: binary patching made easy with the --file-patch,
        --vm-patch, --fork-nopper options
 
 **Installed size:** `96 KB`  
 **How to install:** `sudo apt install shellnoob`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 {{< /spoiler >}}
 
 ##### shellnoob
 
 
 ```
 root@kali:~# shellnoob -h
 shellnoob.py [--from-INPUT] (input_file_path | - ) [--to-OUTPUT] [output_file_path | - ]
 shellnoob.py -c (prepend a breakpoint (Warning: only few platforms/OS are supported!)
 shellnoob.py --64 (64 bits mode, default: 32 bits)
 shellnoob.py --intel (intel syntax mode, default: att)
 shellnoob.py -q (quite mode)
 shellnoob.py -v (or -vv, -vvv)
 shellnoob.py --to-strace (compiles it & run strace)
 shellnoob.py --to-gdb (compiles it & run gdb & set breakpoint on entrypoint)
 
 Standalone "plugins"
 shellnoob.py -i [--to-asm | --to-opcode ] (for interactive mode)
 shellnoob.py --get-const <const>
 shellnoob.py --get-sysnum <sysnum>
 shellnoob.py --get-strerror <errno>
 shellnoob.py --file-patch <exe_fp> <file_offset> <data> (in hex). (Warning: tested only on x86/x86_64)
 shellnoob.py --vm-patch <exe_fp> <vm_address> <data> (in hex). (Warning: tested only on x86/x86_64)
 shellnoob.py --fork-nopper <exe_fp> (this nops out the calls to fork(). Warning: tested only on x86/x86_64)
 
 "Installation"
 shellnoob.py --install [--force] (this just copies the script in a convinient position)
 shellnoob.py --uninstall [--force]
 
 Supported INPUT format: asm, obj, bin, hex, c, shellstorm
 Supported OUTPUT format: asm, obj, exe, bin, hex, c, completec, python, bash, ruby, pretty, safeasm
 All combinations from INPUT to OUTPUT are supported!
 
 Check out the README file for more info.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## shellnoob Usage Example

Start in interactive mode (`-i`) in asm to opcode mode (`–to-opcode`):

```
root@kali:~# shellnoob -i --to-opcode
asm_to_opcode selected (type "quit" or ^C to end)
>> xchg %eax, %esp
xchg %eax, %esp ~> 94
>> ret
ret ~> c3
>>
```
