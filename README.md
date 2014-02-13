Debugging Android Devices on Linux (Specifically Ubuntu 12) 
===============

To get your devices recognized by your unix distro you may need to authorize the device.  This file and mini-tutorial works for ubuntu, other distros and your mileage may vary ... 

1. If you already have a /etc/udev/rules.d/51-android.rules BACK IT UP
2. As ROOT (sudo) save the contents below to a file at /etc/udev/rules.d/51-android.rules 
3. Open a terminal 
4. sudo chmod a+r /etc/udev/rules.d/51-android.rules to allow read permission for all accounts 
5. reboot

You can also try to restart the udev server, kill and restart the adb server, then unplug and re-plug the usb cable but it's just easier to let the system handle it for you with a reboot
 
NOTES:
  Other distro's may require different files and internal commands but this should work on most systems
  On VirtualBox don't forget to attach the USB device (phone etc) at the menu else linux won't see it


Walk through at http://mofodv.com/debugging-android-devices-on-linux including how to add a missing mfg
===============

51-android.rules contents
---------------
```
#Acer
SUBSYSTEM=="usb", ATTRS{idVendor}=="0502", MODE="0660", GROUP="plugdev" 

#ASUS	
SUBSYSTEM=="usb", ATTRS{idVendor}=="0b05", MODE="0660", GROUP="plugdev" 

#Dell
SUBSYSTEM=="usb", ATTRS{idVendor}=="413c", MODE="0660", GROUP="plugdev" 

#Foxconn
SUBSYSTEM=="usb", ATTRS{idVendor}=="0489", MODE="0660", GROUP="plugdev" 

#Fujitsu/Fujitsu Toshiba
SUBSYSTEM=="usb", ATTRS{idVendor}=="04c5", MODE="0660", GROUP="plugdev" 

#Garmin-Asus
SUBSYSTEM=="usb", ATTRS{idVendor}=="091e", MODE="0660", GROUP="plugdev" 

#Google
SUBSYSTEM=="usb", ATTRS{idVendor}=="18d1", MODE="0660", GROUP="plugdev" 

#Haier
SUBSYSTEM=="usb", ATTRS{idVendor}=="201E", MODE="0660", GROUP="plugdev" 

#Hisense
SUBSYSTEM=="usb", ATTRS{idVendor}=="109b", MODE="0660", GROUP="plugdev" 

#HTC	
SUBSYSTEM=="usb", ATTRS{idVendor}=="0bb4", MODE="0660", GROUP="plugdev" 

#Huawei	
SUBSYSTEM=="usb", ATTRS{idVendor}=="12d1", MODE="0660", GROUP="plugdev" 

#K-Touch
SUBSYSTEM=="usb", ATTRS{idVendor}=="24e3", MODE="0660", GROUP="plugdev" 

#KT Tech	
SUBSYSTEM=="usb", ATTRS{idVendor}=="2116", MODE="0660", GROUP="plugdev" 

#Kyocera
SUBSYSTEM=="usb", ATTRS{idVendor}=="0482", MODE="0660", GROUP="plugdev" 

#Lenovo
SUBSYSTEM=="usb", ATTRS{idVendor}=="17ef", MODE="0660", GROUP="plugdev" 

#LG
SUBSYSTEM=="usb", ATTRS{idVendor}=="1004", MODE="0660", GROUP="plugdev" 

#Motorola
SUBSYSTEM=="usb", ATTRS{idVendor}=="22b8", MODE="0660", GROUP="plugdev" 

#MTK	
SUBSYSTEM=="usb", ATTRS{idVendor}=="0e8d", MODE="0660", GROUP="plugdev" 

#NEC	
SUBSYSTEM=="usb", ATTRS{idVendor}=="0409", MODE="0660", GROUP="plugdev" 

#Nook
SUBSYSTEM=="usb", ATTRS{idVendor}=="2080", MODE="0660", GROUP="plugdev" 

#Nvidia
SUBSYSTEM=="usb", ATTRS{idVendor}=="0955", MODE="0660", GROUP="plugdev" 

#OTGV
SUBSYSTEM=="usb", ATTRS{idVendor}=="2257", MODE="0660", GROUP="plugdev" 

#Pantech
SUBSYSTEM=="usb", ATTRS{idVendor}=="10a9", MODE="0660", GROUP="plugdev" 

#Pegatron
SUBSYSTEM=="usb", ATTRS{idVendor}=="1d4d", MODE="0660", GROUP="plugdev" 

#Philips
SUBSYSTEM=="usb", ATTRS{idVendor}=="0471", MODE="0660", GROUP="plugdev" 

#PMC-Sierra	
SUBSYSTEM=="usb", ATTRS{idVendor}=="04da", MODE="0660", GROUP="plugdev" 

#Qualcomm	
SUBSYSTEM=="usb", ATTRS{idVendor}=="05c6", MODE="0660", GROUP="plugdev" 

#SK Telesys	
SUBSYSTEM=="usb", ATTRS{idVendor}=="1f53", MODE="0660", GROUP="plugdev" 

#Samsung	
SUBSYSTEM=="usb", ATTRS{idVendor}=="04e8", MODE="0660", GROUP="plugdev" 

#Sharp	
SUBSYSTEM=="usb", ATTRS{idVendor}=="04dd", MODE="0660", GROUP="plugdev" 

#Sony	
SUBSYSTEM=="usb", ATTRS{idVendor}=="054c", MODE="0660", GROUP="plugdev" 

#Sony Ericsson
SUBSYSTEM=="usb", ATTRS{idVendor}=="0fce", MODE="0660", GROUP="plugdev" 

#Teleepoch
SUBSYSTEM=="usb", ATTRS{idVendor}=="2340", MODE="0660", GROUP="plugdev" 

#Toshiba
SUBSYSTEM=="usb", ATTRS{idVendor}=="0930", MODE="0660", GROUP="plugdev" 

#ZTE
SUBSYSTEM=="usb", ATTRS{idVendor}=="19d2", MODE="0660", GROUP="plugdev" 
```
