android-rules.d
===============

Android Linux USB rule.d file for debugging android devices

To get your devices recognized by your unix distro you may need to authorize the usb device.  This file and mini-tutorial works for ubuntu, other distros and your mileage may vary ... 

1. Grab the 51-android.rules file
2. open it with gedit (sudo gedit ... ) and make sure your mfg is there
3. If you cant find your mfg see http://mofodv.com/debugging-android-devices-on-linux for how to customize it
4. Save the file to /etc/udev/rules.d/51-android.rules
5. sudo chmod R+a /etc/udev/ruelst.d/51-android.rules
6. Reboot

You can also try to restart the udev server, kill and restart the adb server, then unplud and re-plug the usb cable but it's just easier to let the ssytem handle it for you

Other distro's may require different files and internal commands but this should work on most systems
