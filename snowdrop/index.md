---
Title: snowdrop
Homepage: http://lcamtuf.coredump.cx/
Repository: https://salsa.debian.org/pkg-security-team/snowdrop/tree/debian/master
Architectures: any
Version: 0.02b-14
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### snowdrop
 
  Snowdrop provides reliable, difficult to remove steganographic watermarking of
  text documents (internal memos, draft research papers, advisories and other
  writing) and C sources (limited distribution software, licensed software,
  or freely available code) so that:
   (1) leaks can be identified if the data goes public.
   (2) original source can be determined and demonstrated if part of the
       document is claimed by somebody else, copied without permission, etc.
  Snowdrop uses redundant steganography using four different logical
  channels, and should be proof to many modifications, including reformatting,
  spell checking and so on.
   
  This package is useful in forensic investigations and security actions. It
  provides three commands: sd-eng, sd-engf and sd-c. sd-eng and sd-engf provide
  watermarking for draft-quality and fine-quality English language text
  documents, respectively, whereas sd-c provides experimental C source code
  watermarking.
   
  Warning: Snowdrop is currently in beta, and may produce bad or corrupted
  results, especially when run on C source code.
 
 **Installed size:** `187 KB`  
 **How to install:** `sudo apt install snowdrop`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libgnutls-openssl27 
 {{< /spoiler >}}
 
 ##### sd-c
 
 Text watermarking and watermark recovery
 
 ```
 root@kali:~# sd-c -h
 snowdrop 0.02b: text watermarking / watermark recovery by lcamtuf@coredump.cx
 
 [*] Weak 32-bit watermarking used (use -6 to change it).
 Usage: sd-c [ -6 ] -e origfile newfile
        sd-c [ -6 ] -l
        sd-c [ -6 ] -i origfile newfile "Recipient" [ "Comment" ] 
 
 First method of calling the program (with -e option) enables watermark
 extraction mode. In this mode, file passed as a first parameter must be
 the original document used to generate second file (or its portions).
 
 Second method (-l) simply lists the contents of the watermark database
 for the module you're now running.
 
 Third method (-i) enables watermark injection mode. File 'origfile' is
 modified and saved as 'newfile'. Mandatory parameter is the recipient
 identifier. Optional comment can be added for your reference.
 
 Additional parameter -6 enables strong, 64-bit watermarking that is suitable
 for providing public documentation of watermarked document abuse.
 
 
 ```
 
 - - -
 
 ##### sd-eng
 
 Text watermarking and watermark recovery
 
 ```
 root@kali:~# sd-eng -h
 snowdrop 0.02b: text watermarking / watermark recovery by lcamtuf@coredump.cx
 
 [*] Weak 32-bit watermarking used (use -6 to change it).
 Usage: sd-eng [ -6 ] -e origfile newfile
        sd-eng [ -6 ] -l
        sd-eng [ -6 ] -i origfile newfile "Recipient" [ "Comment" ] 
 
 First method of calling the program (with -e option) enables watermark
 extraction mode. In this mode, file passed as a first parameter must be
 the original document used to generate second file (or its portions).
 
 Second method (-l) simply lists the contents of the watermark database
 for the module you're now running.
 
 Third method (-i) enables watermark injection mode. File 'origfile' is
 modified and saved as 'newfile'. Mandatory parameter is the recipient
 identifier. Optional comment can be added for your reference.
 
 Additional parameter -6 enables strong, 64-bit watermarking that is suitable
 for providing public documentation of watermarked document abuse.
 
 This module supports SD_SYNONYMS environment variable that should
 point to an alternative 'synonyms' file, if necessary. Make sure
 to keep the copy of used alternative file for further reference.
 
 ```
 
 - - -
 
 ##### sd-engf
 
 Text watermarking and watermark recovery
 
 ```
 root@kali:~# sd-engf -h
 snowdrop 0.02b: text watermarking / watermark recovery by lcamtuf@coredump.cx
 
 [*] Weak 32-bit watermarking used (use -6 to change it).
 Usage: sd-engf [ -6 ] -e origfile newfile
        sd-engf [ -6 ] -l
        sd-engf [ -6 ] -i origfile newfile "Recipient" [ "Comment" ] 
 
 First method of calling the program (with -e option) enables watermark
 extraction mode. In this mode, file passed as a first parameter must be
 the original document used to generate second file (or its portions).
 
 Second method (-l) simply lists the contents of the watermark database
 for the module you're now running.
 
 Third method (-i) enables watermark injection mode. File 'origfile' is
 modified and saved as 'newfile'. Mandatory parameter is the recipient
 identifier. Optional comment can be added for your reference.
 
 Additional parameter -6 enables strong, 64-bit watermarking that is suitable
 for providing public documentation of watermarked document abuse.
 
 This module supports SD_SYNONYMS environment variable that should
 point to an alternative 'synonyms' file, if necessary. Make sure
 to keep the copy of used alternative file for further reference.
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
