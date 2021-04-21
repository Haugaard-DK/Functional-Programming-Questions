## 2  Currying

* The principle of currying

   ​	Currying is the technique of converting a function that takes multiple arguments into a sequence of functions that each take a single argument

* How to implement and use currying in Elm and Haskell

  * Elm

    * Define a function with n arguments

    * Define another function in terms of the first function being partially applied, that is, having only one argument passed to it

    * Call the second function and pass it the remaining arguments that the first function was expecting

     ```elm
     -- A simple example of currying could be something like the following function. --
     multThree : number -> number -> number -> number
     multThree x y z = x * y * z
     
     -- A function can also use another function in its call, like the following: --
     applyTwice : (a -> a) -> a -> a
     applyTwice f x = f (f x)
     
     putTogether : number
     putTogether = applyTwice (multThree 2 3) 4
     -- This should then return 96, the math behind sounds as following ((2 * 3 * 2 * 3 = 36) * 4 = 144) --
     
     -- Our good old multThree function can also easily be used in conjunction with the map function --
     -- to multiply the elements within it by our chosen numbers --
     mapExample : List number -> List number
     mapExample list = List.map (multThree 2 2) list
     -- This should then result in every element within the list being passed through --
     -- the multThree function as (2 * 2 * listElement) --
     ```

  * Haskell

    * Pretty much the same as elm

   ```haskell
   -- Haskell is infact so similar to elm in terms of currying that we will use the same examples but just with Haskell --
      multThree :: (Num a) -> a -> a -> a -> a
      multThree x y z = x * y * z
      
      applyTwice :: (a -> a) -> a -> a
      applyTwice f x = f (f x)
      
      putTogether :: number
      putTogether = applyTwice (multThree 2 3) 4
      
      mapExample :: List number -> List number
      mapExample list = List.Map (multThree 2 2) list
   ```

* Typical currying use cases

  ​	Currying is used so often without even thinking about it, that it is hard to say that there is a single specific case where you'd not use it.
