---
Title: chromium
Homepage: http://www.chromium.org/Home
Repository: https://salsa.debian.org/chromium-team/chromium
Architectures: i386 amd64 arm64 armhf ppc64el all
Version: 119.0.6045.159-1
Metapackages: kali-linux-everything 
Icon: images/chromium-logo.svg
PackagesInfo: |
 ### chromium
 
  Web browser that aims to build a safer, faster, and more stable internet
  browsing experience.
   
  This package contains the web browser component.
 
 **Installed size:** `222.96 MB`  
 **How to install:** `sudo apt install chromium`  
 
 {{< spoiler "Dependencies:" >}}
 * chromium-common 
 * libasound2 
 * libatk-bridge2.0-0 
 * libatk1.0-0 
 * libatomic1 
 * libatspi2.0-0 
 * libc6 
 * libcairo2 
 * libcups2 
 * libdbus-1-3 
 * libdouble-conversion3 
 * libdrm2 
 * libevent-2.1-7 
 * libexpat1 
 * libflac12 
 * libfontconfig1 
 * libfreetype6 
 * libgbm1 
 * libgcc-s1 
 * libglib2.0-0 
 * libgtk-3-0 | xdg-desktop-portal-backend
 * libjpeg62-turbo 
 * libjsoncpp25 
 * liblcms2-2 
 * libminizip1
 * libnspr4 
 * libnss3 
 * libopenh264-7 
 * libopenjp2-7 
 * libopus0 
 * libpango-1.0-0 
 * libpng16-16 
 * libpulse0 
 * libsnappy1v5 
 * libstdc++6 
 * libwebp7 
 * libwebpdemux2 
 * libwebpmux3 
 * libwoff1 
 * libx11-6
 * libxcb1 
 * libxcomposite1 
 * libxdamage1 
 * libxext6
 * libxfixes3
 * libxkbcommon0 
 * libxml2 
 * libxnvctrl0
 * libxrandr2
 * libxslt1.1 
 * zlib1g 
 {{< /spoiler >}}
 
 ##### chromium
 
 The web browser from Google
 
 ```
 root@kali:~# chromium -h
 chromium [-h|--help] [-g|--debug] [--temp-profile] [options] [URL]
 
         -g or --debug              Start within /usr/bin/gdb
         -h or --help               This help screen
         --temp-profile             Start with a new and temporary profile
         --enable-remote-extensions Allow extensions from remote sites
 
  Other supported options are:
        chromium has hundreds of undocumented command-line flags that are added
        and  removed  at  the  whim of the developers.  Here, we document rela-
        tively stable flags.
 
        -h or --help
               Show help output.
 
        -g or --debug
               Start a debugging session within /usr/bin/gdb.
 
        --temp-profile
               Use a throw-away/temporary profile for this session.  This  cre-
               ates  an  entirely  new user profile temporarily.  It is not the
               same as incognito mode.
 
        --enable-remote-extensions
               Allow installation and updates of remote extensions.
 
        --user-data-dir=DIR
               Specifies the directory that user data (your "profile") is  kept
               in.  Defaults to $HOME/.config/chromium .  Separate instances of
               chromium must use separate user data directories; repeated invo-
               cations  of  chromium will reuse an existing process for a given
               user data directory.
 
        --incognito
               Open in incognito mode.
 
        --new-window
               If PATH or URL is given, open it in a new window.
 
        --proxy-server=host:port
               Specify the HTTP/SOCKS4/SOCKS5 proxy server to use for requests.
               This overrides any environment variables or settings picked  via
               the options dialog.  An individual proxy server is specified us-
               ing the format:
 
                 [<proxy-scheme>://]<proxy-host>[:<proxy-port>]
 
               Where <proxy-scheme> is the protocol of the proxy server, and is
               one of:
 
                 "http", "socks", "socks4", "socks5".
 
               If  the  <proxy-scheme>  is omitted, it defaults to "http". Also
               note that "socks" is equivalent to "socks5".
 
               Examples:
 
                 --proxy-server="foopy:99"
                     Use the HTTP proxy "foopy:99" to load all URLs.
 
                 --proxy-server="socks://foobar:1080"
                     Use the SOCKS v5 proxy "foobar:1080" to load all URLs.
 
                 --proxy-server="socks4://foobar:1080"
                     Use the SOCKS v4 proxy "foobar:1080" to load all URLs.
 
                 --proxy-server="socks5://foobar:66"
                     Use the SOCKS v5 proxy "foobar:66" to load all URLs.
 
               It is also possible to specify a separate proxy server for  dif-
               ferent URL types, by prefixing the proxy server specifier with a
               URL specifier:
 
               Example:
 
                 --proxy-server="https=proxy1:80;http=socks4://baz:1080"
                     Load  https://* URLs using the HTTP proxy "proxy1:80". And
               load http://*
                     URLs using the SOCKS v4 proxy "baz:1080".
 
        --no-proxy-server
               Disables the proxy server.  Overrides any environment  variables
               or settings picked via the options dialog.
 
        --proxy-auto-detect
               Autodetect proxy configuration.  Overrides any environment vari-
               ables or settings picked via the options dialog.
 
        --proxy-pac-url=URL
               Specify  proxy autoconfiguration URL.  Overrides any environment
               variables or settings picked via the options dialog.
 
        --password-store=<basic|gnome|kwallet>
               Set the password store to use.  The default is to  automatically
               detect  based  on  the  desktop  environment.  basic selects the
               built in,  unencrypted  password  store.   gnome  selects  Gnome
               keyring.  kwallet selects (KDE) KWallet.  (Note that KWallet may
               not work reliably outside KDE.)
 
        --version
               Show version information.
 
        As  a  GTK+  app,  chromium also obeys GTK+ command-line flags, such as
        --display.  See the GTK documentation for more:
 
               <http://library.gnome.org/devel/gtk/stable/gtk-running.html>
 
               <http://library.gnome.org/devel/gtk/stable/gtk-x11.html>
 
  See 'man chromium' for more details
 ```
 
 - - -
 
 ### chromium-common
 
  Web browser that aims to build a safer, faster, and more stable internet
  browsing experience.
   
  This package contains resources that are in common to different chromium
  packages.
 
 **Installed size:** `16.82 MB`  
 **How to install:** `sudo apt install chromium-common`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libjsoncpp25 
 * libstdc++6 
 * libx11-6
 * libxnvctrl0
 * x11-utils
 * xdg-utils
 * zlib1g 
 {{< /spoiler >}}
 
 
 - - -
 
 ### chromium-driver
 
  Web browser that aims to build a safer, faster, and more stable internet
  browsing experience.
   
  This package provides a bridge between the browser component and the selenium
  automatic webdriver.
 
 **Installed size:** `15.56 MB`  
 **How to install:** `sudo apt install chromium-driver`  
 
 {{< spoiler "Dependencies:" >}}
 * chromium 
 * libatomic1 
 * libc6 
 * libdouble-conversion3 
 * libevent-2.1-7 
 * libgcc-s1 
 * libglib2.0-0 
 * libjsoncpp25 
 * libminizip1
 * libnspr4 
 * libnss3 
 * libstdc++6 
 * libxcb1 
 * zlib1g 
 {{< /spoiler >}}
 
 ##### chromedriver
 
 
 ```
 root@kali:~# chromedriver -h
 Usage: chromedriver [OPTIONS]
 
 Options
   --port=PORT                     port to listen on
   --adb-port=PORT                 adb server port
   --log-path=FILE                 write server log to file instead of stderr, increases log level to INFO
   --log-level=LEVEL               set log level: ALL, DEBUG, INFO, WARNING, SEVERE, OFF
   --verbose                       log verbosely (equivalent to --log-level=ALL)
   --silent                        log nothing (equivalent to --log-level=OFF)
   --append-log                    append log file instead of rewriting
   --replayable                    (experimental) log verbosely and don't truncate long strings so that the log can be replayed.
   --version                       print the version number and exit
   --url-base                      base URL path prefix for commands, e.g. wd/url
   --readable-timestamp            add readable timestamps to log
   --enable-chrome-logs            show logs from the browser (overrides other logging options)
   --bidi-mapper-path              custom bidi mapper path
   --disable-dev-shm-usage         do not use /dev/shm (add this switch if seeing errors related to shared memory)
   --allowed-ips=LIST              comma-separated allowlist of remote IP addresses which are allowed to connect to ChromeDriver
   --allowed-origins=LIST          comma-separated allowlist of request origins which are allowed to connect to ChromeDriver. Using `*` to allow any host origin is dangerous!
 ```
 
 - - -
 
 ### chromium-l10n
 
  Web browser that aims to build a safer, faster, and more stable internet
  browsing experience.
   
  This package contains language packages for:
  am, ar, bg, bn, ca, cs, da, de, el, en-GB, es-419, es, et, fi, fil, fr, gu, he,
  hi, hr, hu, id, it, ja, kn, ko, lt, lv, ml, mr, nb, nl, pl, pt-BR, pt-PT,
  ro, ru, sk, sl, sr, sv, sw, ta, te, th, tr, uk, vi, zh-CN, zh-TW
 
 **Installed size:** `87.12 MB`  
 **How to install:** `sudo apt install chromium-l10n`  
 
 {{< spoiler "Dependencies:" >}}
 * chromium 
 {{< /spoiler >}}
 
 
 - - -
 
 ### chromium-sandbox
 
  Web browser that aims to build a safer, faster, and more stable internet
  browsing experience.
   
  This package contains the setuid chromium sandbox.
 
 **Installed size:** `341 KB`  
 **How to install:** `sudo apt install chromium-sandbox`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 
 - - -
 
 ### chromium-shell
 
  Web browser that aims to build a safer, faster, and more stable internet
  browsing experience.
   
  This package provides a minimal version of the chromium user interface
  (the content shell).
 
 **Installed size:** `161.81 MB`  
 **How to install:** `sudo apt install chromium-shell`  
 
 {{< spoiler "Dependencies:" >}}
 * chromium-common 
 * libasound2 
 * libatk-bridge2.0-0 
 * libatk1.0-0 
 * libatomic1 
 * libatspi2.0-0 
 * libc6 
 * libcairo2 
 * libdbus-1-3 
 * libdouble-conversion3 
 * libdrm2 
 * libevent-2.1-7 
 * libexpat1 
 * libflac12 
 * libfontconfig1 
 * libfreetype6 
 * libgbm1 
 * libgcc-s1 
 * libglib2.0-0 
 * libjpeg62-turbo 
 * libjsoncpp25 
 * libminizip1
 * libnspr4 
 * libnss3 
 * libopenh264-7 
 * libopus0 
 * libpango-1.0-0 
 * libpng16-16 
 * libpulse0 
 * libsnappy1v5 
 * libstdc++6 
 * libwebp7 
 * libwebpdemux2 
 * libwebpmux3 
 * libwoff1 
 * libx11-6
 * libxcb1 
 * libxcomposite1 
 * libxdamage1 
 * libxext6
 * libxfixes3
 * libxkbcommon0 
 * libxml2 
 * libxnvctrl0
 * libxrandr2
 * libxslt1.1 
 * zlib1g 
 {{< /spoiler >}}
 
 ##### chromium-shell
 
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
