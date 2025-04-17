---
title: Quaternions - another way to view rotations
date: 2025-02-08 22:26
author: dillonsemail2012
comments: true
categories: [Engineering Projects, MATLAB]
tags:
- education
- math
- mathematics
- philosophy
- physics
---
<!-- wp:embed {"url":"https://youtu.be/idIu5ZaYSjw","type":"video","providerNameSlug":"youtube","responsive":true,"className":"wp-embed-aspect-16-9 wp-has-aspect-ratio"} -->
<figure class="wp-block-embed is-type-video is-provider-youtube wp-block-embed-youtube wp-embed-aspect-16-9 wp-has-aspect-ratio"><div class="wp-block-embed__wrapper">
https://youtu.be/idIu5ZaYSjw
</div></figure>
<!-- /wp:embed -->

<!-- wp:paragraph -->
<p>In my rigid body dynamics class at SJSU, I was tasked to create a rotation with a quaternion given Euler angles. The process of the math behind this is somewhat complex, with trig values being used to find 4 “Euler parameters”, which are in turn used to calculate the 3 lambda values (representing the quaternion vector) and the theta (the angle that the object will rotate about)</p>
<!-- /wp:paragraph -->

<!-- wp:embed {"url":"https://youtu.be/OQVqJggmVik","type":"video","providerNameSlug":"youtube","responsive":true,"className":"wp-embed-aspect-4-3 wp-has-aspect-ratio"} -->
<figure class="wp-block-embed is-type-video is-provider-youtube wp-block-embed-youtube wp-embed-aspect-4-3 wp-has-aspect-ratio"><div class="wp-block-embed__wrapper">
https://youtu.be/OQVqJggmVik
</div></figure>
<!-- /wp:embed -->

<!-- wp:paragraph -->
<p>We first started with 90 degree variants of the Euler angles for simplicity (the lambda vector pointing from the corner to corner of the graph). In addition, we hand calculated a Euler to quaternion rotation in class and did a sanity check against our MATLAB code.</p>
<!-- /wp:paragraph -->

<!-- wp:embed {"url":"https://youtube.com/shorts/6oAluOwtx7M?feature=share","type":"video","providerNameSlug":"youtube","responsive":true,"className":"wp-embed-aspect-4-3 wp-has-aspect-ratio"} -->
<figure class="wp-block-embed is-type-video is-provider-youtube wp-block-embed-youtube wp-embed-aspect-4-3 wp-has-aspect-ratio"><div class="wp-block-embed__wrapper">
https://youtube.com/shorts/6oAluOwtx7M?feature=share
</div></figure>
<!-- /wp:embed -->

<!-- wp:paragraph -->
<p>This was in a group of 3 and was a lot of fun. It was all done in matlab and the final script was not long at all. Displaying the lambda values in the title of the graphs was very satisfying, and really reminded me how important grammar and graph design is in processes like these. The final wacky variants were nice to include just because of their visual appeal :)</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":233,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://dillonsmith57.wordpress.com/wp-content/uploads/2025/02/screenshot-2025-02-08-220457.png?w=599" alt="" class="wp-image-233" /></figure>
<!-- /wp:image -->
