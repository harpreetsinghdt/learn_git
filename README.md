# Learn Git

> Initialize Git on the folder

```
git init
```

> Check git verion (git version 2.37.1.windows.1)

```it --version```

```it config --global user.name "Harpreet Singh"```

```it config --global user.email "harpreetsinghdt@gmail.com"```

> Check current status of repository

```it status```

## Adding File To Staging Area

> Move single file to staging area

```it add filename.txt```

> Move all files to staging area

```it add .```

```it add --a```

```it commit -m "First Commit"```

```it restore --staged filename.txt```

```it checkout -- filename.txt```

```it checkout -f```

## Checking Git Log

> Show commit history, press q to exit from history

```it log```

```it log -p```

> Show n number of log

```it log -p -3```

> Show short summary, addition, deletion

```it log --stat```

> Show log with format

```it log --pretty```

> Show all commits in one line

```it log --pretty=oneline```

> Show commit, author, message

```it log --pretty=short```

> Show commit, author, commitor, message

```it log --pretty=full```

> Show previous n.years/months/weeks/days

```it log --since=2.days```

> Show formatted output as abbreviated commit hash -- author name

```it log --pretty=format"%h -- %an"```

> Show formatted output as abbreviated commit hash -- author email

```it log --pretty=format"%h -- %ae"```

> It will open vim editor to change commit message for that file and will update the new commit message etc

```it commit --amend```

## Create New File

> Create new file at working directory

```touch index.html```

> Press i for insert text, esc for stop insert mode, :wq for save and exit file)

```vim index.html```

> Also can edit file in notepad

```notepad index.html```

> Compares working directory to staging area

```it diff```

> Compares previous commit to current staging area

```it diff --staged```

> Direct commit, only commit tracked files and skip untracked files

```it commit -a -m "direct commit only tracked files and skip untracked files"```

> Delete a file

```it rm manager.txt```

> Rename file

```it mv school.php myschool.php```

> Remove tracked file from git cache after adding to ignore but before it was tracked by git

```it rm --cached manager.txt```

> Remove currect directory which is currently a git repository - git will no more tracking files from this folder

```rm -rf .git```

## Git Clone from remote

> Cloning / making local copy of repository from github with same name as on github

```it clone https://github.com/harpreetsinghdt/javascript-code.git```

> Cloning/ making local copy of repository from github with new name as mentioned after repository url

```it clone https://github.com/harpreetsinghdt/javascript-code.git jscode```

## Git Add Remote Repo

```it remote add origin https://github.com/harpreetsinghdt/codehome.git```

```it branch -M main```

```it push -u origin main```

> Check remote directory name

```it remote```

> Tells pull & push path)

```it remote -v```
