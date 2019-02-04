# Git For Humans

This is a companion repo for me to learn git from _Git For Humans_ by David Demaree.

# Cheat Sheet

## Chapter 2: Basics

```shell
git config --global user.name "Athena Liu"
git config --global user.email "sdathenaliu@gmail.com"

git init

git clone https://somerepo.git

git status
git add README.md
git add .
git commit -m "Initial commit"

git commit -a -m "message"
```

## Chapter 3: Branches

```shell
# Create branch and switch to it:
git branch <branch_name>
git checkout <branch_name>
    # Equally:
git checkout -b <new_branch>

# Check which branch you are at:
git branch

# Merge branch
git checkout master
git merge <branch_name>
```

## Chapter 4: Remotes

```shell
git remote add <name> <url>
git remote add origin https://github.com/XiaoheLiu/git-for-humans.git

git push <remote_name> <branch>
git push origin master
git push -u origin ch4 # Branch ch4 set up to track remote branch ch4 from origin.

git pull <remote_name> <branch>
git pull origin master

git fetch <remote>
git fetch origin
# fetch made a copy of the remote repos by the name of origin/*

git branch --remote # see fetched remote branches
```

## Chapter 5: History

```shell
# Show commit history including Date, Author, etc.:
git log

# Sepcify formatting:
git log --pretty='format:%h -%an: %s' # shortedid, author, message

# Show shortened commit ID and message:
git log --oneline

# Show commits in branch-b that aren't in branch-a
git log --oneline branch-a..branch-b
git log --oneline ch4..master

# Filtering:
git log --author='Athena Liu' --grep='log' --oneline ch5_History.md
    # show commits with author='Athena Liu', message contains 'log', which modifies the ch5_History.md file.

git diff
# Difference between current head and 2 commit before it:
git diff --stat HEAD~2
# Show change of a specific file:
git diff --stat HEAD~10 ch3_Branches.md

# Tagging Commits
git tag [-a] [-m] <tagname> [<commit>]
git tag learn_tagging -a -m "Learn how to tag commits"
    # Delete a tag:
git tag -d <tagname>
    # List of tags:
git tag -l

git checkout <branchname | tagname | commit id>
git checkout ch4
git checkout learn_tagging
git checkout 67e99ff
```
