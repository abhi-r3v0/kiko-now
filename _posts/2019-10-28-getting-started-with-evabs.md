---
layout: post
title: Getting Started with Android Security
tags:
  - Android
  - CTF
  - EVABS
---

# EVABS

## Introduction

### What are CTFs?
In this blog post, we'll see how we can kickstart learning Android security in a CTF approach. CTF stands for 'Capture The Flag' which is basically gamifying and making the learning process more intuitive and fun. In a CTF, a user is given intentionally vulnerable softwares/hardwares. The 'software/hardware' mentioned here includes, but is not limited to:

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
The advantage of CTF-style approach is that the user gets to verify if he successfully exploited a particular service/application/program or not, by getting a flag.
