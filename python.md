
## Default template

```console
#!/usr/bin/env python
# -*- coding: utf8 -*-

if __name__ == "__main__":

```


## install python 2.7 (Ubuntu 16.04)

```console
$ sudp apt-get install python python-bs4 python-requests
```


## json read/write

```console
import json

if __name__ == "__main__":

    FILENAME = "test.json"

    with open( FILENAME, 'a+' ) as json_file:
        contents = json_file.read()
        contents = json.loads(contents.decode('utf-8-sig').encode('utf-8'), 'utf-8')

    with open( FILENAME, 'w+' ) as json_file:
        json.dump( contents, json_file, indent=4, separators=(',', ': ') )
```


## sort list of dictionary

```console
contents = sorted( contents, key=lambda k: k['key'], reverse=True )
```
