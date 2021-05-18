# Readings: Game of Greed 2

## Python Scope & the LEGB Rule: 

- there are two main scops :

    * Global scope: The names that you define in this scope are available to all your code.

    * Local scope: The names that you define in this scope are only available or visible to the code within the scope.

## Names and Scopes in Python

![](https://www.pythontutorial.net/wp-content/uploads/2020/11/Python-nonlocal-Scopes-nonlocal-variable-lookup.png)

Python is a dynamically-typed language, variables in Python come into existence when you first assign them a value

## Using the LEGB Rule for Python Scope

- Functions: The Local Scope

The local scope or function scope is a Python scope created at function calls.

- Nested Functions: The Enclosing Scope

Enclosing or nonlocal scope is observed when you nest functions inside other functions.

- Modules: The Global Scope :

From the moment you start a Python program, you’re in the global Python scope. Internally, Python turns your program’s main script into a module called main to hold the main program’s execution. The namespace of this module is the main global scope of your program.

- built-in:

scope is a special Python scope that’s created or loaded whenever you run a script or open an interactive session.
