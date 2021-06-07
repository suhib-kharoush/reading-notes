# Python Exceptions: An Introduction:

- A Python program terminates as soon as it encounters an error. In Python, an error can be a syntax error or an exception. In this article, you will see what an exception is and how it differs from a syntax error.
![](https://files.realpython.com/media/intro.8915db1758d8.png)

- Raising an Exception:
!(https://files.realpython.com/media/raise.3931e8819e08.png)

- The AssertionError Exception
![](https://files.realpython.com/media/assert.f6d344f0c0b4.png)

- The else Clause
![](https://files.realpython.com/media/try_except_else.703aaeeb63d3.png)

- Cleaning Up After Using finally
![](https://files.realpython.com/media/try_except_else_finally.a7fac6c36c55.png)

# Reading and Writing Files in Python:

- What Is a File?
- a file is a contiguous set of bytes used to store data. This data is organized in a specific format and can be anything as simple as a text file or as complicated as a program executable. In the end, these byte files are then translated into binary 1 and 0 for easier processing by the computer.

- Files on most modern file systems are composed of three main parts:
- 1. Header: metadata about the contents of the file (file name, size, type, and so on)
- 2. Data: contents of the file as written by the creator or editor
- 3. End of file (EOF): special character that indicates the end of the file
![](https://files.realpython.com/media/FileFormat.02335d06829d.png)

- File Paths:

- When you access a file on an operating system, a file path is required. The file path is a string that represents the location of a file. It’s broken up into three major parts:
- 1. Folder Path: the file folder location on the file system where subsequent folders are separated by a forward slash / (Unix) or backslash \ (Windows)
- 2. File Name: the actual name of the file
- 3. Extension: the end of the file path pre-pended with a period (.) used to indicate the file type

- Here’s a quick example. Let’s say we have a file located within a file structure like this:
- /
- │
- ├── path/
- |   │
- │   ├── to/
- │   │   └── cats.gif
- │   │
- │   └── dog_breeds.txt
- |
- └── animals.csv