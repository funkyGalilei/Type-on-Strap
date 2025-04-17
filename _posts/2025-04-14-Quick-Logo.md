---
title: "A Quick Personal Logo in Processing"
featured-image: logo.gif
featured-image-alt: My personal logo that i made
categories: Creativity, Programming
tags:
- visualization
- processing
- logo
- quick
---
Now, this was actually one of the first projects I've done in Processing that was *actually* quick, not just "quick" turning into "long" haha. I wanted to make a personal logo, and to keep it simple. If you look reaaaaallly closely you can see inspiration from the Processing organization's logo (I'm joking ik it looks the same basically without the line of the "P").

![smoothing]({{ site.baseurl }}/assets/images/logo.gif)


A long time ago in high school I actually coded a similar visualization fo my name written in JavaScript as I was learning on Khan Academy. I'm gonna login and see if that code is still stored somewhere and see if I can encode it into this website once I become more knowledgable. One of the funny things about that old project I remember is that the shapes started from different parts of the screen, and then translated so my name was visible, but only for a second, and then they wizzed off screen.
Now, the thing with Processing is that it runs on my local computer, and isn't shared or ran client side. Which is why I am going to port and experience using p5.js soon, so the logo can actually be animated like it is in the gif below:

---

I know it seems dumb to write something in Java and then display it as a gif on a website instead of just using the script itself, but I'm still getting situated in Jekyll and I'll be sure to link it up with that knowledge. Something about a script that works on my own machine and just having it be local or an executable to hand out is ideal in my mind. It's obviously not, and I should be more knowledgeable as a web developer, but after only writing scripts and programs on closed system software for a while, its just something I'm used to.
One color theory method I wanted to implement in this sketch was a Blender-like ColorRamp, to transition between 2 colors. That's definitely on the TODO list. In the past and with this sketch I set the `colorMode()` to HSB, and then added a sin wave value to shift the hue backwards and forwards to give it a little motion. In the future, I'll potentially use the `lerp()` function or easing to transition between discrete colors I pick out. I added some actual motion as well, and had the shapes sway back and forth with the `rotate` function, which was easy enough.
I hope to do more quick, cool mini-visualizations like this one in the future, alongside more fleshed out projects that a solid backbone. Sometimes small, cutish things are useful for learning as well! Thanks for reading :)
 
