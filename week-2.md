# Week 2️⃣

1. [Week 1️⃣ Recap](https://somup.com/cZVYbmkmf1)

## Terminal Basics

[Video](https://somup.com/cZVYFjkmfH)

### 🔑 Points

1. The terminal in conjunction with a 🐚 program is an alternative to a GUI.
1. The terminal is a text-based interface to your computer.
1. The terminal is a program that runs other text-based programs.
1. Type `pwd` to see where you are in your computer's file system.
1. Type `ls` to see what files and folders are in your current directory.
1. Type `cd` to change directories. `cd` by itself will take you to your home 🏠 directory.

### Breaking Down `cd Code`

[Video](https://somup.com/cZVYFFkmhi)

1. `cd` is a 🐚 **command** that takes an argument.
1. We use a space as a **delimiter** that separates the program from its argument.
1. `Code` is the **argument** to `cd`.

## Authenticating with GitHub CLI

**You may want to set up Chrome or FF as your default browser** for this part for consistency. You can always change it back later, if desired.

Login to GitHub in your browser and then...

As per last week you should have already installed GitHub CLI. That's `gh`.

At this time you'll want to do `gh auth login` and follow the prompts.

Choose: `> GitHub.com`. Select `> HTTPS`.

Enter 'Y' and press 'enter' for: `Authenticate Git with your GitHub credentials? (Y/n)`

Select: `Login with a web browser`.

You'll want to authenticate with GitHub.com. You'll need to paste a code into the browser. It says: `! First copy your one-time code: <code>`. Copy that code and paste it into the browser as instructed.

Basically, just follow the prompts and choose the default options.

## Git/GitHub Cloning

[Video](https://somup.com/cZVYFykmhB)

1. Git is a version control system.
1. GitHub is a website that hosts Git repositories.
1. Git is a program that runs in the terminal.
1. `clone` is a Git command that **clones** a **remote repository** (i.e. a repository on GitHub) to your local machine.

## Hidden Files and Directories 📁

[Video](https://somup.com/cZVYFmkm1i)

1. Hidden files and directories are prefixed with a `.`.
1. `ls` by itself will not show hidden files and directories.
1. `ls -a` will show hidden files and directories. The `-a` is a **flag** that modifies the behavior of `ls` such that it shows **all** files and directories (including hidden 🙈 ones).

## Open Up VS Code from the Terminal

[Video](https://somup.com/cZVYF9km1g)

1. `code .` will open up VS Code in your current directory.
1. Once inside of VS Code, try 'command + shift + p'. This will open up the command palette. Type 'shell' and you will see a command called 'Shell Command: Install 'code' command in PATH'. Select it and press 'enter'. This will allow you to open up VS Code from the terminal by typing `code .`, if it didn't work for you before.

### Special Instructions for Windows Users

[Video](https://somup.com/cZVYF8km1f)

We want our line endings to be consistent with Unix. This is important for cross-platform compatibility. You can read more about it [here](https://docs.github.com/en/github/using-git/configuring-git-to-handle-line-endings).

## Git Commands

[Video](https://somup.com/cZVYqXkmin)

1. `git status` will show you the current state of your repository.
1. `git add .` will add all of your changes to the staging area. Or, just `git add` followed by the name of the file you want to add.
1. `git commit -m "message"` will commit your changes to your local repository. The `-m` is a flag that allows you to add a message to your commit.

### Git Commit Messages

[Video](https://somup.com/cZVYqqkmiY)

1. Commit messages should be in the imperative mood.
1. Commit messages should be short and sweet.
1. Commit messages should be descriptive.

**Example:** `git commit -m "Add git commands video"`

☝️ This is a good commit message because it is short, descriptive, and in the imperative mood. It capitalizes the first word and does not end with a period.

### Logging and Pushing

**Note:** Whenever you do `git log`, on Mac/Linux you will need to press 'q' to exit the log.

[Video](https://screenpal.com/watch/cZVYqpVJtXD)

1. `git log` will show you the commit history of your repository.
1. `git push` will push your changes to the remote repository (i.e. GitHub).

### Review and GitHub Features

[Video](https://somup.com/cZVYqPkmjO)

## Homework Due Saturday by 11:59pm

### Terminal and Git/GitHub

For the BrightSpace submission, you would share the screenshot files (or a video) and a link to your GitHub repository 👇🏾.

1. Post a screenshot(s) of your terminal `history`. Highlight the commands that you ran for this week's homework. You can use the `history` command to see your terminal history. You can also use the up and down arrows to cycle through your history. You can also use the `history` command with a `grep` to search for a specific command. For example: `history | grep "cd Code"`.
1. Continue making 2-3 changes to your repository.
1. Add a new file called `reflections.md`. As the name implies, using your MarkDown skills with proper headings, some lists, etc. reflect and summarize what you learned and what it means to you. What is the terminal? Why might we care? What is Git and GitHub? For what? Why do we care? What is the actual 🤬 meaning? How do you anticipate that this tools would help someone working as a developer?

Upon completion, you can navigate to your `Code` directory, where you cloned `throwaway` and you can remove it: `rm -rf throwaway`. This will remove the directory and all of its contents. This is optional, but it will keep your `Code` directory clean.

### HTML/CSS Podcast 🎶

1. Create your own summary 🎶 (in MarkDown, of course) letting me know about what you already knew and what you learned from [this episode](https://syntax.fm/show/158/the-fundamentals-html-css).
1. Tell me your thoughts on these [new CSS features](https://syntax.fm/show/695/5-new-css-features-you-should-know).

A video or audio recording of your summary would be nice too.

Post these in BrightSpace.

### HTML/CSS Skills Demo

❗ As you work on this, you should be committing your changes to your local repository and pushing them to your remote repository on GitHub.

You are tasked with creating a 1-2 page website that showcases your baseline HTML/CSS skills. It can just be a bio page, similar to your GitHub profile. However, you will want to add more depth and detail. You'll want to definitely add some images too.

You will also want to create a 'Contact Me' form. This can be on a separate page, or it can be all on 1️⃣ page. The form is not going to be functional of course. I just need to see that you know how to create an [HTML form](https://developer.mozilla.org/en-US/docs/Learn/Forms/How_to_structure_a_web_form) properly and that you know how to style it with CSS 💄.

Make this your own. You should include various input types including text, email, radio buttons, checkboxes, and a dropdown. You should also include a textarea. You should also include a submit button.

I'm interested in **semantic HTML.** You don't need to be a professional designer, but you should make it look as nice as you can and use a variety of CSS skills. I'm particularly interested in seeing you use **flexbox** or even **grid,** if you covered that.

Without further ado, here's [the template repo to use for IN1](https://classroom.github.com/a/Z7NbQVzl), and here's [IN2](https://classroom.github.com/a/LY6ThckU).

As this is all on GitHub and I have access to your repos via GitHub Classroom, you don't need to submit anything to BrightSpace. I will be able to see your work **as long as you push your changes to GitHub.**

---

## Bonus

For extra credit, [register for an account on CodePip](https://codepip.com/) and earn 2️⃣ points per game finished. Send me the screenshot. Max of 10 extra credit points.

You must also send me an brief explanation of the results of each game via video. Tell me about what you learned. Convince me that you didn't just jump on YouTube and 'copy' the answers. I want to see that you actually learned something.