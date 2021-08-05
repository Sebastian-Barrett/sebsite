---
layout: default
title: Rendering
permalink: /rendering
---

# Rendering
> Rendering engine + python = cool videos

I use [POV-Ray rendering](http://www.povray.org/) to render scenes that I created using [python](/sebsite/python) and a [POV-Ray python library](https://github.com/Zulko/vapory). In python I control the positions of an array of spheres using math to model them into 2D and 3D waves or [parametric curves](/sebsite/parametric). The positions of the balls vary slowly over time to create hundreds of individual frames, which I combine into videos using python.  The colors of the balls are altered by height or density or their ball number, to make them look better.  

## Moving dots
The idea to create videos of moving dots was based on my previous work on [parametric curves](/sebsite/parametric) and my desire to learn more python.

All of the spheres follow parametric path, slightly faster than the previous sphere. It is simple but it can create some pretty emergent behavior. 
<div class="gallery2">
    <figure class="gallery__item">
        <video autoplay loop muted playsinline src="/sebsite/images/dots1.mp4" class="gallery__img"></video> 
        <figcaption>3D parametric</figcaption>
    </figure>
    <figure class="gallery__item">
        <video autoplay loop muted playsinline src="/sebsite/images/dots4.mp4" class="gallery__img"></video> 
        <figcaption>2D parametric</figcaption>
    </figure>
    <figure class="gallery__item">
        <video autoplay loop muted playsinline src="/sebsite/images/dots5.mp4" class="gallery__img"></video> 
        <figcaption>2D parametric</figcaption>
    </figure>
    <figure class="gallery__item">
        <video autoplay loop muted playsinline src="/sebsite/images/dots2.mp4" class="gallery__img"></video> 
        <figcaption>Many circular paths</figcaption>
    </figure>
</div>


## 2D waves

<div class="gallery2">
    <figure class="gallery__item">
        <video autoplay loop muted playsinline src="/sebsite/images/dots_sine_loop.mp4" class="gallery__img"></video> 
        <figcaption>Sine wave</figcaption>
    </figure>
    <figure class="gallery__item">
        <video autoplay loop muted playsinline src="/sebsite/images/dots_3waves_loop.mp4" class="gallery__img"></video> 
        <figcaption>3 sine waves</figcaption>
    </figure>
    <figure class="gallery__item">
        <video autoplay loop muted playsinline src="/sebsite/images/dots_sawtooth_loop.mp4" class="gallery__img"></video>     
        <figcaption>Sawtooth wave</figcaption>
    </figure>
    <figure class="gallery__item">
        <video autoplay loop muted playsinline src="/sebsite/images/dots_triangle_loop.mp4" class="gallery__img"></video> 
        <figcaption>Triangle wave</figcaption>
    </figure>
    <figure class="gallery__item">
        <video autoplay loop muted playsinline src="/sebsite/images/dots_spike_loop.mp4" class="gallery__img"></video> 
        <figcaption>Spike wave</figcaption>
    </figure>
    <figure class="gallery__item">
        <video autoplay loop muted playsinline src="/sebsite/images/dots_square_loop.mp4" class="gallery__img"></video>    
        <figcaption>Square wave</figcaption>
    </figure>
</div>
    
## 3D waves
<video autoplay loop muted playsinline src="/sebsite/images/dots_85_center_wave_good.mp4" width="512" height="384"></video>

## Water simulations

## Unit cell models