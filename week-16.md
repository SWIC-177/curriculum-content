# Week 16

## Homework Due Saturday

### How to Proceed with the Rest of This Homework/Lesson

You will be using your HTML Tailwind projects that you created and deployed about 2️⃣ months back. As a reminder, [here](https://github.com/SWIC-177/tailwind-demo/blob/e8c7d3e26bc2bbaaa46dd5a725fb4cc12e5b7cda/index.html#L63) was the one that I created for the lesson. You would have created your own rendition of some type of form styled with Tailwind and [launched it on Netlify.](https://github.com/orgs/SWIC-177/discussions/categories/show-and-tell?page=2)

If you don't have your own working version of this repository, you may fork the one used in this lesson demo, as mentioned in the video content 👇🏾, but you will not receive full credit for this homework. You should have your own version of this repository.

Since everyone's should be a bit different, at least in the look and feel, and considering that this may be a bit challenging for some, you are strongly encouraged to share ideas in our [Q&A Discussions.](https://github.com/orgs/SWIC-177/discussions/categories/q-a) However, please do not share entire code snippets. Instead, share ideas and concepts. This is a great way to learn from each other and to help each other out without lazily copying and pasting code.

We will be using the forms that you created, specifically. Your form should have at least 3️⃣ fields. You may need to update your HTML form accordingly in order to follow along with this lesson. Make sure that you hare making appropriate commits.

Specifically, you must implement at least 3️⃣ different JS validations on your form. Whenever there is a violation, the appropriate feedback should be displayed to the user. As soon as the error is corrected, the feedback should disappear.

The rest of this lesson will serve as a guide, not a code-along. You will adapt this to **your own** form. You may follow this closely as most of the forms will probably be the similar, but it should be adapted to your own form and not identical to this one.

This lesson will be using the [validator.js library.](https://github.com/validatorjs/validator.js) You are not obligated to use it, but it is a good library to use for realistic and reliable form validation.

The lesson goes above and beyond the requirements for this homework, so leverage as much or as little as needed. As always, code quality and commit messages are important.

For your submission, you will need to push your work to GitHub, which will update your Netlify deploy. You will then write a brief reflection and summary of what you did/learned. Share this along with your deployed link in our [Show and Tell](https://github.com/orgs/SWIC-177/discussions/categories/show-and-tell).

Since we are basically sharing the codes, **the most important part of this submission will be a detailed video walk through of your code.** Your video should be upwards of 10 minutes long and should show your form in action. You should show how the form behaves when the user enters incorrect data and how the form behaves when the user enters correct data. You should also show how the form behaves when the user tries to submit the form with incorrect data.
It is critical that you convey an understanding and clear explanation of the code that you wrote. You should be able to explain why you wrote the code that you did and how it works. You should also be able to explain how you would modify the code to add additional validations or change the behavior of the form.

In addition to the video, you will create a Gist. You will provide reflections on your experience working through this lesson. Be sure to mention new things that you learned, for instance in the MDN links 👇🏾.

Include a direct link to your 'Show and Tell' and also for your video in your BrightSpace submission. Again, a direct link works best. If I have to download your video, I will not be happy. 😡

### Form Validation Overview

When we mention form validation, we are talking about ensuring that the data entered into a form is correct. This can be as simple as ensuring that a field is not empty, or as complex as ensuring that a field is a valid email address.

Through the use of HTML attributes such as `required`, `minlength`, `maxlength`, and `pattern`, we can enforce some basic validation rules. However, these rules are built into the browser and have 0️⃣ effect until the user clicks the submit button. Instead, we can use JavaScript to provide instant feedback to the user as they type in the form 🚸.

#### Additional Resources

For further clarity, you should read the following from MDN:

1. [What is form validation?](https://developer.mozilla.org/en-US/docs/Learn/Forms/Form_validation#what_is_form_validation)
1. [Different Types of Client-Side Validation](https://developer.mozilla.org/en-US/docs/Learn/Forms/Form_validation#different_types_of_client-side_validation)

### Updating Some HTML and CSS First

[Video](https://go.screenpal.com/watch/cZh1caVMJbp)

**Note:** Here is how I set up my Tailwind directives. It's a bit different from the video, but shouldn't make a big difference. I just didn't feel that `is-error` was a bona fide 'component.' It felt more like a utility that worked with the `error` Tailwind component.

```css
@layer components {
  .error {
    @apply mt-2 scale-y-0 font-semibold text-red-500;
  }
}

@layer utilities {
  .is-error {
    @apply scale-y-100 transition-transform delay-75;
  }
}
```

### Prepping for JS

There are a few updates that you will want to add as we didn't originally set this repo up to use JS. Therefore, there is no ESLint and Prettier set up! 😱

1. Copy/paste [`./.vscode/extensions.json`](https://github.com/SWIC-177/tailwind-demo/blob/main/.vscode/extensions.json) into your `.vscode` folder. Make sure that you install any of the missing extensions.
1. Copy/paste [`./.vscode/settings.json`](https://github.com/SWIC-177/tailwind-demo/blob/main/.vscode/settings.json) into your `.vscode` folder.
1. Copy/paste [`.eslintignore`](https://github.com/SWIC-177/tailwind-demo/blob/main/.eslintignore) into your project's root directory. Repeat this for [.prettierignore](https://github.com/SWIC-177/tailwind-demo/blob/main/.prettierignore).
1. Copy/paste [`.eslintrc.js`](https://github.com/SWIC-177/tailwind-demo/blob/main/eslint.config.js) into your project's root directory. The ESLint configuration is using the new 'flat file' structure for ESLint v9. I don't really get the benefit or anything, but let's just use it and move on.
1. Copy/paste [`package.json`](https://github.com/SWIC-177/tailwind-demo/blob/main/package.json). You will need to run `npm i` to install the necessary packages.
1. Copy/paste [`tailwind.config.js`](https://github.com/SWIC-177/tailwind-demo/blob/main/tailwind.config.js). Notice the update to include any Tailwind found in the JS files!

At this point, you should have ESLint and Prettier set up with VS Code. If you get stuck, [ask questions](https://github.com/orgs/SWIC-177/discussions/categories/q-a)) before moving on.

### Form Validation Planning and Pseudo-Code

For the purposes of this lesson, we will be applying the following validations to our form:

1. The name field must not be empty. Let's assume a minimum of 6 characters with at least one space. It should be a full name. The message will say, "Please enter your full name."
1. The email field must not be empty and must be a valid email address. The message will say, "Please enter a valid email address."
1. The phone number field must not be empty and must be a valid phone number. The message will say, "Please enter a valid phone number."
1. The message field must be between 10 and 100 characters. The message will say, "Please enter a message between 10 and 100 characters."
1. The 'Submit' button should be disabled until all fields have been touched and are valid.

You can set up the same or similar rules. You can also add more validations if you wish.

Here's some pseudo-code (these can make for good commit messages!) to consider before we start writing the actual code:

```text
/**
 * TODO:
 * 1. 'Select' all of the input fields.
 * 2. 'Select' the submit button.
 * 3. Add event listeners to each input field, such that
 *  upon losing focus (`blur` event) on the input fields, we will
 * show the error. For now, we are not validating the input fields.
 */
```

### Select the Form Inputs

In the code shown in the video 👇🏾, I use the **spread operator** to 'mix in' an additional elements into a new array. For reference, here's a simpler example of this an array of strings:

```js
const names = ["John", "Jane", "Jack"];
const newName = "Jill";

const newNames = [...names, newName]; // ['John', 'Jane', 'Jack', 'Jill']
```

Now, that code can be simplified to:

```js
const names = [...["John", "Jane", "Jack"], "Jill"]; // ['John', 'Jane', 'Jack', 'Jill']
```

We are just spreading an array out inline. You don't have to do it in such a short way. Write the code in a way that makes sense to you, but do try to avoid unnecessary mutations, as we are doing with the spread.

[Select all of the input fields](https://somup.com/cZh1VC5D4s)

### Add Event Listeners to the Input Fields

Before proceeding, review the following from MDN:

1. [_What is an event?_](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Events#what_is_an_event)
1. [_Using `addEventListener()`_](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Events#using_addeventlistener)

Again, if you have specific questions, use the [Q&A Discussions](https://github.com/orgs/SWIC-177/discussions/categories/q-a).

Also, in the upcoming video, I use a `forEach`. It's very similar to `map`, but it doesn't create a new array or return anything. It's just a way to iterate over an array. You can use `map` if you want, but you don't need to return anything.

```js
const names = ["John", "Jane", "Jack"];

// I'm just using side effects with `console.log`. No need for a `map`...
names.forEach((name) => {
  console.log(name);
});
```

[Add event listeners to the input fields](https://somup.com/cZh1nh5DaG)

### Start Validating the Form

Here's some more pseudo-code to consider:

```text
1. Whenever an input field, is blurred, identify it and get its value.
2. Utilize the `id` attribute and this value to call some type of
validation function. This function will return a boolean value.
It will take the value and 'validate' it based on the rules we set.
```

To implement this, I chose to use [`find`.](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/find)

`find` works similarly to `filter` in that it works on any object that is based on the Array prototype, but it doesn't create any new array. Instead, it immediately returns whatever element matches the condition. If no element matches, it returns `undefined`.

```js
const names = ["John", "Jane", "Jack"];

// It just returns the first matching element. It doesn't make a whole array.
const foundName = names.find((name) => name.startsWith("J")); // 'John'
```

The code also calls a **method.** Recall that a method is a function that is a property of an object. Here's a simplistic example related to some strings:

```js
const nameISelected = "John";

// This is a contrived example, as there's no reason to duplicate the method.
const names = [
  {
    name: "John",
    validateAdulthood(age) {
      return age >= 18;
    },
  },
  {
    name: "Jane",
    validateAdulthood(age) {
      return age >= 18;
    },
  },
  {
    name: "Jack",
    validateAdulthood(age) {
      return age >= 18;
    },
  },
];

/**
 * 1. Find the person whose name matches `nameISelected`.
 * 2. Call the `validateAdulthood` method with the age of 21.
 */
const isAdult = names
  .find((person) => person.name === nameISelected)
  .validateAdulthood(21); // true
```

[Call validation method on blur](https://somup.com/cZh1nA5DAw)

### Displaying the Error Message

We'll add some 'library functions,' one to show the error and the other to remove the error message. This will receive the element in question along with an error message. Specifically, here's the pseudo-code:

1. Create a function that will accept an element and an error message.
1. Each of these elements has a parent `div`. We will use this to append the error message.
1. We'll either update the `innerHTML` of the parent `div` or, just add/remove the `is-error` class to toggle the visibility of the error message.

When writing these we'll be using some new DOM methods:

1. [`parentNode`](https://developer.mozilla.org/en-US/docs/Web/API/Node/parentNode). This is used to find the parent of an element.
1. [`classList`](https://developer.mozilla.org/en-US/docs/Web/API/Element/classList). This is used to add or remove CSS 💄 classes from an element.
1. [`appendChild`](https://developer.mozilla.org/en-US/docs/Web/API/Node/appendChild). This is used to add a child element to a parent element.

[Show/hide the error](https://somup.com/cZh1eU5DkF)

### Validating the other Fields

At this point, I installed [Validator.js](https://github.com/validatorjs/validator.js). `npm install validator`.

[Validate the other fields](https://somup.com/cZh1eB5DkJ)

---

Upon exploring the enabling/disabling of the Submit button, it was determined that this was a bit much at this point. However, how do you think that it could be done? Write up a few thoughts and include them in your Gist.
