# Readings: Testing and Modules

![](https://files.realpython.com/media/unittest.mock-Tutorial_Watermarked.8e92b54478af.jpg)

## Unit tests:
Unit tests are some pieces of code to exercise the input, the output and the behaviour of your code. You can write them anytime you want.our code will be more reliable: after a change you can run your tests and be in peace

## TDD :
Test-Driven Development is a strategy to think (and write!) tests first. More than any checking, we need to think about our software design first.

## Unit testing Cycle

- 🆘 Write a unit test and make it fail (it needs to fail because the feature isn’t there, right? If this test passes, call the Ghostbusters, really)

- ✅ Write the feature and make the test pass! (you can dance after that)
- 🔵 Refactor the code — the first version doesn’t need to be the beautiful one (don’t be shy)


----------------------------------------------------------------
## Modular programming:
 Modular programming is the process of breaking a large, unwieldy programming task into separate, smaller, more manageable subtasks or modules. 

## advantages to modularizing:

- Simplicity: Easier to understand and debug the code. Easier to understand and debug the code.Rather than focusing on the entire problem at hand, a module typically focuses on one relatively small portion of the problem.

- Maintainability: Modules are typically designed so that they enforce logical boundaries between different problem domains.

- Reusability: can be used in several different parts of a program, or even in several different programs. This eliminates the need to recreate duplicate code.

- Scoping: Modules typically define a separate namespace, which helps avoid collisions between identifiers in different areas of a program.

----------------------------------------------------------------

## Recursion
![](https://res.cloudinary.com/practicaldev/image/fetch/s--KA7Ky3uR--/c_imagga_scale,f_auto,fl_progressive,h_420,q_auto,w_1000/https://dev-to-uploads.s3.amazonaws.com/i/226xc0p9pgtgadnin92j.jpeg)

### What is Recursion? 
The process in which a function calls itself directly or indirectly is called recursion and the corresponding function is called as recursive function. Using recursive algorithm, certain problems can be solved quite easily.
### Why Use Recursion?
Most programming problems are solvable without recursion. So, strictly speaking, recursion usually isn’t necessary.

However, some situations particularly lend themselves to a self-referential definition—for example, the definition of ancestors shown above. If you were devising an algorithm to handle such a case programmatically, a recursive solution would likely be cleaner and more concise.
![](https://files.realpython.com/media/Thinking-Recursively-in-Python_Watermarked.1825397c00ea.jpg)

### How a particular problem is solved using recursion? 
The idea is to represent a problem in terms of one or more smaller problems, and add one or more base conditions that stop the recursion. For example, we compute factorial n if we know factorial of (n-1). The base case for factorial would be n = 0. We return 1 when n = 0. 

