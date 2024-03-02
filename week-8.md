# Week 8

## Homework Review

1. [We read through _Eloquent JavaScript_](https://somup.com/cZenFPpHiA). Hopefully, this will help you separate out what we really need to know.
2. [Some of this part](https://somup.com/cZenq1pHiM) was not covered in last week's lesson. We will cover it this week.

## How Do Computers Translate Human Language to 1s and 0s?

[This video](https://youtu.be/MijmeoH9LT4?si=vPFU72qsuC7LVB5A) ties together the concepts of 'How Computers Work' and how we use higher-level languages to communicate with them.

## Update Package Dependencies (`"devDependencies"`)

[This one](https://somup.com/cZenqbpHjn) is optional. Feel free to skip it if you are not interested in the details.

## Homework Code Review

[Video](https://somup.com/cZenqwpHj0)

## Create Data and Store It On the Heap

To interact and give instructions to a computer, everything we do is in terms of data and memory. Data must be created and then stored in a computer's memory for future access. Case and point, every single value that we create in JavaScript - `"string"`, `23`, `true`, `{name: "Manav", age: 230}, [1, 2, 3, "hello", { name: "Manav", age: 23 }]` - is stored in a generic area of memory commonly referred to as the heap. But how do we access this abstract data from memory? By creating references.

Note that we have not yet explained **collection types:** `{name: "Manav", age: 230}, [1, 2, 3, "hello", { name: "Manav", age: 23 }]`

## Create Primitive Data Types

[Primitives](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures#Data_types) are data types that can only hold **one discrete piece of data**.

There are seven primitive data types in all, but two are beyond the scope of this course.

Let's start with the three primitives we will use most:

### Strings

Strings are characters contained inside single ('') or double ("") quotation marks. JS works with the words just as they are shown. For example, "Hello, World!" is a string.

```javascript
// Using `""` - double quotation marks
"Manav";

// Using `''` - single quotation marks
'Manav'

"Hello, world";
'My name';
"23"; // ⚠️ If it has quotation marks, it's a STRING - not a NUMBER 👇🏽
"true";
'It was the best of times, it was the blurst of times...';

// However, don't mix up the 2 else your code will surely break!
"Manav' // Notice that this code is not recognized as a valid string.
```

### Numbers

Numbers are any numbers not contained in quotation marks.

```javascript
// Number examples:
23;
8675309;
1.99;
-1000;
9e3;
```

### Booleans

Booleans are `true` or `false`.

## Bind Data to Variable References with `const` and the Assignment Operator

In programming, it's commonplace to create 'references' to values in memory. This is the concept of 'instantiating a variable' (`const`, `let`) and 'assigning a value to a variable' (=). Whenever a value in memory no longer has a reference to it, the JS garbage collector comes along to completely removes it from memory.

```javascript
/**
 * `=` is an ASSIGNMENT OPERATOR. It takes whatever is on the right side and assigns it to the left.
 * So...on the right, we have a STRING. We can tell it's a STRING b/c it's wrapped in "".
 * On the left, a couple of things are happening:
 *   1. `const` is a keyword that reserves space in memory.
 *   2. After `const`, we give a name for that space in memory.
 *   3. The right side is assigned to the left side via an ASSIGNMENT OPERATOR, `=`.
 */
const js = "JavaScript"; // Semicolons are 'technically' optional...but it's kind of like writing sentences without periods.
const java = "Java";

// If we intend to RE-ASSIGN the VALUE associated with a VARIABLE, then we probably want to use 'let'
let x = 3;

/**
 * RE-ASSIGN the VALUE BOUND BY 'x'.
 * '3' is 'thrown out' and replaced
 */
x = 4;
```

There a couple of different schools of thoughts on `const` vs `let` (or even their predecessor, `var`). We will always use `const` unless we have a deliberate intent to replace a value.

## Operators and Operands

`+`, `-`, `*`, `/`, all behave...pretty much as you would expect...

Here's one that you might not know: `%`. This gives us the remainder whenever it's used with 2 operands (fancy word for numbers that we are working with). So...what would `3 % 2` be? `1` - the remainder of dividing `3` by `2` is `1`.

### Concatenate with `+`

```javascript
const firstName = "Manav";
const lastName = "Misra";

const fullName = firstName + " " + lastName; // "Manav Misra"
```

`+` can can also be used with **strings** to **concatenate** (fancy word that means 'combining' things) them. For example, `"Hello"` + `" world!"` would give us: `"Hello world!"`.

```javascript
const name = "Manav";
const numOfYears = 8;

console.log(
  "Hi, my name is, " +
    name +
    "I have been learning programming for about " +
    numOfYears +
    " years."
);
```

#### Coercion with `+` and `-`

Concatenation can be tricky when dealing with different data types such as mixing **numbers** and **strings.**

If any of the numbers have quotation marks, JS will treat them all as strings. "2" + 2 would give us... 22, because there was a "2" string.

Along the same lines, "22" - 3 = 19. In this case, using 'truly mathematical operator" will convert strings into numbers.

Whenever JS decides on its own to 'convert' the data type, this is known as implicit conversion. JS is a dynamically typed language; this means that we are free to change the type of our data whenever we please (as opposed to statically typed languages) and JS will also change data types as it sees fit.

### Interpolation with Template Literals

```javascript
const name = "Manav";
const numOfYears = 8;

console.log(
  `Hi, my name is ${name}. I have been learning programming for about ${numOfYears} years.`
);
```

Don't do **string concatenation** with `+`! Use **template literals** instead. They are easier to read and write.

## Assignments and Comparisons

[Video](https://somup.com/cZenqCpHj4)

- We only want to use **strict equality** (`===`) in our JavaScript.
- ⚠️ Don't confuse `==` with `===`! `==` is not strict equality. The linter will catch this for you.
- ⚠️ Understand the difference between the **assignment operator** (`=`) and the **equality operator** (`===`). The former is used to assign a value to a variable with `const`. The latter is used to compare two values.

## Logical Operators

We know how to create **boolean expressions**. We know how to use **comparison operators**. Now, we can use **logical operators** to combine these expressions.

### Logical AND (`&&`)

The logical AND operator (`&&`) returns `true` if both operands are `true`. Otherwise, it returns `false`.

```javascript
// We can go for ice cream if it's sunny and warm
const isSunny = true;
const isWarm = true;

const canGoForIceCream = isSunny && isWarm; // true
```

`**` is a **binary operator.** It requires two operands. It reads from left to right.

If the first operand is `false`, the second operand is not even evaluated. This is called **logical 'AND' short-circuiting**.

If the first operand is `true`, the second operand is evaluated. If the second operand is `true`, the entire expression is `true`. If the second operand is `false`, the entire expression is `false`.

### Logical OR (`||`)

The logical OR operator (`||`) returns `true` if at least one of the operands is `true`. Otherwise, it returns `false`.

```javascript
// We can go for ice cream if it's sunny or warm
const isSunny = true;
const isWarm = false;

const canGoForIceCream = isSunny || isWarm; // true
```

`||` is a **binary operator.** It requires two operands. It reads from left to right.

If the first operand is `true`, the second operand is not even evaluated. This is called **'logical OR' short-circuiting**.

If the first operand is `false`, the second operand is evaluated. If the second operand is `true`, the entire expression is `true`. If the second operand is `false`, the entire expression is `false`.

### Logical NOT (`!`)

The logical NOT operator (`!`) returns `true` if the operand is `false`. It returns `false` if the operand is `true`.

```javascript
// We can go for ice cream if it's not raining
const isRaining = false;

const canGoForIceCream = !isRaining; // true
```

`!` is a **unary operator.** It requires one operand. It reads from right to left.

## Homework Due for Tuesday (20 points)

Although we just mostly reviewed things that we have already done, we did add more examples and explanation. How do you feel about it now? Review, reflect share you 🎶 and thoughts in yet another well formatted MD document.

I also want you to share a few examples of your own. You can use the examples from the video or create your own. Just make sure to use the following:

- **Strings**
- **Numbers**
- **Booleans**
- **Variables** (`const`, `let`)
- **Operators** (`+`, `-`, `*`, `/`, `%`, `===`, `&&`, `||`, `!`)
- **Template Literals**

You can just add some [fenced code blocks/snippets](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/creating-and-highlighting-code-blocks#fenced-code-blocks) directly in your MD file.

**Make sure** that your MD is properly annotated so that it renders properly. I will certainly take off points at this point in the course if you are not paying attention to details in your MarkDown!

You can view this file in 'Raw' mode and copy some of this structure if you want.

---

## Homework Due For Thursday (10 points)

Finish reading the rest of Chapter 1 in _Eloquent JavaScript_ and share your thoughts in a well formatted MD document.

---

## Refactor ♻️ Your HTML-CSS Project with Tailwind CSS

### Strip Out All Styles from the HTML-CSS Project

You'll reference the HTML-CSS project repo that you created a couple of weeks ago.

In the [video], you see me strip...er...strip out the styles from the HTML-CSS project. This includes StyleLint and Modern Normalize 🔥.

As a reference, your `package.json` should look similar to this after following the video:

```json
{
  "name": "html-css-template",
  "private": true,
  "version": "0.0.0",
  "type": "module",
  "scripts": {
    "dev": "vite",
    "build": "vite build",
    "preview": "vite preview"
  },
  "devDependencies": {
    "vite": "^5.0.8"
  }
}
```

Just be very aware of not messing up the JSON regarding the commas and brackets. It's easy to do!

**Add, commit, and push your changes to GitHub.**

### Additional Updates

Replace the contents of `.gitignore` with just this: `node_modules`. All of the other stuff is not necessary for our purposes.

You can do a `git add .gitignore` and `git commit -m "Update .gitignore"`.

---

You can also get rid of the Stylelint VS Code extension in `.vscode/extensions.json` and replace it with the Tailwind CSS extension. Here's a diff of what that would look like:

```diff
diff --git a/.vscode/extensions.json b/.vscode/extensions.json
index 04ad6f9..a998402 100644
--- a/.vscode/extensions.json
+++ b/.vscode/extensions.json
@@ -1,8 +1,8 @@
 {
   "recommendations": [
+    "bradlc.vscode-tailwindcss",
     "esbenp.prettier-vscode",
     "htmlhint.vscode-htmlhint",
-    "stylelint.vscode-stylelint",
     "usernamehw.errorlens",
     "vsls-contrib.codetour"
   ]
```

### Install Tailwind CSS

[Video](https://somup.com/cZn6hYpo0T)

We [install Tailwind via Vite.](https://tailwindcss.com/docs/guides/vite)

### Improving our Developer Experience with Tailwind CSS

[Video](https://somup.com/cZn6hxpo0B)

We install [Tailwind's Prettier plugin.](https://github.com/tailwindlabs/prettier-plugin-tailwindcss)

### Homework Due For Saturday (10 points)

You already know...👀. Rework your HTML-CSS using 💯 Tailwind classes only.

Of course, we are limiting ourselves to [the default color palette](https://tailwindcss.com/docs/customizing-colors#default-color-palette). It is definitely possibly to fully customize Tailwind, but not necessary for our purposes. Just stick with what's available unless you really want to explore more.

If you used some type of background images in your original you have to do some additional Tailwind customizations. An easy way to do this is to just use [arbitrary values](https://tailwindcss.com/docs/background-image#arbitrary-values). Or, just don't worry about the the background images! Replace with a nice gradient

As always, please keep a good commit history. Do an `add` and `commit` after each logical unit or work or task that you completed. You can do that directly from VS Code as you have seen in the videos. Or, from the terminal.

**DON'T FORGET TO PUSH YOUR WORK TO GITHUB!**

Once you have done that, you can DM me in Teams and I can access your work directly via GitHub Classroom. Or, even better, just shoot me that link to your repo once again.

One last thing - if possible create a submission on BrightSpace. That means you can just upload a screenshot of your work or whatever. This makes it easier for me to enter the score! Yeah, it's silly 🙃 🤦🏾‍♀️.

## Tailwind Refactor ♻️ Example

**This section is optional.** I just wanted to show you how I did it for the example that I created in the video.

1. [Header](https://somup.com/cZnZ0Lpzxi)
1. [Main Section](https://somup.com/cZnTchpzx0)
1. [Form](https://somup.com/cZnTcDpzxa)
1. [Additional Styles](https://somup.com/cZnTc0pzxm)

For the mobile view I ended up doing this for better spacing/margins throughout:

```diff
diff --git a/index.html b/index.html
index 51138df..8572806 100644
--- a/index.html
+++ b/index.html
@@ -7,9 +7,9 @@
     <title>Manav Misra</title>
     <link rel="stylesheet" href="./style.css" />
   </head>
-  <body class="bg-slate-900 tracking-wide text-white *:p-8">
+  <body class="bg-slate-900 tracking-wide text-white">
     <header
-      class="flex items-center justify-center gap-x-4 bg-white text-slate-900"
+      class="flex items-center justify-center gap-x-4 bg-white p-8 text-slate-900"
     >
       <img
         src="./images/me.jpg"
@@ -24,8 +24,8 @@
       </div>
     </header>

-    <main>
-      <section class="px-0 *:mb-4">
+    <main class="py-4">
+      <section class="*:mb-4 *:px-8">
         <h2 class="text-2xl font-medium underline underline-offset-2">
           About Me
         </h2>
@@ -60,7 +60,9 @@
         </ul>
       </section>

-      <form class="flex flex-col gap-y-4 [&>input]:rounded [&>label]:sr-only">
+      <form
+        class="flex flex-col gap-y-4 px-8 py-4 [&>input]:min-h-12 [&>input]:rounded [&>label]:sr-only"
+      >
         <label for="name">Name</label>
         <input type="text" id="name" placeholder="Your Name" />

@@ -79,7 +81,7 @@
       </form>
     </main>

-    <footer class="divide-x border-t-2 border-white pt-4">
+    <footer class="divide-x border-t-2 border-white p-8">
       <a href="https://github.com/manavm1990" class="pr-2">GitHub</a>
       <a href="https://www.linkedin.com/in/manavm1990/" class="pl-3"
         >LinkedIn</a
```

Here's how that looks:

1. [Mobile View](https://somup.com/cZnTcvpzxS)

---

[Tailwind Finale](https://somup.com/cZenrDpHXA)
