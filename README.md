# scrcpy-android

- This application is android port to desktop applicaton [**Scrcpy**](https://github.com/Genymobile/scrcpy).

- This application mirrors display and touch controls from a remote android device to scrcpy-android device.

- scrcpy-android uses ADB-Connect interface to connect to android device to be mirrored.



## Download

[scrcpy-debug.apk](https://github.com/happyman/scrcpy-android/releases/tag/v0.1)


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

## JDK note

from https://github.com/huage2580/scrcpy-android/issues/4

```
# in WSL 2.0, Ubuntu 20.04
$ sudo apt install gradle openjdk-11-jdk
$ mkdir /mnt/c/Users/happyman/AndroidSdk/
# download sdkmanger .. from web site: https://developer.android.com/studio
# choose commandlinetools-linux-11076708_latest.zip
# extract to sdk directory /mnt/c/Users/happyman/AndroidSdk/cmdline-tools
# add env variables
$ echo "export ANDROID_SDK_ROOT=/mnt/c/Users/happyman/AndroidSdk/" >> ~/.bashrc
$ echo "export PATH=$PATH:ANDROID_SDK_ROOT/cmdline_tools/bin" >> ~/.bashrc
# re-enter bash
# choose /usr/lib/jvm/java-11-openjdk-amd64/bin/java   
$ sudo update-alternatives --config java
$ sdkmanager --sdk_root=/mnt/c/Users/happyman/AndroidSdk/ --update
$ sdkmanager --sdk_root=/mnt/c/Users/happyman/AndroidSdk/ "platforms;android-25" "build-tools;25.0.2" "extras;google;m2repository" "extras;android;m2repository"
$ sdkmanager --sdk_root=/mnt/c/Users/happyman/AndroidSdk/ --licenses

```
## Building with Gradle

    ./gradlew assembleDebug
    
    
 
## LICENSE

- scrcpy-android part is licensed under the GPLv3.

- The server part is licensed under the Apache License 2.0.
