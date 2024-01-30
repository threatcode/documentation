---
Title: maskprocessor
Homepage: https://github.com/hashcat/maskprocessor
Repository: https://salsa.debian.org/pkg-security-team/maskprocessor
Architectures: any
Version: 0.73+git20170609.1708898-3
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-passwords 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### maskprocessor
 
  Maskprocessor is a fast word list generator. It enumerates all combinations
  from a given user-defined keyspace and outputs the results. Since it supports
  different alphabets (which also can be combined) at different positions in the
  generation template ('mask'), this approach allows a more fine-tunable
  generation of candidates than using 'naive' brute force enumeration of words.
  Masks are defined using the description also used in the Hashcat password
  recovery utility.
 
 **Installed size:** `45 KB`  
 **How to install:** `sudo apt install maskprocessor`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### mp32
 
 High-performance word generator with a per-position configurable charset
 
 ```
 root@kali:~# mp32 -h
 High-Performance word generator with a per-position configureable charset
 
 Usage: mp32 [options]... mask
 
 * Startup:
 
   -V,  --version             Print version
   -h,  --help                Print help
 
 * Increment:
 
   -i,  --increment=NUM:NUM   Enable increment mode. 1st NUM=start, 2nd NUM=stop
                              Example: -i 4:8 searches lengths 4-8 (inclusive)
 
 * Misc:
 
        --combinations        Calculate number of combinations
        --hex-charset         Assume charset is given in hex
   -q,  --seq-max=NUM         Maximum number of multiple sequential characters
   -r,  --occurrence-max=NUM  Maximum number of occurrence of a character
 
 * Resources:
 
   -s,  --start-at=WORD       Start at specific position
   -l,  --stop-at=WORD        Stop at specific position
 
 * Files:
 
   -o,  --output-file=FILE    Output-file
 
 * Custom charsets:
 
   -1,  --custom-charset1=CS  User-defineable charsets
   -2,  --custom-charset2=CS  Example:
   -3,  --custom-charset3=CS  --custom-charset1=?dabcdef
   -4,  --custom-charset4=CS  sets charset ?1 to 0123456789abcdef
 
 * Built-in charsets:
 
   ?l = abcdefghijklmnopqrstuvwxyz
   ?u = ABCDEFGHIJKLMNOPQRSTUVWXYZ
   ?d = 0123456789
   ?s =  !"#$%&'()*+,-./:;<=>?@[\]^_`{|}~
   ?a = ?l?u?d?s
   ?b = 0x00 - 0xff
 
 ```
 
 - - -
 
 ##### mp64
 
 High-performance word generator with a per-position configurable charset
 
 ```
 root@kali:~# mp64 -h
 High-Performance word generator with a per-position configureable charset
 
 Usage: mp64 [options]... mask
 
 * Startup:
 
   -V,  --version             Print version
   -h,  --help                Print help
 
 * Increment:
 
   -i,  --increment=NUM:NUM   Enable increment mode. 1st NUM=start, 2nd NUM=stop
                              Example: -i 4:8 searches lengths 4-8 (inclusive)
 
 * Misc:
 
        --combinations        Calculate number of combinations
        --hex-charset         Assume charset is given in hex
   -q,  --seq-max=NUM         Maximum number of multiple sequential characters
   -r,  --occurrence-max=NUM  Maximum number of occurrence of a character
 
 * Resources:
 
   -s,  --start-at=WORD       Start at specific position
   -l,  --stop-at=WORD        Stop at specific position
 
 * Files:
 
   -o,  --output-file=FILE    Output-file
 
 * Custom charsets:
 
   -1,  --custom-charset1=CS  User-defineable charsets
   -2,  --custom-charset2=CS  Example:
   -3,  --custom-charset3=CS  --custom-charset1=?dabcdef
   -4,  --custom-charset4=CS  sets charset ?1 to 0123456789abcdef
 
 * Built-in charsets:
 
   ?l = abcdefghijklmnopqrstuvwxyz
   ?u = ABCDEFGHIJKLMNOPQRSTUVWXYZ
   ?d = 0123456789
   ?s =  !"#$%&'()*+,-./:;<=>?@[\]^_`{|}~
   ?a = ?l?u?d?s
   ?b = 0x00 - 0xff
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## maskprocessor Usage Example

Generate a list of words beginning with (`pass`) and append one digit (`?d`) and one lowercase letter (`?l`):

```
root@kali:~# maskprocessor pass?d?l
pass0a
pass0b
pass0c
pass0d
pass0e
pass0f
pass0g
```
