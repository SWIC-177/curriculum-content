# Week 1️⃣2️⃣

## Review 📚

### Pass by Copy 📦

In JS, **primitive data types are passed by copy.** This means that when you assign a primitive value to a variable, the value is copied to the new variable. This is why when you change the value of the new variable, the original variable remains unchanged.

[Video](https://go.screenpal.com/watch/cZf1oGVs3Uy)

### Pass by Value 📦

This is just a variation of the same concept, but applies to calling functions with **primitive arguments.**

[Video](https://somup.com/cZf1osCAYP)

### Pass by Reference 📦

In JS, **objects are passed by reference.** This means that when you assign an object to a variable, you are actually assigning a reference to the object in memory. This is why when you change the object through the new variable, the original object is also changed.

An analogy would be two remotes that control the same 📺. Regardless of which remote changes the 📺 channel, the same 📺 is updated.

Previously, with the primitives, each remote controlled its own 📺.

[Video](https://somup.com/cZf1oRCArX)

## Mutations 🧬...and How 2️⃣ Avoid Them 🙅🏾‍♂️

Generally in programming, and especially when working with React, the most widely used (not necessarily the best) JavaScript UI library, we want to avoid mutating state. This is because it can lead to bugs that are difficult to track down.

How do we do this? By creating new objects and arrays instead of modifying existing ones. The most common way to do this is by using the **spread operator** (`...`).

This spread operator is used on any **iterable** type (like arrays and object literals). By iterable, we mean something that we can ➿ through.

Given our previous example, we can use the spread operator to create a new object with the same properties as the original object, but with a new value for the `name` property.

```js
const person = {
  name: "John Doe",
  age: 23,
  address: {
    street: "123 Main St",
    city: "New York",
    state: "NY",
    zip: "10001",
  },
};

// Create a new object with the same properties as the original object.
const otherPerson = { ...person };

otherPerson.name = "Jane Doe";

console.log(`Person's name is: ${person.name}`);
console.log(`Other Person's name is: ${otherPerson.name}`);
```

That's it. However, if you were to updated the **nested object** `address` in the `otherPerson` object, you would still be mutating the original object. This is because the spread operator only creates a **shallow copy** of the object. We'll...address this :) in a future lesson.

[Video](https://somup.com/cZf1DICAra)

**Note:** In the video I meant to do: `return p2Update`, not `return p`, as that just returns the original object!

1️⃣ analogy for the spread operator is that we can think of the object literal as a grocery bag of several items. We then SPREAD the items out on the table, go grab a new 👜 and we go find the same items and fill up a new bag. 🤷🏾‍♀️

### Refactor ♻️

[Video](https://somup.com/cZf1D0CAr8)

## First Part of Homework Due Tuesday

Update your 'JS First Blood 🩸' with the code examples shown (and `commit` and `push`, of course.) Let me know where to look 👀 for your work, whether you are overwriting `index.js` or you are keeping separate named files.

Write up a brief gist on what you think about all of this pass by copy, pass by value, pass by reference stuff. How do you feel about it? How do you think you would explain it to someone else? What analogies would you use?

How did you like the refactored version of the code; the fancy one-line arrow function with with implicit return? 🤓

## Second Part of Homework Due Tuesday

Copy/paste this code into your _JS First Blood._

```js
const people = [
  {
    id: 1,
    name: "John Doe",
    age: 23,
  },
  {
    id: 2,
    name: "Jane Doe",
    age: 29,
  },
  {
    id: 3,
    name: "Jim Doe",
    age: 34,
  },
  {
    id: 4,
    name: "Jill Doe",
    age: 45,
  },
  {
    id: 5,
    name: "Jack Doe",
    age: 56,
  },
  {
    id: 6,
    name: "Jenny Doe",
    age: 67,
  },
];

function renameOdds(p) {
  for (let i = 0; i < p.length; i++) {
    if (p[i].id % 2 !== 0) {
      p[i].name = "Odd Name";
    }
  }

  return p;
}

console.log(renameOdds(people));
```

You will notice the following linting error(s):

```sh
  35:33  error    Unary operator '++' used                          no-plusplus
  37:7   error    Assignment to property of function parameter 'p'  no-param-reassign
  44:1   warning  Unexpected console statement                      no-console

✖ 3 problems (2 errors, 1 warning)
```

You can ignore the ⚠️, of course. But, resolve the errors.

BTW, I generated the above output by running ESLint from the terminal with the Node Package EXecutor (npx) like so: `npx eslint index.js`. Naturally, you shouldn't have to do this as the errors should be showing up in VS Code automatically based upon our template repo and it's `setting.json` and `extensions.json` files.

Create a video to explain your work **along with committing and pushing the code itself.** Make sure it's clear in the BrightSpace submission where the work is!

---

## Methods

Thus far, we've been writing functions in the **global scope.** This is perfectly fine, as functions, unlike other data are meant to be used and reused by whoever needs them. Once the function is defined, it's just there and ready to use.

For instance:

```js
const sayHello = (greeting, name) => `${greeting} ${name}!`;
```

This function can be used by anyone, anywhere in the code. It's just there, ready to be called.

Alternatively, in object-oriented programming, we can define functions within objects. These are called **methods.**

**Methods** are nothing but functions that are scoped inside of an object literal. They are used to perform actions on the object itself, similar to what is done in traditional object-oriented programming.

```js
const person = {
  name: "John Doe",
  age: 23,
  address: {
    street: "123 Main St",
    city: "New York",
    state: "NY",
    zip: "10001",
  },
  sayHello(greeting) {
    return `${greeting} ${this.name}.`;
  },
};
```

In this code, we **cannot** just call `sayHello` in the global scope. We must call it on the `person` object: `person.sayHello()`.

[Video](https://youtu.be/irL9S40NfCQ?si=xr62CImwh5J5Rs89)

## _Eloquent JavaScript_ Review

1. [Eloquent Functions I](https://somup.com/cZfQbpCpUx)
1. [Eloquent Functions II](https://somup.com/cZf6cICpL8)
1. [Eloquent Data Structures I](https://somup.com/cZf6caCpN8)

## The Dual Nature of the Primitives: Strings, Numbers, and Booleans

Clearly, we've seen that **JS Objects** use **dot notation** to access properties and methods.

Everything in JS is an object except for **primitive data types.**

However, **primitive data types** like strings, numbers, and booleans can also use **dot notation** to access properties and methods. 😕

```js
const name = "John Doe";
console.log(name.length);
```

This is because JS automatically wraps the primitive in an object when you try to access a property or method on it. This is called **boxing.**

[Boxing of Primitive Data Types](https://somup.com/cZf6cGCp83)

## Moar _Eloquent JavaScript_ Review

1. [Eloquent Data Structures II](https://somup.com/cZf6VeCpPX)
1. [Eloquent Data Structures III](https://somup.com/cZf6V6CpPU)

## Homework Due Thursday I

This will be a Gist. Now that we've read through _Eloquent JavaScript_ 'together,' ☝️ what's changed since you wrote up the last Gist? What concepts are more clear? What can you add to the overall understanding of the material? What are you still struggling with?

Of course, we also mentioned **methods,** so how do you feel about those? Upload your Gist link to BrightSpace.

## Homework Due Thursday II

Now that we have covered it, go and find out about 3 methods in the MDN documentation 📝. Add a brief video explanation of each. You can walk through the documentation and/or do an actual brief code demo. There is no need to commit and push the code unless you want. You could even just have CoPilot help you out and then just focus on giving your explanation/perspective.

**DO NOT** just use the same ones that I used! Find out about 3 new ones! You may want to explore `String`, `Number`, `Array`, `Set`, `Object` and/or `Date` methods. But, pick any 3 that you find interesting or useful.

Share your video link in the BrightSpace submission.

### 5 Points Extra Credit

I will award an extra 5️⃣ points if you share your video in our [GitHub Discussion Board's Show and Tell](https://github.com/orgs/SWIC-177/discussions/categories/show-and-tell).

Regardless, you still need to upload it to BrightSpace so that I can easily see it, but if you do share it in the Discussion Board, just let me know in the BrightSpace submission, and I will review and comment it on there. It may need to be a link on the video on YouTube (you can do unlisted) or Vimeo or ScreenPal, etc. Discussions may not allow video uploads. Links are so much easier to work with anyway! :)

---

## JavaScript is a Multi-Paradigm Language

JavaScript is a multi-paradigm language. This means that it supports multiple programming paradigms. A **programming paradigm** is a style of programming. There are several programming paradigms, including:

1. **Imperative:** This is the most common programming paradigm for beginners, especially. It is based on the idea of changing the state of the program by executing commands. This is what we've been doing thus far.
1. **Declarative/Functional:** This is based on the idea of describing what you want to happen, rather than how you want it to happen. This is what we will be moving towards. It uses functions and expressions to describe the logic of a program. Purely functional programming (e.g. Haskell) is a subset of declarative programming. From a purist's perspective, JavaScript is not a functional programming language, but it does support functional programming concepts.
1. **Object-Oriented:** This is based on the idea of objects that contain data and methods. It is the core of how JavaScript was designed, but is arguably not as commonly used in modern JavaScript.

The fact that JavaScript supports multiple paradigms is one of the reasons it is so popular. It is a very flexible language that can be used in many different ways.

1. [Multi-Paradigm with Imperative and OOP](https://somup.com/cZf6nVCpRH)
1. [Improved OOP with Clean Code](https://somup.com/cZf6n4CpW5)

### The Functional Approach is NOT a Good Fit for This Problem

Upon starting to work this particular problem out in a functional way, it turns out that it's not a good fit for this problem. Here, we have a ➿ with a definite star and end. We are mutating the data as we go along. This is a good fit for an imperative approach.

For the record, here's the functional approach, heavily commented:

```js
/**
 * Calculates the sum of a range of numbers.
 *
 * @param {Object} [options] - The options for the range.
 * @param {number} [options.start=1] - The starting number of the range.
 * @param {number} [options.stop=10] - The ending number of the range.
 * @param {number} [options.step=1] - The step size between numbers in the range.
 * @returns {number} The sum of the numbers in the range.
 */
function sumRange({ start = 1, stop = 10, step = 1 } = {}) {
  // Create an array...
  return Array.from(
    // ...with the length of the range calculated from the `start`, `stop`, and `step` values.
    { length: (stop - start) / step + 1 },

    // Use a CALLBACK FUNCTION to fill the array with the numbers in the range.
    (_, i) => start + i * step

    // Use the REDUCE METHOD to calculate the sum of the numbers in the array.
  ).reduce(
    (acc, currentNumber) => acc + currentNumber,

    // Set the initial value of the ACCUMULATOR to `0`.
    0
  );
}

console.log(sumRange()); // 55
```

This is overly complex for the problem. In programming, it's about using the right tool for the job. In this case, the imperative approach is the right tool.

However, in most real-world scenarios, we are not solving relatively trivial looping problems like the one here. The most common task that we have, especially on the front end is transforming arrays of objects into HTML markup. This is where the functional approach shines, and where we are headed.

## Homework Due Saturday

1. Write a Gist on the multi-paradigm nature of JavaScript. Don't worry about that functional code, but do make sure to mention the **clean code** that was mentioned. Specifically, why did we use a single object instead of multiple arguments? What are the benefits of this approach? What is **destructuring?** How do we specify **default values** for function arguments?
2. Read this post about [using the DOM.](https://developer.mozilla.org/en-US/docs/Web/API/Document_object_model/Using_the_Document_Object_Model) What does it mean to you? Can you anticipate where we are going next? Can you conceive of how/why the JS programming fundamentals that we have covered will be used as we transition back to the web browser? 🔮
