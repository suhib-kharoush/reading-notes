# What is functional programming?
- Functional programming is a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data.

- The first fundamental concept we learn when we want to understand functional programming is pure functions.

#### Functions as first-class entities:
- The idea of functions as first-class entities is that functions are also treated as values and used as data.

- Functions as first-class entities can:
 - refer to it from constants and variables.
 - pass it as a parameter to other functions.
 - return it as result from other functions.


 #### Higher-order functions:
 - When we talk about higher-order functions, we mean a function that either:
  - takes one or more functions as arguments, or
  - returns a function as its result.


  # Refactoring JavaScript for Performance and Readability:

  - Scenario 1:
   - We're an URL-shortening website, like TinyURL. We accept a long URL and return a short URL that forwards visitors to the long URL. We have two functions:
   
const URLstore = [];

- function makeShort(URL) {
 - const rndName = Math.random().toString(36).substring(2);
  - URLstore.push({[rndName]: URL});
  - return rndName;
}

- function getLong(shortURL) {
  - for (let i = 0; i < URLstore.length; i++) {
    - if (URLstore[i].hasOwnProperty(shortURL) !== false) {
      return URLstore[i][shortURL];
    }
  }
}

- Scenario 2:
- We're a social media website where user URLs are generated randomly. Instead of random gibberish, we're going to use the friendly-words package that the Glitch team works on.


