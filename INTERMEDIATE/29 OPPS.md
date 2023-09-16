
In Python, you can access and modify attributes of an object using dot notation. This allows you to retrieve the values of an object's attributes or assign new values to them. Here's how you can get and set attributes:

### Getting Attributes:

To retrieve the value of an attribute, you simply use the dot notation followed by the attribute name:

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

# Create an instance
john = Person("John Doe", 30)

# Access attributes
print(john.name)  # Output: "John Doe"
print(john.age)   # Output: 30
```

### Setting Attributes:

To assign a new value to an attribute, you use the dot notation followed by the attribute name and the assignment operator (`=`):

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

# Create an instance
john = Person("John Doe", 30)

# Modify attributes
john.name = "John Smith"
john.age = 31

# Access modified attributes
print(john.name)  # Output: "John Smith"
print(john.age)   # Output: 31
```

### Using Methods for Attribute Access:

Sometimes, it's a good practice to use methods to get or set attributes, especially if you want to perform additional logic or validations.

```python
class Person:
    def __init__(self, name, age):
        self._name = name
        self._age = age

    def get_name(self):
        return self._name

    def set_name(self, name):
        self._name = name

# Create an instance
john = Person("John Doe", 30)

# Access attributes using methods
print(john.get_name())  # Output: "John Doe"

# Modify attributes using methods
john.set_name("John Smith")
print(john.get_name())  # Output: "John Smith"
```

In this example, the `_name` attribute is accessed and modified using the `get_name` and `set_name` methods.

### Using Properties (Getter and Setter):

Python also allows you to use properties to define methods that will be used for getting and setting attributes. This allows you to have more control over the access and modification of attributes.

```python
class Person:
    def __init__(self, name, age):
        self._name = name
        self._age = age

    @property
    def name(self):
        return self._name

    @name.setter
    def name(self, value):
        self._name = value

# Create an instance
john = Person("John Doe", 30)

# Access attributes using properties
print(john.name)  # Output: "John Doe"

# Modify attributes using properties
john.name = "John Smith"
print(john.name)  # Output: "John Smith"
```

In this example, `@property` is used to define a method that will be used to retrieve the value of `name`, and `@name.setter` is used to define a method that will be used to set the value of `name`.

Using properties can provide a more controlled and organized way to handle attribute access.