---
Title: dnswalk
Homepage: https://github.com/davebarr/dnswalk
Repository: https://salsa.debian.org/debian/dnswalk
Architectures: all
Version: 2.0.2.dfsg.1-3
Metapackages: kali-linux-everything kali-linux-large kali-tools-information-gathering 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### dnswalk
 
  dnswalk is a DNS debugger.  It performs zone transfers of specified
  domains, and checks the database in numerous ways for internal
  consistency, as well as accuracy.
 
 **Installed size:** `46 KB`  
 **How to install:** `sudo apt install dnswalk`  
 
 {{< spoiler "Dependencies:" >}}
 * libnet-dns-perl
 * perl
 {{< /spoiler >}}
 
 ##### dnswalk
 
 A DNS database debugger
 
 ```
 root@kali:~# dnswalk --help
 /usr/bin/dnswalk version [unknown] calling Getopt::Std::getopts (version 1.13 [paranoid]),
 running under Perl version 5.36.0.
 
 Usage: dnswalk [-OPTIONS [-MORE_OPTIONS]] [--] [PROGRAM_ARG1 ...]
 
 The following single-character options are accepted:
 	With arguments: -D
 	Boolean (without arguments): -r -f -i -a -d -m -F -l
 
 Options may be merged together.  -- stops processing of options.
 Space is not required between options and their arguments.
   [Now continuing due to backward compatibility and excessive paranoia.
    See 'perldoc Getopt::Std' about $Getopt::Std::STANDARD_HELP_VERSION.]
 Usage: dnswalk domain
 domain MUST end with a '.'
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## dnswalk Usage Example

Attempt to get DNS zone information from the target domain (`example.com.`):

```
root@kali:~# dnswalk example.com.
Checking example.com.
```

```
root@kali:~# dnswalk -r -d example.com.
Checking example.com.
```
