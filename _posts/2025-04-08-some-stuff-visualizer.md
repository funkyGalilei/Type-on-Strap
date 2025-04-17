---
title: some stuff Visualizer
date: 2025-04-08 01:57
comments: true
categories: [Creativity, Processing, Programming]
---
<!-- wp:paragraph -->
<p>I wanted to make a quick video stinger for a youtube video, so I made a visual that was subdued but still a little interesting. I had an idea to have some shapes float around in a bubble, and it pretty much stayed the same throughout the whole process.<br></p>
<!-- /wp:paragraph -->

<!-- wp:embed {"url":"https://youtube.com/shorts/Mb5klCMAhLw?feature=share","type":"video","providerNameSlug":"youtube","responsive":true,"className":"wp-embed-aspect-4-3 wp-has-aspect-ratio"} -->
<figure class="wp-block-embed is-type-video is-provider-youtube wp-block-embed-youtube wp-embed-aspect-4-3 wp-has-aspect-ratio"><div class="wp-block-embed__wrapper">
https://youtube.com/shorts/Mb5klCMAhLw?feature=share
</div></figure>
<!-- /wp:embed -->

<!-- wp:paragraph -->
<p>This project really helped me fully understand and use classes in Processing, and classes as a concept. I first used the classes data type to make a grid, which proved easy enough to define in the main function with 2 for loops. I then wanted the grid points to only be within a circle, where I would be drawing a circle with a wide stroke to provide some separation. This was also pretty straightforward after looking up the equation of the interior of the circle (I should’ve had this memorized from geometry in high school, but ya know) and there I had my grid in a circle. <br></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph {"className":"is-style-text-annotation","fontSize":"medium"} -->
<p class="is-style-text-annotation has-medium-font-size">*I also ended up making a boolean variable called inCircle in the class, and just didn’t draw anything to the canvas if the var was false. There is probably a better way of doing this, since those computations don’t go anywhere, but the nice side of this visual light coding is that performance is basically irrelevant at this scale.<br></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>After this, I just needed to draw a shape to those grid points. I decided I wanted the type of shape (rectangle, triangle, or a rectangle), the size, and the color to be variable. Speaking of the color, I didn’t manually code the combinations but instead used a color library named Color Harmony. It’s great, and I got some of the ideas from the examples listed <a href="http://cagewebdev.com/colorharmony-processing-library/#:~:text=ColorHarmony%20is%20a%20Processing.org,%2Dtime%2C%20in%20Processing%20sketches.">here</a>:<br></p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":367,"width":"346px","height":"auto","sizeSlug":"full","linkDestination":"none","align":"left"} -->
<figure class="wp-block-image alignleft size-full is-resized"><img src="https://dillonsmith57.wordpress.com/wp-content/uploads/2025/04/0013.png" alt="" class="wp-image-367" style="width:346px;height:auto" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>For the update function, I wanted the shapes to breathe a little bit by getting bigger and smaller slowly. Sin curves are the best. I had no idea before I started using Blender or animating things that sin waves are so so so useful when it comes to giving anything a little bit of natural motion.&nbsp;</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>After that stuff, the last thing to do was to add some wrapped text around the circle. Which wasn’t as elementary as I thought it was going to be. I plan on animating the text around the circle, and I’ll be able to speak on it more then. I honestly just found an example <a href="http://learningprocessing.com/examples/chp17/example-17-08-textalongcurve">here </a>that I pretty much just ripped and it worked well. Sometimes that’s what you gotta do coding haha. Most of the time though I attempt to write it myself, even with a reference so my brain will remember it more for next time. <br></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Anyway, I hope to make improvements on the code in a bunch of ways, and develop some quick parameters that can be changed in a separate window. That way, I could develop a bunch of stingers that would be a unique outro every time! :) <br></p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>class Module {
  float x;
  float y;
  color randColor;
  float size;
  boolean inCircle;
  int shape;
  float phase;
  
  // Constructor
  Module(float xTemporary, float yTemporary, boolean inCircleTemp, float offset) {
    x = xTemporary - offset;
    y = yTemporary - offset;
    inCircle = inCircleTemp;
    
    randColor = colors&#091;(int)random(8)];
    //size = random(20.0, 40.0); // with 15
    size = random(40.0, 70.0);
    shape = int(round(random(1, 3))); // 1 for circle, 2 for rect(), 3 for triangle
    phase = random(0, 10);
  }
  
  void update() {
    float amplitude = .4;
    size = sin(time + phase) * amplitude + size;
    //time = time + 0.00005;
    time = time + 0.00003;

  }
  
  void display() {

    if (inCircle) {
        fill(randColor);
        if (shape == 1) {
          ellipse(x, y, size + 10, size + 10);
        } else if (shape == 2) {
          rect(x, y, size, size);
        } else if (shape == 3) {
          float triFactor = 0.6;
          triangle(x, y, x-size*triFactor, y-size*triFactor, x+size*triFactor, y-size*triFactor);
        }
    } else {
        //fill(25);
        //ellipse(x, y, 10, 10);
    }
  }
}
</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p><a href="https://github.com/funkyGalilei/someStuffVisualizer">https://github.com/funkyGalilei/someStuffVisualizer</a></p>
<!-- /wp:paragraph -->
