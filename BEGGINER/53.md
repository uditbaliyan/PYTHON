

Working with dates and times in Python is made easy with the `datetime` module. This module provides classes and functions to manipulate dates and times. Here are some common operations you can perform with dates and times:

### 1. **Importing the datetime Module:**

```python
from datetime import datetime, date, time, timedelta
```

### 2. **Creating a Date or Time Object:**

```python
# Creating a date object
today = date.today()
print(today)  # Output: YYYY-MM-DD

# Creating a time object
current_time = time(hour=10, minute=30, second=45)
print(current_time)  # Output: HH:MM:SS

# Creating a datetime object
now = datetime.now()
print(now)  # Output: YYYY-MM-DD HH:MM:SS
```

### 3. **Formatting Dates and Times:**

```python
# Formatting a datetime object as a string
formatted_date = now.strftime("%Y-%m-%d %H:%M:%S")
print(formatted_date)  # Output: YYYY-MM-DD HH:MM:SS
```

### 4. **Parsing Dates from Strings:**

```python
# Parsing a string into a datetime object
date_string = "2022-09-15 12:30:00"
parsed_date = datetime.strptime(date_string, "%Y-%m-%d %H:%M:%S")
print(parsed_date)  # Output: 2022-09-15 12:30:00
```

### 5. **Performing Arithmetic Operations with Dates and Times:**

```python
# Calculating the difference between two dates
birthday = date(1990, 1, 1)
age = today - birthday
print(age.days)  # Output: Number of days

# Adding or subtracting time durations
new_time = current_time + timedelta(hours=2, minutes=15)
print(new_time)  # Output: HH:MM:SS
```

### 6. **Working with Time Zones:**

```python
from datetime import timezone

# Getting the current UTC time
now_utc = datetime.now(timezone.utc)
print(now_utc)  # Output: YYYY-MM-DD HH:MM:SS in UTC
```

### 7. **Using Timedelta for Time Differences:**

```python
# Creating a timedelta object
time_difference = timedelta(days=5, hours=3, minutes=20)
future_date = today + time_difference
print(future_date)  # Output: YYYY-MM-DD
```

### 8. **Converting Between Time Zones:**

```python
from pytz import timezone

# Installing pytz library: pip install pytz

# Define time zones
eastern = timezone('US/Eastern')
central = timezone('US/Central')

# Get current time in specified time zone
fmt = '%Y-%m-%d %H:%M:%S %Z%z'
now_eastern = datetime.now(eastern)
print(now_eastern.strftime(fmt))  # Output: Current time in Eastern Time

now_central = now_eastern.astimezone(central)
print(now_central.strftime(fmt))  # Output: Current time in Central Time
```

### 9. **Handling Daylight Saving Time:**

```python
# The pytz library handles DST transitions automatically
from pytz import timezone

eastern = timezone('US/Eastern')
utc_dt = datetime(2023, 3, 12, 5, 0, 0, tzinfo=eastern)

print(utc_dt.strftime('%Y-%m-%d %H:%M:%S %Z%z'))  # Output: 2023-03-12 05:00:00 EST-0500
```

### 10. **Finding the Day of the Week:**

```python
day_of_week = today.strftime("%A")
print(day_of_week)  # Output: Name of the day (e.g., 'Monday')
```

### Conclusion:

The `datetime` module provides a wide range of functions for working with dates and times. Whether you need to perform basic operations like creating and formatting dates, or more complex tasks like handling time zones, Python's `datetime` module has you covered.