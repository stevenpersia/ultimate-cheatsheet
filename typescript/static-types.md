# Static Types

```boolean```

```js
let isAwesome: boolean = true;
```

----

```string```

```js
let name: string = 'Steven';

let joke: string = `
	Q: Why did the chicken cross the road?
	A: ${punchline}
`;
```

----

```number```

```js
let decimalNumber: number = 42;         // → 42
let binaryNumber: number = 0b101010;    // → 42
let octalNumber: number = 0o52;         // → 42
let hexadecimalNumber: number = 0x2a;   // → 42
```

----

```array```

```js
let myPetFamily: string[] = ['rocket', 'fluffly', 'harry'];
let myPetFamily: Array<string> = ['rocket', 'fluffly', 'harry'];
```

----

```enum```

```js
// Enum start to 0.
enum Sizes {
    Small,
    Medium,
    Large,
}

Sizes.Small;    // → 0
Sizes.Medium;   // → 1
Sizes.Large;    // → 2

// Enum start to 1.
enum Sizes {
    Small = 1,
    Medium,
    Large,
}

Sizes.Small;    // → 1
Sizes.Medium;   // → 2
Sizes.Large;    // → 3

// String values can also be assigned to an enum.
enum ThemeColors {
    Primary = 'primary',
    Secondary = 'secondary',
    Dark = 'dark',
    DarkSecondary = 'darkSecondary',
}
```

----

```any```

```js
let something: any = 4;     // → number
something = 'a string';     // → string
something = false;          // → boolean
```

----

```void```

```js
// When there is no type associated with something.
const doSomething = (): void => {
    console.log('Ok...');
};
```

----

```null``` and ```undefined``` 

```js
let anUndefinedVariable: undefined = undefined;
let aNullVariable: null = null;
```