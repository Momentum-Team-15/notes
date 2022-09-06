

## 💡 To run this code, type `python` at the command line prompt.

That will start a Python REPL where you can run Python code! Good practice would be to type this in there and see what you get.

Don't type the `>>>`. That is showing you the start of the prompt in the Python REPL.

# Python Lists

- Collections enclosed by `[]`
- Trailing comma can be used
- Indexed like JS arrays, starting at `0`

```py
>>> nerf_guns = ['Rampage', 'Shockwave RD-15', 'Mediator',]
>>> my_list[0]
'Rampage'
```

## Examples of frequently used list methods

### `append()` adds an item to the end

This is like `push` in JS.

```py
>>> nerf_guns.append('Jolt')
>>> nerf_guns
['Rampage', 'Shockwave RD-15', 'Mediator', 'Jolt']
```

### `pop()` removes the last item from the end

```py
>>> nerf_guns.pop() # this returns the item you popped off the list, and alters the list
'Jolt'
>>> nerf_guns
['Rampage', 'Shockwave RD-15', 'Mediator']
```

### `remove()` deletes a specified item

```py
>>> nerf_guns.remove('Mediator') # this does not return the thing you removed, but it does change the list
>>> nerf_guns
['Rampage', 'Shockwave RD-15']
```

---

# Python Dictionaries

## key: value pairs enclosed by `{}`

Similar to JS objects.

Notice that you need to put quotation marks around the keys, unlike in JS objects (but like JSON!).

Trailing commas also 👍 in dictionaries, as in lists.

```py
>>> fruit_amounts = {
    'apples': 3,
    'bananas': 4,
    'papayas': 2,
    }
```

## Obtain values by their keys, NOT their position

You have to use square brackets enclosing a string to retrieve values by their key. Dot notation will not work like it does in JS.

```py
>>> fruit_amounts['apples']
3
>>> fruit_amounts.apples # ⛔ NOPE! This won't work!
```

---

## Add or reassign values to dictionaries like this:

```py
>>> fruit_amounts['pears'] = 5
>>> fruit_amounts['bananas'] = 10
>>> fruit_amounts
{'apples': 3, 'bananas': 10, 'papayas': 2, 'pears': 5}
```

Notice you can change values for existing keys and you can also add new keys with values **with the same syntax**.

---

# Python Tuples

## Ordered collections enclosed by `()`

Tuples are like lists but they are immutable (can't be changed).

```py
>>> dimensions = (2, 4, 10)
```

## Obtain data using index, as with lists

```py
>>> dimensions[1]
4
```

---

## Unpack tuples by assigning each value to a variable

```py
>>> length, width, height = (2, 4, 10)
>>> length
2
>>> width
4
>>> height
10
```

---
