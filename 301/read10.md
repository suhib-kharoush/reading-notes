# JavaScript error messages:

- Types of error messages:
- The first thing that indicates us that something is wrong with our code is the (in)famous error message that the one we saw just moments ago, it usually appears on our console (being developer tools of the browser, terminal or whatever else we are using).

- Syntax error:
- this error occurs when we have something that can't be parsed in terms of syntax.

- Types error:
- This type of errors show up the types number, string, ..etc we are trying to use or access are incompatible.


#### Debugging:
- ![](https://miro.medium.com/max/625/1*ByuRUFwh_Nul0ZOOx4QVRg.png)


- We can use debug in our visual studio when press debug tab.
- ![](https://miro.medium.com/max/875/1*q0ybXMtFlQdnXQuOUNRQSw.png)

#### Call stack:
![](https://miro.medium.com/max/625/1*LHpmsxV3f2znpxhuAFuIqA.png);

- Tools to avoid runtime errors:
- quokk: to evaluate my code as I type.
- eslint: to make sure my style guide is consistency.


# JavaScript call stack:
- The JavaScript engine  is a single-threaded interpreter comprising of a heap and a single call stack. The browser provides web APIs like the DOM, AJAX, and Timers.

- Temporarily store:
 - When a function is invoked (called), the function, its parameters, and variables are pushed into the call stack to form a stack frame. This stack frame is a memory location in the stack. The memory is cleared when the function returns as it is pop out of the stack.

 ![](https://cdn-media-1.freecodecamp.org/images/QgR2uIk7tW0YNz0Xm8g0jAPeRFI0e4sCejsv)

 #### Call stack:
 - A call stack is a mechanism for an interpreter to keep track of its place in a script that calls multiple functions — what function is currently being run and what functions are called from within that function, etc.



