## List files in directory by size
```bash
ls -lShr
```

## Show disk usage of directories
```bash
du -hd 1 | sort -h
```

## Sort files by size (including directories)
```bash
du -a <dir> | sort -n -r
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


## Get size of s3 directory
```bash
aws s3 ls --summarize --human-readable --recursive s3://<bucket-name>/<path>
```


## Clear memory cache
```bash
sync && echo 3 | sudo tee /proc/sys/vm/drop_caches
```


## Rename extensions of multiple files
```
find . -name '*.yml' -exec sh -c 'mv "$0" "${0%.yml}.yaml"' {} \;
```


## Add public key for a given key ID
```
sudo apt-key adv --recv-keys --keyserver keyserver.ubuntu.com "keyID"
```


## Change MySQL user's password
```
SET PASSWORD FOR 'foo'@'localhost' = PASSWORD('bar');
```


## Swap tmux windows
```
C-b : swap-window -s <source-window-no> -t <target-window-no>
```


## Move tmux window to an empty index
```
C-b : move-window -t 0
```


## List tmux windows
```
C-b w
```


## Delete all subdirectories without deleting parent directory
```
find <path-to-parent>/parent -maxdepth 1 -mindepth 1 -type d -exec rm -rf {} \;
```


## Get full path of a file
```
readlink -f file.txt
```


## Name a tmux pane
```
printf '\033]2;%s\033\\' '<pane-title>'
```


## Redirect stdout and stderr to a log file
```
some_command > some_file.log 2>&1
```


## Execute nth command from history
```
!n
```

## Re-load inputrc
```
bind -f ~/.inputrc
```


## GroupBy sum on a column
```
awk '{arr[$1]+=$2} END {for (i in arr) {print i,arr[i]}}
```


## Discard first line of stdin
```
tail -n +2
```


## Force SSH to ask for password
```
ssh -o PubkeyAuthentication=no -o PreferredAuthentications=password user@example.com
```
