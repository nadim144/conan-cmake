# Chapter-1 Introduction to python

### Why python?
***
* Python is dynamically typed langauage, where C/C++ are statically type language.. 
* python is cross functional (Windows/Linux/MacOS) means program portability - porting program to new platform ussally need only cut and paste. This is true even for GUI, DB Access, Web programming, OS interfacing and Directory access.
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
**Answer**: python supports all `4` programming models
1. Function programming model
1. Procedural programming model
1. Object-oriented programming model
1. Event-driven programming model

# Chapter-2 Getting Started
There are different python implementations are: [To-Do]
- **`CPython`**: CPython is the reference implementation of the Python programming language, CPython compiles Python code into bytecode before interpreting it. It's compatible with various Python packages and modules
- **`PyPy`**: 
- **`Jython`**: 
- **`IronPython`**: 

`Note:` All the implementations are compiler as well as interpreters. The compiler convert the python program into intermediate bytecode. Then the intepreter interprets this bytecode

### **Python Installation under Windows.**
Please follow this link: [Python Installation under Windows](https://www.digitalocean.com/community/tutorials/install-python-windows-10)

### **Python Installation under Linux (Ubuntu 24.04 LTS)**
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
[To Do] - It might be you think why C/C++ compilation process is required to know. because we are comparing statically type vs dynamic type language.
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

## **Identifiers and Keywords**
+ Python is a case sensetive language, and python identifier is a name used to identify a variable, funtion, class, module and other objects.
+ python has 35 keywords and all keywords are in lowercase.

![alt text](https://i.pinimg.com/originals/6d/70/99/6d7099fda7524830e6ceaf840b97974a.jpg)

**I have one idea,** why not let's print the kywords list. So, below is program which print the list of keyword available in python. 

expand the chapter-3 folder and inside that you will find keywords.py file and execute. 

**`Program 3.1`**

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

## **Python Data Types**
Python supports **three (3)** categories of **data types**.

+ **`Basic data type:`** **int**, **float**, **complex**, **bool**, **string**, and **bytes** 
+ **`Container type:`** **list**, **tuple**, **set** and **dict**
+ **`User-define type:`** **class**

### **Basic data type:**
There are different basic data types in python are **int**, **float**, **complex**, **bool**, **string**, and **bytes** 

Let's discuss it one by one. start with **int** means **integer** types. In python **integer** data type can be express in the form of **Binary**, **Decimal**, **Octal** and **Hexadecimal**. 
+ Where Binary will start with **0b/0B** example: **0b10111** or **0B10111**
+ Decimal is normal decimal value like: **156**
+ And **Octal** will start with **0o/0O** example - **0o432** or **0O432**
+ And last Hexadecimal will start with **0x/0X** example - **0x4A3** or **0X4A3**

**float** basic data type can be express in **fractional** or **exponential** form. as an example - **314.1528**, **3.141528e2** and **3.141528E2**

**complex** basic data type contains **real** and **imaginary** part. as an example - **3+2j** where **3** is real part and **2j** is imaginary part.

**bool** basic data type can have any of two boolean value **True** and **False**, firs character of value will capital.

**string** basic data type is and immutable collection of unicode characters enclosed within **' '**, **" "**, **""" """**. examples - **'Md Nadim Ahmad'**, **"Md Nadim Ahmad"** and **"""Md Nadim Ahmad"""**.

**byte** basic data type is **[To Do]**

**`Note:`** Type of data type can be found using **type()** function. Let undersatnad with examples. 

**`Program 3.2`**

**Write a program to find the data type of following values:**
- 35 
- 31.4 
- Nadim

expand the chapter-3 folder and you will find **finddatatype.py** file.
```
i = 35;
detectedtypeof = type(i);
print(detectedtypeof);

d = 3.14
print(type(d));

str = "Nadim";
print(type(str));
```
Let's understand program line by line. first of all to execute this program we don't required to import module as we did  earlier **import sys** and **import keyword** in past two program respectively in chapter-2 (version.py) and chapter-3 (kyword.py). 

**For the 35**, I taken one variable **i** and assign value **35** in it and taken another variable **detectedtypeof** which get assign by return value of **type(i)** and next we print the **detectedtypeof** which output will **<class 'int'>** because 35 is interger value.

**For the 3.14,** I optimize online of code, instead of creating extra variable "detectedtypeof" directly we pass **type(d)** into **print()** method. where **d** is variable which get assign by the value **3.14**. and which output will be **<class 'float'>**, because 3.14 is float value.

**For Nadim**, same as 3.14. and output will be **<class 'str'>**, beacuse Nadim is a string value. 

**Now, Let see the output:** I executed this program on Windows, however on Linux the output will be same.
```
PS D:\let-us-python\chapter-3> python .\finddatatype.py
<class 'int'>
<class 'float'>
<class 'str'>
```
