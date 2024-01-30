---
Title: enumiax
Homepage: https://enumiax.sourceforge.net/
Repository: https://gitlab.com/kalilinux/packages/enumiax
Architectures: any
Version: 0.4a-1kali4
Metapackages: kali-linux-everything kali-linux-large kali-tools-voip kali-tools-vulnerability 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### enumiax
 
  enumIAX is an Inter Asterisk Exchange protocol username
  brute-force enumerator.
  enumIAX may operate in two distinct modes; Sequential
  Username Guessing or Dictionary Attack.
 
 **Installed size:** `35 KB`  
 **How to install:** `sudo apt install enumiax`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### enumiax
 
 
 ```
 root@kali:~# enumiax --help
 enumiax: invalid option -- '-'
 enumIAX 0.4a
 Dustin D. Trammell <dtrammell@tippingpoint.com>
 
 Usage: enumiax [options] target
   options:
     -d <dict>   Dictionary attack using <dict> file
     -i <count>  Interval for auto-save (# of operations, default 1000)
     -m #        Minimum username length (in characters)
     -M #        Maximum username length (in characters)
     -r #        Rate-limit calls (in microseconds)
     -s <file>   Read session state from state file
     -v          Increase verbosity (repeat for additional verbosity)
     -V          Print version information and exit
     -h          Print help/usage information and exit
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## enumiax Usage Example

Run a dictionary attack (`-d /usr/share/wordlists/metasploit/unix_users.txt`) against the target host (`192.168.1.1`):

```
root@kali:~# enumiax -d /usr/share/wordlists/metasploit/unix_users.txt 192.168.1.1
```
