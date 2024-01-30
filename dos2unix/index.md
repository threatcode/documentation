---
Title: dos2unix
Homepage: https://waterlan.home.xs4all.nl/dos2unix.html
Repository: https://salsa.debian.org/debian/dos2unix
Architectures: any
Version: 7.5.1-1
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### dos2unix
 
  This package contains utilities dos2unix, unix2dos, mac2unix,
  unix2mac to convert the line endings of text files between UNIX (LF),
  DOS (CRLF) and Mac (CR) formats.
   
  Text files under Windows and DOS typically have two ASCII characters
  at the end of each line: CR (carriage return) followed by LF (line
  feed). Older Macs used just CR, while UNIX uses just LF. While most
  modern editors can read all these formats, there may still be a need
  to convert files between them.
   
  This is the classic utility developed in 1989.
 
 **Installed size:** `1.80 MB`  
 **How to install:** `sudo apt install dos2unix`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### dos2unix
 
 DOS/Mac to Unix and vice versa text file format converter
 
 ```
 root@kali:~# dos2unix -h
 Usage: dos2unix [options] [file ...] [-n infile outfile ...]
  --allow-chown         allow file ownership change
  -ascii                convert only line breaks (default)
  -iso                  conversion between DOS and ISO-8859-1 character set
    -1252               use Windows code page 1252 (Western European)
    -437                use DOS code page 437 (US) (default)
    -850                use DOS code page 850 (Western European)
    -860                use DOS code page 860 (Portuguese)
    -863                use DOS code page 863 (French Canadian)
    -865                use DOS code page 865 (Nordic)
  -7                    convert 8 bit characters to 7 bit space
  -b, --keep-bom        keep Byte Order Mark
  -c, --convmode        conversion mode
    convmode            ascii, 7bit, iso, mac, default to ascii
  -e, --add-eol         add a line break to the last line if there isn't one
  -f, --force           force conversion of binary files
  -h, --help            display this help text
  -i, --info[=FLAGS]    display file information
    file ...            files to analyze
  -k, --keepdate        keep output file date
  -L, --license         display software license
  -l, --newline         add additional newline
  -m, --add-bom         add Byte Order Mark (default UTF-8)
  -n, --newfile         write to new file
    infile              original file in new-file mode
    outfile             output file in new-file mode
  --no-allow-chown      don't allow file ownership change (default)
  --no-add-eol          don't add a line break to the last line if there isn't one (default)
  -O, --to-stdout       write to standard output
  -o, --oldfile         write to old file (default)
    file ...            files to convert in old-file mode
  -q, --quiet           quiet mode, suppress all warnings
  -r, --remove-bom      remove Byte Order Mark (default)
  -s, --safe            skip binary files (default)
  -u,  --keep-utf16     keep UTF-16 encoding
  -ul, --assume-utf16le assume that the input format is UTF-16LE
  -ub, --assume-utf16be assume that the input format is UTF-16BE
  -v,  --verbose        verbose operation
  -F, --follow-symlink  follow symbolic links and convert the targets
  -R, --replace-symlink replace symbolic links with converted files
                          (original target files remain unchanged)
  -S, --skip-symlink    keep symbolic links and targets unchanged (default)
  -V, --version         display version number
 ```
 
 - - -
 
 ##### mac2unix
 
 DOS/Mac to Unix and vice versa text file format converter
 
 ```
 root@kali:~# mac2unix -h
 Usage: mac2unix [options] [file ...] [-n infile outfile ...]
  --allow-chown         allow file ownership change
  -ascii                convert only line breaks (default)
  -iso                  conversion between DOS and ISO-8859-1 character set
    -1252               use Windows code page 1252 (Western European)
    -437                use DOS code page 437 (US) (default)
    -850                use DOS code page 850 (Western European)
    -860                use DOS code page 860 (Portuguese)
    -863                use DOS code page 863 (French Canadian)
    -865                use DOS code page 865 (Nordic)
  -7                    convert 8 bit characters to 7 bit space
  -b, --keep-bom        keep Byte Order Mark
  -c, --convmode        conversion mode
    convmode            ascii, 7bit, iso, mac, default to ascii
  -e, --add-eol         add a line break to the last line if there isn't one
  -f, --force           force conversion of binary files
  -h, --help            display this help text
  -i, --info[=FLAGS]    display file information
    file ...            files to analyze
  -k, --keepdate        keep output file date
  -L, --license         display software license
  -l, --newline         add additional newline
  -m, --add-bom         add Byte Order Mark (default UTF-8)
  -n, --newfile         write to new file
    infile              original file in new-file mode
    outfile             output file in new-file mode
  --no-allow-chown      don't allow file ownership change (default)
  --no-add-eol          don't add a line break to the last line if there isn't one (default)
  -O, --to-stdout       write to standard output
  -o, --oldfile         write to old file (default)
    file ...            files to convert in old-file mode
  -q, --quiet           quiet mode, suppress all warnings
  -r, --remove-bom      remove Byte Order Mark (default)
  -s, --safe            skip binary files (default)
  -u,  --keep-utf16     keep UTF-16 encoding
  -ul, --assume-utf16le assume that the input format is UTF-16LE
  -ub, --assume-utf16be assume that the input format is UTF-16BE
  -v,  --verbose        verbose operation
  -F, --follow-symlink  follow symbolic links and convert the targets
  -R, --replace-symlink replace symbolic links with converted files
                          (original target files remain unchanged)
  -S, --skip-symlink    keep symbolic links and targets unchanged (default)
  -V, --version         display version number
 ```
 
 - - -
 
 ##### unix2dos
 
 DOS/Mac to Unix and vice versa text file format converter
 
 ```
 root@kali:~# unix2dos -h
 Usage: unix2dos [options] [file ...] [-n infile outfile ...]
  --allow-chown         allow file ownership change
  -ascii                convert only line breaks (default)
  -iso                  conversion between DOS and ISO-8859-1 character set
    -1252               use Windows code page 1252 (Western European)
    -437                use DOS code page 437 (US) (default)
    -850                use DOS code page 850 (Western European)
    -860                use DOS code page 860 (Portuguese)
    -863                use DOS code page 863 (French Canadian)
    -865                use DOS code page 865 (Nordic)
  -7                    convert 8 bit characters to 7 bit space
  -b, --keep-bom        keep Byte Order Mark (default)
  -c, --convmode        conversion mode
    convmode            ascii, 7bit, iso, mac, default to ascii
  -e, --add-eol         add a line break to the last line if there isn't one
  -f, --force           force conversion of binary files
  -h, --help            display this help text
  -i, --info[=FLAGS]    display file information
    file ...            files to analyze
  -k, --keepdate        keep output file date
  -L, --license         display software license
  -l, --newline         add additional newline
  -m, --add-bom         add Byte Order Mark (default UTF-8)
  -n, --newfile         write to new file
    infile              original file in new-file mode
    outfile             output file in new-file mode
  --no-allow-chown      don't allow file ownership change (default)
  --no-add-eol          don't add a line break to the last line if there isn't one (default)
  -O, --to-stdout       write to standard output
  -o, --oldfile         write to old file (default)
    file ...            files to convert in old-file mode
  -q, --quiet           quiet mode, suppress all warnings
  -r, --remove-bom      remove Byte Order Mark
  -s, --safe            skip binary files (default)
  -u,  --keep-utf16     keep UTF-16 encoding
  -ul, --assume-utf16le assume that the input format is UTF-16LE
  -ub, --assume-utf16be assume that the input format is UTF-16BE
  -v,  --verbose        verbose operation
  -F, --follow-symlink  follow symbolic links and convert the targets
  -R, --replace-symlink replace symbolic links with converted files
                          (original target files remain unchanged)
  -S, --skip-symlink    keep symbolic links and targets unchanged (default)
  -V, --version         display version number
 ```
 
 - - -
 
 ##### unix2mac
 
 DOS/Mac to Unix and vice versa text file format converter
 
 ```
 root@kali:~# unix2mac -h
 Usage: unix2mac [options] [file ...] [-n infile outfile ...]
  --allow-chown         allow file ownership change
  -ascii                convert only line breaks (default)
  -iso                  conversion between DOS and ISO-8859-1 character set
    -1252               use Windows code page 1252 (Western European)
    -437                use DOS code page 437 (US) (default)
    -850                use DOS code page 850 (Western European)
    -860                use DOS code page 860 (Portuguese)
    -863                use DOS code page 863 (French Canadian)
    -865                use DOS code page 865 (Nordic)
  -7                    convert 8 bit characters to 7 bit space
  -b, --keep-bom        keep Byte Order Mark (default)
  -c, --convmode        conversion mode
    convmode            ascii, 7bit, iso, mac, default to ascii
  -e, --add-eol         add a line break to the last line if there isn't one
  -f, --force           force conversion of binary files
  -h, --help            display this help text
  -i, --info[=FLAGS]    display file information
    file ...            files to analyze
  -k, --keepdate        keep output file date
  -L, --license         display software license
  -l, --newline         add additional newline
  -m, --add-bom         add Byte Order Mark (default UTF-8)
  -n, --newfile         write to new file
    infile              original file in new-file mode
    outfile             output file in new-file mode
  --no-allow-chown      don't allow file ownership change (default)
  --no-add-eol          don't add a line break to the last line if there isn't one (default)
  -O, --to-stdout       write to standard output
  -o, --oldfile         write to old file (default)
    file ...            files to convert in old-file mode
  -q, --quiet           quiet mode, suppress all warnings
  -r, --remove-bom      remove Byte Order Mark
  -s, --safe            skip binary files (default)
  -u,  --keep-utf16     keep UTF-16 encoding
  -ul, --assume-utf16le assume that the input format is UTF-16LE
  -ub, --assume-utf16be assume that the input format is UTF-16BE
  -v,  --verbose        verbose operation
  -F, --follow-symlink  follow symbolic links and convert the targets
  -R, --replace-symlink replace symbolic links with converted files
                          (original target files remain unchanged)
  -S, --skip-symlink    keep symbolic links and targets unchanged (default)
  -V, --version         display version number
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## unix2dos Usage Example

```
root@kali:~# unix2dos -n unix.txt dos.txt
unix2dos: converting file unix.txt to file dos.txt in DOS format ...
```

## unix2mac Usage Example

```
root@kali:~# unix2mac -n unix.txt mac.txt
unix2mac: converting file unix.txt to file mac.txt in Mac format ...
```

## dos2unix Usage Example

```
root@kali:~# dos2unix -n dos.txt unix2.txt
dos2unix: converting file dos.txt to file unix2.txt in Unix format ...
```

## mac2unix Usage Example

```
root@kali:~# mac2unix -n mac.txt unix3.txt
mac2unix: converting file mac.txt to file unix3.txt in Unix format ...
```
