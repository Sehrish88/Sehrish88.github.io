---
layout: post
title:      "Understanding Logic and Conditionals in Ruby"
date:       2020-01-07 13:39:27 -0500
permalink:  understanding_logic_and_conditionals_in_ruby
---

# 
Dealing with logic and conditionals in Ruby taught me that programming is all about common sense, and acumen. It is very similar to trying to learn  a new language such as Spanish or French in that you have to understand the meaning of certain terms, how to use them, and how they will be interpreted. You've got to figure out what exactly logical operators, also referred to as booleans, specifically mean. Certain conditions have to be met in order for certain logical operators to evaluate as "true". 

One of the ways I try to grasp these conditionals and increase my understanding of them is to translate them in to English. I try to come up with an English sentence for the boolean expressions.  For example when I come across the boolean  "&&", I know that the return value of that expression will evaluate to "true" if and only if both values are true. I can visualize this with a real life example and a sentence. Let's say I am a vegan individual and I would like some tomato soup. If I go to my favorite restaurant, I can only have tomato soup IF it is both vegan AND the restaurant still has some. 

Another concept that I had a little trouble grasping was that these logical operators (&&, ||, !) come in two versions. However, the difference between the two versions lies in "operator precedence". This means that in an expression, which operator is performed first in that expression is determined by operator precedence. I found this concept easy to grasp when I compared it  to order of operations in a math equation in which the multiplication and division operators bind stronger and precede the addition operator. In Ruby, the "&&", "| |" and "!" operators bind stronger than and precede their counterparts of "and", "or" and "not". 
