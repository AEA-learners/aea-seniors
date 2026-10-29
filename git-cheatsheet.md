# 🪄 Git Cheat Sheet

A quick reference for the commands we use in class.

## 🌿 Branches

```
git branch                      - Lists your local branches (the current one has a *).
git branch -D [branch-name]     - Force-deletes a LOCAL branch, even if it was never merged
                                  into main. (Lowercase -d is the safe version: it only
                                  deletes if the work has already been merged.)
git checkout main               - Switches to the main branch. The files in your folder
                                  change to match that branch.
git checkout [name]             - Switches to any branch that already exists.
git checkout -b [name]          - Creates a new branch from the current one and jumps into it.
git switch [name]               - Does the same as checkout [name], with a clearer name.
git push origin --delete [name] - Deletes the REMOTE branch (the one on GitHub).
                                  "origin" is the nickname for the GitHub address.
```

## 📦 The Everyday Cycle

```
git status                      - Shows what changed and what is ready to commit.
git add [file]                  - Puts a file into the "box" for the next commit.
git add .                       - Puts all changes into the box.
git commit -m "message"         - Seals the box: creates a save point on YOUR computer,
                                  with your message as the label.
git push                        - Sends the commits of the current branch to GitHub.
git push -u origin [name]       - Sends a new branch for the first time and links your local
                                  branch to the remote one (after that, "git push" is enough).
git pull                        - Brings changes from GitHub to your computer.
git fetch                       - Only downloads what's new on GitHub, without merging yet.
git log                         - Shows the commit history.
```

## 📥 Copying Repositories

```
git clone [url]                 - Downloads the whole repository to your computer.
git clone --mirror [url]        - Creates a full backup (all branches and the full history).
git remote update               - Inside a --mirror backup, updates it with what's new
                                  on GitHub.
git ls-remote [url]             - Asks GitHub what exists there, without downloading.
                                  Great for testing if your connection and password work.
```

## ⚠️ Dangerous Commands (use with care)

```
git push --force origin [name]  - Overwrites the remote branch with your version, erasing
                                  whatever was different there.
git commit --amend -m "text"    - Rewrites the LAST commit (here, just its message).
                                  If it was already pushed, it only reaches GitHub
                                  with --force.
```

## ⚙️ Configuration

```
git config --local user.name "X"     - Sets the commit author name for this repository only.
git config --local user.email "Y"    - Sets the commit email for this repository only.
git config --global ...              - Same, but applies to ALL repositories on the computer.
git config --local --unset user.name - Removes the configured name.
git config --local credential.helper "cache --timeout=3600"
                                     - Keeps your password/token in memory for 1 hour.
git credential-cache exit            - Clears what was kept in that cache right now.
```

## 💡 Three Ideas to Remember

- **Local vs. remote:** many commands come in two versions, one that changes your computer (`git branch -D`) and one that changes GitHub (`git push origin --delete`). Deleting on one side does not delete on the other.
- **Commit is not push:** a commit saves on your computer, and only a push takes it to GitHub.
- **When in doubt, `git status`:** it never changes anything, and it shows you where you are.