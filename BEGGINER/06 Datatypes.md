In Python, data types are classifications that categorize various types of data, indicating the operations that can be performed on them and the way they are stored in memory. Here are some of the basic data types in Python:

1. **Numeric Types**:
   - **int**: Integer numbers without decimal points (e.g., -5, 0, 100).
   - **float**: Floating-point numbers with decimal points (e.g., -3.14, 0.0, 2.71828).
   - **complex**: Complex numbers with a real and imaginary part (e.g., 1 + 2j, 3 - 4j).

   ```python
   # Examples of numeric types
   x = 5          # int
   y = 3.14       # float
   z = 2 + 3j     # complex
   ```

2. **Sequence Types**:
   - **str**: Strings, which are sequences of characters (e.g., "Hello", 'Python').

   ```python
   # Examples of strings
   greeting = "Hello"
   name = 'Python'
   ```

3. **Boolean Type**:
   - **bool**: Represents boolean values, either `True` or `False`.

   ```python
   # Example of boolean type
   is_valid = True
   ```

4. **None Type**:
   - **NoneType**: Represents the absence of a value or a null value.

   ```python
   # Example of NoneType
   my_variable = None
   ```

5. **Sequence Types**:
   - **list**: Ordered collections of items of any type, mutable (can be changed).
   - **tuple**: Ordered collections of items of any type, immutable (cannot be changed).
   - **range**: Represents a range of numbers.

   ```python
   # Examples of sequence types
   my_list = [1, 2, 3]      # list
   my_tuple = (1, 2, 3)     # tuple
   my_range = range(5)     # range
   ```

6. **Mapping Type**:
   - **dict**: Key-value pairs where keys must be unique.

   ```python
   # Example of a dictionary
   my_dict = {'name': 'John', 'age': 30}
   ```

7. **Set Types**:
   - **set**: Unordered collections of unique elements.
   - **frozenset**: Immutable version of a set.

   ```python
   # Examples of set types
   my_set = {1, 2, 3}             # set
   my_frozenset = frozenset({4, 5, 6})  # frozenset
   ```

8. **Binary Types**:
   - **bytes**: Immutable sequences of bytes.
   - **bytearray**: Mutable sequences of bytes.

   ```python
   # Examples of binary types
   my_bytes = b'Hello'             # bytes
   my_bytearray = bytearray(b'World')  # bytearray
   ```

These are some of the fundamental data types in Python. Understanding these types is crucial for effective programming. Keep in mind that Python is dynamically typed, meaning you don't need to declare the type of a variable explicitly. The interpreter infers the type based on the value assigned.