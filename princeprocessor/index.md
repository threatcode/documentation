---
Title: princeprocessor
Homepage: https://github.com/hashcat/princeprocessor
Repository: https://salsa.debian.org/pkg-security-team/princeprocessor
Architectures: amd64 arm64 mips64el ppc64el s390x alpha kfreebsd-amd64 ppc64 riscv64 sparc64 x32
Version: 0.22-4
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### princeprocessor
 
  Princeprocessor is a password candidate generator and can be thought of
  as an advanced combinator attack. Rather than taking as input two different
  wordlists and then outputting all the possible two word combinations though,
  princeprocessor only has one input wordlist and builds "chains" of combined
  words. These chains can have 1 to N words from the input wordlist
  concatenated together.
  The name PRINCE is used as an acronym and stands for PRobability INfinite
  Chained Elements, which are the building blocks of the algorithm.
 
 **Installed size:** `121 KB`  
 **How to install:** `sudo apt install princeprocessor`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### princeprocessor
 
 Standalone password candidate generator using the PRINCE algorithm
 
 ```
 root@kali:~# princeprocessor -h
 Usage: princeprocessor [options] [<] wordlist
 
 * Startup:
 
   -V,  --version             Print version
   -h,  --help                Print help
 
 * Misc:
 
        --keyspace            Calculate number of combinations
 
 * Optimization:
 
        --pw-min=NUM          Print candidate if length is greater than NUM
        --pw-max=NUM          Print candidate if length is smaller than NUM
        --elem-cnt-min=NUM    Minimum number of elements per chain
        --elem-cnt-max=NUM    Maximum number of elements per chain
        --wl-dist-len         Calculate output length distribution from wordlist
        --wl-max=NUM          Load only NUM words from input wordlist or use 0 to disable
   -c,  --dupe-check-disable  Disable dupes check for faster initial load
        --save-pos-disable    Save the position for later resume with -s
 
 * Resources:
 
   -s,  --skip=NUM            Skip NUM passwords from start (for distributed)
   -l,  --limit=NUM           Limit output to NUM passwords (for distributed)
 
 * Files:
 
   -o,  --output-file=FILE    Output-file
 
 * Amplifier:
 
        --case-permute        For each word in the wordlist that begins with a letter
                              generate a word with the opposite case of the first letter
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
