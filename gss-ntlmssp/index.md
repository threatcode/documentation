---
Title: gss-ntlmssp
Homepage: https://github.com/gssapi/gss-ntlmssp/
Repository: https://salsa.debian.org/freeipa-team/gss-ntlmssp
Architectures: any
Version: 1.2.0-1
Metapackages: 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### gss-ntlmssp
 
  GSS-NTLMSSP is a GSSAPI mechanism plugin that implements NTLMSSP.
  NTLMSSP is a Microsoft Security Provider that implements various
  versions and falvors of the NTLM challenge-response family.
   
  GSS-NTLMSSP, implements both NTLM and NTLMv2 and all the various
  security variants to the key exchange that Microsoft introduced and
  documented over time.
   
  This code implements the NTLMSSP mechanism as a GSSAPI loadable
  mechanism and has been tested to work with MIT Kerberos' 1.11
  implementation of GSSAPI.
   
  This package supplies the MIT GSSAPI plugin.
 
 **Installed size:** `157 KB`  
 **How to install:** `sudo apt install gss-ntlmssp`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libgssapi-krb5-2 
 * libssl3 
 * libunistring5 
 * libwbclient0 
 * zlib1g 
 {{< /spoiler >}}
 
 
 - - -
 
 ### gss-ntlmssp-dev
 
  GSS-NTLMSSP is a GSSAPI mechanism plugin that implements NTLMSSP.
  NTLMSSP is a Microsoft Security Provider that implements various
  versions and falvors of the NTLM challenge-response family.
   
  GSS-NTLMSSP, implements both NTLM and NTLMv2 and all the various
  security variants to the key exchange that Microsoft introduced and
  documented over time.
   
  This code implements the NTLMSSP mechanism as a GSSAPI loadable
  mechanism and has been tested to work with MIT Kerberos' 1.11
  implementation of GSSAPI.
   
  This package supplies the development header.
 
 **Installed size:** `16 KB`  
 **How to install:** `sudo apt install gss-ntlmssp-dev`  
 
 {{< spoiler "Dependencies:" >}}
 * gss-ntlmssp 
 {{< /spoiler >}}
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
