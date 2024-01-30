---
Title: pdfid
Homepage: https://blog.didierstevens.com/programs/pdf-tools/
Repository: https://gitlab.com/kalilinux/packages/pdfid
Architectures: all
Version: 0.2.8-0kali1
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-forensics kali-tools-respond 
Icon: images/pdfid-logo.svg
PackagesInfo: |
 ### pdfid
 
  This tool is not a PDF parser, but it will scan a file to
  look for certain PDF keywords, allowing you to identify PDF
  documents that contain (for example) JavaScript or execute
  an action when opened. PDFiD will also handle name
  obfuscation.
 
 **Installed size:** `104 KB`  
 **How to install:** `sudo apt install pdfid`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-simplejson
 {{< /spoiler >}}
 
 ##### pdfid
 
 
 ```
 root@kali:~# pdfid -h
 Usage: pdfid [options] [pdf-file|zip-file|url|@file] ...
 Tool to test a PDF file
 
 Arguments:
 pdf-file and zip-file can be a single file, several files, and/or @file
 @file: run PDFiD on each file listed in the text file specified
 wildcards are supported
 
 Source code put in the public domain by Didier Stevens, no Copyright
 Use at your own risk
 https://DidierStevens.com
 
 Options:
   --version             show program's version number and exit
   -h, --help            show this help message and exit
   -s, --scan            scan the given directory
   -a, --all             display all the names
   -e, --extra           display extra data, like dates
   -f, --force           force the scan of the file, even without proper %PDF
                         header
   -d, --disarm          disable JavaScript and auto launch
   -p PLUGINS, --plugins=PLUGINS
                         plugins to load (separate plugins with a comma , ;
                         @file supported)
   -c, --csv             output csv data when using plugins
   -m MINIMUMSCORE, --minimumscore=MINIMUMSCORE
                         minimum score for plugin results output
   -v, --verbose         verbose (will also raise catched exceptions)
   -S SELECT, --select=SELECT
                         selection expression
   -n, --nozero          supress output for counts equal to zero
   -o OUTPUT, --output=OUTPUT
                         output to log file
   --pluginoptions=PLUGINOPTIONS
                         options for the plugin
   -l, --literalfilenames
                         take filenames literally, no wildcard matching
   --recursedir          Recurse directories (wildcards and here files (@...)
                         allowed)
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## pdfid Usage Example

```
root@kali:~# pdfid /usr/share/doc/texmf/fonts/lm/lm-info.pdf
PDFiD 0.0.12 /usr/share/doc/texmf/fonts/lm/lm-info.pdf
 PDF Header: %PDF-1.4
 obj                  526
 endobj               526
 stream               151
 endstream            151
 xref                   1
 trailer                1
 startxref              1
 /Page                 26
 /Encrypt               0
 /ObjStm                0
 /JS                    0
 /JavaScript            0
 /AA                    0
 /OpenAction            0
 /AcroForm              0
 /JBIG2Decode           0
 /RichMedia             0
 /Launch                0
 /EmbeddedFile          0
 /Colors > 2^24         0
 ```
