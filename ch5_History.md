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
