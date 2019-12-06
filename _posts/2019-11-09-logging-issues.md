---
layout: post
title: "[PART 3] Level 1: Debug Me - Android Logging Issues"
tags: [EVABS]

---

In this post, we'll be solving our first EVABS level: **Debug**, which deals with the sensitive data logging issues in Android applications.

**Level: 1**
**Points: 10**
**Difficulty: Easy**

## Preface

[**Logging**](https://developer.android.com/reference/android/util/Log) is a generic feature that has been in use in software development life cycles for many years. They are important to understand what is happening in the background of a running software. Logs also provide essential intel while identifying issues/errors.  

Android also provides this feature using which you can test your application's working and debug it incase you find any issues. Android provides a tool called the **ADB (Android Debug Bridge)** which is a tool that can be installed on your computer (which you might have already done by now from the [first part](https://www.hawkspawn.com/blog/getting-started-with-evabs/) of this series) running Windows/Mac/Linux. ADB also ships with the default Android SDK that can be downloaded from the official [Android Studio](https://developer.android.com/studio) web page.

## Understanding The Issue

Let's fire up EVABS and navigate to `Challenges`. Select `Debug Me`. It Looks, something like this:

As you can see, there are two buttons `LOG THE KEY` and `HINT`.

Clicking `LOG THE KEY` gives us a message:

```
SYS_CTRL_FAILURE: The developer was not supposed to log important data. Your secret key has been logged

```

Let's also take a look at the hint

```
How do you find the log of running apps in an Android device using ADB?
```

Hmm. Let's Google this hint.

We easily find the answer: Using ADB logcat

### ADB Logcat

*ADB Logcat* is a feature provided by the command-line tool ADB, which is a tool used for communicating with the Android device from a computer. 

Let's now try to get the log of an Android device/emulator to understand this.

Step 1: Connect your Android device to your PC or start up your emulator.

Step 2: Open EVABS and navigate to 

cred://app/launch?page=https://www.google.com

