# Chapter-1 Introduction to python

### Why python?
***
* Python is not a statically typed language, it is dynamically typed. 
* python is cross functional means program portability - porting program to new platform ussally need only cut and paste. This is true even for GUI, DB Access, Web programming, OS interfacing and Directory access.
* strong libray support from text matching to networking and vast collection of third-party libraries.
* very easy to component integration.

### Where is python used?
***
1. System programming
1. Building GUI application (using TkInter oe WxWidget framework)
1. Scripting program
1. Component Integration
1. Databse programming
1. Numeric and scientific application
1. Game programming
1. Robotics programming (CAN signal end-to-end testing using robotframework)

### What programming model does python supports?
***
**Answer**: python supports all **`4`** programming models
1. Function programming model
1. Procedural programming model
1. Object-oriented programming model
1. Event-driven programming model

# Chapter-2 Getting Started
There are different python implementations are: (Need-to-update/To-Do)
- **`CPython`**: CPython is the reference implementation of the Python programming language, CPython compiles Python code into bytecode before interpreting it. It's compatible with various Python packages and modules
- **`PyPy`**: 
- **`Jython`**: 
- **`IronPython`**: 

`Note:` All the implementations are compiler as well as interpreters. The compiler convert the python program into intermediate bytecode. Then the intepreter interprets this bytecode

### **-- Python Installation under Windows.**
Please follow this link: [Python Installation under Windows](https://www.digitalocean.com/community/tutorials/install-python-windows-10)

### **-- Python Installation under Linux (Ubuntu 24.04 LTS)**
Please follow this link: [Python Installation under Linux (Ubuntu 24.04 LTS)](https://phoenixnap.com/kb/how-to-install-python-3-ubuntu)

After installation of python on your respective OS (Windows/Linux) on your preference. I would reccomend to learn something about package, What is package and who create pakage and how it available for end users? `Here package means Third-party pakage.`

### **Third-party package**

+ Pythonist in python community create packages (libraries) and make them available for use for other programmers. They use `PyPI` - Python package index ([www.pypi.org](https://pypi.org/)) to distribute their packages. PyPI maintains the list such third-party python packages available.
+ There are third-party packages available for literally doing everything under the roof. Some packages that are popularly used for creating **Data Science** applications include:
    + **NumPy :** NumPy is advanced mathematical operations library with support for large multi-dimensional arrays and matrices.
    + **SciPy :** SciPy is a scientific computing library for **Optimization**, **Integration**, **Interpolation**, **Signal processing**, **Image processing**, etc.
    + **Pandas :** Pandas library is used for manipulating **numerical tables** and **times series**
    + **MatPlotLib :** MatPlotLib is used for **2D** and **3D** data visualization.
    + **OpenCV :** OpenCV is open source **Computer Vision** libarary. it it used for computer vision programs

+ You too can register at `PyPI` and upload your packages there. You should follow the guidelines given at  ([www.pypi.org](https://pypi.org/)) to create the package, build it and upload it to the **Python Package Index.**
+ **`pip`** is commonly used tool for installing packages from **`PyPi`**. This tool get installed when you install Python for Windows.

### **Compilation Approach in C/C++.**
[To Do]
### **Compilation Approach in Python.**
[To Do]

**After all this.** Let's write our first program in python. Usally in C/C++ programming laguage we write **Hello World!** program. But here, as a our first python program I would like to differ from traditional **Hello World** program. Instead of that, I would prefer wirte our first python program to find which **version of python** is install in out machine either Windows/Linux.

Let's open VS code and create a folder, named as **[chapter-2]** and inside that folder create a python file named as **version.py**

**`Note:`** In Python `semicolon (;)` is completlly optional, either you put or not put at the end of statement it is upto you. if you are C/C++ programming background then probably you are habituate putting semicolon at the end. if you doesn't put, It doesn't impact on you program. I have written both version of code with semicolon and without semicolon. Both version will work fine. Trust me. 

**With semicolon (;)**
```
import sys;
print(sys.version);
```
**Without semicolon (;)**
```
import sys
print(sys.version)
```
Let, first interpret the our first program on both Windows and Linux and see the output. 

**Windows:**
+ Open command line terminal either from VS Code or actual cmd.
+ Navigate to the **\let-us-python\chapter-2>** folder.
+ Run this command as: **\let-us-python\chapter-2> python .\version.py**
> PS D:\let-us-python\chapter-2> python .\version.py

Output:
```
3.13.0 (tags/v3.13.0:60403a5, Oct  7 2024, 09:38:07) [MSC v.1941 64 bit (AMD64)]
```

**Linux:**
> mna@DESKTOP-194LI0R:/mnt/d/let-us-python/chapter-2$ python3 version.py 

```
3.12.3 (main, Sep 11 2024, 14:17:37) [GCC 13.2.0]
```
# Chapter-3 Python Basics

### **Identifiers and Keywords**
+ Python is a case sensetive language, and python identifier is a name used to identify a variable, funtion, class, module and other objects.
+ python has 35 keywords and all keywords are in lowercase.

![alt text](https://i.pinimg.com/originals/6d/70/99/6d7099fda7524830e6ceaf840b97974a.jpg)

**I have one idea,** why not let's print the kywords list. So, below is program which print the list of keyword available in python. 

expand the chapter-3 folder and inside that you will find keywords.py file and execute. 

**`Program 2.1`**

**Write a program to print the list of keywords in python available.**

```
import keyword
print(keyword.kwlist)
```
+ To print the list of keyword we need to import the **`keyword`** module
+ Then after print the keyword list, using **`print(keyword.kwlist)`**

Lets execute the program on Windows and Linux.

**Windows :**
```
PS D:\let-us-python\chapter-3> python .\keywords.py
['False', 'None', 'True', 'and', 'as', 'assert', 'async', 'await', 'break', 'class', 'continue', 'def', 'del', 'elif', 'else', 'except', 'finally', 'for', 'from', 'global', 'if', 'import', 'in', 'is', 'lambda', 'nonlocal', 'not', 'or', 'pass', 'raise', 'return', 'try', 'while', 'with', 'yield']
```
**Linux :**
```
mna@DESKTOP-194LI0R:/mnt/d/let-us-python/chapter-3$ python3 keywords.py 
['False', 'None', 'True', 'and', 'as', 'assert', 'async', 'await', 'break', 'class', 'continue', 'def', 'del', 'elif', 'else', 'except', 'finally', 'for', 'from', 'global', 'if', 'import', 'in', 'is', 'lambda', 'nonlocal', 'not', 'or', 'pass', 'raise', 'return', 'try', 'while', 'with', 'yield']
```

**`Note:`** if you observe that, we written program to print the list of keyword, and output is coming in list form, In python we define list as in square brackate **[]**. 