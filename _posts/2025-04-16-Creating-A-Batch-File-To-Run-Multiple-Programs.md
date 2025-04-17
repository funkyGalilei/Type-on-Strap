
---
title: "Creating a Batch File to Run Multiple Programs"
categories:
- Programming
- Creativity
tags:
- creativity
- powershell
- utility
---


So, the goal I wanted to achieve is a method to click a single button, and have a streaming setup be activated along with OBS, which will capture it. To do this, arranging files into an executable and "building" the code could have been a solution, but I have no idea on how to do that. Instead, I turned to batch files! They are just commands you can write in a simple text editor and can run anything a command line interface could run like Powershell on Windows. All the files and references are local to my machine, so there wasn't a need to make an executable yet.


---
I had 3 programs I wanted to call:
- the main pngtuber
	- This creates a character that will move when I talk
- the reference image
	- Which will create a warping png image used as a reference image while drawing
- the tablet software
	- the character I use moves their hand around while drawing, and this could be adapted into my own code. However, I haven't figured out global java hooks quite yet, so I use a program called Spud's Tablet Program found here:
	
https://sadwhale-studios.itch.io/spud-tablet

- OBS itself as well
	- For capturing the content, and recording to a video file.
The code is short and is listed below:

***

```@echo off
:: MAIN PNGTUBER
processing-java --sketch="c:UserspngtuberProcessing" --run

:: REFERENCE IMAGE WARP
processing-java --sketch="c:refImageWarp" --run

:: TABLET MAPPING VISUALIZER
cd "C:UsersNimoDSDocuments"
start tablet.exe
@pause
```

***

The echo command turns on output to the window that comes up, and the `pause` command keeps the window up after the commands are executed. I couldn't run processing sketches at first, but then I found out that the main sketches that call the others need to be named the same as the folder that they are located in. If you run them in the Processing IDE, a warning comes up but you can still run them, so I was confused for a while.

This random blog post was very helpful, and I'm glad people post useful and informative things on the world wide web! :)
https://www.dsfcode.com/using-processing-via-the-command-line/

An example of another simple file opening mspaint, notepad and the calculator:

![windows opened up]({{ site.baseurl}}/assets/image/batchFile.png)

I'm glad I learned about this, and hope to maybe use Powershell commands more in the future. This was a rather simple use case, but I know that they can get advanced and be used to do IT work, as well as create more complicated scripts. Using command line tools is also important if I ever learn Linux or anything like that. Thanks!
 
