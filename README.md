# git-cheat-sheet

## What is the version controll system(VCS)?
The version controll system allows the developer to make many versions of there application, they can save every step of there work in a version so they can go back to any step they want and get it again.

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
 
When we make a new file in the git project, it will not be direct tracked, we have to tell git to track and decument all changes in this file, to do that we have to add this file to the stage area by typing ```git add <FILE_NAME>```.

After adding the file to the stage area, you have to commit all changes in all files that you hav done, and it is always recommended to add message with the commit using this command: ```git commit -m "YOUR_MESSAGE"```.

After *commit* all changes Git will automaticlly move all changes to the repository (third area) and save them.

 
