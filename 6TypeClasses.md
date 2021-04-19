# 06 Type Classes


A Type class is a class used to instatiate different types of objects along with the rest of the project so that any errors are encountered as early as possible.

A Type class could look like the following :

```haskell 
module Types where 

import GHC.Generics
import data.Aeseon (FromJSON, ToJSON)

data Object = Object
{Name :: String
,Quantity :: Int
} deriving (Show, Generic)

instance ToJSON Object
instance FromJSON Object
```