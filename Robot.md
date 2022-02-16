---
layout: default
title: Robot
permalink: /robot
---

# Robot

<div class="clearfix">
    <img alt="Robot" src="/sebsite/images/robot.jpg" class="rightfloat">
    <p>I made a little robot able to be controlled remotely from a laptop and autonomously try to navigate a maze for a university course. </p>
</div>

## Chassis
<div class="clearfix">
    <img alt="Robot" src="/sebsite/images/robotjoint.jpg" class="rightfloat">
    <p>The chassis for the robot was laser cut so that the electronics and the wheels were separable. 4 pins were set up so that when the electronics were placed on the base the pins connected.</p>
</div>

## Electronics
<div class="clearfix">
    <img alt="Robot" src="/sebsite/images/robotinside.jpg" class="rightfloat">
    <p>The robot uses an Arduino, bluetooth module, distance sensor, motor driver, two motors and a 9V battery. The thinking parts are all contained within the top of the box and connected by a big mess of wires. </p>
</div>

## Code
The robot was controlled from my laptop, using a serial monitor to send WASD commands to the bluetooth module. The commands were interpreted by the Arduino and then the motor driver was used to make the relevant wheel movements. The movements are recorded and can be played backwards to attempt to move the robot back to the start (it didn't really work because of friction). The distance sensor frequently measured the frontal distance and sent it back to the computer. 

## Autonomous navigation 
There was also a maze mode, where it would try to get through a maze by following the right wall. I could program right turns because the battery voltage varied over usage, so instead I made to robot bounce against the wall by constantly doing a wide right turning and then pivoting left every time a close wall is detected.

<video autoplay loop muted playsinline controls src="/sebsite/images/robotmoving.mp4" class="gallery__img"></video>