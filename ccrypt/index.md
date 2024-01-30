---
Title: ccrypt
Homepage: http://ccrypt.sourceforge.net/
Repository: https://salsa.debian.org/pkg-security-team/ccrypt
Architectures: any all
Version: 1.11-2
Metapackages: kali-linux-everything kali-tools-crypto-stego 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### ccrypt
 
  ccrypt is a utility for encrypting and decrypting files and streams. It was
  designed as a replacement for the standard unix crypt utility, which is
  notorious for using a very weak encryption algorithm. ccrypt is based on the
  Rijndael cipher, which is the U.S. government's chosen candidate for the
  Advanced Encryption Standard (AES, see http://www.nist.gov/aes). This cipher is
  believed to provide very strong security.
 
 **Installed size:** `181 KB`  
 **How to install:** `sudo apt install ccrypt`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libcrypt1 
 {{< /spoiler >}}
 
 ##### ccat
 
 Encrypt and decrypt files and streams
 
 ```
 root@kali:~# ccat -h
 ccrypt 1.11. Secure encryption and decryption of files and streams.
 
 Usage: ccrypt [mode] [options] [file...]
        ccencrypt [options] [file...]
        ccdecrypt [options] [file...]
        ccat [options] file...
 
 Modes:
     -e, --encrypt         encrypt
     -d, --decrypt         decrypt
     -c, --cat             cat; decrypt files to stdout
     -x, --keychange       change key
     -u, --unixcrypt       decrypt old unix crypt files
 
 Options:
     -h, --help            print this help message and exit
     -V, --version         print version info and exit
     -L, --license         print license info and exit
     -v, --verbose         print progress information to stderr
     -q, --quiet           run quietly; suppress warnings
     -f, --force           overwrite existing files without asking
     -m, --mismatch        allow decryption with non-matching key
     -E, --envvar var      read keyword from environment variable (unsafe)
     -K, --key key         give keyword on command line (unsafe)
     -k, --keyfile file    read keyword(s) as first line(s) from file
     -P, --prompt prompt   use this prompt instead of default
     -S, --suffix .suf     use suffix .suf instead of default .cpt
     -s, --strictsuffix    refuse to encrypt files which already have suffix
     -F, --envvar2 var     as -E for second keyword (for keychange mode)
     -H, --key2 key        as -K for second keyword (for keychange mode)
     -Q, --prompt2 prompt  as -P for second keyword (for keychange mode)
     -t, --timid           prompt twice for encryption keys (default)
     -b, --brave           prompt only once for encryption keys
     -y, --keyref file     encryption key must match this encrypted file
     -r, --recursive       recurse through directories
     -R, --rec-symlinks    follow symbolic links as subdirectories
     -l, --symlinks        dereference symbolic links
     -T, --tmpfiles        use temporary files instead of overwriting (unsafe)
     --                    end of options, filenames follow
 ```
 
 - - -
 
 ##### ccdecrypt
 
 Encrypt and decrypt files and streams
 
 ```
 root@kali:~# ccdecrypt -h
 ccrypt 1.11. Secure encryption and decryption of files and streams.
 
 Usage: ccrypt [mode] [options] [file...]
        ccencrypt [options] [file...]
        ccdecrypt [options] [file...]
        ccat [options] file...
 
 Modes:
     -e, --encrypt         encrypt
     -d, --decrypt         decrypt
     -c, --cat             cat; decrypt files to stdout
     -x, --keychange       change key
     -u, --unixcrypt       decrypt old unix crypt files
 
 Options:
     -h, --help            print this help message and exit
     -V, --version         print version info and exit
     -L, --license         print license info and exit
     -v, --verbose         print progress information to stderr
     -q, --quiet           run quietly; suppress warnings
     -f, --force           overwrite existing files without asking
     -m, --mismatch        allow decryption with non-matching key
     -E, --envvar var      read keyword from environment variable (unsafe)
     -K, --key key         give keyword on command line (unsafe)
     -k, --keyfile file    read keyword(s) as first line(s) from file
     -P, --prompt prompt   use this prompt instead of default
     -S, --suffix .suf     use suffix .suf instead of default .cpt
     -s, --strictsuffix    refuse to encrypt files which already have suffix
     -F, --envvar2 var     as -E for second keyword (for keychange mode)
     -H, --key2 key        as -K for second keyword (for keychange mode)
     -Q, --prompt2 prompt  as -P for second keyword (for keychange mode)
     -t, --timid           prompt twice for encryption keys (default)
     -b, --brave           prompt only once for encryption keys
     -y, --keyref file     encryption key must match this encrypted file
     -r, --recursive       recurse through directories
     -R, --rec-symlinks    follow symbolic links as subdirectories
     -l, --symlinks        dereference symbolic links
     -T, --tmpfiles        use temporary files instead of overwriting (unsafe)
     --                    end of options, filenames follow
 ```
 
 - - -
 
 ##### ccencrypt
 
 Encrypt and decrypt files and streams
 
 ```
 root@kali:~# ccencrypt -h
 ccrypt 1.11. Secure encryption and decryption of files and streams.
 
 Usage: ccrypt [mode] [options] [file...]
        ccencrypt [options] [file...]
        ccdecrypt [options] [file...]
        ccat [options] file...
 
 Modes:
     -e, --encrypt         encrypt
     -d, --decrypt         decrypt
     -c, --cat             cat; decrypt files to stdout
     -x, --keychange       change key
     -u, --unixcrypt       decrypt old unix crypt files
 
 Options:
     -h, --help            print this help message and exit
     -V, --version         print version info and exit
     -L, --license         print license info and exit
     -v, --verbose         print progress information to stderr
     -q, --quiet           run quietly; suppress warnings
     -f, --force           overwrite existing files without asking
     -m, --mismatch        allow decryption with non-matching key
     -E, --envvar var      read keyword from environment variable (unsafe)
     -K, --key key         give keyword on command line (unsafe)
     -k, --keyfile file    read keyword(s) as first line(s) from file
     -P, --prompt prompt   use this prompt instead of default
     -S, --suffix .suf     use suffix .suf instead of default .cpt
     -s, --strictsuffix    refuse to encrypt files which already have suffix
     -F, --envvar2 var     as -E for second keyword (for keychange mode)
     -H, --key2 key        as -K for second keyword (for keychange mode)
     -Q, --prompt2 prompt  as -P for second keyword (for keychange mode)
     -t, --timid           prompt twice for encryption keys (default)
     -b, --brave           prompt only once for encryption keys
     -y, --keyref file     encryption key must match this encrypted file
     -r, --recursive       recurse through directories
     -R, --rec-symlinks    follow symbolic links as subdirectories
     -l, --symlinks        dereference symbolic links
     -T, --tmpfiles        use temporary files instead of overwriting (unsafe)
     --                    end of options, filenames follow
 ```
 
 - - -
 
 ##### ccguess
 
 Search for ccrypt encryption keys
 
 ```
 root@kali:~# ccguess -h
 ccguess 1.11. Search for ccrypt encryption keys.
 
 Usage: ccguess [options] file...
 Options:
     -h, --help              print this help message and exit
     -V, --version           print version info and exit
     -L, --license           print license info and exit
     -K, --key <key>         specify approximate key
     -d, --depth             try up to this many changes to key (default: 5)
     -c, --continue          keep trying more keys after first match
     -n, --non-printable     allow non-printable characters in keys
     -t, --chartable <chars> characters to use in passwords (default: printable)
 Arguments:
     file...               files to read encrypted data from, or '-' for stdin
 ```
 
 - - -
 
 ##### ccrypt
 
 Encrypt and decrypt files and streams
 
 ```
 root@kali:~# ccrypt -h
 ccrypt 1.11. Secure encryption and decryption of files and streams.
 
 Usage: ccrypt [mode] [options] [file...]
        ccencrypt [options] [file...]
        ccdecrypt [options] [file...]
        ccat [options] file...
 
 Modes:
     -e, --encrypt         encrypt
     -d, --decrypt         decrypt
     -c, --cat             cat; decrypt files to stdout
     -x, --keychange       change key
     -u, --unixcrypt       decrypt old unix crypt files
 
 Options:
     -h, --help            print this help message and exit
     -V, --version         print version info and exit
     -L, --license         print license info and exit
     -v, --verbose         print progress information to stderr
     -q, --quiet           run quietly; suppress warnings
     -f, --force           overwrite existing files without asking
     -m, --mismatch        allow decryption with non-matching key
     -E, --envvar var      read keyword from environment variable (unsafe)
     -K, --key key         give keyword on command line (unsafe)
     -k, --keyfile file    read keyword(s) as first line(s) from file
     -P, --prompt prompt   use this prompt instead of default
     -S, --suffix .suf     use suffix .suf instead of default .cpt
     -s, --strictsuffix    refuse to encrypt files which already have suffix
     -F, --envvar2 var     as -E for second keyword (for keychange mode)
     -H, --key2 key        as -K for second keyword (for keychange mode)
     -Q, --prompt2 prompt  as -P for second keyword (for keychange mode)
     -t, --timid           prompt twice for encryption keys (default)
     -b, --brave           prompt only once for encryption keys
     -y, --keyref file     encryption key must match this encrypted file
     -r, --recursive       recurse through directories
     -R, --rec-symlinks    follow symbolic links as subdirectories
     -l, --symlinks        dereference symbolic links
     -T, --tmpfiles        use temporary files instead of overwriting (unsafe)
     --                    end of options, filenames follow
 ```
 
 - - -
 
 ### elpa-ps-ccrypt
 
  elpa-ps-ccrypt provides low-level support for reading, writing, and
  loading files encrypted with ccrypt. It hooks into the low-level file I/O
  functions (including write-region and insert-file-contents) so that they
  automatically encrypt or decrypt a file if the file appears to need it
  (based on the extension of the file name). Packages like Rmail, VM, GNUS,
  and Info should be able to work with encrypted files without modification.
 
 **Installed size:** `76 KB`  
 **How to install:** `sudo apt install elpa-ps-ccrypt`  
 
 {{< spoiler "Dependencies:" >}}
 * ccrypt 
 * dh-elpa-helper
 * emacsen-common
 {{< /spoiler >}}
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
