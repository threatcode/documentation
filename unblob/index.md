---
Title: unblob
Homepage: https://unblob.org/
Repository: https://gitlab.com/kalilinux/packages/unblob
Architectures: all
Version: 23.10.31+ds-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### unblob
 
  This package contains an accurate, fast, and easy-to-use extraction suite. It
  parses unknown binary blobs for more than 30 different archive, compression,
  and file-system formats, extracts their content recursively, and carves out
  unknown chunks that have not been accounted for.
   
  This package installs the library for Python 3.
 
 **Installed size:** `420 KB`  
 **How to install:** `sudo apt install unblob`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-arpy
 * python3-attr
 * python3-click
 * python3-cryptography 
 * python3-dissect.cstruct
 * python3-jefferson
 * python3-lark
 * python3-lief
 * python3-lz4
 * python3-magic
 * python3-plotext
 * python3-pluggy
 * python3-pyfatfs
 * python3-pyperscan
 * python3-rarfile
 * python3-rich
 * python3-structlog
 * python3-treelib
 * python3-ubireader
 * python3-unblob-native
 {{< /spoiler >}}
 
 ##### unblob
 
 
 ```
 root@kali:~# unblob -h
 Usage: unblob [OPTIONS] FILE
 
   A tool for getting information out of any kind of binary blob.
 
   You also need these extractor commands to be able to extract the supported
   file types: 7z, debugfs, jefferson, lz4, lziprecover, lzop, sasquatch,
   sasquatch-v4be, simg2img, ubireader_extract_files, ubireader_extract_images,
   unar, zstd
 
   NOTE: Some older extractors might not be compatible.
 
 Options:
   -e, --extract-dir DIRECTORY     Extract the files to this directory. Will be
                                   created if doesn't exist.
   -f, --force                     Force extraction even if outputs already
                                   exist (they are removed).
   -d, --depth INTEGER RANGE       Recursion depth. How deep should we extract
                                   containers.  [default: 10; x>=1]
   -n, --entropy-depth INTEGER RANGE
                                   Entropy calculation depth. How deep should
                                   we calculate entropy for unknown files? 1
                                   means input files only, 0 turns it off.
                                   [default: 1; x>=0]
   -P, --plugins-path PATH         Load plugins from the provided path.
   -S, --skip-magic TEXT           Skip processing files with given magic
                                   prefix  [default: BFLT, JPEG, GIF, PNG,
                                   SQLite, compiled Java class, TrueType Font
                                   data, PDF document, magic binary file, MS
                                   Windows icon resource, Web Open Font Format,
                                   GNU message catalog, Xilinx BIT data,
                                   Microsoft Excel, Microsoft Word, Microsoft
                                   PowerPoint, Microsoft OOXML, OpenDocument,
                                   Macromedia Flash data, MPEG, HP Printer Job
                                   Language, Erlang BEAM file, python,
                                   Composite Document File V2 Document, Windows
                                   Embedded CE binary image]
   -p, --process-num INTEGER RANGE
                                   Number of worker processes to process files
                                   parallelly.  [default: 8; x>=1]
   --report PATH                   File to store metadata generated during the
                                   extraction process (in JSON format).
   --log PATH                      File to save logs (in text format). Defaults
                                   to unblob.log.
   -s, --skip_extraction           Only carve chunks and skip further
                                   extraction
   -k, --keep-extracted-chunks     Keep extracted chunks
   -v, --verbose                   Verbosity level, counting, maximum level: 3
                                   (use: -v, -vv, -vvv)
   --show-external-dependencies    Shows commands needs to be available for
                                   unblob to work properly
   --version                       Shows unblob version
   -h, --help                      Show this message and exit.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
