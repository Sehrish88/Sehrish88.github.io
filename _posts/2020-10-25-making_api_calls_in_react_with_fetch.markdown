---
layout: post
title:      "Making API Calls in React With Fetch "
date:       2020-10-25 13:10:27 -0400
permalink:  making_api_calls_in_react_with_fetch
---

 

Modern software today attempts to run processes that are asynchronous, meaning they let other tasks run while one task is completing. In JavaScript there are two types of asynchronous code, older style callback functions and the newer promises. This is where fetch() comes in as it is the newer style of async code which modern web APIs use and it returns a promise.  

The modern method of fetching data from a server is  to update particular sections of a webpage without having to load an entire new page. It used to be that when you requested information from a website, you’d have to wait for the response and load an entire page again which made for a poor user experience. 

One of the most popular websites today, which utilizes asynchronous programming and updates sections without reloading the entire page is Facebook. Facebook also developed React.js which is an in-demand JavaScript library. My final project at Flatiron School was to build a React.js application which would fetch data from an API using the fetch() function which is a JavaScript function that fetches data from APIs asynchronously. 

We can make HTTP requests from web browsers using the fetch() API. It requires a parameter of the URL from which you want to request the  information. It then returns a promise. You can use the then() or catch() methods to handle that promise. Once the request is complete, the resource is available and will be resolved into a Response object. The response object has numerous helpful methods and properties in order to inspect that response. In my project I used the json() method on the response object to extract the JSON content from my backend API. 

You can build an application with full CRUD functionality using fetch() and JavaScript. A fetch request by default is a GET request and if you want to perform a different type of method, you have to specify that. For example POST, DELETE, UPDATE. I kept my fetch requests to POST and GET methods. Because of the POST methods, I am able to create new users and new skills in my SKill Swap React project, and the GET method enables me to display a list of my users and skills from my backend API. 

