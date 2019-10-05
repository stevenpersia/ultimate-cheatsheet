# Interfaces

`basic example`

```js
interface SquareConfig {
  color: string;
  width: number;
}

let config: SquareConfig = { color: "black", width: 10 };
```

---

`optional`

```js
interface SquareConfig {
  color?: string;
  width?: number;
}

let config: SquareConfig = { color: "black" };
```

---

`readonly`

```js
interface SquareConfig {
  color?: string;
  readonly width?: number;
}

let config: SquareConfig = { color: "black", width: 10 };
config.color = "white" // ok
config.width = 20 // error!
```

---

`index signature`

```js
interface SquareConfig {
  color?: string;
  width?: number;
}

let config: SquareConfig = { color: "black", width: 10, height: 10 }; // error: Object literal may only specify known properties, but 'height' does not exist in type 'SquareConfig'.

interface SquareConfig {
  color?: string;
  width?: number;
  [key: string]: any;
}

let config: SquareConfig = { color: "black", width: 10, height: 10 }; // ok

interface StringArray {
  [index: number]: string;
}

let array: StringArray = ["Bob", "Fred"]; // ok

// Error: indexing with a numeric string might get you a completely separate type!
interface NotOkay {
  [x: number]: SquareConfig;
  [x: string]: TriangleConfig;
}

interface NumberDictionary {
  [index: string]: number;
  length: number; // ok, length is a number
  name: string; // error, the type of 'name' is not a subtype of the indexer
}

interface NumberOrStringDictionary {
  [index: string]: number | string;
  length: number; // ok, length is a number
  name: string; // ok, name is a string
}

interface ReadonlyStringArray {
    readonly [index: number]: string;
}
let myArray: ReadonlyStringArray = ["Alice", "Bob"];
myArray[2] = "Mallory"; // error!
```

---

`class types basic`

```js
interface ClockInterface {
  currentTime: Date;
  setTime(d: Date): void;
}

class Clock implements ClockInterface {
  currentTime: Date = new Date();
  setTime(d: Date) {
    this.currentTime = d;
  }
  constructor(h: number, m: number) {}
}
```

---

`class types with constructor`

```js
interface ClockConstructor {
  new(hour: number, minute: number): ClockInterface;
}
interface ClockInterface {
  tick(): void;
}

function createClock(
  ctor: ClockConstructor,
  hour: number,
  minute: number
): ClockInterface {
  return new ctor(hour, minute);
}

class DigitalClock implements ClockInterface {
  constructor(h: number, m: number) {}
  tick() {
    console.log("beep beep");
  }
}
class AnalogClock implements ClockInterface {
  constructor(h: number, m: number) {}
  tick() {
    console.log("tick tock");
  }
}

let digital = createClock(DigitalClock, 12, 17);
let analog = createClock(AnalogClock, 7, 32);

// another way to use class expressions

interface ClockConstructor {
  new (hour: number, minute: number);
}

interface ClockInterface {
  tick();
}

const Clock: ClockConstructor = class Clock implements ClockInterface {
  constructor(h: number, m: number) {}
  tick() {
      console.log("beep beep");
  }
}
```

---

`extending interfaces`

```js
interface Shape {
    color: string;
}

interface PenStroke {
    penWidth: number;
}

interface Square extends Shape, PenStroke {
    sideLength: number;
}

let square = {} as Square;
square.color = "blue";
square.sideLength = 10;
square.penWidth = 5.0;
```

---

`hybrid types`

```js
// An object that acts as both a function and an object, with additional properties.
interface Counter {
    (start: number): string;
    interval: number;
    reset(): void;
}

function getCounter(): Counter {
    let counter = (function (start: number) { }) as Counter;
    counter.interval = 123;
    counter.reset = function () { };
    return counter;
}

let c = getCounter();
c(10);
c.reset();
c.interval = 5.0;
```
