```
hw12 = '%s %s %d' % (hello, world, 12)  # sprintf style string formatting
print (hw12)  # prints "hello world 12"
```
If you want access to the index of each element within the body of a loop, use the built-in `enumerate` function:
```
animals = ['cat', 'dog', 'monkey']
for idx, animal in enumerate(animals):
    print ('#%d: %s' % (idx + 1, animal))
```
#1: cat<Br/>
#2: dog<Br/>
#3: monkey<Br/>
