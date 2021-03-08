# Using Git Branches

## Branches
When Git is initialized in a project, the *Main* (or Master) branch are automatically created depending on when the project was created. (Repositories created after October 1, 2020 will have the default as Main)

The Main branch for most projects is used for the code that:

* Works
* Has been tested
* Ready for production

While developing code, Main is not appropriate until you have verified the new code works.

Branches help to not only separate your working code from code ready for production: but are also helpful while working on different features: keeping code for different features separate to make sure they work on their own, before combining and making sure it works with the rest of the code. 

When working with others on the same project: branches also help to separate code the different developers are working on. It allows for everyone to isolate their work while it is in progress and merge it later.


## Commands
| Commands | Description |
| -------- | ----------- |
|` $ git branch `| Lists available branches. This will have an asterisk symbol (*) to notify which branch you are currently on   |
|`$ git branch nameOfBranch`| Creates a new branch “nameOfBranch”. This will only create a branch as an extension of the branch you are currently on. You will remain on the same branch you were when the command was made. |
|`$ git checkout nameOfBranch`| Switches you over to branch “nameOfBranch”. |
|`$ git checkout -b nameOfBranch`| Combines the previous two methods: creates a new branch and moves you over to that new branch. |
|`$ git merge nameOfBranch`| Will combine content of branch specified with the branch you are on. (Move to branch you want content on, then merge content you want to move from another branch) |
|`$ git branch -d nameOfBranch`| Deletes/removes branch specified |

## Merging

When you are working on one component at a time, merging a branch after completing it before creating a new branch: the branch is a direct child of the code it is merging into. 

In many cases you might have multiple branches, and the content from branches have a similar ancestor but do not share the code of the other branches. This will be the case when you are working with other developers on different features for the same project. 

When branches start getting merged, there will become points where the branches share some history, having a point in the same code they came from, but the current code was no longer the code the branch attempting to be merged came from. In this case Git will compare the different versions and combine them.

## Conflicts

Merge conflicts often occur when the same part of a file was changed differently in two branches. 
Your terminal will notify you of the conflict, and if you later need a reminder you can run `$ git status` which will provide information on what was not merged. 

As git is not able to automatically get these to merge, you will have to go in manually to fix or merge the issues. `$ git log` has some options available to help you investigate what changes were made with commits in whichever branch you are on, which can help you find where the conflict is. Different GUIs are also available which can help to provide further details on changes made in a commit. 


## Basic Workflow
*	Initialize git on project if it has not already been 
    >`$ git init`
*	Create a new branch for what you are working on, and switch to it 
    >`$ git checkout -b feature` or `$ git branch feature ` then `$ git checkout feature`
*	Make changes in your new branch and commit them.
*	Switch back to Main 
    >`$ git checkout main`
*	Merge your new content over 
    >`$ git merge feature`
*	Fix any conflicts that arise.
*	Delete branch you no longer need 
    >`$ git branch -d feature`
*	Make sure to also commit to retain your changes after merging.
