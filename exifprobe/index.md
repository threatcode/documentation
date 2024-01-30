---
Title: exifprobe
Homepage: https://github.com/hfiguiere/exifprobe
Repository: https://salsa.debian.org/pkg-security-team/exifprobe
Architectures: any
Version: 2.0.1+git20170416.3c2b769-5
Metapackages: kali-linux-everything kali-tools-forensics kali-tools-respond 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### exifprobe
 
  Exifprobe reads image files produced by digital cameras (including
  several so-called "raw" file formats) and reports the structure of
  the files and the auxiliary data and metadata contained within them.
   
  In addition to TIFF, JPEG and EXIF, the program understands several
  formats which may contain "raw" camera data, including MRW, CIFF/CRW,
  JP2/JPEG2000, RAF, and X3F, as well as most TIFF-derived "raw" formats,
  including DNG, ORF, CR2, NEF, K25/KDC/DCR and PEF.
   
  This program is useful in forensics investigations.
 
 **Installed size:** `499 KB`  
 **How to install:** `sudo apt install exifprobe`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### exifgrep
 
 Select and reformat the output of exifprobe
 
 ```
 root@kali:~# exifgrep -h
 Usage: exifgrep [-var|-export] [-num] [-r] [-t] [-n] [-c] [egrep-options] egrep-pattern [NOT egrep-pattern] imagefilename[s]
 ```
 
 - - -
 
 ##### exifprobe
 
 Probe and report structure and metadata content of camera image files
 
 ```
 root@kali:~# exifprobe -h
 Usage:
 exifprobe [options] filenames(s)
 	-h - print this help message
 	-V - print program version and copyright
 
 	-R - Report mode: only tagnames and decimal values, indented, inline
 	-S - Structure mode: everything, offset values not inline (default)
 	-L - List mode: list all tags and values (only); no structure
 	-Z - Zero (turn off) all output flags
 
 	-a - toggle print addresses in hex and decimal
 	-D - toggle print enabled addresses, tag numbers and values in decimal only
 	-X - toggle print enabled addresses, tag numbers and values in hex only
 	-I - toggle indent (after address -> before -> none)
 	-i - toggle "inline" print of IFD values
 	-n - toggle printing of filename at start of each output line
 	-c - toggle use of color to highlight certain sections
 	-u - print all 16 bits of unicode data
 
 	-p[items] - toggle print identifiers for:
 		s - sections
 		g - segments
 		e - IFD entries
 		a - expand known entries in APP0...APPN segents
 		m - print MakerNote scheme detection info
 		M - debug MakerNote scheme detection info
 		l - long tagnames (default in List mode)
 
 	-e[items] - toggle print IFD entry items:
 		t - tagname
 		n - tag number in decimal
 		N - tag number in hex
 		T - entry type
 		v - value in decimal
 		V - value in hex
 		o - file offset to value in decimal
 		O - file offset to value in hex
 		r - relative (unadjusted) offset in decimal
 		R - print "raw" values where expansion of values is needed
 		a - print ascii strings until null, rather than by length
 		A - print ALL elements of multiple-value tags
 
 	-M[len|a] - hex/ascii dump 'len' (or all) bytes of unknown MakerNotes
 	-A[len|a] - hex/ascii dump 'len' (or all) bytes of unknown APPn segments
 	-U[len|a] - hex/ascii dump 'len' (or all) bytes of UNDEFINED data of unknown format
 	-B[len|a] - hex/ascii dump 'len' (or all) bytes of binary images or invalid JPEG data
 	-N[num]   - force noteversion 'num' for MakerNote interpretation
 	-m[name]  - force use of maker 'name' to select MakerNote interpretation routines
 	-l[model] - force use of 'model' to select MakerNote interpretation routines
 
 	-O[offset]       - start processing at 'offset' in file
 	-C[make]+[model] - print makes matching 'make', models matching 'model' (substrings)
 
 	Program: 'exifprobe' version 2.1.0
 	Compiled: no date
 	Copyright (C) 2005 Duane H. Hesser, (C) 2011-2015 Hubert Figuiere
 		(open source; see LICENSE.EXIFPROBE)
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
