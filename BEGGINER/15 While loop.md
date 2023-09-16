A `while` loop in Python is used to repeatedly execute a block of code as long as a specified condition is true. It keeps evaluating the condition before each iteration. Here's how you use a `while` loop:

### Basic `while` Loop:

```python
while condition:
    # Code to be executed as long as the condition is true
```

Here, `condition` is a boolean expression. As long as it evaluates to `True`, the code block will be executed.

### Example:

```python
count = 0

while count < 5:
    print(count)
    count += 1
```

This will output:

```
0
1
2
3
4
```

### Infinite Loop:

Be cautious when using `while` loops, as an incorrect condition may lead to an infinite loop, which can cause your program to run indefinitely. It's important to have a way to break out of the loop.

```python
# This is an example of an infinite loop
# Avoid running this code
while True:
    print("This will run forever!")
```

### Using `break` Statement:

You can use the `break` statement to exit the loop prematurely based on a certain condition.

```python
count = 0

while True:
    if count >= 5:
        break
    print(count)
    count += 1
```

This will produce the same output as the earlier example, but it uses a `break` statement to exit the loop when `count` reaches 5.

### Using `continue` Statement:

The `continue` statement allows you to skip the rest of the loop's code and move to the next iteration.

```python
count = 0

while count < 5:
    count += 1
    if count == 3:
        continue
    print(count)
```

This will output:

```
1
2
4
5
```

In this example, when `count` is 3, the `continue` statement is executed, skipping the `print(count)` statement.

### Using `else` with `while`:

You can include an `else` block that will be executed when the `while` loop condition becomes `False`.

```python
count = 0

while count < 5:
    print(count)
    count += 1
else:
    print("Loop completed")
```

This will output:

```
0
1
2
3
4
Loop completed
```

### Common Use Cases:

- `while` loops are often used when you don't know in advance how many times the loop will need to run.
- They are used for tasks that require repeated execution until a certain condition is met, such as user input validation or data processing.

Remember to be cautious with `while` loops to avoid creating infinite loops, and ensure there's a way to exit the loop based on the condition.