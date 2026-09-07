# Exercises

Try these without running the code first. Write down your reasoning, then verify it in Python.

## Variables and assignment

### Exercise 1: 

What happens, and why?

```python
mass = 12
print(Mass)
```
---
Return to [Variables and assignment](python-tutorial.md#variables-and-assignment).

## Operators and expressions
### Exercise 2: 

What happens, and why?

```python
adjusted = raw + 2
raw = 8
print(adjusted)
```



### Exercise 3: 

Predict both outputs:

```python
print(17 / 5)
print(17 // 5)
```

### Exercise 4: 

Predict the output:

```python
x = 2
print((x + 3) ** 2)
```

---
Return to [Variables and assignment](python-tutorial.md#operators-and-expressions).


### Exercise 5: list length and indexing

Predict both outputs:

```python
observations = [3.2, 4.1, 5.0, 5.9]
print(len(observations))
print(observations[-1])
```

### Exercise 6: slicing

Predict the output:

```python
codes = ["A", "B", "C", "D", "E"]
print(codes[1:4])
```

### Exercise 7: dictionary lookup

Predict the output:

```python
weights = {"low": 0.5, "medium": 1.0, "high": 1.5}
print(weights["high"])
```

### Exercise 8: loop state

Predict the output:

```python
values = [2, 3, 4]
products = []

for value in values:
    products.append(value * 10)

print(products)
```

### Exercise 9: conditionals

Predict the output:

```python
score = 75

if score >= 80:
    category = "high"
elif score >= 60:
    category = "medium"
else:
    category = "low"

print(category)
```

### Exercise 10: functions

Predict the output:

```python
def normalize(value, maximum):
    return value / maximum

print(normalize(15, 20))
```

### Exercise 11: combine the concepts

Predict the output:

```python
records = {"group_a": [2, 4, 6], "group_b": [1, 3, 5]}
selected = records["group_a"][1:]
squared = []

for value in selected:
    squared.append(value ** 2)

print(squared)
```

### Exercise 12: structuring a script

Put these parts in a conventional order: the import statement, configuration value, function definition, and main code. Then explain why the import must appear before the call to `math.sqrt`.

```python
def calculate_side(area):
    return math.sqrt(area)

AREA = 64

import math

print(calculate_side(AREA))
```

---
