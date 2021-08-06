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
To create wave simulations I created a 2D array of spheres, then altered set the height of each sphere based on a wave equation of the form: 

$$
\\ y=A\sin(kx-\omega t) \\
$$

These waves can be summed to create shaped waves using finite <a href="/sebsite/fourier">fourier series</a> as shown:
<div class="gallery2">
    <figure class="gallery__item">
        <video autoplay loop muted playsinline src="/sebsite/images/dots_sine_loop.mp4" class="gallery__img"></video> 
        <figcaption>Sine wave</figcaption>
    </figure>
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
    <figure class="gallery__item">
        <video autoplay loop muted playsinline src="/sebsite/images/dots_94_2diff_freq.mp4" class="gallery__img"></video> 
        <figcaption>2 waves interfering</figcaption>
    </figure><figure class="gallery__item">
        <video autoplay loop muted playsinline src="/sebsite/images/dots_95_4diff_freq.mp4" class="gallery__img"></video> 
        <figcaption>4 waves interfering</figcaption>
    </figure>
</div>
    
## Other
I have also made other animations using assorted methods to define the spheres movements:
<div class="gallery2">
    <video autoplay loop muted playsinline src="/sebsite/images/dots3.mp4" class="gallery__img"></video> 
    <video autoplay loop muted playsinline src="/sebsite/images/dots_86_increase_frequency.mp4" class="gallery__img"></video> 
    <video autoplay loop muted playsinline src="/sebsite/images/dots_93_crosswaves.mp4" class="gallery__img"></video> 
    <video autoplay loop muted playsinline src="/sebsite/images/dots_57_sheet.mp4" class="gallery__img"></video> 
    <video autoplay loop muted playsinline src="/sebsite/images/dots_58_plaid.mp4" class="gallery__img"></video> 
</div>


## 3D waves
The next obvious step was to upgrade to 3D waves and other patterns:
Defining the waves in 3d was much more complicated as each sphere needs to move towards and away from the origin of the wave, so each sphere is moving in a unique direction, rather than just up and down. The equations I devised are:

$$
x=A\frac{x_g-x_o}{d}\sin(kd-\omega t)  \\
y=A\frac{y_g-y_o}{d}\sin(kd-\omega t)  \\
z=A\frac{z_g-z_o}{d}\sin(kd-\omega t)  \\
$$

Where $$(x_g,y_g,z_g)$$ is the grid position of the sphere, and $$(x_o,y_o,z_o)$$ is the position of the wave's origin and $$d$$ is the distance between the origin of the wave and grid position of the sphere. These displacements can also be summed to simulate interference between several waves. 

<div class="gallery2">
    <video autoplay loop muted playsinline src="/sebsite/images/dots_85_center_wave_good.mp4" class="gallery__img"></video> 
    <video autoplay loop muted playsinline src="/sebsite/images/dots_77_4_interference_diff_freq.mp4" class="gallery__img"></video> 
    <video autoplay loop muted playsinline src="/sebsite/images/dots_63_cube_pulse_in.mp4" class="gallery__img"></video> 
    <video autoplay loop muted playsinline src="/sebsite/images/dots_72_pulsing_wave.mp4" class="gallery__img"></video> 
    <video autoplay loop muted playsinline src="/sebsite/images/dots6.mp4" class="gallery__img"></video> 
    <video autoplay loop muted playsinline src="/sebsite/images/dots7.mp4" class="gallery__img"></video> 
</div>

