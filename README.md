# RNGoose
RNGoose is a package to provide better and easier rng functions into JS. Allows for seeds and other stuff.

## How to use
All you have to do is require the package `rngoose`. In this documentation we will be importing it with the name random in all examples.
```js
const random = require("rngoose");

const number = random.int();
console.log(number); // Returns any number between 1 and 6 (inclusive)
```

## Functions
##### Random Integer
```js
// Returns a random number between 1 and 6, just like a die.
const die = random.int(); 		

// Returns a random number between 1 and 100.
const score = random.int(100); 

// Returns a random number between 3 and 6.
const items = random.int(3, 6); 

// Returns a number between 1 and 100, using the seed 150 and salt 1.5. When using seeds, the result number is always the same for the same seed. This is useful to generate worlds for example. Salt acts as a modifier for the seed, when you have different random generators with the same min, max and seed, you sometimes want to be different between them but still keeping the seed features, that's where salt comes in.
const seeded = random.int(1, 100, { seed: 150, salt: 1.5 }); 
```

##### Random Floats
Acts the same way as random integers, but with floating points
```js
// Returns a random float number between 1 and 6, just like a die.
const die = random.float(); 		

// Returns a random float number between 1 and 100.
const score = random.float(100); 

// Returns a random float number between 3 and 6.
const items = random.float(3, 6); 

// You got the point
const seeded = random.float(1, 100, { seed: 150, salt: 1.5 }); 
```

##### Classic Random
Returns a random float between 0 and 1, just like Math.random() function does, with the slight difference you can pass seed and salt for rngoose one
```js
const rdm = random.n();
const seeded = random.n({ seed: 656525 });
```