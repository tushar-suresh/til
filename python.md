## Intersection of a list of lists
```python
set.intersection(*[set(l) for l in ll])
```


## Interweave two lists
```python
chain.from_iterable(zip_longest(x, y, fillvalue=None))
```


## Merge-sort two sorted lists in ascending order
```python
def merge_sorted_lists(list1, list2):
    merged_list = []
    i = j = 0
    while i < len(list1) and j < len(list2):
        if list1[i] < list2[j]:
            merged_list.append(list1[i])
            i += 1
        else:
            merged_list.append(list2[j])
            j += 1

    if i == len(list1):
        merged_list.extend(list2[j:])
    else:
        merged_list.extend(list1[i:])

    return merged_list
```


## Simple flask server
```python
from flask import Flask, jsonify

app = Flask(__name__)
app.config['JSONIFY_PRETTYPRINT_REGULAR'] = False


@app.route('/hello/world')
def search():
    return jsonify(result={'hello': 'world'})


if __name__ == '__main__':
    app.run(host='0.0.0.0', port=8000, debug=True)
```


## Text utils
```python
import string

from nltk.tokenize import RegexpTokenizer
from nltk.corpus import stopwords

punctuation_remover = RegexpTokenizer(r'\w+')
english_stopwords = stopwords.words('english')

transtable = {ord(c): None for c in string.punctuation}


def remove_punctuations(text):
    return text.translate(transtable).lower()


def normalize_text(text):
    tokens = [t for t in punctuation_remover.tokenize(text.lower())
              if t not in english_stopwords]
    return ' '.join(tokens)


def remove_duplicate_strings(strings_list):
    seen = set()
    seen_add = seen.add
    return [s for s in strings_list if not (s in seen or seen_add(s))]
```


## Numpy scipy linux requirements
```bash
sudo apt-get install libblas-dev liblapack-dev libatlas-base-dev gfortran
```


## Set up ipython to auto reload all modules
```bash
ipython profile create
vim ~/.ipython/profile_default/ipython_config.py
c.InteractiveShellApp.extensions = ['autoreload']
c.InteractiveShellApp.exec_lines = ['%autoreload 2']
```


## Install python binary from source
```bash
wget https://www.python.org/ftp/python/2.7.9/Python-2.7.9.tgz
tar -xvf Python-2.7.9.tgz
cd Python-2.7.9
./configure --prefix=/opt/python2.7.9
make && sudo make install
```


## Understand context managers
http://jeffknupp.com/blog/2016/03/07/python-with-context-managers/


## Clean virtualenv
```bash
pip freeze | xargs pip uninstall -y
```


## Serialize JSON object into string without whitespace
```
json.dumps(separators=(',', ':'))
```


## Convert epoch time to human readable date string
```
datetime.fromtimestamp(epoch_time_in_ms / 1000).isoformat()
```


## Split on last delimiter once
```
str.rsplit(delimiter, 1)
```
