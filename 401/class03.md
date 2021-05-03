 # FileIO & Exceptions
![](https://dbader.org/static/figures/python-reading-writing-files.jpg)

 ### What is a file ?
 a file is a contiguous set of bytes used to store data. This data is organized in a specific format and can be anything as simple as a text file or as complicated as a program executable.

 ### Parts of the file :
- Header: metadata about the contents of the file (file name, size, type, and so on)
- Data: contents of the file as written by the creator or editor
- End of file (EOF): special character that indicates the end of the file

### What is a File Paths 
Folder Path: the file folder location on the file system where subsequent folders are separated by a forward slash / (Unix) or backslash \ (Windows)

### File Paths Parts :

- File Name: the actual name of the file
- Extension: the end of the file path pre-pended with a period (.) - - used to indicate the file type

### Opening and Closing a File in Python
1. Open :
    This is done by invoking the open() built-in function.
2. close :
    This is done by invoking the close() built-in function.

__Example__:
> reader = open('dog_breeds.txt')
>
> #or you can use => with open('dog_breeds.txt') as reader: 
>
> try:
>
>     # Further file processing goes here
> finally:
>
>     reader.close()

### options for file mode : 

|                               Character#                                   |                             Meaning                              |
| :-----------------------------------------------------------------------: | :-----------------------------------------------------------: |
|'r' | ''	Open for reading (default)  |
|'w' |	Open for writing, truncating (overwriting) the file first |
|'rb' or 'wb' |Open in binary mode (read/write using byte data) |

-----------------------

# Python Exceptions
![](https://techvidvan.com/tutorials/wp-content/uploads/sites/2/2020/07/exception-handling-in-python.jpg)

Expections happen when the python code is syntactically correct but u run into an error (the last line of the error tells you what type of exception it is)

## Raising an exception 
raise allows you to throw an exception at any time.


## The AssertionError Exception
assert enables you to verify if a certain condition is met and throw an exception if it isn’t.

 ## The try and except Block: Handling Exceptions
 
- In the try clause, all statements are executed until an exception is encountered.

- except is used to catch and handle the exception(s) that are encountered in the try clause.


## The else Clause
In Python, using the else statement, you can instruct a program to execute a certain block of code only in the absence of exceptions.
else lets you code sections that should run only when no exceptions are encountered in the try clause.

## finally
 finally enables you to execute sections of code that should always run, with or without any previously encountered exceptions.
 Everything in the finally clause will be executed it doesn't matter if u run into an exception 