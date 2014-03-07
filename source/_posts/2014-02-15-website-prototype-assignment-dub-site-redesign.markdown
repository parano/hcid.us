---
layout: post
title: "Website Prototype: dub Site Redesign"
date: 2014-02-15 16:57:15 -0800
comments: true
categories: [HCID, Prototyping Studio]
---

##Background

Our weekly prototyping assignments started with low fidelity prototyping to higher fidelity ones. This week we are proposed to build an interactive wireframe for a website prototype. We are giving an existing website(our very own dub website), to analyze its current content and functionality and redesign the information architecture, navigation and general layout.


##Design
{% img right /images/prototyping/a5/dub-site.png 300 %}

After an extensive research and analysis on the current dub website (dub.washington.edu/), I got a basic understanding of all the functionality and content of this site. And synthesis with three user interviews about their experience of using this website, I have the following findings about users’ usual practice of using this site:

* Calendar is the most regularly used functionality for dub members, to track the newest events, specially the weekly dub seminar;
* For other audience who want to get to know about dub community, the people and their publications/projects are the most visited pages;
* The blog is less popular among visitors which may because of its lack of updates;

According to all these findings, I think there are several main problems in terms of information architecture:

<!-- more -->

* The most regularly used information(events, seminars) is located in secondary pages instead of homepage, and the upcoming event is not being highlighted.
* There are some huge list of names/titles of people/publication/project which makes it difficult to navigate through. A better index or search function is needed.
* The connections between dub people, and their publications and projects are not effectively presented. 


##Prototyping Process

To address these problems, I redesigned the information architecture of this site while remaining most of the functionalities of the original website. Here I will introduce my new design:

###Home Page

I use the masthead area to present the most important news and announcements. I envision this is a dynamic area with a wide image as background, so as to give new visitors a visualized impression of dub.

Following the masthead, is a selected partition of the most recent blog posts and news with some thumbnails and a detailed text paragraph of introduction with a link to view the whole article. Here I wish to present all the must-know news, announcements as well as the upcoming dub seminar, so that dub members could get to know about the weekly talk directly from the home page.

<div class="center">
{% img /images/prototyping/a5/index.png 380 %}{% img /images/prototyping/a5/drop-down-menu.png 380 %}
</div>

The DUB logo on the top left corner is the top level menu across the whole site in the format of a hover to drop-down menu. User can use this menu as a shortcut to quickly redirect to the target resource.

###People/Publications/Projects Page

The DUB people page lists all the dub members and provides a link to their own page. The current website has a huge list of names with only their department. It’s actually very annoying for new visitors to get to know about the people here. Take my experience for example, to find a professor interested in the field of data visualization, I have to press ‘command’ key and click on all the links, and then check them one by one. 

It will be much better if we can show some rudimentary information about the professor in the listing page. But the drawback of this approach is you need to scroll down the page a lot to find a specific one.

So in my design, I try to combine both approaches where I put the name list on the left as a quick reference. And put a list of short introductions with a portrait image on the right side. In order to navigate to a certain people faster, I made the reference list a folding menu list because it’s actually a very long list referring to the current website.

{% img center /images/prototyping/a5/people-list.png 500 %}

For the current dub site, I found these are a lot of links between the dub people, the projects and the publications. But by click on a link and jump to another page, users can’t really percept or memorize all the connections easily. They are connected but visually disconnected. 

Take into account this observation, I designed this vertical accordion page to show each person’s related publications and projects. There are three columns in this accordion page where the introduction page is unfolded by default. When the user click on the publications or the projects, the corresponding partition will unfold and the previously unfold column will be enfolded:

{% img center /images/prototyping/a5/accordion.gif 500 %}

{% img /images/prototyping/a5/people-name.png 266 %}{% img /images/prototyping/a5/people-publications.png 266 %}{% img /images/prototyping/a5/people-projects.png 267 %}

###Calendar Page

I personally don’t like using such calendar view to show recent events, but most dub members are already getting used to this approach and the current calendar page is actually the most visited page according to the survey. So I keep the same functionality in the new design, and put the entrance on the upper right corner of the navbar for faster accessing.

##Prototyping Tools

To create such an interactive wireframe prototype, I have several different tool to choose from: using HTML/CSS or using a specification prototyping software such as Axure, Balsamiq etc. As I’m already very familiar with developing websites, I choose to learn and use Axure this time so as to learn something new. 

Building the home page in Axure is pretty easy. I made it without reading any extra documentation or tutorial. Because most elements in the homepage are very basic, and the interaction with those elements are very simple. But when I started to build the people profile page, it becomes very tricky. I searched for several implementation of accordion menu in Axure, but they are neither too expensive, nor have no documentation or any clue for you to reuse it. To work around this problem, I build three different pages and use link to simulate the accordion page, but the transition is too slow.

{% img right /images/prototyping/a5/axure.png 400 %}

Another thing about axure is that comparing to using template in web development, it’s really hard to reuse partition of the page in other pages. I have to copy the navbar, the footer, and the navigation menu on every page. And each time I want to update a link in the menu, I have to change it on every page, which is very annoying.

After creating this prototype in Axure, I guess I will not use Axure again. My reason is that comparing using HTML/CSS/Javascript to using Axure, the only drawback is the learning curve is relatively higher. However, for someone who is already familiar with web developing, there is no need to learn Axure. Actually with the help of countless open source components and frameworks(Bootstrap, Blueprint) from the web development community, a developer can build the prototype very quickly. 

Another reason is that for only creating the wireframe, using Axure may be easier. Nevertheless, to learn to implement some advanced interaction in Axure, it may take even more time than the HTML/CSS/Javascript approach. 

Thanks to Axure, I can publish the prototype online: http://fik3lo.axshare.com/. Not all the links in this page can work due to time constraint. 

##Reflection

Here is some feedbacks I collected from other classmates:

* Drop down menu on the top left corner may need some improvement. There is plenty space on the top of the page for all the links, replace it using a navigation bar with link to ‘home’, ‘people’, ‘publications’, will be better. 

* No one knows how to use the Search on the top right corner. I think it’s better to add a tooltips for the search functionality.

* Didn’t consider the situation where the faculty or student don’t have any publications/projects. The page will definitely change a lot or have some blank. 

I also created a video to introduce my design via recording people using this prototype. Most of the interaction in the video in understandable to audiences, and they can get the idea of showing the connections between people and their publications/projects through a single page accordion menu. Nevertheless, my tester got confused when he was using the prototype alone. The page redirection transition makes it harder to perceive this idea.

Here is the video I made to present this website prototyp:

<div class="video-container">
<iframe src="//player.vimeo.com/video/86963982" width="500" height="281" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe> 
</div>




