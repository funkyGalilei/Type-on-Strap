---
title: Calculating the Deformation of a Simple Beam under a Distributed Load
date: 2023-02-27 23:08
author: dillonsemail2012
comments: true
categories: [Engineering Projects, MATLAB]
---
<!-- wp:paragraph -->
<p>This was a part of an assignment for my AE 114 class, which deals with structures. This problem was possible to do in excel with recursive formulas, but I like having all the moving parts be explicit in a script, along with the annotations on the graphs you can do inside the code. I was really proud of the highlighting of the max bending point on all the graphs, because that was one of the requirements for the homework assignment. Weirdly enough, printing out the statement declaring the maximum deflection at the end was the hardest part lol. I say that because while learning most programming languages, tutorials take you through printing a statement first. This wasn’t the case in MATLAB (at least for me). I hope this shows what I’ve been up to in my 114! :)</p>
<!-- /wp:paragraph -->

<!-- wp:separator -->
<hr class="wp-block-separator has-alpha-channel-opacity" />
<!-- /wp:separator -->

<!-- wp:jetpack/slideshow {"align":"","ids":[120,121,122,123],"sizeSlug":"large"} -->
<div class="wp-block-jetpack-slideshow" data-effect="slide"><div class="wp-block-jetpack-slideshow_container swiper-container"><ul class="wp-block-jetpack-slideshow_swiper-wrapper swiper-wrapper"><li class="wp-block-jetpack-slideshow_slide swiper-slide"><figure><img alt="" class="wp-block-jetpack-slideshow_image wp-image-120" data-id="120" src="https://dillonsmith57.wordpress.com/wp-content/uploads/2023/02/beaminbending-1.png?w=605" /></figure></li><li class="wp-block-jetpack-slideshow_slide swiper-slide"><figure><img alt="" class="wp-block-jetpack-slideshow_image wp-image-121" data-id="121" src="https://dillonsmith57.wordpress.com/wp-content/uploads/2023/02/beaminbending1-1.png?w=700" /></figure></li><li class="wp-block-jetpack-slideshow_slide swiper-slide"><figure><img alt="" class="wp-block-jetpack-slideshow_image wp-image-122" data-id="122" src="https://dillonsmith57.wordpress.com/wp-content/uploads/2023/02/beaminbending2-1.png?w=700" /></figure></li><li class="wp-block-jetpack-slideshow_slide swiper-slide"><figure><img alt="" class="wp-block-jetpack-slideshow_image wp-image-123" data-id="123" src="https://dillonsmith57.wordpress.com/wp-content/uploads/2023/02/beaminbending3-1.png?w=700" /></figure></li></ul><a class="wp-block-jetpack-slideshow_button-prev swiper-button-prev swiper-button-white" role="button"></a><a class="wp-block-jetpack-slideshow_button-next swiper-button-next swiper-button-white" role="button"></a><a aria-label="Pause Slideshow" class="wp-block-jetpack-slideshow_button-pause" role="button"></a><div class="wp-block-jetpack-slideshow_pagination swiper-pagination swiper-pagination-white"></div></div></div>
<!-- /wp:jetpack/slideshow -->

<!-- wp:code {"fontSize":"small"} -->
<pre class="wp-block-code has-small-font-size"><code>
%% Calculating Shear Stress, Bending Moment, Axial Stress, &amp; Deformation for a Simply Supported Beam under a distributed load
% - written by Dillon Smith
% 
% valid for rectangular distribtued loads
%% 
% * V = Vprev +f*(delta x) + R
% * M  = Vprev *(delta x) + Mprev + f *(delta x)^2/2
% * Ix = 1/12 b h^3
% * d^2w/dx^2 = M/E*I
%% 
% Inputs for Shear and bending placed right at the top of the code

n = 150; % number of steps
totalX = 15; % total length of the beam
deltaX = totalX/n;

% % to be able to calculate the number of steps it takes to get to some
% % distance to potentially add a for loop
% distanceToFirstCut = 5;
% % m is the earlier n (for i = 2:m, for i = m:n)
% m = distanceToFirstCut/deltaX; 

% just preallocating
V = zeros(n, 1);
M = zeros(n, 1);
R = zeros(n, 1); 

% defining initial values
V(1) = 1800;
M(1) = -6000;
R(1) = 0; % Reaction force
% distributed load value
f = -200;
% Shear and Bending
%% 
% * recursive formulas that require a for loop


x = linspace(0, totalX, n);

% this for loop is valid for one component of the beam, i e from the left
% most part of the beam to the first cut
for i = 2:n
    V(i) = V(i-1) + f.*deltaX + R(i);
    M(i) = V(i-1).*deltaX + M(i-1) + (f .* deltaX .^2)/2;
end
% outputting figure
figure(1)
plot(x, V, "LineWidth",2,"color", "black")
xlabel("Distance (in)")
ylabel("Shear Force (lb)")
title("Shear Force Across the Beam")
set(gca,"XGrid","off","YGrid","on")
&#091;maxShearStress, index] = max(V,&#091;],'ComparisonMethod','abs');
hold on
plot(x(index), maxShearStress, "ro", "LineWidth",2, "MarkerSize",11)
hold off

figure(2)
plot(x, M, "LineWidth",2,"color", "black")
ylabel("Bending Moment (lb* in)")
xlabel("Distance (in)")
title("Bending Moment Across the Beam")
% Max Axial Stress

% inertia from given cross section
b = 3; % in inches
h = 6;
I = 1/12 *b*h^3; % in in^4
y = h/2; % only for a rectangle
&#091;maxBendingMoment, index] = max(M,&#091;],'ComparisonMethod','abs');
hold on
plot(x(index), maxBendingMoment, "ro", "MarkerSize",11, "LineWidth",2)
set(gca,"XGrid","off","YGrid","on")
hold off
maxSigma = y .* maxBendingMoment/I;
% Vertical Deformation
%% 
% * there's no for loop required, because the equation is not recursive, w will 
% just for another matrix on top of x

E = 10400000; % for Aluminum 7075-T6
M1 = 6000; % moment at the left of the beam, in lbs*ft
M2 = -1500; % moment at the right
w = 200; % in lbs/ft
L = totalX; % its just shorter

% y is vertical displacement
y = (1/(E*I))*((-w/24*x.^4 + (x.^3)/6*(w*L/2+(M2 + M1)/L) - M1/2*x.^2) + (-w/24*L^4+ 1/6*(w*L/2+(M2+M1)/L)*L^3 - M1/2*L^2)*(1/(-L)).*x);

&#091;maxDisplacement, index] =  max(y,&#091;],'ComparisonMethod','abs');
maxDisplacementIn = maxDisplacement * 12; % conversion to inches
displacementIn = y .* 12; % this is for the not to scale plot
whereMaxDisplacement = index * deltaX;

figure(3)
plot(x, y, "LineWidth",8, "Color","black")
hold on
plot(x(index), maxDisplacement, "o", "MarkerSize",10, "LineWidth",2, "color", "magenta")
% just a baseline to maybe seee variations easier at scale
line(&#091;0 15], &#091;0 0], 'Color','red','LineStyle','--')
hold off
% below is just formatting
axis(&#091;0 totalX -totalX totalX])
set(gca,"XGrid","off","YGrid","on")
yticks(&#091;-15 -1 0 1 15])
yticklabels({'15', '-1', 'midline', '1', '15'})
ylabel("Displacement (ft)")
xlabel("Distance (ft)")
title("Vertical Deformation (To Scale)")

figure(4)
plot(x, displacementIn,"Color","black", "LineWidth", 4)

% axis(&#091;0 totalX -maxDisplacementIn*1.1 maxDisplacementIn*1.1])
ylabel("Displacement (in)")
xlabel("Distance (ft)")
title("Vertical Deformation (Not To Scale)")
hold on
plot(x(index), maxDisplacementIn, "o", "MarkerSize",10, "LineWidth",2, "color", "magenta")
line(&#091;0 15], &#091;0 0], 'Color','red','LineStyle','--')
hold off
%%
whatIwantToSay = "The maximum displacement this beam undergoes is\n%0.9f inches, at %1.2f inches along the beam";
fprintf(whatIwantToSay, maxDisplacementIn, whereMaxDisplacement)</code></pre>
<!-- /wp:code -->
