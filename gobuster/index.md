---
Title: gobuster
Homepage: https://github.com/OJ/gobuster
Repository: https://gitlab.com/kalilinux/packages/gobuster
Architectures: any
Version: 3.6.0-0kali1
Metapackages: kali-linux-everything kali-linux-large 
Icon: images/gobuster-logo.svg
PackagesInfo: |
 ### gobuster
 
  Gobuster is a tool used to brute-force URIs including directories and
  files as well as DNS subdomains.
 
 **Installed size:** `7.71 MB`  
 **How to install:** `sudo apt install gobuster`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### gobuster
 
 
 ```
 root@kali:~# gobuster -h
 Usage:
   gobuster [command]
 
 Available Commands:
   completion  Generate the autocompletion script for the specified shell
   dir         Uses directory/file enumeration mode
   dns         Uses DNS subdomain enumeration mode
   fuzz        Uses fuzzing mode. Replaces the keyword FUZZ in the URL, Headers and the request body
   gcs         Uses gcs bucket enumeration mode
   help        Help about any command
   s3          Uses aws bucket enumeration mode
   tftp        Uses TFTP enumeration mode
   version     shows the current version
   vhost       Uses VHOST enumeration mode (you most probably want to use the IP address as the URL parameter)
 
 Flags:
       --debug                 Enable debug output
       --delay duration        Time each thread waits between requests (e.g. 1500ms)
   -h, --help                  help for gobuster
       --no-color              Disable color output
       --no-error              Don't display errors
   -z, --no-progress           Don't display progress
   -o, --output string         Output file to write results to (defaults to stdout)
   -p, --pattern string        File containing replacement patterns
   -q, --quiet                 Don't print the banner and other noise
   -t, --threads int           Number of concurrent threads (default 10)
   -v, --verbose               Verbose output (errors)
   -w, --wordlist string       Path to the wordlist. Set to - to use STDIN.
       --wordlist-offset int   Resume from a given position in the wordlist (defaults to 0)
 
 Use "gobuster [command] --help" for more information about a command.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## Video

<script type="text/javascript" src="https://asciinema.org/a/102166.js" id="asciicast-102166" async></script>

## gobuster Usage Examples

Scan a website (`-u http://192.168.0.155/`) for directories using a wordlist (`-w /usr/share/wordlists/dirb/common.txt`) and print the full URLs of discovered paths (`-e`):

```
root@kali:~# gobuster -e -u http://192.168.0.155/ -w /usr/share/wordlists/dirb/common.txt

Gobuster v1.2                OJ Reeves (@TheColonial)
=====================================================
[+] Mode         : dir
[+] Url/Domain   : http://192.168.0.155/
[+] Threads      : 10
[+] Wordlist     : /usr/share/wordlists/dirb/common.txt
[+] Status codes : 301,302,307,200,204
[+] Expanded     : true
=====================================================
http://192.168.0.155/blog (Status: 301)
http://192.168.0.155/index.html (Status: 200)
http://192.168.0.155/index (Status: 200)
http://192.168.0.155/photo (Status: 301)
http://192.168.0.155/wordpress (Status: 301)
=====================================================
```
