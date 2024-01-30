---
Title: zerofree
Homepage: https://frippery.org/uml/
Repository: https://salsa.debian.org/debian/zerofree
Architectures: any
Version: 1.1.1-1
Metapackages: kali-linux-everything kali-linux-large 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### zerofree
 
  Zerofree finds the unallocated blocks with non-zero value content in
  an ext2, ext3 or ext4 file-system and fills them with zeroes
  (zerofree can also work with another value than zero). This is mostly
  useful if the device on which this file-system resides is a disk
  image. In this case, depending on the type of disk image, a secondary
  utility may be able to reduce the size of the disk image after
  zerofree has been run. Zerofree requires the file-system to be
  unmounted or mounted read-only.
   
  The usual way to achieve the same result (zeroing the unused
  blocks) is to run "dd" to create a file full of zeroes that takes up
  the entire free space on the drive, and then delete this file. This
  has many disadvantages, which zerofree alleviates:
   * it is slow;
   * it makes the disk image (temporarily) grow to its maximal extent;
   * it (temporarily) uses all free space on the disk, so other
     concurrent write actions may fail.
   
  Zerofree has been written to be run from GNU/Linux systems installed
  as guest OSes inside a virtual machine. If this is not your case, you
  almost certainly don't need this package. (One other use case would
  be to erase sensitive data a little bit more securely than with a
  simple "rm").
 
 **Installed size:** `25 KB`  
 **How to install:** `sudo apt install zerofree`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libext2fs2 
 {{< /spoiler >}}
 
 ##### zerofree
 
 Zero free blocks from ext2, ext3 and ext4 file-systems
 
 ```
 root@kali:~# zerofree -h
 zerofree: invalid option -- 'h'
 usage: zerofree [-n] [-v] [-f fillval] filesystem
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
