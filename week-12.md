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
