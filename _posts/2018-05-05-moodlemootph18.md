---
title: treehouses.io in MoodleMoot Philippines 2018
layout: post
author: mappuji
---

Last April we speak at MoodleMoot Philippines 2018 where we talk about our progress in packaging Learning Management System (LMS) especially Moodle and introducing [treehouses/remote](https://github.com/treehouses/remote/issues) to the audience.

The story is a little bit funny. One of the organizers of the MoodleMoot Philippines was sending me a message and inviting me to connect on LinkedIn. She reads that I have a little bit experience with Moodle and ask me if I interested attending the conference. I don't know why, but I automatically answered by not only attending if possible I want to speak there talk about our advancement in deploying Moodle LMS in small devices like Raspberry Pi. Then the rest is history. Yeah, there was a time where I invited to talk directly in Manila, but because I don't have a budget for that I talk about my constraint and then they offer me an options to talk remotely and turned out not only me that talking in this conference remotely, there are also some other presenter even from outside Asia.

The story was started from a small project to setup a simple LMS in Madagascar, and at that time our primary LMS, which is BeLL-Apps is in maintenance mode and our new LMS Planet is still under development. We then decide to use Moodle to bootstrap the project and deploy it in Madagascar. The problem back then is we want to have the stuff running both in amd64 (server) and also arm devices which is Raspberry Pi (specifically RPi 3).

***

Okay, lets dive deeper to the content of my talk.

### The problem

Deploy Moodle in Raspberry Pi is easy, even more easy if you deploy it in `amd64`. We can just deploy it directly in the machine by installing MySQL or PostgreSQL and the Moodle with some web server via Nginx or Apache, but we choose another path.

Since the beginning we want to build a platform where people can deploy various educational apps in single board computer. One of them is is Moodle, but we also want to deploy another application like our own LMS called [open-learning-exchange/planet](https://github.com/open-learning-exchange/planet/).

In essence the requirements are

* Easy to setup and operate the software
* Run on small machine (Raspberry Pi mostly)
* Able to deploy multiple applications

So we choose Docker.

<center><img src="{{ site.url }}/assets/images/container-meme.jpg" alt="Container container everywhere!" style="width: 400px;"/></center><br>

If you never heard about Docker, it is a container engine, an implementation of container technology. For the past 4 years, it is reinventing how we deploy software and make container technology become mainstream.

What is special with Docker? If you come from the time where you can spawn another instance of software by installing some Virtual Machine engine like Virtual Box or VMWare, it is something similar but quite different. Well, my first time meeting with virtual machine was using it for doing some cheat on my favorite online game. Just several years ago I know that people using virtual machine for managing server and deploying application on the internet.

<center><img src="{{ site.url }}/assets/images/run-on-my-machine.jpeg" alt="Container container everywhere!" style="width: 400px;"/></center><br>

Well, the problem is still about deployment. Docker and container technology in general want to reduce time installing application and giving us more time to test and deploy our application, instead of spending time in repetitive installation process.

