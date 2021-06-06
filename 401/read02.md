# Recursion:
- What is Recursion? 
- The process in which a function calls itself directly or indirectly is called recursion and the corresponding function is called as recursive function.

- What is base condition in recursion?
- In the recursive program, the solution to the base case is provided and the solution of the bigger problem is expressed in terms of smaller problems. 

- Why Stack Overflow error occurs in recursion? 
- If the base case is not reached or not defined, then the stack overflow problem may arise. Let us take an example to understand this.

# In Tests We Trust — TDD with Python:
- Unit tests and TDD?
- Unit tests are some pieces of code to exercise the input, the output and the behaviour of my code. I can write them anytime I want.

- Baby Steps:
- The API is pretty straightforward and your work was almost done. But with TDD we need to think about tests first. And to be ok with the possibility of the beginning to be hard sometimes — and it’s totally fine. 

- The AAA: Arrange, Act and Assert:
- Arrange: we need to organize the data needed to execute that piece of code (input).
- Act: here we will execute the code being tested (exercise the behaviour).
- Assert: after executing the code, you will check if the result (output) is the same as you were expecting.

- The Cycle:
- The cycle is made by three steps:
- 1. 🆘 Write a unit test and make it fail (it needs to fail because the feature isn’t there, right? If this test passes, call the Ghostbusters, really)
- 2. ✅ Write the feature and make the test pass!.
- 3. 🔵 Refactor the code — the first version doesn’t need to be the beautiful one.

![](https://miro.medium.com/max/875/1*dTd_0x8gdefpRt9tUtekPQ.png)