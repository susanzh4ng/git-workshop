# Git Workshop


### Miscellaneous ###
* Need to make sure you are in the correct folder before you start writing any git commands in your terminal/command line
* **Staging area** the “area” where Git puts all of the changes we have selected using “git add”
* **Working area** the “area” where all the code files we are currently working on (the files that are being changed) goes
* **Local repository** the collection of code for your project located on your own computer
* **Remote repository** the collection of code for your project located on GitHub/online
* **.gitignore** file that holds essential, but secret, variables to your code that will not be published to GitHub
* `cd [newDirectory]` “change directory”
* `cd ..` gets you out of your current directory
* `q` gets you out of a terminal response
* `code .` opens your file in your IDE
* `clear` clears terminal
* `ls` see which files make up the repo


### Basic Git Commands ###
**(#.) steps needed to push code to GitHub**
* `status` check to see which files are being tracked or need to be commited
* `init` establishes that your current code will be initiated in version history; Git now can start tracking all of the files in the directory for any changes; not needed when cloning a repository
* `clone` bring a repo down from the internet (remote repository like Github) to your local machine
* `git log --all --graph` outputs commit history, including the commit hash that you would need to view and restore back to previous commits
* `add .` ***(1.)*** chooses all the files in your current directory to be included in in your newest code version; adds all files to the staging area
* `git reset [fileOrDirectory]` chooses file(s) to take away from the staging area, and to be put back into the working area; same arguments as “add”
* `commit -m "[descriptiveMessage]"` ***(2.)*** create a version in your repository’s version history
* `git commit -m “[descriptiveMessage]” –amend` edit previous commit
* `git checkout [commitHash] .` all files are being restored to what it was at the prior commit; restore commits after “add” but before “commit”
* `push` ***(3.)*** pushes new commits onto GitHub
	* `push origin master` pushes your changes to master branch
	* `push -u origin [anotherBranch]` sets up stream so that pushing to anotherBranch is the default
* `pull` pull changes down from the remote repo to your local machine
* `git rm -rf .git` completely removes Git from your project; no longer has access to the Git repository


### Git Branching ###
* `git branch` see the branches that make up the repo
* `git checkout -b [new-branch]` creates new branch
* `git checkout [existing-branch]` switches you to work on another branch
* `git diff [another-branch]` see how another-branch differs from the branch you are currently on
* `git branch -d [merged-branch]` deletes branch; only use if the branch has already been merged
* ***Merging Code:***
* When you merge two branches together, the result will go on the branch that you are currently working on
* ***(1.)*** `git merge [featureBranch] -m “[message]”` merging featureBranch’s code with masterBranch’s code; acts as a commit
	* **Merge Conflicts:**
		* after `git merge`, you might experience merge conflicts; in your IDE, simply delete the line of code that you do not want, and then “add .” and “merge”
		* VS Code allows you to manage merge conflicts within the IDE's terminal, BUT easiest way is to resolve it within GitHub's interface


### How to initialize a repository remotely ###
* make sure you are in the directory that you want the local repository to be located
* `git clone [respositoryURL] [optionalDirectoryName]` copies over the remote repository to your computer
* `git status` check to see if on master branch
* `git add .` adds files to staging area
* `git commit -m "[message]" `
* `git push origin master` update all of the remote tracking branches to the current state in GitHub
* `git fetch` update all of the remote tracking branches to the current state in GitHub
* `git pull origin [branch]` copies over the code from a remote repository; updating your computer’s code with what is on GitHub


### How to initialize a repository locally ###
* Create the folder and files in VS Code
* `git init` initializes empty Git repository
* `git status` check to see if on master branch
* `git add .` adds files to staging area
* `git commit -m "[message]" `
* Create repo (same name as the VS Code folder's name) in GitHub
* ` git remote add origin [repositoryURL]` adds a link between the local and remote repositories
	* `git remote remove origin` removes the link between the local and remote respositories 
* `git remote -v` gives details on your project’s remote repository
* `git push origin master`


!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!The Test to See if README updates in new Branch!!!!!!!!!!!!!!!