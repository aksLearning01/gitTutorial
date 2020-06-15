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



History and File Management Commands
Git History / File Management Commands
 

Lecture Command Listing -- History
git log
git help log
git log --oneline --graph --decorate --color
 

Lecture Command Listing -- Removing Files
pwd
git status
mate debug.log
ls
git status
git add .
git status
git commit -m "adding log file that really does not belong here"
clear
git status
git rm debug.log
ls
git status
git commit -m "removing log file"
clear
mate info.log
ls
git add info.log
git commit -m "adding info log"
git status
clear
ls
rm info.log
ls
git status
git add .
git add -u
clear
git status
git commit -m "Removing info.log"
 

Lecture Command Listing -- Moving Files
ls
mkdir web
ls
git mv index.html web
cd web/
ll
pwd
cd ..
ls
git status
git commit -m "Moving index.html file to web folder"
clear
 

Lecture Command Listing -- Ignoring Files
mate application.log
ls
git status
mate .iitignore
git status
ls -a
git add .gitignore
clear
git status
git commit -m "adding ignore file"
 

## Command Reference
Seeing Repository History

git log
git log --oneline --graph --decorate --color
Git's log command displays the repository's history in reverse chronological order. The no-params version displays the standard view.

Git log options from above: --oneline Compacts log data on to one line, abbreviating the SHA1 hash --graph Adds asterisk marks and pipes next to each commit to show the branching graph lines --decorate Adds the markers for branch names and tags next to corresponding commits --color Adds some color to the output -- nice to have, depending on the operating system
Removing a file using Git

git rm file-name
Removing a file using Terminal

rm file-name
This removes the file outside Git's knowledge

Updating Git's Index (staging area)

git add -u
The -u parameter will recursively update Git's staging area regarding deleted/moved files outside of Git.

Making a directory (folder)

mkdir folder-name
The mkdir command is a nearly universal command for creating a directory/folder.

Making a directory (folder)

git mv source destination
The git mv command will move the source (file or folder) to the destination with Git.


## SSH Authentication Commands
 

Lecture Command Listing
cd ~
cd .ssh
mkdir .ssh
cd .ssh
pwd
ssh-keygen -t rsa -C "jason@jasongtaylor.com"
mate id_rsa.pub
ssh -T git@github.com
 

Command Reference
Generating an SSH Key

ssh-keygen -t rsa -C "your.name@your-company.com"
Use your actual email address in the example above.

Verify SSH authentication

ssh -T git@github.com
Above command uses ssh to connect to GitHub over the SSH protocol.

## Git Remote Commands
 

 Command Listing
git status
git remote add origin git@github.com:scm-ninja/git-demo.git
git remote -v
git push -u origin master
git push origin master
ls
cd web/
mate index.html
clear
git commit -am "Updating index page for GH"
git status
git pull origin master
git push origin master
 

Command Reference
Creating a remote repository reference

git remote add remote-name remote-repository-location
Using git remote add command allows us to associate a remote repository. Normally, you want to paste in the full URL for the remote repository given to you by your Git host (GitHub). By convention, the first or primary remote repository is named origin.

List Git's Remotes

git remote -v
The git remote command lists the names of all the remote repositories and the -v parameter (verbose) will display the full URL of the remote repository for each remote name listed

Send Changes to Remote

git push -u remote-name branch-name
git push remote-name branch-name
The git push sends all your local changes (commits) on branch branch-name to the remote named remote-name. The -u parameter is needed the first time you push a branch to the remote.

Receive Changes from Remote

git pull remote-name branch-name
The git pull receives all your remote changes (commits) from the remote named remote-name and on branch branch-name.
