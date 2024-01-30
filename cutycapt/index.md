---
Title: cutycapt
Homepage: http://cutycapt.sourceforge.net/
Repository: https://anonscm.debian.org/cgit/collab-maint/cutycapt.git
Architectures: any
Version: 0.0~svn10-0.1
Metapackages: kali-linux-default kali-linux-everything kali-linux-large kali-tools-information-gathering kali-tools-reporting kali-tools-vulnerability kali-tools-web 
Icon: images/cutycapt-logo.svg
PackagesInfo: |
 ### cutycapt
 
  CutyCapt is a small cross-platform command-line utility to capture WebKit's
  rendering of a web page into a variety of vector and bitmap formats, including
  SVG, PDF, PS, PNG, JPEG, TIFF, GIF, and BMP.
 
 **Installed size:** `66 KB`  
 **How to install:** `sudo apt install cutycapt`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libgcc1 
 * libqt5core5a 
 * libqt5gui5  | libqt5gui5-gles 
 * libqt5network5 
 * libqt5printsupport5 
 * libqt5svg5 
 * libqt5webkit5 
 * libqt5widgets5 
 * libstdc++6 
 {{< /spoiler >}}
 
 ##### cutycapt
 
 Utility to capture WebKit's rendering of a web page
 
 ```
 root@kali:~# man cutycapt
 CUTYCAPT(1)                 General Commands Manual                CUTYCAPT(1)
 
 NAME
        cutycapt - utility to capture WebKit's rendering of a web page
 
 SYNOPSIS
        cutycapt [options] --url=http://www.someurl.com --out=output.png
 
 DESCRIPTION
        This manual page documents briefly the cutycapt command.
 
        CutyCapt  is a small cross-platform command-line utility to capture We-
        bKit's rendering of a web page into a variety of vector and bitmap for-
        mats, including SVG, PDF, PS, PNG, JPEG, TIFF, GIF, and BMP.
 
 OPTIONS
        A summary of options is included below.
 
        --help Show summary of options.
 
        --url=<url>
               The URL to capture (http:...|file:...|...)
 
        --out=<path>
               The target file (.png|pdf|ps|svg|jpeg|...)
 
        --out-format=<f>
               Like extension in --out, overrides heuristic
 
        --min-width=<int>
               Minimal width for the image (default: 800)
 
        --min-height=<int>
               Minimal height for the image (default: 600)
 
        --max-wait=<ms>
               Don't wait more than (default: 90000, infinite: 0)
 
        --delay=<ms>
               After successful load, wait (default: 0)
 
        --user-style-path=<path>
               Location of user style sheet file, if any
 
        --user-style-string=<css>
               User style rules specified as text
 
        --header=<name>:<value>
               Request header; repeatable; some can't be set
 
        --method=<get|post|put>
               Specifies the request method (default: get)
 
        --body-string=<string>
               Unencoded request body (default: none)
 
        --body-base64=<base64>
               Base64-encoded request body (default: none)
 
        --app-name=<name>
               Application name used in User-Agent; default is none
 
        --app-version=<version>
               Application version used in User-Agent; default is none
 
        --user-agent=<string>
               Override the User-Agent header Qt would set
 
        --javascript=<on|off>
               JavaScript execution (default: on)
 
        --java=<on|off>
               Java execution (default: unknown)
 
        --plugins=<on|off>
               Plugin execution (default: unknown)
 
        --private-browsing=<on|off>
               Private browsing (default: unknown)
 
        --auto-load-images=<on|off>
               Automatic image loading (default: on)
 
        --js-can-open-windows=<on|off>
               Script can open windows? (default: unknown)
 
        --js-can-access-clipboard=<on|off>
               Script clipboard privs (default: unknown)
 
        --print-backgrounds=<on|off>
               Backgrounds in PDF/PS output (default: off)
 
        --zoom-factor=<float>
               Page zoom factor (default: no zooming)
 
        --zoom-text-only=<on|off>
               Whether to zoom only the text (default: off)
 
        --http-proxy=<url>
               Address for HTTP proxy server (default: none)
 
 AUTHOR
        CutyCapt was written by Bjorn Hohrmann <bjoern@hoehrmann.de>.
 
        This manual page was written by David Paleino  <dapal@debian.org>,  for
        the  Debian  project (and may be used by others), and is licensed under
        the GNU General Public License, version 2 or later.
 
                                  June 28, 2010                     CUTYCAPT(1)
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## Screenshots

![cutycapt](images/cutycapt.png)

## cutycapt Usage Example

Take a capture of the URL (`–url=http://www.kali.org`) and save it to disk (`–out=kali.png`):

```
root@kali:~# cutycapt --url=http://www.kali.org --out=kali.png
libpng warning: iCCP: known incorrect sRGB profile
libpng warning: iCCP: known incorrect sRGB profile
```
