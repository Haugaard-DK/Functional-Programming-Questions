## 1  Functions

Explain in your own words with code examples in Elm and Haskell

* Functions as first class citizens

  ​	Allows you to pass functions as variables
  ```elm
  function = a b -> a + b
  
  var fList = [(a -> a * 2), (a -> a - 2), (a -> a + 100)]
  ```

* higher order functions

  ​	Returns a function as its result or takes one or more functions as arguments
  
  ```elm
  addToEachElement : List number -> List number
  addToEachElement list =
  List.map (function 3) list
  
  ```

* lambdas

  ​	We would like to just create a function "right where we need it"

  ​	We only plan to use the function once.

  ​	The function is fairly simple

  ​ We want to return a function from a function.
  
  ​ Lambda functions are marked with a Backlash ( \ )
  
  ```elm
  doSomethingWithLambda List number -> List number
  doSomethingWithLambda list =
  List.map (\a -> ((1.5 * a + 3) / 2)) list
  ```

  


