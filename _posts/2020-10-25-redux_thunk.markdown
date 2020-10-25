---
layout: post
title:      "Redux Thunk"
date:       2020-10-25 19:03:06 +0000
permalink:  redux_thunk
---


One of the requirements for the final React-Redux portfolio project at Flatiron School was to use redux middleware to respond to and modify state change. State is an object available to React components and is where property values are stored. Redux is an open source JavaScript library for managing an application’s state. Although Redux is commonly used with React, it can also be used with any other view library. View libraries basically render your app in the browser. Redux is used for application state management by maintaining your state in an immutable state object which cannot be changed directly and has to be re-rendered in a new object when changes are made. 

Redux makes it easy to debug your application. This is done by logging actions and state so you can understand the errors via the redux dev tools which let you inspect state changes.  It also solves the problem of one way data flow. In React, we know that data is passed as props down a component tree from parent to child components. For data to be passed back up the tree we need callback functions to be passed down to any component which needs to pass the data upwards. This means that components which don’t need that data must accept props which they don’t need and it just makes accessing data and the data flow harder than it needs to be. 

This is where Redux comes in by giving us the connect() function which gives any component access to the redux store which is where the state is housed. Components can then pull any data that they need directly from the store. However with a redux store you can only do simple synchronous updates by dispatching an action. 

If you want to write asynchronous logic to interact with the store, you need middleware. Thunk is one such Redux middleware which extends the store’s abilities. It allows you to write action creators that return a function and not an action. You can use thunk to perform asynchronous  dispatch if a certain condition is met.The function that is returned by thunk receives the store’s dispatch method which is used to dispatch synchronous actions inside the function’s body once the asynchronous actions have been completed. Redux thunk deal with functions as actions. 

To add redux thunk to you project, you must npm install redux thunk. After this you need to import redux-thunk and insert its middleware into Redux. Then you need to wrap thunk in the applyMiddleware call and pass it in as a parameter. After doing all this you can now dispatch functions that do whatever you want them to do. 

