---
Title: ddrescue
Homepage: http://www.garloff.de/kurt/linux/ddrescue/
Repository: https://gitlab.com/kalilinux/packages/ddrescue
Architectures: amd64 arm64
Version: 1.99.13-0kali1
Metapackages: kali-linux-everything kali-linux-large kali-tools-forensics kali-tools-recover kali-tools-respond 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### ddrescue
 
  When your disk has crashed and you try to copy it over to another one,
  standard Unix tools like cp, cat, and dd will abort on every I/O error,
  dd_rescue does not.
  It optimizes copying by using large blocks as long as no errors occur
  and falls back to smaller blocks. It supports reverse direction copying
  (to approach a bad spot from the top), sparse copying, preallocating
  space, splice zerocopy, and bypassing the kernel pagecache with O_DIRECT.
  dd_rescue provides safe deletion of data by overwriting files (or better
  partitions/disks) multiple times with fast random numbers.
  With the ddr_hash plugin, it supports calculating a hash value (such as
  a sha256sum) or an HMAC during copying.
 
 **Installed size:** `407 KB`  
 **How to install:** `sudo apt install ddrescue`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * liblzo2-2 
 * libssl3 
 {{< /spoiler >}}
 
 ##### dd_rescue
 
 Data recovery and protection tool
 
 ```
 root@kali:~# dd_rescue -h
 
 dd_rescue Version 1.99.13, kurt@garloff.de, GNU GPL v2/v3
  (DD_RESCUE_1_99_13)
  (compiled May 10 2023 19:21:14 by gcc (Debian 12.2.0-14) 12.2.0)
  (features: O_DIRECT dl/libfallocate fallocate splice fitrim xattr rdrnd avx2)
 dd_rescue is free software. It's protected by the terms of GNU GPL v2 or v3
  (at your option).
 dd_rescue copies data from one file (or device or pipe) to others.
 USAGE: dd_rescue [options] infile outfile
 Options: -s ipos    start position in  input file (default=0),
          -S opos    start position in output file (def=ipos),
          -b softbs  block size for copy operation (def=131072, 1048576 for -d),
          -B hardbs  fallback block size in case of errs (def=4096, 512 for -d),
          -e maxerr  exit after maxerr errors (def=0=infinite),
          -m maxxfer maximum amount of data to be transferred (def=0=inf),
          -M         avoid extending outfile,
          -x         count opos from the end of outfile (eXtend),
          -y syncsz  frequency of fsync calls in bytes (def=512*softbs),
          -l logfile name of a file to log errors and summary to (def=""),
          -o bbfile  name of a file to log bad blocks numbers (def=""),
          -r         reverse direction copy (def=forward),
          -R         repeatedly write same block (def if infile is /dev/zero),
          -t         truncate output file at start (def=no),
          -T         truncate output file at last pos (def=no),
          -u         undo writes by deleting outfile and issuing fstrim
          -d/D       use O_DIRECT for input/output (def=no),
          -k         use efficient in-kernel zerocopy splice,
          -P         use fallocate to preallocate target space,
          -L plug1[=par1[:par2]][,plug2[,..]]    load plugins,
          -w         abort on Write errors (def=no),
          -W         read target block and avoid Writes if identical (def=no),
          -a         detect zero-filled blocks and write spArsely (def=no),
          -A         Always write blocks, zeroed if err (def=no),
          -i         interactive: ask before overwriting data (def=no),
          -f         force: skip some sanity checks (def=no),
          -p         preserve: preserve ownership, perms, times, attrs (def=no),
          -C limit   rateControl: avoid xfer data faster than limit B/s
          -Y oname   Secondary output file (multiple possible),
          -F off[-off]r/rep[,off[-off]w/rep[,...]]  fault injection (hardbs off) r/w
          -q         quiet operation,
          -v         verbose operation,
          -c 0/1     switch off/on colors (def=auto),
          -V         display version and exit,
          -h         display this help and exit.
 Instead of infile, -z/Z SEED or -z/Z SEEDFILE may be specified, taking the PRNG
  from libc or frandom (RC4 based) as input. SEED = 0 means a time based seed;
  Using /dev/urandom as SEEDFILE gives good pseudo random numbers.
 Likewise, -3 SEED/SEEDFILE will overwrite ofile 3 times (r,ir,0, BSI M7.15).
  With -4 SEED/SEEDFILE you get an additional random pass (r,ir,r2,0).
  With -2 SEED/SEEDFILE you only get one random pass (r,0).
 
 Sizes may be given in units b(=512), k(=1024), M(=1024^2) or G(1024^3) bytes
 This program is useful to rescue data in case of I/O errors, because
  it does not normally abort or truncate the output.
 It may also help data protection by securely overwriting data.
 There are plugins for compression, hashing and encryption.
 Have a look a the man page for more details and long options.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## dd_rescue Usage Example

Start at position 100 of the input file (`-s 100 /var/log/messages`) and write, beginning at position 0 of the destination file (`-S 0 /tmp/ddrescue-out`):

```
root@kali:~# dd_rescue -s 100 /var/log/messages -S 0 /tmp/ddrescue-out
dd_rescue: (info): Using softbs=65536, hardbs=4096
dd_rescue: (info) expect to copy 1766kB from /var/log/messages
dd_rescue: (info): ipos:      1024.1k, opos:      1024.0k, xferd:      1024.0k
                   errs:      0, errxfer:         0.0k, succxfer:      1024.0k
             +curr.rate:  1122807kB/s, avg.rate:  1018906kB/s, avg.load:  0.0%
             >.......................-.................<  57%  ETA:  0:00:00
dd_rescue: (info): read /var/log/messages (1767.0k): EOF
dd_rescue: (info): Summary for /var/log/messages -> /tmp/ddrescue-out:
dd_rescue: (info): ipos:      1767.0k, opos:      1767.0k, xferd:      1767.0k
                   errs:      0, errxfer:         0.0k, succxfer:      1767.0k
             +curr.rate:   352945kB/s, avg.rate:   568151kB/s, avg.load:  0.0%
             >.......................-................-< 100%  ETA:  0:00:00
```
