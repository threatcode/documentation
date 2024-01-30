---
Title: undbx
Homepage: https://github.com/ZungBang/undbx
Repository: https://salsa.debian.org/pkg-security-team/undbx
Architectures: any
Version: 0.21-4
Metapackages: kali-linux-everything kali-tools-forensics kali-tools-recover kali-tools-respond 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### undbx
 
  UnDBX is a tool to extract, recover and undelete e-mail messages from MS
  Outlook Express .dbx files (or similar e-mail programs in MS Windows).
  Corrupted .dbx files can be parsed to try to recover messages from it. It
  can also try to undelete messages, not only from Deleted Items but also
  from fragments of deleted messages that were not overwritten.
   
  UnDBX is useful in forensics investigations.
 
 **Installed size:** `61 KB`  
 **How to install:** `sudo apt install undbx`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### undbx
 
 A tool to extract e-mails from Outlook Express .dbx files.
 
 ```
 root@kali:~# undbx -h
 UnDBX v0.21 (Dec 26 2022)
 Usage: undbx [<OPTION>] <DBX-FOLDER | DBX-FILE> [<OUTPUT-FOLDER>]
 
 Options:
 	-h, --help        	 show this message
 	-V, --version     	 show only version string
 	-v, --verbosity N 	 set verbosity level to N [default: 3]
 	-r, --recover     	 enable recovery mode
 	-s, --safe-mode   	 generate locale-safe file names
 	-D, --delete      	 delete messages from the destination directory
 	                  	 that were deleted from the dbx file
 	                  	 [default behavior is to move such messages to
 	                  	  a sub-directory named 'deleted']
 	-i, --ignore0     	 ignore empty messages
 	-d, --debug       	 output debug messages
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
