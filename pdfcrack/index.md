---
Title: pdfcrack
Homepage: http://pdfcrack.sf.net
Repository: https://salsa.debian.org/debian/pdfcrack
Architectures: any
Version: 0.20-1
Metapackages: kali-linux-everything kali-tools-passwords 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### pdfcrack
 
  PDFCrack is a simple tool for recovering passwords from pdf-documents.
   
  It should be able to handle all pdfs that uses the standard security handler
  but the pdf-parsing routines are a bit of a quick hack so you might stumble
  across some pdfs where the parser needs to be fixed to handle.
   
  The main PDFCrack features are:
   
    - Supports the standard security handler (revision 2, 3 and 4) on all known
      PDF-versions.
    - Supports cracking both owner and userpasswords.
    - Both wordlists and bruteforcing the password are supported.
    - Simple permutations (currently only trying first character as Upper Case).
    - Save and load a running job.
    - Simple benchmarking.
    - Optimised search for owner-password when user-password is known.
   
  This program can be used in forensics investigations or similar activities,
  to legal password crack.
 
 **Installed size:** `89 KB`  
 **How to install:** `sudo apt install pdfcrack`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### pdfcrack
 
 Password recovery tool for PDF-files
 
 ```
 root@kali:~# pdfcrack -h
 Usage: pdfcrack -f filename [OPTIONS]
 OPTIONS:
 -b, --bench		perform benchmark and exit
 -c, --charset=STRING	Use the characters in STRING as charset
 -w, --wordlist=FILE	Use FILE as source of passwords to try
 -n, --minpw=INTEGER	Skip trying passwords shorter than this
 -m, --maxpw=INTEGER	Stop when reaching this passwordlength
 -l, --loadState=FILE	Continue from the state saved in FILENAME
 -o, --owner		Work with the ownerpassword
 -u, --user		Work with the userpassword (default)
 -p, --password=STRING	Give userpassword to speed up breaking
 			ownerpassword (implies -o)
 -q, --quiet		Run quietly
 -s, --permutate		Try permutating the passwords (currently only
 			supports switching first character to uppercase)
 -v, --version		Print version and exit
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
