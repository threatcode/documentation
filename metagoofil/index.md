---
Title: metagoofil
Homepage: https://github.com/opsdisk/metagoofil
Repository: https://gitlab.com/kalilinux/packages/metagoofil
Architectures: all
Version: 1:1.2.0+git20221009-0kali1
Metapackages: kali-linux-everything kali-tools-information-gathering kali-tools-reporting 
Icon: images/metagoofil-logo.svg
PackagesInfo: |
 ### metagoofil
 
  Metagoofil is an information gathering tool designed for extracting metadata of
  public documents (pdf,doc,xls,ppt,docx,pptx,xlsx) belonging to a target
  company.
   
  Metagoofil will perform a search in Google to identify and download the
  documents to local disk.
  Metagoofil does no longer extract the metadata. See
  /usr/share/doc/metagoofil/README.md.gz.
 
 **Installed size:** `126 KB`  
 **How to install:** `sudo apt install metagoofil`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-googlesearch
 * python3-requests
 {{< /spoiler >}}
 
 ##### metagoofil
 
 
 ```
 root@kali:~# metagoofil -h
 usage: metagoofil.py [-h] -d DOMAIN [-e DELAY] [-f [SAVE_FILE]]
                      [-i URL_TIMEOUT] [-l SEARCH_MAX] [-n DOWNLOAD_FILE_LIMIT]
                      [-o SAVE_DIRECTORY] [-r NUMBER_OF_THREADS] -t FILE_TYPES
                      [-u [USER_AGENT]] [-w]
 
 Metagoofil v1.2.0 - Search Google and download specific file types.
 
 options:
   -h, --help            show this help message and exit
   -d DOMAIN             Domain to search.
   -e DELAY              Delay (in seconds) between searches. If it's too small
                         Google may block your IP, too big and your search may
                         take a while. Default: 30.0
   -f [SAVE_FILE]        Save the html links to a file.
                         no -f = Do not save links
                         -f = Save links to html_links_<TIMESTAMP>.txt
                         -f SAVE_FILE = Save links to SAVE_FILE
   -i URL_TIMEOUT        Number of seconds to wait before timeout for
                         unreachable/stale pages. Default: 15
   -l SEARCH_MAX         Maximum results to search. Default: 100
   -n DOWNLOAD_FILE_LIMIT
                         Maximum number of files to download per filetype.
                         Default: 100
   -o SAVE_DIRECTORY     Directory to save downloaded files. Default is current
                         working directory, "."
   -r NUMBER_OF_THREADS  Number of downloader threads. Default: 8
   -t FILE_TYPES         file_types to download
                         (pdf,doc,xls,ppt,odp,ods,docx,xlsx,pptx). To search
                         all 17,576 three-letter file extensions, type "ALL"
   -u [USER_AGENT]       User-Agent for file retrieval against -d domain.
                         no -u = "Mozilla/5.0 (compatible; Googlebot/2.1; +http://www.google.com/bot.html)"
                         -u = Randomize User-Agent
                         -u "My custom user agent 2.0" = Your customized User-Agent
   -w                    Download the files, instead of just viewing search
                         results.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## metagoofil Usage Example

Scan for documents from a domain (`-d kali.org)` that are PDF files (`-t pdf`), searching 100 results (`-l 100`), download 25 files (`-n 25`), saving the downloads to a directory (`-o kalipdf`), and saving the output to a file (`-f kalipdf.html`):

```
root@kali:~# metagoofil -d kali.org -t pdf -l 100 -n 25 -o kalipdf -f kalipdf.html

******************************************************
*     /\/\   ___| |_ __ _  __ _  ___   ___  / _(_) | *
*    /    \ / _ \ __/ _` |/ _` |/ _ \ / _ \| |_| | | *
*   / /\/\ \  __/ || (_| | (_| | (_) | (_) |  _| | | *
*   \/    \/\___|\__\__,_|\__, |\___/ \___/|_| |_|_| *
*                         |___/                      *
* Metagoofil Ver 2.2                                 *
* Christian Martorella                               *
* Edge-Security.com                                  *
* cmartorella_at_edge-security.com                   *
******************************************************
['pdf']

[-] Starting online search...

[-] Searching for pdf files, with a limit of 100
        Searching 100 results...
Results: 21 files found
Starting to download 25 of them:
```
