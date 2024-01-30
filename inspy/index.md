---
Title: inspy
Homepage: https://github.com/gojhonny/InSpy
Repository: https://gitlab.com/kalilinux/packages/inspy
Architectures: all
Version: 3.0.0-0kali4
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### inspy
 
  This package contains a Python based LinkedIn enumeration tool.
   
  You will need an API key from HunterIO.
 
 **Installed size:** `45 KB`  
 **How to install:** `sudo apt install inspy`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-bs4
 * python3-requests
 {{< /spoiler >}}
 
 ##### inspy
 
 
 ```
 root@kali:~# inspy -h
 usage: inspy [-h] [--domain DOMAIN] [--email EMAIL] [--titles [file]]
              [--html file] [--csv file] [--json file] [--xml file]
              company
 
 InSpy - A LinkedIn enumeration tool by Jonathan Broche (@LeapSecurity),
 version 3.0.0
 
 positional arguments:
   company          Company name to use for tasks.
 
 options:
   -h, --help       show this help message and exit
   --domain DOMAIN  Company domain to use for searching.
   --email EMAIL    Email format to create email addresses with. [Accepted
                    Formats: first.last@xyz.com, last.first@xyz.com,
                    firstl@xyz.com, lfirst@xyz.com, flast@xyz.com,
                    lastf@xyz.com, first@xyz.com, last@xyz.com]
   --titles [file]  Discover employees by title and/or department. Titles and
                    departments are imported from a new line delimited file.
                    [Default: title-list-small.txt]
 
 Output Options:
   --html file      Print results in HTML file.
   --csv file       Print results in CSV format.
   --json file      Print results in JSON.
   --xml file       Print results in XML.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## inspy Usage Examples

Search LinkedIn for `google` employees (`–empspy`) with the provided wordlist of job titles (`/usr/share/inspy/wordlists/title-list-large.txt`).

```
root@kali:~# inspy --empspy /usr/share/inspy/wordlists/title-list-large.txt google
```

Search for technologies (`–techspy`) in use at the target company (`cisco`) using the provided list of terms (`/usr/share/inspy/wordlists/tech-list-small.txt`).

```
root@kali:~# inspy --techspy /usr/share/inspy/wordlists/tech-list-small.txt cisco
```
