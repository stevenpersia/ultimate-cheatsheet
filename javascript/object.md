# Object

Objects in JavaScript are collections of key/value pairs.
An object can be created with figure brackets {…}

----
```Create object```

```js
const employee = { 					// Name object "employee"
  name: 'Michael Jam', 			// By key "name" store value "Michael Jam"
  email: 'michael@example.com',
  age: 30,
  ocupation: 'Accountant'
};

// Print console
console.log(employee);

// Output
{ name: "Michael Jam", email: "michael@example.com", age: 30, ocupation: "Accountant" }
```

----
```Values```

Accessible values of an object
Property values are accessible using the dot notation :

```js
const employee = {
  name: 'Michael Jam',
  email: 'michael@example.com',
  age: 30,
  ocupation: 'Accountant'
};

// Print console
console.log(employee.name);
console.log(employee.age);

// Output
Michael Jam
30
```

----
```Key```

Add new key of an object.

```js
const employee = {
  name: 'Michael Jam',
  email: 'michael@example.com',
  age: 30,
  ocupation: 'Accountant'
};

// Print console
console.log(employee);

// Output
{ name: "Michael Jam", email: "michael@example.com", age: 30, ocupation: "Accountant" }

employee.city = "San Francisco";   // Add new key "city" and value "San Francisco"
employee.phone = "44-23125";	   // Add new key "phone" and value "12345"

// Print console
console.log(employee);

// Output
{ name: "Michael Jam", email: "michael@example.com", age: 28,
  ocupation: "Accountant", city:"San Francisco", phone: "44-23125" }
```
----
```Modify```

Modify values to a key of an object.

```js
const employee = {
  name: 'Michael Jam',
  email: 'michael@example.com',
  age: 30,
  ocupation: 'Accountant'
};

// Print console
console.log(employee);

// Output
{ name: "Michael Jam", email: "michael@example.com", age: 30, ocupation: "Accountant" }

employee.name = "Michael Jam Pier"; // Modify the value of a key "name"
employee.age = 28;					// Modify the value of a key "age"

// Print console
console.log(employee);

// Output
{ name: "Michael Jam Pier", email: "michael@example.com", age: 28, ocupation: "Accountant" }
```

----
```Object.values()```

Creates an array containing the values of an object.

```js
const employee = {
  name: 'Michael Jam',
  email: 'michael@example.com',
  age: 30,
  ocupation: 'Accountant'
};

// Get all values of the object
const values = Object.values(employee);

// Print console
console.log(values);

// Output
["Michael Jam", "michael@example.com", 30, "Accountant"]
```

----
```Object.keys()```

Creates an array containing the keys of an object.

```js
const employee = {
  name: 'Michael Jam',
  email: 'michael@example.com',
  age: 30,
  ocupation: 'Accountant'
};

// Get the keys of the object
const keys = Object.keys(employee);

// Print console
console.log(keys);

// Output
["name", "email", "age", "ocupation"]
```

----
```Object.assign()```

Copy values from one object to another.

```js
const employee = {
  name: 'Michael Jam',
  email: 'michael@example.com',
  age: 30,
  ocupation: 'Accountant'
};

const address = {
  city : 'New York',
  country : 'United States',
};

// Merge the objects
const newObject = Object.assign(employee, address);

// Print console
console.log(newObject);

// Output
["Michael Jam", "michael@example.com", 30, "Accountant", "New York", "United States"]
```

----
```operator (...)```

Copy values from one object to another with operator (...).

```js
const employee = {
  name: 'Michael Jam',
  email: 'michael@example.com',
  age: 30,
  ocupation: 'Accountant'
};

const address = {
  city : 'New York',
  country : 'United States',
};

// Merge the objects
const newObject = {...employee, ...address};

// Print console
console.log(newObject);

// Output
["Michael Jam", "michael@example.com", 30, "Accountant", "New York", "United States"]
```