# Learn Git

> [!NOTE]
> Initialize Git on the folder

> **git init** 




> Check git verion (git version 2.37.1.windows.1)

**git --version**


**git config --global user.name "Harpreet Singh"**

**git config --global user.email "harpreetsinghdt@gmail.com"**


> Check current status of repository

**git status**


## Adding File To Staging Area

> Move single file to staging area

**git add filename.txt**

>Move all files to staging area

**git add .**

**git add --a**

**git commit -m "First Commit"**

**git restore --staged filename.txt**

**git checkout -- filename.txt**

**git checkout -f**


## Checking Git Log

> Show commit history, press q to exit from history

**git log**

**git log -p**

> Show n number of log

**git log -p -3**

> Show short summary, addition, deletion

**git log --stat**

> Show log with format

**git log --pretty**

> Show all commits in one line

**git log --pretty=oneline**

> Show commit, author, message

**git log --pretty=short**

> Show commit, author, commitor, message

**git log --pretty=full**

> Show previous n.years/months/weeks/days

**git log --since=2.days**

> Show formatted output as abbreviated commit hash -- author name

**git log --pretty=format"%h -- %an"**

> Show formatted output as abbreviated commit hash -- author email

**git log --pretty=format"%h -- %ae"**

> It will open vim editor to change commit message for that file and will update the new commit message etc

**git commit --amend**

## Create New File

> Create new file at working directory

**touch index.html**

> Press i for insert text, esc for stop insert mode, :wq for save and exit file)

**vim index.html**

>  Also can edit file in notepad

**notepad index.html**

> Compares working directory to staging area

**git diff**

> Compares previous commit to current staging area

**git diff --staged**

> Direct commit, only commit tracked files and skip untracked files

**git commit -a -m "direct commit only tracked files and skip untracked files"**

>  Delete a file

**git rm manager.txt**

> Rename file

**git mv school.php myschool.php**

> Remove tracked file from git cache after adding to ignore but before it was tracked by git

**git rm --cached manager.txt**

> Remove currect directory which is currently a git repository - git will no more tracking files from this folder

**rm -rf .git**


## Git Clone from remote

> Cloning / making local copy of repository from github with same name as on github

**git clone https://github.com/harpreetsinghdt/javascript-code.git**

> Cloning/ making local copy of repository from github with new name as mentioned after repository url

**git clone https://github.com/harpreetsinghdt/javascript-code.git jscode**


## Git Add Remote Repo 

**git remote add origin https://github.com/harpreetsinghdt/codehome.git**

**git branch -M main**

**git push -u origin main**

> Check remote directory name

**git remote**

> Tells pull & push path)

**git remote -v**