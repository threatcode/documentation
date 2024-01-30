---
Title: davtest
Homepage: https://github.com/cldrn/davtest
Repository: https://gitlab.com/kalilinux/packages/davtest
Architectures: all
Version: 1.2+git20230307.34d31db-0kali1
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-web 
Icon: images/davtest-logo.svg
PackagesInfo: |
 ### davtest
 
  DAVTest tests WebDAV enabled servers by uploading test
  executable files, and then (optionally) uploading files
  which allow for command execution or other actions directly
  on the target. It is meant for penetration testers to
  quickly and easily determine if enabled DAV services are
  exploitable.
 
 **Installed size:** `69 KB`  
 **How to install:** `sudo apt install davtest`  
 
 {{< spoiler "Dependencies:" >}}
 * libhttp-dav-perl
 * perl
 {{< /spoiler >}}
 
 ##### davtest
 
 
 ```
 root@kali:~# davtest -h
 ^^^^^^^^^^^^^^  ERROR ^^^^^^^^^^^^^^
 
 /usr/bin/davtest -url <url> [options]
 
  -auth+ 	Authorization (user:password)
  -realm+ Auth Realm
  -cleanup	delete everything uploaded when done
  -directory+	postfix portion of directory to create
  -debug+	DAV debug level 1-3 (2 & 3 log req/resp to /tmp/perldav_debug.txt)
  -move		PUT text files then MOVE to executable
  -copy		PUT text files then COPY to executable
  -nocreate 	don't create a directory
  -quiet	 	only print out summary
  -rand+ 	use this instead of a random string for filenames
  -sendbd+	send backdoors:
 			auto - for any succeeded test
 			ext - extension matching file name(s) in backdoors/ dir
  -uploadfile+	upload this file (requires -uploadloc)
  -uploadloc+	upload file to this relative location/name (requires -uploadfile)
  -url+		url of DAV location
 
 Example: /usr/bin/davtest -url http://localhost/davdir
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## davtest Usage Example

Scan the given WebDAV server (`-url http://192.168.1.209`):

```
root@kali:~# davtest -url http://192.168.1.209
********************************************************
 Testing DAV connection
OPEN        SUCCEED:        http://192.168.1.209
********************************************************
NOTE    Random string for this session: B0yG9nhdFS8gox
********************************************************
 Creating directory
MKCOL       SUCCEED:        Created http://192.168.1.209/DavTestDir_B0yG9nhdFS8gox
********************************************************
 Sending test files
PUT asp FAIL
PUT cgi FAIL
PUT txt SUCCEED:    http://192.168.1.209/DavTestDir_B0yG9nhdFS8gox/davtest_B0yG9nhdFS8gox.txt
PUT pl  SUCCEED:    http://192.168.1.209/DavTestDir_B0yG9nhdFS8gox/davtest_B0yG9nhdFS8gox.pl
PUT jsp SUCCEED:    http://192.168.1.209/DavTestDir_B0yG9nhdFS8gox/davtest_B0yG9nhdFS8gox.jsp
PUT cfm SUCCEED:    http://192.168.1.209/DavTestDir_B0yG9nhdFS8gox/davtest_B0yG9nhdFS8gox.cfm
PUT aspx    FAIL
PUT jhtml   SUCCEED:    http://192.168.1.209/DavTestDir_B0yG9nhdFS8gox/davtest_B0yG9nhdFS8gox.jhtml
PUT php SUCCEED:    http://192.168.1.209/DavTestDir_B0yG9nhdFS8gox/davtest_B0yG9nhdFS8gox.php
PUT html    SUCCEED:    http://192.168.1.209/DavTestDir_B0yG9nhdFS8gox/davtest_B0yG9nhdFS8gox.html
PUT shtml   FAIL
********************************************************
 Checking for test file execution
EXEC    txt SUCCEED:    http://192.168.1.209/DavTestDir_B0yG9nhdFS8gox/davtest_B0yG9nhdFS8gox.txt
EXEC    pl  FAIL
EXEC    jsp FAIL
EXEC    cfm FAIL
EXEC    jhtml   FAIL
EXEC    php FAIL
EXEC    html    SUCCEED:    http://192.168.1.209/DavTestDir_B0yG9nhdFS8gox/davtest_B0yG9nhdFS8gox.html

********************************************************
/usr/bin/davtest Summary:
Created: http://192.168.1.209/DavTestDir_B0yG9nhdFS8gox
PUT File: http://192.168.1.209/DavTestDir_B0yG9nhdFS8gox/davtest_B0yG9nhdFS8gox.txt
PUT File: http://192.168.1.209/DavTestDir_B0yG9nhdFS8gox/davtest_B0yG9nhdFS8gox.pl
PUT File: http://192.168.1.209/DavTestDir_B0yG9nhdFS8gox/davtest_B0yG9nhdFS8gox.jsp
PUT File: http://192.168.1.209/DavTestDir_B0yG9nhdFS8gox/davtest_B0yG9nhdFS8gox.cfm
PUT File: http://192.168.1.209/DavTestDir_B0yG9nhdFS8gox/davtest_B0yG9nhdFS8gox.jhtml
PUT File: http://192.168.1.209/DavTestDir_B0yG9nhdFS8gox/davtest_B0yG9nhdFS8gox.php
PUT File: http://192.168.1.209/DavTestDir_B0yG9nhdFS8gox/davtest_B0yG9nhdFS8gox.html
Executes: http://192.168.1.209/DavTestDir_B0yG9nhdFS8gox/davtest_B0yG9nhdFS8gox.txt
Executes: http://192.168.1.209/DavTestDir_B0yG9nhdFS8gox/davtest_B0yG9nhdFS8gox.html
```
