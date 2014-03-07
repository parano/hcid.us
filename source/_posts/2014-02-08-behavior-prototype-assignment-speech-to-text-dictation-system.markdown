---
layout: post
title: "Behavior Prototype: Speech-to-Text Dictation System"
date: 2014-02-08 13:23:00 -0800
comments: true
categories: [HCID, Prototyping Studio]
---

>This article and its related work is developed by Hadiza Ismaila, Chaoyu Yang, and Chase Chen-Hung Wu.

In order to learn about user’s behavior of intuitive verbal commands on speech-to-text system, we designed and implemented a rapid behavioral prototype for user testing. Built by Google Drive with a person playing the speech-to-text system (a.k.a. Wizard of Oz), our rapid prototype was tested and modified for several rounds with approaches such as simple text input, editing, error handling, and cursor moving. We summarized and organized the result into different categories of interactive patterns, and came up with valuable learnings and insights from our result analysis. 

<div class="video-container">
<iframe width="640" height="360" src="//www.youtube.com/embed/p3B-Bi3ZO8g" frameborder="0" allowfullscreen></iframe>
</div>

<!-- more -->

##Background
{% img right /images/prototyping/a4/draft.png 250 %}

Our task for this assignment is to create a behavioral prototype to explore the user interaction scenario of three choices: Speech to text dictation, Home alarm system, or Gesture recognition platform. After extensive research on all three topics, our group decided to work on speech-to-text dictation system, considering it as an inspiring and challenging topic.

The scenario for our testing is the user using speech to text dictation application that makes use of voice recognition to create and edit simple documents. This includes using spoken language to input text and using verbal command for simple text editing tasks.

We were particularly interested in exploring the following two questions through the user testing:

* Expectation of verbal commands for text editing tasks
* Tolerance for errors during dictation. 

We expected to use low-cost, low-tech materials to build the prototype, in order to speed up our explore our testing and modification process, and also achieve the goal of answering user experience questions. The prototype should allow us to modify rapidly, which gives us the flexibility to control and compare the variable we want to observe. Last but not least, we would like to create a realistic interactive experience of our prototype, just like any user using a real dictation application during testing.


##Prototype

While planning out our prototype, we came up with three approaches of building it:

####Google Drive
{% img left /images/prototyping/a4/prototype.png 300 %}

The first approach is using Google Drive (Google Doc) to type down the speech manually. The user will be asked to giving verbal commands to a laptop that shows a window of Google Doc, while a VoIP application running in the background that connects our wizard. Our wizard would be one of our teammate, acting as a part of our prototype: sitting somewhere else, using VoIP to hear the user’s voice, and typing down anything he heard on the document, which will also show up on the user’s screen. 

Our concern of this prototype is that our typing speed is much slower than an actual dictation program. Plus the tooltips on the typing cursor showing the typist’s name, a user can easily tell it’s someone typing in the background. 

####Simple Web Program

The second approach is to build a simple web program, which allows you to prepare a paragraph of text, and pop up word by word in the testing. The tester will see the web program in an extended monitor with another operator in the other side, listening to Skype voice call, inserting words by clicking and modifying text manually.

The problem with this prototype is that we need to ask the user to input a specific paragraph of text. And when we are modifying the text, the user can see the mouse and cursor moving, which makes it seem less realistic.

####Google Slides

The third idea is using Google Slides to pop up the pre-defined paragraph word by word while the user speaking. It’s very similar to the second approach while it also allow us to do more complicated modification during the testing. However, the drawback is that it’s hard to modify anything in the middle of the testing because you can’t just create new slides in front of the user, and if you change one of the slides, it will be discontinuoud to the next ones.

####Decision: Google Drive, & Setup
{% img right /images/prototyping/a4/decision.jpg 300 %}

After trying out different approaches and comparing their performance, we decided to choose the Google Drive one, since it provides more flexibility for us than other designs to modify prototype in short time, which helps up explore the users’ expectation of verbal editing commands in both greater width and depth.

Part of our prototype was connectivity, and we applied FaceTime to do so. We made FaceTime run in the background to transfer user’s sound to our wizard, while our wizard typing down words manually on Google Doc from another laptop. We were hoping this would make the prototype look like a real system or provide environment similar to a real system.

We were attempting to convince our users that they are testing some part of a real dictating application. Below shows how we created the context:

* Our wizard and users were staying in different rooms, and the tester would not be (or be less) aware of typing sound by wizard.
* Since we were using Google Drive as a main role of our prototype, we told our user that our system is an extension of Google Drive. We readjusted the display of Google Drive, and put on an annotation, “Google Drive Dictation System / Trial”, to make user ignore the low fidelity parts of prototype.
* We typed down anything that the user said during the test, pretending to be a not-smart-enough system.
* During the test, we arranged and applied several possible mistakes made by system, in order to observe user’s error handling.

##Testing 1
{% img left /images/prototyping/a4/testing1.png 300 %}

Initially, we conducted an exploratory user test on two participants. We expected to explore users’ reaction to general functions and events of a speech-to-text system: structure of users’ verbal commands, error handling behavior during dictation, and complexity of their commands (system’s perspective). Therefore our prototype had no pre-defined set of verbal commands, which gave the users flexibility to use any verbal command of their choice.

We provided them with a short passage to dictate to the speech-to-text system. Users were also asked to perform the following tasks and to ensure that each sentence was correctly generated by the system.

####Passage

The giant panda is perhaps the most powerful symbol in the world when it comes to species conservation. This peaceful, bamboo-eating member of the bear family faces a number of threats. It’s forest habitat is fragmented and populations are small and isolated from each other.

####Task

All operations should be verbal commands. No other available input methods.
* Input the first sentence
* Input the second sentence
* Input the third sentence 
* Replace the second sentence with Existing pandas are facing lots of threats.

The wizard typed down the sentences while users spoke. He/she would generate predefined mistakes in the sentences, which enabled users to provide verbal commands to correct the mistakes.

##Evaluation 1

####Dictation/Error Recognition
{% img right /images/prototyping/a4/evaluation1.png 300 %}

Since the users read from a passage on a paper, they dictated at a quite fast pace and paid more attention to the text they were reading than the text being displayed on the screen. They only noticed a mistake made by the system after they were done reading a particular sentence. They reviewed the generated text in order to find mistakes and give commands to the system to correct them.

####Complexity of Verbal Commands

One interesting finding was that the use of natural language in verbal commands. Some of their commands for editing was far from trying to match operations that are normally provided by keyboard or mouse. Instead of regularized/robotic commands, they operated in phrases and complete sentences rather one word. 

Following are the examples of verbal commands they used in correcting errors made by the system:

* Change consolation to conservation.
* No, the bamboo is not pregnant. it is fragmented.
* Instead of stress put threats.
* Replace stress with threat.
* Correct et to eating.
* Add a comma after peaceful.
* Replace pregnant with fragmented.
* Delete the second sentence.

####Same Function, Different Commands

Also, users used different commands for correcting same mistakes in a particular scenario. They expected the system to understand or accommodate multiple commands for the same function instead of using one specific command. 

####Improvement in Next Iteration

At this round we found users frequently questioning about the authenticity of the system, since the system only responded to the speech we assigned them. We couldn't evaluate user tolerance for error handling because the errors were few and the wizard responded to any command the user gave. Additionally, since the users were restricted to a set of instructions, the commands were only limited to changing a particular word or sentence.  The test was not sufficient enough to get meaningful answers to our questions. As a result, we refined our prototype and conducted further testing.

##Testing 2

{% img left /images/prototyping/a4/testing2.png 300 %}

We found two other users for our second round of testing. We provided them with the same passage and made a few changes to the task.

####Task

* Input the first sentence
* Input the second sentence
* Input any sentence of your choice

This time, the wizard responded to not only the input text dictated but every word the user said to make it seem more believable. Also, the wizard deliberately doesn't respond to some error correction commands made by the user to test what other ways the user might give commands for correcting the same mistake. We wanted to explore more commands a user would use and see if there were predictable patterns of commonly used commands.

##Evaluation 2

With adding a random scenario and typing everything uttered, users were convinced that this was an authentic system. 

####Dictation/ Error Recognition

In this round of testing, we noticed that users paid more attention to the screen when dictating a random sentence to the computer and could easily identify errors made by the computer and make just-in-time corrections. Also, they dictated in a slower pace than they did when reading from a text.

####Similar commands

{% img right /images/prototyping/a4/evaluation2.png 300 %}

We also noticed similarity of words and phrases used as voice commands for editing and correcting an error across all users.
Commonly used phrases include:

* Change incorrect word to correct word
* Replace incorrect word to correct word
* Delete incorrect word and replace with correct word
* Correct incorrect word with correct word

####Error Handling / Correction

When correction was done in real time, the user simply repeats the word until the system gets it right. If after multiple tries, the system doesn’t understand or respond to their command, they spell out the word to the system. 

####Improvement in Next Iteration

Although making changes made our system more authentic and enabled us to get more insights on similar commands, The results were not very different from the previous test and the commands were also still limited to the change and delete functions. We realized that giving the user predefined text to read from wasn't so effective and decided to perform another test without any predefined text or task.

##Testing 3

{% img right /images/prototyping/a4/testing3.png 300 %}


For the final round of testing, we simply asked our user to speak any sentences that came to mind gave them the freedom to do any editing task. Here, the wizard kept generating many random and repetitive errors in order to have a better understanding of how tolerant a user can be of errors generated by the system.

##Evaluation 3
By putting the user in a more flexible scenario, we got more insights on verbal commands for other functions such as moving cursors, copy and paste and navigating to a particular line.

####Moving cursors
User came up with the following commands to navigate the cursor to a desired location for editing. 

* go up - To move cursor up 
* go down - To move cursor down
* go back - To move cursor left
* go to 4th line, delete this line

####Cut and Paste

Surprisingly, the user used the cut and paste function to move a particular sentence to the end of the document. At first the user gave a complex command: 

> “Cut this line and paste it in the end of the document.”

But when the user realized that the system was unresponsive to her command she split the sentence in two separate command and said each command one after the other.

####Error Handling

Because the system kept generating random and repetitive errors,  the user kept repeating commands for a while before the system responded to the command which frustrated them.

##Conclusion

From the testing, we can deduce that the set up of our prototype the use of google doc and facetime made it effective. Learning from each test and iterating and refining our design helped us to gain valuable knowledge about users expectations of verbal commands and their tolerance for errors in a simple dictation/editing task.

####Overall User Expectation of Verbal commands

Users expected to use phrases and sentences in their natural language as verbal commands for editing, and they also expected the flexibility of saying a command in multiple ways so they don’t have to learn the command. Words such as “change”, “replace”, “correct” and “delete” were commonly used across all users when changing or correcting a word.

####Overall Tolerance for Error Handling

Our testing showed that users were quite tolerant of occasional mistakes as they did not expect the system to perfectly get everything right. They only became frustrated when the system repeatedly failed to understand a particular utterance or their commands. 

##Takeaway

The fidelity of behavioral prototype does not necessarily influence the quality of testing. User can be way more engaged into the testing scenario than we expect, if with right instructions. The point is to approach the same goal of learning with minimal effort of building prototyping, which is especially perfect for rapid modification based on result and feedback of each testing.

Although the fidelity does not necessarily matter, a thorough plan is required for the entire process. We planned out the structure and general workflow for our prototyping and testing in advance, in order to make sure our process supported by strong base of theories and analysis. In this way, every possible modification during the iteration of prototyping and testing would all follow the major direction of our plan, which makes work faster, more precise, and easier to facilitate.





