# Monads in Haskell

A Monad is something that handles side effects in Haskell.
The Monad represent the world that the side effect needs to happen in.
For example if we have a function which has to print something to the console, that function will take a Monad representing the console and the string to be printed.
The function will then print the string to the console and thereby changing the Monad, which will then be returned with the change.
In this way we can pass around representations of data and stay pure.
