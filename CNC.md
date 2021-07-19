---
layout: default
title: CNC
permalink: /cnc
---

# CNC milling
Learning to CNC mill was an excellent skill because it is able to make a wide variety of very strong parts. 
My [puzzle box](/sebsite/puzzlebox) and [my game](/sebsite/game) both use CNC. 

## Marble run
<div class="clearfix">
    <img alt="Marble run" src="/sebsite/images/marblerun.jpg" id="rightfloat">
    <p>This was my first CNC project, so I chose a simple shallow to mill in order to learn how. I learnt a lot about tool types, feeds and speeds, modeling in fusion 360, designing tool paths, G-code and CNC operation.</p> 
    <p>To make the actual shape I created a parametrically defined curve and used my <a href="/sebsite/parametric">python program</a> to turn it into a DXF curve. Then I used rhino to put a pipe around the curve and cut the solid shape created out of a cylindrical object.</p>
</div>

youtube cnc video
 
## Grand Teton
<div class="clearfix">
    <img alt="Grand Teton" src="/sebsite/images/teton.jpg" id="rightfloat">
    <p>The Grand Teton is a mountain in Wyoming that my dad climbed and I decided to make him a mini topographical map of it because I wanted to try topographical CNC. I downloaded a STL file of the mountain from an online <a href="https://jthatch.com/Terrain2STL/">terrain to STL converter</a>. I started with a big 8mm end mill for aggressive clearing and then did finer stepdowns with a smaller 6mm end mill and finishing parallel passes with a small 3mm ball mill. Afterwards I laser engraved "Grand Teton" into the wood and oiled it for protection.</p>
</div>

<iframe src="https://gmail1265769.autodesk360.com/shares/public/SH919a0QTf3c32634dcf815c514eef38cdc0?mode=embed" width="100%" height="500" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>


## Wave
<div class="clearfix">
    <img alt="Wave" src="/sebsite/images/wave.jpg" id="rightfloat">
    <p>This is water ripple frozen into wood. I used my <a href="/sebsite/python">python DXF program</a> to convert a wave equation to DXF file. I modelled my wave as a cosine wave with an exponential decay:
    \(y = ae^{-bx}\cos{cx}\)</p>
    <img alt="Wave graph" src="/sebsite/images/wavegraph.jpg" width="50%" width-max="600">
</div>

Then in rhino I revolved that curve to make the wave surface:

<img alt="Wave model" src="/sebsite/images/wavemodel.jpg" width-max="600">

I also made a surface defined by equation: $$z = xye^{-x^2+y^2}$$. To model this surface I wrote a python program to create a DXF file with a large grid of points at set x y positions and a z height determined by the surface equation. Then in rhino I was able to fit a surface through the point grid. 

<img alt="Surface model" src="/sebsite/images/surface.PNG" width-max="500">

Then I used both of these models to make a cam path in Fusion 360 to cut them out of a block of wood. You can view the cam path with the top left button shaped like a mill:

<iframe src="https://gmail1265769.autodesk360.com/shares/public/SH919a0QTf3c32634dcf1593a955fb1769b2?mode=embed" width="100%" height="500" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>


