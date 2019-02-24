---
layout: post
title: "Moving your android apps to the external storage"
feature-img: "assets/img/pexels/android-app-blog-267389.jpg"
tags: [android, ubuntu]
---

Since recently I've been playing more with [my modest android smartphone](http://en.wikipedia.org/wiki/HTC_Wildfire_S), I started suffering from his lack of internal storage memory. His 150 MBs quickly become insufficient since it comes with plenty of pre-installed applications that can't be erased unless you [root your phone](http://en.wikipedia.org/wiki/Android_rooting).

I was looking for an easier way to make more room for applications when I found this [excellent howto](http://www.howtogeek.com/114667/how-to-install-android-apps-to-the-sd-card-by-default-move-almost-any-app-to-the-sd-card/). You will need to setup your phone to store by default in the external storage, and then suddenly almost any installed application can be moved to the external storage, and the newly installed applications will go there by default.

I'll describe the process that I made in order to configure my phone. I used a laptop with an [Ubuntu Linux](http://www.ubuntu.com/) distribution installed.

First, we need to install the Android SDK Manager in the computer. In Ubuntu, we can [use a PPA repository](http://www.upubuntu.com/2012/07/install-android-sdk-manager-revision-20.html):

```bash
sudo add-apt-repository ppa:upubuntu-com/sdk
sudo apt-get update
sudo apt-get install ia32-libs android-sdk
```

Now we can open the Android SDK Manager and install the SDK Platform-Tools if we don't already have it.

Then, we need to connect our phone to one of the laptop's USB. We allow USB debugging on our phone in Setup > Applications > Development.

Finally, we reconfigure the storage defaults:

```bash
cd ~/android-sdk-linux/platform-tools
./adb kill-server
sudo ./adb start-server
./adb devices
./adb shell pm setInstallLocation 2
```
