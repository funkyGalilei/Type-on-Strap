---
title: "Everything is Flappy Bird"
categories:
- Creativity
- Programming
- Processing
tags:
- coding
- fun code
---


# Flappy bird 
An iconic game that had a billion alternate versions made in the 2000s. And now we think of it fondly as an example of how a game with only one mechanic (and an annoying one at best in my opinion) can gain fame and fortune. Well, that’s a bit mean of me to say that it's annoying, but you get my point. 

![smoothing]({{ site.baseurl }}/assets/images/smoothing.png)

Flappy bird is so in the zeitgeist that now it's used as an example to teach kids how to code. It's 1D motion, so there’s only one variable to keep track of, which makes it a great learning example. And then I accidentally coded it when I was trying to do something else:

![smoothing]({{ site.baseurl }}/assets/images/mouseInputSmooth.gif)

I was originally trying to make a **moving average filter**, a filter that would limit the change a variable can go through by clamping values. This was going to be for my pngTuber project, as I was not satisfied with not having control over certain values in other programs.

To recap some differences, pngTuber Remix and others have a mic sensitivity function, which triggers a “speaking” phase when the mic intensity goes over a certain limit. Instead of a trigger method, I wanted to index into an array of values based on the mic sensitivity. Like a puppet changing the angle of their mouth depending on how much sound someone is speaking. In certain programs you can play an animation, which is honestly pretty close to the effect I’m looking for. In pngTuber Remix, I made a sprite sheet and then an animation was played of the visor on the knight character falling down. Which is good, but I didn’t like the intensity being visually represented as max going up and falling down at a constant rate no matter what.

So, that’s why I started programming my own png tuber capabilities in processing. The issue with a direct mapping (I had the intensity map to index and show an image in a sequence) is that there’s a lot of noise, and it comes across as quite jittery. I could have less images (I rendered about 48 I believe) and select based on a wider bin of intensities, but I liked the smoother visual. So to remove that noise, I needed to add a filter. I’m learning a lot about moving average filters, and signal cleaning right now due to taking MATLAB courses, but those are more for when you have the complete signal. Going back and applying an algorithm like [this (a wikipedia article on moving average](https://en.wikipedia.org/wiki/Moving_average) would work very well, but it needs values ahead of the current spot on the x-axis, or time. I can only reference previous values as it’s live. There are various methods of [reducing](https://en.wikipedia.org/wiki/Noise_reduction) noise in audio, but I just needed a simple intensity feature. The ones that already exist are super advanced and would be overkill for what I want.

So, I first made a visualizer where a ball would be raised if the mouse was clicked by a set value. I also wanted to see how my function would perform on small movements, so I used the lerp() function, set to move the ball's position back to the bottom by a percentage. The small movements at the end of the ball’s return would be zeroed out hopefully by this algorithm. And it was! The resulting visualized variable was much more snappy **and** didn’t rise as quickly either when the mouse click was spammed. All in all, I think flappy bird is awesome and I’m glad I was able to learn more about how even 1D motion can get more complicated than I thought. 

I look forward to applying this to audio signals, and extending the GUI on my pngTuber program to adjust the sensitivity, and maybe add some other simple filters to it! :)
