# Week 1️⃣3️⃣

## Rounding off Some JS Programming Fundamentals

Below is a brief, minimal outline of the major concepts to be aware of as we round off some JavaScript programming fundamentals and move back into the DOM.

These fundamental JavaScript concepts, such as functions, conditional logic, data types, arrays, and objects, form the foundation for working with the DOM and building interactive web pages. Understanding how to manipulate and interact with data using these concepts will be crucial as we move forward.

If you have any doubts or queries, please ask ASAP on our [Discussions - Q&A?](https://github.com/orgs/SWIC-177/discussions/categories/q-a)

1. **Functions**

   - Functions are reusable blocks of code that can take parameters and return values.
   - Functions can be declared using the `function` keyword or as arrow functions.
   - Parameters are placeholders for values passed to the function, while arguments are the actual values.
   - Functions have their own scope, and variables declared inside a function are not accessible outside of it.

2. **Conditional Logic**

   - `if` statements execute a block of code if a specified condition is true.
   - `else` statements provide an alternative block of code to execute if the condition is false.
   - `else if` statements allow for multiple conditions to be checked.
   - Comparison operators (`===`, `!==`, `>`, `<`, `>=`, `<=`) are used to compare values in conditions.

3. **Logical Operators**

   - Logical AND (`&&`) returns true if both operands are true.
   - Logical OR (`||`) returns true if at least one operand is true.
   - Logical NOT (`!`) negates a boolean value.

4. **Primitive Data Types**

   - `undefined` represents a variable that has been declared but not assigned a value.
   - `null` represents a deliberate non-value or null value.
   - Primitive data types are immutable and are passed by value.

5. **Collection/Composite Data Types**

   - Arrays are ordered collections of elements accessed by numerical indices.
   - Objects (object literals) are unordered collections of key-value pairs accessed by their keys.
   - `const` with arrays and objects does not make them immutable, but prevents reassignment of the variable.

6. **Object Literals**
   - Object literals are a way to create objects with properties and values.
   - Properties can be accessed using dot notation (`object.property`) or bracket notation (`object["property"]`).
   - Functions can work with object literals by passing them as arguments or returning them.

## Callbacks and Closures

1. [Closures](https://youtu.be/3CfCole_3hw?si=OXZnd7BHUpxIQdQu)
1. [`.map` Method](https://youtu.be/d6WMQgChmQ8?si=aAXZnPD3Ov28aRhX)

## Homework Due Tuesday I

2️⃣ Gists (can be put into the same MD file) summarizing the following:

1. Summarize what you learned from the videos. How was the solution code for **closures** different from your own? What did you pick up from the official solution video walkthrough.
1. Summarize what you learned from the video walkthrough on `map`. Given the AI explanation and the supplemental video, what did you learn about `map`? Compare and contrast using `map` with a `for`/`while` loop.

## Homework Due Tuesday II

Create a 'teach back' video to give your explanation of the following code:

```js
const INCREMENTS = [1, 2, 3];

function createScoreIncrementor(increment) {
  return (score) => score + increment;
}

const scoreUpdaters = INCREMENTS.map(createScoreIncrementor);
```

Be detailed and mindful of terminology. Show your face as you would do in an interview situation and verify that you 🎤 is working well enough to produce reasonably good audio.

Submit the video (direct link preferred) in BrightSpace.

## Homework Due Tuesday III

Create another example of using a `map` function with an array of objects. The objects should have at least two properties. The `map` function should return a new array of objects with at least one property modified. Create a video walkthrough of your code, explaining what you are doing and why. Submit the video (direct link preferred) in BrightSpace. 5 points bonus for sharing your video in our [Show and Tell](https://github.com/orgs/SWIC-177/discussions/categories/show-and-tell). To earn the bonus points, your video must be shared **as a direct link (e.g. ScreenPal, Vimeo, YouTube, etc.) and not as an attachment.**

The link can be 'unlisted' so that it does not appear in search results. Or, you may want to start making these public and adding them to your portfolio/resume.
