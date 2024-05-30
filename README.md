# Git Cheat Sheet - Commands and Tricks

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

## Commands

### Configuration
`git config --global user.name "Your Name"`: Set your name for Git commits.

`git config --global user.email "your.email@example.com"`: Set your email for Git commits.

### Creating Repositories
`git init`: Initialize a new Git repository in the current directory.

`git clone [url]`: Clone a repository from a remote source (e.g., GitHub).

### Basic Snapshotting
`git status`: Show the status of your working directory and staging area.

`git add [file]`: Add a file to the staging area.

`git add .`: Add all changes in the current directory to the staging area.

`git commit -m "Commit message"`: Commit the staged changes with a descriptive message.

`git commit -am "Commit message"`: Stage and commit all tracked files with a single command.

### Branching and Merging
`git branch`: List all local branches in the repository.

`git branch [branch-name]`: Create a new branch.

`git checkout [branch-name]: Switch to the specified branch.

`git checkout -b [branch-name]`: Create and switch to a new branch.

`git merge [branch-name]`: Merge the specified branch into the current branch.

`git branch -d [branch-name]`: Delete the specified branch.

### Remote Repositories
`git remote -v`: Show the URLs of remote repositories.

`git remote add [name] [url]`: Add a new remote repository.

`git fetch [remote]`: Fetch changes from the remote repository without merging.

`git pull [remote]`: Fetch and merge changes from the remote repository.

`git push [remote] [branch]`: Push changes to the remote repository.

### Inspecting and Comparing
`git log`: Show the commit history for the current branch.

`git log --oneline`: Show the commit history with a summary (one line per commit).

`git diff`: Show changes between working directory and staging area.

`git diff --staged`: Show changes between staging area and last commit.

`git show [commit]`: Show information about a specific commit.

### Undoing Changes
`git reset [file]`: Unstage a file while retaining changes in the working directory.

`git checkout -- [file]`: Discard changes in the working directory.

`git revert [commit]`: Create a new commit that undoes the changes from a previous commit.

`git reset --hard [commit]`: Reset the working directory and staging area to a specific commit.

### Stashing
`git stash`: Stash the changes in the working directory for later use.

`git stash list`: List all stashed changes.

`git stash apply`: Apply the most recently stashed changes.

`git stash drop`: Remove the most recently stashed changes.

### Tagging
`git tag`: List all tags in the repository.

`git tag [tag-name]`: Create a new tag.

`git push [remote] [tag-name]`: Push a specific tag to the remote repository.

### Useful Aliases
`git config --global alias.st status`: Create an alias for git status.

`git config --global alias.ci commit`: Create an alias for git commit.

`git config --global alias.co checkout`: Create an alias for git checkout.

`git config --global alias.br branch`: Create an alias for git branch.

## Git Tricks
### 1. Undoing the Last Commit
If you accidentally committed something and want to undo it:

`git reset --soft HEAD~1`: This command undoes the last commit but keeps the changes staged.
`git reset --hard HEAD~1`: This command undoes the last commit and discards the changes.

### 2. Amending the Last Commit
If you need to make changes to the last commit:

`git commit --amend`: This command allows you to modify the previous commit, including the commit message.

### 3. Stashing Changes
If you need to temporarily save changes without committing them:

`git stash`: Stashes your current changes.
`git stash pop`: Applies the stashed changes back to your working directory.

### 4. Viewing a Pretty Log
For a more readable and graphical log:

`git log --oneline --graph --decorate --all`: Displays a condensed and visual representation of the commit history.

### 5. Checking Out a Previous Commit
To check out a specific commit without creating a new branch:

`git checkout [commit-hash]`: Switches to the specified commit.
`git switch -`: Switches back to the previous branch you were working on.

### 6. Creating Aliases
Create shortcuts for frequently used commands:

`git config --global alias.co checkout`:Creates an alias for git checkout.
`git config --global alias.br branch`: Creates an alias for git branch.
`git config --global alias.ci commit`: Creates an alias for git commit.
`git config --global alias.st status`: Creates an alias for git status.

### 7. Interactive Rebase
To clean up your commit history:

`git rebase -i HEAD~n`: Allows you to interactively rebase the last n commits.

### 8. Blaming a File
To find out who made changes to a file:

`git blame [file]`: Shows who last modified each line of a file.

### 9. Ignoring Untracked Files
To temporarily ignore untracked files:

`git clean -fd`: Removes untracked files and directories.
`git clean -fdn`: Shows what would be removed without actually doing it.

### 10. Squashing Commits
To combine multiple commits into one:

`git rebase -i HEAD~n`: Mark commits as squash or s to merge them into a single commit.

### 11. Showing Changes in a Branch
To see what has changed in a branch compared to another branch:

`git diff [branch1]..[branch2]`: Shows differences between the two branches.

### 12. Bisecting
To find the commit that introduced a bug:

`git bisect start`: Starts the bisect session.
`git bisect bad`: Marks the current commit as bad.
`git bisect good [commit]`: Marks the specified commit as good.
`git bisect reset`: Ends the bisect session and returns to the original branch.

### 13. Resetting a Branch to a Remote State
To match a local branch to a remote branch:

`git fetch origin`: Fetches the latest changes from the remote repository.
`git reset --hard origin/[branch]`: Resets the local branch to match the remote branch.

### 14. Cherry-Picking Commits
To apply specific commits from one branch to another:

`git cherry-pick [commit]`: Applies the specified commit to the current branch.

### 15. Auto-Correcting Commands
If you mistype a Git command:

`git config --global help.autocorrect 1`: Auto-corrects typos in Git commands (with a slight delay).

