---
layout: post
title: "Mobile Prototype: Tweak The Tweet"
date: 2014-02-28 11:30:05 -0800
comments: true
categories: [HCID, Prototyping Studio]
---

##Background

{% img right /images/prototyping/a6/designspecification.jpg 230%}

This week, our HCID 520 prototyping class is ready to extend our prototyping skills to building mobile applications. Our task is to build a working prototype of the TtT([Tweak The Tweet](http://faculty.washington.edu/kstarbi/tweak-the-tweet.html)) mobile app, to support future usability study. 

TtT is an application that is part of HCDE Professor [Kate Starbird](http://faculty.washington.edu/kstarbi/)’s work in crisis research. She studies the “use of social media during crisis events, specifically looking at how the converging audience (aka, the ‘crowd’) can contribute—and is already contributing—to crisis response efforts.“

TtT uses Twitter to gather and direct information during crises to people who can act on it to the benefit of affected people and communities. And TtT aims to allow digital volunteers to provide information in a form that is more easily and reliably processed and analyzed.

We are given the design specification of this application that written by Grace Jang. It includes all the user interfaces, interactions and functional requirements of this app. And the prototype is suppose to be consistent with the specification. 

<!-- more -->

Here is a short video demo about this mobile prototype I developed:

<div class="video-container">
<iframe src="//player.vimeo.com/video/87334846" width="500" height="281" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe> 
</div>

##Prototyping

{% img left /images/prototyping/a6/phonegap.jpg 270%}

There are lots of tools for prototyping high fidelity mobile applications. Considering the scale of this application, non-programming approaches, such as App Inventor or Axure, might be very hard to manage and even harder to adapt to change in future works. So I choose PhoneGap(also known as Apache Cordova) and web technology to build this prototype since I am already very familiar with web programming. 

PhoneGap is a mobile development framework that allows software engineers to build application for mobile devices using web technologies(JavaScript, HTML5, CSS3). It use a middle layer that contains a webview inside a native app to render the UIs, and integrate many system service and apis into corresponding JavaScript functions. 

Taking advantage of using web, I can create highly customized user interface using HTML and CSS. And thanks to jQuery Mobile and Bootstrap, creating the UIs defined in the specification is not hard at all. Here is some screenshot of the UIs I made using web:

{% img /images/prototyping/a6/1.jpg 266%}{% img /images/prototyping/a6/2.jpg 266%}{% img /images/prototyping/a6/3.jpg 266%}

{% img /images/prototyping/a6/4.jpg 266%}{% img /images/prototyping/a6/5.jpg 266%}{% img /images/prototyping/a6/6.jpg 266%}

{% img /images/prototyping/a6/7.jpg 266%}{% img /images/prototyping/a6/8.jpg 266%}{% img /images/prototyping/a6/9.jpg 266%}


I started with build a mobile web application: using a local HTTP server to host the application and do testing in the browser. PhoneGap also provides a toolkit for developers to create all the files you need to pack up the web app into a native app installer. This allow me to use XCode to load the project folder generated from PhoneGap, and install this application on an iOS emulator. 

{% img /images/prototyping/a6/vim.jpg 400%}{% img /images/prototyping/a6/xcode.jpg 400%}


##Reflection

{% img right /images/prototyping/a6/login.jpg 230%}


One thing confused me a lot in the beginning is the authentication page in the design specification. It defined a customized login page for twitter and suppose that page can be implemented. But in fact, this kind of customized login page only exist before Twitter canceled their support for ```HTTP Basic Auth``` due to security reason. Nowadays twitter only support ```OAuth``` for authentication, which means the mobile app will redirect to a web page provided by twitter and not allowed to store the users’ password.

It’s possible that the author of this design specification didn’t discuss its design with a developer in detail. So that he or she can not really recognize all the constraints in designing this application. Moreover, since this app only need twitter authentication to post a tweet, it’s more appropriate to use [Twitter Sheet](https://dev.twitter.com/docs/ios/using-tweet-sheet) or for PhoneGap, the [Web Intents](https://dev.twitter.com/docs/intents). Because in that case, the application itself don’t need to worry about the authentication.

In general, I think prototyping TtT app using the web is a good choice. Comparing to developing native application, developing a mobile web application is arguably cheaper and faster, which is exactly what we expect from a prototyping tool. Although there are some constraints of building mobile app using web, including offline functioning, system level features, and UI responding speed, but the TtT app doesn’t require any offline feature or system level apis. Also for prototyping, the speed of webview is totally acceptable.
