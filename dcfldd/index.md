---
Title: dcfldd
Homepage: https://github.com/resurrecting-open-source-projects/dcfldd
Repository: https://salsa.debian.org/debian/dcfldd
Architectures: any
Version: 1.9.1-1
Metapackages: kali-linux-everything kali-linux-large kali-tools-forensics kali-tools-respond 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### dcfldd
 
  dcfldd was initially developed at Department of Defense Computer Forensics
  Lab (DCFL). This tool is based on the dd program with the following additional
  features:
   
   - Hashing on-the-fly: dcfldd can hash the input data as it is being
     transferred, helping to ensure data integrity.
   - Status output: dcfldd can update the user of its progress in terms of the
     amount of data transferred and how much longer operation will take.
   - Flexible disk wipes: dcfldd can be used to wipe disks quickly and with a
     known pattern if desired.
   - Image/wipe verify: dcfldd can verify that a target drive is a bit-for-bit
     match of the specified input file or pattern.
   - Multiple outputs: dcfldd can output to multiple files or disks at the same
     time.
   - Split output: dcfldd can split output to multiple files with more
     configurability than the split command.
   - Piped output and logs: dcfldd can send all its log data and output to
     commands as well as files natively.
   - When dd uses a default block size (bs, ibs, obs) of 512 bytes, dcfldd uses
     32768 bytes (32 KiB) which is HUGELY more efficient.
   - The following options are present in dcfldd but not in dd: ALGORITHMlog:,
     errlog, hash, hashconv, hashformat, hashlog, hashlog:, hashwindow, limit,
     of:, pattern, sizeprobe, split, splitformat, statusinterval, textpattern,
     totalhashformat, verifylog, verifylog:, vf.
 
 **Installed size:** `114 KB`  
 **How to install:** `sudo apt install dcfldd`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### dcfldd
 
 Enhanced version of dd for forensics and security
 
 ```
 root@kali:~# dcfldd --help
 Usage: dcfldd [OPTION]...
 Enhanced version of dd for forensics and security.
 
   bs=BYTES            force ibs=BYTES and obs=BYTES (default=32768)
   cbs=BYTES           convert BYTES bytes at a time
   conv=KEYWORDS       convert the file as per the comma separated keyword list
   count=BLOCKS        copy only BLOCKS input blocks
   limit=BYTES         similar to count but using BYTES instead of BLOCKS
   ibs=BYTES           read BYTES bytes at a time
   if=FILE             read from FILE instead of stdin
   obs=BYTES           write BYTES bytes at a time
   of=FILE             write to FILE instead of stdout
   of:=COMMAND         exec and write output to process COMMAND
   seek=BLOCKS         skip BLOCKS obs-sized blocks at start of output
   skip=BLOCKS         skip BLOCKS ibs-sized blocks at start of input
   pattern=HEX         use the specified binary pattern as input
   textpattern=TEXT    use repeating TEXT as input
   errlog=FILE         send error messages to FILE as well as stderr
   hash=NAME           do hash calculation (md5, sha1, sha256, sha384 or sha512)
   hashlog=FILE        send hash output to FILE instead of stderr
   hashwindow=BYTES    perform a hash on every BYTES amount of data
   hashlog:=COMMAND    exec and write hashlog to process COMMAND
   ALGORITHMlog:=COMMAND    also works in the same fashion of hashlog:=COMMAND
   hashconv=[before|after]  perform the hashing before or after the conversions
   hashformat=FORMAT        display each hashwindow according to FORMAT
   totalhashformat=FORMAT   display the total hash value according to FORMAT
   status=[on|off]          display a continual status message on stderr
   statusinterval=N         update the status message every N blocks
   sizeprobe=[if|of|BYTES]  what to use as value to percentage indicator
   split=BYTES              write every BYTES amount of data to a new file
   splitformat=[TEXT|MAC|WIN]  the file extension format for split operation
   vf=FILE                  verify that FILE matches the specified input
   verifylog=FILE           send verify results to FILE instead of stderr
   verifylog:=COMMAND       exec and write verify results to process COMMAND
   diffwr=[on|off]          only write to output if destination block content differs
 
   --help              display this help and exit
   --version           output version information and exit
 
 Read the manpage dcfldd(1) for more details about each option and to see
 some examples.
 
 Report bugs at
 https://github.com/resurrecting-open-source-projects/dcfldd/issues
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
