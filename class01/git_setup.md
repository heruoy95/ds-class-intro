# What is Git?
Git is, in short, a version control software. Read [a short intro to Git](https://git-scm.com/book/en/v2/Getting-Started-What-is-Git%3F) to understand how it does version control.

*Additional reading*: Atlassian's [What is version control](https://www.atlassian.com/git/tutorials/what-is-version-control)

# Why is version control useful?
* **Backup your work** 
* **Collaborate with others** 

# Installing Git
Check out [this page](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) for instructions on how to install Git on your laptop. 

For MacOS, you might already have Git, you can check by running `git --version` in your command line and see. For Windows, it's likely you'll need to install Git for Windows per web page above. For a bit more detail, you can refer to [this second page](https://www.atlassian.com/git/tutorials/install-git#windows) with step-by-step instructios.

Make sure you have the command line tool (terminal) but not the GitHub GUI desktop version. After installation, make sure your `git` is working by running `git --version` in your terminal.

# GitHub 
[GitHub](https://github.com/) is a place to host Git repositories:

> GitHub is a code hosting platform for version control and collaboration. It lets you and others work together on projects from anywhere.

If you do not have a GitHub account yet, please go ahead and create one. Follow the instructions in account set up to configure your local Git. 

If you're interested, spend 10 min to read and follow [this `Hello-Would` tutorial](https://guides.github.com/activities/hello-world/) to get some initial ideas for version control, repos, and how to use GitHub. 

# Git basics
### Get an existing repo
`git clone <repo url goes here>`
### Create a new repo
`git init <project name goes here>`

## When you’re ready to push code

### 1. See what’s changed since the last commit
`git status` shows files that have changed or are untracked
`git diff [optional: filename]` shows the changes themselves

### 2. “Stage” the things you want to include in your commit
This includes both files that have changed and new files you want to add.

`git add <file or directory>`

### 3. Commit your changes and add a useful message

`git commit -m ‘message goes here’`

### 4. (optional) Pull from the origin repo

`git pull`

If any other changes were made since you last pulled, this will attempt to merge them with yours. If you don’t do this and you need to, the remote repo will tell you.

### 5. Push to the origin repo

`git push`

## Additional useful commands
### `git log`
See the history of commits present in your copy of the repo.
### `git checkout <revision #, or branch name> <optional filename>`
If you give a revision number, this changes your files to how they were when that commit was the latest. Think of this like a time machine for going to old commits, without changing/losing anything in the present repo.

**WARNING:** if you specify a file, using `git checkout` without committing your latest changes will wipe them out.

If you give a branch name, `git checkout` will switch you to the most recent commit in that named branch and make that branch the active one (so new commits will be added to that branch)
### `git rm`
Remove a file from the repo
### `git mv`
Rename/move a file in the repo
### `git stash`
Save your changes to a “stash”, but don’t commit them. Useful if you might want to come back to things later, but want to wipe your changes clean right now.

# Task for the class:

1. In terminal/command line, navigate to the folder you want to put this repo.

2. Clone the repo
```
git clone https://github.com/Tian-Su/intro_to_data_science_2017.git
cd intro_to_data_science_2017
```

3. Check your current branch
```
git branch
```

4. Switch to branch `class01`
```
git branch class01 origin/class01
git checkout class01
```

5. Navigate to the folder `class01`. Create a test file with your name
```
cd class01
touch <your_name.txt>
```

6. Add the newly ceated file
```
git add <your_name.txt>
```
7. Commit the change
```
git commit -m "test git function"
```
8. push the change to remote

```
# you many need to do 'git pull' (pull the most recent change) first, if you see the promp

git push
```


## Git Cheatsheet
[PDF](https://training.github.com/kit/downloads/github-git-cheat-sheet.pdf)