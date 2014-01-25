---
layout: post
title: "Paper Prototype Assignment: Wearable UIs"
date: 2014-01-21 17:49:25 -0800
comments: true
categories: [HCID, Prototyping Studio] 
---

Design
------


{% img right /images/prototyping/a1/metronome.jpg 160 %} 
For this paper prototype assignment, I designed a metronome application that works on both mobile phone and smart watch. It helps to improve musical performance like a traditional metronome while wearable device enabled us to create an even better user experience.

In the picture is a mechanical wind-up metronome which can produce a steady beats: “Da Da Da Da ...”. The consistent tempo help internalizing a clear sense of timing and tempo while musician is playing. By adjusting the metronome, the device can produce varying tempi, usually ranging from 40 to 208 BPM(Beats Per Minutes).

Existing software metronomes and electronic metronomes usually produce the tempo by sound. The problem with using sound is that the sound may be interruptive for audience, and it’s hard to follow the sound on stage(noisy environment). 

One thing I found most excited about using Pebble is vibrating on wrist. It enabled a new dimension of sensing information from a digital device without actively paying attention to the device. My idea is by setting the smartwatch to vibrate in a certain tempo, to give musician a more strong sense of the beats. 

<!-- more -->

{% img left /images/prototyping/a1/sketch.JPG 320 %} 

I sketched my first design on whiteboard. It uses the mobile phone interface to set the tempo, while user can also adjust the tempo directly from the watch.

There are two ways to change the BPM value from the phone. One is by spinning the wheel in the middle of the screen, and the other one is by continuously tapping on the button to give an approximate speed. The first method is more accurate and the second one is more intuitive and more useful for composers.
The wheel is easy to understand, it’s like a metaphor of physical tuner. But I’m not sure about the “tapping” part. So I start to make a paper prototype and test this design.



Prototype
---------
I build the first version of this prototype within 10 minutes. It’s a quick and dirty one, with only the necessary components on one white paper. To operate this prototype, I need to change the BPM value by writing on a small sticky note and change it while the user using the prototype. 

I made a watch face and attach it to a Pebble watch so that the user can actually wear the watch and try the interactions in a more realistic setting. Once the user click start on the phone, the smart watch will launch this app which allow the user to adjust the tempo by the “up/down” button, and exit the app through the “Home” button.

{% img left /images/prototyping/a1/p1.1.jpg 320 %} 
{% img /images/prototyping/a1/p1.2.jpg 320 %} 

As some effects can’t be implemented with paper prototype, I will just tell them what happens on the interface or the devices. That includes slight changes on the BPM number, the vibrating of the watch, the sound tempo make by the phone, and the backlight feedback for clicking the tap button.

       
After several tests, I build a second version based on the feedbacks from the tests with the first paper prototype.

With the second paper prototype, I use cardboard to create a base in the shape of an iPhone so that the user can actually hold the phone on hand. I use a scrolling bar to change the BPM value so that the feedback from tapping and wheel could be faster in the testing. And the scrolling up and down actually simulate the animation I want for this interface. While the user is adjusting the wheel, I will scroll the bar up or down according to the user’s operation. In the first time the user touch the “Tap” button, a pop-up dialog will show up to tell the user how to use this button.

{% img left /images/prototyping/a1/p2.1.JPG 320 %} 
{% img /images/prototyping/a1/p2.2.jpg 320 %} 


Testing & Analysis
------------------
This is a minute clip presenting the usability testing for the 2 iterations of my paper prototype:

<div class="video-container">
<iframe src="//player.vimeo.com/video/84655291" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe> 
</div>

During the tests with the first prototype, I found that the text “Try tap your tempo” on the left side is extremely helpful for the user to understand how to use it. I tried to remove it and test it with another user, and it failed in the tapping part. The user can’t understand how to use the Tap button without this simple instruction. But I also noticed that this text instruction is unnecessary after the user figure out how to use it. So I change it to a dialog format.

On the other hand, spinning the wheel is more like a self explaining UI component, user can easily figure out how to use it. That may because it looks just like a rotary knob, and it’s natural for it to change the number above it. And this metaphor is widely used in many software interface for turning volume, adjusting parameters and also hardwares such as the classic iPod.

I found that changing the number instantly (or faster) will largely help the user to understand the UI, and replacing the sticky notes is too time-consuming in the test. That’s why I use a scrolling bar for changing the BPM value in the improved version, as it’s just an increasing array of numbers.

Another problem I found in the testing is that user barely use the interface on smartwatch to adjust the tempo. Most of the time they just use the mobile phone to adjust the tempo and to start/stop the beats, although most of them like the idea of vibrating on smartwatch. On a second thought, this app can totally work without the mobile phone: adjusting one number is easy enough to operate on a watch with a simple interface like the one I designed. Moreover if the smartwatch have a motion sensor and microphone, it’s possible to ask the user to set the tempo by snapping their finger which is even more fun to use.

Beside adjusting the tempo, the phone actually allow us to do more complicate operations. For example, the user can choose a song from the music library and let the watch vibrate in a rhythmic beats, or use the phone to connect and sync the tempo among multiple smart watches, which may be useful for a band to collaborate. 
