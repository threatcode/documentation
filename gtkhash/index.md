---
Title: gtkhash
Homepage: https://gtkhash.org
Repository: https://salsa.debian.org/debian/gtkhash
Architectures: any
Version: 1.5-1
Metapackages: kali-linux-everything kali-linux-nethunter 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### caja-gtkhash
 
  The GtkHash extension for caja which allows users to compute
  message digests or checksums using the mhash library.
  Currently supported hash functions include MD5, MD6, SHA1,
  SHA256, SHA512, RIPEMD, TIGER and WHIRLPOOL.
 
 **Installed size:** `89 KB`  
 **How to install:** `sudo apt install caja-gtkhash`  
 
 {{< spoiler "Dependencies:" >}}
 * gtkhash 
 * libb2-1 
 * libc6 
 * libcaja-extension1 
 * libgcrypt20 
 * libglib2.0-0 
 * libgtk-3-0 
 * libnettle8
 * zlib1g 
 {{< /spoiler >}}
 
 
 - - -
 
 ### gtkhash
 
  GtkHash is a small GTK+ utility which allows users to compute
  message digests or checksums using the mhash library.
  Currently supported hash functions include MD5, MD6, SHA1,
  SHA256, SHA512, RIPEMD, TIGER and WHIRLPOOL.
 
 **Installed size:** `497 KB`  
 **How to install:** `sudo apt install gtkhash`  
 
 {{< spoiler "Dependencies:" >}}
 * dconf-gsettings-backend | gsettings-backend
 * libb2-1 
 * libc6 
 * libgcrypt20 
 * libglib2.0-0 
 * libgtk-3-0 
 * libnettle8
 * zlib1g 
 {{< /spoiler >}}
 
 ##### gtkhash
 
 A GTK+ utility for computing checksums and more
 
 ```
 root@kali:~# gtkhash -h
 Usage:
   gtkhash [OPTION?] [FILE|URI...]
 
 Help Options:
   -h, --help                    Show help options
   --help-all                    Show all help options
   --help-gtk                    Show GTK+ Options
 
 Application Options:
   -c, --check=DIGEST            Check against the specified digest or checksum
   -C, --check-file=FILE|URI     Check digests or checksums from the specified file
   -f, --function=FUNCTION       Enable the specified Hash Function (e.g. MD5)
   -t, --text=TEXT               Hash the specified text
   -v, --version                 Show version information
   --display=DISPLAY             X display to use
 
 ```
 
 - - -
 
 ### nemo-gtkhash
 
  The GtkHash extension for nemo which allows users to compute
  message digests or checksums using the mhash library.
  Currently supported hash functions include MD5, MD6, SHA1,
  SHA256, SHA512, RIPEMD, TIGER and WHIRLPOOL.
 
 **Installed size:** `83 KB`  
 **How to install:** `sudo apt install nemo-gtkhash`  
 
 {{< spoiler "Dependencies:" >}}
 * gtkhash 
 * libb2-1 
 * libc6 
 * libgcrypt20 
 * libglib2.0-0 
 * libgtk-3-0 
 * libnemo-extension1 
 * libnettle8
 * zlib1g 
 {{< /spoiler >}}
 
 
 - - -
 
 ### thunar-gtkhash
 
  The GtkHash extension for thunar which allows users to compute
  message digests or checksums using the mhash library.
  Currently supported hash functions include MD5, MD6, SHA1,
  SHA256, SHA512, RIPEMD, TIGER and WHIRLPOOL.
 
 **Installed size:** `82 KB`  
 **How to install:** `sudo apt install thunar-gtkhash`  
 
 {{< spoiler "Dependencies:" >}}
 * gtkhash 
 * libb2-1 
 * libc6 
 * libgcrypt20 
 * libglib2.0-0 
 * libgtk-3-0 
 * libnettle8
 * libthunarx-3-0 
 * zlib1g 
 {{< /spoiler >}}
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
