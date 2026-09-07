# Exercises

Try these without running the code first. Write down your reasoning, then verify it in Python.

## Variables and assignment

### Exercise 1: 

What happens, and why?

```python
mass = 12
print(Mass)
```

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

## Comments

### Exercise 5: 

Which line is a valid Python comment?

1. `// Calculate the average`
2. `# Calculate the average`
3. `/* Calculate the average */`
4. `<!-- Calculate the average -->`

## Lists
### Exercise 6:

Predict both outputs:

```python
observations = [3.2, 4.1, 5.0, 5.9]
print(len(observations))
print(observations[-1])
```

### Exercise 7: 

Predict the output:

```python
codes = ["A", "B", "C", "D", "E"]
print(codes[1:4])
```

## Strings

### Exercise 8: 
Predict the output:

```python
sensor_id = 4
amplitude = 0.094812

print(f"Sensor {sensor_id}: peak = {amplitude:.1f} m/s²")
```


## Conditional execution

### Exercise 9: 

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

## Loops

### Exercise 10: 

Predict the output:

```python
values = [2, 3, 4]
products = []

for value in values:
    products.append(value * 10)

print(products)
```

## Dictionaries

### Exercise 11: 

Predict the output:

```python
weights = {"low": 0.5, "medium": 1.0, "high": 1.5}
print(weights["high"])
```
### Exercise 12: 

Predict the output:

```python
records = {"group_a": [2, 4, 6], "group_b": [1, 3, 5]}
selected = records["group_a"][1:]
squared = []

for value in selected:
    squared.append(value ** 2)

print(squared)
```


## Functions

### Exercise 13: 

Predict the output:

```python
def normalize(value, maximum):
    return value / maximum

print(normalize(15, 20))
```

## Scripts, programs, and code structure

### Exercise 14: 

Put these parts in a conventional order: the import statement, configuration value, function definition, and main code. Then explain why the import must appear before the call to `math.sqrt`.

```python
def calculate_side(area):
    return math.sqrt(area)

AREA = 64

import math

print(calculate_side(AREA))
```

---
