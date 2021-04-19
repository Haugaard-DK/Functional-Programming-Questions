## 4  Union Types

* How to handle polymorphism using union types

* How to handle errors using union types

  

  Elm and Haskell have different syntax for union types:

  ```elm
  type Maybe a

  ​	= Just a

  ​	| Nothing
  ``` 

  ```haskell
  data Maybe a

  ​	= Nothing 

  ​	| Just a

  ```
  
  
