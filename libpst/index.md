---
Title: libpst
Homepage: https://www.five-ten-sg.com/libpst/
Repository: https://salsa.debian.org/debian/libpst
Architectures: any
Version: 0.6.76-1
Metapackages: kali-linux-everything kali-linux-large kali-tools-forensics kali-tools-respond 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### libpst-dev
 
  Library for accessing data from Microsoft Outlook PST files.
   
  This package include the files needed for developing with libpst,
  including the headers, static library and documentation.
 
 **Installed size:** `2.58 MB`  
 **How to install:** `sudo apt install libpst-dev`  
 
 {{< spoiler "Dependencies:" >}}
 * libpst4 
 {{< /spoiler >}}
 
 
 - - -
 
 ### libpst4
 
  Library for accessing data from Microsoft Outlook PST files.
   
  This package include the libpst shared library used by applications.
 
 **Installed size:** `220 KB`  
 **How to install:** `sudo apt install libpst4`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * zlib1g 
 {{< /spoiler >}}
 
 
 - - -
 
 ### pst-utils
 
  This package contains tools based on libpst to read data from Microsoft
  Outlook PST files.
    * readpst - export data from PST files to a variety of formats, including
      mbox, MH and KMail. Other packages like mb2md are available for subsequent
      conversions to Maildir and other formats.
    * lspst - list data in PST files.
    * pst2ldif - extract contacts from a PST file and prepare them for input in
      LDAP
    * pst2dii - export data from PST files to Summation dii load file format
 
 **Installed size:** `218 KB`  
 **How to install:** `sudo apt install pst-utils`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libgcc-s1 
 * libgd3 
 * libglib2.0-0 
 * libgsf-1-114 
 * libpst4 
 * libstdc++6 
 {{< /spoiler >}}
 
 ##### lspst
 
 List PST (MS Outlook Personal Folders) file data
 
 ```
 root@kali:~# lspst -h
 lspst / LibPST v0.6.76
 Little Endian implementation being used.
 Usage: lspst [OPTIONS] {PST FILENAME}
 OPTIONS:
 	-d <filename> 	- Debug to file. This is a binary log. Use readlog to print it
 	-l	- Print the date, CC and BCC fields of emails too (by default only the From and Subject)
 	-f <date_format> 	- Select the date format in ctime format (by default "%F %T")
 	-h	- Help. This screen
 	-V	- Version. Display program version
 ```
 
 - - -
 
 ##### nick2ldif
 
 
 
 - - -
 
 ##### pst2dii
 
 Extract email messages from an MS Outlook .pst file in DII load format
 
 ```
 root@kali:~# pst2dii -h
 pst2dii v0.6.76
 Little Endian implementation being used.
 Usage: pst2dii -f ttf-font-file [OPTIONS] {PST FILENAME}
 	-f ttf-font-file  	- Set the font file
 OPTIONS:
 	-B bates-prefix   	- Set the bates prefix string
 	-O dii-output-file	- Set the dii load file output filename
 	-V                	- Version. Display program version
 	-b bates-number   	- Set the starting bates sequence number
 	-c bates-color    	- Specify the color of the bates stamps as 6 digit hex
 	-d filename       	- Debug to file.
 	-h                	- Help. This screen
 	-o dirname        	- Output directory to write files to.
 ```
 
 - - -
 
 ##### pst2ldif
 
 Extract contacts from an MS Outlook .pst file in .ldif format
 
 ```
 root@kali:~# pst2ldif -h
 pst2ldif v0.6.76
 Little Endian implementation being used.
 Usage: pst2ldif [OPTIONS] {PST FILENAME}
 OPTIONS:
 	-V	- Version. Display program version
 	-b ldapbase	- set the LDAP base value
 	-c class	- set the class of the LDAP objects (may contain more than one)
 	-d <filename>	- Debug to file.
 	-h	- Help. This screen
 	-l line	- extra line to insert in the LDIF file for each contact
 	-o	- use old schema, default is new schema
 ```
 
 - - -
 
 ##### readpst
 
 Convert PST (MS Outlook Personal Folders) files to mbox and other formats
 
 ```
 root@kali:~# readpst -h
 ReadPST / LibPST v0.6.76
 Little Endian implementation being used.
 Usage: readpst [OPTIONS] {PST FILENAME}
 OPTIONS:
 	-V	- Version. Display program version
 	-C charset	- character set for items with an unspecified character set
 	-D	- Include deleted items in output
 	-L <level> 	- Set debug level; 1=debug,2=info,3=warn.
 	-M	- Write emails in the MH (rfc822) format
 	-S	- Separate. Write emails in the separate format
 	-a <attachment-extension-list>	- Discard any attachment without an extension on the list
 	-b	- Don't save RTF-Body attachments
 	-c[v|l]	- Set the Contact output mode. -cv = VCard, -cl = EMail list
 	-d <filename> 	- Debug to file.
 	-e	- As with -M, but include extensions on output files
 	-h	- Help. This screen
 	-j <integer>	- Number of parallel jobs to run
 	-k	- KMail. Output in kmail format
 	-m	- As with -e, but write .msg files also
 	-o <dirname>	- Output directory to write files to. CWD is changed *after* opening pst file
 	-q	- Quiet. Only print error messages
 	-r	- Recursive. Output in a recursive format
 	-t[eajc]	- Set the output type list. e = email, a = attachment, j = journal, c = contact
 	-u	- Thunderbird mode. Write two extra .size and .type files
 	-w	- Overwrite any output mbox files
 	-8	- Output bodies in UTF-8, rather than original encoding, if UTF-8 version is available
 
 Only one of -M -S -e -k -m -r should be specified
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
