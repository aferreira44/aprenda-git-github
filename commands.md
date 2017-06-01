# Como Usar o Git e o GitHub

## Git Bash Config -> [Gist .bash_profile](https://gist.github.com/aferreira44/0bcbd8814371a88da1c9bf99e8fa0801)

1. Only extract all Gist files in the /~ directory.

---

## Principais Comandos

### Show the git version installed

`git --version`

### Config the colors red and green for file changes on git diff

`git config --global color.ui auto`

### Store your passwords in cache to clone HTTPS repositories without type the password everytime

`git config --global credential.helper wincred`

### Set Visual Studio Code as git default text editor

`git config --global core.editor "code -n -w"`

### [Config pushdefault](https://git-scm.com/docs/git-config#git-config-pushdefault)

`git config --global push.default upstream`

### [Config mergeconflictStyle](https://git-scm.com/docs/git-config#git-config-mergeconflictStyle)

`git config --global merge.conflictstyle diff3`

### Resolv errors of longpath lentgh limit on Windows

`git config --system core.longpaths true`

### Init a repository

`git init`

### Add the file filename.txt to staging area

`git add filename.txt`

### Add all the files changed to staging area

`git add -A`

### Add only new and modified files to staging area, without deleted

`git add .`

### Add only modified and deleted files to staging area, without new

`git add -u`

### Reset the changes on filename.txt in staging area

`git reset filename.txt`

Reset the changes on the working directory and the staging area

`git reset --hard`

### Revert a commit, on a wrong branch, for example

`git reset --soft HEAD^`

### Show the repository status and files changed

`git status`

### Add a commit to the repository

- Dica: *[Git Commit Message Style Guide](http://udacity.github.io/git-styleguide/)*

`git commit`

### Add a commit to the repository with a message

`git commit -m "Commit message"`

### Clone a repository

`git clone https://github.com/udacity/asteroids.git`

### Show an history of commits

`git log`

### Show an history of commits with statistics about the files changed

`git log --stat`

### Show an history of commits limited by n numbers of commits

`git log -n 1`

### Show an history of commits of the branch coins

`git log coins`

### Show an history of commits with only one line about each commit

`git log --oneline`

### Show the branches master and coins in a graphic mode

`git log --graph --oneline master coins`

### Show the difference between the working directory and the staging area

`git diff`

### Show the difference between the staging area and the repository

`git diff --staged`

### Show the difference between two commits

`git diff de7e1f1c415394459f8546d13b72366211922509 fb306b6774946601fe471308d09f9594c00d5d59`

### Show the difference between a commit and its father

`git show 4035769377cce96a88d5c1167079e12f30492391`

### Show the actual branches

`git branch`

### Create the branch named feature in the repository

`git branch feature`

### Change HEAD to a specific commit

`git checkout b0678b161fcf74467ed3a63110557e3d6229cfa6`

### Change HEAD to branch master

`git checkout master`

### Create a new branch called new-feature and checkout into it

`git checkout -b new-feature`

### Merge branch coins into master

`git merge master coins`

### Delete a branch called coins

`git branch -d coins`

---

## Resolving merge conflicts

Try to merge new-branch into master

`git merge master new-branch`

1. Resolve what part of code is the correct and save the modified files

```shell
<<<<<<< HEAD
code of my branch
||||||| merged common ancestors
code of original file
=======
code of master branch
>>>>>>> master
```

1. Add the modified files on both branches to the staging area with `git add`

1. Commit the resolved conflicts to confirm the merge with `git commit`

---

## Remote Repositories and GitHub

### Show the remote repositories configured

`git remote`

### Show the remote repositories configured with more information

`git remote -v`

### Configure a remote repository with a public repository on GitHub

`git remote add origin git@github.com:username/repository-name.git`

### Configure the remote repository of a fork called upstream

`git remote add upstream https://github.com/udacity/create-your-own-adventure.git`

### Remove a remote repository

`git remote rm remote-name`

### Send the branch master to a remote repository

`git push origin master`

### Pull the changes of the remote repository and merge into the actual branch

`git pull origin master`

### Get all the changes made on a remote repository branch into a local remote branch (need to make a `git merge` after this to merge into another branch)

`git fetch origin`
`git merge master origin/master`

### GitHub Collaboration

1. Fork the repository on GitHub
1. Clone your repository forked to your local machine
1. Create a new branch
1. Make the changes on files
1. Commit your changes
1. Push your new branch to GitHub
1. Create a pull request on GitHub
1. If it were conflicts:

- git pull origin master
- git checkout pull-branch
- git merge master pull-branch (it will have a conflitc)
- resolve the conflicts on text editor
- git commit
- git push origin pull-branch
- merge the pull request on GitHub

### Native File Comparison Utility

Windows

`FC game_old.js game_new.js`

Unix

`diff -u game_old.js game_new.js`