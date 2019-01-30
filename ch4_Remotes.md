# Chapter 4: Remotes

`git remote add <name> <url>`

`git remote add origin https://github.com/XiaoheLiu/git-for-humans.git`

_Or for better security, use the ssh protocol instead._

#### git push

`git push <remote_name> <branch>`

`git push origin master`

`git push -u origin ch4`
_Branch ch4 set up to track remote branch ch4 from origin._

#### git pull

`git pull <remote_name> <branch>`

`git pull origin master`

Always pull before you push new changes to avoid merge conflicts.

#### git fetch

`git fetch origin`

`git branch --remote`
_fetch made a copy of the remote repos by the name of origin/\* :_

```
athena@LXH-Mac:~/Desktop/repo/git-for-humans\$ git branch --remote
origin/ch3
origin/ch4
origin/master
```
