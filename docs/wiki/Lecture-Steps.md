**English** · [Dansk](Lecture-Steps-da) · [Bahasa Melayu](Lecture-Steps-ms)

# Lecture steps

## 1. Install Git and Git Bash

**What we did:** Downloaded Git for Windows, accepted the licence, kept the default options (Git Bash ticked) and set Git Bash as the default terminal profile in VS Code. Mac users skip this: Bash is already installed.

![Install Git and Git Bash](https://git.tirsystem.com/Tirsvad-Udemy-100-days-of-code/070-version-control/raw/branch/main/docs/images/01-install-git.png)

**What we gained:** A working `git` command and a Unix-style shell on Windows, so every later command in the course runs the same on all systems.

## 2. What is version control?

**What we did:** Version control saves versions (save points) of your files. If code gets corrupted you compare with an earlier version and roll back. Git also supports cloning, forking, pull requests and merging.

![What is version control?](https://git.tirsystem.com/Tirsvad-Udemy-100-days-of-code/070-version-control/raw/branch/main/docs/images/02-version-control.png)

**What we gained:** The idea that nothing is lost: every change is a recoverable step, which makes experimenting safe.

## 3. Local version control

**What we did:** In a folder `Story` we ran `git init`, created `chapter1.txt`, staged it with `git add`, saved it with `git commit -m "Complete chapter 1"` (present tense), looked at history with `git log`, compared with `git diff` and restored a file with `git checkout -- <file>`.

![Local version control](https://git.tirsystem.com/Tirsvad-Udemy-100-days-of-code/070-version-control/raw/branch/main/docs/images/03-local-git.png)
![Local version control](https://git.tirsystem.com/Tirsvad-Udemy-100-days-of-code/070-version-control/raw/branch/main/docs/images/03b-diff-restore.png)

**What we gained:** The working directory vs. the staging area, how to make a commit, read the history and undo unwanted edits.

## 4. GitHub and remote repositories

**What we did:** Created a GitHub account and an empty repository (public or private), then connected the local repository with `git remote add origin <url>` and uploaded with `git push -u origin main`. The screenshot pushes to a local bare repository so it works offline.

![GitHub and remote repositories](https://git.tirsystem.com/Tirsvad-Udemy-100-days-of-code/070-version-control/raw/branch/main/docs/images/04-remote-push.png)

**What we gained:** A remote copy as backup and for sharing, and the meaning of `origin` and the `main` branch.

## 5. The .gitignore file

**What we did:** Created `.gitignore` before the first commit and listed `secrets.txt`, `.DS_Store`, `*.pyc` and `.venv/`. Git then stops showing those files and never commits them. Templates per language: github.com/github/gitignore.

![The .gitignore file](https://git.tirsystem.com/Tirsvad-Udemy-100-days-of-code/070-version-control/raw/branch/main/docs/images/05-gitignore.png)

**What we gained:** How to keep passwords and API keys out of local and public repositories, and that wildcards and `#` comments work in the file.

## 6. Branching and merging

**What we did:** Created the branch `alien-plot` with `git branch`, switched with `git checkout`, committed there, switched back to `main` and combined the work with `git merge alien-plot`. Optional practice: learngitbranching.js.org.

![Branching and merging](https://git.tirsystem.com/Tirsvad-Udemy-100-days-of-code/070-version-control/raw/branch/main/docs/images/06-branching.png)

**What we gained:** Experiments and new features can live apart from `main`, which stays stable, and are merged only when they work.

## 7. Forking and pull requests

**What we did:** Reviewed the four areas (working directory, staging area, local repository, remote repository). A fork is your own copy of someone else's repository; after changing it you open a pull request asking the owner to merge. Only the owner can merge.

![Forking and pull requests](https://git.tirsystem.com/Tirsvad-Udemy-100-days-of-code/070-version-control/raw/branch/main/docs/images/08-four-areas.png)
![Forking and pull requests](https://git.tirsystem.com/Tirsvad-Udemy-100-days-of-code/070-version-control/raw/branch/main/docs/images/07-fork-pull-request.png)

**What we gained:** How open-source collaboration works: propose changes without touching the original, review each other's code and contribute to projects.
