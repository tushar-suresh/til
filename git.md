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
git for-each-ref --sort=committerdate refs/remotes/<remote-name> --format='%(HEAD) %(color:yellow)%(refname:short)%(color:reset) - %(color:red)%(objectname:short)%(color:reset) - %(contents:subject) - %(authorname) (%(color:green)%(committerdate:relative)%(color:reset))'
```

### Email the last commit in the current branch
```
git send-email -1

```

### Force a 'git stash pop'
```
git stash show -p | git apply && git stash drop

```

### Get current branch
```
git symbolic-ref --short HEAD
```


### Fix/Reset author information in the last n commits
```
git rebase -i YOUR_SHA -x "git commit --amend --reset-author -CHEAD"
```

### Set user given date to commit
```
GIT_COMMITTER_DATE="ISO_FORMAT_DATE" git commit --date="ISO_FORMAT_DATE"
```

### Update author time when amending commit
```
git commit --amend --reset-author
```
