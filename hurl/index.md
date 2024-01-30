---
Title: hurl
Homepage: https://github.com/fnord0/hURL
Repository: https://gitlab.com/kalilinux/packages/hurl
Architectures: all
Version: 2.1-0kali3
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### hurl
 
  This package contains a hexadecimal & URL (en/de)coder.
 
 **Installed size:** `187 KB`  
 **How to install:** `sudo apt install hurl`  
 
 {{< spoiler "Dependencies:" >}}
 * libcgi-pm-perl
 * perl
 {{< /spoiler >}}
 
 ##### hURL
 
 
 ```
 root@kali:~# hURL -h
 .::[ hURL - hexadecimal & URL (en/de)coder ]::.
 v2.1 @COPYLEFT  ->  fnord0 <at> riseup <dot> net
 
   USAGE: /usr/bin/hURL [ -flag|--flag ] [ -f <file1>,<file2> ] [ string ]
 
   COMMAND LINE ARGUMENTS
    -M|--menu	=> Menu-driven GUI		 ;  /usr/bin/hURL -M
    -U|--URL	=> URL encode			 ;  /usr/bin/hURL -U "hello world"
    -u|--url	=> uRL decode			 ;  /usr/bin/hURL -u "hello%20world"
    -D|--DURL	=> Double URL encode		 ;  /usr/bin/hURL -D "hello world"
    -d|--durl	=> double URL decode		 ;  /usr/bin/hURL -d "hello%2520world"
    -B|--BASE64	=> Base64 encode		 ;  /usr/bin/hURL -B "hello world"
    -b|--base64	=> base64 decode		 ;  /usr/bin/hURL -b "aGVsbG8gd29ybGQ="
    -H|--HTML	=> HTML encode			 ;  /usr/bin/hURL -H "<hello world>"
    -h|--html	=> hTML decode			 ;  /usr/bin/hURL -h "&lt;hello world&gt;"
    -X|--HEX	=> ascii ->  heX		 ;  /usr/bin/hURL -X "hello world"
 	--esc   :: output in escaped string	    ; "\x00\x01\x02\x03 ..."
 	--pair  :: output in hexpair format	    ; 00010203 ...
    -x|--hex	=> hex   ->  ascii		 ;  /usr/bin/hURL -x "68656c6c6f20776f726c64"
    -I|--INT	=> Int   ->  hex		 ;  /usr/bin/hURL -I "10"
    -i|--int	=> hex   ->  int		 ;  /usr/bin/hURL -i "0xa"
    -n|--nint	=> -int  ->  hex		 ;  /usr/bin/hURL -n -- -77
    -N|--NHEX	=> -hex  ->  iNt		 ;  /usr/bin/hURL -N 0xffffffb3
    -T|--INTB	=> inT   ->  bin		 ;  /usr/bin/hURL -T 30
    -t|--bint	=> bin   ->  int		 ;  /usr/bin/hURL -t 1010
    -F|--FLOATH	=> Float ->  hex		 ;  /usr/bin/hURL -F 3.33
    -l|--hfloat	=> hex   ->  float		 ;  /usr/bin/hURL -l 0x40551ed8
    -o|--octh	=> octal ->  hex		 ;  /usr/bin/hURL -o 35
    -O|--HOCT	=> hex   ->  Octal		 ;  /usr/bin/hURL -O 0x12
    -0|--binh	=> bin   ->  hex		 ;  /usr/bin/hURL -0 1100011
    -1|--hexb	=> hex   ->  bin		 ;  /usr/bin/hURL -1 0x63
    -2|--SHA1	=> SHA1 checksum		 ;  /usr/bin/hURL -2 "hello world"
    -3|--SHA224	=> SHA224 checksum		 ;  /usr/bin/hURL -3 "hello world"
    -4|--SHA256	=> SHA256 checksum		 ;  /usr/bin/hURL -4 "hello world"
    -5|--SHA384	=> SHA384 checksum		 ;  /usr/bin/hURL -5 "hello world"
    -6|--SHA512	=> SHA512 checksum		 ;  /usr/bin/hURL -6 "hello world"
    -7|--ROT13	=> ROT13 encode			 ;  /usr/bin/hURL -7 "hello world"
    -8|--rot13	=> ROT13 decode			 ;  /usr/bin/hURL -8 "uryyb jbeyq"
    -9|--stack	=> push string 2 stack (corelan) ;  /usr/bin/hURL -9 "hello world"
 	--esc   :: output in escaped string	    ; "\x00\x01\x02\x03 ..."
 	--pair  :: output in hexpair format	    ; 00010203 ...
 	--ansiC :: output in C format		    ; 0x00, 0x01, 0x02, 0x03 ...
    -m|--md5	=> md5 digest			 ;  /usr/bin/hURL -m "hello world"
    -e|--net	=> int -> hex (net-byte order)   ;  /usr/bin/hURL -e 4444
    -E|--NET	=> hex (nEt-byte order) ->  int  ;  /usr/bin/hURL -E 5c11
    -w|--wbin	=> hex [file] -> binary [file]	 ;  /usr/bin/hURL -w -f <INfile> <OUTfile>
    -r|--rbin	=> binary [file] -> hex (corelan);  /usr/bin/hURL -r -f /tmp/msgbox.bin
 	--esc   :: output in escaped string	    ; "\x00\x01\x02\x03 ..."
 	--pair  :: output in hexpair format	    ; 00010203 ...
 	--ansiC :: output in C format		    ; 0x00, 0x01, 0x02, 0x03 ...
 
    --color|--nocolor	=> enable/disable colored output [default is ENABLED]
    --corelan		=> display corelan reference
    --help		=> displays help
    --man		=> displays extended help with examples
    --version		=> displays version information
 
    -s				=> suppress (display result only)
    -f|--file <file1>,<file2>	=> use file(s) as input
    [string]			=> string as input
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## hurl Usage Examples

Decode the given base64-encoded string (`-b “S2FsaSBMaW51eAo=”`) and display the result:

```
root@kali:~# hURL -b "S2FsaSBMaW51eAo="

Original string       :: S2FsaSBMaW51eAo=
base64 DEcoded string :: Kali Linux
```
