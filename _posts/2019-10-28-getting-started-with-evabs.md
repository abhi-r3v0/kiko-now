---
layout: post
title: "[PART 1] Getting Started with EVABS "
tags: [EVABS]

---

## Introduction
In this blog post, we'll see how we can kickstart learning Android security in a CTF approach.

### What are CTFs?
CTF stands for 'Capture The Flag' which is basically gamifying and making the learning process more intuitive and fun. In a CTF, a user is given intentionally vulnerable softwares/hardwares. The 'software/hardware' mentioned here includes, but is not limited to:

* Web applications
* Programs/executables
* Images/video/audio files
* Mobile applications
* IoT devices

The user then uses his skills and exploits the vulnerability and finds the 'flag'. A flag is usually a random text with/without a pre-defined pattern. For example, all the flags for EVABS are of the format ```EVABS{s0m3_rand0m_t3xt_h3r3}```. The flow of a CTF goes like this:

* Identifying the vulnerability
* Exploiting the vulnerability
* Capturing the flags and submitting them for points/rewards

An example of a CTF can be found here: [Pico CTF](https://picoctf.com/)

### What is EVABS?
EVABS - Extremely Vulnerable Android Labs is a CTF-style, Android application that has many known native vulnerabilities embedded in it. It can be installed in Android devices that run 4.4 (Kitkat) and above. The project is open sourced at this [GitHub](https://github.com/abhi-r3v0/EVABS) repository. 

### Why EVABS?
1. The advantage of CTF-style approach is that the user gets to verify if he successfully exploited a particular service/application/program or not, by getting a flag and submitting it to a flag verifying service online.
2. EVABS is finely crafted to match the requirements of a beginner. EVABS is divided into 12 levels and with each level, the difficulty linearly increases and user learns a new kind of attack.
3. The vulnerabilities in EVABS replicate real-world vulnerabilties. This helps people focusing on bug bounty/CTFs as well.
4. EVABS is open source. This means it can be used as a medium to understand how not to write a piece of code :)

---
## Requirements and Environment Setup
#### Must Have
* A rooted device or emulator. A rooted device is recommended
    - For a rooted device, one of the below devices are recommended
  
      | __Device__  |  __make__  | 
      |-------------|------------|
      | Moto G5/6   | Motorola   | 
      | Pixel       | Google     |
      | 3/3T/5/5T   | OnePlus    |
      
      Any other device of your choice could be used, provided, they have `root` available. You can check if your device can be rooted easily by Googling.
      
    - If you're choosig an emulator, either you can use [Genymotion](https://www.genymotion.com/fun-zone/) or use the default Android emulator shipped with the [Android SDK](https://developer.android.com/studio/run/managing-avds). You can also use any emulator of your choice as well. 

* Android platform tools
  - On Linux:
    - `sudo apt-get install android-tools-adb`
  - On Mac:
    - `brew cask install android-platform-tools`
    
* Java
* Mac/linux operating system recomended

#### Recommended
* Android Studio
* Android SDK
* Sublime Text Editor
* [Adhrit](https://github.com/abhi-r3v0/Adhrit)

### Checking Setup

* Cheking for Java:
`java --version`
* Cheking ADB
`adb --version`

---
## Installation

### Installing the APK file from Android device

* Head to the EVABS repository [here](https://github.com/abhi-r3v0/EVABS) and dowload the APK file `EVABS v1.1.apk` or directly download the APK file [EVABS v1.1.apk](https://github.com/abhi-r3v0/EVABS/blob/master/EVABSv1.1.apk) from phone browser
* Allow APK installation from [unkown sources in device settings](https://android.gadgethacks.com/how-to/android-basics-enable-unknown-sources-sideload-apps-0161947/)
* Click on the donwloaded APK file and install the app

### Installing the APK using ADB (phone/emulator)

* Head to the EVABS repository [here](https://github.com/abhi-r3v0/EVABS) and dowload the APK file `EVABS v1.1.apk` or directly download the APK file [EVABS v1.1.apk](https://github.com/abhi-r3v0/EVABS/blob/master/EVABSv1.1.apk)
* Enable [USB Debugging](https://www.embarcadero.com/starthere/xe5/mobdevsetup/android/en/enabling_usb_debugging_on_an_android_device.html) in your device
* Connect the device via USB. If you are using an emulator, skip this step. Instead, start the emulator.
* Try:
    `adb devices`
    
    This should list your connected device. If you are connecting your device for the first time, allow the computer by confirming the message that would pop-up on the device.

* Install the APK 
    `adb install -r path/to/EVABSv1.1.apk`
    
    You will receive a success message if the installation completes.
    
### Building Locally

* Head to the EVABS repository [here](https://github.com/abhi-r3v0/EVABS) and either clone the repository or download as a zip file.
* Extract the zip file to your `Android Studio Projects` directory.
    `unzip EVABS-master.zip path/to/AndroidStudioProjects`
* Fire up Android Studio and navigate to **File - Open** and select the extracted project directory. This will open the project. 
* Deploying 
  - Running the app without generating a signed APK
    - Click on **Run** and EVABS will be deployed in the connected device/emulator. 
    
  - Building a signed APK
    - Navigate to **Build - Generate Signed APK**. Create a new signature if you haven't created already. Sign the APK (v2 recommended) as **release**. You'll find the APK file as `AndroidStudioProjects/EVABS-master/app/release/app-release.apk`
    - Install this APK with ADB as discussed in the earlier section.
    
## Conclusion

This winds up the basic setup procedure. As we start completing labs, we will be installing the other necessary tools so that the context of the tool is understood. proceed to PART 2 to continue.
