# Introduction to Python
## Why Python

<img src="figures/programming_languages_recommended.png" alt="Python" width="70%" align="center"/>

https://businessoverbroadway.com/2019/01/13/programming-languages-most-used-and-recommended-by-data-scientists/


-  Python is extremely popular and widely used, especially for data science.
    +  Popular and getting more so in Bioinformatics, especially for building tools.
    +  For analysis, R is arguably more useful currently due to the huge number of packages available from [Bioconductor](http://bioconductor.org/) and [CRAN](https://cran.r-project.org/).
    +  The best option is to learn [Python, R, and bash](http://omgenomics.com/programming-languages/). A little of each will go a long way.
-  Freely available to [download](https://www.python.org/downloads/) for Windows, Linux, Mac OS X, etc.
-  Python is extremely versatile
    +  Used for a wide range of purposes from automating simple tasks to massive software projects with wide adoption [by many large companies.](https://realpython.com/world-class-companies-using-python/)
-  Installed on almost every Linux server.
-  Vast number of resources online: If you can Google for it you can learn how to do it.


------

##  Background

###  What is a programming language and why do we need it?

Speaking to a computer in its native language is tedious and complicated. A programming language is a way for humans to describe a set of operations to a computer in a more abstract and understandable way. A helper program then translates our description of the operations into a set of instructions (machine code) for the computer to carry out.<br>

Some day we may develop a programming language that allows us to communicate our instructions to the computer in our native language (Alexa, turn on the TV). Except for simple cases, this option doesn't exist yet, largely because human languages are complicated and instructions can be difficult to understand (even for other humans).

In order for the helper program to work properly, we need to use a concise language:
-  Well defined vocabulary for describing the basic set of supported operations.
-  Well defined set of Data Types that have a defined set of valid operations (add, subtract, etc).
-  Well defined syntax that leaves no ambiguity about when the computer should carry out each instruction.

Specifically in Python:

<img src="figures/python_interpreter.png" alt="PythonInterpreter" width="90%" align="center"/> <br><br>



-----

### A brief history of Python
-  Initially developed during the late 1980's by [Guido van Rossum](https://en.wikipedia.org/wiki/Guido_van_Rossum), BDFL until 2018.
-  First development version released in 1991. Version 1 released in 1994.
-  Python 2.0.0 released June, 2001
    -  Python 2.x end-of-life Jan 1, 2020.
    -  This version was so popular and widely used that many Bioinformatics programs were written using it. Some of these tools have been converted to support v3.x, others are in the process of being upgraded or have been abandoned and will stay on v2.x. The last Python 2.x release is still available for [download](https://www.python.org/downloads/release/python-2718/).
-  Python 3.x (December 2008) was a significant re-design and broke compatibility with some parts of v2.x.
-  The current version is 3.14.

-----

### Interesting features of Python
-  High level: It hides a lot of the complicated details.
-  Interpreted: programs are compiled to byte code and run on a virtual machine instead of being compiled to native machine language
    -  This provides the option of running Python interactively, or writing Python scripts.
-  Garbage Collected: memory is allocated and freed for you automatically
-  Spaces matter in Python and are part of the language syntax. Be careful with copy/paste!
-  In Python, "Readability counts".
    *  There is a style guide called [Python Enhancement Proposal 8 (PEP8)](https://www.python.org/dev/peps/pep-0008/) that documents and encourages consistent, readable code. If you plan to share your code with others, it is good practice to follow the style guide (or adopt the style used by the rest of the team).
    *  These best practices are also known as writing "pythonic" or "idiomatic" python, [this guide](https://docs.python-guide.org/writing/style/) has more details. Try ```import this``` in your Python interpreter if you are a fan of programmer philosophy.

----

### Base Python and the extensive package ecosystem
-  Python has been extremely successful partly because it is modular and highly extensible. The core of Python is relatively small and compact, but this is supplemented with a large ["standard library"](https://docs.python.org/3/library/) that adds a large amount of additional functionality.
    +  Thousands of additional packages are available from the [PyPI](https://pypi.org/) repository.
    +  PythonPath variable
    +  Where do libraries live?
    +  Virtual Environments
    +  Conflicts and package versions
        -  Virtual environments
        -  Conda


-----

## Project Jupyter
- Developed for interactive data science and scientific computing across all programming languages
- Non-profit, open-source
- Free

<img src="figures/jupyter_intro.png" alt="Jupyter" width="70%" align="center"/>

-----

## Disclaimer
**Learning all the nuances of python takes a long time! Our goal here is to introduce you to as many concepts as possible
but if you are serious about mastering python you will need to apply yourself beyond this introduction.**

## Hello World!


```python
print("Hello World!")
```

    Hello World!


## Basic Data Types
### Built in data types

<style>
/* Default table styling */
table {
    border-collapse: collapse;
    margin: 20px auto;
    font-family: 'Arial', sans-serif;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
    background-color: white;
}

/* Different width classes */
.table-30 {
    width: 30%;
}

.table-50 {
    width: 50%;
}

.table-70 {
    width: 70%;
}

.table-full {
    width: 100%;
}

/* Header styling */
th {
    background-color: #2c3e50;
    color: white;
    padding: 12px 15px;
    text-align: center;
    font-weight: bold;
    border: 1px solid #34495e;
}

/* Cell styling */
td {
    padding: 10px 15px;
    text-align: center;
    border: 1px solid #ddd;
    color: #333;
}

/* Hover effect for rows */
tbody tr:hover {
    background-color: #f5f5f5;
    transform: scale(1.02);
    transition: all 0.3s ease;
    cursor: pointer;
}

/* Alternating row colors */
tbody tr:nth-child(even) {
    background-color: #f9f9f9;
}

tbody tr:nth-child(odd) {
    background-color: white;
}

/* Hover effect for individual cells */
td:hover {
    background-color: #e8f4f8;
}

/* Add smooth transitions */
td, tr {
    transition: background-color 0.2s ease, transform 0.2s ease;
}
</style>

<div class="table-30">
| Data type | Functions |
| :-: | :-: |
| Text/Character | str() |
| Numeric | int(), float(), complex() |
| Sequence | list[], tuple()/(), range() |
| Mapping | dict()/{} |
| Set | set()/{}, frozenset() |
| Boolean | bool() |
| Binary | bytes(), bytearray(), memoryview() |
| None | None |
</div>


### Integers, Floating-point numbers, booleans, strings.

<div class="table-50">
| Language | Python | R |
| :-: | :-: | :-: |
| Integer data | int() | as.integer(), integer() |
| Float data | float() | numeric() |
| Logical data | bool(), [True, False] | as.logical(), logical(), (TRUE, FALSE) |
| Character data | str() | as.character(), character() |
</div>

#### Integer


```python
a = int(5)
```


```python
a
```




    5




```python
b = 5
```


```python
b
```




    5




```python
type(a)
```




    int




```python
type(b)
```




    int



#### Arithmetic operators
<img src="figures/operators.png" alt="if flow" width="600px"/>

#### Exercise
Creat different data types and perform some operations.

### Sequence data

<div class="table-70"></div>
| Data type | Usage | Characteristics |
| :-: | :-: | :-: |
| Lists | Store multiple items in a single variable | Ordered, mutable, allow duplicate values |
| Tuples | Store multiple items in a single variable | Ordered, immutable, allow duplicate values |
| Range | Create an immutable sequence of numbers | Immutable, a range of integers |
</div>


__*Immutable* means that an object's state or value cannot be changed after its creation.__


```python
range1 = range(6)
```


```python
range1[0]
```




    0




```python
range1[0] = 3
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    Cell In[16], line 1
    ----> 1 range1[0] = 3


    TypeError: 'range' object does not support item assignment



```python
range1
```




    range(0, 6)




```python
len(range1)
```




    6




```python
range1[5]
```




    5




```python
range1[6] = 8
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    Cell In[20], line 1
    ----> 1 range1[6] = 8


    TypeError: 'range' object does not support item assignment



```python

```
