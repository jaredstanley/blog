---
title: Fish Feeder - Arduino
description: We were catching an early flight to go skiing last weekend – at midnight i remembered that Leo, H’s fish, was not accounted for while we were going to be gone.
month: 11
day: 25
year: 2012
---
We were catching an early flight to go skiing last weekend – at midnight i remembered that Leo, H’s fish, was not accounted for while we were going to be gone. In the past we’ve had neighbors watch his forefather(fish died) and then had friends, but that was awkward and I 1.didn’t want to have to ask anyone and 2.didn’t have time even if i wanted to.

I’ve been consulting at an agency recently. A guy who works with me has been doing cool projects and getting me excited about stuff so I immediately thought of Arduino + servo.



Retina mbp
I hadn’t messed with the Arduino since I got my new computer so was concerned there would be issues getting up and running. Indeed it wasn’t just plug/play as there were no usb options when I fired up the IDE. This was easily fixed however. I googled and found this url for FTDI USB drivers, installed and re-opened and it worked.

Timer
I knew i’d need some sort of timer and was unfamiliar w this on Arduino  As it was so late and timer functionality was so common I assumed I could just find some code online. I was correct.

Right on the Arduino site I found a time library appropriately called Time, and was pleasantly surprised to find along with it a TimeAlarm library. Even better.

These libraries require you to set a time when the Arduino boots up and then that essentially becomes the system time.


Loaded Straw + Servo over Leo’s Bowl

Setup & Testing
I got the servo running and hooked to the timer; the servo was moving slow and so I created a shake() function to help any straggling fish food pieces to eject.

I couldn’t find any AA batteries so i ran down to 7-11 and picked some up.

Tested the code on a 10-second time, and then hoped for the best with setting it up for Leo.

Setting up the hardware was the most difficult part – I just stacked some of H’s wood blocks near Leo’s bowl and then hot-glued the servo to the top block(i didn’t want the servo to fall in the bowl and fry Leo) and then rubber-banded a drinking straw (that I had cut down/singed one end) to the servo arm.

 


Arduino / Breadboard Setup next to Bowl

 


Arduino + Breadboard + Fish Bowl

 

The fish lived and the straw was empty, so I guess it worked.

In the future I’ll be using this again, but I’ll have to figure out a way to have multiple feedings.

Here’s the Arduino sketch
