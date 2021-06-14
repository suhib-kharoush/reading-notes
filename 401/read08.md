# List Comprehensions in Python:

- List comprehensions provide a concise way to create lists.

- It consists of brackets containing an expression followed by a for clause, then
zero or more for or if clauses. The expressions can be anything, meaning you can
put in all kinds of objects in lists.

- expression(i):
- Expression is based on the variable used for each element in the old list.

- for i in old_list:
- The word for followed by the variable name to use, followed by the word in the
old list.

- if filter(i):
- Apply a filter with an If-statement.

## Create a list using loops and list comprehension:
-  Assume we want to create a list of squares. Start with an empty list:
- example:
- squares = []

- for x in range(10):
 -   squares.append(x**2)
 
- print squares
- [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]

# Or you can use list comprehensions to get the same result:
- squares = [x**2 for x in range(10)]

- print squares
- [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]

## Multiplying parts of a list
- Multiply every part of a list by three and assign it to a new list.

- example:
- list1 = [3,4,5]
 
- multiplied = [item*3 for item in list1] 
 
- print multiplied 
- [9,12,15]

## Lower/Upper case converter:
- Let’s show how easy you can convert lower case / upper case letters.
- >>> [x.lower() for x in ["A","B","C"]]
- ['a', 'b', 'c']

- >>> [x.upper() for x in ["a","b","c"]]
- ['A', 'B', 'C']
