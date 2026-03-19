Author - Mahesh Khot

# git-commands-reference
Collection of Git commands with explanations and when to use them.

# Git

Version Control System is a tool that helps to track changes in code.

Git is a Version Control System. It is:

- popular  
- free & open source  
- fast & scalable

- Git Used for
1) Track the history  
2) Collaborate  

# GitHub

A website that allows developers to store and manage their code using Git.

https://github.com

# GitHub Account

- Create a new repository: git-commands-reference  
- Make your first commit

  # Note - <br> tag is used between two lines to insert new line

  # Setting up Git

You can use Git from the following environments:

- Visual Studio Code  
- Windows (Git Bash)  
- Mac (Terminal)  

## ✅ Verify Installation

Run the following command to check if Git is installed:

git --version

# Configuring Git

## Set Username
git config --global user.name "Your Name"

## Set Email
git config --global user.email "your@email.com"

## Check Configuration
git config --list

# Git using VS code:
Create new folder & open it in VS code.
Basic cmd of git

# Clone & Status

## 📥 Clone
Clone a repository from GitHub to your local machine.

Command:
git clone <repository-link>

## 📊 Status
Check the current state of your working directory and staging area.

Command:
git status


# Remote vs Local

## 🌐 Remote
Refers to the repository hosted on GitHub (cloud).

## 💻 Local
Refers to your system (laptop/PC) where you write and modify code.

## 📂 Change Directory

Use the following command to navigate between folders:

Command:
cd <directory-name>

# Move to Parent Directory

## Command
cd ..

## When to use
Use this command to move one level up (back) in the directory structure.

## Example
cd ..

cd /        # go to root directory  
cd ~        # go to home directory  

# Create Directory

## Command
mkdir LocalRepo

## When to use
Use this command to create a new folder/directory.

## Example
mkdir LocalRepo

mkdir project-name      # create a folder  
mkdir -p a/b/c          # create nested directories  

# Remove Directory

## Command
rm -r LocalRepo


## 🗑️ Remove Empty Directory
rmdir <directory-name>

## 🔥 Remove Non-Empty Directory (Important)
rm -r <directory-name>

## ⚠️ Force Delete
rm -rf <directory-name>

## When to use
- `rmdir` → when folder is empty  
- `rm -r` → when folder contains files  
- `rm -rf` → force delete (use carefully ⚠️)

## Example
rm -r LocalRepo

rm -rf deletes permanently (no recycle bin ❌)

# List Files

## Command
ls

## When to use
Use this command to list all files and folders in the current directory.

## Example
ls

ls -l   # detailed list  
ls -a   # show hidden files  

# Git File States

Git tracks files in different states:

## 🆕 Untracked
New files that Git is not tracking yet.

## ✏️ Modified
Files that have been changed but not staged.

## 📦 Staged
Files that are added to the staging area and ready to commit.

## ✅ Unmodified
Files that have no changes.

# Add & Commit

## 📥 Add
Add new or modified files to the staging area.

Command:
git add <file-name>

## 📝 Commit
Save the staged changes as a snapshot in the repository.

Command:
git commit -m "your message"

git add .        # add all files
git commit -m "initial commit"

# Push Command

## 🚀 Push
Push your local commits to the remote repository (GitHub).

Command:
git push origin main

git push -u origin main   # set upstream (first time push)
git push                  # push after upstream is set

git push -u origin main   # set upstream

git branch -vv            # check

# git branch --unset-upstream   # remove

# Init & First Push (Local → GitHub)

## 🆕 Initialize Repository
Create a new Git repository in your project folder.

git init

# create new repo in GitHup to push local repo on GitHub dont add README.md there.

## 🔗 Add Remote Repository
Connect your local repo to GitHub.

git remote add origin <repository-link>

## 🔍 Verify Remote
Check if the remote is added correctly.

git remote -v

## 🌿 Check Branch
View current branch.

git branch

## 🔄 Rename Branch (to main)
Rename default(master) branch to main.

git branch -M main

## 🚀 Push to GitHub
Push your local code to remote repository.

git push origin main
if you know we are going to work on this repo for long time then we can use below cmd to create shortcuter for main branch then we can push using only git push command no need to write origin main again and again.

git push -u origin main

Now we can create README.md in local repo & add, commit & push.

# 🚀 Git Workflow (Clone Remote → Local)
# 🚀 Git Workflow

## Steps

1. Create a new repository on GitHub (initialize with README.md)

2. Clone the repository  
   git clone <repo-link>

3. Make changes to your code  

4. Stage changes  
   git add .

5. Commit changes  
   git commit -m "your message"

6. Push changes to GitHub  
   git push origin main


# 🚀 Upload Existing Local Project to GitHub

## 🆕 Initialize Repository
Create a new Git repository in your project folder.

git init

---

## 🌐 Create Repository on GitHub
Create a new repository on GitHub.

⚠️ Important:
- Do NOT add README.md
- Do NOT add .gitignore
- Do NOT initialize anything

---

## 🔗 Add Remote Repository
Connect your local project to GitHub.

git remote add origin <repository-link>

---

## 🔍 Verify Remote
Check if the remote is added correctly.

git remote -v

---

## 🌿 Check Current Branch
View current branch name.

git branch

---

## 🔄 Rename Branch to main
Rename default branch (master → main).

git branch -M main

---

## 📦 Add Files to Staging
Add all project files.

git add .

---

## 📝 Commit Changes
Save your changes.

git commit -m "initial commit"

---

## 🚀 Push to GitHub
Push your code to the remote repository.

git push origin main

---

## 🔥 Set Upstream (Recommended)
If you will work on this repo regularly, set upstream branch:

git push -u origin main

👉 After this, you can simply use:
git push

---

## 📄 Add README Later
Now you can create README.md locally, then:

git add README.md  
git commit -m "add README"  
git push

# 🌿 Git Branches

Branches allow you to work on different features independently without affecting the main codebase.

## 🔹 Main Branch
- Usually called `main` (or `master`)
- Contains stable, production-ready code

## 🔹 Feature Branch
- Used to develop new features or fixes
- Created from main branch
- Merged back after completion

# 🌿 Branch Commands

## 📌 Check Branches
git branch

## 🔄 Rename Branch
git branch -M main

## 🔀 Switch Branch
git checkout <branch-name>   # standard (commonly used)

# Optional (modern alternative)
git switch <branch-name>

## ➕ Create New Branch
git checkout -b <branch-name>   # standard

# Optional (modern alternative)
git switch -c <branch-name>

## ❌ Delete Branch
git branch -d <branch-name>
we can not delete current branch on which we are right now first we need to checkout current branch then we can delete it.

# code pushed on new branch that will be only on new branch not in main branch.

# 🔀 Merging Code

## 🧪 Way 1: Using Commands

### Compare Changes
git diff <branch-name>  
# Compare commits, branches, and files

### Merge Branch
git merge <branch-name>  
# Merge selected branch into current branch

---

## 🌐 Way 2: Using GitHub

Create a Pull Request (PR) to merge changes via GitHub UI.

# 🔄 Pull Request (PR)

A Pull Request allows you to notify others about changes you have pushed to a branch on GitHub.

It is used to review, discuss, and merge changes into the main branch.

# 🔄 Pull Request (PR)

A Pull Request allows you to notify others about changes you have pushed to a branch on GitHub.

It is used to review, discuss, and merge changes into the main branch.

after this global repo(Githhub) code is marged but now we want that change into main also so we need to use below cmd

# 📥 Pull Command

## Command
git pull origin main

## What it does
Fetches the latest changes from the remote repository and merges them into your current branch.

## When to use
Use this command to update your local code with the latest changes from GitHub.

git pull origin main   # before starting work  
git pull               # if upstream is set  


# ⚠️ Resolving Merge Conflicts

A merge conflict occurs when Git cannot automatically resolve differences between two branches.

## When it happens
- Same file edited in multiple branches  
- Same lines changed differently  

## How to resolve

1. Open the conflicted file  
2. Look for conflict markers:

<<<<<<< HEAD  
your changes  
=======  
incoming changes  
>>>>>>> branch-name  

3. Edit and keep the correct code  
4. Remove conflict markers  
5. Save the file  

## Final steps

git add <file-name>  
git commit -m "resolve merge conflict"

## using command line(## 🧪 Way 1: Using Commands)

# git merge <Branch name>
after this for both/all branch we can to merge(if auto merge is not possible then we need to manual resolve it) & then we need to push on github using git push cmd.



# # 🔄 Undoing Changes

## 📦 Case 1: Staged Changes
Unstage files (move back to working directory):

git reset <file-name>  
git reset  

---

## 📝 Case 2: Last Commit
Undo last commit (keep changes):

git reset HEAD~1  

---

## 🧨 Case 3: Multiple Commits

git reset <commit-hash>        # move to specific commit (keep changes)  
git reset --hard <commit-hash> # ⚠️ delete changes permanently  

---

## ⚠️ Warning
- `--hard` will delete changes permanently (no recovery)  
- Use carefully  

# git log   # to get commit hash



# View Commit History

## Command
git log

## When to use
Use this command to view the commit history of your repository.

## Example
git log


git log --oneline        # short commit history  
git log --graph          # show branch structure  
git log --oneline --graph --all   # best view  


# 🍴 Fork

A fork is a copy of an existing repository that allows you to freely experiment with changes without affecting the original project.

## Key Points
- Creates a copy of the original repository (upstream)  
- Used to contribute to open-source projects  
- Changes can be submitted back using a Pull Request  

## Simple Meaning
Fork = copy someone else's repo to your GitHub

# # Fork Workflow

1. Fork repository on GitHub  
2. Clone forked repo  
3. Make changes  
4. Push changes  
5. Create Pull Request  

