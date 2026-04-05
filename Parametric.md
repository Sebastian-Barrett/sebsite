---
layout: default
title: Parametric
permalink: /parametric
---

# Parametric curves

Parametric curves are curve where the x and y positions are defined by functions eg. $$(\cos(3t),\sin(2t))$$. I have used them for years to make interesting patterns and animations with [desmos](https://www.desmos.com/calculator) and [python](/sebsite/python). I use them in [laser cutting](/sebsite/laser), [rendering](/sebsite/rendering), [puzzle box](/sebsite/puzzlebox) and the sebsite logo.

## Desmos dots
<div class="clearfix">
    <p>The first thing I did with parametric functions was in <a href="https://www.desmos.com/calculator">desmos</a>, a graphing calculator. I defined a parametric curve as a path and them made a lot of points follow that path all at slightly faster speeds. This is a simple definition that creates beautiful emergent behaviors. You can change the parameters in the graph <a href="https://www.desmos.com/calculator/vdyulhrk8k" target="_blank">here</a>.</p>
</div>

<div class="gallery2">
    <video autoplay controls muted playsinline src="/sebsite/images/desmosdots1.mp4" class="gallery__img"></video> 
    <video controls muted playsinline src="/sebsite/images/desmosdots2.mp4" class="gallery__img"></video> 
    <video controls muted playsinline src="/sebsite/images/desmosdots3.mp4" class="gallery__img"></video> 
    <video controls muted playsinline src="/sebsite/images/desmosdots4.mp4" class="gallery__img"></video> 
    <video controls muted playsinline src="/sebsite/images/desmosdots5.mp4" class="gallery__img"></video> 
</div>

## Rendering 
<div class="clearfix">
    <video autoplay loop muted playsinline src="/sebsite/images/dots1.mp4" class="rightfloat"></video> 
    <blockquote>Python + rendering engine > graphing calculator</blockquote>
    <p>When I started teaching myself python I quickly realized I could do so much more than with a graphing calculator, which lead to me finding a rendering engine to use with python. I did some of the same 2D things, but was also able to expand into 3D parametric curves and model waves in 2D planes and 3D volumes. Look at some of these renderings on my <a href="/sebsite/rendering">rendering</a> page.</p>
</div>
<div class="gallery2">
    <video autoplay loop muted playsinline src="/sebsite/images/dots2.mp4" class="gallery__img"></video> 
    <div>
        <video autoplay loop muted playsinline src="/sebsite/images/dots3.mp4" class="gallery__img"></video> 
        <caption>Every ball moves in a circle, and the outer balls circle faster than the inner balls.</caption> 
    </div>
</div>


## Python DXF
I wanted to <a href="/sebsite/laser">laser cut</a> some of the parametric curves so I found a method to turn equations into a DXF file using a python module called <a href="https://ezdxf.readthedocs.io/en/stable/" target="_blank">ezdxf</a>. The first version worked by approximating parametric curves using a lot of really small straight lines, then I improved this to make a fitted curve through a bunch of points on the parametric curve. 
<div class="clearfix">
    <img alt="DXF" src="/sebsite/images/parametricgrid.jpg" class="rightfloat">

To create these patterns I started by defining an equation with constants and then vary the constants to find interesting shapes. For example:

$$
(X,Y) \\
X=\sin(t)+\frac{\sin(at)}{2}+ \frac{\sin(bt)}{4} \\
Y=\cos(t)+\frac{\cos(at)}{2}+ \frac{\cos(bt)}{4}\\
$$

However manually varying the constants a and b is slow. So I simply added a few lines to my python DXF program to loop through 40 values of a and b between 0 and 20. This created thousands of curves at a time! Then, I just had to find my favorites.
</div>

I used these DXFs to laser cut parametric coasters.
<div class="gallery" > 
    <img alt="Coaster" src="/sebsite/images/coaster1.jpg" class="gallery__img">
    <img alt="Coaster" src="/sebsite/images/coaster2.jpg" class="gallery__img">
    <img alt="Coaster" src="/sebsite/images/coaster4.jpg" class="gallery__img">
    <img alt="Coaster" src="/sebsite/images/coaster5.jpg" class="gallery__img">
    <img alt="Coaster" src="/sebsite/images/coaster6.jpg" class="gallery__img">
    <img alt="Coaster" src="/sebsite/images/coaster7.jpg" class="gallery__img">
    <img alt="Coaster" src="/sebsite/images/coaster3.jpg" class="gallery__img">
    <img alt="Coaster" src="/sebsite/images/coaster8.jpg" class="gallery__img">
</div>