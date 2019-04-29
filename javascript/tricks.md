Get Unique Values of an Array

```js
const arr = [...new Set([1, 2, 3, 3])]
arr  // → [1, 2, 3]
```
----

Filter falsy values (0, undefined, null, false, ...) out of an array

```js
arr.map(item => {
        // ...
    })
    // Get rid of bad values
    .filter(Boolean);
```
----

Create empty object

```js
let obj = Object.create(null);

// obj.__proto__ === "undefined"
// No object properties exist until you add them
```
----

Merge objects

```js
const person = { name: 'Steven Persia', gender: 'Male' };
const tools = { computer: 'Mac', editor: 'Visual Studio Code' };
const attributes = { handsomeness: 'Extreme', hair: 'Brown', eyes: 'Brown' };

const summary = {...person, ...tools, ...attributes};

/*
Object {
  "computer": "Mac",
  "editor": "Visual Studio Code",
  "eyes": "Brown",
  "gender": "Male",
  "hair": "Brown",
  "handsomeness": "Extreme",
  "name": "Steven Persia",
}
*/
```
----

Require function parameters

```js
const isRequired = () => { throw new Error('param is required'); };

const hello = (name = isRequired()) => { console.log(`hello ${name}`) };

// This will throw an error because no name is provided
hello();

// This will also throw an error
hello(undefined);

// These are good!
hello(null);
hello('Steven');
```
----

Destructuring aliases

```js
const obj = { x: 1 };

// Grabs obj.x as { x }
const { x } = obj;

// Grabs obj.x as { otherName }
const { x: otherName } = obj;
```
----

Get query string parameters

```js
// Assuming "?post=1234&action=edit"

const urlParams = new URLSearchParams(window.location.search);

console.log(urlParams.has('post')); // true
console.log(urlParams.get('action')); // "edit"
console.log(urlParams.getAll('action')); // ["edit"]
console.log(urlParams.toString()); // "?post=1234&action=edit"
console.log(urlParams.append('active', '1')); // "?post=1234&action=edit&active=1"
```
----

Array of numbers to strings

```js
const arr = [1,2,3,4,5].map(String);
arr  // → ["1","2","3","4","5"]
```
