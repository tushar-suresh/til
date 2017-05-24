## Push code to multiple remote repositories
```bash
git remote set-url <remote-name> --add --push origin git://original/repo.git
git remote set-url <remote-name> --add --push origin git://another/repo.git
```


## Speed up git status operations
```bash
sudo git config --system core.untrackedCache true
```
HT https://news.ycombinator.com/item?id=11388479


## See file from a specific commit
```bash
git show REVISION:path/to/file
```


## Reset git branch without checkout
```
git branch -f otherbranch currentbranch
```


## Apply specific files from a stash
```
git checkout stash@{0} -- <filename1> <filename2>
```

### List remote braches by date of last commit
```
git for-each-ref --sort=committerdate refs/heads/ --format='%(HEAD) %(color:yellow)%(refname:short)%(color:reset) - %(color:red)%(objectname:short)%(color:reset) - %(contents:subject) - %(authorname) (%(color:green)%(committerdate:relative)%(color:reset))'
```

### Email the last commit in the current branch
```
git send-email -1

```
