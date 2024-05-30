# Git Cheat Sheet

## What is the version control system(VCS)?
The version control system allows the developer to make many versions of there application, they can save every step of there work in a version so they can go back to any step they want and get it again.

This system helps the developers to save there works and and make them sure that whatever the changes are, they can go back to the last step and get the last version.

*Example*: A developer works on project, and this project works perfectly, the developer has an amazing idea to add an new feature to his project. He added it, but then he realized that all changes he done crache the project. If the developer does not work with VCS then he has to delete all the new changes be him selve and it can be hard and difficult. But with VCS he can get the last version of the project (The project before adding the new feature) with one command.

The VCS helps also the developers when they work on a big project together, the VCS allows to split the project so every developer can work on his own part of the project and finaly with one merge the developers can get there project as onw piece again.

*Summery* 
The VCS allowes to:
* keep Versions of every file and directory
* Document all changes with descriptive message
* Display differences

On of the most famous VCS is ***git***.

## Git Install
To install git you have to downlad it from there Web site or simply click here [install git](https://git-scm.com/downloads), follow the instructions to install it on your OS.
To test if the git is correctly installed type in the terminal:

```git```

or

```git --version```


## Configuration
`git config --global user.name "Your Name"`: Set your name for Git commits.

`git config --global user.email "your.email@example.com"`: Set your email for Git commits.

## Creating Repositories
`git init`: Initialize a new Git repository in the current directory.

`git clone [url]`: Clone a repository from a remote source (e.g., GitHub).

## Basic Snapshotting
`git status`: Show the status of your working directory and staging area.

`git add [file]`: Add a file to the staging area.

`git add .`: Add all changes in the current directory to the staging area.

`git commit -m "Commit message"`: Commit the staged changes with a descriptive message.

`git commit -am "Commit message"`: Stage and commit all tracked files with a single command.

## Branching and Merging
`git branch`: List all local branches in the repository.

`git branch [branch-name]`: Create a new branch.

`git checkout [branch-name]: Switch to the specified branch.

`git checkout -b [branch-name]`: Create and switch to a new branch.

`git merge [branch-name]`: Merge the specified branch into the current branch.

`git branch -d [branch-name]`: Delete the specified branch.

## Remote Repositories
`git remote -v`: Show the URLs of remote repositories.

`git remote add [name] [url]`: Add a new remote repository.

`git fetch [remote]`: Fetch changes from the remote repository without merging.

`git pull [remote]`: Fetch and merge changes from the remote repository.

`git push [remote] [branch]`: Push changes to the remote repository.

## Inspecting and Comparing
`git log`: Show the commit history for the current branch.

`git log --oneline`: Show the commit history with a summary (one line per commit).

`git diff`: Show changes between working directory and staging area.

`git diff --staged`: Show changes between staging area and last commit.

`git show [commit]`: Show information about a specific commit.

## Undoing Changes
`git reset [file]`: Unstage a file while retaining changes in the working directory.

`git checkout -- [file]`: Discard changes in the working directory.

`git revert [commit]`: Create a new commit that undoes the changes from a previous commit.

`git reset --hard [commit]`: Reset the working directory and staging area to a specific commit.

## Stashing
`git stash`: Stash the changes in the working directory for later use.

`git stash list`: List all stashed changes.

`git stash apply`: Apply the most recently stashed changes.

`git stash drop`: Remove the most recently stashed changes.

## Tagging
`git tag`: List all tags in the repository.

`git tag [tag-name]`: Create a new tag.

`git push [remote] [tag-name]`: Push a specific tag to the remote repository.

## Useful Aliases
`git config --global alias.st status`: Create an alias for git status.

`git config --global alias.ci commit`: Create an alias for git commit.

`git config --global alias.co checkout`: Create an alias for git checkout.

`git config --global alias.br branch`: Create an alias for git branch.

