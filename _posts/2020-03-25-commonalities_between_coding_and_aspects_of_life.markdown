---
layout: post
title:      "Commonalities Between Coding and Aspects of Life"
date:       2020-03-25 21:50:39 -0400
permalink:  commonalities_between_coding_and_aspects_of_life
---


Recently, we had to build a Sinatra application and many times in the controller routes code would have to be repeated. For example, for certain routes like /edit and the delete actions, I'd have to write code that would ensure that the user was logged in and had proper credentials to edit or delete a post. Also, I had to write the same line of code in my controller routes which dealth with showing a certain user's page, editing a post, and sending a patch request. My code was getting pretty cluttered and repetetive until I used the aid of helper methods. Helper methos are just methods you can define which include code that you will need to use again and again in your application. These methods can then be called in any controller and they help to clean up your code. 

Using the helper methods felt great, I got the same feeling I get when cleaning my room and getting rid of junk. It felt like I was decluttering. Another reason to use helper methods is because I have come to learn that as programmers we are lazy, and it is this laziness that compels us to write eloquent code that is not repepetitive and is also easy for us to access again and again. As with most things in life, simplicity and eloquence is key, and those are golden qualities when it comes to writing code. 





