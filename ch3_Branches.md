# Chapter 3: Branches

```shell
git branch ch3
git checkout ch3

# The above two lines equals to:
git checkout -b ch3

# Check which branch you are at:
git branch

git commit -am "Add chapter 3"
```

_This is what you will see if merge conflict arises:_

```
<<<<<<< HEAD
git checkout master
git merge ch3
=======
git conflict!
git conflict!!

> > > > > > > ch3
```

_After dealing with the conflicts, do_

```shell
git add .
git commit -m "Merge ch3 into master, w/ resolved conflicts"
```
