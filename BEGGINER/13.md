
A `for` loop in Python is used to iterate over a sequence (such as a list, tuple, string, etc.) or other iterable objects. It allows you to perform a set of operations for each item in the sequence. Here's how you use a `for` loop:

### Basic `for` Loop:

```python
for item in sequence:
    # Code to be executed for each item
```

Here, `item` is a variable that will take on the value of each element in the sequence, one at a time.

### Example with a List:

```python
fruits = ["apple", "banana", "cherry"]

for fruit in fruits:
    print(fruit)
```

This will output:

```
apple
banana
cherry
```

### Using `range()` with `for` Loop:

The `range()` function generates a sequence of numbers. It is often used with `for` loops to perform a certain task a specified number of times.

```python
for i in range(5):
    print(i)
```

This will output:

```
0
1
2
3
4
```

### Iterating Over a String:

Strings are also iterable in Python. You can use a `for` loop to go through each character in a string.

```python
for char in "Python":
    print(char)
```

This will output:

```
P
y
t
h
o
n
```

### Using `enumerate()` for Index and Value:

`enumerate()` is a built-in function that can be used with `for` loops to get both the index and value of items in a sequence.

```python
fruits = ["apple", "banana", "cherry"]

for index, fruit in enumerate(fruits):
    print(f"Index {index}: {fruit}")
```

This will output:

```
Index 0: apple
Index 1: banana
Index 2: cherry
```

### Nested `for` Loops:

You can also have loops inside loops, known as nested loops.

```python
for i in range(3):
    for j in range(2):
        print(i, j)
```

This will output:

```
0 0
0 1
1 0
1 1
2 0
2 1
```

### `break` and `continue` Statements:

- `break`: Terminates the loop prematurely.
- `continue`: Skips the rest of the loop and moves to the next iteration.

These are useful for controlling the flow of a loop based on certain conditions.

```python
for i in range(5):
    if i == 2:
        break
    print(i)
```

This will output:

```
0
1
```

```python
for i in range(5):
    if i == 2:
        continue
    print(i)
```

This will output:

```
0
1
3
4
```

These are the basics of using `for` loops in Python. They are crucial for iterating over collections of data and performing operations on each item. Let me know if you have any further questions!