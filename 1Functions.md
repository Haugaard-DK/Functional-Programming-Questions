## 1  Functions

* Functions as first class citizens

  ​	Allows you to pass functions as variables
  ```elm
  -- A Function in Elm --
  function = \a b -> a + b
  
  -- A list of functions in Elm --
  var functionList = [(\a -> a * 2), (\a -> a - 2), (\a -> a + 100)]
  ```
  ```haskell
  -- A simple Haskell function to add two numbers together --
  simpleAddFunction :: Integer -> Integer -> Integer
  simpleAddFunction = A B = A + B
  ```

* higher order functions

  ​	Returns a function as its result or takes one or more functions as arguments
  
  ```elm
  -- This Function uses our previously created function to add our chosen number, --
  -- to the numbers that are in the list of numbers that the function is given. --
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
  -- Our function here is chosen to use a lambda function marked by the backslash, --
  -- as we have no interest in using this particular function anywhere else. --
  doSomethingWithLambda List number -> List number
  doSomethingWithLambda list =
  List.map (\a -> ((1.5 * a + 3) / 2)) list
  ```
  ```haskell
  -- Here our previous Haskell function is turned into a lambda or anonymous function --
  simpleAddFunction :: Integer -> Integer -> Integer
  simpleAddFunction = (\A B = A + B)
  ```

  


