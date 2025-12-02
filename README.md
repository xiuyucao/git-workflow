# Git Workflow

## 0 Configure Git
Configure git by running the following commands in the terminal
```
git config --global user.name "John Smith"
git config --global user.email "johnsmith@gmail.com"
git config --global credential.helper "store --file ~/.git-credentails"
```
Git will save the credentails in the location you assign (i.e., "~/.git-credentails"). You can customize this location.

## 1 Create Repository in Github
## 2 Clone the repo to local
* Basic terminal codes
  * `pwd` --> print working directory
  * `cd Users/xycao/download` --> change working directory
  * `ls`  --> list the files of the working directory
    * `ls -a`  --> show all (include hidden files)
  * `git clone https://github.com/xiuyucao/git-workflow.git`  --> clone the repository to local

## 3 cd to the working directory
* working directory setup
  * set `.gitignore` to ignore files you do not want to do version control

## 4 Create R project
File --> New project --> existing --> choose your working directory

## 5 Organize and working in your working directory
I recommend organizing in the structure of `scripts/` and `data/`

## 6 Git
![](images/git_chart.png)

* `git status -s`  --> check the status
* `git add [file]`  --> add the file to the staging area
  * `git add .` --> add all the files
  * `git reset <file>` --> remove the added file from the stage
* `git commit -m "[commit message]"`  --> commit the change to git
* `git log` --> show all the history git commits
  * `git log --oneline`
  
## 7 Push local commmits to remote (Github)
* `git push`

## 8 Branches
To better organize the project, it is good practice to use branches.

Check the branches of the repository by doing `git branch`

The main (some places called master) branch is the stable version of the code. We do not want to try new feature on this branch. That's why we need another branch. The basic idea is we create a branch which is an isolated developing environment and try new features we like. If satisfying, we merge the branch. This is also very helpful when 2 developers working on the project at the same time.

* Check branches: `git branch`
  * `git branch -a` - show all branches including remote ones
* Create a branch: `git branch branch1`
* Switch to a branch: `git checkout branch1`
  * or can create and switch at the same time: `git checkout -b branch1`
* Merging branches
  * First switch to the branch we want to merge other branhes into
  * `git merge branch1`
* Delete a branch: first switch to another branch, then:
  * `git branch -d branch1` - for merged branches
  * `git branch -D branch1` - regardless of the merge status

## APP. Other useful codes
* `git reset --hard HEAD` --> resets the current branch to the latest commit (HEAD) 
