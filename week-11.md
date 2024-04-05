# Week 11

## Homework Due Tuesday

Head on over to the [**4th edition of _Eloquent JavaScript_**](https://eloquentjavascript.net/03_functions.html) and read _Chapter 3️⃣_ on Functions up to the part on **closures.** [This video](https://somup.com/cZeZbuCbWB) shows where to start and stop.

Write up an MD file (Gist) that summarizes what you got out of the chapter. What can you add from your own perspective? Are the concepts relatable to anything that you have seen in other courses or maybe in your own life? What are some examples that you can think of that would help you understand the concepts better?

Compare and contrast what's in this chapter with what we've already seen and done. What was new and different? What was the same? What was easier? What was harder?

Note that this particular code example from the reading is not great for a few reasons. Do give it a once over though and jot down your thoughts.

```js
const hummus = function (factor) {
  const ingredient = function (amount, unit, name) {
    let ingredientAmount = amount * factor;
    if (ingredientAmount > 1) {
      unit += "s";
    }
    console.log(`${ingredientAmount} ${unit} ${name}`);
  };
  ingredient(1, "can", "chickpeas");
  ingredient(0.25, "cup", "tahini");
  ingredient(0.25, "cup", "lemon juice");
  ingredient(1, "clove", "garlic");
  ingredient(2, "tablespoon", "olive oil");
  ingredient(0.5, "teaspoon", "cumin");
};
```

Also, the author tends to use `let` and for the reasons we have mentioned previously and as per our ESLint Style Guide, we should be using `const`.

## ➿ Code 👩🏾‍💻 Review

[Video](https://youtu.be/SUX8UZg0RnA?si=4GwBNijvJZHbq2Hb)

## First Part of HW Due Thursday

Compare and contrast your video code walkthrough with the one above ☝️. What was different? What was the same? Was there anything new or different that you learned from watching this video? It's fine if there's not. Just jot down your thoughts in a GitHub Gist in MD format. This 1️⃣ can be fairly short...

## Second Part of HW Due Thursday

This will be a short video explanation, like an interview question.

Consider these 2️⃣ code snippets:

```js
const name = "John Doe";
let otherName = name;

console.log(`Name is: ${name}`);
console.log(`Other name is: ${otherName}`);

otherName = "Jane Doe";

console.log(`Name is: ${name}`);
console.log(`Other name is: ${otherName}`);

otherName = 23;
console.log(`Name is: ${name}`);
console.log(`Other name is: ${otherName}`);
```

---

```js
const younger1 = 13;
let younger2 = younger1;

function incrementAge(age) {
  return age + 1;
}

younger2 = incrementAge(younger2);

console.log(`Younger1 is: ${younger1}`);
console.log(`Younger2 is: ${younger2}`);
```

Using these code snippets (paste them in 1️⃣ at a time), walkthrough the code, explain why the output is what it is and...answer the following question: How does this code illustrate the concept of JS **primitives being 'pass by copy/value'?**

## Third Part of HW Due Thursday

Read _Eloquent JavaScript_ [Chapter 4️⃣] up until _The Lycanthrope's Log._ This [video shows where to start and stop.](https://somup.com/cZfVeUCtmr)

Write up an MD file (Gist) that summarizes what you got out of the chapter. What can you add from your own perspective? Are the concepts relatable to anything that you have seen in other courses or maybe in your own life? What are some examples that you can think of that would help you understand the concepts better?

## Fourth Part of HW Due Thursday

Consider this code snippet:

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

const otherPerson = person;

otherPerson.name = "Jane Doe";

console.log(`Person's name is: ${person.name}`);
console.log(`Other Person's name is: ${otherPerson.name}`);
```

In a video response (a la an interview question), explain why the output is what it is. How does this code illustrate the concept of JS **objects being 'pass by reference'?**

Also, in the same video, explain how we would access the `zip` property of the `address` object in the `person` object.

---

## Functions are First Class

In JavaScript, functions are first-class citizens. This means that they can be passed around like any other value. This is a powerful concept that allows us to write more modular and reusable code.

Anything that we can do with another data type, we can do with functions! We can assign them to variables, pass them as arguments to other functions, and return them from other functions.

### Creating Functions with `const` (or `let`)

If functions are 'first-class citizens' in JavaScript, then we should be able to assign them to variables just like any other type of data.

[Arrow Functions](https://somup.com/cZfhe1CaTW)

### Passing Functions as Arguments

If functions are 'first-class citizens' in JavaScript, then we should be able to pass them as arguments to other functions, just like any other type of data.

[Passing Functions as Arguments](https://somup.com/cZfhnoCa3K)

### Returning Functions from Functions

If functions are 'first-class citizens' in JavaScript, then we should be able to return them from other functions, just like any other type of data.

This really unlocks some powerful **functional programming** patterns that we can use in our code. In this case, **higher order functions,** **closures** and even **currying**.

[Returning Functions from Functions](https://somup.com/cZfhn7CaTf)

## Homework Due Saturday (20 points)

These are some deep concepts! What do you think 🤔? Naturally, you'll write up an MD Gist that summarizes your thoughts and perspectives on these concepts. What's your level of comfort with them? Do you have any other analogies or perspectives that you would use to explain these things in an interview?

In addition to the write up, I want you to emulate the code from the videos and add them to 'JS First 🩸 Blood.' Notice that I said emulate. That means that you don't need to just blindly copy what I am doing. Change something up. The data, the variables names something. You'll find that if you change up the code even just a bit and think about it rather than just copy it, the learning will go much better. 🤓

---

Finally, try this exercise on:

We need some functions that we can call on the fly that will increment a hypothetical score board. So, for instance, thinking about 🏀, we can increment the score by 1️⃣, 2️⃣ or 3️⃣. For 🏈, it can be: 2️⃣, 3️⃣ or 6️⃣.

Create a function that will take in a score and return a function that will increment the score by that amount. So, if we pass in 3️⃣, we should get back a function that will increment the score by 3️⃣.

You should find this to be similar to what you saw in the video 📹 for the 'multipliers.' But these are...'adders.'

---

As usual, **commit** and **push** the code to 'JS First Blood' and **submit** the link to the Gist in (Not so Bright) BrightSpace! You can just keep overwriting the 'index' file, or you can create a new file for each of the exercises. **Be sure to mention in your submissions what files I should be looking at!**
