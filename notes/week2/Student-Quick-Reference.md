# **Python Quick Reference Card**

## Input --> Calculate --> Output

### Getting Input

```
# Text input (always returns string)
name = input("What's your name? ")

# Number input - whole numbers
age = int(input("How old are you? "))

# Number input - decimals allowed
height = float(input("Height in meters? "))

```
**Remember:** `input()` ALWAYS gives you a string. Convert it!

### Math Operators

```
+     # Addition:        5 + 3 = 8
-     # Subtraction:     5 - 3 = 2
*     # Multiplication:  5 * 3 = 15
/     # Division:        5 / 2 = 2.5 (always gives decimal)
//    # Integer divide:  5 // 2 = 2 (drops decimal)
%     # Modulus:         5 % 2 = 1 (remainder)
**    # Exponent:        5 ** 2 = 25 (5 squared)
```

**Order:** Parentheses --> Exponents --> Multipl/Divide --> Add/ Subtract

```
result = 2 + 3 * 4       # = 14 (multiply first)
result = (2 + 3) * 4     # = 20 (parentheses first)
```

### Variables
```
# Good names - clear and descriptive
user_name = "Alex"
garden_length = 12.5
total_price = 45.99

# Bad names - unclear
x = "Alex"
gl = 12.5
tp = 45.99
```

### Rules:
    * Start with letter or underscore
    * Can contain letters, numbers, underscores
    * Case sensitive: `Name` is not `name`
    * No spaces or special characters

## Output Formatting with f-strings

### Basic f-string
```
name = "Jordan"
age = 16
print(f"I'm {name} and I'm {age}")
# Output: I'm Jordan and I'm 16
```

### Format Numbers - 2 Decimals
```
price = 9.5
print(f"Price: ${price:.2f}")
# Output: Price: $9.50
```

### Format Numbers - Commas
```
big = 1234567
print(f"Total: {big:,}")
# Output: Total: 1,234,567
```

### Math Inside f-strings
```
length = 10
width = 5
print(f"Area: {length * width} square feet")
# Output: Area: 50 square feet
```

## Common Patterns
### Get, Calculate, Display
```
# 1. Get input
radius = float(input("Radius? "))

# 2. Calculate
area = 3.14159 * radius ** 2

# 3. Display
print(f"Area: {area:.2f} square units")
```

### Multiple Calculations
```
length = float(input("Length? "))
width = float(input("Width? "))

perimeter = 2 * (length + width)
area = length * width

print(f"Perimeter: {perimeter:.2f}")
print(f"Area: {area:.2f}")
```

### Type Conversion Reference
```
# String to integer
int("42")         # → 42
int("3.14")       # ✗ ERROR!

# String to float
float("3.14")     # → 3.14
float("42")       # → 42.0

# Number to string
str(42)           # → "42"
str(3.14)         # → "3.14"
```

## Common Mistakes & Fixes
### Forgot to convert input -- WRONG
```
age = input("Age? ")
print(age + 1)  # ERROR!
```

### Fixed
```
age = int(input("Age? "))
print(age + 1)  # Works!
```

### Used int() for decimals -- WRONG
```
height = int(input("Height? "))  # User types 1.75, gets 1
```
### Forgot f in f-string - WRONG
```
name = "Sam"
print("Hi {name}")  # Prints: Hi {name}
```

### Fixed
```
print(f"Hi {name}")  # Prints: Hi Sam
```

### Math on strings - WRONG
```
num1 = "5"
num2 = "3"
print(num1 + num2)  # Prints: 53
```

### Fixed
```
num1 = int("5")
num2 = int("3")
print(num1 + num2)  # Prints: 8
```

### Program Template
```
# Name: Your Name
# Date: Today's Date
# Assignment: Assignment Name
# Description: What this program does

# ========== GET INPUT ==========
# Get information from user
variable1 = int(input("Prompt: "))
variable2 = float(input("Prompt: "))

# ========== CALCULATE ==========
# Perform calculations
result1 = variable1 + variable2
result2 = variable1 * 2

# ========== DISPLAY OUTPUT ==========
# Show results to user
print(f"Result 1: {result1:.2f}")
print(f"Result 2: {result2:.2f}")
```
