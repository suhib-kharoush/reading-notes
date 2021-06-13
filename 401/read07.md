# Python Scope & the LEGB Rule:
- The concept of scope rules how variables and names are looked up in your code. It determines the visibility of a variable within the code. 

- The letters in the acronym LEGB stand for Local, Enclosing, Global, and Built-in scopes. This summarizes not only the Python scope levels but also the sequence of steps that Python follows when resolving names in a program.

## Understanding Scope:
- In programming, the scope of a name defines the area of a program in which you can unambiguously access that name, such as variables, functions, objects, and so on.

- General scopes:
- - Global scope: The names that you define in this scope are available to all your code.
- - Local scope: The names that you define in this scope are only available or visible to the code within the scope.

- Python Scope vs Namespace:
- In Python, the concept of scope is closely related to the concept of the namespace. As you’ve learned so far, a Python scope determines where in your program a name is visible. Python scopes are implemented as dictionaries that map names to objects. These dictionaries are commonly called namespaces. These are the concrete mechanisms that Python uses to store names. They’re stored in a special attribute called .__dict__.

- Using the LEGB Rule for Python Scope:
- Python resolves names using the so-called LEGB rule, which is named after the Python scope for names. 

- Local (or function) scope is the code block or body of any Python function or lambda expression. This Python scope contains the names that you define inside the function.
- Enclosing (or nonlocal) scope is a special scope that only exists for nested functions.
- Global (or module) scope is the top-most scope in a Python program, script, or module.
- Built-in scope is a special Python scope that’s created or loaded whenever you run a script or open an interactive session.

- square() is a function that computes the square of a given number, base. 

## Nested Functions: The Enclosing Scope:
- When you call outer_func(), you’re also creating a local scope. The local scope of outer_func() is, at the same time, the enclosing scope of inner_func(). 
