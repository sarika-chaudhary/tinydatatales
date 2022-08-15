---
title: "Version Control with Git"
date: 2022-08-15
categories: 
- git
subtitle: "Basic commands to get started with git"
tags: 
- git
image:
  preview_only: true
---

## 1. What is a version control system?

- Manual version control.

- VCS helps us manage our project's files.

- A project can be anything from building websites to writing a thesis.
  Different kinds of files that are required for such projects
  like .txt files, js, css, html, etc.

## 2. How version control system can be helpful?

- History: git keeps track of every change that we make to our project.

- Collaboration: We generally use email for collaboration.

- Feature Branches: add features and merge them later.

## 3. What is git, and how does it work?

- Git is one of the most popular and decentralised version control systems.

- It keeps snapshots of the entire directory at different points.

## 4. How to install git?

- For Macbook use following command to install git:

  - `brew install git`

- To check the version of R in your system, type following command:
  - `git --version`

- To look for latest updates and to download git directly from the website use 
following url:

  - [https://git-scm.com/](https://git-scm.com/)

- To check git configuration, use the following command:
  - `git config --list`

- To add configuration:
   - `git config --global user.name "Sarika Chaudhary"`
   - `git config --global user.email "sarika61_ssf@jnu.ac.in"`
   
**Git is now ready for action.**

## 5. Making repository, Staging and Committing Changes

### Making Repo
- Create a folder on the desktop for example projects.
- Make a directory by typing `mkdir "hello-world"` within projects.
- Go to the hello-world folder. 
- Let us track any changes that are happening in the hello-world folder.
    In other words, let us create a git repository by:
  - `git init`

### Staging and Committing Changes
- Let us create an html file by `touch index.html
- Open index.html in emacs and add a line `<h1>Hello World<h1>`
- To check if any changes have been made to the directory
  - `git status`
- We have made one change in the `index.html` file and thinks that it can be one milestone in our project, we can now commit it.
- But before committing, we need to keep it in the staging area. We can do it by:
  - `git add index.html`
- Now, we can make our first commit using
  - `git commit -m "first draft(any comment here)"
- To check for commits:
  - `git log`
- suppose  we have typed something by mistake or deleted the file.
    We can get back to the last commit by
  - `git checkout -- .`

## 6. Cloning an existing repository.
- To clone a git repo, use following command
  - `git clone https://github.com/ep624/New-Project.git`
- It is helpful working together on projects. Anyone can use codes developed
   by others to improvise it.

## 7. Pushing to a server
- Make a repository on github. (e.g. project-work)
- To check for the origin link:
  - `git remote -v`
- To set a different origin url:
  - `git remote set-url origin https://github.com/sarika-chaudhary/project-work.git` use link of your github repo.
- Check again with `git remote -v`
- We are now ready to push to the server by 
  - `git push origin main`
- It might ask GitHub username or password. (if ssh link is used then it will not ask for password)
- One can always pull before starting work to get the most updated files by 
  - `git pull origin main`

## 8. Working with branches
- If we have a basic structure ready and we do not want to mess with the original file. In such cases, we use branches to make experiments and try new changes without impacting the original file. (it is like making a copy)
- Suppose that we want to write the second line of html file without impacting the original first line code. We can do it by creating a branch called secondline:
  - `git branch secondline`
- To check branches
  - `git brach`
- Now, to work on the secondline branch, switch to secondline branch by 
  - `git checkout secondline`
- Add second line in emacs and commit the changes
  - `<h2>Nice to connect to you all<h2>` (add second line in html file)
  - `git commit -am "second line done"` (-am here means a indicates add for stagging and m indicates message for committing)

- Now, if we want to switch to main brach:
  - `git checkout main`
  - `git status` indicates that there is no change in the main branch.
- If we want to a create branch and move to that branch simultaneously:
  - `git checkout -b thirdline`
- It will create a copy of the branch that we were on when new branch was created. 

- Add thirdline in emacs and commit the change
  - `<h3>Okay, see you soon!<h3>`
  - `git commit -am "finish"`

## 9. Merging branches or Feature Branches 

- We have secondline and thirdline branches. To check branches:
  - `git branch`
- We would need to merge them to get the final version
- While staying in secondline branch merge with thirdline branch:
  - `git checkout secondline`
  - `git merge thirdline`
- Merging is done, to check
  - `git log`
- To check further details about the merge 
  - `git show 1606ad9ff05463` 
- It is better to use one branch, like the secondline branch as
    a developer branch and thirdline as feature branch.
    In that way, there are fewer conflicts.
- To check changes between commits:
  - `git diff`

## 10. What is GitHub?

- It is a platform for sharing codes.
    (similar to social media)
