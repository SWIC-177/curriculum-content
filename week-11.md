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
