---
layout: default
title: CNC
permalink: /cnc
---

# CNC machining
<div class="clearfix">
    <video autoplay muted loop playsinline controls src="/sebsite/images/redback/laser cutting.mp4" class="rightfloat"></video> 
    <p class="leftfloat">I learnt CNC machining in 2020 and it has become one of my most valuable skills! CNC machining is a computer controlled process where a cutting tool moves through solid material to cut out the programed part. I started machining wood on routers, and have progressed up to machining tool steels on a 5-axis mill and turning bearing shafts on a CNC lathe. I have machined parts for many personal projects, <a href="/sebsite/redback">Redback Racing</a>, my thesis, and <a href="/sebsite/Machinistchess">chess board</a>. </p>
    <p class="leftfloat">I work at UNSW designing and making parts for UNSW researchers, which has greatly expanded my skills! Researchers always seem to want massive or tiny parts and they often have unusual material requirements. The largest part was bigger than the working volume of the machine and required rotating halfway and the <a href="/sebsite/letterpunches">most detailed parts</a> required 0.2mm endmills, which is the size of 2-3 human hairs. I have machined materials including rubber, tool steel, teflon, and foam.</p>
</div>

<div class="clearfix">
    <img src="/sebsite/images/CNC/CNC badge.png" class="leftfloat" style="max-height: 250px;">
    <p class="rightfloat">I also enjoy teaching CNC machining to students at the Kirby Makerspace where I run machine inductions for our Tormach, Symbiosis and HAAS 3 and 5 axis machines. I wrote the <a href="https://www.making.unsw.edu.au/learn/haas-5-axis-32-induction/" target="_blank">CNC inductions</a> for several machines: students have to program a part designed to teach them about different toolpath strategies. I also got to write the advanced learning material for students which covers <a href="https://www.making.unsw.edu.au/learn/advanced-cnc-milling-feeds-and-speeds-and-more/" target="_blank">feed and speeds</a>, <a href="https://www.making.unsw.edu.au/learn/advanced-cnc-milling-probing/" target="_blank">probing</a>, <a href="https://www.making.unsw.edu.au/learn/advanced-cnc-milling-tooling/" target="_blank">tooling</a> and other <a href="https://www.making.unsw.edu.au/learn/advanced-cnc-milling-machinist-essentials/" target="_blank">essential knowledge</a> in depth.</p> 
</div>

# MECH4100 bearing press fits
<div class="clearfix">
    <video autoplay muted loop playsinline controls src="/sebsite/images/CNC/acrylic reaming.mp4" class="rightfloat"></video> 
    <p class="leftfloat">During a final year course at UNSW students design and make stirling engines where they make most of the simple parts, and I helped make the harder parts for them. They make acrylic bearing mounts, which get laser cut then I enlarged the bearing holes for a precise press fit. I also drilled and threaded side holes so that set screws could be used to fix some components in place.</p>
</div>

# Gallery
<div class="gallery" >
    <figure class="gallery__item">
        <img src="/sebsite/images/CNC/cryogenic brackets.jpg" class="gallery__img">
        <figcaption>Machinist Chess set</figcaption>
    </figure>
    <figure class="gallery__item">
        <iframe src="https://gmail1265769.autodesk360.com/shares/public/SH919a0QTf3c32634dcf815c514eef38cdc0?mode=embed" class="viewer3d" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>
        <figcaption>Grand Teton CAD</figcaption>
    </figure>
    <figure class="gallery__item">
        <img src="/sebsite/images/teton.jpg" class="gallery__img">
        <figcaption>Grand Teton</figcaption>
    </figure>
    <figure class="gallery__item">
        <video autoplay muted loop playsinline controls src="/sebsite/images/CNC/julio plate.mp4" class="rightfloat"></video> 
        <figcaption></figcaption>
    </figure>
    <figure class="gallery__item">
        <img src="/sebsite/images/CNC/Blank.jpg" class="gallery__img">
        <figcaption></figcaption>
    </figure>
    <figure class="gallery__item">
        <img src="/sebsite/images/CNC/Blank.jpg" class="gallery__img">
        <figcaption></figcaption>
    </figure>

    

# Grand Teton
<div class="clearfix">
    <img alt="Grand Teton" src="/sebsite/images/teton.jpg" class="rightfloat">
    <p>The Grand Teton is a mountain in Wyoming that my dad climbed and I decided to make him a mini topographical map of it because I wanted to try topographical CNC. I downloaded a STL file of the mountain from an online <a href="https://jthatch.com/Terrain2STL/" target="_blank">terrain STL generator</a>. I started with a big 8mm end mill for aggressive clearing and then did finer stepdowns with a smaller 6mm end mill and finishing parallel passes with a small 3mm ball mill. Afterwards I laser engraved "Grand Teton" into the wood and oiled it for protection.</p>
</div>

<iframe src="https://gmail1265769.autodesk360.com/shares/public/SH919a0QTf3c32634dcf815c514eef38cdc0?mode=embed" class="viewer3d" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>


# Marble run
<div class="clearfix">
    <img alt="Marble run" src="/sebsite/images/marblerun.jpg" class="rightfloat">
    <p>This was my first CNC project, so I chose a simple shallow to mill in order to learn how. </p> 
    <p>To make the actual shape I created a parametrically defined curve and used my <a href="/sebsite/parametric">python program</a> to turn it into a DXF curve. Then I used rhino to put a pipe around the curve and cut the solid shape created out of a cylindrical object.</p>
    <iframe src="https://www.youtube.com/embed/H_PB5cSu4eQ" class="youtube" frameborder="0" allowfullscreen></iframe>
</div>

# Wave
<div class="clearfix">
    <img alt="Wave" src="/sebsite/images/wave.jpg" class="rightfloat">
    <p>This is water ripple frozen into wood. I used my <a href="/sebsite/python">python DXF program</a> to convert a wave equation to DXF file. I modelled my wave as a cosine wave with an exponential decay:
    \(y = ae^{-bx}\cos{cx}\)</p>
    <img alt="Wave graph" src="/sebsite/images/wavegraph.jpg" width="50%" width-max="600">
    <p>Then in Rhino I revolved that curve to make the wave surface.</p>
</div>

<div class="clearfix">
    <img alt="Surface model" src="/sebsite/images/surface.jpg" class="rightfloat">
    <p>I also made a surface defined by equation: $$z = xye^{-(x^2+y^2)}$$ To model this surface I wrote a python program to create a DXF file with a large grid of points at set x y positions and a z height determined by the surface equation. Then in rhino I was able to fit a surface through the point grid. </p>
</div>

I used both of these models to make a cam path in Fusion 360 to cut them out of the wood. You can view the cam path with the top left button shaped like a mill:

<iframe src="https://gmail1265769.autodesk360.com/shares/public/SH919a0QTf3c32634dcf1593a955fb1769b2?mode=embed" class="viewer3d" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>


