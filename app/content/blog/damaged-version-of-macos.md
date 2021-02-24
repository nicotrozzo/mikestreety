---
title: Damaged version of macOS
published: 2017-8-10
updated: 2017-8-10
intro: I was recently trying to install a copy of macOS from a USB stick I'd made and kept getting an error saying the OS was damaged. I created the stick using both the command line and the OSX Install Disk Creator and whatever I&nbsp;did I&nbsp;got the error.
tags:
 - Geekery
---

I was recently trying to install a copy of macOS from a USB stick I'd made and kept getting an error saying the OS was damaged. I created the stick using both the command line and the OSX Install Disk Creator and whatever I did I got the following message:

> This copy of the Install macOS Sierra.app application is damaged, and can't be used to install macOS.

No matter what I tried, I got the error. After some googling, I was led to [this Apple thread](https://discussions.apple.com/thread/7675283?start=0&tstart=0)​, however, as the installer was on a USB stick and not the computer, this fix did not work.

It turns out the computer thought it was 2012 (verified by typing `date` into the terminal) and so thought the new OS was corrupt. This was resolved (thanks to [macworld](http://www.macworld.com/article/3097533/macs/installing-os-x-what-to-do-when-this-copy-of-the-install-os-x-application-cannot-be-verified.html) ) by correcting the date of the computer. 

Connect to the internet (if you can) and type the following in terminal. If you can't get to the internet, the macworld article explains an alternative method.

<pre class="language-bash">ntpdate -u time.apple.com</pre>