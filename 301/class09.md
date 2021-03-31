# Read: 09 - Refactoring
 <b>Complexity</b> is anything that makes software hard to understand or to modify.
`immutability` and `pure function` are big advantages to build side-effect-free functions, so it is easier to maintain systems.
Immutability Unchanging over time or unable to be changed.

![Functional Programming](https://res.cloudinary.com/practicaldev/image/fetch/s--YdnYpB3u--/c_imagga_scale,f_auto,fl_progressive,h_900,q_auto,w_1600/https://thepracticaldev.s3.amazonaws.com/i/nty82qv6m2sdjdwla7ue.png)

## FUNCTIONAL PROGRAMMING

**Functional Programming** is a programming paradigm that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data.

In other words, the program should return new data without modifying the original data.

## pure functions

The first fundamental concept we learn when we want to understand functional programming is pure functions.

* It returns the same result if, given the same arguments (it is also referred to as deterministic), It does not cause any observable side effects

* If our function reads external files, it’s not a pure function — the file’s contents can change

* Any function that relies on a random number generator cannot be pure.

* It does not cause any observable side effects  .
Examples of observable side effects include modifying a global object or a parameter passed by reference.

   `pure functions + immutable data = referential transparency`

 Functions as first-class entities can:
- refer to it from constants and variables .
- pass it as a parameter to other functions .
- return it as result from other functions .

example:
* not pure:

```js
let counter = 1;
function increaseCounter (value) {counter = value + 1;}
increaseCounter(counter);
console.log(counter); // 2
```

* pure:

```js
let counter = 1;
function increaseCounter (value) { value + 1;}
increaseCounter(counter); // 2
console.log(counter); // 1
```

### Pure functions benefits

* Immutability

Unchanging over time or unable to be changed.
When data is immutable, its state cannot change after it’s created. If you want to change an immutable object, you can’t. Instead, you create a new object with the new value.


### Refactoring JavaScript 

some straightforward to implement methods that can lead to easier-to-read code. 

* Cache variables 

* Check for Web APIs before implementing your own functionality

It's important to get your code right the first time because in many businesses there isn't much value in refactoring. Or at least, it's hard to convince stakeholders that eventually uncaged for codebase will grind productivity to a halt.

* Filter :The filter function expects a true or false value to determine if the element should or should not be included in the result collection.

* Map : transforms a collection by applying a function to all of its elements and building a new collection from the returned values.

* Reduce :to receive a function and a collection, and return a value created by combining the items.