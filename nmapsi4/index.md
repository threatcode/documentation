---
Title: nmapsi4
Homepage: https://www.nmapsi4.org
Repository: https://salsa.debian.org/pkg-security-team/nmapsi4
Architectures: any
Version: 0.5~alpha2-4
Metapackages: kali-linux-everything 
Icon: images/nmapsi4-logo.svg
PackagesInfo: |
 ### nmapsi4
 
  NmapSI4 is a complete Qt-based Gui with the design goal to provide a complete
  nmap interface for users, in order to manage all options of this power
  security net scanner.
 
 **Installed size:** `1.25 MB`  
 **How to install:** `sudo apt install nmapsi4`  
 
 {{< spoiler "Dependencies:" >}}
 * bind9-dnsutils
 * libc6 
 * libgcc-s1 
 * libqt5core5a 
 * libqt5dbus5 
 * libqt5gui5  | libqt5gui5-gles 
 * libqt5network5 
 * libqt5qml5 
 * libqt5quick5  | libqt5quick5-gles 
 * libqt5webenginewidgets5 
 * libqt5widgets5 
 * libstdc++6 
 * nmap
 {{< /spoiler >}}
 
 ##### nmapsi4
 
 A Qt4 interface for nmap
 
 ```
 root@kali:~# man nmapsi4
 nmapsi4(1)                  General Commands Manual                 nmapsi4(1)
 
 NAME
        nmapsi4 - A Qt4 interface for nmap
 
 SYNOPSIS
        nmapsi4 [Qt-options] [KDE-options] [File]
 
 DESCRIPTION
        This  manual  page  documents briefly the nmapsi4 QT Application.  This
        manual page was written for the Debian GNU/Linux  distribution  because
        the original program does not have a manual page.
 
        nmapsi4  is  a full-featured interface for the nmap(1) security network
        scanner.
 
 OPTIONS
    Arguments:
        File(s)
               file(s) to open
 
    General Options
        --help Show help about options
 
        --help-qt
               Show Qt specific options
 
        --help-kde
               Show KDE specific options
 
        --help-all
               Show all options
 
        --author
               Show author information
 
        -v, --version
               Show version information
 
        --license
               Show license information
 
        --     End of options
               This manual page was prepared by Francesco Cecconi
               <francesco.cecconi@gmail.com> for the Debian GNU/Linux system
               (but may be used by others).
 
 SEE ALSO
        If the khelpcenter program is properly installed at your site, the com-
        mand
 
               khelpcenter help:/nmapsi4
 
        should give you access to the complete manual.
 
        Alternatively the manual can be browsed in konqueror giving it the URL
        help:/nmapsi4
 
 QT Application                  April 25, 2007                      nmapsi4(1)
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
