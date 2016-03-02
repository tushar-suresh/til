## List files in directory by size
```bash
ls -lShr
```

## Show disk usage of directories
```bash
du -hd 1 | sort -h
```


## Update and prune packages
```bash
sudo apt-get update && sudo apt-get upgrade && sudo apt-get autoremove && sudo apt-get remove && sudo apt-get autoclean && sudo apt-get clean
```


## Refresh executable cache
```bash
hash -r
```
HT https://github.com/ipython/ipython/issues/3018/#issuecomment-14935933


## List all hidden files
```bash
ls -ld .?*
```
