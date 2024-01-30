---
Title: blueranger
Homepage: http://www.hackfromacave.com/projects/blueranger.html
Repository: https://gitlab.com/kalilinux/packages/blueranger
Architectures: any
Version: 0.1-1kali6
Metapackages: kali-linux-everything kali-linux-large kali-tools-bluetooth kali-tools-wireless 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### blueranger
 
  BlueRanger is a simple Bash script which uses Link
  Quality to locate Bluetooth device radios. It sends
  l2cap (Bluetooth) pings to create a connection
  between Bluetooth interfaces, since most devices
  allow pings without any authentication or
  authorization. The higher the link quality, the
  closer the device (in theory).
   
  Use a Bluetooth Class 1 adapter for long range
  location detection. Switch to a Class 3 adapter
  for more precise short range locating. The
  precision and accuracy depend on the build quality
  of the Bluetooth adapter, interference, and response
  from the remote device. Fluctuations may occur even
  when neither device is in motion.
 
 **Installed size:** `13 KB`  
 **How to install:** `sudo apt install blueranger`  
 
 ##### blueranger
 
 
 ```
 root@kali:~# blueranger -h
 
 BlueRanger 1.0 by JP Dunning (.ronin) 
 <www.hackfromacave.com>
 (c) 2009-2012 Shadow Cave LLC.
 
 NAME
 	blueranger
 
 SYNOPSIS
         /usr/bin/blueranger <hciX> <bdaddr>
 
 DESCRIPTION
 	<hciX>         Local interface
 	<bdaddr>       Remote Device Address
 
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}

## blueranger Usage Example

Use the Bluetooth interface (`hci1`) to scan for the specified remote address (`20:C9:D0:43:4B:D8`):

```
root@kali:~# blueranger hci1 20:C9:D0:43:4B:D8

Starting ...

Close with 2 X Crtl+C


      (((B(l(u(e(R)a)n)g)e)r)))

By JP Dunning (.ronin)
www.hackfromacave.com

Locating: ares (20:C9:D0:43:4B:D8)
Ping Count: 1

Proximity Change    Link Quality
----------------    ------------
FOUND           255/255

Range
------------------------------------
|*
------------------------------------
```
