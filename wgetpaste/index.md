---
Title: wgetpaste
Homepage: http://wgetpaste.zlin.dk/
Repository: https://gitlab.com/kalilinux/packages/wgetpaste
Architectures: all
Version: 2.30-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### wgetpaste
 
  This package contains a script that automates pasting to a number of pastebin
  services.
 
 **Installed size:** `49 KB`  
 **How to install:** `sudo apt install wgetpaste`  
 
 {{< spoiler "Dependencies:" >}}
 * wget
 {{< /spoiler >}}
 
 ##### wgetpaste
 
 
 ```
 root@kali:~# wgetpaste -h
 Usage: /usr/bin/wgetpaste [options] [file[s]]
 
 Options:
     -l, --language LANG           set language (defaults to "Plain Text")
     -d, --description DESCRIPTION set description (defaults to "stdin" or filename)
     -n, --nick NICK               set nick (defaults to your username)
     -s, --service SERVICE         set service to use (defaults to "dpaste")
     -e, --expiration EXPIRATION   set when it should expire (defaults to "30 days")
 
     -S, --list-services           list supported pastebin services
     -L, --list-languages          list languages supported by the specified service
     -E, --list-expiration         list expiration setting supported by the specified service
 
     -u, --tinyurl URL             convert input url to tinyurl
 
     -c, --command COMMAND         paste COMMAND and the output of COMMAND
     -i, --info                    append the output of `emerge --info`
     -I, --info-only               paste the output of `emerge --info` only
     -x, --xcut                    read input from clipboard (requires x11-misc/xclip)
     -X, --xpaste                  write resulting url to the X primary selection buffer (requires x11-misc/xclip)
     -C, --xclippaste              write resulting url to the X clipboard selection buffer (requires x11-misc/xclip)
 
     -r, --raw                     show url for the raw paste (no syntax highlighting or html)
     -t, --tee                     use tee to show what is being pasted
     -v, --verbose                 show wget stderr output if no url is received
         --completions             emit output suitable for shell completions (only affects --list-*)
         --debug                   be *very* verbose (implies -v)
 
     -h, --help                    show this help
     -g, --ignore-configs          ignore /etc/wgetpaste.conf, ~/.wgetpaste.conf etc.
         --version                 show version information
 
 Defaults (DEFAULT_{NICK,LANGUAGE,EXPIRATION}[_${SERVICE}] and DEFAULT_SERVICE)
 can be overridden globally in /etc/wgetpaste.conf or /etc/wgetpaste.d/*.conf or
 per user in any of ~/.wgetpaste.conf or ~/.wgetpaste.d/*.conf.
 
 An additional http header can be passed by setting HEADER_${SERVICE} in any of the
 configuration files mentioned above. For example, authenticating with github gist:
 HEADER_gists="Authorization: token 1234abc56789...", or with gitlab snippets:
 HEADER_snippets="PRIVATE-TOKEN: 1234abc56789..."
 
 You can also set PUBLIC_gists='false' if you want to default to secret instead of
 public github gists. In the case of gitlab, you can set VISIBILITY_snippets= to
 'public', 'private' or 'internal'"
 
 To change your gitlab server, you can override the default API URL setting
 URL_snippets='https://gitlab.[server].com/api/v4/snippets'
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
