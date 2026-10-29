# AEA SENIORS

### A guide to Git & GitHub for our class

This page explains **how GitHub works** and what all those strange words mean: *push, pull, clone, fork, branch, pull request*... By the end, they will sound like normal words.

You don't need to memorize anything. Read it once, come back whenever you get confused. In each lesson, your teacher will tell you **exactly** what to do, so this guide is just the map. 

---

##  Table of Contents

1. [The Problem We Are Solving](#-the-problem-we-are-solving)
2. [Git vs. GitHub](#-git-vs-github)
3. [The Dictionary](#-the-dictionary)
4. [🌿 Branches: Parallel Universes for Your Code](#-branches-parallel-universes-for-your-code)
5. [The Journey of Your Code](#-the-journey-of-your-code)
6. [Clone vs. Fork vs. Branch](#-clone-vs-fork-vs-branch)
7. [Pull Requests: The Polite Knock](#-pull-requests-the-polite-knock)
8. [Merge Conflicts: Don't Panic](#-merge-conflicts-dont-panic)
9. [The Spellbook](#-the-spellbook-quick-reference)
10. [Golden Rules for Our Class](#-golden-rules-for-our-class)
11. [Mini FAQ](#-mini-faq)

---

##  The Problem We Are Solving

Imagine **20 people writing one story together**, each on their own computer.

- Who has the latest version?
- What if someone deletes a chapter by accident?
- What if two people change the same page at the same time?
- How do you go back to *yesterday's* version?

Without a system, this is chaos. With Git and GitHub, it becomes calm, organized, and even a little bit magical.

---

##  Git vs. GitHub

People mix these two up all the time. They are **different things**:

| | What it is | Where it lives | Analogy |
|---|---|---|---|
| **Git** | A tool that tracks every change in your files | On your computer | 📷 A camera that takes snapshots of your work |
| **GitHub** | A website that stores your Git projects online | On the internet | ☁️ A cloud photo album where you share the snapshots |

**Git** works even without internet. **GitHub** is where everyone meets, shares, and collaborates.

---

##  The Dictionary

Here are the most important words, in plain English:

| Word | Meaning | Think of it as... |
|---|---|---|
| **Repository** (repo) | A project folder that Git is watching, with its whole history | 🏛️ A library of your project |
| **Commit** | A saved snapshot of your work, with a short message | 💾 A save point in a video game |
| **Branch** | A separate line of work, safe from everyone else's changes | 🌌 A parallel universe |
| **main** | The "official" branch of the project | 👑 The main timeline |
| **Clone** | Download a full copy of a repo to your computer | 📥 Photocopying the entire library |
| **Push** | Send your commits from your computer to GitHub | 🚀 Uploading your save points |
| **Pull** | Bring new changes from GitHub to your computer | 🧲 Downloading what others did |
| **Fork** | Make your own copy of someone else's repo, on GitHub | 🍴 Taking a recipe and making it yours |
| **Pull Request** (PR) | A request that says "please add my changes to the project" | 🚪 A polite knock on the door |
| **Merge** | Combine the changes from one branch into another | 🧬 Joining two timelines into one |
| **Conflict** | Two people changed the same line, and Git needs a human to decide | ⚔️ Two people grabbing the same pencil |

---

## 🌿 Branches: Parallel Universes for Your Code

This is the **most important idea** in this guide. Take your time here.

### What is a branch?

A **branch** is a separate copy of the project where you can **make changes freely**, without touching anybody else's work.

Think of a movie multiverse: there is one **main timeline**, and heroes can jump into **parallel universes** to try risky things. If something explodes in the parallel universe, the main timeline is still safe.

That's exactly what a branch is.

### What does it look like?

Every dot is a **commit** (a save point):

```
main:      ●───●───●───────────●───●
                    \         /
my-branch:           ●───●───●
```

1. The project starts on **main**.
2. At the third dot, you create **my-branch**. A new universe is born. 🌱
3. You make your own commits there (the three dots below).
4. When your work is ready, it can be **merged** back into main.

While you are working in your branch, **main does not change**, and nobody else's branch changes either.

### Why do branches exist?

-  **Safety:** you can experiment and break things without breaking the project.
-  **Teamwork:** 20 people can work at the same time without stepping on each other's toes.
-  **Clarity:** it's easy to see who did what, and when.
-  **Organization:** one branch per task, per person, or per idea.

### Branches in our class

In our class, **every student has their own branch, named after their nickname**. 🦊

That means:

- Your branch is **your personal universe**. Everything you create goes there.
- Your classmates have their own universes. You will **never** overwrite their work, and they won't overwrite yours.
- Your teacher can look at your branch and see **your exercises and your history**.

Your computer is already prepared, and your lessons will tell you what to do. All you have to remember is: **I work in MY branch.**

### The life of a branch

```
1.  Create the branch      →  a new universe is born
2.   Work and commit        →  create things, take snapshots
3.  Push the branch        →  upload your universe to GitHub
4.  Pull Request (optional) →  ask to join main
5.  Merge                   →  your changes become part of the main timeline
```

### Quick branch facts

- Creating a branch is **fast and free**. Make as many as you want.
- A branch is **not a full copy** of the files; Git is clever about it.
- You can **switch** between branches, and your files change to match each universe.
- Good branch names are short and clear: `fox-exercises`, `fix-login-bug`, `add-menu`.

---

##  The Journey of Your Code

Imagine you are **shipping a package** to the cloud. Your code goes through four stops:

```
📝 Your files   →   📦 add   →   🏷️ commit   →   🚀 push   →   ☁️ GitHub
 (you edit)        (put it       (seal and        (send it
                    in the box)   label the box)   to the cloud)
```

1. **You edit files.** You write code, create things, fix things.
2. **`add`:** you choose *which* changes go into the box (the "staging area").
3. **`commit`:** you seal the box and write a label: *"Added the homepage title"*. This is your save point. It's saved **on your computer only**.
4. **`push`:** you ship the box to GitHub. Now it's online and your teacher can see it. ☁️

> 💡 **Important:** a commit is **not** on GitHub until you push. Commit = saved on your computer. Push = saved online.

And in the other direction:

- **`pull`** = bring new things from GitHub to your computer. 🧲
- **`clone`** = download a repository for the very first time. 📥

### How to write a good commit message

Your message is the label on the box. Future you will be grateful. 🙏

| 👎 Bad | 👍 Good |
|---|---|
| `stuff` | `Add navigation menu` |
| `fix` | `Fix button color on the home page` |
| `asdfgh` | `Finish exercise 3` |
| `final final REAL` | `Update README with project description` |

---

## 🥊 Clone vs. Fork vs. Branch

These three are **very** often confused. Here's the difference:

| | Where does the copy go? | Whose is it? | When do you use it? |
|---|---|---|---|
| **Clone** | To **your computer** | It's still linked to the original repo | To start working on a project |
| **Fork** | To **your GitHub account** | It becomes **your own** repo | To contribute to a project you don't own (very common in open source) |
| **Branch** | **Inside the same repo** | Same repo, separate line of work | To work on something without disturbing others |

A simple way to remember it:

- 📥 **Clone** = "I want this on my computer."
- 🍴 **Fork** = "I want my own copy on GitHub."
- 🌿 **Branch** = "I want my own space inside this project."

> 🏫 In our class we mostly use **clones and branches**. Forks are what you'll use later, when you contribute to real open-source projects around the world. 🌍

---

## 🚪 Pull Requests: The Polite Knock

A **Pull Request** (or **PR**) is how you say:

> *"Hello! I made some changes in my branch. Could you please take a look and add them to the project?"*

Here's how it works:

1. You finish your work in your branch and push it.
2. On GitHub, you open a **Pull Request**.
3. Other people can **read your changes**, leave **comments**, and suggest improvements. 💬
4. When everyone is happy, the PR is **merged**, and your work joins the main timeline. 🎉

Why do PRs exist? Because in real teams, nobody changes `main` directly. Code is **reviewed** first, like a teacher reading your essay before it's published. This catches mistakes and helps everyone learn.

Great PRs have:

- ✅ A clear title (*"Add contact form"*)
- ✅ A short description of what you changed and why
- ✅ Small, focused changes (easier to review!)

---

## ⚔️ Merge Conflicts: Don't Panic

Sometimes two people change **the same line of the same file**. When Git tries to combine them, it says:

> *"I don't know which one is right. Human, please decide!"* 🤷

This is called a **merge conflict**, and it happens to **everybody**, even to developers with 20 years of experience.

It looks like this inside the file:

```
<<<<<<< HEAD
Title: My Amazing Page
=======
Title: My Awesome Website
>>>>>>> other-branch
```

To solve it, you choose which version to keep (or mix them), delete the strange `<<<<<<<`, `=======` and `>>>>>>>` lines, save the file, and commit.

**The best way to avoid conflicts?** Work in your own branch (like we do in class), commit often, and pull regularly. 😉

---

## 🪄 The Spellbook (Quick Reference)

Every wizard has a spellbook. You don't need to memorize these. **Your lessons will always tell you what to run.**

| Spell (command) | What it does |
|---|---|
| `git clone <url>` | 📥 Downloads a repository to your computer |
| `git status` | 👀 Shows what changed and what is ready to commit |
| `git add <file>` | 📦 Puts a changed file into the box |
| `git add .` | 📦 Puts **all** changes into the box |
| `git commit -m "message"` | 🏷️ Seals the box with a label (save point!) |
| `git push` | 🚀 Sends your commits to GitHub |
| `git pull` | 🧲 Brings new changes from GitHub |
| `git branch` | 🌿 Lists your branches |
| `git switch <name>` | 🌌 Jumps to another branch |
| `git log` | 📜 Shows the history of commits |

> 🧠 **Tip:** when in doubt, run `git status`. It's like asking Git *"What's going on?"* and it always answers kindly.

---

## 🏅 Golden Rules for Our Class

1. 🦊 **Use only your nickname.** Never your real name, in your branch, your files, or your messages.
2. 🌌 **Work only in your own branch.** Other branches belong to your classmates.
3. 🚫 **Never delete or overwrite someone else's work.** Not by accident, not as a joke.
4. 💾 **Commit small and often.** Many little save points are better than one giant one.
5. 🏷️ **Write clear commit messages.** Say what you did.
6. 🔒 **Never put passwords, personal data, or private information in your files.** Everything you push is saved in the history.
7. 🙋 **Ask for help!** Errors are normal. Every developer sees red error messages every single day.

---

## ❓ Mini FAQ

**Can I break the project?**
Very hard! Your work lives in your own branch, and Git keeps the history of everything. Almost anything can be undone.

**I made a mistake in my last commit. Is it over?**
Not at all. Tell your teacher. Mistakes in Git are fixable, and it's a great way to learn.

**What's the difference between "commit" and "push"?**
Commit = save point on **your computer**. Push = upload to **GitHub**. You need both.

**Why can't I see my classmate's files in my branch?**
Because each branch is its own universe. That's the whole point! 🌌

**Do I need to memorize all the commands?**
No! Even professionals look them up all the time. Understanding the *ideas* matters much more than memorizing the words.

---

## 🚀 Ready?

You now know more about Git and GitHub than most people on the planet. Seriously! 🌍

Remember the big picture:

> 🌿 You work in **your branch** → 💾 you make **commits** → 🚀 you **push** to GitHub → 👩‍🏫 your teacher sees your progress.

See you in class. Happy coding! 💻✨
