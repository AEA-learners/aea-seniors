# Exercise 1: Getting to know GitHub and VS Code

 **Goal:** create your first web page and send it to GitHub from your own branch.

>  **Tip:** you are reading this file in VS Code. Press **Ctrl + Shift + V** to see it in a nicer, formatted view.

---

## What you will learn

- What a `.bat` file is (and how to use it safely)
- How to open a project folder in VS Code
- How to use the VS Code terminal
- How to create an HTML file and a CSS file
- How to do your first **add → commit → push**

---

##  Before you start: the rules

1. Use **only your nickname**. Never your real name.
2. Work **only in your own branch**.
3. Do not write passwords or personal information in your files.
4. If something looks strange, **stop and ask your teacher**.

---

## Part 1: What is a `.bat` file?

You will use two special files today: **`start-class.bat`** and **`end-class.bat`**.

A `.bat` file is a **list of commands saved in a file**. When you double-click it, the computer runs all the commands for you, one after another. Think of it as a **shortcut that presses many buttons at once** 🎛️.

When you run one, a **black window** opens. This is normal! You will type some words in it, and it will show messages. Do **not** close the window until you see "Press any key to continue".

| File | What it does for you |
|---|---|
| `start-class.bat` | Asks for your nickname, then creates (or opens) **your own branch** |
| `end-class.bat` | Sends your work to GitHub and cleans the computer for the next student |

These files were made by your teacher. They are safe. 😊

> 🔒 Please **do not edit, move, or delete** these files. Other students need them too.

---

## Part 2: Start your class

1. Open **File Explorer** and go to the folder **`C:\Turma`**. Find **`start-class.bat`** and **double-click** it.
2. When it asks for your nickname, type it and press **Enter**.
   - Use only **lowercase letters, numbers, and hyphens** (example: `blue-fox`).
   - **No spaces. No real names.**
3. It will ask if your nickname is correct. Type **Y** and press **Enter**.
4. Wait until you see the final message. Then press any key to close the window.

✅ **Done!** You now have your own universe (your branch). 🌌

---

## Part 3: Open the project in VS Code

1. Open **Visual Studio Code**.
2. Click **File → Open Folder...**
3. Choose the folder **`C:\Turma\aea-seniors`** and click **Select Folder**.
4. If VS Code asks *"Do you trust the authors?"*, click **Yes, I trust the authors**.

On the left side you will see the project files. This is the **Explorer**.

### Open the terminal

Click **Terminal → New Terminal** (or press **Ctrl + `**).

A panel opens at the bottom. This is the **terminal**: a place where you type commands. It is already inside your project folder. 🎉

---

## Part 4: Look around

Type each command in the terminal and press **Enter**.

### 1. Where am I?

```
git branch
```

You will see a list of branches. The one with a **star ⭐ (`*`)** is the branch you are in.

✅ The star must be next to **your nickname**.
🛑 If the star is next to **`main`**, **STOP** and call your teacher.

### 2. What is happening?

```
git status
```

It should say `On branch your-nickname` and `nothing to commit, working tree clean`. This means you have no changes yet.

> 🧠 When in doubt, run `git status`. It never changes anything. It only tells you what is going on.

---

## Part 5: Create your web page

### Your mission

> **Write a page about your favorite genre.**
> It can be a genre of **music** 🎵, **movies** 🎬, **books** 📚, or **games** 🎮.

### Step 1: Open the exercise folder

In the Explorer (left side), open the folders **`activities` → `exercise-1`**.

### Step 2: Create `index.html`

1. **Right-click** the `exercise-1` folder.
2. Click **New File**.
3. Type the name **`index.html`** and press **Enter**.
4. Copy this code into the file, then **change the parts in CAPITAL LETTERS**:

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title>My Favorite Genre</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>

  <h1>Hi, I'm YOUR-NICKNAME!</h1>

  <h2>My favorite genre is: YOUR GENRE</h2>

  <p>It is a type of: MUSIC / MOVIES / BOOKS / GAMES</p>

  <p>I like it because... WRITE 2 OR 3 SENTENCES HERE.</p>

  <h3>My top 3 examples</h3>
  <ul>
    <li>EXAMPLE 1</li>
    <li>EXAMPLE 2</li>
    <li>EXAMPLE 3</li>
  </ul>

</body>
</html>
```

5. Press **Ctrl + S** to save.

### Step 3: Create `style.css`

CSS is the file that gives **colors and style** to your page. 🎨

1. Right-click the `exercise-1` folder again → **New File**.
2. Name it **`style.css`**.
3. Copy this code:

```css
body {
  background-color: lightblue;
  font-family: Arial, sans-serif;
  text-align: center;
}

h1 {
  color: darkblue;
}

li {
  font-size: 20px;
}
```

4. Press **Ctrl + S** to save.

### Step 4: See your page

1. In the Explorer, **right-click `index.html`**.
2. Click **Reveal in File Explorer**.
3. **Double-click `index.html`**. Your page opens in the browser! 

Want to change something? Edit the file in VS Code, press **Ctrl + S**, and **refresh** the browser page (**F5**).

>  **Try it:** change `lightblue` to another color, like `pink`, `lightgreen`, or `orange`.

---

## Part 6: Send your work to GitHub 🚀

Now your files only exist **on this computer**. Let's send them to GitHub. Use the terminal in VS Code.

### 1. See what changed

```
git status
```

You will see your new files in **red**. Git is saying: *"I see these new files, but I'm not tracking them yet."*

### 2. Put your files in the box 

```
git add .
```

(The dot means "everything".)

### 3. Check again

```
git status
```

Now the files are **green**. They are in the box, ready to be sealed.

### 4. Seal the box with a label 

```
git commit -m "Add my favorite genre page"
```

This creates a **save point** (a *commit*) on your computer. The text between the quotes is the label. Write what you did.

### 5. Send it to GitHub 

```
git push
```

This uploads your save point to GitHub. Your teacher can now see it!

### 6. See your history 

```
git log
```

You will see your commit with **your nickname** and your message. Press **Q** to leave this screen.

You just did your first add → commit → push.**

**Show your screen to your teacher before you continue.**

---

##  Bonus mission

1. Change something in your page (a color, a new sentence, a fourth example).
2. Save with **Ctrl + S**.
3. Do the same cycle again:

```
git add .
git commit -m "Change the background color"
git push
```

4. Run `git log`. Now you should see **two commits**!

---

## Part 7: End your class

1. **Save all your files** (**Ctrl + K**, then **S**).
2. Close the browser tab with your page.
3. Go back to the folder **`C:\Turma`** and double-click **`end-class.bat`**.
4. Wait for the message that says your work was sent. If you see an **ERROR** message, **do not close the window** and call your teacher.
5. Press any key to close.

> ℹ️ It may say *"nothing to commit"*. That is fine! It means you already sent everything. 

The computer is now clean for the next student.

---

## ✅ Final checklist

- [ ] I started with `start-class.bat`
- [ ] My star ⭐ was on **my nickname**, not `main`
- [ ] I created `index.html` and `style.css`
- [ ] I saw my page in the browser
- [ ] I did `git add`, `git commit`, and `git push`
- [ ] I checked `git log` and showed my teacher
- [ ] I finished with `end-class.bat`

---

## 🆘 Something went wrong?

| Problem | What to do |
|---|---|
| The star is next to `main` | **Stop.** Call your teacher. |
| `Author identity unknown` | You skipped `start-class.bat`. Call your teacher. |
| `git push` shows an error | Do **not** try anything else. Call your teacher. |
| My page looks wrong | Check that you pressed **Ctrl + S**, then press **F5** in the browser. |
| My page is blank | Check the code: every `<tag>` needs a closing `</tag>`. |
| I don't know what is happening | Type `git status` and read the message. |

> ⚠️ **Never** use `git push --force`. It can erase other people's work.

---

## 📖 New words from today

| Word | Meaning |
|---|---|
| **Branch** | Your own universe inside the project 🌌 |
| **HTML** | The file that holds the **content** of a web page |
| **CSS** | The file that holds the **style** (colors, fonts) |
| **Terminal** | A place where you type commands |
| **Add** | Put your changes in the box 📦 |
| **Commit** | Seal the box with a label (a save point) 🏷️ |
| **Push** | Send your commits to GitHub 🚀 |
| **Log** | The history of your commits 📜 |
