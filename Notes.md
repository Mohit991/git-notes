# Git
## Basic Linux Commands
`ls` - Lists all the files in your current directory.  
`mkdir <folder_name>` - Creates a new folder called folder_name in your directory.  
`cd <folder_name>` - Moves you to a folder called folder_name in your directory.  

## Basic Git Commands
`git -v` - Git version  
`git config --global user.name "<name>"` - Setting the name of the user.  
`git config --global user.email "<email>"` - Setting the email of the user.  
`git config --global core.editor "code --wait"` - Setting default code editor.  
`git config --global -e` - Opens the .gitconfig file using below default code editor. This file contains git configs.  
`git init` - Initilizes a repo as a git repo. Files in this repo can now be tracked by git.  
`git status` - Provies status of you git repo. Branch, commits, tracked and untracked files etc.  
`git add <file_name/s>` or `git add .` - Adds file/s into the staging area. `git add .` adds all the untracked files to the staging area.  
`git commit -m "<commit_message>"` - Commit changes to git. -m is the message flag.  
`git commit` - Opens the default code editor so you can write a longer commit message.  
`git restore --staged <file_name/s>` - Removes file/s from the staging area. These files become untracked again.  
`git log` - Shows git commit history.  This commad will show you previous commits. It will show each commits IDs, author, date and commit message.  
`git reset <commit_id>` - Restores the project to as it was on the given commit_id. All the commits made after the given commit_id will be removed from the git history. All the files or changes which were done after this commit, they will be moved to the unstaged area.  
`git stash` - When you do not want to commit some changes but also do not want to lose these changes, you can use this command. 
It takes your uncommitted changes (both staged and unstaged), saves them away for later use, and then reverts them from your working copy.  
`git stash clear` - Clears all the stashed changes. You cannot get those changes back at all.  
`git stash pop` - Re-applies the previously stashed changes.  

## Git Remote Repo Commands
`git remote add origin <github_repo_link>` - Adds the github repo to your local project. You can now sync your code with this github repo by using pull and push. From this github repo, other people can clone and make changes to your code as well. **origin** is the name of the github repo.  
By default, all guthub repos are named origin.  
`git push origin main` - It will push your changes to the orgin repo. It will push to the main branch.  
So, push means sending the changes to a remote repo, origin is the name of the repo and master is the name of the branch.  
`git clone <URL>` - Downloads the repo folder into your machine.  

## Branches
Whenever you work on a new feature or on a bug, you should always create a new branch.  
**You should never commit on the main branch**  
`git branch <branch_name>` - Creating a new branch called branch_name.  
`git checkout <branch_name>` - Moves your head to the branch called branch_name.  
**feature branch** - A feature branch is a copy of the main codebase in a version control system (VCS) that developers use to work on a new feature, enhancement, or bug fix.
Feature branches are a popular strategy for open-source projects because they allow developers to work independently without interfering with each other's work or the main codebase.  
`head` - This is a pointer which will point to a branch. All the commits will be done on head. If your head is pointing to the main branch then commits will be done on the main branch and if it is pointing to a feature branch then changes will be done on the feature branch.  
`git merge <branch_name>` - Merges your branch called branch_name with the main/master branch.  
`git push origin <branch_name>` - Pushed your commits/changes to the branch called branch_name. All the commits you did will be added to this branch.  
We use a popular variation of this called `git push origin master` to push changes into the master branch.  
`git fetch <remote>` - Fetch all of the branches from the repository. This also downloads all of the required commits and files from the other repository.  
`git fetch <remote> <branch>` - Same as the above command, but only fetch the specified branch.  
eg. `git fetch origin main`.  
`git fetch --all` - A power move which fetches all registered remotes and their branches.  
`git pull <remote> <branch>` - Fetch and merge changes from a remote repository into your local repository.  
<remote> is the name of the remote repository (e.g., origin).  
<branch> The name of the branch you want to pull from (e.g., main).
eg. `git pull origin main`.  


**Flow** - First do a pull, then do push. 

## Merge Conflicts
A merge conflict occurs when two or more developers make competing changes to the same file or line of code, or when one developer deletes a file while another is modifying it.  
Which changes should be taken while merging.  

## Forking
There is a project on someone's github repo. I want to make changes to this project. But I dont have access to this account. No one without access can make changes to a project in someone'e else's repo without access.  
So, we create a copy of this project in our own account. This is called **forking**. Now, you can make changes to this project.  
From where you forked this project that is known as upstream URL.  
`git remote add upstream <URL>` - This will fork the repo on the URL to your account.  
## Pull Request (PR)
A pull request is a way for developers to propose changes to a project, get feedback, and merge those changes into the main codebase.  
You made some changes in your branch, now you want to merge these changes into the master/main branch. You create a PR to do that.  
PRs will also be created when you fork a project. Make changes in fork and now want to merge these changes to the main project's main branch.  
_Note: You can only have one PR per branch. If you create a PR and after that make a commit, you commit will be added to the same PR._  

## Workflow  
Create a new branch for your feature or bug. Make commits to this branch, as many as you want. After you are done, create a PR. Do this for every new feature or bug. When the PR is completed, your changes will be merged into the main branch.  
