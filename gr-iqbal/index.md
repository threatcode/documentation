---
Title: gr-iqbal
Homepage: https://git.osmocom.org/gr-iqbal
Repository: https://salsa.debian.org/bottoms/pkg-gr-iqbal
Architectures: any
Version: 0.38.2-2
Metapackages: kali-linux-everything kali-tools-sdr kali-tools-wireless 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### gr-iqbal
 
  The general idea is to suppress symmetrical images caused by IQ
  imbalance in the RX path of quadrature receivers.
  It's composed of two subblocks:
   
  "IQ Bal Fix": This applies the actual correction. to a complex
  stream. The correction parameters are only magnitude/phase and the
  actual correction algo is the same as applied in hardware in the USRP.
  You can either specify the correction parameters manually on the
  block, or send them via 'messages'.
   
  "IQ Bal Optimize": This blocks tries to blindly detect the imbalance
  by minimizing the correlation between the left and right part of the
  spectrum. See the code for the "how it does it". The general idea is
  inspired from papers found on the internet and the way some SDR
  software achieve the same things (sdr# for eg, although there are
  significant differences in the actual implementation).
 
 **Installed size:** `1.25 MB`  
 **How to install:** `sudo apt install gr-iqbal`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libgcc-s1 
 * libgnuradio-iqbalance3.9.0 
 * libgnuradio-runtime3.10.8 
 * libpython3.11 
 * libstdc++6 
 * python3
 * python3 
 * python3-numpy 
 * python3-numpy-abi9
 {{< /spoiler >}}
 
 
 - - -
 
 ### libgnuradio-iqbalance3.9.0
 
  The general idea is to suppress symmetrical images caused by IQ
  imbalance in the RX path of quadrature receivers.
  It's composed of two subblocks: "IQ Bal Fix" and "IQ Bal Optimize".
   
  This package provides a shared library for gr-iqbal.
 
 **Installed size:** `72 KB`  
 **How to install:** `sudo apt install libgnuradio-iqbalance3.9.0`  
 
 {{< spoiler "Dependencies:" >}}
 * libc6 
 * libfftw3-single3 
 * libgcc-s1 
 * libgnuradio-pmt3.10.8 
 * libgnuradio-runtime3.10.8 
 * libstdc++6 
 {{< /spoiler >}}
 
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
