
String manipulation in Python involves operations that allow you to modify, concatenate, format, and perform various operations on strings.

Here are some common string manipulation techniques:

1. **Concatenation**: This involves combining two or more strings into a single string.

   ```python
   first_name = "John"
   last_name = "Doe"
   full_name = first_name + " " + last_name
   print(full_name)  # Output: "John Doe"
   ```

2. **String Formatting**: This allows you to embed variables within strings for more dynamic output.

   ```python
   name = "Jane"
   age = 30
   message = f"Hello, my name is {name} and I am {age} years old."
   print(message)  # Output: "Hello, my name is Jane and I am 30 years old."
   ```

3. **String Indexing and Slicing**: You can access individual characters or sections of a string using indices.

   ```python
   text = "Python"
   print(text[0])  # Output: "P" (first character)
   print(text[1:4])  # Output: "yth" (slicing from index 1 to 3)
   ```

4. **String Methods**: Python provides many built-in methods for string manipulation, such as `upper()`, `lower()`, `strip()`, `replace()`, `split()`, and more.

   ```python
   text = "   Hello, World!   "
   print(text.strip())  # Output: "Hello, World!" (remove leading and trailing spaces)
   print(text.upper())  # Output: "   HELLO, WORLD!   " (convert to uppercase)
   print(text.replace("Hello", "Hi"))  # Output: "   Hi, World!   " (replace "Hello" with "Hi")
   ```

5. **String Length**: You can find the length of a string using the `len()` function.

   ```python
   text = "Hello, World!"
   print(len(text))  # Output: 13 (length of the string)
   ```

6. **String Splitting and Joining**: You can split a string into a list of substrings or join a list of strings into a single string.

   ```python
   sentence = "This is a sample sentence."
   words = sentence.split()  # Split into a list of words
   print(words)  # Output: ['This', 'is', 'a', 'sample', 'sentence.']

   new_sentence = ' '.join(words)  # Join the list into a sentence
   print(new_sentence)  # Output: "This is a sample sentence."
   ```

These are some of the fundamental string manipulation techniques in Python. They provide you with the tools needed to work with textual data effectively. Let me know if you'd like further clarification on any of these techniques!