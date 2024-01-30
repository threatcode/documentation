---
Title: twofi
Homepage: https://www.digininja.org/projects/twofi.php
Repository: https://gitlab.com/kalilinux/packages/twofi
Architectures: all
Version: 2.0-0kali2
Metapackages: kali-linux-everything kali-linux-large kali-tools-information-gathering kali-tools-passwords 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### twofi
 
  When attempting to crack passwords custom word lists are
  very useful additions to standard dictionaries. An
  interesting idea originally released on the "7 Habits of
  Highly Effective Hackers" blog was to use Twitter to help
  generate those lists based on searches for keywords related
  to the list that is being cracked. I've expanded this idea
  into twofi which will take multiple search terms and return
  a word list sorted by most common first.
 
 **Installed size:** `38 KB`  
 **How to install:** `sudo apt install twofi`  
 
 {{< spoiler "Dependencies:" >}}
 * ruby
 * ruby-twitter
 {{< /spoiler >}}
 
 ##### twofi
 
 
 ```
 root@kali:~# twofi -h
 twoif 2.0-beta Robin Wood (robin@digininja.org) (www.digininja.org)
 twoif - Twitter Words of Interest
 
 Usage: twoif [OPTIONS]
 	--help, -h: show help
 	--config <file>: config file, default is twofi.yml
 	--count, -c: include the count with the words
 	--min_word_length, -m: minimum word length
 	--term_file, -T <file>: a file containing a list of terms
 	--terms, -t: comma separated search terms
 		quote words containing spaces, no space after commas
 	--user_file, -U <file>: a file containing a list of users
 	--users, -u: comma separated usernames
 		quote words containing spaces, no space after commas
 	--verbose, -v: verbose
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## Video

<script id="asciicast-32180" src="https://asciinema.org/a/32180.js" async type="text/javascript"></script>
