---
layout: default
title: About
permalink: /about/
---

[Treehouses](http://treehouses.io) is community-powered project initiated by [Open Learning Exchange](https://www.ole.org/) to develop SBC-based (single board computer) learning management system mainly for used in resource constraint place like place with minimum electricity and internet connection.

It is focused in Raspberry Pi, but the effort will be replicated in other platform as well, for example we build docker for armv7, armv6 and arm64 for several learning management system where any SBC with the same architecture can leverage.

The main idea was building a platform where we can install Docker image of any kind of Learning Management System in machine as small as Raspberry Pi.

Our efforts divided into several projects, those are

* [treehouses/builder](https://github.com/treehouses/builder) -  a specialized Raspberry Pi Image with prepackaged Docker engine and several tools.
* [treehouses/remote](https://github.com/treehouses/remote) - remote control your Raspberry Pi with an Android Bluetooth remote.
* [treehouses/cli](https://github.com/treehouses/cli) - a command line tool for Raspberry Pi.
* Docker-related project
  * [treehouses/moodole](https://github.com/treehouses/moodole) - Multiarch Docker of Moodle LMS
  * [treehouses/rpi-couchdb](https://github.com/treehouses/rpi-couchdb) - Multiarch Docker of CouchDB
