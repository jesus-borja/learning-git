# Demo repository (also a private one... it's not private anymore)

This is suposed to be a description for the project.
It's also important to say that this README.md file is used in Github to show information about the repository :)
 
## Now locally from linux
 
I'm continuing with the crash course of git & github. Thanks FreeCodeCamp.org and Nico from youtube.com/c/HolaMundoDev :)

## git init 

This command is used when we start a new repository locally, instead of first creating one on Github and then cloning it to a local machine.
It can be executed in any directory where we want to keep track of the files that are in it.
 
## git status 
 
This command help us know wich files have been created, but aren't tracked by git yet, wich ones have been modified or deleted
 
## git add .
 
This is often used to tell git to track all the files in a specified directory (more specifically in the directory where it was called).
This is considered a bad practice because there may be some files that we have changed, but not necessarily want to push'em. Or there may be binary files, or images that we don't want to upload because they use too much space.
It should be used when we are completely sure that all the changes we have done are going to be useful. 

### git add `<filename>`
 
We can alse use git add to add a single file to the stage, where they are waiting to be confirmed.
 
## git commit -m "Commit title" -m "Commit description"

 (Commit in spanish means "Comprometer")
The first "-m" is used to give a message about the commit, ideally it is related to the why we're making a commit.
We're forced to provide a title for commiting a change.
The second "-m" is used to provide a better description of what the commit does.

## git commit -am "Commit title" -m "Commit description"

This command helps us add (that's what -a means) and commit our changes at the same time.

## git remote

Until the remote command means that it will be stored somewhere else, but not this computer and it's commonly used to give it a reference to a remote repository on github.

## git remote add origin `github.url`

This is the full command that we usually use when we want to connect a local repository to github.

## git remote -v

Tells us the connections a local repository has outside of this computer.

## git push -u origin master

When we create a local repository and we want to upload it to github we need to tell github where it has to store our commits.
This command helps us to do exactly that and it's a shortcut so we don't need to tell it every time we make a push.
Whit this command we save the information to push on the local repo.

## git push
So far all the changes we've done and commited have been made locally, this hasn't modified our repo in github.
To do so, we use `git push`. What it does is tell git to push all the changes we have done locally to the remote server in github.com.

## .gitignore
This file is used when we want to have files or information that is not tracked by git.
For this purpose, we use a file named `.gitignore` and inside this file we will place all the files or paths that we want git to ignore.
For example, we may do this to ignore the file where some enviroment variables are (.env) or paths were some modules are stores (like node_modules):

## git status -s
This command is really similar to `git status`, it just modifies how the changes are displayed in console.
This is a screenshot of the output when we execute `git status`:

And this is when we execute `git status -s`:

The red "M" means that the file has been modified, but aren't in the stage area just yet.
Therefore, the green "M" means that the file is in the stage area and ready to be commited.
For last, the red "??" means that a file isn't tracked yet by git.

After we  add a file that wasn't being tracked it appears with a green "A", this means that we are adding this file to the commit.

## git diff
This command helps us know what changes have been done before moving our files to the stage.

### git diff --stage
When we use this command we are able to see the changes of the files that are already in the stage

## git log
Shows all the information about the commits that have been made to the open repo.

### git log --oneline
This command shows all the commit titles with their own hash code that identifies the commit.

# Git branches
Usually when we initialize a repo the branch in wich we are is the main branch.
To check it out we use the command `git branch`.

## Create a new branch
To create a new branch we use the command `git checkout -b <branch-name>`
This command automatically creates a new branch with the given name and also moves us to that branch.

## git checkout `<branch>`
This command is useful to switch between the different branches that our repo could have.

## git merge `<branch>`
This command tries to unify the actual branch (the one you are in) and the branch with the given name.

## Delete branch

Once we've finished our features or fixes in a branch, and as they usually aren't reused we should  delete them.
That's done whith the command `git branch -d <branch-name>`
