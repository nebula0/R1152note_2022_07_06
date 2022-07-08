#git_github 

看不懂但能用
[ref](https://cythilya.github.io/2018/05/27/git-merge-and-solve-conflict/)


## rebase

```git
git fetch
git rebase <remote>/<branch>
git push <remote> <branch>
```
等於
```git
git pull —-rebase
git push <remote> <branch>
```

## merge
```git
git pull <remote> <branch>
git push <remote> <branch>
```
等於

```git
git fetch
git merge <remote>/<branch>
git push <remote> <branch>
```