---
Title: tightvnc
Homepage: https://www.tightvnc.com
Repository: https://salsa.debian.org/debian-remote-team/tightvnc
Architectures: any
Version: 1:1.3.10-7
Metapackages: kali-linux-default kali-linux-everything kali-linux-large 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### tightvncpasswd
 
  VNC stands for Virtual Network Computing. It is, in essence, a remote
  display system which allows you to view a computing `desktop' environment
  not only on the machine where it is running, but from anywhere on the
  Internet and from a wide variety of machine architectures.
   
  This package provides the vncpasswd tool mandatory for the tightvncserver
  and optional for the xtightvncviewer.
 
 **Installed size:** `69 KB`  
 **How to install:** `sudo apt install tightvncpasswd`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### tightvncpasswd
 
 Set passwords for VNC server
 
 ```
 root@kali:~# man tightvncpasswd
 vncpasswd(1)                       TightVNC                       vncpasswd(1)
 
 NAME
        vncpasswd - set passwords for VNC server
 
 SYNOPSIS
        vncpasswd [file]
        vncpasswd -t
        vncpasswd -f
 
 DESCRIPTION
        The vncpasswd utility should be used to create and change passwords for
        the  TightVNC  server  authentication.  Xvnc  uses  such passwords when
        started with the -rfbauth command-line option (or when started from the
        vncserver script).
 
        vncpasswd allows one to enter either one or two  passwords.  The  first
        password  is the primary one, the second password can be used for view-
        only authentication. Xvnc will restrict mouse and keyboard  input  from
        clients  who  authenticated  with the view-only password. The vncpasswd
        utility asks interactively if it should set the second password.
 
        The password file name defaults to $HOME/.vnc/passwd unless the -t com-
        mand-line  option  was  used  (see  the  OPTIONS  section  below).  The
        $HOME/.vnc/ directory will be created if it does not exist.
 
        Each password has to be longer than five characters (unless the -f com-
        mand-line  option was used, see its description below).  Only the first
        eight characters are significant. If the primary password is too short,
        the program will abort. If the view-only password is  too  short,  then
        only the primary password will be saved.
 
        Unless  a  file  name was provided in the command-line explicitly, this
        utility may perform certain sanity checks to prevent writing a password
        file into some hazardous place.
 
        If at least one password was saved successfully,  vncpasswd  will  exit
        with  status  code 0. Otherwise the returned status code will be set to
        1.
 
 OPTIONS
        -t     Write  passwords  into   /tmp/$USER-vnc/passwd,   creating   the
               /tmp/$USER-vnc/ directory if it does not exist, and checking the
               permissions  on  that directory (the mode must be 700). This op-
               tion can help to improve security when your home  partition  may
               be shared via network (e.g. when using NFS).
 
        -f     Filter  mode.  Read  plain-text  passwords from stdin, write en-
               crypted versions to stdout. One or two  passwords  (full-control
               and view-only) can be supplied in the input stream, newline ter-
               minates a password.  Note that in the filter mode, short or even
               empty passwords will be silently accepted.
 
 SEE ALSO
        vncserver(1), Xvnc(1), vncviewer(1), vncconnect(1)
 
 AUTHORS
        Original VNC was developed in AT&T Laboratories Cambridge. TightVNC ad-
        ditions  were  implemented  by  Constantin Kaplinsky. Many other people
        participated in development, testing and support.
 
        Man page authors:
        Marcus Brinkmann <Marcus.Brinkmann@ruhr-uni-bochum.de>,
        Tim Waugh <twaugh@redhat.com>,
        Constantin Kaplinsky <const@tightvnc.com>
 
                                   August 2006                     vncpasswd(1)
 ```
 
 - - -
 
 ### tightvncserver
 
  VNC stands for Virtual Network Computing. It is, in essence, a remote
  display system which allows you to view a computing `desktop' environment
  not only on the machine where it is running, but from anywhere on the
  Internet and from a wide variety of machine architectures.
   
  This package provides a server to which X clients can connect and the
  server generates a display that can be viewed with a vncviewer.
   
  The difference between the tightvncserver and the normal vncserver is the
  data encoding, optimized for low bandwidth connections. If the client do not
  support jpeg or zlib encoding it can use the default one. Later versions of
  vncserver (> 3.3.3r2) support a new automatic encoding that should be equally
  good as the tightvnc encoding.
   
  Note: This server does not support or need a display. You need a vncviewer to
  see something. However, this viewer may also be on a computer running other
  operating systems in the local net.
 
 **Installed size:** `1.69 MB`  
 **How to install:** `sudo apt install tightvncserver`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libjpeg62-turbo 
 * libx11-6
 * perl
 * tightvncpasswd 
 * x11-common | xserver-common
 * x11-utils
 * xauth
 * zlib1g 
 {{< /spoiler >}}
 
 ##### Xtightvnc
 
 An X server providing VNC connectivity
 
 ```
 root@kali:~# Xtightvnc -h
 Unrecognized option: -h
 use: X [:<display>] [option]
 -a #                   mouse acceleration (pixels)
 -ac                    disable access control restrictions
 -audit int             set audit trail level
 -auth file             select authorization file
 bc                     enable bug compatibility
 -bs                    disable any backing store support
 -c                     turns off key-click
 c #                    key-click volume (0-100)
 -cc int                default color visual class
 -co file               color database file
 -core                  generate core dump on fatal error
 -dpi int               screen resolution in dots per inch
 -deferglyphs [none|all|16] defer loading of [no|all|16-bit] glyphs
 -f #                   bell base (0-100)
 -fc string             cursor font
 -fn string             default font name
 -fp string             default font path
 -help                  prints message with these options
 -I                     ignore all remaining arguments
 -ld int                limit data space to N Kb
 -lf int                limit number of open files to N
 -ls int                limit stack space to N Kb
 -nolock                disable the locking mechanism
 -logo                  enable logo in screen saver
 nologo                 disable logo in screen saver
 -nolisten string       don't listen on protocol
 -p #                   screen-saver pattern duration (minutes)
 -pn                    accept failure to listen on all ports
 -nopn                  reject failure to listen on all ports
 -r                     turns off auto-repeat
 r                      turns on auto-repeat 
 -s #                   screen-saver timeout (minutes)
 -su                    disable any save under support
 -t #                   mouse threshold (pixels)
 -terminate             terminate at server reset
 -to #                  connection time out
 -tst                   disable testing extensions
 ttyxx                  server started from init on /dev/ttyxx
 v                      video blanking for screen-saver
 -v                     screen-saver without video blanking
 -wm                    WhenMapped default backing-store
 -x string              loads named extension at init time 
 -query host-name       contact named host for XDMCP
 -broadcast             broadcast for XDMCP
 -indirect host-name    contact named host for indirect XDMCP
 -port port-num         UDP port number to send messages to
 -once                  Terminate server after one session
 -class display-class   specify display class to send in manage
 -cookie xdm-auth-bits  specify the magic cookie for XDMCP
 -displayID display-id  manufacturer display ID for request
 -geometry WxH          set framebuffer width & height
 -depth D               set framebuffer depth
 -pixelformat format    set pixel format (BGRnnn or RGBnnn)
 -udpinputport port     UDP port for keyboard/pointer data
 -rfbport port          TCP port for RFB protocol
 -rfbwait time          max time in ms to wait for RFB client
 -nocursor              don't put up a cursor
 -rfbauth passwd-file   use authentication on RFB protocol
 -httpd dir             serve files via HTTP from here
 -httpport port         port for HTTP
 -deferupdate time      time in ms to defer updates (default 40)
 -economictranslate     less memory-hungry translation
 -lazytight             disable "gradient" filter in tight encoding
 -desktop name          VNC desktop name (default x11)
 -alwaysshared          always treat new clients as shared
 -nevershared           never treat new clients as shared
 -dontdisconnect        don't disconnect existing clients when a new non-shared
                        connection comes in (refuse new connection instead)
 -viewonly              let clients only to view the desktop
 -localhost             only allow connections from localhost
 -interface ipaddr      only bind to specified interface address
 -inetd                 Xvnc is launched by inetd
 -compatiblekbd         set META key = ALT key as in the original VNC
 -version               report Xvnc version on stderr
 ```
 
 - - -
 
 ##### tightvncconnect
 
 Connect a VNC server to a VNC viewer
 
 ```
 root@kali:~# tightvncconnect -h
 usage: tightvncconnect [-display Xvnc-display] host[:port]
 Tells Xvnc to connect to a listening VNC viewer on the given host and port
 ```
 
 - - -
 
 ##### tightvncserver
 
 A wrapper to launch an X server for VNC.
 
 ```
 root@kali:~# tightvncserver -h
 TightVNC Server version 1.3.10
 
 Usage: tightvncserver [<OPTIONS>] [:<DISPLAY#>]
        tightvncserver -kill :<DISPLAY#>
 
 <OPTIONS> are Xtightvnc options, or:
 
         -name <DESKTOP-NAME>
         -depth <DEPTH>
         -geometry <WIDTH>x<HEIGHT>
         -httpport number
         -basehttpport number
         -alwaysshared
         -nevershared
         -pixelformat rgb<NNN>
         -pixelformat bgr<NNN>
 
 See vncserver and Xtightvnc manual pages for more information.
 ```
 
 - - -
 
 ### xtightvncviewer
 
  VNC stands for Virtual Network Computing. It is, in essence, a remote
  display system which allows you to view a computing `desktop' environment
  not only on the machine where it is running, but from anywhere on the
  Internet and from a wide variety of machine architectures.
   
  It is implemented in a client/server model. This package provides a client
  for X, with this you can connect to a vncserver somewhere in the network
  and display its content in a window. There are vncserver available for other
  operating systems.
   
  The difference between the xtightvncviewer and the normal vncviewer is the
  data encoding, optimized for low bandwidth connections. If the client do not
  support jpeg or zlib encoding it can use the default one. Later versions of
  xvncviewer (> 3.3.3r2) support a new automatic encoding that should be equally
  good as the tightvnc encoding.
 
 **Installed size:** `182 KB`  
 **How to install:** `sudo apt install xtightvncviewer`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libjpeg62-turbo 
 * libx11-6
 * libxaw7 
 * libxext6
 * libxmu6 
 * libxt6
 * zlib1g 
 {{< /spoiler >}}
 
 ##### xtightvncviewer
 
 An X viewer client for VNC
 
 ```
 root@kali:~# man xtightvncviewer
 vncviewer(1)                       TightVNC                       vncviewer(1)
 
 NAME
        vncviewer - an X viewer client for VNC
 
 SYNOPSIS
        vncviewer [options] [host][:display]
        vncviewer [options] [host][::port]
        vncviewer [options] -listen [display]
        vncviewer -help
 
 DESCRIPTION
        vncviewer  is  an Xt-based client application for the VNC (Virtual Net-
        work Computing) system. It can connect  to  any  VNC-compatible  server
        such  as Xvnc or WinVNC, allowing you to control desktop environment of
        a different machine.
 
        You can use F8 to display a pop-up utility menu. Press F8 twice to pass
        single F8 to the remote side.
 
 OPTIONS
        -help  Prints a short usage notice to stderr.
 
        -listen
               Make the viewer listen on port 5500+display for reverse  connec-
               tions  from  a server. WinVNC supports reverse connections using
               the "Add New Client" menu option, or the -connect  command  line
               option. Xvnc requires the use of the helper program vncconnect.
 
        -via gateway
               Automatically create encrypted TCP tunnel to the gateway machine
               before  connection,  connect  to  the  host  through that tunnel
               (TightVNC-specific). By default, this option invokes  SSH  local
               port forwarding, assuming that SSH client binary can be accessed
               as  /usr/bin/ssh. Note that when using the -via option, the host
               machine name should be specified as known  to  the  gateway  ma-
               chine,  e.g.   "localhost"  denotes the gateway, not the machine
               where vncviewer was launched. See the ENVIRONMENT section  below
               for the information on configuring the -via option.
 
        -shared
               When  connecting, specify that a shared connection is requested.
               In TightVNC, this is the default mode, allowing you to share the
               desktop with other clients already using it.
 
        -noshared
               When connecting, specify that the session  may  not  be  shared.
               This  would  either disconnect other connected clients or refuse
               your connection, depending on the server configuration.
 
        -viewonly
               Disable transfer of mouse and keyboard events from the client to
               the server.
 
        -fullscreen
               Start in full-screen mode. Please be  aware  that  operating  in
               full-screen  mode may confuse X window managers. Typically, such
               conflicts cause incorrect handling of input focus  or  make  the
               viewer  window disappear mysteriously. See the grabKeyboard set-
               ting in the RESOURCES section below for a method to solve  input
               focus problem.
 
        -noraiseonbeep
               By  default,  the  viewer  shows and raises its window on remote
               beep  (bell)  event.  This  option   disables   such   behaviour
               (TightVNC-specific).
 
        -passwd passwd-file
               File  from  which  to get the password (as generated by the vnc-
               passwd(1) program). This option affects only  the  standard  VNC
               authentication.
 
        -encodings encoding-list
               TightVNC  supports  several different compression methods to en-
               code screen updates; this option specifies a set of them to  use
               in  order  of preference. Encodings are specified separated with
               spaces, and must thus be enclosed in quotes if more than one  is
               specified.  Available  encodings,  in default order for a remote
               connection, are "copyrect tight hextile zlib corre rre raw". For
               a local connection (to the same machine), the default  order  to
               try is "raw copyrect tight hextile zlib corre rre". Raw encoding
               is  always  assumed as a last option if no other encoding can be
               used for some reason. For more information on encodings, see the
               section ENCODINGS below.
 
        -bgr233
               Always use the BGR233 format to encode pixel data. This  reduces
               network traffic, but colors may be represented inaccurately. The
               bgr233 format is an 8-bit "true color" format, with 2 bits blue,
               3 bits green, and 3 bits red.
 
        -owncmap
               Try to use a PseudoColor visual and a private colormap. This al-
               lows the VNC server to control the colormap.
 
        -truecolour, -truecolor
               Try to use a TrueColor visual.
 
        -depth depth
               On an X server which supports multiple TrueColor visuals of dif-
               ferent  depths,  attempt  to  use the specified one (in bits per
               pixel); if successful, this depth will be requested from the VNC
               server.
 
        -compresslevel level
               Use specified compression level (0..9) for  "tight"  and  "zlib"
               encodings  (TightVNC-specific). Level 1 uses minimum of CPU time
               and achieves weak compression ratios, while level 9 offers  best
               compression  but is slow in terms of CPU time consumption on the
               server side. Use high levels with very slow network connections,
               and low levels when working over high-speed LANs. It's not  rec-
               ommended  to  use  compression level 0, reasonable choices start
               from the level 1.
 
        -quality level
               Use the specified JPEG quality level (0..9) for the "tight"  en-
               coding  (TightVNC-specific).  Quality  level 0 denotes bad image
               quality but very impressive compression ratios,  while  level  9
               offers very good image quality at lower compression ratios. Note
               that  the  "tight" encoder uses JPEG to encode only those screen
               areas that look suitable for lossy compression, so quality level
               0 does not always mean unacceptable image quality.
 
        -nojpeg
               Disable lossy JPEG compression in Tight encoding  (TightVNC-spe-
               cific).   Disabling JPEG compression is not a good idea in typi-
               cal cases, as that makes the Tight encoder less  efficient.  You
               might  want  to  use this option if it's absolutely necessary to
               achieve perfect image quality (see also the -quality option).
 
        -nocursorshape
               Disable cursor shape updates, protocol extensions used to handle
               remote   cursor   movements   locally   on   the   client   side
               (TightVNC-specific). Using cursor shape updates decreases delays
               with  remote  cursor  movements, and can improve bandwidth usage
               dramatically.
 
        -x11cursor
               Use a real X11 cursor with X-style cursor shape updates, instead
               of drawing the remote cursor on  the  framebuffer.  This  option
               also  disables  the dot cursor, and disables cursor position up-
               dates in non-fullscreen mode.
 
        -autopass
               Read a plain-text password from stdin. This option affects  only
               the standard VNC authentication.
 
 ENCODINGS
        The  server  supplies  information in whatever format is desired by the
        client, in order to make the client as easy as possible  to  implement.
        If  the  client  represents itself as able to use multiple formats, the
        server will choose one.
 
        Pixel format refers to the representation of an individual  pixel.  The
        most  common  formats  are 24 and 16 bit "true-color" values, and 8-bit
        "color map" representations, where an arbitrary map converts the  color
        number to RGB values.
 
        Encoding refers to how a rectangle of pixels are sent (all pixel infor-
        mation in VNC is sent as rectangles). All rectangles come with a header
        giving the location and size of the rectangle and an encoding type used
        by the data which follows. These types are listed below.
 
        Raw    The  raw  encoding  simply  sends width*height pixel values. All
               clients are required to support this encoding type. Raw is  also
               the  fastest when the server and viewer are on the same machine,
               as the connection speed is essentially infinite and raw encoding
               minimizes processing time.
 
        CopyRect
               The Copy Rectangle encoding is efficient when something is being
               moved; the only data sent is the location of  a  rectangle  from
               which  data  should  be copied to the current location. Copyrect
               could also be used to efficiently transmit a repeated pattern.
 
        RRE    The Rise-and-Run-length-Encoding is basically a  2D  version  of
               run-length encoding (RLE). In this encoding, a sequence of iden-
               tical  pixels are compressed to a single value and repeat count.
               In VNC, this is implemented with a background  color,  and  then
               specifications of an arbitrary number of subrectangles and color
               for each. This is an efficient encoding for large blocks of con-
               stant color.
 
        CoRRE  This  is  a  minor  variation on RRE, using a maximum of 255x255
               pixel rectangles. This allows for single-byte values to be used,
               reducing packet size. This is in general more efficient, because
               the savings from sending 1-byte values generally  outweighs  the
               losses from the (relatively rare) cases where very large regions
               are painted the same color.
 
        Hextile
               Here,  rectangles are split up in to 16x16 tiles, which are sent
               in a predetermined order. The data within the tiles is sent  ei-
               ther raw or as a variant on RRE. Hextile encoding is usually the
               best  choice  for using in high-speed network environments (e.g.
               Ethernet local-area networks).
 
        Zlib   Zlib is a very simple encoding that uses zlib  library  to  com-
               press  raw  pixel data. This encoding achieves good compression,
               but consumes a lot of CPU time. Support  for  this  encoding  is
               provided  for  compatibility with VNC servers that might not un-
               derstand Tight encoding which is more  efficient  than  Zlib  in
               nearly all real-life situations.
 
        Tight  Like Zlib encoding, Tight encoding uses zlib library to compress
               the  pixel  data, but it pre-processes data to maximize compres-
               sion ratios, and to minimize CPU  usage  on  compression.  Also,
               JPEG  compression  may be used to encode color-rich screen areas
               (see the description of -quality  and  -nojpeg  options  above).
               Tight encoding is usually the best choice for low-bandwidth net-
               work environments (e.g. slow modem connections).
 
 RESOURCES
        X  resources  that  vncviewer knows about, aside from the normal Xt re-
        sources, are as follows:
 
        shareDesktop
               Equivalent of -shared/-noshared options. Default true.
 
        viewOnly
               Equivalent of -viewonly option. Default false.
 
        fullScreen
               Equivalent of -fullscreen option. Default false.
 
        grabKeyboard
               Grab keyboard in full-screen mode. This can help to solve  prob-
               lems with losing keyboard focus. Default false.
 
        raiseOnBeep
               Equivalent  of -noraiseonbeep option, when set to false. Default
               true.
 
        passwordFile
               Equivalent of -passwd option.
 
        passwordDialog
               Whether to use a dialog box to get the password (true) or get it
               from the tty (false). Irrelevant if passwordFile is set. Default
               false.
 
        encodings
               Equivalent of -encodings option.
 
        compressLevel
               Equivalent of -compresslevel option (TightVNC-specific).
 
        qualityLevel
               Equivalent of -quality option (TightVNC-specific).
 
        enableJPEG
               Equivalent of -nojpeg option, when set to false. Default true.
 
        useRemoteCursor
               Equivalent  of  -nocursorshape  option,  when   set   to   false
               (TightVNC-specific). Default true.
 
        useBGR233
               Equivalent of -bgr233 option. Default false.
 
        nColours
               When using BGR233, try to allocate this many "exact" colors from
               the  BGR233  color  cube.  When using a shared colormap, setting
               this resource lower leaves more colors for other X clients.  Ir-
               relevant  when  using  truecolor.  Default  is  256 (i.e. all of
               them).
 
        useSharedColours
               If the number of "exact" BGR233 colors successfully allocated is
               less than 256 then the rest are filled in  using  the  "nearest"
               colors  available.  This  resource  says whether to only use the
               "exact" BGR233 colors for this purpose, or whether to use  other
               clients'  "shared"  colors as well. Default true (i.e. use other
               clients' colors).
 
        forceOwnCmap
               Equivalent of -owncmap option. Default false.
 
        forceTrueColour
               Equivalent of -truecolour option. Default false.
 
        requestedDepth
               Equivalent of -depth option.
 
        useSharedMemory
               Use MIT shared memory extension if on the same machine as the  X
               server. Default true.
 
        wmDecorationWidth, wmDecorationHeight
               The  total  width  and height taken up by window manager decora-
               tions.  This is used to calculate the maximum size  of  the  VNC
               viewer window.  Default is width 4, height 24.
 
        bumpScrollTime, bumpScrollPixels
               When  in full screen mode and the VNC desktop is bigger than the
               X display, scrolling happens whenever the mouse hits the edge of
               the screen. The maximum speed of scrolling  is  bumpScrollPixels
               pixels  every  bumpScrollTime  milliseconds. The actual speed of
               scrolling will be slower than this, of course, depending on  how
               fast your machine is.  Default 20 pixels every 25 milliseconds.
 
        popupButtonCount
               The  number  of buttons in the popup window. See the README file
               for more information on how to customize the buttons.
 
        debug  For debugging. Default false.
 
        rawDelay, copyRectDelay
               For debugging, see the README file for details. Default 0 (off).
 
 ENVIRONMENT
        When started with the -via option, vncviewer reads the VNC_VIA_CMD  en-
        vironment  variable, expands patterns beginning with the "%" character,
        and executes result as a command assuming that it would create TCP tun-
        nel that should be used for VNC connection. If not set,  this  environ-
        ment variable defaults to "/usr/bin/ssh -f -L %L:%H:%R %G sleep 20".
 
        The following patterns are recognized in the VNC_VIA_CMD (note that all
        the  patterns  %G,  %H,  %L  and %R must be present in the command tem-
        plate):
 
        %%     A literal "%";
 
        %G     gateway host name;
 
        %H     remote VNC host name, as known to the gateway;
 
        %L     local TCP port number;
 
        %R     remote TCP port number.
 
 SEE ALSO
        vncserver(1), Xvnc(1), vncpasswd(1), vncconnect(1), ssh(1)
 
 AUTHORS
        Original VNC was developed in AT&T Laboratories Cambridge. TightVNC ad-
        ditions were implemented by Constantin  Kaplinsky.  Many  other  people
        participated in development, testing and support.
 
        Man page authors:
        Marcus Brinkmann <Marcus.Brinkmann@ruhr-uni-bochum.de>,
        Terran Melconian <terran@consistent.org>,
        Tim Waugh <twaugh@redhat.com>,
        Constantin Kaplinsky <const@tightvnc.com>
 
                                   August 2006                     vncviewer(1)
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
