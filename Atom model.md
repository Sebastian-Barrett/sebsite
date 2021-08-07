---
layout: default
title: Atom model
permalink: /atommodel
---

# Atom models
Based on my work with [rendering](/sebsite/rendering) and my interest in computational chemistry I decided to try simple modeling of the behavior of ions and molecules. 

## Ion model
<div class="clearfix">
<iframe src="https://www.desmos.com/calculator/muhzqughnh?embed" class="rightfloat" height="250" style="border: 1px solid #ccc" frameborder=0></iframe>
<p>To start I used a simple model with positive and negative ions, that are attracted to the opposite polarity. I also included a stronger, shorter range force to represent nuclear repulsion that prevents ions from colliding. The graph shows the force curves for similar and oppositely charged ions from this equation.</p> 

$$
F=-\frac{k_1q_1q_1}{r^2} - \frac{k_2}{r^6}
$$
</div>

<div class="clearfix">
<iframe src="https://www.desmos.com/calculator/rutrkqvxan?embed" class="rightfloat" height="250" style="border: 1px solid #ccc" frameborder=0></iframe>

<p>Then I created several ions each with position, velocity and acceleration represented as vectors. I changed time in small steps, and each time step I determined the acceleration by summing the forces from all the other ions. Then I altered the velocity using the acceleration and the position using the velocity. This means that I am approximating a smooth movement path with a series small linear jumps as represented in the second <a href="https://www.desmos.com/calculator/nkzwpv0hxu">graph</a>, only with finer steps.</p>
</div>

Then I rendered each of the time steps to create individual video frames and combined them into a video. I also constricted the ions to boxes to stop them from flying away and I had to break the conservation of energy to get stable results. It took a lot of trial and error to create something that look interesting but eventually I was able to observe behaviors like the formation of pairs, chains and even a lattice. 

<div class="gallery2">
    <video autoplay loop muted playsinline src="/sebsite/images/ion_animation_4.mp4" class="gallery__img"></video> 
    <video autoplay loop muted playsinline src="/sebsite/images/ion_animation_12_chain.mp4" class="gallery__img"></video> 
    <video autoplay loop muted playsinline src="/sebsite/images/ion_animation_14_form_cube.mp4" class="gallery__img"></video> 
    <video autoplay loop muted playsinline src="/sebsite/images/ion_animation_21.mp4" class="gallery__img"></video> 
</div>

## Water model
The obvious next step from ions was molecules, so I chose the basic water molecule. This was a lot more complicated to create because I had to deal with angular rotation and momentum (I taught myself lots of math and physics). I represented water with 3 ions with fixed relative positions. Every time step I went through the process of calculating:
1. Forces on each ion in each water
2. Torque and attractive force 
3. Angular velocity and velocity
4. Rotation and position 

As always it took lots of trial and error, and I have included some of the errors here:

<div class="gallery2">
    <video autoplay loop muted playsinline src="/sebsite/images/H2O_animation_1.mp4" class="gallery__img"></video> 
    <video autoplay loop muted playsinline src="/sebsite/images/H2O_animation_3.mp4" class="gallery__img"></video> 
    <video autoplay loop muted playsinline src="/sebsite/images/H2O_animation_6.mp4" class="gallery__img"></video> 
    <video autoplay loop muted playsinline src="/sebsite/images/H2O_animation_11_join.mp4" class="gallery__img"></video> 
</div>

And here are the better ones:
<div class="gallery2">
    <video autoplay loop muted playsinline src="/sebsite/images/H2O_animation_17_bonding.mp4" class="gallery__img"></video> 
    <video autoplay loop muted playsinline src="/sebsite/images/H2O_animation_18_bonding.mp4" class="gallery__img"></video> 
</div>

## Unit cell models
I did materials science and one assignment asked for atomic lattice sketches, so in my typical overcomplicated style I decided to render them instead of draw them. 

