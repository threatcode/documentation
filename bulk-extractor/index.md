---
Title: bulk-extractor
Homepage: https://github.com/simsong/bulk_extractor
Repository: https://gitlab.com/kalilinux/packages/bulk-extractor
Architectures: amd64 arm64
Version: 2.0.3-0kali1
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-forensics kali-tools-respond 
Icon: images/bulk-extractor-logo.svg
PackagesInfo: |
 ### bulk-extractor
 
  bulk_extractor is a C++ program that scans a disk image, a file,
  or a directory of files and extracts useful information without
  parsing the file system or file system structures. The results are
  stored in feature files that can be easily inspected, parsed, or
  processed with automated tools. bulk_extractor also creates
  histograms of features that it finds, as features that are more
  common tend to be more important.
 
 **Installed size:** `19.52 MB`  
 **How to install:** `sudo apt install bulk-extractor`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libewf2 
 * libexpat1 
 * libgcc-s1 
 * libgcrypt20 
 * libstdc++6 
 * zlib1g 
 {{< /spoiler >}}
 
 ##### bulk_extractor
 
 Scans a disk image for regular expressions and other content.
 
 ```
 root@kali:~# bulk_extractor -h
 bulk_extractor version 2.0.3: A high-performance flexible digital forensics program.
 Usage:
   bulk_extractor [OPTION...] image_name
 
   -A, --offset_add arg          Offset added (in bytes) to feature locations 
                                 (default: 0)
   -b, --banner_file arg         Path of file whose contents are prepended to 
                                 top of all feature files
   -C, --context_window arg      Size of context window reported in bytes 
                                 (default: 16)
   -d, --debug arg               enable debugging (default: 1)
   -D, --debug_help              help on debugging
   -E, --enable_exclusive arg    disable all scanners except the one specified. 
                                 Same as -x all -E scanner.
   -e, --enable arg              enable a scanner (can be repeated)
   -x, --disable arg             disable a scanner (can be repeated)
   -f, --find arg                search for a pattern (can be repeated)
   -F, --find_file arg           read patterns to search from a file (can be 
                                 repeated)
   -G, --pagesize arg            page size in bytes (default: 16777216)
   -g, --marginsize arg          margin size in bytes (default: 4194304)
   -j, --threads arg             number of threads (default: 8)
   -J, --no_threads              read and process data in the primary thread
   -M, --max_depth arg           max recursion depth (default: 12)
       --max_bad_alloc_errors arg
                                 max bad allocation errors (default: 3)
       --max_minute_wait arg     maximum number of minutes to wait until all 
                                 data are read (default: 60)
       --notify_main_thread      Display notifications in the main thread after 
                                 phase1 completes. Useful for running with 
                                 ThreadSanitizer
       --notify_async            Display notificaitons asynchronously (default)
   -o, --outdir arg              output directory [REQUIRED]
   -P, --scanner_dir arg         directories for scanner shared libraries (can 
                                 be repeated). Default directories include 
                                 /usr/local/lib/bulk_extractor, 
                                 /usr/lib/bulk_extractor and any directories 
                                 specified in the BE_PATH environment variable.
   -p, --path arg                print the value of <path>[:length][/h][/r] with 
                                 optional length, hex output, or raw output.
   -q, --quit                    no status or performance output
   -r, --alert_list arg          file to read alert list from
   -R, --recurse                 treat image file as a directory to recursively 
                                 explore
   -S, --set arg                 set a name=value option (can be repeated)
   -s, --sampling arg            random sampling parameter frac[:passes]
   -V, --version                 Display PACKAGE_VERSION (currently) 2.0.3
   -w, --stop_list arg           file to read stop list from
   -Y, --scan arg                specify <start>[-end] of area on disk to scan
   -z, --page_start arg          specify a starting page number
   -Z, --zap                     wipe the output directory (recursively) before 
                                 starting
   -0, --no_notify               disable real-time notification
   -1, --version1                version 1.0 notification (console-output)
   -H, --info_scanners           report information about each scanner
   -h, --help                    print help screen
 
 Global config options: 
    -S notify_rate=1    seconds between notificaiton update (notify_rate)
    -S debug_histogram_malloc_fail_frequency=0    Set >0 to make histogram maker fail with memory allocations (debug_histogram_malloc_fail_frequency)
    -S hash_alg=sha1    Specifies hash algorithm to be used for all hash calculations (hash_alg)
    -S report_read_errors=1    Report read errors (report_read_errors)
 
 These scanners enabled; disable with -x:
    -x accts - disable scanner accts
      -S ssn_mode=0    0=Normal; 1=No `SSN' required; 2=No dashes required
      -S min_phone_digits=7    Min. digits required in a phone
    -x aes - disable scanner aes
      -S scan_aes_128=1    Scan for 128-bit AES keys; 0=No, 1=Yes
      -S scan_aes_192=0    Scan for 192-bit AES keys; 0=No, 1=Yes
      -S scan_aes_256=1    Scan for 256-bit AES keys; 0=No, 1=Yes
    -x base64 - disable scanner base64
    -x elf - disable scanner elf
    -x email - disable scanner email
    -x evtx - disable scanner evtx
    -x exif - disable scanner exif
      -S exif_debug=0    debug exif decoder
    -x facebook - disable scanner facebook
    -x find - disable scanner find
    -x gps - disable scanner gps
    -x gzip - disable scanner gzip
      -S gzip_max_uncompr_size=268435456    maximum size for decompressing GZIP objects
    -x httplogs - disable scanner httplogs
    -x json - disable scanner json
    -x kml_carved - disable scanner kml_carved
    -x msxml - disable scanner msxml
    -x net - disable scanner net
      -S carve_net_memory=0    Carve network  memory structures
      -S min_carve_packet_bytes=40    Smallest network packet to carve
    -x ntfsindx - disable scanner ntfsindx
    -x ntfslogfile - disable scanner ntfslogfile
    -x ntfsmft - disable scanner ntfsmft
    -x ntfsusn - disable scanner ntfsusn
    -x pdf - disable scanner pdf
      -S pdf_dump_hex=0    Dump the contents of PDF buffers as hex
      -S pdf_dump_text=0    Dump the contents of PDF buffers showing extracted text
    -x rar - disable scanner rar
      -S rar_find_components=1    Search for RAR components
      -S rar_find_volumes=1    Search for RAR volumes
    -x sqlite - disable scanner sqlite
    -x utmp - disable scanner utmp
    -x vcard_carved - disable scanner vcard_carved
    -x windirs - disable scanner windirs
      -S opt_weird_file_size=157286400    Threshold for FAT32 scanner
      -S opt_weird_file_size2=536870912    Threshold for FAT32 scanner
      -S opt_weird_cluster_count=67108864    Threshold for FAT32 scanner
      -S opt_weird_cluster_count2=268435456    Threshold for FAT32 scanner
      -S opt_max_bits_in_attrib=3    Ignore FAT32 entries with more attributes set than this
      -S opt_max_weird_count=2    Number of 'weird' counts to ignore a FAT32 entry
      -S opt_last_year=2028    Ignore FAT32 entries with a later year than this
    -x winlnk - disable scanner winlnk
    -x winpe - disable scanner winpe
    -x winprefetch - disable scanner winprefetch
    -x zip - disable scanner zip
      -S zip_min_uncompr_size=6    Minimum size of a ZIP uncompressed object
      -S zip_max_uncompr_size=268435456    Maximum size of a ZIP uncompressed object
      -S zip_name_len_max=1024    Maximum name of a ZIP component filename
 These scanners disabled; enable with -e:
    -e base16 - enable scanner base16
    -e hiberfile - enable scanner hiberfile
    -e outlook - enable scanner outlook
    -e wordlist - enable scanner wordlist
      -S word_min=6    Minimum word size
      -S word_max=16    Maximum word size
      -S max_output_file_size=100000000    Maximum size of the words output file
      -S strings=0    Scan for strings instead of words
    -e xor - enable scanner xor
      -S xor_mask=255    XOR mask value, in decimal
 ```
 
 - - -
 
 ##### test_be
 
 
 ```
 root@kali:~# test_be -h
 
 Catch v2.13.6
 usage:
   test_be [<test name|pattern|tags> ... ] options
 
 where options are:
   -?, -h, --help                            display usage information
   -l, --list-tests                          list all/matching test cases
   -t, --list-tags                           list all/matching tags
   -s, --success                             include successful tests in
                                             output
   -b, --break                               break into debugger on failure
   -e, --nothrow                             skip exception tests
   -i, --invisibles                          show invisibles (tabs, newlines)
   -o, --out <filename>                      output filename
   -r, --reporter <name>                     reporter to use (defaults to
                                             console)
   -n, --name <name>                         suite name
   -a, --abort                               abort at first failure
   -x, --abortx <no. failures>               abort after x failures
   -w, --warn <warning name>                 enable warnings
   -d, --durations <yes|no>                  show test durations
   -D, --min-duration <seconds>              show test durations for tests
                                             taking at least the given number
                                             of seconds
   -f, --input-file <filename>               load test names to run from a
                                             file
   -#, --filenames-as-tags                   adds a tag for the filename
   -c, --section <section name>              specify section to run
   -v, --verbosity <quiet|normal|high>       set output verbosity
   --list-test-names-only                    list all/matching test cases
                                             names only
   --list-reporters                          list all reporters
   --order <decl|lex|rand>                   test case order (defaults to
                                             decl)
   --rng-seed <'time'|number>                set a specific seed for random
                                             numbers
   --use-colour <yes|no>                     should output be colourised
   --libidentify                             report name and version according
                                             to libidentify standard
   --wait-for-keypress <never|start|exit     waits for a keypress before
   |both>                                    exiting
   --benchmark-samples <samples>             number of samples to collect
                                             (default: 100)
   --benchmark-resamples <resamples>         number of resamples for the
                                             bootstrap (default: 100000)
   --benchmark-confidence-interval           confidence interval for the
   <confidence interval>                     bootstrap (between 0 and 1,
                                             default: 0.95)
   --benchmark-no-analysis                   perform only measurements; do not
                                             perform any analysis
   --benchmark-warmup-time                   amount of time in milliseconds
   <benchmarkWarmupTime>                     spent on warming up each test
                                             (default: 100)
 
 For more detailed usage please see the project docs
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## bulk_extractor Usage Example

Extract files to the output directory (`-o bulk-out`) after analyzing the image file (`xp-laptop-2005-07-04-1430.img`):

```
root@kali:~# bulk_extractor -o bulk-out xp-laptop-2005-07-04-1430.img
bulk_extractor version: 1.3
Hostname: kali
Input file: xp-laptop-2005-07-04-1430.img
Output directory: bulk-out
Disk Size: 536715264
Threads: 1
Phase 1.
13:02:46 Offset 0MB (0.00%) Done in n/a at 13:02:45
13:03:39 Offset 67MB (12.50%) Done in  0:06:14 at 13:09:53
13:04:43 Offset 134MB (25.01%) Done in  0:05:50 at 13:10:33
13:04:55 Offset 201MB (37.51%) Done in  0:03:36 at 13:08:31
13:06:01 Offset 268MB (50.01%) Done in  0:03:15 at 13:09:16
13:06:48 Offset 335MB (62.52%) Done in  0:02:25 at 13:09:13
13:07:04 Offset 402MB (75.02%) Done in  0:01:25 at 13:08:29
13:07:20 Offset 469MB (87.53%) Done in  0:00:39 at 13:07:59
All Data is Read; waiting for threads to finish...
Time elapsed waiting for 1 thread to finish:
     (please wait for another 60 min .)
Time elapsed waiting for 1 thread to finish:
    6 sec (please wait for another 59 min 54 sec.)
Thread 0: Processing 520093696

Time elapsed waiting for 1 thread to finish:
    12 sec (please wait for another 59 min 48 sec.)
Thread 0: Processing 520093696

Time elapsed waiting for 1 thread to finish:
    18 sec (please wait for another 59 min 42 sec.)
Thread 0: Processing 520093696

Time elapsed waiting for 1 thread to finish:
    24 sec (please wait for another 59 min 36 sec.)
Thread 0: Processing 520093696

Time elapsed waiting for 1 thread to finish:
    30 sec (please wait for another 59 min 30 sec.)
Thread 0: Processing 520093696

All Threads Finished!
Producer time spent waiting: 335.984 sec.
Average consumer time spent waiting: 0.143353 sec.
*******************************************
** bulk_extractor is probably CPU bound. **
**    Run on a computer with more cores  **
**      to get better performance.       **
*******************************************
Phase 2. Shutting down scanners
Phase 3. Creating Histograms
   ccn histogram...   ccn_track2 histogram...   domain histogram...
   email histogram...   ether histogram...   find histogram...
   ip histogram...   tcp histogram...   telephone histogram...
   url histogram...   url microsoft-live...   url services...
   url facebook-address...   url facebook-id...   url searches...

Elapsed time: 378.5 sec.
Overall performance: 1.418 MBytes/sec.
Total email features found: 899
```
