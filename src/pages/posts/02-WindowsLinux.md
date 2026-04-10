---
layout: ../../layouts/PostLayout.astro
title: The next Windows might be a Linux distro
author: Joseph Herrera
date: 02-29-2024
---

Bold opening, I know, let me elaborate.

For years, Windows has been the dominant operating system for everyday users on desktop. It has maintained this position because they know when to evolve and when to keep things from the past.

It's clear that for many, Microsoft hates open source and of course Linux, but this has radically change in a couple of years on the direction of Satya Nadella. Microsoft now wants to join in on the group of people that make software free (as in freedom) for everyone.

They used the chromium source to renovate the edge browser which is now killing it in features and performance. They own GitHub, which is the preferred platform for open source developers. Not only that, but many of the projects they are making are open source too.

This all might seem like they only like to grab free code and have free workers, and yes that's part of it, but there's more.

As I mentioned, it's the favorite OS for regular users, but developers like MacOS or even Linux more (unless you have to develop a software for Windows of course). This is because of security, tools and features that Windows doesn't offer. So, how those Microsoft plan on gaining more developers over?

# Windows Subsystem for Linux
It's amazing, you basically have Linux inside Windows. Sharing your directory of files. You can open your code on VS Code and use the Linux commands there. You can even install and run Linux programs on Windows. By default it comes with Ubuntu, which is the most popular Distro, so it's alright.

I tried this two times, when it had recently launched (the first version) and the now version two. The first time, the installation was a little complicated, copy and pasting commands complicated, but you had to download Ubuntu from the Windows Store and a lot of weird steps. Now, the installation requieres one command and following the simple steps:

```bash
wsl --install
```

# Sudo for Windows
This is a very recent addition to Windows 11 and of the reasons I am making this article. Sudo is as the Microsoft article explains: "Sudo for Windows is a new way for users to run elevated commands (as an administrator) directly from an unelevated console session on Windows."

This was a feature exclusive to Unix based systems like MacOS or Linux. Another feature taught for devs.

# WineHQ
From their website: "Wine ... is a compatibility layer capable of running Windows applications on several POSIX-compliant operating systems, such as Linux, macOS, & BSD."

This tool allows you to run some old Windows apps even better than at Windows itself on Linux or MacOS.

Having this technology in mind, I don't see impossible to have a Windows OS based on Linux with a backwards combability layer using this or a similar technology.

# Conclusion
As you can see, Microsoft is slowly adding features to Windows to make it a platform for developers. As time goes by, the reasons to keep the OS based on MS-DOS a vulnerable and exclusive system seems less and less. The main reason of course, is money. The moment Microsoft can find profit on a open source OS they might switch.
