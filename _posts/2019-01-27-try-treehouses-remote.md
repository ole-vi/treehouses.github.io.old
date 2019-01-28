---
title: Try Treehouses Remote An easy way to control your Raspberry Pi via Android phone
layout: post
author: empeje
---

## Background

> We want to make our software easy to operate

Have you ever imagine that you can bring your battery-powered RaspberryPi in your bag and you can control it via an Android phone? Then you can do a fancy hack. My friend ever did something similar with a laptop plus an SDR (Software Defined Radio) device to hijack his friend remote controlled car door. But image now you can do the prank with the your Android phone.

We inspired by our systems administrator and operator in the field who more-likely familiar with phone rather than advance computer skills. Which expected because the one who operate our software and hardware is volunteer working in a remote area. We want to make our software easy to operate. So instead of telling them how to do an SSH and fancy terminal, we create an app that can connect to the RaspberryPi as simple as pairing our Bluetooth headset to our phone.

## Getting Started

Requirements:
* Android Phone
  - [ ] Install [treehouses/remote](https://github.com/treehouses/remote/releases) app
* RaspberryPi 3B or higher (any version with bluetooth)
  - [ ] Install [treehouses/builder][GETTING_STARTED] image (in this example we use treehouses image version `75`)
* A laptop
  - [ ] Install [Etcher](https://www.balena.io/etcher/)
  - [ ] Install [Tor Browser](https://www.torproject.org/projects/torbrowser.html.en) (we have a fun demonstration)
* Wifi Access point with good internet connection

Once you're done you can do the following steps

### Step 1 - Burn the downloaded image to a microSD card

Since we don't want to repeat ourself, we  recommend you to follow the steps on our [getting started page][GETTING_STARTED] to download and burn the image to your SDCard.

### Step 2 - Insert the SD card to the RaspberryPi

After you burn your newly downloaded image to RaspberryPi you need to insert it to the RaspberryPi and plug the it to the power cable. Wait until the RaspberryPi green light blipping continuously. Here is the example on one of our machine.

<center><img src="{{ site.url }}/assets/images/post-treehouses-remote/remote-0.jpg" alt="Wait till green light up" style="width: 300px;"/></center>

### Step 3 - Open Treehouses Remote and connect to the RaspberryPi's Bluetooth

Now make sure the apk you download have been installed in your Android phone. And open it.

* Open

* Click `CONNECT TO RPI`

<center><img src="{{ site.url }}/assets/images/post-treehouses-remote/remote-1.png" alt="Welcome screen treehouses/remote" style="width: 300px;"/></center>

* Wait until the list of bluetooth device show up
* Click treehouses bluetooth

<center><img src="{{ site.url }}/assets/images/post-treehouses-remote/remote-2.png" alt="Connect to your treehouses raspberry pi bluetooth device" style="width: 300px;"/></center>

### Step 3 - Tada 🎉now you can run any commands on RaspberryPi via your Android

* After connected, click the side bar by clicking three strips in the top left
* Click terminal

<center><img src="{{ site.url }}/assets/images/post-treehouses-remote/remote-3.png" alt="Go to terminal" style="width: 300px;"/></center>

* Now you arrive in terminal screen, you can command your RaspberryPi as it were in SSH session

<center><img src="{{ site.url }}/assets/images/post-treehouses-remote/remote-4.png" alt="Remote terminal" style="width: 300px;"/></center>

* Try prebuilt command (e.g. `Treehouses Detectrpi`,`Docker ps`)

<center><img src="{{ site.url }}/assets/images/post-treehouses-remote/remote-5.png" alt="Example detect rpi" style="width: 300px;"/></center>

<center><img src="{{ site.url }}/assets/images/post-treehouses-remote/remote-6.png" alt="Example docker ps" style="width: 300px;"/></center>

### Bonus Step - Expose your machine to Tor network

* Connect to internet with treehouses cli
* use these commands

```bash
treehouses wifi $SSID $SSID_PASSWORD_IF_ANY
# example
treehouses wifi treehouses-wifi # if no password required
treehouses wifi treehouses-wifi treehouses-password
```

So your RaspberryPi once booted with treehouses image has our Planet Learning Management system installed and ready to use, you can expose it to Tor network and make it possible for other people to use it.

* Create your a Tor Tunnel, follow this commands

```bash
treehouses tor add 80 # expose port 80
treehouses tor add 2200 # expose couchdb port if required
treehouses tor start

treehouses tor list # to list all the port
treehouses tor # to get the onion address
```

* Congratulations 🎉, now you can open your RPi's app on your Tor browser, here is example of our setup.

<center><img src="{{ site.url }}/assets/images/post-treehouses-remote/remote-8.png" alt="Example docker ps" style="width: 800px;"/></center>

[GETTING_STARTED]: http://treehouses.io/getting-started)
