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

## <font color='darkred'>Disclaimer</font>
**Learning all the nuances of python takes a long time! Our goal here is to introduce you to as many concepts as possible
but if you are serious about mastering python you will need to apply yourself beyond this introduction.**

## Installation
We are going to use a python distribution platform, Anaconda. It was designed to meet the demand of Data Sciences and AI projects. It can be installed on all three operating systems and has 45 million users as of 2024. It includes over 300 packages, offers jupyter Notebooks and jupyter Lab and includes _conda_, the package and environment manager. It makes installing a lot of python packages very easy. Please follow the instructions below to install Anaconda. Instructions for all platforms can be found at <https://www.anaconda.com/docs/getting-started/anaconda/install>
- Macs: Two options are available. One is to use the graphic installer. The other is to use the Command Line installer.
  - For graphic installer, please go to <https://www.anaconda.com/download> and follow the instructions in the "Download Now" panel. This option installs Anaconda in /opt/anacondas in the file system. In order to install Anaconda into your Home directory (especially in the case where there are multiple users), Command Line installation is recommended.
  - For Command Line installer
    - Mac Arm architecture
      - Download: wget https://repo.anaconda.com/archive/Anaconda3-2025.06-0-MacOSX-arm64.sh
      - Install: bash ~/Anaconda3-2025.06-0-MacOSX-arm64.sh
    - Mac Intel architecture
      - Download: wget https://repo.anaconda.com/archive/Anaconda3-2025.06-0-MacOSX-x86_64.sh
      - Install: bash ~/Anaconda3-2025.06-0-MacOSX-x86_64.sh
- Linux:
  - Download: wget https://repo.anaconda.com/archive/Anaconda3-2025.06-0-Linux-x86_64.sh
  - Install: bash ~/Anaconda3-2025.06-0-Linux-x86_64.sh
- Windows: Please install in your ubuntu subsystem so that conda is available for installing other python packages later
  - Download: wget https://repo.anaconda.com/archive/Anaconda3-2025.06-0-Linux-x86_64.sh
  - Install: bash ~/Anaconda3-2025.06-0-Linux-x86_64.sh

After Anaconda is successfully installed, please open a new Command Line interface to see the effect.

## Hello World!

**[Input:]**

```python
print("Hello World!")
```

**[Output:]**

```
Hello World!
```

---

## Functions and how to find help
As in any other programming language, a function is a predefined set of operations. In order to find the information on what parameters a function requires, one has 2 options:
- use the help() function
- use _shift_ + _tab_

**[Input:]**

```python
help(print)
```

**[Output:]**

```
Help on built-in function print in module builtins:

print(*args, sep=' ', end='\n', file=None, flush=False)
    Prints the values to a stream, or to sys.stdout by default.

    sep
      string inserted between values, default a space.
    end
      string appended after the last value, default a newline.
    file
      a file-like object (stream); defaults to the current sys.stdout.
    flush
      whether to forcibly flush the stream.

```

---

_*args_ means that the function _print_ can accept any number of arguments.

## Basic Data Types
### Built in data types

<style>
/* Custom table style */
table.custom-table {
    border-collapse: collapse;
    margin: 20px auto; 
    width: 40%;
    font-size: 15px;
    border: 2px solid #444;
}

table.custom-table th {
    background: #2d2d2d;
    color: white;
    padding: 8px 12px;
    border: 1px solid #555;
    text-align: center;
}

table.custom-table td {
    padding: 8px 12px;
    border: 1px solid #999;
    text-align: center;
}

table.custom-table tbody tr:nth-child(even) {
    background-color: #f9f9f9;
}

table.custom-table tbody tr:nth-child(odd) {
    background-color: white;
}

table.custom-table tr:hover {
    background-color: #f5f5f5;
    transform: scale(1.02);
    transition: all 0.3s ease;
    cursor: pointer;
}
</style>

<table class="custom-table">
<thead>
<tr>
    <th>Data type</th>
    <th>Functions</th>
</tr>
</thead>

<tbody>
<tr><td>Text/Character</td><td>str()</td></tr>
<tr><td>Numeric</td><td>int(), float(), complex()</td></tr>
<tr><td>Sequence</td><td>list()/[], tuple()/(), range()</td></tr>
<tr><td>Mapping</td><td>dict()/{} </td></tr>
<tr><td>Set</td><td>set()/{}, frozenset()</td></tr>
<tr><td>Boolean</td><td>bool()</td></tr>
<tr><td>Binary</td><td>bytes(), bytearray(), memoryview()</td></tr>
<tr><td>None</td><td>None</td></tr>
</tbody>
</table>


### Integers, Floating-point numbers, booleans, strings.

<style>
/* Custom table style */
table.width-50 {
    border-collapse: collapse;
    margin: 20px auto; 
    width: 50%;
    font-size: 15px;
    border: 2px solid #444;
}

table.width-50 th {
    background: #2d2d2d;
    color: white;
    padding: 8px 12px;
    border: 1px solid #555;
    text-align: center;
}

table.width-50 td {
    padding: 8px 12px;
    border: 1px solid #999;
    text-align: center;
}

table.width-50 tbody tr:nth-child(even) {
    background-color: #f9f9f9;
}

table.width-50 tbody tr:nth-child(odd) {
    background-color: white;
}

table.width-50 tr:hover {
    background-color: #f5f5f5;
    transform: scale(1.02);
    transition: all 0.3s ease;
    cursor: pointer;
}
</style>

<table class="width-50">
<thead>
<tr>
    <th>Language</th>
    <th>Python</th>
    <th>R</th>
</tr>
</thead>

<tbody>
<tr>
    <td>Integer data</td>
    <td>int()</td>
    <td>as.integer(), integer()</td>
</tr>

<tr>
    <td>Float data</td>
    <td>float()</td>
    <td>numeric()</td>
</tr>

<tr>
    <td>Logical data</td>
    <td>bool(), [True, False]</td>
    <td>as.logical(), logical(), (TRUE, FALSE)</td>
</tr>

<tr>
    <td>Character data</td>
    <td>str()</td>
    <td>as.character(), character()</td>
</tr>
</tbody>
</table>


#### Integer

**[Input:]**

```python
a = int(5)
```

---

**[Input:]**

```python
a
```

**[Output:]**

```
5
```

---

**[Input:]**

```python
b = 5
```

---

**[Input:]**

```python
b
```

**[Output:]**

```
5
```

---

**[Input:]**

```python
type(a)
```

**[Output:]**

```
int
```

---

**[Input:]**

```python
type(b)
```

**[Output:]**

```
int
```

---

#### Arithmetic operators
<img src="figures/operators.png" alt="if flow" width="600px"/>

#### <font color='blue'>Exercise</font>
Creat different data types (integers, floats, booleans and strings) and perform some operations.

## Sequence data

<style>
/* Custom table style */
table.width-70 {
    border-collapse: collapse;
    margin: 20px auto; 
    width: 70%;
    font-size: 15px;
    border: 2px solid #444;
}

table.width-70 th {
    background: #2d2d2d;
    color: white;
    padding: 8px 12px;
    border: 1px solid #555;
    text-align: center;
}

table.width-70 td {
    padding: 8px 12px;
    border: 1px solid #999;
    text-align: center;
}

table.width-70 tbody tr:nth-child(even) {
    background-color: #f9f9f9;
}

table.width-70 tbody tr:nth-child(odd) {
    background-color: white;
}

table.width-70 tr:hover {
    background-color: #f5f5f5;
    transform: scale(1.02);
    transition: all 0.3s ease;
    cursor: pointer;
}
</style>

<table class="width-70">
<thead>
<tr>
    <th>Data type</th>
    <th>Usage</th>
    <th>Characteristics</th>
</tr>
</thead>

<tbody>
<tr>
    <td>Lists</td>
    <td>Store multiple items in a single variable</td>
    <td>Ordered, mutable, allow duplicate values</td>
</tr>

<tr>
    <td>Tuples</td>
    <td>Store multiple items in a single variable</td>
    <td>Ordered, immutable, allow duplicate values</td>
</tr>

<tr>
    <td>Range</td>
    <td>Create an immutable sequence of numbers</td>
    <td>Immutable, a range of integers</td>
</tr>
</tbody>
</table>


__*Immutable* means that an object's state or value cannot be changed after its creation.__ Let's take a look at one example to understand what __immutable__ means in python. Here we will create a variable using **range()** function.

### Range

**[Input:]**

```python
range_example = range(6)
```

---

**[Input:]**

```python
range_example
```

**[Output:]**

```
range(0, 6)
```

---

**[Input:]**

```python
range_example[0]
```

**[Output:]**

```
0
```

---

**[Input:]**

```python
range_example[0] = 3
```

**[Output:]**

**Error:**

```
---------------------------------------------------------------------------
TypeError                                 Traceback (most recent call last)
Cell In[22], line 1
----> 1 range_example[0] = 3

TypeError: 'range' object does not support item assignment
```

---

**[Input:]**

```python
range_example[5]
```

**[Output:]**

```
5
```

---

**[Input:]**

```python
range_example[6] = 8
```

**[Output:]**

**Error:**

```
---------------------------------------------------------------------------
TypeError                                 Traceback (most recent call last)
Cell In[24], line 1
----> 1 range_example[6] = 8

TypeError: 'range' object does not support item assignment
```

---

Range function is usually used in a for loop. For example,

**[Input:]**

```python
protein_seq = "MTKAAVGLVKNRAWGIPSDF"
protein_len = len(protein_seq)
for i in range(protein_len):
    print(f"The ", i+1, "th amino acid is: ", protein_seq[i])

```

**[Output:]**

```
The  1 th amino acid is:  M
The  2 th amino acid is:  T
The  3 th amino acid is:  K
The  4 th amino acid is:  A
The  5 th amino acid is:  A
The  6 th amino acid is:  V
The  7 th amino acid is:  G
The  8 th amino acid is:  L
The  9 th amino acid is:  V
The  10 th amino acid is:  K
The  11 th amino acid is:  N
The  12 th amino acid is:  R
The  13 th amino acid is:  A
The  14 th amino acid is:  W
The  15 th amino acid is:  G
The  16 th amino acid is:  I
The  17 th amino acid is:  P
The  18 th amino acid is:  S
The  19 th amino acid is:  D
The  20 th amino acid is:  F
```

---

### List
A list can be created by using the function **list()** or by simply using **()**.

**[Input:]**

```python
list_example = list(("NDUFAF7", "AGMAT", "TOP1MT", "IARS2", "MTFP1", "SLC25A51", "PRORP", "SLC25A52", "ENDOG"))
```

---

**[Input:]**

```python
list_example
```

**[Output:]**

```
['NDUFAF7',
 'AGMAT',
 'TOP1MT',
 'IARS2',
 'MTFP1',
 'SLC25A51',
 'PRORP',
 'SLC25A52',
 'ENDOG']
```

---

**[Input:]**

```python
len(list_example)
```

**[Output:]**

```
9
```

---

**[Input:]**

```python
type(list_example)
```

**[Output:]**

```
list
```

---

List is mutable, which means that one may modify the values of a list after its creation.

<table class="width-70">
<thead>
<tr>
    <th>Function</th>
    <th>Operation</th>
</tr>
</thead>

<tbody>
<tr>
    <td>append</td>
    <td>Add an element at the end of the list</td>
</tr>

<tr>
    <td>extend</td>
    <td>Add multiple elements at the end of the list</td>
</tr>

<tr>
    <td>insert</td>
    <td>Add an element at a specific position</td>
</tr>

<tr>
    <td>remove</td>
    <td>Remove the first occurrence of an element</td>
</tr>

<tr>
    <td>pop</td>
    <td>Removes an element at a specific position or the last element if no index is specified</td>
</tr>

<tr>
    <td>del</td>
    <td>Delete object</td>
</tr>
</tbody>
</table>



For example, let's add an element to **list_example**

**[Input:]**

```python
list_example.append("CKMT2")
list_example
```

**[Output:]**

```
['NDUFAF7',
 'AGMAT',
 'TOP1MT',
 'IARS2',
 'MTFP1',
 'SLC25A51',
 'PRORP',
 'SLC25A52',
 'ENDOG',
 'CKMT2']
```

---

We see a new syntax, __object.function()__. This is the way to call a method that is bound to an object in python. A method is a function that is defined specifically for an object of a class in python. In order to know what methods are bound to an object, we can use the following operation:
- methods = [method_name for method_name in dir(obj) if callable(getattr(obj, method_name)) and not method_name.startswith("__")]

**[Input:]**

```python
methods = [method_name for method_name in dir(list_example) if callable(getattr(list_example, method_name)) and not method_name.startswith("__")]
methods
```

**[Output:]**

```
['append',
 'clear',
 'copy',
 'count',
 'extend',
 'index',
 'insert',
 'pop',
 'remove',
 'reverse',
 'sort']
```

---

### <font color="blue">Exercise</font>
Let's modify __list_example__ by using the functions listed above, add element(s), delete element(s), ...

## Mapping data - Dictionaries
Dictionaries in python store data in __key:value__ pairs.
- An ordered collection (starting in python 3.7)
- Changable
- Do not allow duplicate keys
- Allows for fast key lookup
- Values can be any python data type

Syntax:<br>
{<br>
&nbsp;&nbsp;&nbsp;&nbsp;Key1: value1,<br>
&nbsp;&nbsp;&nbsp;&nbsp;Key2: value2,<br>
&nbsp;&nbsp;&nbsp;&nbsp;...,<br>
&nbsp;&nbsp;&nbsp;&nbsp;KeyN: valueN,<br>
}

**[Input:]**

```python
dict_example = {
    "gene_name": "CKMT2",
    "gene_biotype": "protein_coding",
    "n_transcripts": 32,
    "n_orthologues": 217,
    "n_paralogues": 4,
    "ensembl_id": "ENSG00000131730",
    "discription": "creatine kinase, mitochondrial 2",
    "loc": "Chromosome 5: 81,233,320-81,266,399",
    "strand": "+",}
dict_example
```

**[Output:]**

```
{'gene_name': 'CKMT2',
 'gene_biotype': 'protein_coding',
 'n_transcripts': 32,
 'n_orthologues': 217,
 'n_paralogues': 4,
 'ensembl_id': 'ENSG00000131730',
 'discription': 'creatine kinase, mitochondrial 2',
 'loc': 'Chromosome 5: 81,233,320-81,266,399',
 'strand': '+'}
```

---

### Access items in the dictionary
- The most intuitive way is to use the keys.

**[Input:]**

```python
dict_example["gene_name"]
```

**[Output:]**

```
'CKMT2'
```

---

But how do one know what keys there are in a dictionary object?

**[Input:]**

```python
methods = [method_name for method_name in dir(dict_example) if callable(getattr(dict_example, method_name))
           and not method_name.startswith("__")]
methods
```

**[Output:]**

```
['clear',
 'copy',
 'fromkeys',
 'get',
 'items',
 'keys',
 'pop',
 'popitem',
 'setdefault',
 'update',
 'values']
```

---

**[Input:]**

```python
dict_example.keys()
```

**[Output:]**

```
dict_keys(['gene_name', 'gene_biotype', 'n_transcripts', 'n_orthologues', 'n_paralogues', 'ensembl_id', 'discription', 'loc', 'strand'])
```

---

How does one extract the values of more than one key. For example, let's try to extract values of the first 5 keys, _gene_name_, _gene_biotype_, and _n_transcripts_. This can be done easily using a for loop.

**[Input:]**

```python
for key in ["gene_name", "gene_biotype", "n_transcripts"]:
    print(f"{key}: ", dict_example.get(key))
```

**[Output:]**

```
gene_name:  CKMT2
gene_biotype:  protein_coding
n_transcripts:  32
```

---

In another example, we are going to update the dictionary with an additional piece of information, using the method _update_.

**[Input:]**

```python
dict_example.update({"pathway": "Mitochondria disease pathway"})
dict_example
dict_example.update(pathway_members = 10)
dict_example
```

**[Output:]**

```
{'gene_name': 'CKMT2',
 'gene_biotype': 'protein_coding',
 'n_transcripts': 32,
 'n_orthologues': 217,
 'n_paralogues': 4,
 'ensembl_id': 'ENSG00000131730',
 'discription': 'creatine kinase, mitochondrial 2',
 'loc': 'Chromosome 5: 81,233,320-81,266,399',
 'strand': '+',
 'pathway': 'Mitochondria disease pathway',
 'pathway_members': 10}
```

---

Because the values can be any python data type, one may create nested dictionaries.

**[Input:]**

```python
nested_dict = {
    "ENSG00000131730": {
        "gene_name": "CKMT2",
        "gene_biotype": "protein_coding",
        "n_transcripts": 32,
        "n_orthologues": 217,
        "n_paralogues": 4,
        "ensembl_id": "ENSG00000131730",
        "discription": "creatine kinase, mitochondrial 2",
        "loc": "Chromosome 5: 81,233,320-81,266,399",
        "strand": "+",},
    "ENSG00000003509": {
        "gene_name": "NDUFAF7",
        "gene_biotype": "protein_coding",
        "n_transcripts": 20,
        "n_orthologues": 210,
        "n_paralogues": 0,
        "ensembl_id": "ENSG00000003509",
        "discription": "NADH:ubiquinone oxidoreductase complex assembly factor 7",
        "loc": "Chromosome 2: 37,231,631-37,253,403 ",
        "strand": "+",},
}
```

---

**[Input:]**

```python
nested_dict
```

**[Output:]**

```
{'ENSG00000131730': {'gene_name': 'CKMT2',
  'gene_biotype': 'protein_coding',
  'n_transcripts': 32,
  'n_orthologues': 217,
  'n_paralogues': 4,
  'ensembl_id': 'ENSG00000131730',
  'discription': 'creatine kinase, mitochondrial 2',
  'loc': 'Chromosome 5: 81,233,320-81,266,399',
  'strand': '+'},
 'ENSG00000003509': {'gene_name': 'NDUFAF7',
  'gene_biotype': 'protein_coding',
  'n_transcripts': 20,
  'n_orthologues': 210,
  'n_paralogues': 0,
  'ensembl_id': 'ENSG00000003509',
  'discription': 'NADH:ubiquinone oxidoreductase complex assembly factor 7',
  'loc': 'Chromosome 2: 37,231,631-37,253,403 ',
  'strand': '+'}}
```

---

**[Input:]**

```python
nested_dict["ENSG00000131730"]["discription"]
```

**[Output:]**

```
'creatine kinase, mitochondrial 2'
```

---

Keys() function can be used to list all the keys in a dictionary.

**[Input:]**

```python
nested_dict.keys()
```

**[Output:]**

```
dict_keys(['ENSG00000131730', 'ENSG00000003509'])
```

---

**[Input:]**

```python
nested_dict['ENSG00000131730'].keys()
```

**[Output:]**

```
dict_keys(['gene_name', 'gene_biotype', 'n_transcripts', 'n_orthologues', 'n_paralogues', 'ensembl_id', 'discription', 'loc', 'strand'])
```

---

Dictionaries can be created using dict() function. 

**[Input:]**

```python
gene_names = ["CKMT2", "NDUFAF7", "AGMAT"]
gene_biotypes = ["protein_coding"] * 3
n_transcripts = [32, 20, 4]
n_orthologues = [217, 210, 195]
n_paralogues = [4, 0, 2]
ensembl_IDs = ["ENSG00000131730", "ENSG00000003509", "ENSG00000116771"]
descriptions = ["creatine kinase, mitochondrial 2", "NADH:ubiquinone oxidoreductase complex assembly factor 7",
                "agmatinase (putative)"]
locus = ["Chromosome 5: 81,233,320-81,266,399", "Chromosome 2: 37,231,631-37,253,403", "Chromosome 1: 15,571,699-15,585,078"]
strands = ["+", "+", "-"]
list_values = zip(gene_names, gene_biotypes, n_transcripts, n_orthologues,
                  n_paralogues, ensembl_IDs, descriptions, locus, strands)
list_keys = ["gene_name", "gene_biotype", "n_transcripts", "n_orthologues",
             "n_paralogues", "ensembl_ID", "Description", "loc", "strand"]
list_dict = [dict(zip(list_keys, value)) for value in list_values]
list_dict
```

**[Output:]**

```
[{'gene_name': 'CKMT2',
  'gene_biotype': 'protein_coding',
  'n_transcripts': 32,
  'n_orthologues': 217,
  'n_paralogues': 4,
  'ensembl_ID': 'ENSG00000131730',
  'Description': 'creatine kinase, mitochondrial 2',
  'loc': 'Chromosome 5: 81,233,320-81,266,399',
  'strand': '+'},
 {'gene_name': 'NDUFAF7',
  'gene_biotype': 'protein_coding',
  'n_transcripts': 20,
  'n_orthologues': 210,
  'n_paralogues': 0,
  'ensembl_ID': 'ENSG00000003509',
  'Description': 'NADH:ubiquinone oxidoreductase complex assembly factor 7',
  'loc': 'Chromosome 2: 37,231,631-37,253,403',
  'strand': '+'},
 {'gene_name': 'AGMAT',
  'gene_biotype': 'protein_coding',
  'n_transcripts': 4,
  'n_orthologues': 195,
  'n_paralogues': 2,
  'ensembl_ID': 'ENSG00000116771',
  'Description': 'agmatinase (putative)',
  'loc': 'Chromosome 1: 15,571,699-15,585,078',
  'strand': '-'}]
```

---

### <font color="blue">Exercise</font>
Please apply the methods available for a dictionary object to get familiar with this data type.


### List comprehension
List comprehension is a very useful method available in python. It creates a new list by performing a pre-defined set of operations on each element of an existing list.
- Short syntax for better readability
- Faster operation than a for loop
- Creates a new list

#### __New_list = <font color="black">[</font><font color="blue">expression</font> <font color="green">for</font> <font color="red">item</font> <font color="green">in</font> <font color="orange">iterable</font> <font color="green">if</font> <font color="purple">condition == True</font><font color="black">]</font>__

**[Input:]**

```python
list_values = zip(gene_names, gene_biotypes, n_transcripts, n_orthologues,
                  n_paralogues, ensembl_IDs, descriptions, locus, strands)
list_dict = [dict(zip(list_keys, value)) for value in list_values]
list_dict
```

**[Output:]**

```
[{'gene_name': 'CKMT2',
  'gene_biotype': 'protein_coding',
  'n_transcripts': 32,
  'n_orthologues': 217,
  'n_paralogues': 4,
  'ensembl_ID': 'ENSG00000131730',
  'Description': 'creatine kinase, mitochondrial 2',
  'loc': 'Chromosome 5: 81,233,320-81,266,399',
  'strand': '+'},
 {'gene_name': 'NDUFAF7',
  'gene_biotype': 'protein_coding',
  'n_transcripts': 20,
  'n_orthologues': 210,
  'n_paralogues': 0,
  'ensembl_ID': 'ENSG00000003509',
  'Description': 'NADH:ubiquinone oxidoreductase complex assembly factor 7',
  'loc': 'Chromosome 2: 37,231,631-37,253,403',
  'strand': '+'},
 {'gene_name': 'AGMAT',
  'gene_biotype': 'protein_coding',
  'n_transcripts': 4,
  'n_orthologues': 195,
  'n_paralogues': 2,
  'ensembl_ID': 'ENSG00000116771',
  'Description': 'agmatinase (putative)',
  'loc': 'Chromosome 1: 15,571,699-15,585,078',
  'strand': '-'}]
```

---

### Let's dissect the operation
#### <font color="black">[</font><font color="blue">dict(zip(list_keys, value))</font> <font color="green">for</font> <font color="red">value</font> <font color="green">in</font> <font color="orange">list_values</font><font color="black">]</font>

### <font color="blue">Exercise</font>
Create a numeric iterable object and perform the same operation on each element of the object without using a for loop.

### <font color="Orange">Challenge</font>
- What is the difference between the above _list_dict_ object with _nested_dict_ object?
- How to modify _list_dict_ to an object that is the same as _nested_dict_?

## File handling

Python offers general-purpose file handling that offers efficient ways to deal with very large data. The biggest advantage that python has comparing to R is the ability to read file line by line to reduce memory usage for large volume data.
- open() is the key function used in file handling
- read(), readline() functions for read files
- write(), writeline() functions for write to files
- close() closes a file that has been open to avoid file corruption and to free system resources
- _with_ statement allows automatic file closing

For example, we are going to read a small example of a genome annotation (gtf) file and parse the information using what we have learned so far.

**[Input:]**

```python
## Initialize the dictionary that will hold the parsed information
annotation = {}

with open("GRCh38.ensembl112.4k.gtf", "r") as f:

    # iterate through the file line-by-line
    for line in f:
        
        # split each line with tab as the delimiter
        fields = line.strip().split("\t")

        # initialize a dictionary to hold the attribute info
        attributes = {}

        # only parse the lines with "gene" in the 3rd column
        if len(fields) == 9 and fields[2] == "gene":
 
            attr_pairs = [attr.strip().split(" ") for attr in fields[8].strip().split(";")]
            
            for pair in attr_pairs[:-1]:
                key = pair[0]
                value = pair[1].strip('"')
                attributes[key] = value
                if key == "gene_id":
                    annotation_key = value

            feature_info = {
            "seqname": fields[0],
            "source": fields[1],
            "start": fields[3],
            "end": fields[4],
            "strand": fields[6],
            "attributes": attributes
            }
            
            annotation[annotation_key] = feature_info

            
#annotation
```

---

## Visulization
Data visualization is one essential step in data analysis. There are many libraries that can be used to generate visualizations in python. The following is a short list to get you started.
- Matplotlib is the most widely used library
- Seaborn buids on top of matplotlib to generate more polished plots
- Plotly is known for its application in creating interactive visualizations
- Bokeh uses _The Grammer of Graphics_ like ggplot but it's native to python

<img src="figures/matplotlib.jpg" alt="Matplotlib" width="70%" align="center"/>

We are going to use the same data set used in Wednesday's R session for some examples of visualization in python.

**[Input:]**

```python
# load python modules
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

# read in the birth weight data using the url or from your local copy
data = pd.read_csv("https://raw.githubusercontent.com/ucdavis-bioinformatics-training/2022_February_Introduction_to_R_for_Bioinformatics/main/birthweight.csv")
```

---

**[Input:]**

```python
display(data.head(8))
```

**[Output:]**

```
     ID birth.date     location  length  birthweight  head.circumference  \
0  1107  1/25/1967      General      52         3.23                  36   
1   697   2/6/1967  Silver Hill      48         3.03                  35   
2  1683  2/14/1967  Silver Hill      53         3.35                  33   
3    27   3/9/1967  Silver Hill      53         3.55                  37   
4  1522  3/13/1967     Memorial      50         2.74                  33   
5   569  3/23/1967     Memorial      50         2.51                  35   
6   365  4/23/1967     Memorial      52         3.53                  37   
7   808   5/5/1967  Silver Hill      48         2.92                  33   

   weeks.gestation smoker  maternal.age  maternal.cigarettes  maternal.height  \
0               38     no            31                    0              164   
1               39     no            27                    0              162   
2               41     no            27                    0              164   
3               41    yes            37                   25              161   
4               39    yes            21                   17              156   
5               39    yes            22                    7              159   
6               40    yes            26                   25              170   
7               34     no            26                    0              167   

   maternal.prepregnant.weight  paternal.age  paternal.education  \
0                           57           NaN                 NaN   
1                           62          27.0                14.0   
2                           62          37.0                14.0   
3                           66          46.0                 NaN   
4                           53          24.0                12.0   
5                           52          23.0                14.0   
6                           62          30.0                10.0   
7                           64          25.0                12.0   

   paternal.cigarettes  paternal.height  low.birthweight  geriatric.pregnancy  
0                  NaN              NaN                0                False  
1                  0.0            178.0                0                False  
2                  0.0            170.0                0                False  
3                  0.0            175.0                0                 True  
4                  7.0            179.0                0                False  
5                 25.0              NaN                1                False  
6                 25.0            181.0                0                False  
7                 25.0            175.0                0                False  
```

---

**[Input:]**

```python
# enter matplotlib mode
%matplotlib

# Let's do some simple plot
data.boxplot(rot = 90)
```

**[Output:]**

```
Using matplotlib backend: module://matplotlib_inline.backend_inline
```

```
<Axes: >
```

![output image](data:image/png;base64,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)

---

### Let's use Seaborn library to generate some visualizations

#### Let's take a look at the data distribution

**[Input:]**

```python
# data distribution plots can be generated using displot() function
sns.displot(data, x = "birthweight")
```

**[Output:]**

```
<seaborn.axisgrid.FacetGrid at 0x16919a810>
```

![output image](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAeoAAAHpCAYAAABN+X+UAAAAOnRFWHRTb2Z0d2FyZQBNYXRwbG90bGliIHZlcnNpb24zLjEwLjAsIGh0dHBzOi8vbWF0cGxvdGxpYi5vcmcvlHJYcgAAAAlwSFlzAAAPYQAAD2EBqD+naQAAJGtJREFUeJzt3X90VPWd//HXQMIAAoHwIwRMSLQ0CSLCgahYNKFQFK2rp2e36ypKtbpsBQTTrSGiJVg1624X6YrAplXgrAdxTxFLW9tClUD91SX8EHBDAIUmh4aNUcgEiCMkn+8fHuZrJD9ImJn7Tub5OGfO6f01eef2tk/uZJLxOeecAACASd28HgAAALSMUAMAYBihBgDAMEINAIBhhBoAAMMINQAAhhFqAAAM6/Khds4pEAiIXxcHAHRGXT7UdXV1SkhIUF1dndejAADQbl0+1AAAdGaEGgAAwwg1AACGEWoAAAwj1AAAGEaoAQAwjFADAGAYoQYAwDBCDQCAYYQaAADDCDUAAIYRagAADCPUAAAYRqgBADCMUAMAYBihBgDAMEINAIBhhBoAAMPivB4AwMWpqKhQTU2N12NExKBBg5Samur1GICnCDXQiVVUVCgzM0v19ae9HiUievXqrf37y4g1YhqhBjqxmpoa1def1jX3LVK/5DSvxwmrQNUR/fnFxaqpqSHUiGmEGugC+iWnKTE1w+sxAEQAbyYDAMAwQg0AgGGEGgAAwwg1AACGEWoAAAwj1AAAGEaoAQAwjFADAGAYoQYAwDBCDQCAYYQaAADDCDUAAIYRagAADCPUAAAYRqgBADCMUAMAYBihBgDAMEINAIBhhBoAAMMINQAAhhFqAAAMI9QAABhGqAEAMIxQAwBgGKEGAMAwT0O9bds23XrrrRo2bJh8Pp9ee+210LYzZ84oPz9fV155pS655BINGzZM99xzj/761796NzAAAFHmaahPnTqlq666SsuWLTtv2+nTp7Vz5049/vjj2rlzp1599VUdOHBAf/M3f+PBpAAAeCPOyy8+ffp0TZ8+vdltCQkJ2rx5c5N1zz33nK6++mpVVFQoNTU1GiMCAOApT0PdXrW1tfL5fOrfv3+L+wSDQQWDwdByIBCIwmQAAERGp3kz2WeffaYFCxbozjvvVL9+/Vrcr6ioSAkJCaFHSkpKFKcEACC8OkWoz5w5ozvuuEONjY1avnx5q/sWFBSotrY29KisrIzSlAAAhJ/5l77PnDmj7373uzp8+LDefPPNVu+mJcnv98vv90dpOgAAIst0qM9F+uDBg9qyZYsGDhzo9UgAAESVp6E+efKkDh06FFo+fPiwdu/ercTERA0bNkx/+7d/q507d+o3v/mNGhoadOzYMUlSYmKievTo4dXYAABEjaehLi0t1eTJk0PLeXl5kqSZM2eqsLBQGzdulCSNHTu2yXFbtmxRbm5utMYEAMAznoY6NzdXzrkWt7e2DQCAWNAp3vUNAECsItQAABhGqAEAMIxQAwBgGKEGAMAwQg0AgGGEGgAAwwg1AACGEWoAAAwj1AAAGEaoAQAwjFADAGAYoQYAwDBCDQCAYYQaAADDCDUAAIYRagAADCPUAAAYRqgBADCMUAMAYBihBgDAMEINAIBhhBoAAMMINQAAhhFqAAAMI9QAABhGqAEAMIxQAwBgGKEGAMAwQg0AgGGEGgAAwwg1AACGEWoAAAwj1AAAGEaoAQAwjFADAGAYoQYAwDBCDQCAYYQaAADDCDUAAIYRagAADCPUAAAYRqgBADCMUAMAYBihBgDAMEINAIBhhBoAAMMINQAAhhFqAAAMI9QAABhGqAEAMIxQAwBgmKeh3rZtm2699VYNGzZMPp9Pr732WpPtzjkVFhZq2LBh6tWrl3Jzc/XBBx94MywAAB7wNNSnTp3SVVddpWXLljW7/V//9V+1ZMkSLVu2TNu3b9fQoUP1rW99S3V1dVGeFAAAb8R5+cWnT5+u6dOnN7vNOaelS5dq4cKF+s53viNJWrNmjZKSkrR27VrNmjWr2eOCwaCCwWBoORAIhH9wAACixOzPqA8fPqxjx45p2rRpoXV+v185OTl65513WjyuqKhICQkJoUdKSko0xgUAICLMhvrYsWOSpKSkpCbrk5KSQtuaU1BQoNra2tCjsrIyonMCABBJnr70fSF8Pl+TZefceeu+zO/3y+/3R3osAACiwuwd9dChQyXpvLvn6urq8+6yAQDoqsyGOj09XUOHDtXmzZtD6z7//HNt3bpV1113nYeTAQAQPZ6+9H3y5EkdOnQotHz48GHt3r1biYmJSk1N1fz58/X0009r5MiRGjlypJ5++mn17t1bd955p4dTAwAQPZ6GurS0VJMnTw4t5+XlSZJmzpyp1atX65FHHlF9fb0efPBBHT9+XNdcc402bdqkvn37ejUyAABR5Wmoc3Nz5ZxrcbvP51NhYaEKCwujNxQAAIaY/Rk1AAAg1AAAmEaoAQAwjFADAGAYoQYAwDBCDQCAYYQaAADDCDUAAIYRagAADCPUAAAYRqgBADCMUAMAYBihBgDAMEINAIBhhBoAAMMINQAAhhFqAAAMI9QAABhGqAEAMIxQAwBgGKEGAMAwQg0AgGGEGgAAwwg1AACGEWoAAAwj1AAAGEaoAQAwjFADAGAYoQYAwDBCDQCAYYQaAADDCDUAAIYRagAADCPUAAAYRqgBADCMUAMAYBihBgDAMEINAIBhhBoAAMMINQAAhhFqAAAMI9QAABhGqAEAMIxQAwBgGKEGAMAwQg0AgGGEGgAAwwg1AACGEWoAAAwj1AAAGEaoAQAwzHSoz549q8cee0zp6enq1auXLrvsMj3xxBNqbGz0ejQAAKIizusBWvPMM89o5cqVWrNmja644gqVlpbq3nvvVUJCgubNm+f1eAAARJzpUL/77ru67bbbdMstt0iS0tLS9PLLL6u0tNTjyQAAiA7TL31PmjRJb7zxhg4cOCBJev/99/XWW2/p5ptvbvGYYDCoQCDQ5AEAQGdl+o46Pz9ftbW1yszMVPfu3dXQ0KCnnnpK//AP/9DiMUVFRVq8eHEUpwQAIHJM31G/8soreumll7R27Vrt3LlTa9as0U9/+lOtWbOmxWMKCgpUW1sbelRWVkZxYgAAwsv0HfWPfvQjLViwQHfccYck6corr9Rf/vIXFRUVaebMmc0e4/f75ff7ozkmAAARY/qO+vTp0+rWremI3bt359ezAAAxw/Qd9a233qqnnnpKqampuuKKK7Rr1y4tWbJE9913n9ejAQAQFaZD/dxzz+nxxx/Xgw8+qOrqag0bNkyzZs3Sj3/8Y69HAwAgKkyHum/fvlq6dKmWLl3q9SgAAHjC9M+oAQCIdYQaAADDCDUAAIYRagAADCPUAAAYRqgBADCMUAMAYBihBgDAMEINAIBhhBoAAMMINQAAhhFqAAAM61CoL7vsMn3yySfnrT9x4oQuu+yyix4KAAB8oUOhPnLkiBoaGs5bHwwGdfTo0YseCgAAfKFdH3O5cePG0H/+wx/+oISEhNByQ0OD3njjDaWlpYVtOAAAYl27Qn377bdLknw+n2bOnNlkW3x8vNLS0vTv//7vYRsOAIBY165QNzY2SpLS09O1fft2DRo0KCJDAQCAL7Qr1OccPnw43HMAAIBmdCjUkvTGG2/ojTfeUHV1dehO+5wXX3zxogcDAAAdDPXixYv1xBNPaMKECUpOTpbP5wv3XAAAQB0M9cqVK7V69Wrdfffd4Z4HAAB8SYd+j/rzzz/XddddF+5ZAADAV3Qo1Pfff7/Wrl0b7lkAAMBXdOil788++0zFxcX64x//qDFjxig+Pr7J9iVLloRlOCBcKioqVFNT4/UYYVdWVub1CBHXVb/HQYMGKTU11esx0Al0KNR79uzR2LFjJUn79u1rso03lsGaiooKZWZmqb7+tNejRMyZ4OdejxB29bWfSPJpxowZXo8SEb169db+/WXEGm3qUKi3bNkS7jmAiKmpqVF9/Wldc98i9UtO83qcsKra+672bSzW2bNnvR4l7M6crpPkNPbOfA1Oz/R6nLAKVB3Rn19crJqaGkKNNnX496iBzqZfcpoSUzO8HiOsAlVHvB4h4voMSe1y/70B7dGhUE+ePLnVl7jffPPNDg8EAAD+vw6F+tzPp885c+aMdu/erX379p33YR0AAKDjOhTqZ599ttn1hYWFOnny5EUNBAAA/r8O/R51S2bMmMHf+QYAIIzCGup3331XPXv2DOdTAgAQ0zr00vd3vvOdJsvOOVVVVam0tFSPP/54WAYDAAAdDHVCQkKT5W7duikjI0NPPPGEpk2bFpbBAABAB0O9atWqcM8BAACacVF/8GTHjh0qKyuTz+fTqFGjNG7cuHDNBQAA1MFQV1dX64477lBJSYn69+8v55xqa2s1efJkrVu3ToMHDw73nAAAxKQOvet77ty5CgQC+uCDD/Tpp5/q+PHj2rdvnwKBgB566KFwzwgAQMzq0B3173//e/3xj39UVlZWaN2oUaP0/PPP82YyAADCqEN31I2Njed9BrUkxcfHq7Gx8aKHAgAAX+hQqL/5zW9q3rx5+utf/xpad/ToUT388MOaMmVK2IYDACDWdSjUy5YtU11dndLS0nT55Zfra1/7mtLT01VXV6fnnnsu3DMCABCzOvQz6pSUFO3cuVObN2/W/v375ZzTqFGjNHXq1HDPBwBATGvXHfWbb76pUaNGKRAISJK+9a1vae7cuXrooYeUnZ2tK664Qn/6058iMigAALGoXaFeunSpHnjgAfXr1++8bQkJCZo1a5aWLFkStuEAAIh17Qr1+++/r5tuuqnF7dOmTdOOHTsueigAAPCFdoX6//7v/5r9taxz4uLi9PHHH1/0UAAA4AvtCvXw4cO1d+/eFrfv2bNHycnJFz0UAAD4QrtCffPNN+vHP/6xPvvss/O21dfXa9GiRfr2t78dtuEAAIh17fr1rMcee0yvvvqqvv71r2vOnDnKyMiQz+dTWVmZnn/+eTU0NGjhwoWRmhUAgJjTrlAnJSXpnXfe0Q9+8AMVFBTIOSdJ8vl8uvHGG7V8+XIlJSVFZFAAAGJRu//gyYgRI/T666/r+PHjOnTokJxzGjlypAYMGBCJ+QAAiGkd+hOikjRgwABlZ2fr6quvjmikjx49qhkzZmjgwIHq3bu3xo4dy6+AAQBiRof+hGi0HD9+XN/4xjc0efJk/e53v9OQIUP04Ycfqn///l6PBgBAVJgO9TPPPKOUlBStWrUqtC4tLa3VY4LBoILBYGj53J87BQBrysrKvB4hIgYNGqTU1FSvx+gyTId648aNuvHGG/V3f/d32rp1q4YPH64HH3xQDzzwQIvHFBUVafHixVGcEgDap772E0k+zZgxw+tRIqJXr97av7+MWIeJ6VB/9NFHWrFihfLy8vToo4/qf/7nf/TQQw/J7/frnnvuafaYgoIC5eXlhZYDgYBSUlKiNTIAtOnM6TpJTmPvzNfg9EyvxwmrQNUR/fnFxaqpqSHUYWI61I2NjZowYYKefvppSdK4ceP0wQcfaMWKFS2G2u/3y+/3R3NMAOiQPkNSlZia4fUYMK7D7/qOhuTkZI0aNarJuqysLFVUVHg0EQAA0WU61N/4xjdUXl7eZN2BAwc0YsQIjyYCACC6TIf64Ycf1nvvvaenn35ahw4d0tq1a1VcXKzZs2d7PRoAAFFhOtTZ2dnasGGDXn75ZY0ePVo/+clPtHTpUt11111ejwYAQFSYfjOZJH3729/mE7kAADHL9B01AACxjlADAGAYoQYAwDBCDQCAYYQaAADDCDUAAIYRagAADCPUAAAYRqgBADCMUAMAYBihBgDAMEINAIBhhBoAAMMINQAAhhFqAAAMI9QAABhGqAEAMIxQAwBgGKEGAMAwQg0AgGGEGgAAwwg1AACGEWoAAAwj1AAAGEaoAQAwjFADAGAYoQYAwDBCDQCAYYQaAADDCDUAAIYRagAADCPUAAAYRqgBADCMUAMAYBihBgDAMEINAIBhhBoAAMMINQAAhhFqAAAMI9QAABhGqAEAMIxQAwBgGKEGAMAwQg0AgGGEGgAAwwg1AACGEWoAAAwj1AAAGEaoAQAwjFADAGAYoQYAwLBOFeqioiL5fD7Nnz/f61EAAIiKThPq7du3q7i4WGPGjPF6FAAAoqZThPrkyZO666679POf/1wDBgzwehwAAKImzusBLsTs2bN1yy23aOrUqXryySdb3TcYDCoYDIaWA4FApMfrMioqKlRTU+P1GGFXVlbm9QgA0GHmQ71u3Trt3LlT27dvv6D9i4qKtHjx4ghP1fVUVFQoMzNL9fWnvR4lYs4EP/d6BABoN9Ohrqys1Lx587Rp0yb17Nnzgo4pKChQXl5eaDkQCCglJSVSI3YZNTU1qq8/rWvuW6R+yWlejxNWVXvf1b6NxTp79qzXowBAu5kO9Y4dO1RdXa3x48eH1jU0NGjbtm1atmyZgsGgunfv3uQYv98vv98f7VG7jH7JaUpMzfB6jLAKVB3xegQA6DDToZ4yZYr27t3bZN29996rzMxM5efnnxdpAAC6GtOh7tu3r0aPHt1k3SWXXKKBAweetx4AgK6oU/x6FgAAscr0HXVzSkpKvB4BAICo4Y4aAADDCDUAAIYRagAADCPUAAAYRqgBADCMUAMAYBihBgDAMEINAIBhhBoAAMMINQAAhhFqAAAMI9QAABhGqAEAMIxQAwBgGKEGAMAwQg0AgGGEGgAAwwg1AACGEWoAAAwj1AAAGEaoAQAwjFADAGAYoQYAwLA4rwcAAHQ9ZWVlXo8QEYMGDVJqampUvyahBgCETX3tJ5J8mjFjhtejRESvXr21f39ZVGNNqAEAYXPmdJ0kp7F35mtweqbX44RVoOqI/vziYtXU1BBqAEDn1mdIqhJTM7weo0vgzWQAABhGqAEAMIxQAwBgGKEGAMAwQg0AgGGEGgAAwwg1AACGEWoAAAwj1AAAGEaoAQAwjFADAGAYoQYAwDBCDQCAYYQaAADDCDUAAIYRagAADCPUAAAYRqgBADCMUAMAYBihBgDAMEINAIBhhBoAAMMINQAAhhFqAAAMI9QAABhmOtRFRUXKzs5W3759NWTIEN1+++0qLy/3eiwAAKLGdKi3bt2q2bNn67333tPmzZt19uxZTZs2TadOnfJ6NAAAoiLO6wFa8/vf/77J8qpVqzRkyBDt2LFDN9xwQ7PHBINBBYPB0HIgEAjrTBUVFaqpqQnrc1pQVlbm9QgAgGaYDvVX1dbWSpISExNb3KeoqEiLFy+OyNevqKhQZmaW6utPR+T5LTgT/NzrEQAAX9JpQu2cU15eniZNmqTRo0e3uF9BQYHy8vJCy4FAQCkpKWGZoaamRvX1p3XNfYvULzktLM9pRdXed7VvY7HOnj3r9SgAgC/pNKGeM2eO9uzZo7feeqvV/fx+v/x+f0Rn6ZecpsTUjIh+jWgLVB3xegQAQDM6Rajnzp2rjRs3atu2bbr00ku9HgcAgKgxHWrnnObOnasNGzaopKRE6enpXo8EAEBUmQ717NmztXbtWv3qV79S3759dezYMUlSQkKCevXq5fF0AABEnunfo16xYoVqa2uVm5ur5OTk0OOVV17xejQAAKLC9B21c87rEQAA8JTpO2oAAGIdoQYAwDBCDQCAYYQaAADDCDUAAIYRagAADCPUAAAYRqgBADCMUAMAYBihBgDAMEINAIBhhBoAAMMINQAAhhFqAAAMI9QAABhGqAEAMIxQAwBgGKEGAMAwQg0AgGGEGgAAwwg1AACGEWoAAAwj1AAAGEaoAQAwjFADAGAYoQYAwDBCDQCAYYQaAADDCDUAAIYRagAADCPUAAAYRqgBADCMUAMAYBihBgDAMEINAIBhhBoAAMMINQAAhhFqAAAMI9QAABhGqAEAMIxQAwBgGKEGAMAwQg0AgGGEGgAAwwg1AACGEWoAAAwj1AAAGEaoAQAwjFADAGAYoQYAwDBCDQCAYZ0i1MuXL1d6erp69uyp8ePH609/+pPXIwEAEBXmQ/3KK69o/vz5WrhwoXbt2qXrr79e06dPV0VFhdejAQAQceZDvWTJEn3/+9/X/fffr6ysLC1dulQpKSlasWKF16MBABBxcV4P0JrPP/9cO3bs0IIFC5qsnzZtmt55551mjwkGgwoGg6Hl2tpaSVIgELjoeU6ePClJ+vQv5TobrL/o57MkUPUXSVLt0YOKj/N5PE148b11TnxvnVOX/t6OffFK7smTJ8PSFEnq27evfL42zpMz7OjRo06Se/vtt5usf+qpp9zXv/71Zo9ZtGiRk8SDBw8ePHiYf9TW1rbZQtN31Od89V8bzrkW/wVSUFCgvLy80HJjY6M+/fRTDRw4sO1/tYRZIBBQSkqKKisr1a9fv6h+7c6A89M2zlHbOEet4/y0zctz1Ldv3zb3MR3qQYMGqXv37jp27FiT9dXV1UpKSmr2GL/fL7/f32Rd//79IzXiBenXrx//A2kF56dtnKO2cY5ax/lpm9VzZPrNZD169ND48eO1efPmJus3b96s6667zqOpAACIHtN31JKUl5enu+++WxMmTNDEiRNVXFysiooK/dM//ZPXowEAEHHmQ/33f//3+uSTT/TEE0+oqqpKo0eP1uuvv64RI0Z4PVqb/H6/Fi1adN5L8fgC56dtnKO2cY5ax/lpm/Vz5HPOOa+HAAAAzTP9M2oAAGIdoQYAwDBCDQCAYYQaAADDCHUHFRUVKTs7W3379tWQIUN0++23q7y8vM3jtm7dqvHjx6tnz5667LLLtHLlyihMG30dOT8lJSXy+XznPfbv3x+lqaNrxYoVGjNmTOiPLEycOFG/+93vWj0mVq6fc9p7jmLtGvqqoqIi+Xw+zZ8/v9X9Yu06OudCzo/Fa4hQd9DWrVs1e/Zsvffee9q8ebPOnj2radOm6dSpUy0ec/jwYd188826/vrrtWvXLj366KN66KGHtH79+ihOHh0dOT/nlJeXq6qqKvQYOXJkFCaOvksvvVT/8i//otLSUpWWluqb3/ymbrvtNn3wwQfN7h9L18857T1H58TKNfRl27dvV3FxscaMGdPqfrF4HUkXfn7OMXUNXfxHZ8A556qrq50kt3Xr1hb3eeSRR1xmZmaTdbNmzXLXXnttpMfz3IWcny1btjhJ7vjx49EbzJgBAwa4X/ziF81ui+Xr58taO0exeg3V1dW5kSNHus2bN7ucnBw3b968FveNxeuoPefH4jXEHXWYnPs4zcTExBb3effddzVt2rQm62688UaVlpbqzJkzEZ3Paxdyfs4ZN26ckpOTNWXKFG3ZsiXSo5nQ0NCgdevW6dSpU5o4cWKz+8Ty9SNd2Dk6J9auodmzZ+uWW27R1KlT29w3Fq+j9pyfcyxdQ+b/Mlln4JxTXl6eJk2apNGjR7e437Fjx877MJGkpCSdPXtWNTU1Sk5OjvSonrjQ85OcnKzi4mKNHz9ewWBQ//Vf/6UpU6aopKREN9xwQxQnjp69e/dq4sSJ+uyzz9SnTx9t2LBBo0aNanbfWL1+2nOOYvEaWrdunXbu3Knt27df0P6xdh219/xYvIYIdRjMmTNHe/bs0VtvvdXmvs19ZGdz67uSCz0/GRkZysjICC1PnDhRlZWV+ulPf9pl/082IyNDu3fv1okTJ7R+/XrNnDlTW7dubTFEsXj9tOccxdo1VFlZqXnz5mnTpk3q2bPnBR8XK9dRR86PxWuIl74v0ty5c7Vx40Zt2bJFl156aav7Dh06tNmP7IyLi9PAgQMjOaZn2nN+mnPttdfq4MGDEZjMhh49euhrX/uaJkyYoKKiIl111VX62c9+1uy+sXj9SO07R83pytfQjh07VF1drfHjxysuLk5xcXHaunWr/uM//kNxcXFqaGg475hYuo46cn6a4/U1xB11BznnNHfuXG3YsEElJSVKT09v85iJEyfq17/+dZN1mzZt0oQJExQfHx+pUT3RkfPTnF27dnW5l+Ja45xTMBhsdlssXT+tae0cNacrX0NTpkzR3r17m6y79957lZmZqfz8fHXv3v28Y2LpOurI+WmO59eQZ29j6+R+8IMfuISEBFdSUuKqqqpCj9OnT4f2WbBggbv77rtDyx999JHr3bu3e/jhh93//u//uhdeeMHFx8e7X/7yl158CxHVkfPz7LPPug0bNrgDBw64ffv2uQULFjhJbv369V58CxFXUFDgtm3b5g4fPuz27NnjHn30UdetWze3adMm51xsXz/ntPccxdo11JyvvquZ66ipts6PxWuIUHeQpGYfq1atCu0zc+ZMl5OT0+S4kpISN27cONejRw+XlpbmVqxYEd3Bo6Qj5+eZZ55xl19+uevZs6cbMGCAmzRpkvvtb38b/eGj5L777nMjRoxwPXr0cIMHD3ZTpkwJBci52L5+zmnvOYq1a6g5Xw0R11FTbZ0fi9cQH3MJAIBhvJkMAADDCDUAAIYRagAADCPUAAAYRqgBADCMUAMAYBihBgDAMEINAIBhhBowKDc3V/Pnz29xe1pampYuXRqR5w63I0eOyOfzaffu3Rd8zOrVq9W/f/+IzQR0JnwoB9AJbd++XZdcckmr+5SUlGjy5Mk6fvy4p9FLSUlRVVWVBg0aFNbn/d73vqcTJ07otddeC+vzAtYQaqATGjx4cKvbz5w5E6VJ2ta9e3cNHTrU6zGATouXvgGjzp49qzlz5qh///4aOHCgHnvsMZ370/xffenb5/Np5cqVuu2223TJJZfo/vvv1+TJkyVJAwYMkM/n0/e+973Q/o2NjXrkkUeUmJiooUOHqrCwMLTthz/8oW699dbQ8tKlS+Xz+fTb3/42tC4jI0P/+Z//GVpetWqVsrKy1LNnT2VmZmr58uWhbc299L1x40aNHDlSvXr10uTJk7VmzRr5fD6dOHGiyTn4wx/+oKysLPXp00c33XSTqqqqJEmFhYVas2aNfvWrX8nn88nn86mkpKS9pxjoHDz9SBAAzcrJyXF9+vRx8+bNc/v373cvvfSS6927tysuLnbOOTdixAj37LPPhvaX5IYMGeJeeOEF9+GHH7ojR4649evXO0muvLzcVVVVuRMnToSeu1+/fq6wsNAdOHDArVmzxvl8vtCnUm3cuNElJCS4hoYG55xzt99+uxs0aJD70Y9+5JxzrqqqyklyZWVlzjnniouLXXJyslu/fr376KOP3Pr1611iYqJbvXq1c865w4cPO0lu165doeX4+Hj3z//8z27//v3u5ZdfdsOHD3eS3PHjx51zzq1atcrFx8e7qVOnuu3bt7sdO3a4rKwsd+eddzrnnKurq3Pf/e533U033RT6CNVgMBi5/0IADxFqwKCcnByXlZXlGhsbQ+vy8/NdVlaWc675UM+fP7/Jc2zZsqVJ/L783JMmTWqyLjs72+Xn5zvnnDtx4oTr1q2bKy0tdY2NjW7gwIGuqKjIZWdnO+ecW7t2rUtKSgodm5KS4tauXdvk+X7yk5+4iRMnOufOD3V+fr4bPXp0k/0XLlx4XqgluUOHDoX2ef7555t83ZkzZ7rbbrvtvHMHdDW89A0Yde2118rn84WWJ06cqIMHD6qhoaHZ/SdMmHDBzz1mzJgmy8nJyaqurpYkJSQkaOzYsSopKdHevXvVrVs3zZo1S++//77q6upUUlKinJwcSdLHH3+syspKff/731efPn1CjyeffFIffvhhs1+7vLxc2dnZTdZdffXV5+3Xu3dvXX755c3OCMQS3kwGdBFtvQv8y+Lj45ss+3w+NTY2hpZzc3NVUlKiHj16KCcnRwMGDNAVV1yht99+WyUlJaFf7zp3zM9//nNdc801TZ6ze/fuzX5t51yTf4CcW3chMza3H9DVEWrAqPfee++85ZEjR7YYwK/q0aOHJLV4B96a3NxcvfDCC4qLi9PUqVMlSTk5OVq3bp0OHDgQuqNOSkrS8OHD9dFHH+muu+66oOfOzMzU66+/3mRdaWlpu2fs0aNHh743oLPhpW/AqMrKSuXl5am8vFwvv/yynnvuOc2bN++Cjx8xYoR8Pp9+85vf6OOPP9bJkycv+NgbbrhBdXV1+vWvf63c3FxJX8T7pZde0uDBgzVq1KjQvoWFhSoqKtLPfvYzHThwQHv37tWqVau0ZMmSZp971qxZ2r9/v/Lz83XgwAH993//t1avXi1J591ptyYtLU179uxReXm5ampqTP1KGhBOhBow6p577lF9fb2uvvpqzZ49W3PnztU//uM/XvDxw4cP1+LFi7VgwQIlJSVpzpw5F3xsQkKCxo0bp8TExFCUr7/+ejU2Nobups+5//779Ytf/EKrV6/WlVdeqZycHK1evVrp6enNPnd6erp++ctf6tVXX9WYMWO0YsUKLVy4UJLk9/sveMYHHnhAGRkZmjBhggYPHqy33377go8FOhOf44c+ADz21FNPaeXKlaqsrPR6FMAcfkYNIOqWL1+u7OxsDRw4UG+//bb+7d/+rV13/EAsIdQAou7gwYN68skn9emnnyo1NVU//OEPVVBQ4PVYgEm89A0AgGG8mQwAAMMINQAAhhFqAAAMI9QAABhGqAEAMIxQAwBgGKEGAMAwQg0AgGH/DyBxzo5b8CiLAAAAAElFTkSuQmCC)

---

**[Input:]**

```python
# One may define a different bin size from the default
sns.displot(data, x = "birthweight", binwidth = 0.1)
```

**[Output:]**

```
<seaborn.axisgrid.FacetGrid at 0x169298b90>
```

![output image](data:image/png;base64,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p0WLFmncuHENPQ8AAPieiH6P+ttvv9Wll17a0LMAAIAfiCjUEyZM0JIlSxp6FgAA8AMRvfR99OhRzZ8/X2+//bb69++v2NjYGh+fNWtWgwwHAEC0iyjUW7Zs0UUXXSRJ2rZtW42P8YNlAAA0nIhCvWbNmoaeAwAA1IK3uQQAwLCInlEPHz78lC9xv/vuuxEPBAAA/ieiUJ/4/vQJx44d0+bNm7Vt27aT3qwDAABELqJQP/bYY7XePnPmTB06dKheAwEAgP9p0O9R33TTTfydbwAAGlCDhvrDDz9U69atG/IuAQCIahG99P2Tn/ykxnXnnMrKylRYWKjf/e53DTIYAACIMNQJCQk1rrdo0ULp6el66KGHNGrUqAYZDAAARBjqhQsXNvQcAACgFhGF+oSioiIVFxfL5/Opb9++GjBgQEPNBQAAFGGo9+3bp1/84hfKz89Xhw4d5JzTwYMHNXz4cC1dulRdunRp6DkBAIhKEf3U95QpU+T3+7V9+3Z988032r9/v7Zt2ya/368777yzoWcEACBqRfSMeuXKlXr77beVmZkZvK1v37566qmn+GEyAAAaUETPqKurq096D2pJio2NVXV1db2HAgAA34ko1FdeeaWmTp2q//73v8HbPv/8c911110aMWJEgw0HAEC0iyjUTz75pCoqKpSamqrevXvr3HPPVVpamioqKvTEE0809IwAAEStiL5HnZycrI0bN2r16tUqKSmRc059+/bVyJEjG3o+AACiWljPqN9991317dtXfr9fknTVVVdpypQpuvPOOzV48GCdf/75eu+99xplUAAAolFYoZ49e7Zuv/12xcfHn/SxhIQETZw4UbNmzWqw4QAAiHZhhfrjjz/WNddcU+fHR40apaKionoPBQAAvhNWqL/88stafy3rhJiYGH311Vf1HgoAAHwnrFB3795dW7durfPjW7ZsUVJSUr2HAgAA3wkr1Ndee61+//vf6+jRoyd9rLKyUjNmzNCPf/zjBhsOAIBoF9avZz344IN6+eWXdd5552ny5MlKT0+Xz+dTcXGxnnrqKVVVVemBBx5orFkBAIg6YYW6W7du+uCDD3THHXcoJydHzjlJks/n09VXX605c+aoW7dujTIoAADRKOw/eNKzZ0+98cYb2r9/vz755BM559SnTx917NixMeYDACCqRfSXySSpY8eOGjx4cEPOAgAAfiCiv/UNAACaBqEGAMAwQg0AgGGEGgAAwwg1AACGEWoAAAwj1AAAGEaoAQAwjFADAGAYoQYAwDBCDQCAYYQaAADDCDUAAIYRagAADCPUAAAYRqgBADCMUAMAYBihBgDAMEINAIBhhBoAAMMINQAAhhFqAAAMI9QAABhGqAEAMMzTUOfl5Wnw4MFq3769unbtqrFjx2rHjh1ejgQAgCmehrqgoECTJk3S+vXrtXr1ah0/flyjRo3S4cOHvRwLAAAzYrw8+MqVK2tcX7hwobp27aqioiJdccUVJ20fCAQUCASC1/1+f6PPCBtKS0tVXl4e1j7FxcWNNE3jiZbHKUU2dyAQUFxcXJMcqyFE8vk8IdLHmpiYqJSUlIiOGS0i/bx4tbaehvqHDh48KEnq1KlTrR/Py8tTbm5uU44EA0pLS5WRkanKyiMR7X8s8G0DT9Q4ouVxVh78WpJPN910U/g7+3yScxEfuynXqL6fz0gfa5s2bVVSUkys61Cfz4tXa2sm1M45ZWdn67LLLlO/fv1q3SYnJ0fZ2dnB636/X8nJyU01IjxSXl6uysojuuTWGYpPSg15v7KtH2rbivk6fvx44w3XgKLlcR47UiHJ6aIbpqtLWkbI+514nOHu9/19m3KNIv18SpE/Vn/ZHn30XK7Ky8sJdR0i/bx4ubZmQj158mRt2bJF77//fp3bxMXFRfRSEM4M8Ump6pSSHvL2/rI9jTdMI4qWx9mua0pEjzPc/b6/rxfC/XxK9XusCE0knxevmAj1lClTtGLFCq1du1Y9evTwehwAAMzwNNTOOU2ZMkXLly9Xfn6+0tLSvBwHAABzPA31pEmTtGTJEr366qtq3769vvjiC0lSQkKC2rRp4+VoAACY4OnvUc+dO1cHDx7UsGHDlJSUFLy8+OKLXo4FAIAZnr/0DQAA6sbf+gYAwDBCDQCAYYQaAADDCDUAAIYRagAADCPUAAAYRqgBADCMUAMAYBihBgDAMEINAIBhhBoAAMMINQAAhhFqAAAMI9QAABhGqAEAMIxQAwBgGKEGAMAwQg0AgGGEGgAAwwg1AACGEWoAAAwj1AAAGEaoAQAwjFADAGAYoQYAwDBCDQCAYYQaAADDCDUAAIYRagAADCPUAAAYRqgBADCMUAMAYBihBgDAMEINAIBhhBoAAMMINQAAhhFqAAAMI9QAABhGqAEAMIxQAwBgGKEGAMAwQg0AgGGEGgAAwwg1AACGEWoAAAwj1AAAGEaoAQAwjFADAGAYoQYAwDBCDQCAYYQaAADDCDUAAIYRagAADCPUAAAYRqgBADCMUAMAYBihBgDAMEINAIBhhBoAAMMINQAAhhFqAAAMI9QAABhGqAEAMIxQAwBgGKEGAMAwQg0AgGGEGgAAwwg1AACGEWoAAAwj1AAAGOZpqNeuXavrr79e55xzjnw+n1555RUvxwEAwBxPQ3348GFdeOGFevLJJ70cAwAAs2K8PPjo0aM1evTokLcPBAIKBALB636/v8FnKi0tVXl5edj7BQIBxcXFRXTMxMREpaSkRLRvpCJ9nPWZNdJjFhcXR3S8hhDJsSM9F7x8nDi9cD8/ze28lSI/d734uuDF102veBrqcOXl5Sk3N7fR7r+0tFQZGZmqrDwS/s4+n+RcRMdt06atSkqKm+ykq8/jjHTWeq3t/3cs8G3E+4ar8uDXkny66aabwt+5HueC1LSPE6dXr3NBzei8lSI+d734utDUXze91KxCnZOTo+zs7OB1v9+v5OTkBrv/8vJyVVYe0SW3zlB8UmrI+5Vt/VDbVszXRTdMV5e0jLCO6S/bo4+ey1V5eXmTnXCRPs76zBrpMaX/re/x48fD2q8+jh2pkOTC/pzW51zw4nHi9Op7LjSH81aK/Nz14uuCF183vdSsQh0XFxfxy8vhiE9KVaeU9JC395ftkSS165oS1n5eC/dxenXME+vrhXA/p/U5F7x8nDi9SM8FL9Tn/PPi65gXX4uaE349CwAAwwg1AACGefrS96FDh/TJJ58Er+/evVubN29Wp06douL7DgAAnI6noS4sLNTw4cOD10/8oNj48eO1aNEij6YCAMAOT0M9bNgwuXr8GgsAAGc6vkcNAIBhhBoAAMMINQAAhhFqAAAMI9QAABhGqAEAMIxQAwBgGKEGAMAwQg0AgGGEGgAAwwg1AACGEWoAAAwj1AAAGEaoAQAwjFADAGAYoQYAwDBCDQCAYYQaAADDCDUAAIYRagAADCPUAAAYRqgBADCMUAMAYBihBgDAMEINAIBhhBoAAMMINQAAhhFqAAAMI9QAABhGqAEAMIxQAwBgGKEGAMAwQg0AgGGEGgAAwwg1AACGEWoAAAwj1AAAGEaoAQAwjFADAGAYoQYAwDBCDQCAYYQaAADDCDUAAIYRagAADCPUAAAYRqgBADCMUAMAYBihBgDAMEINAIBhhBoAAMMINQAAhhFqAAAMI9QAABhGqAEAMIxQAwBgGKEGAMAwQg0AgGGEGgAAwwg1AACGEWoAAAwj1AAAGEaoAQAwjFADAGAYoQYAwDBCDQCAYYQaAADDCDUAAIYRagAADCPUAAAYRqgBADDM81DPmTNHaWlpat26tQYOHKj33nvP65EAADDD01C/+OKLmjZtmh544AFt2rRJl19+uUaPHq3S0lIvxwIAwAxPQz1r1izddtttmjBhgjIzMzV79mwlJydr7ty5Xo4FAIAZMV4d+Ntvv1VRUZHuu+++GrePGjVKH3zwQa37BAIBBQKB4PWDBw9Kkvx+f4PMdOjQIUnSN/+3Q8cDlSHv5y/7v+/m+XyXYmN8YR3T/8V3rx4UFRUFjx+qFi1aqLq6Oqx9JGnHjh2SInic9Zg10mNKka9vvT4vHJNj1nPfqDmmB18XvDzmoUOHGqw5ktS+fXv5fKdZb+eRzz//3Ely69atq3H7I4884s4777xa95kxY4aTxIULFy5cuJwRl4MHD562l549oz7hh/+ScM7V+a+LnJwcZWdnB69XV1frm2++UefOnU//L5JG4Pf7lZycrL179yo+Pr7Jj99csE6hYZ1CwzqFhnUKjdfr1L59+9Nu41moExMT1bJlS33xxRc1bt+3b5+6detW6z5xcXGKi4urcVuHDh0aa8SQxcfH8z9CCFin0LBOoWGdQsM6hcbyOnn2w2StWrXSwIEDtXr16hq3r169WpdeeqlHUwEAYIunL31nZ2dr3LhxGjRokLKysjR//nyVlpbqN7/5jZdjAQBghqeh/vnPf66vv/5aDz30kMrKytSvXz+98cYb6tmzp5djhSwuLk4zZsw46eV41MQ6hYZ1Cg3rFBrWKTTNYZ18zjnn9RAAAKB2nv8JUQAAUDdCDQCAYYQaAADDCDUAAIYR6jrk5eVp8ODBat++vbp27aqxY8cG/0bsqRQUFGjgwIFq3bq1evXqpXnz5jXBtN6JZJ3y8/Pl8/lOupSUlDTR1E1v7ty56t+/f/CPKmRlZenNN9885T7Rdi5J4a9TNJ5LtcnLy5PP59O0adNOuV00nlPfF8o6WTynCHUdCgoKNGnSJK1fv16rV6/W8ePHNWrUKB0+fLjOfXbv3q1rr71Wl19+uTZt2qT7779fd955p5YtW9aEkzetSNbphB07dqisrCx46dOnTxNM7I0ePXro0UcfVWFhoQoLC3XllVdqzJgx2r59e63bR+O5JIW/TidE07n0Qxs2bND8+fPVv3//U24XrefUCaGu0wmmzqn6v71GdNi3b5+T5AoKCurc5t5773UZGRk1bps4caIbMmRIY49nRijrtGbNGifJ7d+/v+kGM6hjx47u2WefrfVjnEv/c6p1ivZzqaKiwvXp08etXr3aDR061E2dOrXObaP5nApnnSyeUzyjDtGJt9Ts1KlTndt8+OGHGjVqVI3brr76ahUWFurYsWONOp8VoazTCQMGDFBSUpJGjBihNWvWNPZoZlRVVWnp0qU6fPiwsrKyat2Gcym0dTohWs+lSZMm6brrrtPIkSNPu200n1PhrNMJls4pz989qzlwzik7O1uXXXaZ+vXrV+d2X3zxxUlvKNKtWzcdP35c5eXlSkpKauxRPRXqOiUlJWn+/PkaOHCgAoGA/v73v2vEiBHKz8/XFVdc0YQTN62tW7cqKytLR48eVbt27bR8+XL17du31m2j+VwKZ52i9VySpKVLl2rjxo3asGFDSNtH6zkV7jpZPKcIdQgmT56sLVu26P333z/ttrW9bWdtt5+JQl2n9PR0paenB69nZWVp7969+stf/nJGf3FNT0/X5s2bdeDAAS1btkzjx49XQUFBnRGK1nMpnHWK1nNp7969mjp1qlatWqXWrVuHvF+0nVORrJPFc4qXvk9jypQpWrFihdasWaMePXqcctuzzz671rftjImJUefOnRtzTM+Fs061GTJkiHbt2tUIk9nRqlUrnXvuuRo0aJDy8vJ04YUX6vHHH69122g+l8JZp9pEw7lUVFSkffv2aeDAgYqJiVFMTIwKCgr0t7/9TTExMaqqqjppn2g8pyJZp9p4fU7xjLoOzjlNmTJFy5cvV35+vtLS0k67T1ZWll577bUat61atUqDBg1SbGxsY43qqUjWqTabNm06Y196q4tzToFAoNaPReO5VJdTrVNtouFcGjFihLZu3VrjtltuuUUZGRmaPn26WrZsedI+0XhORbJOtfH8nPLsx9iMu+OOO1xCQoLLz893ZWVlwcuRI0eC29x3331u3LhxweufffaZa9u2rbvrrrvcv//9b7dgwQIXGxvrXnrpJS8eQpOIZJ0ee+wxt3z5crdz5063bds2d9999zlJbtmyZV48hCaRk5Pj1q5d63bv3u22bNni7r//fteiRQu3atUq5xzn0gnhrlM0nkt1+eFPM3NO1e5062TxnCLUdZBU62XhwoXBbcaPH++GDh1aY7/8/Hw3YMAA16pVK5eamurmzp3btIM3sUjW6U9/+pPr3bu3a926tevYsaO77LLL3Ouvv970wzehW2+91fXs2dO1atXKdenSxY0YMSIYH+c4l04Id52i8Vyqyw8DxDlVu9Otk8Vzire5BADAMH6YDAAAwwg1AACGEWoAAAwj1AAAGEaoAQAwjFADAGAYoQYAwDBCDQCAYYQaMGDYsGGaNm1anR9PTU3V7NmzG+W+G9qePXvk8/m0efPmkPdZtGiROnTo0GgzAc0Zb8oBNAMbNmzQWWeddcpt8vPzNXz4cO3fv9/T6CUnJ6usrEyJiYkNer8333yzDhw4oFdeeaVB7xewjlADzUCXLl1O+fFjx4410SSn17JlS5199tlejwGcMXjpGzDi+PHjmjx5sjp06KDOnTvrwQcf1Ik/xf/Dl759Pp/mzZunMWPG6KyzztKECRM0fPhwSVLHjh3l8/l08803B7evrq7Wvffeq06dOunss8/WzJkzgx+7++67df311wevz549Wz6fT6+//nrwtvT0dD399NPB6wsXLlRmZqZat26tjIwMzZkzJ/ix2l76XrFihfr06aM2bdpo+PDhWrx4sXw+nw4cOFBjDd566y1lZmaqXbt2uuaaa1RWViZJmjlzphYvXqxXX31VPp9PPp9P+fn54S4x0Dx5+pYgAJxz372jT7t27dzUqVNdSUmJe/75513btm3d/PnznXPO9ezZ0z322GPB7SW5rl27ugULFrhPP/3U7dmzxy1btsxJcjt27HBlZWXuwIEDwfuOj493M2fOdDt37nSLFy92Pp8v+K5UK1ascAkJCa6qqso559zYsWNdYmKi++1vf+ucc66srMxJcsXFxc455+bPn++SkpLcsmXL3GeffeaWLVvmOnXq5BYtWuScc2737t1Oktu0aVPwemxsrLvnnntcSUmJe+GFF1z37t2dJLd//37nnHMLFy50sbGxbuTIkW7Dhg2uqKjIZWZmuhtuuME551xFRYX72c9+5q655prgW6kGAoHG+4QAhhBqwIChQ4e6zMxMV11dHbxt+vTpLjMz0zlXe6inTZtW4z7WrFlTI37fv+/LLrusxm2DBw9206dPd845d+DAAdeiRQtXWFjoqqurXefOnV1eXp4bPHiwc865JUuWuG7dugX3TU5OdkuWLKlxf3/4wx9cVlaWc+7kUE+fPt3169evxvYPPPDASaGW5D755JPgNk899VSN444fP96NGTPmpLUDznS89A0YMWTIEPl8vuD1rKws7dq1S1VVVbVuP2jQoJDvu3///jWuJyUlad++fZKkhIQEXXTRRcrPz9fWrVvVokULTZw4UR9//LEqKiqUn5+voUOHSpK++uor7d27V7fddpvatWsXvDz88MP69NNPaz32jh07NHjw4Bq3XXzxxSdt17ZtW/Xu3bvWGYFoxg+TAc3U6X4K/PtiY2NrXPf5fKqurg5eHzZsmPLz89WqVSsNHTpUHTt21Pnnn69169YpPz8/+OtdJ/Z55plndMkll9S4z5YtW9Z6bOdcjX+AnLgtlBlr2w6INoQaMGL9+vUnXe/Tp0+dAfyhVq1aSVKdz8BPZdiwYVqwYIFiYmI0cuRISdLQoUO1dOlS7dy5M/iMulu3burevbs+++wz3XjjjSHdd0ZGht54440atxUWFoY9Y6tWrSJ6bEBzx0vfgBF79+5Vdna2duzYoRdeeEFPPPGEpk6dGvL+PXv2lM/n07/+9S999dVXOnToUMj7XnHFFaqoqNBrr72mYcOGSfou3s8//7y6dOmivn37BredOXOm8vLy9Pjjj2vnzp3aunWrFi5cqFmzZtV63xMnTlRJSYmmT5+unTt36h//+IcWLVokSSc90z6V1NRUbdmyRTt27FB5ebmpX0kDGhOhBoz41a9+pcrKSl188cWaNGmSpkyZol//+tch79+9e3fl5ubqvvvuU7du3TR58uSQ901ISNCAAQPUqVOnYJQvv/xyVVdXB59NnzBhwgQ9++yzWrRokS644AINHTpUixYtUlpaWq33nZaWppdeekkvv/yy+vfvr7lz5+qBBx6QJMXFxYU84+2336709HQNGjRIXbp00bp160LeF2jOfI5vAgFoYo888ojmzZunvXv3ej0KYB7fowbQ6ObMmaPBgwerc+fOWrdunf785z+H9YwfiGaEGkCj27Vrlx5++GF98803SklJ0d13362cnByvxwKaBV76BgDAMH6YDAAAwwg1AACGEWoAAAwj1AAAGEaoAQAwjFADAGAYoQYAwDBCDQCAYf8PKg+Fi5sntn0AAAAASUVORK5CYII=)

---

**[Input:]**

```python
sns.relplot(data, x = "birthweight", y = "head.circumference", hue = "smoker")
```

**[Output:]**

```
<seaborn.axisgrid.FacetGrid at 0x168b95880>
```

![output image](data:image/png;base64,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goyIiIiYloKMiIiImJaCjIiIiJiWgoyIiIiYloKMiIiImJaCjIiIiJiWgoyIiIiYloKMiIiImJaXuwsQEXGZjHjITQGLJ3j7g91W1O4fDoHh7q3NxbJthSRn2cjJtxPk60WDYF/8vD3dXZZIjVOQERHzy8+GEz/DNw9A+smitgbtYdD/wQ8vgmHAjW9Dg3burdNF4tNzmbt8H9/uisfuMPD18mBMTHMm92tFg2A/d5cnUqMshmEY7i6iOmVkZBASEkJ6ejpWq9Xd5YhIdYj/Fd4dAIajZLt3ANzyCXw6Cvzrwd0bIDTKLSW6Skp2Pg8s2s4PB5NL9U3o24JHh7XD31t/o8rFQ2NkRMTcbFkQ+0LpEANQkAOH10LLAZCTAsd+qOnqXO5slq3MEAPwyaYTJGfm13BFIu6lICMi5pafBfE7yu9P+C+EtSr6/6PmDzLx6Xnl9uXbHaTnFtRgNSLupyAjIubm5QshTcrvD2kK2UlF/9+gfc3UVI3CAn3K7bNYINBXl5Xk4qIgIyLm5l8P+k8vu89igQ7Xw8FV4OkNHa6r2dqqQUSwL63qB5bZN6BtA8IrCDoidZGCjIiYX+PLYOAT4PG76cdefjDsBdj9FXj6wO1fFp2dMbkIqx/vj+tB8/CAEu3dokJ49sYuWP293VSZiHto1pKI1A22rKJLSMn7wcMLQptDVhIYhVCvJQQ1Aq+680v+TEYe8em5nMmwEVXPnwirH/WDfN1dlkiNU5ARERER09KlJRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS23Bpn58+cTHR2N1WrFarUSExPDihUrSiyzd+9ebrjhBkJCQggODqZPnz6cOHHCTRWLXFzyC+2cTM3hSFIW8em5GIYBQLatkLiUHI4mZ5OUaSv5JnsBpMXB2UOQfgocdjdUblJZiXD2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REQEzz33HADp6encfffdREREYLVaueqqq/j111+Ll589ezbdunXjww8/pFWrVvj6+uKqBws4dWnp3DOXBg0aVKLdMAwsFgt2u/3CKxMREZFS4uPjue222/jb3/7GjTfeSGZmJj/88ENxMPj+++9p2rQpGzZsYOPGjUycOJGff/6Zfv368csvv/D5559zzz33MGTIEKKiosjJyWHYsGH06dOHzZs3k5iYyF133cXUqVNZsGBBqe3HxsYycuRI5syZw5QpUzAMg2uvvZawsDCWL19OSEgI77zzDoMGDeLAgQOEhYUBcOjQIb744guWLFmCp6eny/aHUzfEW79+fYX9/fv3d7ogV9MN8UREpC7Ztm0b3bt359ixYzRv3rxE3/jx44mNjeXIkSN4eBRddGnfvj0RERFs2LABALvdTkhICO+//z633nor7733HtOnTycuLo7AwEAAli9fzvXXX8/p06dp2LBh8WDfO++8kzFjxvDOO+9w2223AUXB6cYbbyQxMRFfX9/iWlq3bs1jjz3G3XffzezZs3n++ec5deoUDRo0cOn+cOqMTG0KKiIiIheTrl27MmjQILp06cLQoUO5+uqrGT16NPXq1QOgU6dOxSEGoGHDhnTu3Ln4a09PT8LDw0lMTARg7969dO3atTjEAPTt2xeHw8H+/ftp2LAhAL/88gvffvstX375JTfeeGPxslu3biUrK4vw8PASdebm5nL48OHir5s3b+7yEANOBplzqa48/fr1c6oYERERqZinpydr1qzhp59+YvXq1bz++us8/vjj/PLLLwCl7u1msVjKbDv3wOdzw0LK8vv2Sy65hPDwcD788EOuvfZafHx8AHA4HERGRhIbG1vq/aGhocX///ug5EpOBZkBAwaUavv9h9UYGRERkepjsVjo27cvffv25f/+7/9o3rw5S5cudWpdHTt2ZOHChWRnZxeHjY0bN+Lh4UHbtm2Ll6tfvz5fffUVAwYM4JZbbuGLL77A29ubyy67jISEBLy8vGjRooUrPl6VODVrKTU1tcQrMTGRlStX0rNnT1avXu3qGkVEROR/fvnlF55//nm2bNnCiRMn+Oqrr0hKSqJDhw5Ore+OO+7Az8+PcePG8d///pd169Zx3333MWbMmOLLSudERETw/fffs2/fPm677TYKCwsZPHgwMTExjBw5klWrVnHs2DF++ukn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J06c4IMPPqB79+5YLBa2bNnCpEmTiIqKYtmyZVVdZbXRGRkREamzUo/B692LLiP9UTWOkTln/vz5vPzyy1x99dUcPHiQVatWAdC3b1/at2/PBx9U7mzQ/v37ad++PVu3buWyyy6rUg1OnZH58MMPGTduHL169SpOToWFhQwdOpT333/fmVWKiIhIVdVrUTQ7adl9JcOMhxfc8Ea1T8G+4447eOSRR3jvvff4xz9+G4/zf//3f1x33XVERUVx88034+Hhwc6dO9m1axfPPvssCxYswG6307t3bwICAvj444/x9/enefOqn0G6oBviHThwgH379mEYBh06dKBt27bOrqra6IyMiIjUecX3kTledDmpBu8jM3bsWL777rtSU7FXrVrF008/zfbt2/H29qZ9+/bcddddTJo0ia+//pq5c+eyd+9e7HY7Xbp04dlnn2XQoEFV3r7u7CsiIiJOGzJkCB06dHDqHjCu4PSdfU+ePMmyZcs4ceIE+fn5JfpeeumlCy5MREREaq+UlBRWr17N999/zxtvvOG2OpwKMmvXruWGG26gZcuW7N+/n86dO3Ps2DEMw6jyIB0RERExn8suu4zU1FReeOEF2rVr57Y6nLq01KtXL4YNG8bTTz9NcHAwv/76KxEREdxxxx0MGzaMKVOmVEetTtGlJRERkbqr0nf2/b29e/cybtw4ALy8vMjNzSUoKIinn36aF154waUFioiIiJTHqSATGBiIzWYDoHHjxhw+fLi4Lzk52TWViYiIiJyHU2Nk+vTpw8aNG+nYsSPXXnstDz/8MLt27eKrr76iT58+rq5RREREpExOBZmXXnqJrKwsoOgx3FlZWXz++ee0bt2al19+2aUFioiIiJRH95ERERER03JqjAxAWloa77//PjNnziQlJQWAbdu2cerUKZcVJyIiIlIRpy4t7dy5k8GDBxMSEsKxY8eYNGkSYWFhLF26lOPHj5d43oKIiIhIdXHqjMxDDz3E+PHjOXjwIH5+fsXtw4cPZ8OGDS4rTkRERKQiTgWZzZs3M3ny5FLtTZo0ISEh4YKLEhEREakMp4KMn58fGRkZpdr3799PgwYNLrgokQtmL4CcFMjPrtzy+dlFy9sLq7Ws3IJC0rLzyS+0V+t2zknPLSAjt+C3huLPWVDuezJyC0jPLb/fGXaHQVpOPtm2CtZbmFdUW0GeS7ft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+BUXF1ed5Veeh2fReIvytL8O/OvVXD11zLBOkeX2DWjbAKufV9mdvlZofGn5K2414MIKExGRauX2IOPj40Pr1q3p0aMHc+bMoWvXrrz66qvF/QUFBfzpT3/i6NGjrFmz5rzjXHx9fYtnQZ171RqNL4VG0aXb/ULgimng7V/zNdURLeoH0veS+qXafb08mDG8A8F+3mW/MbB+0aBejzKCTqebILixiysVERFXKufPVPcxDAObzQb8FmIOHjzIunXrCA8Pd3N1F8gaCbd/Dr8ugi0fQEEOtLserngQ6rVwd3Wm1iDYl5du6cqKXfF8sPEoGbmFDGjXgPuuakOL8ApmLEHRrLHJG2Ddc3D8JwgIh74PQtuhEGjyY05EpI5z66ylWbNmMXz4cKKiosjMzGTRokXMnTuXlStXMnDgQEaNGsW2bdv49ttvadiwYfH7wsLC8PHxqdQ2atWspXMc9qKBvYaj6HKSzsS4jGEYJGXZcDgMrH7eBPhWIavbMoteHl4QFFF9RYqIiMu49YzMmTNnGDNmDPHx8YSEhBAdHc3KlSsZMmQIx44dY9myZQB069atxPvWrVvHgAEDar5gV/HwhOBG7q6iTrJYLEQE+zn3Zt/gopeIiJhGrbuPjKvVyjMyIiIi4hJuH+wrIiIi4iwFGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLbcGmfnz5xMdHY3VasVqtRITE8OKFSuK+w3DYPbs2TRu3Bh/f38GDBjA7t27a77QwnxIPQ57v4MtH0H8r5CdXPN1uFtmPBz/uWgfHF4H6SfdXVH1yc+ClCOw8wvY9jEkHYDcNHdXJSIif+Dlzo03bdqUuXPn0rp1awAWLlzIiBEj2L59O506deJvf/sbL730EgsWLKBt27Y8++yzDBkyhP379xMcHFwzRdrz4cRP8M9boSD3t/aWA+DGt8EaWTN1uFvqMfhkFJw99FtbYAMYtwwiOrqtrGqRl14UYFY8Bobjt/be90C/RyGwvvtqExGREiyGYRjuLuL3wsLCmDdvHhMmTKBx48Y8+OCDTJ8+HQCbzUbDhg154YUXmDx5cqXWl5GRQUhICOnp6Vit1qoXlHoM3uwFhbbSfZffD1f9Fbx8qr5eM8lJhc/vgOMbS/eFRMHENXUr0MX/Cu/0K7vvlk+hw3U1W4+IiJSr1oyRsdvtLFq0iOzsbGJiYjh69CgJCQlcffXVxcv4+vrSv39/fvrpp3LXY7PZyMjIKPG6IMc3lh1iALZ8CNmJF7Z+M8hJLjvEAKTHQWZCzdZTnewF8Ms75ff/+CLkpNRcPSIiUiG3B5ldu3YRFBSEr68v99xzD0uXLqVjx44kJBT9cmzYsGGJ5Rs2bFjcV5Y5c+YQEhJS/IqKirqwAtPiyu/Lzyr6xVfXFeRU3J+XWjN11AR7fsVjf7ISi5YREZFawe1Bpl27duzYsYNNmzYxZcoUxo0bx549e4r7LRZLieUNwyjV9nszZ84kPT29+BUXV0EQqYxmMeX3hbUC74ALW78Z+IWCl1/5/SEXGBZrEy9/uOSq8vujeoNvDY3PEhGR83J7kPHx8aF169b06NGDOXPm0LVrV1599VUaNWoEUOrsS2JiYqmzNL/n6+tbPAvq3OuC1G8L9duU3Tf0OQguv5Y6I7gh9H2g7L6OI+vW4FcPD+h0Y1F4+yNP76LBvj6BNV6WiIiUze1B5o8Mw8Bms9GyZUsaNWrEmjVrivvy8/NZv349l19+ec0VZI2EPy+FjjeCh+f/2prAzQuhWd+aq8OdvPyg1yQY8vRvv+C9/aHPvTD8BfCv59byXC60GUxYCc1/9/2N6AjjlxedhRMRkVrDrbOWZs2axfDhw4mKiiIzM5NFixYxd+5cVq5cyZAhQ3jhhReYM2cOH330EW3atOH5558nNja2StOvL3jW0jm2rKJBr4X54BsE1sbOr8us7IWQFQ/5OUVBJqghePm6u6rqk5MKuSlFU7D9QiGogbsrEhGRP3DrfWTOnDnDmDFjiI+PJyQkhOjo6OIQA/DYY4+Rm5vLvffeS2pqKr1792b16tU1dw+Z3/MNKnpdzDy96tZ4mPMJqFf0EhGRWqvW3UfG1Vx2RkZERERqnVo3RkZERESkshRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS03Pr065pw7pmYGRkZbq5ERESkpODgYCwWi7vLMLU6H2QyMzMBiIqKcnMlIiIiJaWnp2O1Wt1dhqlZjHOnLOooh8PB6dOn3ZJ6MzIyiIqKIi4uTgdqGbR/zk/76Py0jyqm/XN+7txHOiNz4er8GRkPDw+aNm3q1hqsVqt+gFRA++f8tI/OT/uoYto/56d9ZE4a7CsiIiKmpSAjIiIipqUgU418fX158skn8fX1dXcptZL2z/lpH52f9lHFtH/OT/vI3Or8YF8RERGpu3RGRkRERExLQUZERERMS0FGRERETEtBxklz5syhZ8+eBAcHExERwciRI9m/f/9537d+/Xq6d++On58frVq14u23366BamueM/snNjYWi8VS6rVv374aqrpmzZ8/n+jo6OJ7V8TExLBixYoK33OxHD/nVHUfXWzH0B/NmTMHi8XCgw8+WOFyF9txdE5l9s/FfgyZkYKMk9avX89f/vIXNm3axJo1aygsLOTqq68mOzu73PccPXqUa665hiuvvJLt27cza9Ys7r//fpYsWVKDldcMZ/bPOfv37yc+Pr741aZNmxqouOY1bdqUuXPnsmXLFrZs2cJVV13FiBEj2L17d5nLX0zHzzlV3UfnXCzH0O9t3ryZd999l+jo6AqXuxiPI6j8/jnnYjyGTMsQl0hMTDQAY/369eUu89hjjxnt27cv0TZ58mSjT58+1V2e21Vm/6xbt84AjNTU1JorrJapV6+e8f7775fZdzEfP79X0T66WI+hzMxMo02bNsaaNWuM/v37Gw888EC5y16Mx1FV9s/FegyZmc7IuEh6ejoAYWFh5S7z888/c/XVV5doGzp0KFu2bKGgoKBa63O3yuyfcy699FIiIyMZNGgQ69atq+7SagW73c6iRYvIzs4mJiamzGUu5uMHKrePzrnYjqG//OUvXHvttQwePPi8y16Mx1FV9s85F9sxZGZ1/llLNcEwDB566CGuuOIKOnfuXO5yCQkJNGzYsERbw4YNKSwsJDk5mcjIyOou1S0qu38iIyN599136d69OzabjY8//phBgwYRGxtLv379arDimrNr1y5iYmLIy8sjKCiIpUuX0rFjxzKXvViPn6rso4vxGFq0aBHbtm1j8+bNlVr+YjuOqrp/LsZjyOwUZFxg6tSp7Ny5kx9//PG8y/7xKafG/+5HWJefflrZ/dOuXTvatWtX/HVMTAxxcXH8/e9/r7M/QNq1a8eOHTtIS0tjyZIljBs3jvXr15f7i/piPH6qso8utmMoLi6OBx54gNWrV+Pn51fp910sx5Ez++diO4bqAl1aukD33Xcfy5YtY926ded9ynajRo1ISEgo0ZaYmIiXlxfh4eHVWabbVGX/lKVPnz4cPHiwGiqrHXx8fGjdujU9evRgzpw5dO3alVdffbXMZS/G4weqto/KUpePoa1bt5KYmEj37t3x8vLCy8uL9evX89prr+Hl5YXdbi/1novpOHJm/5SlLh9DdYHOyDjJMAzuu+8+li5dSmxsLC1btjzve2JiYvjmm29KtK1evZoePXrg7e1dXaW6hTP7pyzbt2+vc6e6K2IYBjabrcy+i+n4qUhF+6gsdfkYGjRoELt27SrRduedd9K+fXumT5+Op6dnqfdcTMeRM/unLHX5GKoT3DbM2OSmTJlihISEGLGxsUZ8fHzxKycnp3iZGTNmGGPGjCn++siRI0ZAQIAxbdo0Y8+ePcYHH3xgeHt7G4sXL3bHR6hWzuyfl19+2Vi6dKlx4MAB47///a8xY8YMAzCWLFnijo9Q7WbOnGls2LDBOHr0qLFz505j1qxZhoeHh7F69WrDMC7u4+ecqu6ji+0YKssfZ+XoOCrpfPtHx5D56IyMk+bPnw/AgAEDSrR/9NFHjB8/HoD4+HhOnDhR3NeyZUuWL1/OtGnTePPNN2ncuDGvvfYao0aNqqmya4wz+yc/P59HHnmEU6dO4e/vT6dOnfjuu++45ppraqrsGnXmzBnGjBlDfHw8ISEhREdHs3LlSoYMGQJc3MfPOVXdRxfbMVQZOo4qpmPI/PT0axERETEtDfYVERER01KQEREREdNSkBERERHTUpARERER01KQEREREdNSkBERERHTUpARERER01KQEREREdNSkBGphQYMGMCDDz5Ybn+LFi145ZVXqmXdrnbs2DEsFgs7duyo9HsWLFhAaGhotdUkInWHHlEgYkKbN28mMDCwwmViY2MZOHAgqampbg0FUVFRxMfHU79+fZeud/z48aSlpfH111+7dL0iYi4KMiIm1KBBgwr7CwoKaqiS8/P09KRRo0buLkNE6ihdWhKppQoLC5k6dSqhoaGEh4fzxBNPcO7RaH+8tGSxWHj77bcZMWIEgYGB3HXXXQwcOBCAevXqYbFYih/WCeBwOHjssccICwujUaNGzJ49u7jv4Ycf5vrrry/++pVXXsFisfDdd98Vt7Vr14533nmn+OuPPvqIDh064OfnR/v27XnrrbeK+8q6tLRs2TLatGmDv78/AwcOZOHChVgsFtLS0krsg1WrVtGhQweCgoIYNmwY8fHxAMyePZuFCxfyr3/9C4vFgsViITY2tqq7WETqAjc/fVtEytC/f38jKCjIeOCBB4x9+/YZn3zyiREQEGC8++67hmEYRvPmzY2XX365eHnAiIiIMD744APj8OHDxrFjx4wlS5YYgLF//34jPj7eSEtLK1631Wo1Zs+ebRw4cMBYuHChYbFYjNWrVxuGYRjLli0zQkJCDLvdbhiGYYwcOdKoX7++8eijjxqGYRjx8fEGYOzdu9cwDMN49913jcjISGPJkiXGkSNHjCVLlhhhYWHGggULDMMwjKNHjxqAsX379uKvvb29jUceecTYt2+f8c9//tNo0qSJARipqamGYRjGRx99ZHh7exuDBw82Nm/ebGzdutXo0KGDcfvttxuGYRiZmZnGn/70J2PYsGFGfHy8ER8fb9hstur7hohIraUgI1IL9e/f3+jQoYPhcDiK26ZPn2506NDBMIyyg8yDDz5YYh3r1q0rEQ5+v+4rrriiRFvPnj2N6dOnG4ZhGGlpaYaHh4exZcsWw+FwGOHh4cacOXOMnj17GoZhGJ999pnRsGHD4vdGRUUZn332WYn1PfPMM0ZMTIxhGKWDzPTp043OnTuXWP7xxx8vFWQA49ChQ8XLvPnmmyW2O27cOGPEiBGl9p2IXFx0aUmklurTpw8Wi6X465iYGA4ePIjdbi9z+R49elR63dHR0SW+joyMJDExEYCQkBC6detGbGwsu3btwsPDg8mTJ/Prr7+SmZlJbGws/fv3ByApKYm4uDgmTpxIUFBQ8evZZ5/l8OHDZW57//799OzZs0Rbr169Si0XEBDAJZdcUmaNIiLnaLCvSB1xvllMv+ft7V3ia4vFgsPhKP56wIABxMbG4uPjQ//+/alXrx6dOnVi48aNxMbGFk/fPvee9957j969e5dYp6enZ5nbNgyjREA711aZGstaTkQubgoyIrXUpk2bSn3dpk2bcgPCH/n4+ACUewanIgMGDOCDDz7Ay8uLwYMHA9C/f38WLVrEgQMHis/INGzYkCZNmnDkyBHuuOOOSq27ffv2LF++vETbli1bqlyjj4+PU59NROoWXVoSqaXi4uJ46KGH2L9/P//85z95/fXXeeCBByr9/ubNm2OxWPj2229JSkoiKyur0u/t168fmZmZfPPNNwwYMAAoCjeffPIJDRo0oGPHjsXLzp49mzlz5vDqq69y4MABdu3axUcffcRLL71U5ronT57Mvn37mD59OgcOHOCLL75gwYIFAKXO1FSkRYsW7Ny5k/3795OcnFyrppyLSM1RkBGppcaOHUtubi69evXiL3/5C/fddx933313pd/fpEkTnnrqKWbMmEHDhg2ZOnVqpd8bEhLCpZdeSlhYWHFoufLKK3E4HMVnY8656667eP/991mwYAFdunShf//+LFiwgJYtW5a57pYtW7J48WK++uoroqOjmT9/Po8//jgAvr6+la5x0qRJtGvXjh49etCgQQM2btxY6feKSN1hMXTRWUTc7LnnnuPtt98mLi7O3aWIiMlojIyI1Li33nqLnj17Eh4ezsaNG5k3b16VzhiJiJyjICMiNe7gwYM8++yzpKSk0KxZMx5++GFmzpzp7rJExIR0aUlERERMS4N9RURExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtP4fByL7NbVIsOsAAAAASUVORK5CYII=)

---

**[Input:]**

```python

```

---

