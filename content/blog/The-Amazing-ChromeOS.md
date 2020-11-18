---
title: "Coding with Raymond - How to Get Minecraft on a Chromebook"
date: 2020-11-17T23:16:03-05:00
slug: ""
description: ""
keywords: []
draft: true
tags: []
math: false
toc: false
---
I have two sisters that are in 6th grade. Because their brains are so malleable, I figured I’d introduce them into the first step of using computers, by playing Minecraft. In most cases, it’d be simple. Just buy Minecraft and tell them to download it. Unfortunately, this did not happen.

They told me they were using ChromeOS, which can’t run Minecraft. Everything was downhill from there. This is the cautionary tale of my journey to ChromeOS.

To my surprise, ChromeOS couldn’t run Minecraft. In fact, it can only run mobile game software. This was astounding, but I was determined to find a way to get the game on there. I mean, I have a degree in Computer Science for a reason right?

Linux seemed like the obvious choice. And I thought about completely wiping their drives and just installing Linux. I thought about how that was too overboard, and how maybe I could just use a virtual machine (It’s a pain to set up). Then, I realized, I could just use a live-persistent copy of a linux on a flash drive.

**Live Persistent**

Linux has this cool tool where you can carry your files wherever you go. You plug it into a computer, run the BIOS command, and you can instantly switch operating systems. You don’t need to run Minecraft on ChromeOS if you just use Linux on a USB drive to run it.  

**Creating a Live Persistent Flash Drive for Ubuntu**
This was the first step, because I’d never used Linux before, but it was pretty simple. I just downloaded an Ubuntu iso image file, and installed another program to burn that onto a flash drive. Then, I ended up mailing it to my sisters which took a couple of days. The plan was to simply put the flash drive in and press the Chrome commands to boot from the USB. It works that way on Windows right? How hard could it be? 

Yes, you’re right. It went terribly, and our adventure continues.

**Enabling USB Booting on Chrome**
Unlike Windows, which can easily boot from a USB by pressing 2 buttons, ChromeOS apparently was hell-bent on ruining my life. I realized ChromeOS won’t allow Bios access unless developer mode is enabled. 

This entire concept took me an eternity to solve. I spent maybe 5 hours reading Wikihows and documents and directing my technologically inept sister how to do this process. It was painful and terrible. 

For the 2 people who plan on buying a ChromeOS and want to unlock its full potential keep reading. 

**How to Enable USB Booting on ChromeOS**

Basically, ChromeOS decided to make modifying the back-end of the OS hell. 1.) You need to enter Developer Mode (Which wipes the entire hard drive, so sucks to suck if you didn’t plan on backing up your entire hard drive) 2.) Once inside developer mode, your still limited by ChromeOS’s terrible firmware so you can’t even fully customize things.

Enter MrChromeBox.tech, a guy who manually fixed these problems. He goes above and beyond by explaining every little nuance related to ChromeOS, like how running Ubuntu on most devices will disable the audio entirely (Thank you again ChromeOS). <a href="https://mrchromebox.tech/"> Here’s his website. </a>

To summarize, It just boils down to this:
**1.)	Enable Chrome Developer Mode**

In order to do any hands-on stuff, developer mode needs to be enabled. This will wipe the hard drive of the Chrome device for whatever reason. Also, it’s extremely easy to switch between these processes, simply by pressing space bar in the middle of it (The firmware can disable this though)

There’s like three commands, the tutorial has the info on how to do this ( Because it depends on your laptop model. 

**2.)	Install the Firmware Utility Script**
Again, in the link, this is as simple as copying and pasting his commands in the chrome terminal. He makes a note that this must be in chronos, not root. So just open a guest window and use that terminal

I had an odd bug where I couldn’t use Sudo as chronos. I had to go into root, create a password for chronos, and then go back and use sudo as chronos.
**3.)	Enable Firmware options by pressing 1**

And there you go. If you’ve followed along so far, you’ll be surprised to notice that you can easily undo any of these changes by pressing spacebar when your Chromebook initially boots. In which case, you’ll have to spend $15 for a unique cable to fix this, *or*, you could re-do the dev mode process again (yay!).

**That’s All Folks**

I hope you enjoyed this because I didn’t. At the end of the day, I managed to bypass ChromeOS’s bullshit and allow my sisters to play Minecraft on their laptops. You can imagine my surprise when the game was laggy and slow, so she stopped playing it after about 30 minutes. 

All in all, 10 out of 10 would recommend. 
