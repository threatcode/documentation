---
Title: phishery
Homepage: https://github.com/ryhanson/phishery
Repository: https://gitlab.com/kalilinux/packages/phishery
Architectures: any
Version: 1.0.2-0kali2
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### phishery
 
  This package contains a Simple SSL Enabled HTTP server with the primary
  purpose of phishing credentials via Basic Authentication.
  The power of phishery is best demonstrated by setting a Word document's
  template to a phishery URL. This causes Microsoft Word to make a request to
  the URL, resulting in an Authentication Dialog being shown to the end-user. The
  ability to inject any .docx file with a URL is possible using phishery's
  -i [in docx], -o [out docx], and -u [url] options.
 
 **Installed size:** `5.05 MB`  
 **How to install:** `sudo apt install phishery`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### phishery
 
 
 ```
 root@kali:~# phishery -h
 |\   \\\\__   O         __    _      __
 | \_/    o \  o  ____  / /_  (_)____/ /_  ___  _______  __
 > _   (( <_ oO  / __ \/ __ \/ / ___/ __ \/ _ \/ ___/ / / /
 | / \__+___/   / /_/ / / / / (__  ) / / /  __/ /  / /_/ /
 |/     |/     / .___/_/ /_/_/____/_/ /_/\___/_/   \__, /
              /_/ Basic Auth Credential Harvester (____/
                  with Word Doc Template Injector
 
   Start the server  : phishery -s settings.json -c credentials.json
   Inject a template : phishery -u https://secure.site.local/docs -i good.docx -o bad.docx
 
   Options:
     -h, --help      Show usage and exit.
     -v              Show version and exit.
     -s              The JSON settings file used to setup the server. [default: "/etc/phishery/settings.json"]
     -c              The JSON file to store harvested credentials. [default: "/etc/phishery/credentials.json"]
     -u              The phishery URL to use as the Word document template.
     -i              The Word .docx file to inject with a template URL.
     -o              The new Word .docx file with the injected template URL.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
