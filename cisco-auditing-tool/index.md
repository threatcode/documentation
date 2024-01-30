---
Title: cisco-auditing-tool
Homepage: http://www.scrypt.net/
Repository: https://gitlab.com/kalilinux/packages/cisco-auditing-tool
Architectures: all
Version: 1.0-1kali5
Metapackages: kali-linux-everything kali-linux-large kali-tools-identify kali-tools-passwords kali-tools-vulnerability 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### cisco-auditing-tool
 
  Perl script which scans cisco routers for common vulnerabilities.
 
 **Installed size:** `266 KB`  
 **How to install:** `sudo apt install cisco-auditing-tool`  
 
 {{< spoiler "Dependencies:" >}}
 * perl
 {{< /spoiler >}}
 
 ##### CAT
 
 Concatenate files and print on the standard output
 
 ```
 root@kali:~# CAT --help
 /usr/bin/CAT version [unknown] calling Getopt::Std::getopts (version 1.13 [paranoid]),
 running under Perl version 5.36.0.
 
 Usage: CAT [-OPTIONS [-MORE_OPTIONS]] [--] [PROGRAM_ARG1 ...]
 
 The following single-character options are accepted:
 	With arguments: -h -f -p -w -a -l
 	Boolean (without arguments): -i -q
 
 Options may be merged together.  -- stops processing of options.
 Space is not required between options and their arguments.
   [Now continuing due to backward compatibility and excessive paranoia.
    See 'perldoc Getopt::Std' about $Getopt::Std::STANDARD_HELP_VERSION.]
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## cisco-auditing-tool Usage Example

Scan the host (`-h 192.168.99.230`) on port 23 (`-p 23`), using a password dictionary file (`-a /usr/share/wordlists/nmap.lst`):

```
root@kali:~# CAT -h 192.168.99.230 -p 23 -a /usr/share/wordlists/nmap.lst

Cisco Auditing Tool - g0ne [null0]

Checking Host: 192.168.99.230


Guessing passwords:

Invalid Password: 123456
Invalid Password: 12345
```
