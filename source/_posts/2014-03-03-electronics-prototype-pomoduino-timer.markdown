---
layout: post
title: "Electronics Prototype: Pomoduino Timer"
date: 2014-03-03 14:10:25 -0800
comments: true
categories: [HCID, Prototyping Studio]
---


##Background

{% img right /images/prototyping/a7/clock.jpg 230%}

Building interactive physical systems is a great joy to me. It’s always fun to design the circuits, solder different parts and make things work. This week, our prototyping studio class gives me a chance to build an electronics prototype with Arduino.  

As there is only one week for me to do this assignment, I decide to make something useful to me and also small enough so that I can handle it in one week. Looking at my dumped alarm clock, I decide to build a Pomodoro Timer out of it.

[Pomodoro Technique](http://en.wikipedia.org/wiki/Pomodoro_Technique) is a popular time management method. Based on the idea that frequent breaks can improves mental agility, this method breaks down the work into intervals, 25 minutes in length, and separated by short breaks. 

To apply Pomodoro Technique in real life, people invented the Pomodoro Timer which is similar to a kitchen timer, but can only time 25 minutes every time. The physical act of winding up the timer confirms the user’s determination to start a task, the ticking to externalises desire to complete the task, and the ringing announces a break.

For this prototyping exercise, I made a pomodoro timer mainly with an Arduino UNO board, a LCD screen, and a motor.  The LCD screen is used to visualize the ticking and how much time left in the running pomodori. The button is the only way to interact with the system which can toggle the status between running and reseted.

<!-- more -->

Here is a demo video of the pomodoro timer I made, which I call it *pomoduino*:
<div class="video-container">
<iframe src="//player.vimeo.com/video/88049469" width="500" height="281" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe> 
</div>

<hr>

##Playing With Electronics And Arduino

####Motor Module

{% img /images/prototyping/a7/motor1.jpg 400 %}{% img /images/prototyping/a7/motor2.jpg 400 %}

The motor module is used to power the bell in the alarm clock. I firstly prepare and test the circuits with an extra motor and migrate it to the motor inside the clock in the end.

The transistor acts like a switch to control the motor; it make use of the signal from Arduino to power another circuit which much higher current. The diode and capacitor in this circuit are meant to protect the circuit from noise and spikes.

####LCD Screen Module

{% img /images/prototyping/a7/screen1.jpg 400 %}{% img /images/prototyping/a7/screen2.jpg 400 %}

The 16 pins LCD screen is widely used with single-chip microcomputers. With arduino, the library and driver for controlling this LCD is actually pre-installed in the Arduino IDE. The challenge here is to neatly layout all these wires and present a clear interface to the user. I bundled all the wires to go through the hole in the center of the clockface, and stick the small breadboard on the surface. 

####Button Module

{% img right /images/prototyping/a7/button.jpg 300 %}

The button here actually works like a switch that can change the state of the system. The system have to keep track on the current and previous value of the button, and only change the state of the system when its value change from LOW to HIGH. That means the state of the system will only be changed when the user push down the button. A tutorial on this could be found [here](http://www.arduino.cc/en/Tutorial/Switch#.UxegtPRdXHA).

####Putting Everything Together

After testing each part, I start to assemble different parts of the hardware together. This is the overall layout of the circuits:

{% img /images/prototyping/a7/circuits.jpg %}


I apply a 9 volts battery to power both the arduino and the motor. The input-output interface(button, LCD screen and a breadboard) is separate from the others, and is positioned in the front of the ‘clock’. Another breadboard is attached to the arduino board, together in the back of the ‘clock’, and used to arrange the motor circuits. I removed the original wires that connected to the motor inside the clock, and soldered another two that is easier to connect to the breadboard.

{% img /images/prototyping/a7/alltogether.jpg 400 %}{% img /images/prototyping/a7/back.jpg 400 %}


##Reflections

####Constraints Of Prototyping

During prototyping electronics, the components we have are usually not ideally to our design. In this project for example, I want to present ‘push button to start’ on the LCD screen. But the LCD is not long enough to contain this sentence so that I change it to a less appropriate one: ‘click to start’.

I recognized that there are always lot of constraints in prototyping electronics, because we can’t get all the hardware parts customized to our need. But most of them it doesn’t matter to the prototype itself, as long as we can continue the following usability testing upon the prototype. Some walkaround could help to build the initial prototype.

####Software Engineering Principles

Building and debugging hardware seems very challenge to me in the beginning. Until I find that I can actually apply my knowledge in developing software to building electronics. The principle of Modular Programming, Encapsulation and API design are also quite useful in building hardware. For example, if I haven’t divided the circuits into separate modules in the beginning, it would take much more effort to deal with all those wires, and also much harder to debug potential issues in hardware or software.

####Be Safe & Follow Best Practice

Playing with electronics is not safe especially when high current circuits are involved in your project. Even with only 9 or 5 volts battery, it’s really easy to break some components in the circuits. We can’t expect every prototyper to be an expert in digital design and create appropriate protect circuits. But as a prototyper, it is important to follow the best practice from all those tutorials and examples, so as to avoid those dangers.

####Fast Prototyping with Arduino

Building prototypes with Arduino is so fast. There is a huge and active online community that contributes to millions of libraries and tutorials. You can easily get start with any type of sensor or components, by just following the tutorials, and use related libraries. The processing language also allow the user to integrate their application with other programming language or applications. I think this is the reason that Arduino is a good choice for prototyping electronics. The less effort you spend on technical problems, the more time you could focus on solving the real problem.

{% img /images/prototyping/a7/books.jpg center %}



