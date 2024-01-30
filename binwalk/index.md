---
Title: binwalk
Homepage: https://github.com/ReFirmLabs/binwalk
Repository: https://salsa.debian.org/pkg-security-team/binwalk
Architectures: all
Version: 2.3.4+dfsg1-1
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-forensics kali-tools-hardware kali-tools-respond 
Icon: images/binwalk-logo.svg
PackagesInfo: |
 ### binwalk
 
  Binwalk is a tool for searching a given binary image for embedded files
  and executable code. Specifically, it is designed for identifying files
  and code embedded inside of firmware images. Binwalk uses the libmagic
  library, so it is compatible with magic signatures created for the Unix
  file utility.
   
  Binwalk also includes a custom magic signature file which contains
  improved signatures for files that are commonly found in firmware images
  such as compressed/archived files, firmware headers, Linux kernels,
  bootloaders, filesystems, etc.
   
  This package is an empty package, because the binary tool is already
  provided with the library, dependency of this package.
 
 **Installed size:** `15 KB`  
 **How to install:** `sudo apt install binwalk`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-binwalk
 {{< /spoiler >}}
 
 ##### binwalk
 
 Tool for searching binary images for embedded files and executable code
 
 ```
 root@kali:~# binwalk -h
 
 Binwalk v2.3.3
 Craig Heffner, ReFirmLabs
 https://github.com/ReFirmLabs/binwalk
 
 Usage: binwalk [OPTIONS] [FILE1] [FILE2] [FILE3] ...
 
 Disassembly Scan Options:
     -Y, --disasm                 Identify the CPU architecture of a file using the capstone disassembler
     -T, --minsn=<int>            Minimum number of consecutive instructions to be considered valid (default: 500)
     -k, --continue               Don't stop at the first match
 
 Signature Scan Options:
     -B, --signature              Scan target file(s) for common file signatures
     -R, --raw=<str>              Scan target file(s) for the specified sequence of bytes
     -A, --opcodes                Scan target file(s) for common executable opcode signatures
     -m, --magic=<file>           Specify a custom magic file to use
     -b, --dumb                   Disable smart signature keywords
     -I, --invalid                Show results marked as invalid
     -x, --exclude=<str>          Exclude results that match <str>
     -y, --include=<str>          Only show results that match <str>
 
 Extraction Options:
     -e, --extract                Automatically extract known file types
     -D, --dd=<type[:ext[:cmd]]>  Extract <type> signatures (regular expression), give the files an extension of <ext>, and execute <cmd>
     -M, --matryoshka             Recursively scan extracted files
     -d, --depth=<int>            Limit matryoshka recursion depth (default: 8 levels deep)
     -C, --directory=<str>        Extract files/folders to a custom directory (default: current working directory)
     -j, --size=<int>             Limit the size of each extracted file
     -n, --count=<int>            Limit the number of extracted files
     -0, --run-as=<str>           Execute external extraction utilities with the specified user's privileges
     -1, --preserve-symlinks      Do not sanitize extracted symlinks that point outside the extraction directory (dangerous)
     -r, --rm                     Delete carved files after extraction
     -z, --carve                  Carve data from files, but don't execute extraction utilities
     -V, --subdirs                Extract into sub-directories named by the offset
 
 Entropy Options:
     -E, --entropy                Calculate file entropy
     -F, --fast                   Use faster, but less detailed, entropy analysis
     -J, --save                   Save plot as a PNG
     -Q, --nlegend                Omit the legend from the entropy plot graph
     -N, --nplot                  Do not generate an entropy plot graph
     -H, --high=<float>           Set the rising edge entropy trigger threshold (default: 0.95)
     -L, --low=<float>            Set the falling edge entropy trigger threshold (default: 0.85)
 
 Binary Diffing Options:
     -W, --hexdump                Perform a hexdump / diff of a file or files
     -G, --green                  Only show lines containing bytes that are the same among all files
     -i, --red                    Only show lines containing bytes that are different among all files
     -U, --blue                   Only show lines containing bytes that are different among some files
     -u, --similar                Only display lines that are the same between all files
     -w, --terse                  Diff all files, but only display a hex dump of the first file
 
 Raw Compression Options:
     -X, --deflate                Scan for raw deflate compression streams
     -Z, --lzma                   Scan for raw LZMA compression streams
     -P, --partial                Perform a superficial, but faster, scan
     -S, --stop                   Stop after the first result
 
 General Options:
     -l, --length=<int>           Number of bytes to scan
     -o, --offset=<int>           Start scan at this file offset
     -O, --base=<int>             Add a base address to all printed offsets
     -K, --block=<int>            Set file block size
     -g, --swap=<int>             Reverse every n bytes before scanning
     -f, --log=<file>             Log results to file
     -c, --csv                    Log results to file in CSV format
     -t, --term                   Format output to fit the terminal window
     -q, --quiet                  Suppress output to stdout
     -v, --verbose                Enable verbose output
     -h, --help                   Show help output
     -a, --finclude=<str>         Only scan files whose names match this regex
     -p, --fexclude=<str>         Do not scan files whose names match this regex
     -s, --status=<int>           Enable the status server on the specified port
 
 ```
 
 - - -
 
 ### python3-binwalk
 
  Binwalk is a tool for searching a given binary image for embedded files
  and executable code. Specifically, it is designed for identifying files
  and code embedded inside of firmware images. Binwalk uses the libmagic
  library, so it is compatible with magic signatures created for the Unix
  file utility.
   
  Binwalk also includes a custom magic signature file which contains
  improved signatures for files that are commonly found in firmware images
  such as compressed/archived files, firmware headers, Linux kernels,
  bootloaders, filesystems, etc.
   
  This is the Python 3 version of the package.
 
 **Installed size:** `559 KB`  
 **How to install:** `sudo apt install python3-binwalk`  
 
 {{< spoiler "Dependencies:" >}}
 * libmagic1
 * python3
 {{< /spoiler >}}
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## binwalk Usage Example

Run a file signature scan (`-B`) on the given firmware file (`ddwrt-linksys-wrt1200ac-webflash.bin`):

```
root@kali:~# binwalk -B ddwrt-linksys-wrt1200ac-webflash.bin

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             TRX firmware header, little endian, image size: 37883904 bytes, CRC32: 0x95C5DF32, flags: 0x1, version: 1, header size: 28 bytes, loader offset: 0x1C, linux kernel offset: 0x0, rootfs offset: 0x0
28            0x1C            uImage header, header size: 64 bytes, header CRC: 0x780C2742, created: 2018-10-10 02:12:20, image size: 2150281 bytes, Data Address: 0x8000, Entry Point: 0x8000, data CRC: 0xA097CFEA, OS: Linux, CPU: ARM, image type: OS Kernel Image, compression type: none, image name: "DD-WRT"
92            0x5C            Linux kernel ARM boot executable zImage (little-endian)
2460          0x99C           device tree image (dtb)
23432         0x5B88          xz compressed data
23776         0x5CE0          xz compressed data
2117484       0x204F6C        device tree image (dtb)
3145756       0x30001C        UBI erase count header, version: 1, EC: 0x0, VID header offset: 0x800, data offset: 0x1000
```
