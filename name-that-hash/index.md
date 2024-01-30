---
Title: name-that-hash
Homepage: https://github.com/HashPals/Name-That-Hash
Repository: https://gitlab.com/kalilinux/packages/name-that-hash
Architectures: all
Version: 1.11.0-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### name-that-hash
 
  This package contains a utility to identify hash types.
   
  Have you ever come across a hash such as 5f4dcc3b5aa765d61d8327deb882cf99 and
  wondered what type of hash type that is?
   
  Name-that-hash will name it for you.
 
 **Installed size:** `123 KB`  
 **How to install:** `sudo apt install name-that-hash`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3 
 * python3-click 
 * python3-colorama
 * python3-pygments
 * python3-rich 
 {{< /spoiler >}}
 
 ##### name-that-hash
 
 
 ```
 root@kali:~# name-that-hash --help
 Usage: name-that-hash [OPTIONS]
 
   Name That Hash - Instantly name the type of any hash!
 
   Github:
 
   https://github.com/hashpals/name-that-hash
 
   From the creator of RustScan and Ciphey. Follow me on Twitter!
 
   https://twitter.com/bee_sec_san
 
   Example usage:
 
       nth --text '5f4dcc3b5aa765d61d8327deb882cf99'
 
       nth --file hash
 
       nth --text '5f4dcc3b5aa765d61d8327deb882cf99' --greppable
 
       Note: Use single quotes ' as inverted commas " do not work well on
       Linux.
 
 Options:
   -t, --text TEXT      Check one hash, use single quotes ' as inverted commas
                        " messes up on Linux.
   -f, --file FILENAME  Checks every hash in a newline separated file.
   -g, --greppable      Are you going to grep this output? Prints in JSON
                        format.
   -b64, --base64       Decodes hashes in Base64 before identification. For
                        files with mixed Base64 & non-encoded it attempts
                        base64 first and then falls back to normal hash
                        identification per hash.
   -a, --accessible     Turn on accessible mode, does not print ASCII art. Also
                        does not print very large blocks of text, as this can
                        cause some pain with screenreaders. This reduces the
                        information you get. If you want the least likely
                        feature but no banner, use --no-banner.
   -e, --extreme        Searches for hashes within a string. This mode will get
                        5d41402abc4b2a76b9719d911017c592 from
                        ####5d41402abc4b2a76b9719d911017c592###
   --no-banner          Removes banner from startup.
   --no-john            Don't print John The Ripper Information.
   --no-hashcat         Don't print Hashcat Information.
   -v, --verbose        Turn on debugging logs. -vvv for maximum logs.
   --help               Show this message and exit.
 ```
 
 - - -
 
 ##### nth
 
 
 ```
 root@kali:~# nth --help
 Usage: nth [OPTIONS]
 
   Name That Hash - Instantly name the type of any hash!
 
   Github:
 
   https://github.com/hashpals/name-that-hash
 
   From the creator of RustScan and Ciphey. Follow me on Twitter!
 
   https://twitter.com/bee_sec_san
 
   Example usage:
 
       nth --text '5f4dcc3b5aa765d61d8327deb882cf99'
 
       nth --file hash
 
       nth --text '5f4dcc3b5aa765d61d8327deb882cf99' --greppable
 
       Note: Use single quotes ' as inverted commas " do not work well on
       Linux.
 
 Options:
   -t, --text TEXT      Check one hash, use single quotes ' as inverted commas
                        " messes up on Linux.
   -f, --file FILENAME  Checks every hash in a newline separated file.
   -g, --greppable      Are you going to grep this output? Prints in JSON
                        format.
   -b64, --base64       Decodes hashes in Base64 before identification. For
                        files with mixed Base64 & non-encoded it attempts
                        base64 first and then falls back to normal hash
                        identification per hash.
   -a, --accessible     Turn on accessible mode, does not print ASCII art. Also
                        does not print very large blocks of text, as this can
                        cause some pain with screenreaders. This reduces the
                        information you get. If you want the least likely
                        feature but no banner, use --no-banner.
   -e, --extreme        Searches for hashes within a string. This mode will get
                        5d41402abc4b2a76b9719d911017c592 from
                        ####5d41402abc4b2a76b9719d911017c592###
   --no-banner          Removes banner from startup.
   --no-john            Don't print John The Ripper Information.
   --no-hashcat         Don't print Hashcat Information.
   -v, --verbose        Turn on debugging logs. -vvv for maximum logs.
   --help               Show this message and exit.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
