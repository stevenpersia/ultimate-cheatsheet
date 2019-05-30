# Array

## Basics
```js
const arr = ["a","b","c","d","e"]
arr                                 // → ["a","b","c","d","e"]
arr[1]                              // → "b"
```
----
```indexOf()```

Find

```js
const arr = ["a","b","c","d","e"]
arr.indexOf("b")                    // → 1
arr.indexOf("e")                    // → -1
```
----
```slice()```

Subset (immutable)

```js
const arr = ["a","b","c","d","e"]
arr.slice(0,1)                      // → ["a"]
arr.slice(1)                        // → ["b","c","d","e"]
arr.slice(1,2)                      // → ["b"]
```
----
```splice()```

Subset (mutative)

```js
const arr = ["a","b","c","d","e"]
const newArr = arr.splice(1)        // new = ["b","c","d","e"]   arr = ["a"]
const newArr = arr.splice(1,2)      // new = ["b","c"]           arr = ["a","d","e"]
```

Replacing items
```js
const arr = ["a","b","c","d","e"]
arr.splice(2, 1, X)                 // → arr = ["a","b",X,"d","e"]
```
----
```concat()```

Adding items (immutable)

```js
const arr = ["a","b","c","d","e"]
arr.concat([X,Y])                   // → ["a","b","c","d","e",X,Y]
```
----
```push()``` ```unshift()``` ```splice()```

Adding items (mutative)
```js
const arr = ["a","b","c","d","e"]
arr.push(X)                         // → arr = ["a","b","c","d","e",X]
arr.unshift(X)                      // → arr = [X,"a","b","c","d","e"]
arr.splice(2, 0, X)                 // → arr = ["a","b",X,"c","d","e"]
```
----
```pop()``` ```shift()``` ```splice()```

Removing items

```js
const arr = ["a","b","c","d","e"]
arr.pop()                           // → "e"    arr = ["a","b","c","d"]
arr.shift()                         // → "a"    arr = ["b","c","d","e"]
arr.splice(2, 1)                    // → ["c"]  arr = ["a","b","d","e"]
```
----
```toString()```

Transforming array to string

```js
const arr = [1,2,3,4]
const str = arr.toString()          // → "1,2,3,4"

// Another way
const str = `${arr}`                // → "1,2,3,4"
```


## Advanced

```splice()```

Inserting items
```js
const arr = ["a","b","c","d","e"]

// after -- [_,_,REF,NEW,_,_]
arr.splice(arr.indexOf(REF)+1, 0, NEW))

// before -- [_,_,NEW,REF,_,_]
arr.splice(arr.indexOf(REF), 0, NEW))
```
----
```filter()```
```js
const arr = [1,2,3,4]
const newArr = arr.filter(num => num % 2 === 0)     // → [2,4]
```
----
```map()```
```js
const arr = [1,2,3,4]
const newArr = arr.map(num => num + 1)              // → [2,3,4,5]
```
----
```flat()```
```js
const arr = [1,[2,[3,[4]]]]
const newArr = arr.flat(3)      // → [1,2,3,4]
```
----
```reverse()```
```js
const arr = [1,2,3,4]
arr.reverse()                   // → [4,3,2,1]
```
----
```reduce()```
```js
const arr = [1,2,3,4]
const newArr = arr.reduce((sum, num) => sum + num)       // → 10
```
----
```find()```
```js
const arr = [1,2,3,4]
const newArr = arr.find(num => num % 2 === 0)            // → 2
```
----
```findIndex()```
```js
const arr = [1,2,3,4]
const newArr = arr.findIndex(num => num % 2 === 0)      // → 1
```
----
```sort()```
```js
const arr = [1,2,3,4]
arr.sort((num1, num2) => num2 - num1)     // Array.sort() mutates the source array
```
----
```some()```
```js
const arr = [1,2,3,4]
arr.some((num) => num % 5 === 0)         // → false
```
----
```copyWithin()```
```js
const arr = [1,2,3,4]
arr.copyWithin(0,2)      // Array.copyWithin() mutates the source array
arr                      // → [3,4,3,4]
```

### Iteration
```forEach()```
```js
const arr = [1,2,3,4]
arr.forEach((num) => console.log(num))      // → 1/2/3/4
```
----
```entries()```
```js
const arr = ["a","b","c","d"]
const newArr = arr.entries()
newArr.next()                  // → {value: [0, "a"], done: false}
newArr.next().value            // → [1, "b"]
newArr.next().value            // → [2, "c"]
newArr.next()                  // → {value: [3, "d"], done: true}
```
----
```keys()```
```js
const arr = ["a","b","c","d"]
const newArr = arr.keys()
newArr.next()                  // → {value: 0, done: false}
// ...
```
----
```values()```
```js
const arr = ["a","b","c","d"]
const newArr = arr.values()
newArr.next()                  // → {value: "a", done: false}
// ...
```
