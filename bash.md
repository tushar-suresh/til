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


## Restart SSH agent
```bash
eval `ssh-agent -s`
```


## Copy files from s3 using wildcards
```bash
aws s3 cp s3://<bucket-name> <local-destination-dir> --recursive --exclude "*" --include "<wildcard>"
```


## Clear memory cache
```bash
sync && echo 3 | sudo tee /proc/sys/vm/drop_caches
```


## Rename extensions of multiple files
```
find . -name '*.yml' -exec sh -c 'mv "$0" "${0%.yml}.yaml"' {} \;
```
