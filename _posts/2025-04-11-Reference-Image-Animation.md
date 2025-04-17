---
title: "Reference Image  Animated!"
excerpt_separator: <!--more-->
categories: 
- Creativity
tags:
- coding
- fun code
---

So here’s the first Youtube Draw Along video I’ve made:

I enjoyed making it, and hope to streamline the process of creating even more so I’m just chilling drawing, instead of programming way too many things just to make a speed paint haha. One of those completely too much ideas I had was the reference image floating around in a frame to add some visual interest. I previously added clouds moving in the background, but I wanted something more *animated* and alive.

<!--more-->

***

![referenceImg]({{ site.baseurl }}/assets/images/imagerotation.gif)


The concept I had was a sci fi knight placed in a medieval setting, with some standard things like a visor updated. But the character didn’t really make much sense so I’m planning on changing some things so stuff is more cohesive. Adding some surrealism to the frame might help, and I’ll change the color pallet of everything else maybe to make it work.

# more visual interest is always better! xD


Anyway, my idea was to have the image look like it was shifting and rotating around in 3D space. I also wanted to have the image zoom into a random quadrant, to help the viewer see details (it makes up only like an eighth of the screen area). Fortunately, the process was pretty easy due to Processing’s P3D renderer. 

The only hiccups I ran into was the texture mapping during the “zoom”. It turned out a new shape had to be created and written to, because there doesn’t seem to be a way to change the u and v values to .vertex. There was also a problem with changing the image’s vertices, as I was just calling different `.vertex()` commands in a loop. It turned out I needed to use `.setVertex` instead (finding an error from reading the documentation is so satisfying but annoying at the same time - I’m glad there’s a solution but why didn’t I know about this lol).

The last issue was the matter of rotating the `PShape`. It was easy to use the `rotateX` and other commands, but when remaking the PShape above I needed the image in the frame to match the rotation of the frame itself. So I just made another variable to track the total rotation to make it match up again. 

I look forward to hopefully optimizing this sketch in the future, especially its just supposed to be a side thing; I wouldn’t want this nice visual using too much of my CPU (I might end up just making a video I can loop from each image but that seems time intensive and annoying but idk). Till the next update! :-)
