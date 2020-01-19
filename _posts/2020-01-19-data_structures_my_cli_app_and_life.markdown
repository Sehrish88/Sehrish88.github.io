---
layout: post
title:      "Data Structures, My CLI App, and Life"
date:       2020-01-19 14:19:07 -0500
permalink:  data_structures_my_cli_app_and_life
---


In this blog I will share my reflections and lessons from the recent CLI application projecf thaf i completed, which involved tne creation of a weather app. in particular, I'd like to highlight the significance of data and data structures. 

# Array of Light

After immersing myself in coding, and more specifically the Ruby language, I quickly learned about its data structures like arrays and hashes. Different data structures are useful for different tasks. Arrays are one of the first types of data structure which we learn about and they can be used to store contiguous data, which is data that comes one after the other without any breaks. Arrays are usually returned when we gather results from running a loop. Arrays also have many of their own methods and we can iterate through arrays to give us specific data that we want. This is exactly what I did in my CLI ten_day_weather_forecast app; I iterated through a big array of weather forecast attributes to pick and extract the specific weather attributes that I wanted to display to the user in my app. 


# Value of Hashes
Data structures like hashes use key and value pairs to store data. Every key has a value, and the value can be a string, integer, or symbol. In my CLI application I used a weather forecast API which returned a huge hash of weather properties. Every weather property like high-temp, low-temp, snow, precipitation etc had a specific value which was based on the city and state entered by the user. The weather hash also included arrays of different weather properties, and I had to iterate through the hash to extract the patient properties that I wanted. 

# Data is Life
Data structures can be seen as a metaphor for life because life is all about data and information, and us trying to classify or extract that data and information. Data structures would be useful in any field which humans have ventured in such as the health field in which patients can be mapped to physicians, or contact information where names can be mapped to phone numbers, or even dictionaries where words can be mapped to definitions. Data structures can prove useful to any field that uses data and as we know, data is everywhere. 


# Data and my CLI App
In constructing my CLI application, I had to first create objects which would deal with data and have relationships and talk to one and other. I also had to write methods that would enable my created objects to communicate and work collaboratively. I had to implement all the lessons I had learned about object oriented programming. Ruby sees everything as an object and even classes themselves are seen as objects by ruby and are instances of the "class" class. The three main classes that my application had were the APIAdapter class, the CLI class, and the Forecast class. 

The API Adapter class' duty was to get the data from the API using the API Key which was saved as a variable, and parse through the JSON document and then return a forecast hash with the initialization of every forecast object that was created using the Forecast class. The Forecast class defined all the attributes that would be extracted from the JSON document, and also had a method which displayed the proper attributes with the proper labels such as "date:, "city" and "state" etc. This display method would be utilized in the CLI class which sets up the user display, and prompts the user for the input which would then be used to display the proper forecast based on the user's city and state. 

Doing this project showed me first hand how classes have relationships and how they utilize methods to communicate with each other, and how their interactions can build a functional and useful application. 
