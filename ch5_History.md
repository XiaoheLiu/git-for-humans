# Chapter 5: History

```shell
# Show commit history including Date, Author, etc.:
git log

# Sepcify formatting:
git log --pretty=oneline
git log --pretty='format:%h -%an: %s' # shortedid, author, message

# Show shortened commit ID and message:
git log --oneline

# Show commits in branch-b that aren't in branch-a
git log --oneline branch-a..branch-b
git log --oneline ch4..master
git log --oneline origin/master..master # works with remotes too

# If currently checked out at <branch-a>, can leave it out in the git log
git checkout branch-a
git log --oneline ..branch-b

# Filtering:
git log --author='Athena Liu' --grep='log' --oneline ch5_History.md
    # show commits with author='Athena Liu', message contains 'log', which modifies the ch5_History.md file.
```

## Configure default text editor

`git config --global core.editor "vim"`

## git diff

`git diff`

Difference between current head and 2 commit before it:
`git diff --stat HEAD~2`

Show change of a specific file:
`git diff --stat HEAD~10 ch3_Branches.md`

## Tagging Commits

`git tag [-a] [-m] <tagname> [-commit>]`

`git tag learn_tagging -a -m "Learn how to tag commits"`

Delete a tag:
`git tag -d <tagname>`

List of tags:
`git tag -l`

## git checkout

```shell
git checkout <branchname | tagname | commit id>

git checkout ch4
git checkout learn_tagging
git checkout 67e99ff
```

If you checkout tag or commit, you will be in the _detached HEAD_ state. You are not supposed to add commit in this case. This serves as a scraching pad.
