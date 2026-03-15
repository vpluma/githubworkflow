Git & GitHub Command Line Workflow
Classroom Guide - Norwalk High School – Computer Science Pathway
Instructor: Mr. Vinson Pluma

This guide explains how to use Git from the command line with GitHub to manage code and collaborate on projects.

Works with:

Git Bash (Windows)

Terminal (Linux / macOS)

SECTION 1 — WHAT GIT AND GITHUB ARE

Git
Git is a version control system used to track changes in code.

Git allows you to:

save versions of your project

revert to earlier versions

collaborate with others

track who changed what

GitHub
GitHub is a cloud platform that stores Git repositories online.

Benefits:

backup your code

collaborate with others

publish projects

build a portfolio

SECTION 2 — FIRST UPLOAD: CREATING A NEW REPOSITORY

Use this workflow when:

you created a project locally

you created an empty repository on GitHub

Step 1 — Open Terminal or Git Bash

Navigate to your project folder.

cd path/to/yourProjectFolder

Example

cd Desktop/myWebProject

Step 2 — Initialize Git

This turns the folder into a Git repository.

git init

Step 3 — Configure Your Identity

This tells Git who is making commits.

git config user.name "Firstname Lastname"
git config user.email "gmail_username@gmail.com
"

Example

git config user.name "Alex Garcia"
git config user.email "alexgarcia@gmail.com
"

Step 4 — Check the Project Status

git status

Git will show which files are new or modified.

Step 5 — Add Files to Git

git add .

This stages all project files.

Step 6 — Create the First Commit

git commit -m "Initial commit"

A commit saves a snapshot of the project.

Step 7 — Rename the Default Branch

Modern Git uses main instead of master.

git branch -M main

Step 8 — Connect the GitHub Repository

Copy the repository URL from GitHub.

Example

https://github.com/username/project_repo_name.git

Add it as the remote repository:

git remote add origin https://github.com/username/project_repo_name.git

Step 9 — Upload Code to GitHub

git push -u origin main

You will be prompted for credentials.

Username: your GitHub username
Password: paste your Personal Access Token

IMPORTANT
GitHub no longer allows account passwords for Git operations.
You must use a Personal Access Token (PAT).

SECTION 3 — MAKING UPDATES TO YOUR PROJECT

Use this workflow whenever you modify your project.

Step 1 — Check Changes

git status

Step 2 — Add Updated Files

git add .

Step 3 — Commit the Changes

Write a clear description.

git commit -m "Added login page"

Example commit messages

Fixed bug in navigation
Added CSS styling
Updated README file

Step 4 — Push Changes to GitHub

git push

Your updates will now appear on GitHub.

SECTION 4 — CLONING AN EXISTING REPOSITORY

Use this when downloading an existing project from GitHub.

Step 1 — Copy the Repository URL

Example

https://github.com/username/project_repo_name.git

Step 2 — Clone the Repository

git clone https://github.com/username/project_repo_name.git

Example

git clone https://github.com/alexgarcia/myproject.git

Step 3 — Enter the Project Directory

cd project_repo_name

Now the repository is on your computer.

SECTION 5 — UPDATING A CLONED PROJECT

If other people have updated the repository, download changes.

git pull origin main

This fetches the latest code from GitHub.

SECTION 6 — IMPORTANT GIT COMMANDS

Command Purpose

git init create new repository
git status show changed files
git add . stage all changes
git commit -m "message" save snapshot
git push upload changes
git pull download changes
git clone copy repository

SECTION 7 — CREATING A .gitignore FILE

A .gitignore file tells Git which files to ignore.

Create it:

touch .gitignore

Example contents

node_modules/
.env
*.log
.DS_Store
Thumbs.db

This prevents uploading unnecessary or sensitive files.

SECTION 8 — COMMON GIT ERRORS AND SOLUTIONS

Authentication Failed

Example message

remote: Support for password authentication was removed

Solution

Use a GitHub Personal Access Token instead of a password.

Repository Not Found

Example

fatal: repository not found

Possible causes

incorrect URL

repository is private

incorrect GitHub username

Fix by verifying the repository URL.

Branch Does Not Exist

Example

src refspec main does not match any

Fix

Make sure you committed before pushing.

git commit -m "first commit"

Then push again.

Remote Already Exists

Example

remote origin already exists

Fix

git remote remove origin

Then add it again

git remote add origin REPOSITORY_URL

Push Rejected

Example

failed to push some refs

Fix

git pull origin main

Then push again.

SECTION 9 — RECOMMENDED GIT WORKFLOW

Typical daily workflow

git pull
git add .
git commit -m "Describe changes"
git push

SECTION 10 — BEST PRACTICES

Commit often
Write clear commit messages
Pull before pushing
Never upload passwords or tokens
Use .gitignore

SECTION 11 — EXAMPLE FULL WORKFLOW

cd myProject
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/username/project.git

git push -u origin main

Later updates

git add .
git commit -m "Updated styling"
git push

SECTION 12 — WHY DEVELOPERS USE GIT

Git is used by major technology companies including:

Google
Microsoft
Amazon
Apple
Netflix

Learning Git is an essential skill for software engineers and developers.
