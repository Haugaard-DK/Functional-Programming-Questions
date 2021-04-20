## 5 Pattern Matching

* How to use pattern matching to destruct various data structures as:

  * –lists

  * –tuples

    A tuple can be destructured as early as in the parameters of a function
    
    ```elm
    -- Destructuring of a tuple --
    vectorToString : Vector -> String
    vectorToString (x, y) =
    "(" ++ String.fromFloat x ++ "," ++ String.fromFloat y ++ ")"
    ```

  * –records

    Records can be destructured the same way
    
    ```elm
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
