---
layout: doc
title: Getting Started
permalink: /getting-started
repo: builder
docs: true
---

So you're pirate who wants to leverage other people result and just want to have something that runs perfectly out of the box? This is the getting started to install [treehouses.io](https://github.com/treehouses) Raspberry Pi Image to your Raspberry Pi. This getting started will demonstrate specifically to Raspberry Pi 3B.

This guide will be specific to Mac OSX but will be applicable to other operating systems such as Linux distribution or Windows.

## Downloading Image

The first step to do for installing the Treehouses RPi image is to download from our official repository here.

{% include download_button.html %}

Or if you need a specific version, you can download it [here](http://dev.ole.org/) or you can click [download](/download) button in the top navigation.

<center><img src="{{ site.url }}/assets/images/th-download-page.png" alt="Our download page!" style="width: 600px;"/></center><br>

You can just click the `DOWNLOAD LATEST TREEHOUSES IMAGE` and you'll get the latest image (not always be stable) or you can browse for the specific version in the given link which will redirect you to [dev.ole.org](http://dev.ole.org).

Okay, suppose you want to download the version 53 of the image. In the [dev.ole.org](http://dev.ole.org) navigate to the desired image.

<center><img src="{{ site.url }}/assets/images/th-image-latest.png" alt="Image latest in the repository" style="width: 600px;"/></center>

<center>Latest Image</center>

<center><img src="{{ site.url }}/assets/images/th-image-53.png" alt="Image 53 in the repository" style="width: 600px;"/></center>

<center>Version 53 Image</center>

<br><center><img src="{{ site.url }}/assets/images/th-image-53-download.png" alt="Download it!" style="width: 600px;"/></center>

<center>Then download it!</center>

## Installing Etcher

In order to burn your image to Micro SD Card, you need a flasher, a small piece of software that copy and format the filesystem of the Micro SD. We recommend you to use Etcher from [Resin.io](https://etcher.io/).

<center><img src="{{ site.url }}/assets/images/th-etcher.png" alt="Download etcher" style="width: 600px;"/></center>

<center>Download Etcher!</center>

<br><center><img src="{{ site.url }}/assets/images/th-etcher-install.png" alt="Install Etcher" style="width: 600px;"/></center>

<center>Then open the package and install it!</center>

## Burn the Image

The next step is to burn your image with Etcher. You only need to open Etcher and do three steps:

* Choose your treehouses image
* Choose your target SD Card (don't forget to plug your card first)
* Click flash!

<br><center><img src="{{ site.url }}/assets/images/th-select-image.png" alt="Etcher Select Image" style="width: 600px;"/></center>

<br><center><img src="{{ site.url }}/assets/images/th-select-device.png" alt="Etcher Select Device" style="width: 600px;"/></center>

<br><center><img src="{{ site.url }}/assets/images/th-flash-complete.png" alt="Etcher Complete" style="width: 600px;"/></center>


## Boot your SD Card

The last step is to insert your Micro SD Card to your Raspberry Pi and then turn on the power, then after few seconds, it will be arriving in the desktop like this.

<br><center><img src="{{ site.url }}/assets/images/th-desktop-starter.png" alt="Fresh Desktop" style="width: 600px;"/></center>

You'll be warned that it has a ssh open and you need to change the default password and username for security purpose.
