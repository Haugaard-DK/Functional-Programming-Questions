## 5 Pattern Matching

* How to use pattern matching to destruct various data structures as:

  * –lists

   ```elm
   -- Destructuring of a list --
   listToString : List String -> String
   listToString list =
    case list of
     [] -> ""
     head :: tail -> head ++ ", " ++ listToString tail
   -- This function will take a list of strings and convert it all to a string, --
   -- We also check for whether or not the list is empty, and if it is we make it return an empty string. --
   -- Should the list however turn out to not be empty then we first check if the list has a head and a tail, --
   -- we then return a string containing the head with a recursive call towards the tail of the list --
   ```

  * –tuples

    A tuple can be destructured as early as in the parameters of a function
    
    ```elm
    -- Simple Destructuring of a tuple --
    vectorToString : Vector -> String
    vectorToString (x, y) =
    "(" ++ String.fromFloat x ++ "," ++ String.fromFloat y ++ ")"
    ```

  * –records

    Records can be destructured the same way
    
    ```elm
    -- Destructuring of record --
    type alias Vector = (Float, Float)

    type alias NamedPoint =
     { name : String
     , point : Vector
     }
     
     namedPointToString : NamedPoint -> String
     namedPointToString {name, point} =
    "Point " ++ name ++ " is located at (" ++ String.fromFloat (Tuple.first point) ++ "," ++ String.fromFloat (Tuple.second point) ++ ")"
    ```

  * –union types

    This has already been explained in the document about 
