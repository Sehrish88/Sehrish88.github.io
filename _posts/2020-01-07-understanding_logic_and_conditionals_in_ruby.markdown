---
layout: post
title:      "Understanding Logic and Conditionals in Ruby "
date:       2020-01-07 13:39:27 -0500
permalink:  understanding_logic_and_conditionals_in_ruby
---

![](https://cdn.educba.com/academy/wp-content/uploads/2020/04/Ruby-if-else.jpg)

Dealing with logic and conditionals in Ruby taught me that programming is all about common sense, and acumen. It is very similar to trying to learn  a new language such as Spanish or French in that you have to understand the meaning of certain terms, how to use them, and how they will be interpreted. You've got to figure out what exactly logical operators, also referred to as booleans, specifically mean. Certain conditions have to be met in order for certain logical operators to evaluate as "`true`". 

 One of the ways I try to grasp these conditionals and increase my understanding of them is to translate them in to English. I try to come up with an English sentence for the `boolean` expressions.  For example when I come across the boolean  `&&,` I know that the return value of that expression will evaluate to `true` if and only if both values are true. I can visualize this with a real life example and a sentence. Let's say I am a vegan individual and I would like some tomato soup. If I go to my favorite restaurant, I can only have tomato soup IF it is both vegan AND the restaurant still has some. I had to utilize conditionals in my 10 Day Weather Forecast Application: 
 
 ` def menu_input
        user_input = gets.strip 
        #if user_input 
        #string must be between 1-16 
       if  user_input.to_i.between?(1,16)
        #user input must be converted to integer, we have to subtract 1 for the index number 
        then index = user_input.to_i - 1
        #We want to use user input to go in to forecast.all array to display forecast
        f = Forecast.all[index]
        f.display
       elsif user_input.to_i > 16
            puts "invalid entry"

       elsif user_input == "end"
        exit`

Another concept that I had a little trouble grasping was that these logical operators come in two versions. However, the difference between the two versions lies in "operator precedence". This means that in an expression, which operator is performed first in that expression is determined by operator precedence. I found this concept easy to grasp when I compared it  to order of operations in a math equation in which the multiplication and division operators bind stronger and precede the addition operator. In Ruby, the conditional operators `&&, ||, !` bind stronger than and precede their counterparts of `and, or and not`. 
