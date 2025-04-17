---
title: Understand Rigid Body Dynamics
date: 2025-02-09 10:32
author: dillonsemail2012
comments: true
categories: [Engineering Projects, MATLAB]
---
<!-- wp:paragraph -->
<p>This project I have featured was one of the first I solved and broke down into components in my undergraduate study. It was given the name “rocking boat”, and we were to plot the motion of a point on the boat. There were 2 systems, the Newtonian and a system labelled B. I made the graphic below which helped me orient things in my mind.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":255} -->
<figure class="wp-block-image"><img src="https://dillonsmith57.wordpress.com/wp-content/uploads/2025/02/agv_vufxsmy9zf4cg3upyztepx50xiuktkrfx3spbp6ipnjlkzlnypdj59g7u0fnukvd9anvjflpfzszswebubxon-cuh0rwwwkfiu1nmduoz-m9d23diais5lmhapnsuvozqr5txkpm7d6vtjbab16gvm69f106hb3fs2048.png" alt="" class="wp-image-255" /><figcaption class="wp-element-caption">Rocking Boat Problem</figcaption></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>We made assumptions, found the Inertia of the boat, and then found the Equations of Motion. This is some of my math below.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":257} -->
<figure class="wp-block-image"><img src="https://dillonsmith57.wordpress.com/wp-content/uploads/2025/02/agv_vucgix_gvvcot3ovagx8bnqgrjuhwufyigzqj9ke3wnyxkz0cgrw0_orbf_efgj1ffqo4m0ndpcxghhb-ypcyhh5vrhq8ydi5b7lm5fly-rkicfjvbm2ueq59ub9ihhzz46quzbdphj7dz_7pde6pjsssyl0lrvgs2048.png" alt="" class="wp-image-257" /></figure>
<!-- /wp:image -->

<!-- wp:image {"id":256} -->
<figure class="wp-block-image"><img src="https://dillonsmith57.wordpress.com/wp-content/uploads/2025/02/agv_vud6x7ls-cfo2rbqiq7xic2zqtlfgxwv3did_p3w4_v9nkmbk7zvxomcs7jafs1vpilg8ma9ipakd1sahsbaajhxhcn0rp4irioy7vv_l8bzrck72afqkd5dxwbzvp-lnopmlmyujwbxmfmn28eoqrstmygw3d0_s2048.png" alt="" class="wp-image-256" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>We ended up using Motion Genesis, a program that exclusively works with dynamic problems. Now, looking back, its a program that has a lot of training wheels and limitations, but it takes scalars and units and was a really good introduction. Using this before MATLAB with all of its corridors was nice. We then got the following outputs and made some sanity checks, choosing the situation when the boat is standing straight up. I’ve really enjoyed looking back on old work, it’s nice to see something that you’ve since gotten a lot better at. I look forward to learning more programs and languages, and building on the foundation I’ve made.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":258} -->
<figure class="wp-block-image"><img src="https://dillonsmith57.wordpress.com/wp-content/uploads/2025/02/agv_vucmipwymw4pecztttv9wcopw9vhvfptijvvvidsnxd-sr4nxyueixwwhhopyri6dftlq5nz8e7nvxmeqiah9-w8tyxubx5kumdbwtdug4tklnvkal0xrdzkjfutx7zd8icuugd2qv4fyhxzh6mtlxlohwne65is2048.png" alt="" class="wp-image-258" /><figcaption class="wp-element-caption">super simple code that gave us a nice output</figcaption></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Here were some of our outputs from Motion Genesis</p>
<!-- /wp:paragraph -->

<!-- wp:jetpack/slideshow {"ids":[253,252,251],"sizeSlug":"large"} -->
<div class="wp-block-jetpack-slideshow aligncenter" data-effect="slide"><div class="wp-block-jetpack-slideshow_container swiper-container"><ul class="wp-block-jetpack-slideshow_swiper-wrapper swiper-wrapper"><li class="wp-block-jetpack-slideshow_slide swiper-slide"><figure><img alt="" class="wp-block-jetpack-slideshow_image wp-image-253" data-id="253" src="https://dillonsmith57.wordpress.com/wp-content/uploads/2025/02/unnamed.png?w=1024" /></figure></li><li class="wp-block-jetpack-slideshow_slide swiper-slide"><figure><img alt="" class="wp-block-jetpack-slideshow_image wp-image-252" data-id="252" src="https://dillonsmith57.wordpress.com/wp-content/uploads/2025/02/unnamed-2.png?w=1024" /></figure></li><li class="wp-block-jetpack-slideshow_slide swiper-slide"><figure><img alt="" class="wp-block-jetpack-slideshow_image wp-image-251" data-id="251" src="https://dillonsmith57.wordpress.com/wp-content/uploads/2025/02/unnamed-1.png?w=1024" /></figure></li></ul><a class="wp-block-jetpack-slideshow_button-prev swiper-button-prev swiper-button-white" role="button"></a><a class="wp-block-jetpack-slideshow_button-next swiper-button-next swiper-button-white" role="button"></a><a aria-label="Pause Slideshow" class="wp-block-jetpack-slideshow_button-pause" role="button"></a><div class="wp-block-jetpack-slideshow_pagination swiper-pagination swiper-pagination-white"></div></div></div>
<!-- /wp:jetpack/slideshow -->
