---
Title: urlcrazy
Homepage: https://www.morningstarsecurity.com/research/urlcrazy
Repository: https://gitlab.com/kalilinux/packages/urlcrazy
Architectures: all
Version: 0.7.3-0kali1
Metapackages: kali-linux-everything kali-linux-large kali-tools-information-gathering 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### urlcrazy
 
  Generate and test domain typos and variations to detect
  and perform typo squatting, URL hijacking, phishing, and
  corporate espionage.
 
 **Installed size:** `1.31 MB`  
 **How to install:** `sudo apt install urlcrazy`  
 
 {{< spoiler "Dependencies:" >}}
 * ruby
 * ruby-async
 * ruby-async-dns
 * ruby-async-http
 * ruby-colorize
 * ruby-httpclient
 * rubygems
 {{< /spoiler >}}
 
 ##### urlcrazy
 
 
 ```
 root@kali:~# urlcrazy -h
 Warning. File descriptor limit may be too low. Check with `ulimit -a` and change with `ulimit -n 10000`
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## Video

<script type="text/javascript" src="https://asciinema.org/a/31882.js" id="asciicast-31882" async></script>

## urlcrazy Usage Example

Search for URLs using the dvorak layout (`-k dvorak`) and do no resolve hostnames (`-r`) for the given domain (`example.com`):

```
root@kali:~# urlcrazy -k dvorak -r example.com
URLCrazy Domain Report
Domain    : example.com
Keyboard  : dvorak
At        : 2014-05-13 17:04:01 -0600

# Please wait. 95 hostnames to process

Typo Type              Typo            CC-A  Extn
---------------------------------------------------
Character Omission     eample.com      ?     com
Character Omission     examle.com      ?     com
Character Omission     exampe.com      ?     com
Character Omission     exampl.com      ?     com
Character Omission     example.cm      ?     cm
Character Omission     exaple.com      ?     com
```
