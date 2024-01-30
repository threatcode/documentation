---
Title: steghide
Homepage: http://steghide.sourceforge.net/
Repository: https://salsa.debian.org/pkg-security-team/steghide
Architectures: any all
Version: 0.5.1-15
Metapackages: kali-linux-everything kali-tools-crypto-stego 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### steghide
 
  Steghide is steganography program which hides bits of a data file
  in some of the least significant bits of another file in such a way
  that the existence of the data file is not visible and cannot be proven.
   
  Steghide is designed to be portable and configurable and features hiding
  data in bmp, jpeg, wav and au files, blowfish encryption, MD5 hashing of
  passphrases to blowfish keys, and pseudo-random distribution of hidden bits
  in the container data.
   
  Steghide is useful in digital forensics investigations.
 
 **Installed size:** `477 KB`  
 **How to install:** `sudo apt install steghide`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libgcc-s1 
 * libjpeg62-turbo 
 * libmcrypt4
 * libmhash2 
 * libstdc++6 
 * zlib1g 
 {{< /spoiler >}}
 
 ##### steghide
 
 A steganography program
 
 ```
 root@kali:~# steghide --help
 steghide version 0.5.1
 
 the first argument must be one of the following:
  embed, --embed          embed data
  extract, --extract      extract data
  info, --info            display information about a cover- or stego-file
    info <filename>       display information about <filename>
  encinfo, --encinfo      display a list of supported encryption algorithms
  version, --version      display version information
  license, --license      display steghide's license
  help, --help            display this usage information
 
 embedding options:
  -ef, --embedfile        select file to be embedded
    -ef <filename>        embed the file <filename>
  -cf, --coverfile        select cover-file
    -cf <filename>        embed into the file <filename>
  -p, --passphrase        specify passphrase
    -p <passphrase>       use <passphrase> to embed data
  -sf, --stegofile        select stego file
    -sf <filename>        write result to <filename> instead of cover-file
  -e, --encryption        select encryption parameters
    -e <a>[<m>]|<m>[<a>]  specify an encryption algorithm and/or mode
    -e none               do not encrypt data before embedding
  -z, --compress          compress data before embedding (default)
    -z <l>                 using level <l> (1 best speed...9 best compression)
  -Z, --dontcompress      do not compress data before embedding
  -K, --nochecksum        do not embed crc32 checksum of embedded data
  -N, --dontembedname     do not embed the name of the original file
  -f, --force             overwrite existing files
  -q, --quiet             suppress information messages
  -v, --verbose           display detailed information
 
 extracting options:
  -sf, --stegofile        select stego file
    -sf <filename>        extract data from <filename>
  -p, --passphrase        specify passphrase
    -p <passphrase>       use <passphrase> to extract data
  -xf, --extractfile      select file name for extracted data
    -xf <filename>        write the extracted data to <filename>
  -f, --force             overwrite existing files
  -q, --quiet             suppress information messages
  -v, --verbose           display detailed information
 
 options for the info command:
  -p, --passphrase        specify passphrase
    -p <passphrase>       use <passphrase> to get info about embedded data
 
 To embed emb.txt in cvr.jpg: steghide embed -cf cvr.jpg -ef emb.txt
 To extract embedded data from stg.jpg: steghide extract -sf stg.jpg
 ```
 
 - - -
 
 ### steghide-doc
 
  Steghide is steganography program which hides bits of a data file
  in some of the least significant bits of another file in such a way
  that the existence of the data file is not visible and cannot be proven.
   
  Steghide is designed to be portable and configurable and features hiding
  data in bmp, jpeg, wav and au files, blowfish encryption, MD5 hashing of
  passphrases to blowfish keys, and pseudo-random distribution of hidden bits
  in the container data.
   
  These packages contains the common documentation files.
 
 **Installed size:** `7.45 MB`  
 **How to install:** `sudo apt install steghide-doc`  
 
 {{< spoiler "Dependencies:" >}}
 * libjs-jquery
 {{< /spoiler >}}
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
