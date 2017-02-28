## Rename current file
```bash
:NERDTreeFind
m
```


## Prettify JSON file
```bash
:%!python -m json.tool
```


## Swap panes
```
Ctrl+W [HJKL]
```


## Re-select last selected visual area
```
gv
```


## Replace last occurrence of character(s) in a line
```
:%s/.*\zsone/two/
```


## Remove trailing whitespace
```
:%s/\s\+$//e
```


## Replace word under cursor with the last yanked value
```
vep
```


## Delete all lines matching a pattern
```
:g/pattern/d
```


## Keep all lines matching a pattern
```
:v/pattern/d
```


## Split lines based on a delimiter
```
:%s/,/,\r/
```


## Replace all occureneces of last searched pattern
```
:%s//<new value>/g
```


## Join lines without space
```
gJ
```
