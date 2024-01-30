---
Title: cmseek
Homepage: https://github.com/Tuhinshubhra/CMSeeK
Repository: https://gitlab.com/kalilinux/packages/cmseek
Architectures: all
Version: 1.1.3-0kali2
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### cmseek
 
  This package contains a CMS Detection and Exploitation suite. It scans
  WordPress, Joomla, Drupal and over 180 other CMSs.
   
  A content management system (CMS) manages the creation and modification of
  digital content. It typically supports multiple users in a collaborative
  environment.
 
 **Installed size:** `400 KB`  
 **How to install:** `sudo apt install cmseek`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-requests
 {{< /spoiler >}}
 
 ##### cmseek
 
 
 ```
 root@kali:~# cmseek -h
 
 CMSeeK Version 1.1.3
 Github: https://github.com/Tuhinshubhra/CMSeeK
 Coded By: @r3dhax0r 
 
 USAGE:
        python3 cmseek.py (for guided scanning) OR
        python3 cmseek.py [OPTIONS] <Target Specification>
 
 SPECIFING TARGET:
       -u URL, --url URL            Target Url
       -l LIST, --list LIST         Path of the file containing list of sites
                                    for multi-site scan (comma separated)
 
 MANIPULATING SCAN:
       -i cms, --ignore--cms cms    Specify which CMS IDs to skip in order to
                                    avoid flase positive. separated by comma ","
 
       --strict-cms cms             Checks target against a list of provided
                                    CMS IDs. separated by comma ","
 
       --skip-scanned               Skips target if it's CMS was previously detected.
 
       --light-scan                 Skips Deep Scan. Does CMS and version detection only.
 
       -o, --only-cms               Only detect CMS, ignore deep scan and version detection.
 
 RE-DIRECT:
       --follow-redirect            Follows all/any redirect(s)
       --no-redirect                Skips all redirects and tests the input target(s)
 
 USER AGENT:
       -r, --random-agent           Use a random user agent
       --googlebot                  Use Google bot user agent
       --user-agent USER_AGENT      Specify a custom user agent
 
 OUTPUT:
       -v, --verbose                Increase output verbosity
 
 VERSION:
       --version                    Show CMSeeK version and exit
 
 HELP & MISCELLANEOUS:
       -h, --help                   Show this help message and exit
       --clear-result               Delete all the scan result
       --batch                      Never ask you to press enter after every site in a list is scanned
 
 EXAMPLE USAGE:
       python3 cmseek.py -u example.com                           # Scan example.com
       python3 cmseek.py -l /home/user/target.txt                 # Scan the sites specified in target.txt (comma separated)
       python3 cmseek.py -u example.com --user-agent Mozilla 5.0  # Scan example.com using custom user-Agent Mozilla is 5.0 used here
       python3 cmseek.py -u example.com --random-agent            # Scan example.com using a random user-Agent
       python3 cmseek.py -v -u example.com                        # enabling verbose output while scanning example.com
 
     
 
  CMSeeK says ~ Aabar dekha hobey
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
