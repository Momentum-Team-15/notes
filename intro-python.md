# Welcome to Phase 2 - Python & Django

---

## Python Origins

- General purpose programming language developed by Guido van Rossum and released in 1991.

### Stated Goals

    1. an easy and intuitive language just as powerful as those of the major competitors;
    2. open source, so anyone can contribute to its development;
    3. code that is as understandable as plain English;
    4. suitable for everyday tasks, allowing for short development times.

---

## Let's write some Python and see what happens.

Copy this code in an empty Python file, but do not run it.

Predict what you think will happen.

Then, run it and check your expectations against what happens.

```py

def greet(names):
    for name in names:
        print(f"Hi, {name}!")

our_names = ["Amy", "Jeanette", "Rebecca", "Dawn", "Dwayne 'The Rock' Johnson"]

greet(our_names)
```

---

## Python/JavaScript Comparison

| JavaScript                              | Python                             |
| --------------------------------------- | ---------------------------------- |
| Runs in browser, generally (client)     | Runs on server, generally          |
| White space NBD                         | White space conveys meaning        |
| Code hoisted, order doesn't matter      | Code read from top to bottom       |
| camelCase                               | snake_case                         |
| `console.log()`                         | `print()`                          |
| `function myFunction(params){}`         | `def myFunction(params):`          |
| `return`                                | `return `                          |
| `let`/`const` declare variables         | variables assigned when delcared   |
| `if/while (condition) { outcome }`      | `if/while condition: outcome`      |
| `else if (condition) {}`                | `elif condition:`                  |
| `else {}`                               | `else:`                            |
| myArray[index] gives item at index      | myList[index] gives item at index  |
| `for (let i of array) { function(i){}}` | `for i in list: fun(i)`            |
| Arrays                                  | Lists                              |
| template literals                       | f strings                          |
| Objects                                 | Dictionaries                       |
| DOM Manipulation                        | Nope                               |
| Event handling/promises                 | asyncio (we probably won't see it) |
---

## Let's try reading some more Python. 

```py

def sum(numbers):
    numbers_copy = numbers.copy()
    sum = 0
    while len(numbers_copy) > 0:
        sum += numbers[len(numbers_copy) - 1]
        numbers_copy.pop()
    print(sum)
    return(sum)

my_sum = sum([1, 2, 3, 17])
```

---

## Quick reference for Python syntax

```py
# variables
var_name = value

# functions
def my_function(parameter1, parameter2):
    # here's where the action happens
    return value_to_be_returned

# to see values in the console
print(value)

# conditionals
if a > b:
    return(a)

# loops
while b < a:
    b += 1

for item in my_list:
   # do something to the item

# remember to use snake_case instead of camelCase
```

---
