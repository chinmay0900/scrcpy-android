# scrcpy-android

- This application is android port to desktop applicaton [**Scrcpy**](https://github.com/Genymobile/scrcpy).

- This application mirrors display and touch controls from a remote android device to scrcpy-android device.

- scrcpy-android uses ADB-Connect interface to connect to android device to be mirrored.



## Download

[scrcpy-release-v2.1.apk](https://github.com/chinmay0900/scrcpy-android/releases/)


## Instructions to use

- Make sure both devices are on same local network.

- Enable **ADB-connect/ADB-wireless/ADB over network** on the device to be mirrored. 

- Open scrcpy-android app and enter ip address of device to be mirrored.

- Select display parameters and bitrate from drop-down menu(1280x720 and 2Mbps works best).

- Set **Navbar** switch if the device to be mirrored has only hardware navigation buttons.

- Hit **start** button.

- Accept and trust(check always allow from this computer) the ADB connection prompt on target device(Some custom roms don't have this prompt).

- Thats all! You should be seeing the screen of remote android device.

- To wake up the remote device, **double tap anywhere on screen**.

- To put the remote device to sleep, **close proxmity sensor and double tap anywhere on the screen**. 

- To bring back the local android system navbar while mirroring the remote device, **swipe up from the bottom edge of screen**.


## Building with Gradle

    ./gradlew assembleDebug
    
    
 
## LICENSE

- scrcpy-android part is licensed under the GPLv3.

- The server part is licensed under the Apache License 2.0.
