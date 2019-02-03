# Chapter 5: History

```shell
# Show commit history including Date, Author, etc.:
git log

# Show commit ID and message:
git log --pretty=oneline

# Show shortened commit ID and message:
git log --oneline

# Show commits in branch-a that aren't in branch-b
git log --oneline branch-a..branch-b
git log --oneline ch4..master
git log --oneline master..origin/master # works with remotes too
```
