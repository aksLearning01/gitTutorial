# Git Starting Commands
 

## Command Listing - Fresh Start
pwd
cd projects/
git init git-demo


## Command Listing - Start with Existing Project
pwd
cd website/
ls
git init

## Command Reference
Present Workding Directory

pwd
Change Directory

cd folder-name
Git initialization

git init [project-name]
project-name parameter is optional. If not supplied, Git will initialize the current directory.


## Command Listing
pwd
ls
mate README.md
ls
git status
git add README.md
git status
git commit -m "Initial commit"
clear
git status


## Command Reference
Express Commit for Tracked files

git commit -am "Awesome commit message"
Use the -a parameter with the git commit command to directly commit newly modified tracked files. Warning: Only do this for small changes. Tracked files are files that have been previously added to Git (committed or staged).

## Adding All Changed Files

git add .
The period parameter for the git add command will recursively add all new and newly modified files.

## Unstage File

git reset HEAD file-name
Following the above command will "unstage" the specified file from Git's staging area (aka index).

## Backout Working Directory Changes

git checkout -- file-name
Following the above command will back out any changes made to the specified file and replace it with the version last committed in Git
