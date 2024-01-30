---
Title: padbuster
Homepage: https://github.com/GDSSecurity/PadBuster
Repository: https://gitlab.com/kalilinux/packages/padbuster
Architectures: all
Version: 0.3.3+git20210818.50e4a3e-1kali1
Metapackages: kali-linux-everything kali-linux-large kali-tools-web 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### padbuster
 
  PadBuster is a Perl script for automating Padding Oracle
  Attacks. PadBuster provides the capability to decrypt
  arbitrary ciphertext, encrypt arbitrary plaintext, and
  perform automated response analysis to determine whether a
  request is vulnerable to padding oracle attacks.
 
 **Installed size:** `40 KB`  
 **How to install:** `sudo apt install padbuster`  
 
 {{< spoiler "Dependencies:" >}}
 * libcompress-raw-zlib-perl
 * libcrypt-ssleay-perl
 * libnet-ssleay-perl
 * libwww-perl
 * perl
 {{< /spoiler >}}
 
 ##### padbuster
 
 
 ```
 root@kali:~# padbuster -h
 Option headers requires an argument
     
     Use: padbuster URL EncryptedSample BlockSize [options]
 
   Where: URL = The target URL (and query string if applicable)
          EncryptedSample = The encrypted value you want to test. Must
                            also be present in the URL, PostData or a Cookie
          BlockSize = The block size being used by the algorithm
 
 Options:
 	 -auth [username:password]: HTTP Basic Authentication 
 	 -bruteforce: Perform brute force against the first block 
 	 -ciphertext [Bytes]: CipherText for Intermediate Bytes (Hex-Encoded)
          -cookies [HTTP Cookies]: Cookies (name1=value1; name2=value2)
          -encoding [0-4]: Encoding Format of Sample (Default 0)
                           0=Base64, 1=Lower HEX, 2=Upper HEX
                           3=.NET UrlToken, 4=WebSafe Base64
          -encodedtext [Encoded String]: Data to Encrypt (Encoded)
          -error [Error String]: Padding Error Message
          -headers [HTTP Headers]: Custom Headers (name1::value1;name2::value2)
 	 -interactive: Prompt for confirmation on decrypted bytes
 	 -intermediate [Bytes]: Intermediate Bytes for CipherText (Hex-Encoded)
 	 -log: Generate log files (creates folder PadBuster.DDMMYY)
 	 -noencode: Do not URL-encode the payload (encoded by default)
 	 -noiv: Sample does not include IV (decrypt first block) 
          -plaintext [String]: Plain-Text to Encrypt
          -post [Post Data]: HTTP Post Data String
 	 -prefix [Prefix]: Prefix bytes to append to each sample (Encoded) 
 	 -proxy [address:port]: Use HTTP/S Proxy
 	 -proxyauth [username:password]: Proxy Authentication
 	 -resume [Block Number]: Resume at this block number
 	 -usebody: Use response body content for response analysis phase
          -verbose: Be Verbose
          -veryverbose: Be Very Verbose (Debug Only)
          
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
