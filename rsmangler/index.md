---
Title: rsmangler
Homepage: https://digi.ninja/projects/rsmangler.php
Repository: https://gitlab.com/kalilinux/packages/rsmangler
Architectures: all
Version: 1.5-0kali3
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-passwords 
Icon: images/rsmangler-logo.svg
PackagesInfo: |
 ### rsmangler
 
  RSMangler will take a wordlist and perform various
  manipulations on it similar to those done by John the
  Ripper the main difference being that it will first take
  the input words and generate all permutations and the
  acronym of the words (in order they appear in the file)
  before it applies the rest of the mangles.
 
 **Installed size:** `24 KB`  
 **How to install:** `sudo apt install rsmangler`  
 
 {{< spoiler "Dependencies:" >}}
 * ruby
 {{< /spoiler >}}
 
 ##### rsmangler
 
 
 ```
 root@kali:~# rsmangler -h
 rsmangler v 1.5 Robin Wood (robin@digi.ninja) <https://digi.ninja>
 
 Basic usage:
 
 	rsmangler --file wordlist.txt
 
 To pass the initial words in on standard in do:
 
 	cat wordlist.txt | rsmangler
 
 To send the output to a file:
 
 	rsmangler --file wordlist.txt --output mangled.txt
 
 	All options are ON by default, these parameters turn them OFF
 
 	Usage: rsmangler [OPTION]
 	--help, -h: show help
 	--file, -f: the input file, use - for STDIN
 	--output, -o: the output file, use - for STDOUT
 	--max, -x: maximum word length
 	--min, -m: minimum word length
 	--perms, -p: permutate all the words
 	--double, -d: double each word
 	--reverse, -r: reverser the word
 	--leet, -t: l33t speak the word
 	--full-leet, -T: all posibilities l33t
 	--capital, -c: capitalise the word
 	--upper, -u: uppercase the word
 	--lower, -l: lowercase the word
 	--swap, -s: swap the case of the word
 	--ed, -e: add ed to the end of the word
 	--ing, -i: add ing to the end of the word
 	--punctuation: add common punctuation to the end of the word
 	--years, -y: add all years from 1990 to current year to start and end
 	--acronym, -a: create an acronym based on all the words entered in order and add to word list
 	--common, -C: add the following words to start and end: admin, sys, pw, pwd
 	--pna: add 01 - 09 to the end of the word
 	--pnb: add 01 - 09 to the beginning of the word
 	--na: add 1 - 123 to the end of the word
 	--nb: add 1 - 123 to the beginning of the word
 	--force: don't check output size
 	--space: add spaces between words
 	--allow-duplicates: allow duplicates in the output list
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## rsmangler Usage Example

Use the original wordlist (`cat words.txt |`) and mangle words with a minimum length of 6 (`-m 6`) and maximum length of 8 (`-x 8`), using stdin as input (`–file -`) and redirecting the results to a new wordlist (`> mangled.txt`):

```
root@kali:~# cat words.txt | rsmangler -m 6 -x 8 --file - > mangled.txt
root@kali:~# wc -l mangled.txt
367 mangled.txt
root@kali:~# wc -l words.txt
3 words.txt
```
