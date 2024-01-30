---
Title: statsprocessor
Homepage: https://github.com/hashcat/statsprocessor
Repository: https://salsa.debian.org/pkg-security-team/statsprocessor
Architectures: any
Version: 0.11+git20160316-3
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-passwords 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### statsprocessor
 
  Statsprocessor is a word generator based on per-position Markov chains
  packed into a single stand-alone binary. It generates candidate words based
  on a Hashcat format .hcstat file by using this information to determine which
  letter is following which letter based on the analysis of the original input
  dictionary used to generate the .hcstat. The resulting words can then, for
  example, be postprocessed and fed into Hashcat or other password recovery
  tools.
 
 **Installed size:** `46 KB`  
 **How to install:** `sudo apt install statsprocessor`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### sp32
 
 Word generator based on per-position Markov chains
 
 ```
 root@kali:~# sp32 -h
 sp by atom, High-Performance word generator based on hashcat markov stats
 
 Usage: sp32 [options]... hcstat-file [filter-mask]
 
 * Startup:
 
   -V,  --version             Print version
   -h,  --help                Print help
 
 * Increment:
 
        --pw-min=NUM          Start incrementing at NUM
        --pw-max=NUM          Stop incrementing at NUM
 
 * Markov:
 
        --markov-disable      Emulates maskprocessor output
        --markov-classic      No per-position tables
        --threshold=NUM       Filter out chars after NUM chars added
                              Set to 0 to disable
 
 * Misc:
 
        --combinations        Calculate number of combinations
        --hex-charset         Assume charset is given in hex
 
 * Resources:
 
   -s,  --skip=NUM            skip number of words (for restore)
   -l,  --limit=NUM           limit number of words (for distributed)
 
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
   ?h = 8 bit characters from 0xc0 - 0xff
   ?D = 8 bit characters from german alphabet
   ?F = 8 bit characters from french alphabet
   ?R = 8 bit characters from russian alphabet
 
 ```
 
 - - -
 
 ##### sp64
 
 Word generator based on per-position Markov chains
 
 ```
 root@kali:~# sp64 -h
 sp by atom, High-Performance word generator based on hashcat markov stats
 
 Usage: sp64 [options]... hcstat-file [filter-mask]
 
 * Startup:
 
   -V,  --version             Print version
   -h,  --help                Print help
 
 * Increment:
 
        --pw-min=NUM          Start incrementing at NUM
        --pw-max=NUM          Stop incrementing at NUM
 
 * Markov:
 
        --markov-disable      Emulates maskprocessor output
        --markov-classic      No per-position tables
        --threshold=NUM       Filter out chars after NUM chars added
                              Set to 0 to disable
 
 * Misc:
 
        --combinations        Calculate number of combinations
        --hex-charset         Assume charset is given in hex
 
 * Resources:
 
   -s,  --skip=NUM            skip number of words (for restore)
   -l,  --limit=NUM           limit number of words (for distributed)
 
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
   ?h = 8 bit characters from 0xc0 - 0xff
   ?D = 8 bit characters from german alphabet
   ?F = 8 bit characters from french alphabet
   ?R = 8 bit characters from russian alphabet
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## statsprocessor Usage Example

Generate passwords with a minimum length of 6 (`–pw-min=6`) and a maximum length of 8 (`–pw-max=8`) using the stats in the provided file (`/usr/share/oclhashcat/hashcat.hcstat`):

```
root@kali:~# statsprocessor --pw-min=6 --pw-max=8 /usr/share/oclhashcat/hashcat.hcstat
13nger
13aner
13rina
13erer
13ller
131200
13ster
13iner
```
