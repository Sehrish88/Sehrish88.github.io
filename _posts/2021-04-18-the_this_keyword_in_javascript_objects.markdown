---
layout: post
title:      "The 'this' keyword in JavaScript Objects"
date:       2021-04-18 18:29:36 +0000
permalink:  the_this_keyword_in_javascript_objects
---

![](https://i.morioh.com/2020/02/29/921d5f3b9edb.jpg)


The *this* keyword in JavaScript has eluded and confused many a programmer when it comes to JavaScript. The simple explanation is that the *this* keyword refers to the objects it belongs to. The confusion lies in the fact that it has different values depending on where and how it is used. Its value is different when it is used in a method, alone, a function, used in a functtion in strict mode, event handlers and objects. In this post, we will discuss *this* in javascript objects. 

We can start by building an animal object. My favorite animals are lions so we will go with that:

```
const lion = {
  dietType: 'carnivore',
  makeSound() {
    console.log('roarrrrr')
  }
}
```

We gave the lion object a property and some functionality via the `makeSound()` method. We can now invoke this method to print the sound a lion makes to the console:

`lion.makeSound() // Prints roarrrrr`

Everything is working fine so far. Say if we wanted to add a method to our *lion* object that prints to the console the `lion`'s `dietType`? We could add that method like so and then invoke it: 

```
const lion = {
  dietType: 'carnivore',
  makeSound() {
    console.log('roarrrrr');
  },
  diet() {
    console.log(dietType);
  }
};
lion.diet()
```

> However we will see that invoking that method does not print that sound a lion makes to the console! Instead, we get a reference error:` "ReferenceError: dietType is not defined"`


