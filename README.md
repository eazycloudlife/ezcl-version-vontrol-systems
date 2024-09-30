| Status      | Proposed                                                     |
| ----------- | ------------------------------------------------------------ |
| Category    | Document                                                     |
| Team        | [DevOps](https://github.com/orgs/easycloudlife/teams/DevOps) |
| Authors(s)  | [eazycloudlife](https://github.com/eazycloudlife)            |
| Created By  | Oct 2024                                                     |
| Modified By | Oct 2024                                                     |

---

### **Index**

1. [What is this repository for?](#what-is-this-repository-for)
2. [Git Basics](#git-basics)
3. [Branching & Merging](#branching--merging)
4. [Viewing Commit History](#viewing-commit-history)
5. [Undoing Changes](#undoing-changes)
6. [Remote Repositories](#remote-repositories)
7. [Advanced Git Commands](#advanced-git-commands)
8. [Git Aliases](#git-aliases)
9. [Git Ignoring Files](#git-ignoring-files)
10. [Git Hooks](#git-hooks)

**[⬆ Back to Index](#index)**

## What is this repository for?

Here's a **comprehensive Git cheat sheet** that covers commands from basic to advanced, grouped by common workflows and use cases:

**[⬆ Back to Index](#index)**

### **Git Basics**

| Command                                               | Description                                                              |
| ----------------------------------------------------- | ------------------------------------------------------------------------ |
| `git config --global user.name "<Your Name>"`         | Configure the user name                                                  |
| `git config --global user.email "<Your Email>"`       | Configure the user email                                                 |
| `git config --global user.password "<Your Password>"` | Configure the user password                                              |
| `git init`                                            | Initialize a new Git repository in your project directory                |
| `git clone <url>`                                     | Clone a remote repository to your local machine                          |
| `git status`                                          | Show the working directory status (untracked, modified files)            |
| `git add <file>`                                      | Stage specific files for the next commit                                 |
| `git add .`                                           | Stage all modified and untracked files for the next commit               |
| `git commit -m "message"`                             | Commit staged changes with a commit message                              |
| `git log`                                             | Show commit history                                                      |
| `git log --oneline`                                   | Show a simplified commit history (one line per commit)                   |
| `git diff`                                            | Show changes between working directory and the last commit               |
| `git diff --staged`                                   | Show changes between staged files and the last commit                    |
| `git pull`                                            | Fetch and merge changes from the remote repository to the current branch |
| `git push`                                            | Push local changes to the remote repository                              |
| `git branch`                                          | List branches                                                            |
| `git branch -d <branch>`                              | Delete a branch (local)                                                  |
| `git checkout <branch>`                               | Switch to a different branch                                             |
| `git checkout -b <branch>`                            | Create and switch to a new branch                                        |

**[⬆ Back to Index](#index)**

---

### **Branching & Merging**

| Command                             | Description                                                    |
| ----------------------------------- | -------------------------------------------------------------- |
| `git branch <branch-name>`          | Create a new branch                                            |
| `git checkout <branch-name>`        | Switch to an existing branch                                   |
| `git checkout -b <branch-name>`     | Create and switch to a new branch                              |
| `git merge <branch-name>`           | Merge changes from a branch into the current branch            |
| `git merge --no-ff <branch-name>`   | Merge with a merge commit (non-fast-forward)                   |
| `git branch -d <branch-name>`       | Delete a branch (safe: only deletes if fully merged)           |
| `git branch -D <branch-name>`       | Force delete a branch (even if not merged)                     |
| `git rebase <branch-name>`          | Reapply commits on top of another base branch                  |
| `git stash`                         | Save changes in a stash (temporarily) without committing       |
| `git stash apply`                   | Reapply stashed changes                                        |
| `git stash drop`                    | Discard stashed changes                                        |
| `git cherry-pick <commit-hash>`     | Apply the changes from a specific commit to the current branch |
| `git tag <tagname>`                 | Create a lightweight tag at the current commit                 |
| `git tag -a <tagname> -m "message"` | Create an annotated tag with a message                         |

**[⬆ Back to Index](#index)**

---

### **Viewing Commit History**

| Command                     | Description                                                              |
| --------------------------- | ------------------------------------------------------------------------ |
| `git log`                   | View full commit history                                                 |
| `git log --oneline`         | View commit history in a compact, one-line-per-commit format             |
| `git log --graph --oneline` | Visualize commit history as a graph                                      |
| `git log --author="<name>"` | View commit history for a specific author                                |
| `git show <commit-hash>`    | Show the details of a specific commit                                    |
| `git blame <file>`          | Show who made each change in the file and when                           |
| `git reflog`                | Show the history of changes to HEAD (useful for recovering lost commits) |

**[⬆ Back to Index](#index)**

---

### **Undoing Changes**

| Command                       | Description                                                                          |
| ----------------------------- | ------------------------------------------------------------------------------------ |
| `git restore <file>`          | Restore the specified file to the last commit state                                  |
| `git restore --staged <file>` | Unstage a file without discarding changes                                            |
| `git reset <commit>`          | Reset the current branch to the specified commit (changes stay in working directory) |
| `git reset --hard <commit>`   | Reset the current branch to a commit and delete all changes since then               |
| `git revert <commit>`         | Create a new commit that undoes changes from the specified commit                    |
| `git clean -fd`               | Remove untracked files and directories                                               |
| `git stash pop`               | Apply and remove the latest stash                                                    |

**[⬆ Back to Index](#index)**

---

### **Remote Repositories**

| Command                                   | Description                                      |
| ----------------------------------------- | ------------------------------------------------ |
| `git remote -v`                           | Show remote URLs associated with your repository |
| `git remote add <name> <url>`             | Add a remote repository                          |
| `git fetch`                               | Fetch changes from the remote repository         |
| `git push <remote> <branch>`              | Push changes to the remote repository            |
| `git pull <remote> <branch>`              | Fetch and merge changes from the remote branch   |
| `git remote rm <name>`                    | Remove a remote repository                       |
| `git remote rename <old-name> <new-name>` | Rename a remote repository                       |

**[⬆ Back to Index](#index)**

---

### **Advanced Git Commands**

| Command                                                 | Description                                                   |
| ------------------------------------------------------- | ------------------------------------------------------------- |
| `git cherry-pick <commit-hash>`                         | Apply a specific commit from another branch into your branch  |
| `git rebase <branch-name>`                              | Reapply commits from your branch on top of another branch     |
| `git bisect start`                                      | Start a bisect session to find a commit that introduced a bug |
| `git bisect bad <commit>`                               | Mark a commit as bad during a bisect session                  |
| `git bisect good <commit>`                              | Mark a commit as good during a bisect session                 |
| `git archive --format=zip --output=<file.zip> <branch>` | Export the contents of a branch as a zip file                 |
| `git shortlog -s -n`                                    | Show the number of commits by author                          |
| `git diff <branch1>..<branch2>`                         | Show the difference between two branches                      |

**[⬆ Back to Index](#index)**

---

### **Git Aliases**

You can create shortcuts for frequently used commands by setting Git aliases:

| Command                                 | Description                       |
| --------------------------------------- | --------------------------------- |
| `git config --global alias.co checkout` | Alias `git co` for `git checkout` |
| `git config --global alias.br branch`   | Alias `git br` for `git branch`   |
| `git config --global alias.ci commit`   | Alias `git ci` for `git commit`   |
| `git config --global alias.st status`   | Alias `git st` for `git status`   |

**[⬆ Back to Index](#index)**

---

### **Git Ignoring Files**

| Command                  | Description                                                  |
| ------------------------ | ------------------------------------------------------------ |
| `.gitignore`             | A file specifying files and directories to be ignored by Git |
| `git rm --cached <file>` | Remove a file from Git tracking while keeping it locally     |

**[⬆ Back to Index](#index)**

---

### **Git Hooks**

Git hooks allow you to run scripts automatically at certain points in the Git workflow (e.g., before committing, before pushing).

| Command                 | Description                           |
| ----------------------- | ------------------------------------- |
| `.git/hooks/pre-commit` | Hook script that runs before a commit |
| `.git/hooks/post-merge` | Hook script that runs after a merge   |

**[⬆ Back to Index](#index)**

---

This cheat sheet covers the essential Git commands, from basic to advanced, that you'll need for effective version control and collaboration.

**[⬆ Back to Index](#index)**
