# Classes and Objects:

- What is the objects?
- Objects are an encapsulation of variables and functions into a single entity. Objects get their variables and functions from classes. Classes are essentially a template to create your objects.


# Thinking Recursively in Python:

- Problems (in life and also in computer science) can often seem big and scary. But if we keep chipping away at them, more often than not we can break them down into smaller chunks trivial enough to solve. This is the essence of thinking recursively, and my aim in this article is to provide you, my dear reader, with the conceptual tools necessary to approach problems from this recursive point of view.

- Dear Pythonic Santa Claus…
- I realize that as fellow Pythonistas we are all consenting adults here, but children seem to grok the beauty of recursion better. So let’s not be adults here for a moment and talk about how we can use recursion to help Santa Claus.
![](https://files.realpython.com/media/santa_claus_2.ecbf2686f1a1.png)

- I propose an algorithm with which he can divide the work of delivering presents among his elves:

- 1. I propose an algorithm with which he can divide the work of delivering presents among his elves:
- 2. Assign titles and responsibilities to the elves based on the number of houses for which they are responsible:
- > 1 He is a manager and can appoint two elves and divide his work among them
- = 1 He is a worker and has to deliver the presents to the house assigned to him
![](https://robocrop.realpython.net/?url=https%3A//files.realpython.com/media/elves_7.8d1af1cd85c8.png&w=1918&sig=24bad525e070e8248cc8fcce28fc3f52c68a69f9)
 - This is the typical structure of a recursive algorithm. If the current problem represents a simple case, solve it. If not, divide it into subproblems and apply the same strategy to them.

 - Recursive Functions in Python

 - Maintaining State:
 - When dealing with recursive functions, keep in mind that each recursive call has its own execution context, so to maintain state during recursion you have to either:
 - - Thread the state through each recursive call so that the current state is part of the current call’s execution context
 - - Keep the state in global scope

 - Recursive Data Structures in Python:
 - A data structure is recursive if it can be deﬁned in terms of a smaller version of itself. A list is an example of a recursive data structure. 

 - Naive Recursion is Naive:
 - The Fibonacci numbers were originally deﬁned by the Italian mathematician Fibonacci in the thirteenth century to model the growth of rabbit populations.