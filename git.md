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
