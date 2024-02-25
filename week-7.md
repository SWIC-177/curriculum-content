# Week 7

## Homework Review

In last week's homework, you were to reflect on my reflections. There's not much left to say about that. We going to end up in a recursive loop if I now reflect on your reflections of my reflections. 🤯 Suffice to say that learning to program, like most worthwhile tasks, requires patient and persistent effort along with some grit and determination.

Next, we walked through the setup of basic 'NodeJS Template Repo'. This is a good starting point for any NodeJS project. A summary of the various files follows.

`.eslintrc.cjs`: This is the configuration file for ESLint, a tool for identifying and reporting on patterns found in ECMAScript/JavaScript code.

`.git`: This is a hidden directory where Git keeps all of its metadata for the repository. This includes objects for your commits, refs to heads, remotes, tags etc.

`.gitignore`: This file specifies intentionally untracked files that Git should ignore. Files already tracked by Git are not affected.

`.prettierignore`: This file is used to exclude certain files from formatting by Prettier, a code formatter.

`.prettierrc`: This is the configuration file for Prettier. It specifies how your code should be formatted.

`.vscode`: This directory stores settings specific to your Visual Studio Code IDE, such as workspace settings and recommended extensions.

`README.md`: This is a documentation file that typically includes information about the project, such as how to install, use, and contribute to the project.

`index.js`: This is typically the entry point file of your Node.js application or module.

`node_modules`: This directory contains all the Node.js dependencies (libraries, modules) that are installed via `npm`.

`package-lock.json`: This is an automatically generated file that is meant to keep track of the exact version of every package that is installed so that a product is 100% reproducible in the same way even if packages are updated by their maintainers.

`package.json`: This file holds various metadata relevant to the project. This file is used to give information to npm that allows it to identify the project as well as handle the project's dependencies.

Finally, we introduced some basic JS code.

```js
// Define a function that adds two numbers
function addNumbers(num1, num2) {
  return num1 + num2;
}

// Call the function and store the result in a variable
const sum = addNumbers(5, 10);

// Print the result to the console
console.log("The sum is:", sum);
```

The code starts by **defining a function** named `addNumbers`. This function takes two **parameters:** `num1` and `num2`. These parameters are placeholders for the actual values that will be passed into the function when it's called.

Inside the function, there's a **return statement.** This statement adds the values of `num1` and `num2` together and returns the result. The **return keyword** means that the function will output this value whenever it's called.

After the function definition, a **variable** named `sum` is declared using the **`const` keyword.** This variable is assigned the result of calling the `addNumbers` function with two arguments: `5` and `10`. The function adds these two numbers together and returns the result, which is then associated or connected with the `sum` variable. By variable, we mean a named spot in the computer's memory. We chose to call this spot `sum`. By using `=` we are assigning the value of the sum of 5 and 10 to the `sum` variable.

Finally, the value of sum is printed to the console using `console.log`. This is a built-in JavaScript function that outputs its arguments to the **console.** This console can be in the terminal (if using Node) or in the browser's console if we are connected to an HTML file. In this case, it's outputting a string `"The sum is:"` followed by the value associated with the variable `sum`. Here, **string** means a sequence of characters. In this case, the sequence is `"The sum is:"`. It's akin to word-for-word dialogue in a book or movie. It's meant for humans to read. JS will not try to interpret it as a number or anything else. It's just a string of characters.

## Fix Template Repo to Include `.vscode` Directory

[Video](https://somup.com/cZnZYbpzOa)

## Re-Read the Same Codes from Last Week

We re-read the same code, but we explore a couple of other facets. Once again, no need to actually do anything. Just watch and listen. Take 🎶.

1. [`;` and `return`](https://somup.com/cZnZY7pztv)
1. [`const`](https://somup.com/cZnZrQpztM)

## Re-Read the _Eloquent JavaScript_ Example Codes

Same thing. Nothing to do but watch and listen. Take 🎶.

1. [Video](https://somup.com/cZnZrOpzub)

## _Eloquent JavaScript_ Reading

[This video](https://somup.com/cZnZrwpzut) shows where to start and stop reading for this week. It's a short reading. Just a few pages. Read _Chapter 1_ up until _Empty Values_.

## JS Basics

### Strings

[Video](https://somup.com/cZnZrMpzuP)

Strings are sequences of characters, such as letters, numbers, and punctuation marks. They are used to represent text and are created by enclosing their content in single or double quotes.

```js
const name = "John";
const greeting = "Hello, world!";
```

### Numbers, Booleans, Comparisons, `const` and `let`

[Video](https://somup.com/cZnZ3FpzUC)

#### Numbers

Numbers are used to represent numeric values. They can be integers (whole numbers) or floating-point numbers (decimals). They are created by simply writing a number with or without a decimal point.

```js
const age = 30;
const price = 9.99;
```

#### Booleans

Booleans are used to represent true or false values. They are created by simply writing `true` or `false`.

```js
const isRaining = true;
const isSunny = false;
```

However, it's not very useful to create Booleans such as this. Instead, we want to create Booleans by comparing values. For example, we might want to compare the value of `age` to `18` and see if `age` is greater than `18`. This would be written as `age > 18`. This would return `true` if `age` is greater than `18` and `false` if `age` is less than or equal to `18`.

```js
const age = 30;
const isAdult = age > 18;
```

#### `const` and `let`

These are used to declare variables. `const` is used to declare a variable that cannot be reassigned. `let` is used to declare a variable that can be reassigned.

#### Primitive Data Types

The examples that we have just seen represent **primitive data types.** These are discrete or single pieces of data.

#### So, Does `const` Mean Constant?

For the purposes of primitive data types the answer is, yes.

However, this is not entirely accurate. As we will see later when dealing with collection/composite types it doesn't necessarily mean 'constant.'

It's more correct to say that `const` means a _constant reference to a specified value._ Or, we can say that variables declared via `const` cannot be reassigned. Once a value is assigned to a variable via `=` it is forever associated or connected with that variable.

#### Primitive Data Types Are Immutable

Once it's been created, a primitive data type cannot be changed or mutated. It has to be thrown away and a new one created. This is why we say that primitive data types are immutable. This is why we say that `const` means constant for primitive data types.

That is why we must use `let` if we want to 'change' the value of a variable. `let` means that we are 'dating' a primitive data type. We can change our mind and date someone else. We can reassign the variable to a new value. We can't do that with `const`. `const` means that we are 'married' to a primitive data type. We can't change our mind. We can't reassign the variable to a new value.

#### Summary

- Strings are sequences of characters.
- Numbers are used to represent numeric values.
- Booleans are used to represent true or false values.
- `const` is used to declare a variable that cannot be reassigned.
- `let` is used to declare a variable that can be reassigned.
- Primitive data types are immutable.

## Homework Due Saturday (20 points)

You already know :).

Summarize the salient points and takeaways from the videos and readings above. Add your own thoughts and reflections. What did you learn? What did you find interesting? What did you find challenging? What do you want to learn more about?

Just submit the links to your MD files. Again, quality writing, use of headings and other features of MD are expected. Be detailed and thorough.
