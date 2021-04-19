## 3  Purity

Explain in your own words with code examples in Elm and Haskell:

* When can a function be defined as pure

  ​	A function is pure when it is returns the same output given the same input regardless of the order they are called in

* What is a side effect

  A function has a side effect if it modifies its state. In other words, a function causes a side effect if it performs any other action apart  from calculating its return value.

  * when to avoid 

    ​	Side effects should be avoided when possible because they can add complexity and debugging

  * when to embrace

    Side effects are needed when you need to do something outside of the program, like changing a website or updating a database

  
