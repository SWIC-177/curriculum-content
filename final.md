# Final Exam - 50 points

This final exam consists of two parts. It is due in it's entirety by Wednesday.

As a general reminder for both parts, recall that to get the benefits of VS Code extensions tooling that leverages our `settings.json`, the app must be opened directly from the root of the project, and not, for example, from some parent directory, such as `Desktop` or `Documents` or `Code`.

And, if prompted to install recommended extensions, do so. If you don't have ESLint and Prettier installed, you will not get the benefits of the linting and formatting tools. JS is difficult enough without having to worry about syntax errors and formatting issues.

Hopefully, all of the above is old hat by now.

## Part 1: Code Analysis and Review - 40 points

You may review [this app.](https://inquisitive-crisp-0ebb90.netlify.app/)

Afterwards, [use this starter code link](https://classroom.github.com/a/zDaSPl0b). Clicking the link will fork a repo to your GitHub account. Clone the repo to your local machine, run `npm i` to install the dependencies and open up in VS Code with `code .`. Again, if prompted to install recommended extensions, do so. You can then run it with `npm run dev` like for your other `wwe`.

Now, for the task at hand, just look in the `README`. Summarily, you are not doing any actual coding, aside from breaking and fixing things to help your own understanding of the code. Instead, you are adding heavy comments and updating the `README` with your findings, including a **personal reflection.**

You **do not** need to concern yourselves with `lib` files. Just take those as is and focus on how they are being applied.

Your reflections should especially focus on the **function components,** (`components`), **state** (managed in a separate class), **props** (the function component parameters) and the render function. All of these are tenets of React and even other frameworks.

We have not explicitly covered these topics, but a majority of the code that is provided all builds upon and uses Js fundamentals that we have covered.

Learning to code involves applying what you already know in new and unfamiliar contexts.

One strategy that you might want to use is to systematically step through [the commit history.](https://github.com/SWIC-177/wwe/commits/main/) You would want to start after [this bulk commit](https://github.com/SWIC-177/wwe/commit/41e0a8992a0d370e4cfc7e7ce418220fb296a7c3). Of course, you can reference these same commits on your own fork of this repo.

This is open-ended. Add as much or as little content is necessary to clearly convey your understanding of the provided codebase. Leverage AI 🤖 (CoPilot and/or Claude) but understand that it's a tool. It's not a replacement for your own genuine understanding and your own personal reflections on these topics.

You can even discuss with your peers, but the work you submit should be your own. And, if you do discuss with your peers, be sure to give credit where credit is due.

### Deliverables

1. A heavily commented codebase. A single commit would be fine in this case, but **make sure that it's a properly written commit message.** I will see this in GitHub Classroom anyway, but it's still helpful to drop the direct link in BrightSpace under 'Final Exam.'
1. A well written `README` that includes your reflections on the codebase. Well-written means that it shows your knowledge of using MarkDown. It includes proper paragraph breaks and headings and is free of spelling and grammatical errors. Don't cut corners on this one. It should at least be as long as this prompt, if not longer. If you submit a plain wall of text, you will not get full credit. The document you are reading now is well-formatted. Emulate this.

You don't need to commit any actual code changes, unless you happen to find a bug or you want to try adding another feature. If it's something worthwhile, you might get a bonus point or two.
