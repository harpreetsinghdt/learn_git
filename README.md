# Learn Git

> Initialize Git on the folder

```
git init
```

> Check git verion (git version 2.37.1.windows.1)

```
git --version
```

## Configure Git

> Let Git know who you are as each Git commit uses this information

```
git config --global user.name "Harpreet Singh"
```

```
git config --global user.email "harpreetsinghdt@gmail.com"
```

> Check current status of repository

```
git status
```

```
git status --short
```

## Adding File To Staging Area

> Move single file to staging area

```
git add filename.txt
```

> Move all files to staging area

```
git add .
```

```
git add --a
```

```
git commit -m "First Commit"
```

```
git restore --staged filename.txt
```

```
git checkout -- filename.txt
```

```
git checkout -f

```

## Checking Git Log

> Show commit history, press q to exit from history

```
git log
```

```
git log -p
```

> Show n number of log

```
git log -p -3
```

> Show short summary, addition, deletion

```
git log --stat
```

> Show log with format

```
git log --pretty
```

> Show all commits in one line

```
git log --pretty=oneline
```

> Show commit, author, message

```
git log --pretty=short
```

> Show commit, author, commitor, message

```
git log --pretty=full
```

> Show previous n.years/months/weeks/days

```
git log --since=2.days
```

> Show formatted output as abbreviated commit hash -- author name

```
git log --pretty=format"%h -- %an"
```

> Show formatted output as abbreviated commit hash -- author email

```
git log --pretty=format"%h -- %ae"
```

> It will open vim editor to change commit message for that file and will update the new commit message etc

```
git commit --amend
```

## Create New File & directory

> Make a new directory(folder) & change control to new directory

```
mkdir myproject
cd myproject
```

> Create new file at working directory

```
touch index.html
```

> Press i for insert text, esc for stop insert mode, :wq for save and exit file)

```
vim index.html
```

> Also can edit file in notepad

```
notepad index.html
```

> Compares working directory to staging area

```
git diff
```

> Compares previous commit to current staging area

```
git diff --staged
```

> Direct commit, only commit tracked files and skip untracked files

```
git commit -a -m "direct commit only tracked files and skip untracked files"
```

> Delete a file

```
git rm manager.txt
```

> Rename file

```
git mv school.php myschool.php
```

> Remove tracked file from git cache after adding to ignore but before it was tracked by git

```
git rm --cached manager.txt
```

> Remove currect directory which is currently a git directory - git will no more tracking files from this folder

```
rm -rf .git
```

## Git Clone from remote

> Cloning / making local copy of repository from github with same name as on github

```
git clone https://github.com/harpreetsinghdt/javascript-code.git
```

> Cloning/ making local copy of repository from github with new name as mentioned after repository url

```
git clone https://github.com/harpreetsinghdt/javascript-code.git jscode
```

## Git Add Remote Repo

```
git remote add origin https://github.com/harpreetsinghdt/codehome.git
```

```
git branch -M main
```

```
git push -u origin main
```

> Check remote directory name

```
git remote
```

> Tells pull & push origin (url)

```
git remote -v
```

## Alias for commands

```
git config --global alias.st status
git st
```

```
git config --global alias.ci commit
git ci
```

```
git config --global alias.unstage 'restore --staged --'
git unstage filename.txt
```

```
git config --global alias.last 'log -p -1'
git last
```

## Git Branches & Merge

> Check all existing branches

```
git branch
```

> Show branches with last commit hash & message

```
git branch -v
```

> Show all branches which are already merged, could be deleted

```
git branch --merged
```

> Show all branches which are not merged yet, shouldn't be deleted

```
git branch --no-merged
```

> To delete a branch, it will give error if branch (develop) is not merged, to force delete use -D

```
git branch -d develop
```

```
git branch --delete <branchname>
```

> Merge branch develop to msater

```
git merge develop
```

> Merge abort branch

```
git merge --abort
```

> Add new branch if not exists and shift to that new branch

```
git checkout -b develop
```

> Shift to another branch

```
git checkout -b develop
```

> To push the current branch and set the remote as upstream

```
git push --set-upstream origin master
```

> To push a local branch to remote branch

```
git push origin develop
```

> Delete a remote branch

```
git push -d origin develop
```

> The upstream branch of your current branch does not match
> the name of your current branch. To push to the upstream branch
> on the remote, use

```
git push origin HEAD:main
```

> To push to the branch of the same name on the remote, use

```
git push origin HEAD
```

> To choose either option permanently, see push.default in 'git help config'.

> To avoid automatically configuring upstream branches when their name doesn't match the local branch, see option 'simple' of branch.autoSetupMerge in 'git help config'.

## Remove the files from git's index

> If you committed node_modules before they were added to the gitignore file, git is going to notice changes each time you add and install a new package, when the node_modules directory changes. So we need one more step to seal the deal.

```
git rm -r --cached node_modules
```

> Now we need to commit our changes. This commit will include our .gitignore addition from the previous step.

```
git commit -m "Remove and ignore node_modules"
```

## Official Tutorials

> _[GitHub Tutorial](https://git-scm.com/docs/gittutorial)_

> _[GitHub Docs](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#headings)_

> _[Generating a new SSH key and adding it to the ssh-agent](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)_

```
 ssh-keygen -t ed25519 -C "harpreetsinghdt@gmail.com"
 eval "$(ssh-agent -s)"
 ssh-add ~/.ssh/id_ed25519
```

> _[Adding a new SSH key to your GitHub account](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account)_

```
 tail ~/.ssh/id_ed25519.pub
```

> [Configure and use aliases in ZSH](https://linuxhint.com/configure-use-aliases-zsh/)