---
Title: memdump
Homepage: http://www.porcupine.org/forensics/tct.html
Repository: https://salsa.debian.org/pkg-security-team/memdump
Architectures: any
Version: 1.01-9
Metapackages: kali-linux-everything kali-linux-large kali-tools-forensics kali-tools-respond 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### memdump
 
  Program which dumps system memory to the standard output stream, skipping over
  holes in memory maps. By default, the program dumps the contents of physical
  memory.
   
  This program will not work if CONFIG_STRICT_DEVMEM is enabled in kernel. Since
  2.6 version, several kernels are enabling this option by default.
   
  memdump is useful in security tests and forensics investigations.
 
 **Installed size:** `44 KB`  
 **How to install:** `sudo apt install memdump`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 {{< /spoiler >}}
 
 ##### memdump
 
 Memory dumper
 
 ```
 root@kali:~# memdump -h
 memdump: invalid option -- 'h'
 memdump: usage: memdump [options]
   -b read_buffer_size     (default 0, use the system page size)
   -k                      (dump kernel memory instead of physical memory)
   -m map_file             (print memory map)
   -p memory_page_size     (default 0, use the system page size)
   -s memory_dump-size     (default 0, dump all memory)
   -v                      (verbose mode for debugging)
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
