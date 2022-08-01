# let & const

- `let` - used for variable.
- `const` - for constant variable.

# Arrow functions

``` javascript
const myFunc = () => {}
```

- solves issues with `this` keyword.

# Exports & Imports (modules)

``` javascript
export default Person;

export const clean = () => {}
```

```javascript
import person, {clean} from "file.js";
// other ways
import {smth as newName} from "file.js";
import * as bundled from "file.js";

```

# Classes

- a blueprint for objects, contains properties and methods.

```javascript
class Person {
	constructor() {
		// props
	}

	methodOne() {
		// 
	}
}

class I extends Person {
	consturctor() {
		super();
	}
}
```

- a class extending another class must call a `super()`.
- In es7 properties can be directly define props inside the class without using constructor method.
```javascript
class Wizzard {
	staff = 'Oak';
	doMagic = () => {/**/}
}
```

# Spread & Rest Operators

- `spread` used to split array elements and object properties
	- can also be used to copy objects and array(reference types).
- `rest` merge bunch of function arguments into a single array

```javascript
const numbers = [1, 2, 3];
const newNumbers = [...numbers, 4, 5];

const person = { name: "Gandalf",}
const wizard = {...person, staff: "Oak"};

// rest args
const sum = (...args) => {/**/}

```

# Array Functions

- `Array.map()` returns a new array by mapping each elements.
- `Array.filtter()` filter elements.