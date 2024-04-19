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

---

## Closing the Gap Between HTML/CSS and JavaScript

Now that we have the basics of programming in JavaScript, we can move back into working in the browser, where we can apply our skills in am more appealing and realistic manner than just outputting to the console.

### BOM and DOM

The Browser Object Model (BOM) and the Document Object Model (DOM) are two separate models that allow us to interact with the browser and the HTML document, respectively.

- **BOM**: The Browser Object Model is a set of objects provided by the browser that allow us to interact with the browser itself. This includes objects like `window`, `navigator`, `location`, `history`, and `screen`. We can use the BOM to manipulate the browser window, change the URL, and interact with the user's screen.
- **DOM**: The Document Object Model is a representation of the HTML document that we can interact with using JavaScript. We can use the DOM to create, modify, and delete elements on the page, as well as add interactivity to our websites.

In both cases, we note that JavaScript itself is just another programming language. It doesn't have any knowledge of what an browser is or what an HTML document is. It's the browser that provides the JavaScript engine with the objects and methods that allow us to interact with the browser and the document.

To put it another way, we are modeling the browser itself along with HTML documents as...objects! JavaScript doesn't know about browsers or HTML, but it sure as heck knows about objects. Anything that can be represented as an object can be manipulated by JavaScript.

This is why JavaScript is so powerful in the browser. It's not because JavaScript is some special language, but because it became 'the chosen one' for browsers back in 1995.

[Let's Read](https://somup.com/cZfD0GC7RM)
[BOM and DOM Demo I](https://somup.com/cZfbc1C7Ss)
[BOM and DOM Demo II](https://somup.com/cZfbcFC7WO)
[BOM and DOM Demo III](https://somup.com/cZfbcvC7WW)

## Homework Due Thursday

1. Write a Gist up about the lesson, including the videos, of course. Convey that you actually watched the videos by commenting on what you saw and what you thought about it.
1. Use MDN and/or AI and explore some other things that can be done with the BOM and DOM. Record a brief video on your findings. Demo them if possible, or just show the explanation and example codes and walk us through it. Just 2 or 3 will be fine. Submit the video (direct link preferred) in BrightSpace.
1. Now, find any site of your choice and record a demo similar, but not identical to mine. Show some text manipulation and the use of `addEventListener`. You don't have to be limited to just `"click"`. There's a lot more you can do with `addEventListener`. Submit the video (direct link preferred) in BrightSpace.

Earn 5 points extra credit by sharing your videos in our [Show and Tell](https://github.com/orgs/SWIC-177/discussions/categories/show-and-tell). To earn the bonus points, your videos must be shared **as direct links (e.g. ScreenPal, Vimeo, YouTube, etc.) and not as attachments.** You can share voff in the same post!

## `map` Practice with the DOM and Beyond

1. [Simple Data Scraping](https://youtu.be/8M0tPevStqs)

## Homework Due Saturday I

Do some 'simple data scraping' on the site of your choice. It can be pretty much whatever you want to do, but should use `map` to 'extract data.'

Record a video of your process and submit the video (direct link preferred) in BrightSpace. For 5️⃣ points extra credit, share your video in our [Show and Tell](https://github.com/orgs/SWIC-177/discussions/categories/show-and-tell). To earn the bonus points, your video must be shared **as a direct link (e.g. ScreenPal, Vimeo, YouTube, etc.) and not as an attachment.**

## Homework Due Saturday II

We are starting some JS work in our new 'browser template repo.' Not much happens as of yet, but...

For _Section 1️⃣,_ here's the [GitHub Classroom Link.](https://classroom.github.com/a/eWpz5OR9).

For _Section 2️⃣,_ here's the [GitHub Classroom Link.](https://classroom.github.com/a/4zvHBur9)

### Videos

You are just to follow along and replicate what's in these videos.

1. [Overview](https://go.screenpal.com/watch/cZfqnhVsW8K) - You'll notice the code is actually a bit different from what's shown in the video. I made some minor updates after the recording.
1. [Commits and ESM](https://somup.com/cZfqnOCNJZ)

In addition to the following the code, I'll need another reflections Gist from you. Give some feedback on what's covered in the videos, including ESM and the `import` and `export` statements. What did you learn? What did you find interesting? What did you find challenging?

As emphasized in the videos, we are coming up on the end here so I'm re-emphasizing the importance of **commit messages,** and leveraging our template repo tooling. I will be grading extra hard for any 💩 commit messages at this point! No excuse between the demos and the extension shown!

---

We will be picking up with finishing this up next week and moving even more into the browser!
