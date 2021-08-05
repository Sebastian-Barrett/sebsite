---
layout: default
title: Rendering
permalink: /rendering
---

# Rendering
> Rendering engine + python = cool videos

I use [POV-Ray rendering](http://www.povray.org/) to render scenes that I created using [python](/sebsite/python) and a [POV-Ray python library](https://github.com/Zulko/vapory). With python I can control the spheres position and color in way that I can describe in code. The positions and colors of the balls vary slowly over time to create hundreds of individual frames, which I combine into videos using python. The colors of the balls are controlled by height, density or time.   

## Moving dots
The idea to create videos of moving dots was based on my previous work on [parametric curves](/sebsite/parametric) and my desire to learn more python.

All of the spheres follow a parametric path, slightly faster than the previous sphere. It is simple but it can create some pretty emergent behavior. 

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
<div  class="clearfix">
    <figure class="rightfloat">
        <video autoplay loop muted playsinline src="/sebsite/images/dots_sine_loop.mp4" class="gallery__img"></video> 
        <figcaption>Sine wave</figcaption>
    </figure>
    <p>To create wave simulations I created a 2D array of spheres, then altered set the height of each sphere based on a wave equation of the form: </p>
    $$
    \\ y=A\sin(kx-\omega t) \\
    $$
    <p>These waves can be summed create shaped waves using finite <a href="https://mathworld.wolfram.com/FourierSeries.html" target="_blank">fourier series</a> as seen:</p>
</div>
<div class="gallery2">
    <figure class="gallery__item">
        <video autoplay loop muted playsinline src="/sebsite/images/dots_half_sine_loop.mp4" class="gallery__img"></video> 
        <figcaption>Half sine wave</figcaption>
    </figure>
    <figure class="gallery__item">
        <video autoplay loop muted playsinline src="/sebsite/images/dots_sawtooth_loop.mp4" class="gallery__img"></video>     
        <figcaption>Sawtooth wave</figcaption>
    </figure>
    <figure class="gallery__item">
        <video autoplay loop muted playsinline src="/sebsite/images/dots_square_loop.mp4" class="gallery__img"></video>    
        <figcaption>Square wave</figcaption>
    </figure>
    <figure class="gallery__item">
        <video autoplay loop muted playsinline src="/sebsite/images/dots_triangle_loop.mp4" class="gallery__img"></video> 
        <figcaption>Triangle wave</figcaption>
    </figure>
    <figure class="gallery__item">
        <video autoplay loop muted playsinline src="/sebsite/images/dots_3waves_loop.mp4" class="gallery__img"></video> 
        <figcaption>3 sine waves</figcaption>
    </figure>
    <figure class="gallery__item">
        <video autoplay loop muted playsinline src="/sebsite/images/dots_spike_loop.mp4" class="gallery__img"></video> 
        <figcaption>Spike wave</figcaption>
    </figure>
</div>

Alternatively the waves can be summed to show interfere waves from different sources:
<div class="gallery2">
    <figure class="gallery__item">
        <video autoplay loop muted playsinline src="/sebsite/images/dots_87_double_slit.mp4" class="gallery__img"></video> 
        <figcaption>Double slit</figcaption>
    </figure>

</div>
    
## Other
I have also made other animations using assorted methods to define the spheres movements:
<div class="gallery2">
    <figure class="gallery__item">
        <video autoplay loop muted playsinline src="/sebsite/images/dots3.mp4" class="gallery__img"></video> 
    </figure>
    <figure class="gallery__item">
        <video autoplay loop muted playsinline src="/sebsite/images/dots_86_increase_frequency.mp4" class="gallery__img"></video> 
    </figure>
    <figure class="gallery__item">
        <video autoplay loop muted playsinline src="/sebsite/images/dots_93_crosswaves.mp4" class="gallery__img"></video> 
    </figure>
    <figure class="gallery__item">
        <video autoplay loop muted playsinline src="/sebsite/images/dots_57_sheet.mp4" class="gallery__img"></video> 
    </figure>
    <figure class="gallery__item">
        <video autoplay loop muted playsinline src="/sebsite/images/dots_58_plaid.mp4" class="gallery__img"></video> 
    </figure>
</div>


## 3D waves
The next obvious step was to upgrade to 3D waves and other patterns:
Defining the waves in 3d was much more complicated as each sphere needs to move towards and away from the origin of the wave, so each sphere is moving in a unique direction, rather than just up and down. The equations I devised are:

$$
x=A\frac{x_g-x_o}{d}\sin(kd-\omega t)  \\
y=A\frac{y_g-y_o}{d}\sin(kd-\omega t)  \\
z=A\frac{z_g-z_o}{d}\sin(kd-\omega t)  \\
$$

Where $$(x_g,y_g,z_g)$$ is the grid position of the sphere, and $$(x_o,y_o,z_o)$$ is the position of the wave's origin and $$d$$ is the distance between the origin of the wave and grid position of the sphere.

<div class="gallery2">
    <figure class="gallery__item">
        <video autoplay loop muted playsinline src="/sebsite/images/dots3.mp4" class="gallery__img"></video> 
    </figure>
</div>

## Water simulations

## Unit cell models