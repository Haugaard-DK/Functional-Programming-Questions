# Monoids

A Monoid is 3 things combined together:
* A set of elements (when I say “set” I mean it in the most abstract way, a “collection”, a “group”, not an actual Set).
* A binary operation (eg. a function which combines two elements) which spits back another element of the same set.
* A neutral element (often called unit) which combined with an element gives us back our element.

For instance, these are all monoids:
* Natural Numbers, under addition, with 0 as the neutral element
* Natural Numbers, under multiplication, with 1 as the neutral element
* Strings, under concatenation, with an empty string as the neutral element

To put all this in to an example lets do the following:
* Two elements combined must create an element of the same set [eg. 2+3=5, we get another natural number]
* Each element combined with the neutral element gives back the same element [eg. 0+2=2 and 2+0=2]
* Composition must be associative [eg. (1+2)+3=1+(2+3)]
