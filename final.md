# Final Exam - 50 points

This final exam consists of two parts. It is due in it's entirety by Wednesday. If you finish the two parts ahead of time, you can move to the Extra Credit section, which is worth up to 10 additional points.

As a general reminder for both parts, recall that to get the benefits of VS Code extensions tooling that leverages our `settings.json`, the app must be opened directly from the root of the project, and not, for example, from some parent directory, such as `Desktop` or `Documents` or `Code`.

And, if prompted to install recommended extensions, do so. If you don't have ESLint and Prettier installed, you will not get the benefits of the linting and formatting tools. JS is difficult enough without having to worry about syntax errors and formatting issues.

Hopefully, all of the above is old hat by now.

## Part 1: Code Analysis and Review - 30 points

You may review [this app.](https://inquisitive-crisp-0ebb90.netlify.app/)

Afterwards, [use this starter code link if you are in Section 1](https://classroom.github.com/a/zDaSPl0b). If you are in Section 2, [use this starter code link.](https://classroom.github.com/a/wbHlJyPI)

Clicking the link will fork a repo to your GitHub account. Clone the repo to your local machine, run `npm i` to install the dependencies and open up in VS Code with `code .`. Again, if prompted to install recommended extensions, do so. You can then run it with `npm run dev` like for your other `wwe`.

Now, for the task at hand, just look in the `README`. Summarily, you are not doing any actual coding, aside from breaking and fixing things to help your own understanding of the code. Instead, you are adding heavy comments and updating the `README` with your findings, including a **personal reflection.**

You **do not** need to concern yourselves with `lib` files. Just take those as is and focus on how they are being applied.

Your reflections should especially focus on the **function components,** (`components`), **state** (managed in a separate class), **props** (the function component parameters) and the render function. All of these are tenets of React and even other frameworks.

We have not explicitly covered these topics, but a majority of the code that is provided all builds upon and uses Js fundamentals that we have covered.

Learning to code involves applying what you already know in new and unfamiliar contexts.

One strategy that you might want to use is to systematically step through [the commit history.](https://github.com/SWIC-177/wwe/commits/main/) You would want to start after [this bulk commit](https://github.com/SWIC-177/wwe/commit/41e0a8992a0d370e4cfc7e7ce418220fb296a7c3). Of course, you can reference these same commits on your own fork of this repo.

This is open-ended. Add as much or as little content is necessary to clearly convey your understanding of the provided codebase. Leverage AI 🤖 (CoPilot and/or Claude) but understand that it's a tool. It's not a replacement for your own genuine understanding and your own personal reflections on these topics.

You can even discuss with your peers, but the work you submit should be your own. And, if you do discuss with your peers, be sure to give credit where credit is due.

### Vanilla Code Review Deliverables

1. A heavily commented codebase. A single commit would be fine in this case, but **make sure that it's a properly written commit message.** I will see this in GitHub Classroom anyway, but it's still helpful to drop the direct link in BrightSpace under 'Final Exam.'
1. A well written `README` that includes your reflections on the codebase. Well-written means that it shows your knowledge of using MarkDown. It includes proper paragraph breaks and headings and is free of spelling and grammatical errors. Don't cut corners on this one. It should at least be as long as this prompt, if not longer. If you submit a plain wall of text, you will not get full credit. The document you are reading now is well-formatted. Emulate this.

You don't need to commit any actual code changes, unless you happen to find a bug or you want to try adding another feature. If it's something worthwhile, you might get a bonus point or two.

## Part 2: React

This part will be mostly a code-along, with the goal of giving a 'free sample' of what React is like.

As the code is provided for you via the videos, any additional insights by way of comments and/or reflections are welcome. Your job is to communicate and reflect on what you have learned, more than just blindly copying code. To this end, you are advised to keep some ongoing notes/thoughts as you watch the videos. You will use these notes to write your reflections.

Your reflections should be personalized and show your own unique understanding of the material. They should not be just a rehash of the video content. Include your own thoughts and insights. Perhaps some analogies or metaphors that help you understand the material. Or, maybe some real-world examples of how you might use this in a project.

1. [React Motivations](https://somup.com/cZhloV5T7I) - One thing I could have mentioned is how terrible Teams is at re-rendering its UI in response to changes in state! :)
1. [React Docs 📝](https://somup.com/cZhloY5T7p) - You are strongly encouraged to play with the docs and their examples as time allows. Any additional concepts that you glean from here may be included in your reflections document for up to 5 additional bonus points. Please cite specifically anything that took the time to read in the React docs so I can give bonus points as appropriate.

### Code-Along

To proceed, if you are in Section 1, [use this starter code link.](https://classroom.github.com/a/WEKoxGKf). If you are in Section 2, [use this starter code link.](https://classroom.github.com/a/kWRywQC4).

As usual, you are responsible for cloning the repo, installing the dependencies, and opening it in VS Code. You can then run it with `npm run dev`.

You also need to commit early and commit often. I don't show that in the videos, but that too should be part of your workflow at this point. **Quality commit messages are a must.** Either use the traditional commit messages with the imperative mood, or use [conventional commits.](https://marketplace.visualstudio.com/items?itemName=vivaxy.vscode-conventional-commits) I will be looking for this in your repos.

1. [Code Overview](https://somup.com/cZhloE5Tsr)

#### JSX

We use JSX to mix JS with HTML. This is an alternative to using template literals in vanilla JS. Instead, we are using this templating language provided by React.

We start by creating a `components` directory inside of `src`. This is where we will store our additional React components.

[First Component](https://go.screenpal.com/watch/cZhloMVLiOO)

One other thing you may have noticed is that we have to say `className` instead of `class` in JSX. This is because `class` is a reserved word in JS.

Similarly, in a `label` tag, we have to use `htmlFor` instead of `for`.

#### Props

Props are the way that we pass data from parent to child components. They are read-only and immutable. They are passed as attributes in JSX.

[Props](https://go.screenpal.com/watch/cZhlDjVLitt)

We don't yet have an 'state' in our app. It's just hard-coded stuff that we are passing down as props.

#### Render the Belts and Champions Data

[Render the Belts and Champions Data](https://go.screenpal.com/watch/cZhlDuVLium)

### React Deliverables

1. As indicated, you should have followed along with the code-along and committed your changes as you went. You should have a series of commits that show your progress through the videos. This should be in Classroom already, so I can find it, but it's nice to get the direct link in BrightSpace.
1. A reflections document that especially the videos before the actual 'code-along.' Again, this should be a well-formatted MD document. You can keep this in the `README`.

---

## Extra Credit - 10 points

1. [Render the Search Component](https://somup.com/cZhlD55TMS)

### `use state`

React is, among other things, a state management library. We can use the `useState` hook to manage state in our components.

1. [use-state](https://somup.com/cZhlD75TLX)
1. [using `searchTerm`](https://somup.com/cZhlDR5TL3)

### Synthetic Events

React wraps the native DOM events in its own synthetic events. This is to ensure that the events work the same way across all browsers.

1. [`onInput`](https://somup.com/cZhlbj5TL4)
1. [Fin](https://somup.com/cZhlbo5TLC)

### Extra Credit Deliverables

Just note that you did the extra credit BrightSpace and I will look for well-written commit messages in the repo!
