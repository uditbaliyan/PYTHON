
In Python, methods are functions that are defined inside a class and are associated with instances of that class. They allow objects to perform actions or operations related to their attributes. Here's how you define and use methods in Python:

### Defining Methods:

```python
class ClassName:
    def method_name(self, parameter1, parameter2):
        # Code for the method
        pass
```

- `method_name`: This is the name of the method. It should follow Python's naming conventions (lowercase with underscores for readability).
- `self`: This is a reference to the instance that the method is being called on. It allows the method to access the object's attributes and other methods.
- `parameter1`, `parameter2`: These are the parameters that the method takes. You can have any number of parameters.

### Example:

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def introduce(self):
        return f"My name is {self.name} and I am {self.age} years old."

    def celebrate_birthday(self):
        self.age += 1
```

In this example, the `Person` class has three methods:

- `__init__`: This is the constructor method that initializes the `name` and `age` attributes when a new instance of `Person` is created.

- `introduce`: This method returns a formatted string introducing the person.

- `celebrate_birthday`: This method increments the person's age by 1.

### Calling Methods:

```python
# Create an instance
john = Person("John Doe", 30)

# Call the methods
print(john.introduce())      # Output: "My name is John Doe and I am 30 years old."
john.celebrate_birthday()
print(john.introduce())      # Output: "My name is John Doe and I am 31 years old."
```

### Methods without `self`:

Sometimes, you might have methods that don't need to access or modify object attributes. In such cases, you can define static methods using the `@staticmethod` decorator.

```python
class Utility:
    @staticmethod
    def add_numbers(x, y):
        return x + y
```

You can call static methods using the class name:

```python
result = Utility.add_numbers(3, 5)
print(result)  # Output: 8
```

### Class Methods:

Class methods are methods that are bound to the class rather than instances. They can access and modify class-level attributes.

```python
class MyClass:
    class_attribute = "This is a class attribute"

    @classmethod
    def class_method(cls):
        return cls.class_attribute
```

You can call class methods using the class name:

```python
print(MyClass.class_method())  # Output: "This is a class attribute"
```

### Special Methods (Magic Methods):

Python also has a set of special methods, also known as magic methods or dunder methods, that start and end with double underscores. These methods allow you to define the behavior of your objects in certain situations (e.g., when they are compared, added together, etc.).

For example, `__str__` allows you to define how an object should be represented as a string:

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def __str__(self):
        return f"My name is {self.name} and I am {self.age} years old."

john = Person("John Doe", 30)
print(john)  # Output: "My name is John Doe and I am 30 years old."
```

Methods are essential for defining the behavior of your objects and for making your code more organized and reusable. They allow you to encapsulate functionality within your classes.