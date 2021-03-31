# JavaScript
![](https://felixgerschau.com/static/3b5ee87f7f9649ddf41cb045cbc962f8/5a190/event-loop-cover.png)

## JavaScript Call Slack

A call stack is a mechanism for an interpreter (like the JavaScript interpreter in a web browser) to keep track of its place in a script that calls multiple functions — what function is currently being run and what functions are called from within that function.

Data structure that uses (LIFO): When we say that the call stack, operates by the data structure principle of Last In, First Out, it means that the last function that gets pushed into the stack is the first to be pop out, when the function returns.

The JavaScript engine (which is found in a hosting environment like the browser), is a single-threaded interpreter comprising of a heap and a single call stack. The browser provides web APIs like the DOM, AJAX, and Timers.

1. It is single-threaded. Meaning it can only do one thing at a time.
2. Code execution is synchronous.
3. A function invocation creates a stack frame that occupies a temporary memory.
4. It works as a LIFO — Last In, First Out data structure.

 **The call stack is primarily used for function invocation (call).**

```js
function firstFunction(){
  console.log("Hello from firstFunction");
}

function secondFunction(){
  firstFunction();
  console.log("The end from secondFunction");
}

secondFunction();
```
the output for the above function will be:

```
"Hello from firstFunction"
"The end from secondFunction"
```

The call slack list:
- secondFunction // first in

Then:
- firstFunction // last in, first out
- secondFunction

Then: 
- empty

### Slack overflow
calling a function inside itself (just like infinite loops)

### What causes a stack overflow?
A stack overflow occurs when there is a recursive function (a function that calls itself) without an exit point. 


----

## JavaScrip Errors

![](https://miro.medium.com/max/1600/1*iHhUyO4DliDwa6x_cO5E3A.gif)

### Errors Names :

1. Reference errors
2. Syntax errors
3. Range errors
4. Type errors


### Types of error messages:
- Reference errors:when you try to use a variable that is not yet declared you get this type of errors.
- Syntax errors:when you have something that cannot be parsed in terms of syntax.
- Range errors:when you  manipulate an object with some kind of length and give it an invalid length and this kind of errors will show up.
- Type errors:show up when the types (number, string and so on) you are trying to use or access are incompatible.


### Debugging and Handling Errors
The best way is to use `console.log()` or by putting a `debugger;` statement at the line of code you want to break.

*Don't forget to remove all `debugger;` lines before ACP*

