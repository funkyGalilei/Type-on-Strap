---
title: Audio Visualizer in Processing
date: 2025-04-07 19:22
comments: true
categories: [Creativity, Processing, Programming]
tags:
- Audio Visual
- music
---
<!-- wp:paragraph -->
<p>Audio Visualizers! They’re a lot of fun! And Programming is fun to me. Especially when it helps visualize some audio. I tend to start at one place programming, and then add on a bunch for functionality and turn a quick thing into a more fleshed out project that takes a lot more effort (I didn’t even want to add this project to a github repo because I thought it was going to be short, but then it ballooned so I figure I should add it now lol).<br></p>
<!-- /wp:paragraph -->

<!-- wp:embed {"url":"https://youtu.be/CTx1wEagYPE","type":"video","providerNameSlug":"youtube","responsive":true,"className":"wp-embed-aspect-16-9 wp-has-aspect-ratio"} -->
<figure class="wp-block-embed is-type-video is-provider-youtube wp-block-embed-youtube wp-embed-aspect-16-9 wp-has-aspect-ratio"><div class="wp-block-embed__wrapper">
https://youtu.be/CTx1wEagYPE
</div></figure>
<!-- /wp:embed -->

<!-- wp:paragraph -->
<p>The start of this one began with the png tuber project, and creating an ellipse that would travel up and down based on the intensity of the noise input. I combined this with noise from a sound file, and then that was the start of the visualizer.&nbsp;<br></p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":333,"sizeSlug":"full","linkDestination":"none","align":"right"} -->
<figure class="wp-block-image alignright size-full"><img src="https://dillonsmith57.wordpress.com/wp-content/uploads/2025/04/smino0443.png" alt="" class="wp-image-333" /><figcaption class="wp-element-caption">Caption: Outputting a 1080x1920 panel actually proved to be a challenge - I was having weird audio sync issues so instead of using Movie Maker and the individual png outputs, I was recording with OBS. However, I couldn’t output that size naturally so it couldn’t fit on screen! There’s a workaround though, so I’ll fix this in the future</figcaption></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>To make it more visually interesting, I changed the mapping of the colors to the intensity of the sound, while having the colors slowly shift over time. I had the location be affected horizontally as well, and had the vertical motion be constant and reset when it reaches the bottom.&nbsp;<br></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>In the future, I definitely want to involve pitch as well (its built into processing’s sound library) and add some more effects. I had an idea where if the noise was almost max (.9 or more), the visualization could switch “modes” and maybe be remapped to travel differently, or have the color switch to black and white only, or add waves or whatever. I’ve seen some rather impressive tutorials and examples, so I know the sky's the limit. I also might learn how to use Touch Designer, which is a software package that is node based, and can work with Python apparently. Effects from that program would probably be a lot more formed, but the good thing with writing this code in Processing is that it's FAST. Which is important if you’re doing in-real-time things, and stuff is difficult to just brute force in Blender or other programs. I still look forward to trying it out though! :-)</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><a href="https://github.com/funkyGalilei/audioVisualProcessing">https://github.com/funkyGalilei/audioVisualProcessing</a></p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>void drawCircle(float fillColor, float brightness, float size, float x, float y) {
    
  fill(fillColor, 255, brightness );
  stroke(fillColor + 10, 255, brightness + 10);
  strokeWeight(30);
  circle(x, y, size);
}</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p></p>
<!-- /wp:paragraph -->
