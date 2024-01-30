---
Title: libimage-exiftool-perl
Homepage: https://exiftool.org/
Repository: https://salsa.debian.org/perl-team/modules/packages/libimage-exiftool-perl
Architectures: all
Version: 12.67+dfsg-1
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### libimage-exiftool-perl
 
  Image::ExifTool is a customizable set of Perl modules plus a full-featured
  command-line application called exiftool for reading and writing meta
  information in a wide variety of files, including the maker note information
  of many digital cameras by various manufacturers such as Canon, Casio, DJI,
  FLIR, FujiFilm, GE, HP, JVC/Victor, Kodak, Leaf, Minolta/Konica-Minolta,
  Nikon, Nintendo, Olympus/Epson, Panasonic/Leica, Pentax/Asahi, Phase One,
  Reconyx, Ricoh, Samsung, Sanyo, Sigma/Foveon and Sony.
   
  The following modules/packages are recommended for specific features, e.g.
  decoding compressed and/or encrypted information from the indicated file
  types, calculating digest values for some information types, etc.:
   
   * Archive::Zip / libarchive-zip-perl: ZIP, DOCX, PPTX, XLSX, ODP, ODS, ODT,
     EIP, iWork
   * Unicode::LineBreak / libunicode-linebreak-perl: for column-alignment of
     alternate language output
   * POSIX::strptime / libposix-strptime-perl: for inverse date/time conversion
   * Time::Piece (in perl core): alternative to POSIX::strptime
   * IO::Compress::RawDeflate + IO::Uncompress::RawInflate (in perl core): for
     reading FLIF images
   * Compress::Raw::Lzma / libcompress-raw-lzma-perl: for reading encoded
     7z files
   * IO::Compress::Brotli + IO::Uncompress::Brotli / libio-compress-brotli-perl:
     for writing/reading compressed JXL metadata
 
 **Installed size:** `22.91 MB`  
 **How to install:** `sudo apt install libimage-exiftool-perl`  
 
 {{< spoiler "Dependencies:" >}}
 * perl
 {{< /spoiler >}}
 
 ##### exiftool
 
 Read and write meta information in files
 
 ```
 root@kali:~# exiftool -h
 Syntax:  exiftool [OPTIONS] FILE
 
 Consult the exiftool documentation for a full list of options.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
