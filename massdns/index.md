---
Title: massdns
Homepage: https://github.com/blechschmidt/massdns
Repository: https://gitlab.com/kalilinux/packages/massdns
Architectures: any
Version: 1.0.0-0kali1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### massdns
 
  This package contains a simple high-performance DNS stub resolver targeting
  those who seek to resolve a massive amount of domain names in the order of
  millions or even billions. Without special configuration, MassDNS is capable
  of resolving over 350,000 names per second using publicly available resolvers.
 
 **Installed size:** `101 KB`  
 **How to install:** `sudo apt install massdns`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### massdns
 
 
 ```
 root@kali:~# massdns -h
 Usage: massdns [options] [domainlist]
   -b  --bindto           Bind to IP address and port. (Default: 0.0.0.0:0)
       --busy-poll        Use busy-wait polling instead of epoll.
   -c  --resolve-count    Number of resolves for a name before giving up. (Default: 50)
       --drop-group       Group to drop privileges to when running as root. (Default: nogroup)
       --drop-user        User to drop privileges to when running as root. (Default: nobody)
       --filter           Only output packets with the specified response code.
       --flush            Flush the output file whenever a response was received.
   -h  --help             Show this help.
       --ignore           Do not output packets with the specified response code.
   -i  --interval         Interval in milliseconds to wait between multiple resolves of the same
                          domain. (Default: 500)
   -l  --error-log        Error log file path. (Default: /dev/stderr)
       --norecurse        Use non-recursive queries. Useful for DNS cache snooping.
   -o  --output           Flags for output formatting.
       --predictable      Use resolvers incrementally. Useful for resolver tests.
       --processes        Number of processes to be used for resolving. (Default: 1)
   -q  --quiet            Quiet mode.
       --rcvbuf           Size of the receive buffer in bytes.
       --retry            Unacceptable DNS response codes. (Default: REFUSED)
   -r  --resolvers        Text file containing DNS resolvers.
       --root             Do not drop privileges when running as root. Not recommended.
   -s  --hashmap-size     Number of concurrent lookups. (Default: 10000)
       --sndbuf           Size of the send buffer in bytes.
       --status-format    Format for real-time status updates, json or ansi (Default: ansi)
       --sticky           Do not switch the resolver when retrying.
       --socket-count     Socket count per process. (Default: 1)
   -t  --type             Record type to be resolved. (Default: A)
       --verify-ip        Verify IP addresses of incoming replies.
   -w  --outfile          Write to the specified output file instead of standard output.
 
 Output flags:
   S - simple text output
   F - full text output
   B - binary output
   J - ndjson output
 
 Advanced flags for the simple output mode:
   d - Include records from the additional section.
   i - Indent any reply record.
   l - Separate replies using a line feed.
   m - Only output reply records that match the question name.
   n - Include records from the answer section.
   q - Print the question.
   r - Print the question with resolver IP address, Unix timestamp and return code prepended.
   s - Separate packet sections using a line feed.
   t - Include TTL and record class within the output.
   u - Include records from the authority section.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
