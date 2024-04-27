# Week 1️⃣4️⃣

**Be sure that you are doing proper commits.** Grading will be stern at this point in the course!

## Importing ESMs

Last week, we created some **named** exports in our JavaScript files. This week, we will learn how to import these exports into other files using the `import` statement.

[Video](https://go.screenpal.com/watch/cZfYDDVMeRC)

## `filter`

The `filter` method is used to create a new array from an existing array. It takes a callback function as an argument and returns a new array containing only the elements that return `true` when the callback function is called.

1. [`filter` Overview](https://go.screenpal.com/watch/cZfYDZVMeSq)
1. [Filtering `BELTS`](https://go.screenpal.com/watch/cZfYDuVMeSA)

## Homework Due Thursday I

You already know...Remove `"Vacant Title"`.

No video is necessary. Just do it and write a proper commit. I should be able to clearly 🆔 this commit and go straight to it to see the work. If it's troublesome for me to find it......🙅🏾‍♂️.

You should also write a relatively short Gist comparing and contrasting the contents of the video with whatever you may have already known/understood about `filter`.

## Homework Due Thursday II

Over the course of implementing some of the original tasks in the exercise, it became clear that this was simply going to be too much for an entry-level exercise.

So, I decided to make [a crazy video](https://youtu.be/18Nx8L_Uw5M) that covers all kinds of topics, much beyond anything that we set out to do. It's a whirlwind that covers a lot of relevant, but perhaps advanced topics. I'm not expecting you to understand everything in the video.

However, all you have to do is watch and learn. The [code shown in the video is even included for you.](https://github.com/SWIC-177/wwe/commits/main/) On GitHub, you may need to click the 'sync code' to...sync up with your repo. Then, you'll do a `git pull` to get the latest changes on your local machine.

If you get stuck on this process, [post a question](https://github.com/SWIC-177/wwe/discussions/categories/q-a).

There are 2️⃣ parts to this submission:

1. **Reflections Gist**: This is an MD file, as usual. The quality and level of detail in your Gist should adequately convey that you did at least watch the video and you're able to formulate some thoughts and feedback on it. I cover a lot of ground in the video, so there should be plenty to write about.
1. Now that you have the codes, you are in a position to use it to:
   1. Filter out the `Tag Team Champions` from the `BELTS` array.
   1. Also, remove the corresponding indices from the `CHAMPIONS` array.

To accomplish this, you will work in your `main.js` file and do: `import { removeCorrespondingItemsByTerm } from "./src/lib";`

~~All you have to do then is to call the function with the proper arguments and just log the results to the console. Make a 'proper' commit and push it up.

## Homework Due ~~Saturday~~ Next Tuesday

### Update/Edit

**UPDATED:** I have removed 🔥 the task regarding sorting. Once again, I overestimated the difficulty. Instead, I walk you through the sort task [in this Q&A video](https://around.co/playback/ff124133-420b-48e4-a38a-aabcbfab4917?sharedKey=7f4e3e6a-94d4-4581-9c69-5b05178719dc).

In this video, we review some parts of VS Code and we fix an issue with the tooling 🧰. We also review ESM, `filter` and just various other JS topics.

Unlike the 'crazy 🤡' video previously, most of this is relevant.

**NOTE:** We didn't fully solve the problem. Expect an update soon regarding that.

1. See if you can devise a test to prove that it passes. I will grade lightly on this part. BTW, CoPilot is excellent at writing tests for you. Just ask it to do so. You may need to do: `npm i -D vitest` and add a script to your `package.json` to run the tests.

---

**5 Points Extra Credit (Due Saturday):** The last task listed:

Create a new ARRAY of objects called `CHAMPIONSHIPS` that contains the following properties:

- `title` - The name of the title.
- `champion` - The name of the champion.

--

**🚨 All work subject to code quality standards and proper commits.**

--

Use [Q&A](https://github.com/SWIC-177/wwe/discussions/categories/q-a).
