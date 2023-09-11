
Reading and writing CSV (Comma-Separated Values) files is a common task in data handling and manipulation. Python provides a built-in module called `csv` for working with CSV files. Here's how you can perform basic operations:

### Reading from a CSV File:

```python
import csv

with open('data.csv', 'r') as file:
    reader = csv.reader(file)
    for row in reader:
        print(row)
```

In this example, `data.csv` is opened in read mode (`'r'`). The `csv.reader()` function is used to read the contents of the file. It returns an iterator that yields rows as lists.

### Writing to a CSV File:

```python
import csv

data = [
    ['Name', 'Age', 'City'],
    ['John Doe', 30, 'New York'],
    ['Jane Smith', 25, 'San Francisco'],
]

with open('data.csv', 'w', newline='') as file:
    writer = csv.writer(file)
    writer.writerows(data)
```

In this example, `data` is a list of lists representing the rows of the CSV file. The file is opened in write mode (`'w'`). The `csv.writer()` function is used to write to the file. The `writerows()` method is used to write multiple rows.

### Writing Dicts to CSV:

You can also write dictionaries to a CSV file using the `csv.DictWriter()` class.

```python
import csv

data = [
    {'Name': 'John Doe', 'Age': 30, 'City': 'New York'},
    {'Name': 'Jane Smith', 'Age': 25, 'City': 'San Francisco'}
]

with open('data.csv', 'w', newline='') as file:
    fieldnames = ['Name', 'Age', 'City']
    writer = csv.DictWriter(file, fieldnames=fieldnames)
    writer.writeheader()
    writer.writerows(data)
```

### Reading Dicts from CSV:

```python
import csv

with open('data.csv', 'r') as file:
    reader = csv.DictReader(file)
    for row in reader:
        print(row)
```

In this example, `csv.DictReader()` is used to read the contents of the file. It interprets the first row as the field names and returns an iterator that yields dictionaries.

### Custom Delimiters and Quote Characters:

You can specify custom delimiters and quote characters when working with CSV files by providing the `delimiter` and `quotechar` parameters to the `csv.reader()` or `csv.writer()` functions.

### Handling CSV Files with Headers:

When reading CSV files with headers, you can access the header row separately from the rest of the data.

```python
import csv

with open('data.csv', 'r') as file:
    reader = csv.reader(file)
    headers = next(reader)  # Get the header row
    for row in reader:
        print(row)
```

### Conclusion:

Working with CSV files is a common task in data processing. The `csv` module in Python provides convenient functions for reading and writing CSV files. It's important to handle exceptions appropriately and to be mindful of the format and structure of the data in your CSV files.