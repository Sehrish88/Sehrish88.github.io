---
layout: post
title:      "The deal with Classes and Instances"
date:       2020-03-02 20:18:26 +0000
permalink:  the_deal_with_classes_and_instances
---

One thing that I have learned while studying Ruby and coding in it is that all things are objects in Ruby. It is an object oriented programming language. Since everything is an bject in Ruby, every object has a class, and being a part of a class, the methods of a class give that object a lot of attributes and functionality. You can call the "#methods" method on any Class/object to return a list of all the methods available to that particular class. 

Furthermore, certain methods are instance methods and can only be called on an instance of that class. For example, for my sinatra application, Joint Reviews, I created two classes; a User class, and a ReviewPost class. Both classes had certain attributes and certain methods that could be performed on them. In order for methods such as "#name" or "#id" to be used on User objects, I would have to create instances of the class. I cannot call the "#name" method on the class itself, it can only be called on an instance of the user class. Building my sinatra application really cleared up for me how classes work with methods and instances of classes work with instance methods. 
