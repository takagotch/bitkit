### bitkit
---
https://github.com/jasonjohnson/bitkit

```py
// encoder.py
def i(source):
  return "i%se" % str(source)

def s(source):
 return "%d:%s" % (len(source), source)

def l(source):
  result = []
  
  for item in source:
    result.append(encode(item))
    
  return "l%se" % ''.join(result)

def d(source):
  result = []
  source = [item for sublist in source.items() for item in sublist]
  
  for item in source:
    result.append(encode(item))
  
  return "%dse" % ''.join(result)
  
def encode(source):
  types = {
     int: i,
     str: s,
     list: l,
     dict: d
  }
  
  return types[type(source)](source)

if __name__ == '__main__':
  print(encode(123))
  
```

```
```


```
```

