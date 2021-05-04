# Read:04 Topic

## Classes and Objects
![](https://res.cloudinary.com/dyd911kmh/image/upload/f_auto,q_auto:best/v1603476086/class2_b3ufes.png)

- __Objects__ :  are an encapsulation of variables and functions into a single entity. Objects get their variables and functions from classes.
- __Classes__  : are essentially a template "blue print" to create your objects.

### Accessing Object Variables
- we can do it using the name of object then the variable
### Accessing Object Functions

- we can do it using the name of object then the function

## Thinking Recursively in Python
![](https://files.realpython.com/media/fixing_problems.ffd6d34e887e.png)

### typical structure of a recursive algorithm:
 If the current problem represents a simple case, solve it. If not, divide it into sub-problems and apply the same strategy to them
 __A recursive function__: is a function defined in terms of itself via self-referential expressions.
  * This means that the function will continue to call itself and repeat its behavior until some condition is met to return a result
  
***When dealing with recursive functions, keep in mind that each recursive call has its own execution context***

## Pytest Fixtures and Coverage 

### Fixtures:
In pytest, you define fixtures using a combination of the pytest.fixture decorator, along with a function definition. For example, say you have a file that returns a list of lines from a file, in which each line is reversed:

### Coverage:
 its a package that will create a report with every part of the python library to the used program
