---
Title: pdf-parser
Homepage: https://blog.didierstevens.com/programs/pdf-tools/
Repository: https://gitlab.com/kalilinux/packages/pdf-parser
Architectures: all
Version: 0.7.8-0kali1
Metapackages: kali-linux-default kali-linux-everything kali-linux-headless kali-linux-large kali-tools-forensics kali-tools-respond 
Icon: images/pdf-parser-logo.svg
PackagesInfo: |
 ### pdf-parser
 
  This tool will parse a PDF document to identify the
  fundamental elements used in the analyzed file. It will not
  render a PDF document.
 
 **Installed size:** `85 KB`  
 **How to install:** `sudo apt install pdf-parser`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * zlib1g
 {{< /spoiler >}}
 
 ##### pdf-parser
 
 
 ```
 root@kali:~# pdf-parser -h
 This program has not been tested with this version of Python (3.11.6)
 Should you encounter problems, please use Python version 3.11.1
 Usage: pdf-parser [options] pdf-file|zip-file|url
 pdf-parser, use it to parse a PDF document
 
 Options:
   --version             show program's version number and exit
   -h, --help            show this help message and exit
   -m, --man             Print manual
   -s SEARCH, --search=SEARCH
                         string to search in indirect objects (except streams)
   -f, --filter          pass stream object through filters (FlateDecode,
                         ASCIIHexDecode, ASCII85Decode, LZWDecode and
                         RunLengthDecode only)
   -o OBJECT, --object=OBJECT
                         id(s) of indirect object(s) to select, use comma (,)
                         to separate ids (version independent)
   -r REFERENCE, --reference=REFERENCE
                         id of indirect object being referenced (version
                         independent)
   -e ELEMENTS, --elements=ELEMENTS
                         type of elements to select (cxtsi)
   -w, --raw             raw output for data and filters
   -a, --stats           display stats for pdf document
   -t TYPE, --type=TYPE  type of indirect object to select
   -O, --objstm          parse stream of /ObjStm objects
   -v, --verbose         display malformed PDF elements
   -x EXTRACT, --extract=EXTRACT
                         filename to extract malformed content to
   -H, --hash            display hash of objects
   -n, --nocanonicalizedoutput
                         do not canonicalize the output
   -d DUMP, --dump=DUMP  filename to dump stream content to
   -D, --debug           display debug info
   -c, --content         display the content for objects without streams or
                         with streams without filters
   --searchstream=SEARCHSTREAM
                         string to search in streams
   --unfiltered          search in unfiltered streams
   --casesensitive       case sensitive search in streams
   --regex               use regex to search in streams
   --overridingfilters=OVERRIDINGFILTERS
                         override filters with given filters (use raw for the
                         raw stream content)
   -g, --generate        generate a Python program that creates the parsed PDF
                         file
   --generateembedded=GENERATEEMBEDDED
                         generate a Python program that embeds the selected
                         indirect object as a file
   -y YARA, --yara=YARA  YARA rule (or directory or @file) to check streams
                         (can be used with option --unfiltered)
   --yarastrings         Print YARA strings
   --decoders=DECODERS   decoders to load (separate decoders with a comma , ;
                         @file supported)
   --decoderoptions=DECODEROPTIONS
                         options for the decoder
   -k KEY, --key=KEY     key to search in dictionaries
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## pdf-parser Usage Example

Display statistics (`-a`) for the given PDF file (`/usr/share/doc/texmf/fonts/lm/lm-info.pdf`):

```
root@kali:~# pdf-parser -a /usr/share/doc/texmf/fonts/lm/lm-info.pdf
Comment: 3
XREF: 1
Trailer: 1
StartXref: 1
Indirect object: 526
  282: 7, 8, 12, 17, 18, 27, 28, 30, 31, 34, 35, 43, 44, 78, 79, 111, 112, 120, 121, 123, 124, 126, 127, 129, 130, 132, 133, 135, 136, 138, 139, 141, 142, 144, 145, 155, 156, 158, 159, 164, 165, 168, 169, 172, 173, 176, 177, 179, 180, 183, 184, 187, 188, 191, 192, 2, 208, 209, 210, 211, 212, 213, 214, 215, 216, 217, 218, 219, 220, 221, 222, 223, 224, 225, 226, 227, 228, 229, 230, 231, 232, 233, 234, 235, 236, 237, 238, 239, 240, 241, 242, 243, 244, 245, 246, 247, 248, 249, 250, 251, 252, 253, 254, 255, 256, 257, 258, 259, 260, 261, 262, 263, 264, 265, 266, 267, 268, 269, 270, 271, 272, 273, 274, 275, 276, 277, 278, 279, 280, 281, 282, 283, 284, 285, 286, 287, 288, 289, 290, 291, 292, 293, 294, 295, 296, 297, 298, 299, 300, 301, 302, 303, 304, 305, 306, 307, 308, 309, 310, 311, 312, 313, 314, 315, 316, 317, 318, 319, 320, 321, 322, 323, 324, 325, 326, 327, 328, 329, 330, 331, 332, 333, 334, 335, 336, 337, 338, 339, 340, 341, 342, 343, 344, 345, 346, 347, 348, 349, 350, 351, 352, 353, 354, 355, 356, 357, 358, 359, 360, 361, 362, 363, 364, 365, 366, 367, 368, 369, 370, 371, 472, 473, 474, 475, 476, 477, 478, 479, 480, 481, 482, 484, 485, 486, 488, 489, 490, 492, 493, 494, 496, 497, 498, 500, 501, 502, 504, 505, 506, 508, 509, 510, 512, 513, 514, 516, 517, 518, 520, 521, 522, 524, 525, 526, 372, 374, 375, 383, 450, 451, 453, 454, 457, 458, 460, 461, 463, 464, 466, 467, 469, 470
 /Catalog 1: 1
 /Encoding 1: 10
 /ExtGState 1: 6
 /Font 105: 11, 4, 5, 14, 20, 21, 22, 23, 24, 25, 26, 33, 46, 47, 48, 49, 50, 51, 52, 53, 54, 55, 56, 57, 58, 59, 60, 61, 62, 63, 64, 65, 66, 67, 68, 69, 70, 71, 72, 73, 74, 75, 76, 77, 81, 82, 83, 84, 85, 86, 87, 88, 89, 90, 91, 92, 93, 94, 95, 96, 97, 98, 99, 100, 101, 102, 103, 104, 105, 106, 107, 108, 109, 110, 161, 162, 163, 167, 171, 175, 182, 186, 190, 15, 37, 39, 41, 114, 116, 118, 147, 149, 151, 153, 16, 38, 40, 42, 115, 117, 119, 148, 150, 152, 154
 /FontDescriptor 94: 9, 373, 376, 377, 378, 379, 380, 381, 382, 384, 385, 386, 387, 388, 389, 390, 391, 392, 393, 394, 395, 396, 397, 398, 399, 400, 401, 402, 403, 404, 405, 406, 407, 408, 409, 410, 411, 412, 413, 414, 415, 416, 417, 418, 419, 420, 421, 422, 423, 424, 425, 426, 427, 428, 429, 430, 431, 432, 433, 434, 435, 436, 437, 438, 439, 440, 441, 442, 443, 444, 445, 446, 447, 448, 449, 452, 455, 456, 459, 462, 465, 468, 471, 483, 487, 491, 495, 499, 503, 507, 511, 515, 519, 523
 /Page 26: 3, 19, 29, 32, 36, 45, 80, 113, 122, 125, 128, 131, 134, 137, 140, 143, 146, 157, 160, 166, 170, 174, 178, 181, 185, 189
 /Pages 15: 195, 196, 194, 198, 199, 200, 197, 202, 203, 201, 205, 206, 207, 204, 193
 /XObject 1: 13
```
