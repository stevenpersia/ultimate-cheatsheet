# String

## Basics

```charAt()```

Returns the character at the specified index

```js
const str = "Hello my name is Steven Persia"
str.charAt(0)                                   // → "H"
str.charAt(1)                                   // → "e"
str.charAt(2)                                   // → "l"
str.charAt(3)                                   // → "l"
str.charAt(4)                                   // → "o"
str.charAt(24)                                  // → "P"
```
----
```concat()```

Joins two or more strings, and returns a copy of the joined strings

```js
const str = "Hello my name is"
const str2 = " Steven Persia"

str.concat(str2)                // → "Hello my name is Steven Persia"
```
----
```indexOf()```

Returns the position of the first found occurence of a specified value in a string

```js
const str = "Hello my name is Steven Persia"

str.indexOf("S")                // → 17
str.indexOf("k")                // → -1
```
----
```replace()```

Searches for a match between a substring (or regex) and a string, and replaces the matched substring with a new substring

```js
const str = "Hello my name is Steven Persia"

str.replace("Steven Persia", "Brad Pitt")     // → "Hello my name is Brad Pitt"
```
----
```slice()```

Extracts a part of a string and returns a new string

```js
const str = "Hello my name is Steven Persia"

str.slice(0, 5)     // → "Hello"
str.slice(1)        // → "ello my name is Steven Persia"
str.slice(9)        // → "name is Steven Persia"
str.slice(9, 13)    // → "name"
```
----
```split()```

Splits a string into an array of substrings

```js
const str = "Hello my name is Steven"

str.split("")     // → ["H", "e", "l", "l", "o", " ", "m", "y", " ", "n", "a", "m", "e", " ", "i", "s", " ", "S", "t", "e", "v", "e", "n"]
str.split(" ")        // → ["Hello", "my", "name", "is", "Steven"]
str.split("my ")        // → ["Hello ", "name is Steven"]
```
----
```toLowerCase()```

Converts a string to lowercase letters

```js
const str = "Hello my name is Steven Persia"

str.toLowerCase()        // → "hello my name is steven persia"
```
----
```toUpperCase()```

Converts a string to uppercase letters

```js
const str = "Hello my name is Steven Persia !"

str.toUpperCase()        // → "HELLO MY NAME IS STEVEN PERSIA !"
```
----
```toString()```

Converts to a string

```js
const num = 1;
const arr = ["a", "b", "c"]

num.toString()              // → "1"
arr.toString()              // → "a,b,c"
```
