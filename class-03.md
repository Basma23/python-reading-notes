# Reading and Writing Files in Python

## What Is a File?

**A file** is a contiguous set of bytes used to store data. This data is organized in a specific format and can be anything as simple as a text file or as complicated as a program executable. In the end, these byte files are then translated into binary 1 and 0 for easier processing by the computer.

**Files on most modern file systems are composed of three main parts:**

- Header: metadata about the contents of the file (file name, size, type, and so on)

- Data: contents of the file as written by the creator or editor

- End of file (EOF): special character that indicates the end of the file

What this data represents depends on the format specification used, which is typically represented by an extension. 

## File Paths

When you access a file on an operating system, a file path is required. The file path is a string that represents the location of a file. It’s broken up into three major parts:

1- Folder Path: the file folder location on the file system where subsequent folders are separated by a forward slash / (Unix) or backslash \ (Windows)

2- File Name: the actual name of the file

3- Extension: the end of the file path pre-pended with a period (.) used to indicate the file type

# Python Exceptions

A Python program terminates as soon as it encounters an error. In Python, an error can be a syntax error or an exception. In this article, you will see what an exception is and how it differs from a syntax error. After that, you will learn about raising exceptions and making assertions. Then, you’ll finish with a demonstration of the try and except block.

## Exceptions versus Syntax Errors

**Syntax errors** occur when the parser detects an incorrect statement.

**Exception error** occurs whenever syntactically correct Python code results in an error.

## Raising an Exception

We can use raise to throw an exception if a condition occurs. The statement can be complemented with a custom exception.