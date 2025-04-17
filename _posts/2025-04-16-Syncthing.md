---
title: "Syncthing, I Wish I Found It Earlier"
categories:
- Blog
- Software Spotlight
tags:
- Programming
- note-taking
---
# Syncthing, a game changer for Logsec and Local Sharing

Syncthing is a psuedo server almost that lets users sync files between different devices. It is open source and you can download it here:

https://syncthing.net/

I'll mainly be talking about my own use case, of wanting to sync notes (stored as markdown files), pictures, and music between my phone, main laptop and secondary older laptop. Syncthing was a perfect solution for this, as my laptop definitely has the space, and these things were going to be stored on my phone anyway. 

When I was originally looking into syncing my files, I could've used Github or Google or any number of cloud services. I'm honestly not usually too worried about a hacker stealing my data, or survellance by any of these companies, but there was something off about my inner most thoughts and lists being stored on a server somewhere that I didn't vibe with. Enter Syncthing, where everything is stored on the devices I would want them to be on.

The setting up process was super easy, and you just connect a devices ID on both devices to connect them. You then set up the folder you want to share, and on the receiving device set the directory. It was super quick and I had my Logsec graph on my phone and could edit things within 15 minutes. Which feels great! I probably won't write long articles on it, but for TODO lists it will be a game changer.

You can also configure how often Syncthing will check for updates from other devices, and runs super well as a background process. It can run well on every device and jumps between 0 and 0.1% on my most powerful laptop. I haven't noticed any loss of battery life in my phone as well.

![Syncthing in Task Manager]({{ site.baseurl}}/assets/images/SyncthingTaskManager.png)

I have a query set up in my `baseJournal` that pulls the undone tasks from my TODO lists, and I end up usually checking stuff off the day after, instead of doing it when I'm done. This is just because I forget, but with this, I can check stuff off on my phone before I go to bed. I just wanted to praise Syncthing and the open source community for giving me the best solution to a problem, and I'll only use cloud storage for larger files, like videos or photos eventually. I don't have a real tower PC yet, but when I do I'm sure I'll get into building and configuring my own server. But before that, Syncthing will be a staple on my main devices! :)