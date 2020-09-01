# git-cheat-sheet

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

## Git
### Git Install
To install git you have to downlad it from there Web site or simply click here [install git](https://git-scm.com/downloads), follow the instructions to install it on your OS.
To test if the git is correctly installed type in the terminal:

```git```

or

```git --version```

### Git configurations
To see your git configurations type in the terminal ```git config --list``` and then a list will be showen. the most important configuration is *name* and *email*.

To change the name type in the terminal: ```git config --globale user.name "<YOUR_NAME>"``` or to change the email: 

```git config --globale user.email "<YOUR_NAME>"```

### Create Git Project
To create a git project we have to tell git in which directory is our project, and tell git to manage this folder by intilizing a git project.
To do that we go to the project folder and open it in the terminal then we type this command: ```git init```

After initilize the git project, a ```.git/``` folder will be added (it will be hidden). This folder is a git repository for this project, and a Git repository tracks all changes made to files in your project, building a history over time. Meaning, if you delete the .git/ folder, then you delete your project’s history.

### Git workflow
The Git prject has always a three areas: 
 * Working directory: is where our files were just created
 * staging area: is where we add all changed files. In this area all files will be tracked
 * a repository
 
When we make a new file in the git project or make a changes to a file in the project, it will not be direct tracked, we have to tell git to track and decument all changes in this file, to do that we have to add this file to the stage area by typing ```git add <FILE_NAME>```.

After adding the file to the stage area, you have to commit all changes in all files that you hav done, and it is always recommended to add message with the commit using this command: ```git commit -m "YOUR_MESSAGE"```.

After *commit* all changes Git will automaticlly move all changes to the repository (third area) and save them.

To compaire between files, commits or fils in stage area and file in the repository, use this command ```git diff``` 

To see all files in the repository, use this command: ```git rm <FILENAME>```


 ## Remote version control system
Is a system based on version control system but with the ability to do all git stuff (save, add and commit changing) online, and to make the work on a project in team easier.

As example we will talk about GitHub RVCS (but it is the same if you work on GitLab or any other RVCS)

### GitHub
Is where the people make there software 
#### make a ripository
##### New Project
To make a ripostory on GitHub you have two ways:
 1. do it online on the GitHub website by following the instructions.
 2. do it localy using the terminal:
  * make a new folder with name of the project (e.g. NewProject)
  * open the folder in the terminal
  * type ```git init```
  Now the git repository of the project (NweProject) has been created, but there is no file in the project/repository (on your GitHub account you will see just the repository name but nothing inside it) A readMe.md file is always recommended to be the first added file, so let's add it (once again in the terminal):
  * ```touch readMe.md```
  * ```git add readMe.md```
  * ```git commit -m "First Commit"```
  * ```remote add origin https://github.com/<USERNAME>/<RepositoryName>.git``` add this folder to the origin
  * ```git push -u origin master``` push this origin to the master branch (Usually in this step git will ask you for the GitHub username and password)
  Now the repository is created and readMe.md is added and now the project is ready to add files, directory, ect....
   
  
##### Existing Folder/Project
* open the folder/project in the terminal and then type
*  ```remote add origin https://github.com/<USERNAME>/<RepositoryName>.git```
* ```git push -u origin master```
  

#### Branches
* The Branch is a copy of the project, will be used to develop a feature  or solve a problem without effect the whole project. 
* A new created repository has at first one branch called *master*, every commit and push you do it will be done in the master branch.
* A new branch can be splited from the master branch and developed separatly from the main project.
* A branch can be created from any other branch.
* A remote branch: is the online branch (e.g. Branch_A on GitHub)
* A local branch: is the branch that you have it on your local desktop (Branch_A on your computer)
* To create a branch (Branch_B) from another branch (Branch_A):
  * go to the Branch_A (chackou to the Branch_A) by typing in the terminal: ```git checkout Branch_A```
  * make the Branch_B by typing: ```git checkout -b Branch_B```
* If you have an old version of the remote branch and you need to get the last version to your local branch, you have to pull: ```git pull```
* After you finish developing the Branch_B you have to merge it into the parent branch (Branch_A):
  * fetch the branch or get all update to out branches (without getting the changes to the local branches):```git fetch```
  * check if the branches have received new changes on the remote: ```git branch -va```
    * if a branch has received new changes on the remote, you have to pull this changes to your local branch: ```git chechout Branch_A``` and then ```git pull```
  * now is every thing ready to be merged
  * checkout to the Branch_A:```git checkout Branch_A```
  * merge the Branch_B into Branch_A: ```git merge Branch_B```
  
 

  
### Common Git Commands
* ```git remote```: to see the main repository you connected with on GitHub (called as origin)
* ```git remote -v```: to see the link of the repository on GitHub
* ```ssh-keygen -t rsa -b 4096 -C "<YOUR_EMAIL>"```: to generate SSH key
* ```ssh-add <SSH_FILE_NAME>```: add ssh key (Sometimes you could not connect to the authentication agent, so you have to type this command: eval $(ssh-agent -s))
* ``` git init```: Turn an existing directory into a git repository
* ```git clone <Repository_link>```: Clone (download) a repository that already exists on GitHub, including all of the files, branches, and commits
* ``` git fetch``` :Downloads all history from the remote tracking branches
* ``` git branch [branch-name]```: Creates a new branch
* ``` git checkout [branch-name]```: Switches to the specified branch and updates the working directory
* ``` git checkout -b [branch-name]```: create a new branch and switches to the specified branch
* ``` git merge [branch]```: Combines the specified branch’s history into the current branch. This is usually done in pull requests, but is an important Git operation.
* ``` git branch -d [branch-name]```: Deletes the specified branch
* ``` git merge```: Combines remote tracking branch into current local branch
* ``` git push```: Uploads all local branch commits to GitHub
* ``` git pull```: Updates your current local working branch with all new commits from the corresponding remote branch on GitHub. git pull is a combination of git fetch and git merge 





*based on*: 
* [Git & GitHub Crash Course for Absolute Beginners [GitHub it]](https://www.udemy.com/course/git-and-github-crash-course/)
* [Git Cheat Sheet](https://github.github.com/training-kit/downloads/github-git-cheat-sheet.pdf)
