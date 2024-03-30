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
