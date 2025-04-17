---
title: Simulating a Hohmann Transfer
date: 2025-02-08 23:12
comments: true
categories: [astronomy, Engineering Projects, MATLAB]
tags:
- nasa
- news
- science
- space
---
<!-- wp:paragraph -->
<p>This was a fun and interesting project I did around orbital dynamics, and a Hohmann Transfer with Impulsive Burns (the math gets more complicated with finite, steady burns). This setup is about the simplest way to view a transition from 2 separate orbits, since the eccentricity is 1 (a circle) and the burn is along the tangent of the circle. Another way of saying a circular orbit is to say a geostationary orbit, or one that “hovers above only 1 location on a body.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":238,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://dillonsmith57.wordpress.com/wp-content/uploads/2025/02/hohmann-transfer.png?w=758" alt="" class="wp-image-238" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Additionally, often this transfer method uses the least amount of impulse, and has a longer transition period than other transitions.</p>
<!-- /wp:paragraph -->

<!-- wp:embed {"url":"https://youtube.com/shorts/_AlcNpZZ0mQ?feature=share","type":"video","providerNameSlug":"youtube","responsive":true,"className":"wp-embed-aspect-4-3 wp-has-aspect-ratio"} -->
<figure class="wp-block-embed is-type-video is-provider-youtube wp-block-embed-youtube wp-embed-aspect-4-3 wp-has-aspect-ratio"><div class="wp-block-embed__wrapper">
https://youtube.com/shorts/_AlcNpZZ0mQ?feature=share
</div></figure>
<!-- /wp:embed -->

<!-- wp:paragraph -->
<p>To attach real scalars to this problem, we chose to model NASA’s DART system, and found that its mass was around 610 kg. From this, we found delta V, or the difference or change in velocity to be 2.83 km/s. This calculation was very straightforward. Creating the animation was an interesting challenge. We tackled the problem in a piecewise manner, first simulating the lower orbit, then the transfer path and then the higher circular orbit. We then switched between them with the solved time to create one seamless animation. I’ve seen other animations on <a href="https://en.wikipedia.org/wiki/Hohmann_transfer_orbit">Wikipedia </a>that have a body on each path, which is another route we could have gone for. All in all, I appreciated this project, and understood how complicated orbital dynamics can get. The jump from Impulsive to Finite burn is significant, and creating code from the ground up requires a solid understanding. </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>I hope to soon familiarize myself with ANSYS STK, and use already built orbital dynamic systems to explore other situations involving space :)<br></p>
<!-- /wp:paragraph -->
