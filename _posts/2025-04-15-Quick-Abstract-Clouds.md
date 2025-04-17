---
layout: post
title: "Abstract Cloud Animation in Processing"
feature-img: "assets/images/clouds.png"
categories:
- Visualization
- Programming
tags:
- processing
- animation
- art
- abstract
---

I originally featured the word "Quick" in the title of this article, but unfortunately for most of my creative project's it was more difficult than anticipated and ballooned into having multiple different options.
The first thing I enjoyed about this project was creating a class to hold every "cloud" (or circle with a variable alpha value)'s data set. I have variables for:
- the previosuly mentioned alpha values, the speed of the horizontal direction
- the path that the circle will travel in (with 4 possible different y locations)
- the original spawn point of the clouds
- a random radius addition for variable circle sizes
- brightness for the color value

![smoothing]({{ site.baseurl }}/assets/images/clouds.png)

I love how in programming, you can get complex behavior out of relatively simple commands. Inside the class, I simply put the original command, something like `x = random (width, width * 1.5 radius)` (to put the circle somewhere off frame) again, and bam, I have an infinite loop of clouds. I actually forgot this the first time I implemented it because I was focused on some other feature as well, and didn't stop the file output until I realized it wasn't going to stop haha.

---
#### GUI and Live Updates
In addition, one of the things I like is live manipulation of variables. I used the **LazyGUI** processing library I've been using for almost all the projects I do now to fine tune parameters. Making values change live is more difficult to do, but I find that restarting the program and waiting for my computer to load just doesn't feel satisfying. I want to be able to boot up a program, and have it run continuously until all the input parameters are dialed in. Now, due to the layout of classes, some variables are used once at the beginning of the process and not called either in `cloud.update()` or `cloud.show()`, such as the spread of
#### Cheating with Davinci Resolve
I was unfamiliar with video formats, as they're just so many. I know I wanted my end file to be transparent when overlayed in OBS. To do this, generating an mp4 with the input ffmpeg *Movie Maker* tool in Processing wouldn't work. I could save a `PGraphics` object to create a transparent png sequence, but video is a separate ball game. I have Davinici Resolve, so I looked up the right output formats, which was a GoProVision and RGB 16 bit format I believe. With this, I decided last minute to add some color with its *Effects* tab, and did a solid color background mixed with the input frame. This was cheating. I should've just selected the color in the original sketch, but honestly, I don't mind. If I want to use this sketch in a different sketch with some differently colored surreal clouds (actually, I think clouds are surreal normally by themselves weirdly enough)  I can just rerun it through Resolve.
#### Conclusion
I hope to add this to a shared repository that contains other quicker visualization scripts as well, so I don't have as many repositories on GitHub. Till next time!
