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
It is easy to iterate over the keys in a dictionary:(迭代ｋｅｙ)
```
d = {'person': 2, 'cat': 4, 'spider': 8}
for animal in d:
    legs = d[animal]
    print ('A %s has %d legs' % (animal, legs))
```
A person has 2 legs<Br/>
A cat has 4 legs<Br/>
A spider has 8 legs<Br/>

If you want access to keys and their corresponding values, use the iteritems method:<Br/>
```
d = {'person': 2, 'cat': 4, 'spider': 8}
for animal, legs in d.iteritems():
    print 'A %s has %d legs' % (animal, legs)
```
A person has 2 legs<Br/>
A spider has 8 legs<Br/>
A cat has 4 legs<Br/>


