# Learn Git

git init (initialize Git on the folder)

git --version (git version 2.37.1.windows.1)

git config --global user.name "Harpreet Singh"

git config --global user.email "harpreetsinghdt@gmail.com"

git status (check current status of repository)

## Adding File To Staging Area

git add .	(to move file to staging area)

git add --a (to move file to staging area)

git add filename.txt (to move file to staging area)

git restore --staged filename.txt ()

git checkout -- filename.txt ()

git checkout -f

git commit -m "First Commit"

## Checking Git Log

git log (show commit history, press q to exit from history)

git log -p (show commit history with changes, press q to exit from history)

git log -p -3 (-n, show with diff)

git log --stat (short summary, addition, deletion)

git log --pretty

git log --pretty=oneline (all commits in one line)

git log --pretty=short (commit, author, detail)

git log --pretty=full (commit, author, commitor, details)

git log --since=2.days (years, months, weeks)

git log --pretty=format"%h -- %an" (format output as abbreviated commit hash -- author name)

git log --pretty=format"%h -- %ae" (format output as abbreviated commit hash -- author email)

git commit --amend (it will open vim editor to change commit msg for that file and will update the new commit msg etc)

## Create New File
touch index.html (create new file)

vim index.html (press i for insert text, esc for stop i mode, :wq for save and exit file)

notepad index.html (also can edit file on notepad)

vim diff (compares working directory to staging area)

vim diff --staged (compares previous commit to current staging area)


git commit -a -m "direct commit only tracked files and skip untracked files"

git rm manager.txt (delete a file)

git mv school.php myschool.php (rename a file)

git rm --cached manager.txt (remove tracked file from git cache after adding to ignore but before it was tracked by git)

rm -rf .git (remove currect directory as git repository - git is no more tracking files from this folder)


## Git Clone from remote

git clone https://github.com/harpreetsinghdt/javascript-code.git (cloning/ making local copy of repository from github with same name as on github)

git clone https://github.com/harpreetsinghdt/javascript-code.git jscode (cloning/ making local copy of repository from github with new name as mentioned after repository url)


## Git Add Remote Repo 

git remote add origin https://github.com/harpreetsinghdt/codehome.git

git branch -M main

git push -u origin main

git remote (tells directory name)

git remote -v (tells pull & push path)
