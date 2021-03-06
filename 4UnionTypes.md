## 4  Union Types

A Union Type is a simple type that can be one of multiple different sub-types.

* How to handle polymorphism using union types

```elm
  -- A union type could look like the following --
  type Status
    = Alive
    | Somewhat_Dead
    | Mostly_Dead
    | Very_Dead
  -- Here we make a union type that could hold different statuses for another object --
  
  -- Now lets make a object to make use of these statuses --
  type alias Subject = 
  { status : Status
  , number : Int
  }
  
  -- Now lets make a function to return a piece of string based on what status our subject object has --
  getSubjectStatus : Subject -> String
  getSubjectStatus subject =
    case subject.status of
        Alive ->
            "Subject " ++ fromInt(subject.number) ++ " is currently still alive..."
        Somewhat_Dead ->
            "Subject " ++ fromInt(subject.number) ++ " is currently not looking as well as before..."
        Mostly_Dead ->
            "Subject " ++ fromInt(subject.number) ++ " is currently looking as if it is on its last legs..."
        Very_Dead ->
            "Subject " ++ fromInt(subject.number) ++ " has reached rigor mortis..."
```

* How to handle errors using union types

  * In the case that the union type value that you want to use can be unset in one way or another, one can use a maybe type to circumvent any potential Null Pointer errors. these maybe types are written a little differently in Elm and Haskell but do look somewhat similar, they can be seen just below this.
  
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
  
  * One can also use union types to make sure there is always a possible response when trying to send or receive a Http request.

  ```elm
  -- This could look something like this --
  errorToString : Http.Error -> String
  errorToString error =
    case error of
        BadUrl url ->
            ("Error, bad url: "++ url)
        Timeout ->
            "Error, connection timed out"
        NetworkError ->
            "Network Error"
        BadStatus code ->
            ("Error "++ String.fromInt code)
        BadBody errMsg ->
            ("Something went wrong with the body: " ++ errMsg)
  ```
