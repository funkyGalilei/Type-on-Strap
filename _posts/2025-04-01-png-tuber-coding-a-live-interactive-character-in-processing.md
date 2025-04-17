---
title: .png tuber - coding a live, interactive character in Processing
date: 2025-04-01 20:56
author: dillonsemail2012
comments: true
categories: [Blender, Creativity, Programming]
---
<!-- wp:paragraph -->
<p>PNG tubers? What are they? Well, you might have heard of Vtubers, which are 3D modelled characters that use live face tracking to essentially create an avatar that mimics the eye motion and facial expressions of people. This is usually live, and can be very impressive. I have learned how to model in blender, but the hardware I have accessible right now (a powerful laptop) can’t quite do anything that intense - especially while running other programs. So instead, there’s these things called png tubers - which are animated characters that are 2D and can have their own animations. When diving down this rabbit hole, I fell onto the 2 main available base programs to start from:</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":283,"sizeSlug":"full","linkDestination":"none","align":"right"} -->
<figure class="wp-block-image alignright size-full"><img src="https://dillonsmith57.wordpress.com/wp-content/uploads/2025/04/knight.gif" alt="" class="wp-image-283" /><figcaption class="wp-element-caption">A snapshot of the WIP project in action - the boxes on the top left represent the state, the main ball represents the audio noise input, and the black ball represents the mouse cursor location. The noise input indexes into a png sequence of the visor, while the cloak is indexed linearly creates an animation.</figcaption></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>And the program that inspired me to write my own is called pngTuber plus:<br><a href="https://kaiakairos.itch.io/pngtuber-plus">https://kaiakairos.itch.io/pngtuber-plus</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Along with a smaller right now program named Veadotube:<br><a href="https://olmewe.itch.io/veadotube-mini">https://olmewe.itch.io/veadotube-mini</a></p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":276,"sizeSlug":"full","linkDestination":"none","align":"left"} -->
<figure class="wp-block-image alignleft size-full"><img src="https://dillonsmith57.wordpress.com/wp-content/uploads/2025/04/completed-knight.png" alt="" class="wp-image-276" /><figcaption class="wp-element-caption">My knight character I modelled in Blender. Unfortunately some blooming compositor effects were lost in import, but I think the result still looks neat! :)</figcaption></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>They are both very interesting and cool, but they didn’t quite do anything that I wanted to do. Which is fine! Of course some things that I have in my head are just going to be different. For one, Veadotube deals with gifs for animation (though honestly just switching in between 2 images looks more convincing than I would have thought), and PNG tuber plus deals with sprite sheets (png images placed horizontally next to each other, forming a long strip like a zoetrope). The files that I was using were .png sequences, .pngs named 0001 and 0002 and so on in their own folder.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>For my idea, I wanted to have a knight character have his visor wobble up and down as audio input came in. And! I wanted to pre render this in Blender! That way, I could get this 3D blender visual I wanted, but with images being switched out instead of the visor - a 3D object with a hundred or something vertices being shifted in real time - with the shaders being updated as the light hit them, and then being run through a compositor for a pixel effect. Of course, with this method I can no longer rotate the model, but I wasn’t planning on that anyways. I just wanted the knight to be able to look down and have the talking animation. So, starting from this want, I started coding using a language called Processing - which is essentially Java, but makes stuff easier. It has its own packages, some of which look very interesting and useful.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>I only started looking at the packages after the basis of the project was up, and I was very glad - mainly because I would have gotten too many choice paralysis. Processing was great though, and is very intuitive: <a href="https://processing.org/">https://processing.org/</a> It didn’t take long to implement the basic functionality, and coding the image loading with a for loop and using the PImage data type was a good way to learn the syntax of the language. The documentation is pretty good - but I was hung up on how to make transparent images using the png export, and it turns out that’s not possible using Processing’s system. You can however write to a graphics object and save that to a file, which took me way too long to learn. I actually considered switching to another platform because of this hangup, but it ended up being able to be worked around. In addition, I got lazy and ended up just having the character in front of a green screen to be chroma keyed out later using OBS. Annoying, but still works. </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>I look forward to talking more about the functions I implemented and which aspects of the program I’m looking to improve. The github repo is linked below:</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><a href="https://github.com/funkyGalilei/pngtuberProcessing">https://github.com/funkyGalilei/pngtuberProcessing</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><br></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><br></p>
<!-- /wp:paragraph -->
