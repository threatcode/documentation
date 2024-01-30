---
Title: unhide.rb
Homepage: https://launchpad.net/unhide.rb
Repository: https://salsa.debian.org/pkg-security-team/unhide.rb
Architectures: all
Version: 22-6
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### unhide.rb
 
  Unhide.rb is a forensics tool to find processes hidden by rootkits.
   
  It looks for active processes in many different ways. Processes found by
  some means but not others are considered to be "hidden", and are reported
  to the user.
   
  Unhide.rb is a tentative of rewrite in Ruby of the original Unhide, which
  is written in C. While being much faster, it does not implement all the
  diagnostics of the original version. It is also less secure as it cannot
  be statically compiled.
   
  This package can be used by rkhunter in its daily scans.
 
 **Installed size:** `32 KB`  
 **How to install:** `sudo apt install unhide.rb`  
 
 {{< spoiler "Dependencies:" >}}
 * procps
 * ruby
 {{< /spoiler >}}
 
 ##### unhide.rb
 
 Scans system for hidden processes and lists any hits on stderr.
 
 ```
 root@kali:~# man unhide.rb
 unhide.rb(8)        unhide.rb - Finder of hidden processes        unhide.rb(8)
 
 NAME
        unhide.rb  -  Scans  system  for hidden processes and lists any hits on
        stderr.
 
 SYNOPSIS
        unhide.rb
 
 DESCRIPTION
        Scans the system for hidden processes.
 
        Progress messages are printed  on  stdout  and  can  be  redirected  to
        /dev/null.
 
        Error  diagnostics  and information about any hidden processes found is
        printed to stderr.
 
 OPTIONS
        unhide.rb takes no options
 
 EXIT STATUS
        0      No hidden processes found
 
        1      Something went wrong during scanning
 
        2      One or more hidden processes were detected
 
 BUGS
        Report  bugs  to  <johan.walles@gmail.com>   or   <https://bugs.launch-
        pad.net/unhide.rb>.
 
 LICENSING
        unhide.rb  is  licensed  under  the  GPL-3, copyright Johan Walles <jo-
        han.walles@gmail.com>.
 
 SEE ALSO
        rkhunter(8)
 
        The unhide.rb home page: <http://launchpad.net/unhide.rb>
 
 NOTES
        unhide.rb is a Ruby port of unhide.  When it  was  first  written,  the
        Ruby port was about 10x faster than the original C program and had much
        better diagnostics when hidden processes were found.   The original un-
        hide program can be found at <http://www.unhide-forensics.info/>.
 
                                   March 2011                      unhide.rb(8)
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
