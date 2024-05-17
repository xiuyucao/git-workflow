# Git Workflow

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
![](data/git_chart.png){width=50%}

* `git status -s`  --> check the status
* `git add [file]`  --> add the file to the staging area
  * `git add .` --> add all the files
* `git commit -m "[commit message]"`  --> commit the change to git
* `git log` --> show all the history git commits
  * `git log --oneline`

