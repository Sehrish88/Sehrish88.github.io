---
layout: post
title:      "The 'this' keyword in JavaScript Objects"
date:       2021-04-18 14:29:36 -0400
permalink:  the_this_keyword_in_javascript_objects
---

![](https://i.morioh.com/2020/02/29/921d5f3b9edb.jpg)


The *this* keyword in JavaScript has eluded and confused many a programmer when it comes to JavaScript. The simple explanation is that the *this* keyword refers to the objects it belongs to. The confusion lies in the fact that it has different values depending on where and how it is used. Its value is different when it is used in a method,used alone, a function, used in a functtion in strict mode, event handlers and objects. In this post, we will discuss *this* in javascript objects. 

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

Everything is working fine so far. Say if we wanted to add a method to our `lion` object that prints to the console the `lion`'s `dietType`? We could add that method like so and then invoke it: 

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

However we will see that invoking that method does not print the sound a lion makes to the console! Instead, we get a reference error:` "ReferenceError: dietType is not defined"` This is strange because we would expect thast the `dietType` would be defined since it is a property of the `lion` object. It is returning `undefined` because in the `scope` of the `.diet()` method we do not automatically have access to the properties of the `lion` object. 

How can we get the `.diet()` method to work? By using the `this` keyword! We have to change the `.diet()` method to use the `this` keyword like so: 

```
const lion = {
  dietType: 'carnivore',
  makeSound() {
    console.log('roarrrrr');
  },
  diet() {
    console.log(this.dietType);
  }
};
lion.diet()
```

Now the `.diet()` method works! As stated earlier, the `this` keyword refers to the object it belongs to and provides access to that object's properties. For this case, the object that `this` belongs to is `lion`, so by using `this` we are able to access the `lion` object and its `dietType` property by using dot notation. 

That was pretty straightforward, however it gets a little complicated when we use the `this` keyword in arrow functions within a method. Lets refactor our `lion` object a bit to use an arrow function for the `diet()` method: 

```
const lion = {
  dietType: 'carnivore',
  makeSound() {
    console.log('roarrrrr');
  },
  diet: () =>  {
    console.log(this.dietType);
  }
};
lion.diet()
```

Calling the `.diet()` method now will print `undefined` to the console. Why is that? This change in behavior resulted from the fact that we used an arrow function to define the `.diet()` method. Arrow functions have a built in functionality which `bind`s or ties the value of the function to an already defined value that is NOT the calling object. In the example above, the value of `this` is an object which exists in the global scope that DOES NOT have a `dietType` property which is why calling the `.diet() `method returns `undefined`.  

Remeber to use the `this` keyword in methods in your objects to be able to access the object's properties,  but avoid defining those methods using arrow functions. 



