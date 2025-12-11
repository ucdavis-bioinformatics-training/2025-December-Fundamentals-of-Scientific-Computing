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

After Anaconda is successfully installed, please open a new Command Line interface to be able to use the installed libraries. If you have chosen to ask the installer not to add configuration to your initialize conda every time you open a new shell, you will have to do it manualy when you need to access any program that Anaconda has installed. Using the following commands in the new Command Line window will accomplish this task.

source \<PATH_TO_CONDA\>/bin/activate
<br>
conda init --all

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
Cell In[12], line 1
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
Cell In[14], line 1
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

# read in the birth weight data and the miRNA expression data using the url or from your local copy
bw = pd.read_csv("https://raw.githubusercontent.com/ucdavis-bioinformatics-training/2022_February_Introduction_to_R_for_Bioinformatics/main/birthweight.csv")
mir = pd.read_csv("https://raw.githubusercontent.com/ucdavis-bioinformatics-training/2022_February_Introduction_to_R_for_Bioinformatics/main/miRNA.csv")
```

---

**[Input:]**

```python
display(bw.head(8))
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
display(mir.head(8))
```

**[Output:]**

```
  Unnamed: 0  sample.27  sample.1522  sample.569  sample.365  sample.1369  \
0     miR-16         46           56          47          54           56   
1     miR-21         52           43          40          35           59   
2   miR-146a         98           97          87          96           84   
3    miR-182         53           45          63          41           46   

   sample.1023  sample.1272  sample.1262  sample.575  ...  sample.1360  \
0           59           49           55          62  ...           70   
1           47           42           45          55  ...           57   
2           96           88           97          96  ...          111   
3           50           49           50          62  ...           46   

   sample.1058  sample.755  sample.462  sample.1088  sample.553  sample.1191  \
0           77          56          65           42          63           66   
1           55          46          58           54          54           48   
2          124         101         101          107         106          102   
3           56          50          60           63          60           50   

   sample.1313  sample.1600  sample.1187  
0           64           50           57  
1           47           44           46  
2          104          111           86  
3           42           67           43  

[4 rows x 43 columns]
```

---

It looks that the miRNA expression table uses the miRNA names as row names. We can tell the _read_csv_ function to use the first column as the row names.

**[Input:]**

```python
mir = pd.read_csv("https://raw.githubusercontent.com/ucdavis-bioinformatics-training/2022_February_Introduction_to_R_for_Bioinformatics/main/miRNA.csv", index_col = 0)
display(mir.head(8))
```

**[Output:]**

```
          sample.27  sample.1522  sample.569  sample.365  sample.1369  \
miR-16           46           56          47          54           56   
miR-21           52           43          40          35           59   
miR-146a         98           97          87          96           84   
miR-182          53           45          63          41           46   

          sample.1023  sample.1272  sample.1262  sample.575  sample.792  ...  \
miR-16             59           49           55          62          63  ...   
miR-21             47           42           45          55          45  ...   
miR-146a           96           88           97          96         104  ...   
miR-182            50           49           50          62          51  ...   

          sample.1360  sample.1058  sample.755  sample.462  sample.1088  \
miR-16             70           77          56          65           42   
miR-21             57           55          46          58           54   
miR-146a          111          124         101         101          107   
miR-182            46           56          50          60           63   

          sample.553  sample.1191  sample.1313  sample.1600  sample.1187  
miR-16            63           66           64           50           57  
miR-21            54           48           47           44           46  
miR-146a         106          102          104          111           86  
miR-182           60           50           42           67           43  

[4 rows x 42 columns]
```

---

**[Input:]**

```python
mir_trans = mir.T
display(mir_trans.head(8))
```

**[Output:]**

```
             miR-16  miR-21  miR-146a  miR-182
sample.27        46      52        98       53
sample.1522      56      43        97       45
sample.569       47      40        87       63
sample.365       54      35        96       41
sample.1369      56      59        84       46
sample.1023      59      47        96       50
sample.1272      49      42        88       49
sample.1262      55      45        97       50
```

---

In order to merge the two dataframes, we will insert a column into the transposed miRNA expression dataframe with the sample IDs. First, let's check what data type does the _ID_ column is in the birth weight dataframe.

**[Input:]**

```python
bw.dtypes
```

**[Output:]**

```
ID                               int64
birth.date                      object
location                        object
length                           int64
birthweight                    float64
head.circumference               int64
weeks.gestation                  int64
smoker                          object
maternal.age                     int64
maternal.cigarettes              int64
maternal.height                  int64
maternal.prepregnant.weight      int64
paternal.age                   float64
paternal.education             float64
paternal.cigarettes            float64
paternal.height                float64
low.birthweight                  int64
geriatric.pregnancy               bool
dtype: object
```

---

**[Input:]**

```python
mir_trans.insert(loc = 0, column = "ID", value = [int(INDEX.split(".")[1]) for INDEX in mir_trans.index])
display(mir_trans.head(8))
```

**[Output:]**

```
               ID  miR-16  miR-21  miR-146a  miR-182
sample.27      27      46      52        98       53
sample.1522  1522      56      43        97       45
sample.569    569      47      40        87       63
sample.365    365      54      35        96       41
sample.1369  1369      56      59        84       46
sample.1023  1023      59      47        96       50
sample.1272  1272      49      42        88       49
sample.1262  1262      55      45        97       50
```

---

**[Input:]**

```python
mir_trans.dtypes
```

**[Output:]**

```
ID          int64
miR-16      int64
miR-21      int64
miR-146a    int64
miR-182     int64
dtype: object
```

---

**[Input:]**

```python
# merge the two dataframes
data = pd.merge(bw, mir_trans, on = "ID", how = "inner")
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

   weeks.gestation smoker  maternal.age  maternal.cigarettes  ...  \
0               38     no            31                    0  ...   
1               39     no            27                    0  ...   
2               41     no            27                    0  ...   
3               41    yes            37                   25  ...   
4               39    yes            21                   17  ...   
5               39    yes            22                    7  ...   
6               40    yes            26                   25  ...   
7               34     no            26                    0  ...   

   paternal.age  paternal.education  paternal.cigarettes  paternal.height  \
0           NaN                 NaN                  NaN              NaN   
1          27.0                14.0                  0.0            178.0   
2          37.0                14.0                  0.0            170.0   
3          46.0                 NaN                  0.0            175.0   
4          24.0                12.0                  7.0            179.0   
5          23.0                14.0                 25.0              NaN   
6          30.0                10.0                 25.0            181.0   
7          25.0                12.0                 25.0            175.0   

   low.birthweight  geriatric.pregnancy  miR-16  miR-21  miR-146a  miR-182  
0                0                False      57      49       116       48  
1                0                False      68      47        98       57  
2                0                False      49      48        98       55  
3                0                 True      46      52        98       53  
4                0                False      56      43        97       45  
5                1                False      47      40        87       63  
6                0                False      54      35        96       41  
7                0                False      59      56       101       74  

[8 rows x 22 columns]
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
<seaborn.axisgrid.FacetGrid at 0x320f2d940>
```

![output image](data:image/png;base64,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)

---

**[Input:]**

```python
# One may define a different bin size from the default
sns.displot(data, x = "birthweight", hue = "location", multiple = "stack")
```

**[Output:]**

```
<seaborn.axisgrid.FacetGrid at 0x321309a90>
```

![output image](data:image/png;base64,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9nnNX3vwx88IALWMsaXsCofD4TZsWdZV437K6XTyDzpqhcEdQtQ1IsDuGB6VcixH89cetDsGANjC2EdiNG3aVNL/f8bsiqysrKvOngEAAFR3xpayyMhINW3aVFu2bHGNu3TpkrZv364bb7zRxmQAAACeZ+vly3Pnzunrr792DR89elR79+5VYGCgwsPDNWXKFC1cuFCtW7dW69attXDhQvn5+enuu++2MTUAAIDn2VrKkpKS1LdvX9fwlRv0R48ereXLl2vGjBm6cOGCxo0bp9OnT+uGG27Q5s2b5e/vb1dkAACASmFrKevTp48syypxusPhUFxcnOLi4qouFAAAgA2MvacMAACgNqGUAQAAGIBSBgAAYABKGQAAgAEoZQAAAAaglAEAABiAUgYAAGAAShkAAIABKGUAAAAGoJQBAAAYgFIGAABgAEoZAACAAShlAAAABqCUAQAAGIBSBgAAYABKGQAAgAEoZQAAAAaglAEAABiAUgYAAGAAShkAAIABKGUAAAAGoJQBAAAYgFIGAABgAEoZAACAAShlAAAABqCUAQAAGIBSBgAAYABKGQAAgAEoZQAAAAaglAEAABiAUgYAAGAAShkAAIABKGUAAAAGoJQBAAAYgFIGAABgAEoZAACAAShlAAAABqCUAQAAGIBSBgAAYABKGQAAgAEoZQAAAAaglAEAABiAUgYAAGAAShkAAIABKGUAAAAGoJQBAAAYgFIGAABgAEoZAACAAShlAAAABqCUAQAAGIBSBgAAYACjS9nly5c1b948RUZGytfXVy1bttTjjz+uoqIiu6MBAAB4lLfdAUrzzDPP6JVXXtGKFSvUrl07JSUl6d5771VAQIAmT55sdzwAAACPMbqUffrppxo2bJiGDBkiSYqIiNCqVauUlJRkczIAAADPMvryZa9evbR161YdPHhQkvTFF19o586dGjx4cInL5OfnKzc31+0HAADAdEafKZs5c6ZycnLUpk0b1alTR4WFhXrqqaf0pz/9qcRl4uPjtWDBgipMCQAAcO2MPlP29ttv66233tLKlSuVkpKiFStW6Nlnn9WKFStKXGb27NnKyclx/Rw/frwKEwMAAFSM0WfKpk+frlmzZumuu+6SJHXo0EHffPON4uPjNXr06GKXcTqdcjqdVRkTAADgmhl9puz8+fPy8nKPWKdOHR6JAQAAahyjz5QNHTpUTz31lMLDw9WuXTvt2bNHixcv1tixY+2OBgAA4FFGl7IXXnhB8+fP17hx45SVlaVmzZrpoYce0qOPPmp3NAAAAI8yupT5+/tryZIlWrJkid1RAAAAKpXR95QBAADUFpQyAAAAA1DKAAAADEApAwAAMAClDAAAwACUMgAAAANQygAAAAxAKQMAADAApQwAAMAAlDIAAAADUMoAAAAMQCkDAAAwQIVKWcuWLXXy5Mmrxp85c0YtW7a85lAAAAC1TYVK2bFjx1RYWHjV+Pz8fH377bfXHAoAAKC28S7PzBs2bHD9+YMPPlBAQIBruLCwUFu3blVERITHwgEAAHv16dNHnTt31pIlS2zLMGbMGJ05c0br16+3LUNVKFcpGz58uCTJ4XBo9OjRbtN8fHwUERGhv/71rx4LBwAAao9jx44pMjJSe/bsUefOnV3j//a3v8myLPuCVZFylbKioiJJUmRkpHbv3q3g4OBKCQUAAHDFT6/M1WQVuqfs6NGjFDIAAGqZ06dP65577lHjxo3l5+enQYMG6dChQ27z7Nq1S71795afn58aN26sgQMH6vTp05Kk999/X7169VKjRo0UFBSk2267TYcPH3YtGxkZKUnq0qWLHA6H+vTpI+nHy5dXrtZJP97DPmnSJIWEhKhevXrq1auXdu/e7ZqemJgoh8OhrVu3KiYmRn5+frrxxhuVnp5eSXvGMyr8SIytW7dqzpw5uv/++zV27Fi3HwAAUPOMGTNGSUlJ2rBhgz799FNZlqXBgweroKBAkrR3717169dP7dq106effqqdO3dq6NChri8H5uXladq0adq9e7e2bt0qLy8v/f73v3ddifv8888lSR9++KEyMzO1du3aYnPMmDFDa9as0YoVK5SSkqJWrVpp4MCBOnXqlNt8c+fO1V//+lclJSXJ29vb+I5SrsuXVyxYsECPP/64YmJiFBoaKofD4elcAADAIIcOHdKGDRu0a9cu3XjjjZKkf/zjHwoLC9P69et1xx13aNGiRYqJidHLL7/sWq5du3auP99+++1u63z99dcVEhKir776Su3bt9d1110nSQoKClLTpk2LzZGXl6eEhAQtX75cgwYNkiS99tpr2rJli15//XVNnz7dNe9TTz2l3r17S5JmzZqlIUOG6OLFi6pXr54H9ojnVaiUvfLKK1q+fLlGjRrl6TwAAMBAqamp8vb21g033OAaFxQUpKioKKWmpkr68UzZHXfcUeI6Dh8+rPnz5+uzzz5Tdna26wxZRkaG2rdvX6Ychw8fVkFBgXr27Oka5+Pjox49erhyXNGxY0fXn0NDQyVJWVlZCg8PL9O2qlqFStmlS5dcLRkAANR8JX370bIs1xUzX1/fUtcxdOhQhYWF6bXXXlOzZs1UVFSk9u3b69KlS+XO8fOrdD/NcYWPj4/rz1emXSmCJqrQPWX333+/Vq5c6eksAADAUG3bttXly5f1n//8xzXu5MmTOnjwoKKjoyX9eGZq69atxS5/8uRJpaamat68eerXr5+io6NdXwC4om7dupJU7APqr2jVqpXq1q2rnTt3usYVFBQoKSnJlaO6qtCZsosXL2rp0qX68MMP1bFjR7cmKkmLFy/2SDjgWmVkZCg7O9vuGB7189PzNVFN/IzBwcHGXjIByqJ169YaNmyYHnjgAb366qvy9/fXrFmz1Lx5cw0bNkySNHv2bHXo0EHjxo3Tn//8Z9WtW1fbtm3THXfcocDAQAUFBWnp0qUKDQ1VRkaGZs2a5baNkJAQ+fr66v3339f111+vevXqXfU4jPr16+vhhx/W9OnTFRgYqPDwcC1atEjnz5/XfffdV2X7ozJUqJTt27fP9VC3L7/80m0aN/3DFBkZGWrTJloXLpy3O0olcCgz56KkmvXsnh8/k0MjR460O4rH+fr6KS0tlWKGam3ZsmWaPHmybrvtNl26dEk333yzNm3a5Do58+tf/1qbN2/WnDlz1KNHD/n6+uqGG27Qn/70J3l5eWn16tWaNGmS2rdvr6ioKD3//POux15Ikre3t55//nk9/vjjevTRR3XTTTcpMTHxqhxPP/20ioqKNGrUKJ09e1YxMTH64IMP1Lhx4yraE5XDYdXwR+Tm5uYqICBAOTk5atiwod1xUIVSUlLUrVs33TD2MTUMjbA7jsf8cDRNe1c+o7ce7KwRsc3tjuNR//j0W41culed756p6yLb2B3HY3Izj+k/byxQcnKyunbtanccAIaq0JkyoDppGBqhwPAou2N4zIW8mnjmz12DkPAa9d8MAMqiQqWsb9++pV6m/OijjyocCAAAoDaqUCn76UtCpR+/9bB37159+eWXV72oHAAAAL+sQqXsueeeK3Z8XFyczp07d02BAAAAaqMKv/uyOCNHjtQbb7zhyVUCAADUCh4tZZ9++qmx75MCAAAwWYUuX/7hD39wG7YsS5mZmUpKStL8+fM9EgwAAKA2qVAp+/nTdb28vBQVFaXHH39cAwYM8EgwAACA2qRCpWzZsmWezgEAAMqpKl8lx6vCKt81PTw2OTlZqampcjgcatu2rbp06eKpXAAAoBRV/Sq52vyqsIiICE2ZMkVTpkyp1O1UqJRlZWXprrvuUmJioho1aiTLspSTk6O+fftq9erVuu666zydEwAA/ER2drYuXDhfJa+Su/KqsOzs7HKXshMnTig+Pl4bN27Uf//7XwUEBKh169YaOXKk7rnnHvn5+VVS6uqnQqVs4sSJys3N1YEDBxQdHS1J+uqrrzR69GhNmjRJq1at8mhIAABQPJNfJXfkyBH17NlTjRo10sKFC9WhQwddvnxZBw8e1BtvvKFmzZrpd7/7nS3ZLMtSYWGhvL3NeeNkhR6J8f777yshIcFVyCSpbdu2eumll/Tee+95LBwAAKi+xo0bJ29vbyUlJenOO+9UdHS0OnTooNtvv10bN27U0KFDJUk5OTl68MEHFRISooYNG+qWW27RF1984VpPXFycOnfurDfffFMREREKCAjQXXfdpbNnz7rmsSxLixYtUsuWLeXr66tOnTrpnXfecU1PTEyUw+HQBx98oJiYGDmdTu3YsUOHDx/WsGHD1KRJEzVo0EDdu3fXhx9+WHU76ScqVMqKiork4+Nz1XgfHx8VFRVdcygAAFC9nTx5Ups3b9b48eNVv379YudxOByyLEtDhgzRiRMntGnTJiUnJ6tr167q16+fTp065Zr38OHDWr9+vd599129++672r59u55++mnX9Hnz5mnZsmVKSEjQgQMHNHXqVI0cOVLbt2932+aMGTMUHx+v1NRUdezYUefOndPgwYP14Ycfas+ePRo4cKCGDh2qjIyMytkxpajQObtbbrlFkydP1qpVq9SsWTNJ0rfffqupU6eqX79+Hg0IAACqn6+//lqWZSkqyv3SanBwsC5evChJGj9+vAYOHKj9+/crKytLTqdTkvTss89q/fr1euedd/Tggw9K+vGE0PLly+Xv7y9JGjVqlLZu3aqnnnpKeXl5Wrx4sT766CPFxsZKklq2bKmdO3fq1VdfVe/evV3bf/zxx9W/f3/XcFBQkDp16uQafvLJJ7Vu3Tpt2LBBEyZMqIQ9U7IKlbIXX3xRw4YNU0REhMLCwuRwOJSRkaEOHTrorbfe8nRGAABQTTkcDrfhzz//XEVFRRoxYoTy8/OVnJysc+fOKSgoyG2+Cxcu6PDhw67hiIgIVyGTpNDQUGVlZUn68b72ixcvupUtSbp06dJVT4aIiYlxG87Ly9OCBQv07rvv6rvvvtPly5d14cKF6nOmLCwsTCkpKdqyZYvS0tJkWZbatm2rW2+91dP5AABANdSqVSs5HA6lpaW5jW/ZsqUkydfXV9KPZ8BCQ0OVmJh41ToaNWrk+vPPb5tyOByuW6au/O/GjRvVvHlzt/munH274ueXUqdPn64PPvhAzz77rFq1aiVfX1/98Y9/1KVLl8r4ST2nXKXso48+0oQJE/TZZ5+pYcOG6t+/v6uV5uTkqF27dnrllVd00003VUpYAABQPQQFBal///568cUXNXHixBLvK+vatatOnDghb29vRUREVGhbbdu2ldPpVEZGhtulyrLYsWOHxowZo9///veSpHPnzunYsWMVynGtylXKlixZogceeEANGza8alpAQIAeeughLV68mFIGAEAVyc08Zuw2Xn75ZfXs2VMxMTGKi4tTx44d5eXlpd27dystLU3dunXTrbfeqtjYWA0fPlzPPPOMoqKi9N1332nTpk0aPnz4VZcbi+Pv769HHnlEU6dOVVFRkXr16qXc3Fx98sknatCggUaPHl3isq1atdLatWs1dOhQORwOzZ8/37YvLZarlH3xxRd65plnSpw+YMAAPfvss9ccCgAAlC44OFi+vn76zxsLqmR7vr5+Cg4OLtcyv/rVr7Rnzx4tXLhQs2fP1n//+185nU61bdtWjzzyiMaNGyeHw6FNmzZp7ty5Gjt2rH744Qc1bdpUN998s5o0aVLmbT3xxBMKCQlRfHy8jhw5okaNGqlr166aM2dOqcs999xzGjt2rG688UYFBwdr5syZys3NLdfn9BSHZVlWWWeuV6+evvzyS7Vq1arY6V9//bU6dOigCxcueCzgtcrNzVVAQIBycnKKPcOHmislJUXdunVT/7nLjH2wYkV8m7pHO5eM11sPdtaI2Oa/vEA18o9Pv9XIpXvVa8pLah5dc17bdiojXVueutf1VX/AU3j3Zc1SrjNlzZs31/79+0ssZfv27VNoaKhHggEAgNKFh4dTlGqQcj08dvDgwXr00Uddzxf5qQsXLuixxx7Tbbfd5rFwAAAAtUW5zpTNmzdPa9eu1a9//WtNmDBBUVFRcjgcSk1N1UsvvaTCwkLNnTu3srICAADUWOUqZU2aNNEnn3yihx9+WLNnz9aV29EcDocGDhyol19+uVw35QEAAOBH5X54bIsWLbRp0yadPn3a9QqF1q1bq3HjxpWRDwAAoFao0AvJJalx48bq3r27evToUamF7Ntvv9XIkSMVFBQkPz8/de7cWcnJyZW2PQAAADtU6DVLVeX06dPq2bOn+vbtq/fee08hISE6fPiw22sXAAAAagKjS9kzzzyjsLAwLVu2zDXul17BkJ+fr/z8fNewXQ+Agzl+OJqmC3nn7Y7hMSePH7I7AiooNTXV7ggex7OrAM8xupRt2LBBAwcO1B133KHt27erefPmGjdunB544IESl4mPj9eCBVXzdGOYLT8/X3I4tHdlyW+hqL4c8vO25zUgKL8LOSclOTRy5Ei7o3icr6+f0tJSKWY2qQkPj3U4HFq3bp2GDx+uY8eOKTIyUnv27FHnzp09vi1PKS1zYmKi+vbtq9OnT5f7yp7RpezIkSNKSEjQtGnTNGfOHH3++eeaNGmSnE6n7rnnnmKXmT17tqZNm+Yazs3NVVhYWFVFhkGcTqdkWXriD79WZLCf3XE8ZtehU0rYlqHg+nXsjoIyKjh/VpKlznfP1HWRbeyO4zG5mcf0nzcWKDs7m1Jmg4yMDEW3idL5C1c/O7Qy+PnWU2paern+W2dlZWn+/Pl677339P3336tx48bq1KmT4uLiFBsbK0nKzMw04suCpZWpiIgITZkyRVOmTJFUeZmNLmVFRUWKiYnRwoULJUldunTRgQMHlJCQUGIpczqdP/6fMfB/BncIUdeIALtjeFTCtgy7I6ACGoSE16hXfsFe2dnZOn/hot56sLOiQxtU6rZSM89p5NK95S7gt99+uwoKCrRixQq1bNlS33//vbZu3apTp0655mnatGllRC5RQUGBfHx8rmkdlZXZ6FIWGhqqtm3buo2Ljo7WmjVrbEoEAIBZokMbGPmL55kzZ7Rz504lJiaqd+/ekn58rFaPHj3c5vvppcCfKioqUnh4uObNm6c///nPrvFX3mt8+PBhtWzZUjk5OZo+fbrWr1+vixcvKiYmRs8995w6deokSYqLi9P69es1adIkPfnkkzp27JgKCwvlcDgq/NlKynytKvxIjKrQs2dPpaenu407ePCgWrRoYVMiAABQFg0aNFCDBg20fv16ty/glZWXl5fuuusu/eMf/3Abv3LlSsXGxqply5ayLEtDhgzRiRMntGnTJiUnJ6tr167q16+f29m4r7/+Wv/85z+1Zs0a7d2791o/WqUxupRNnTpVn332mRYuXKivv/5aK1eu1NKlSzV+/Hi7owEAgFJ4e3tr+fLlWrFihRo1aqSePXtqzpw52rdvX5nXMWLECO3atUvffPONpB/Pnq1evdr1pZlt27Zp//79+t///V/FxMSodevWevbZZ9WoUSO98847rvVcunRJb775prp06aKOHTuWepbs+uuvdxXKKz8ZGVVzy4jRpax79+5at26dVq1apfbt2+uJJ57QkiVLNGLECLujAQCAX3D77bfru+++cz1NITExUV27dtXy5cvLtHyXLl3Upk0brVq1SpK0fft2ZWVl6c4775QkJScn69y5cwoKCnIrUUePHtXhw4dd62nRooWuu+66Mm1zx44d2rt3r9tPs2bNyvfBK8joe8ok6bbbbtNtt91mdwwAAFAB9erVU//+/dW/f389+uijuv/++/XYY49pzJgxZVp+xIgRWrlypWbNmqWVK1dq4MCBCg4OlvTjmbPQ0FAlJiZetdxPv0FZv379MueNjIy86tuX3t5VU5eMPlMGAABqlrZt2yovL6/M8999993av3+/kpOT9c4777hdLevatatOnDghb29vtWrVyu3nSnGrTow/UwYAAEqWmnnOyG2cPHlSd9xxh8aOHauOHTvK399fSUlJWrRokYYNG1bm9URGRurGG2/Ufffdp8uXL7ste+uttyo2NlbDhw/XM888o6ioKH333XfatGmThg8frpiYmHLnthOlDACAaig4OFh+vvU0cuneKtmen2+9cp19atCggW644QY999xzOnz4sAoKChQWFqYHHnhAc+bMKde2R4wYofHjx+uee+6Rr6+va7zD4dCmTZs0d+5cjR07Vj/88IOaNm2qm2++WU2aNCnXNkxAKQMAoBoKDw9Xalq6sa9Zcjqdio+PV3x8fKnzWZbl+nNERITb8BXjxo3TuHHjil3e399fzz//vJ5//vlip8fFxSkuLu4X8/bp06fYbUvSsWPHypy5tPX8EkoZAADVVHh4OK+4qkG40R8AAMAAlDIAAAADUMoAAAAMQCkD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)

---

Let's take a look at how to plot the relationship between some variables.

**[Input:]**

```python
sns.relplot(data, x = "birthweight", y = "head.circumference", hue = "smoker")
```

**[Output:]**

```
<seaborn.axisgrid.FacetGrid at 0x3213aa0d0>
```

![output image](data:image/png;base64,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goyIiIiYloKMiIiImJaCjIiIiJiWgoyIiIiYloKMiIiImJaCjIiIiJiWgoyIiIiYloKMiIiImJaXuwsQEXGZjHjITQGLJ3j7g91W1O4fDoHh7q3NxbJthSRn2cjJtxPk60WDYF/8vD3dXZZIjVOQERHzy8+GEz/DNw9A+smitgbtYdD/wQ8vgmHAjW9Dg3burdNF4tNzmbt8H9/uisfuMPD18mBMTHMm92tFg2A/d5cnUqMshmEY7i6iOmVkZBASEkJ6ejpWq9Xd5YhIdYj/Fd4dAIajZLt3ANzyCXw6Cvzrwd0bIDTKLSW6Skp2Pg8s2s4PB5NL9U3o24JHh7XD31t/o8rFQ2NkRMTcbFkQ+0LpEANQkAOH10LLAZCTAsd+qOnqXO5slq3MEAPwyaYTJGfm13BFIu6lICMi5pafBfE7yu9P+C+EtSr6/6PmDzLx6Xnl9uXbHaTnFtRgNSLupyAjIubm5QshTcrvD2kK2UlF/9+gfc3UVI3CAn3K7bNYINBXl5Xk4qIgIyLm5l8P+k8vu89igQ7Xw8FV4OkNHa6r2dqqQUSwL63qB5bZN6BtA8IrCDoidZGCjIiYX+PLYOAT4PG76cdefjDsBdj9FXj6wO1fFp2dMbkIqx/vj+tB8/CAEu3dokJ49sYuWP293VSZiHto1pKI1A22rKJLSMn7wcMLQptDVhIYhVCvJQQ1Aq+680v+TEYe8em5nMmwEVXPnwirH/WDfN1dlkiNU5ARERER09KlJRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS23Bpn58+cTHR2N1WrFarUSExPDihUrSiyzd+9ebrjhBkJCQggODqZPnz6cOHHCTRWLXFzyC+2cTM3hSFIW8em5GIYBQLatkLiUHI4mZ5OUaSv5JnsBpMXB2UOQfgocdjdUblJZiXD2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REQEzz33HADp6encfffdREREYLVaueqqq/j111+Ll589ezbdunXjww8/pFWrVvj6+uKqBws4dWnp3DOXBg0aVKLdMAwsFgt2u/3CKxMREZFS4uPjue222/jb3/7GjTfeSGZmJj/88ENxMPj+++9p2rQpGzZsYOPGjUycOJGff/6Zfv368csvv/D5559zzz33MGTIEKKiosjJyWHYsGH06dOHzZs3k5iYyF133cXUqVNZsGBBqe3HxsYycuRI5syZw5QpUzAMg2uvvZawsDCWL19OSEgI77zzDoMGDeLAgQOEhYUBcOjQIb744guWLFmCp6eny/aHUzfEW79+fYX9/fv3d7ogV9MN8UREpC7Ztm0b3bt359ixYzRv3rxE3/jx44mNjeXIkSN4eBRddGnfvj0RERFs2LABALvdTkhICO+//z633nor7733HtOnTycuLo7AwEAAli9fzvXXX8/p06dp2LBh8WDfO++8kzFjxvDOO+9w2223AUXB6cYbbyQxMRFfX9/iWlq3bs1jjz3G3XffzezZs3n++ec5deoUDRo0cOn+cOqMTG0KKiIiIheTrl27MmjQILp06cLQoUO5+uqrGT16NPXq1QOgU6dOxSEGoGHDhnTu3Ln4a09PT8LDw0lMTARg7969dO3atTjEAPTt2xeHw8H+/ftp2LAhAL/88gvffvstX375JTfeeGPxslu3biUrK4vw8PASdebm5nL48OHir5s3b+7yEANOBplzqa48/fr1c6oYERERqZinpydr1qzhp59+YvXq1bz++us8/vjj/PLLLwCl7u1msVjKbDv3wOdzw0LK8vv2Sy65hPDwcD788EOuvfZafHx8AHA4HERGRhIbG1vq/aGhocX///ug5EpOBZkBAwaUavv9h9UYGRERkepjsVjo27cvffv25f/+7/9o3rw5S5cudWpdHTt2ZOHChWRnZxeHjY0bN+Lh4UHbtm2Ll6tfvz5fffUVAwYM4JZbbuGLL77A29ubyy67jISEBLy8vGjRooUrPl6VODVrKTU1tcQrMTGRlStX0rNnT1avXu3qGkVEROR/fvnlF55//nm2bNnCiRMn+Oqrr0hKSqJDhw5Ore+OO+7Az8+PcePG8d///pd169Zx3333MWbMmOLLSudERETw/fffs2/fPm677TYKCwsZPHgwMTExjBw5klWrVnHs2DF++ukn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J06c4IMPPqB79+5YLBa2bNnCpEmTiIqKYtmyZVVdZbXRGRkREamzUo/B692LLiP9UTWOkTln/vz5vPzyy1x99dUcPHiQVatWAdC3b1/at2/PBx9U7mzQ/v37ad++PVu3buWyyy6rUg1OnZH58MMPGTduHL169SpOToWFhQwdOpT333/fmVWKiIhIVdVrUTQ7adl9JcOMhxfc8Ea1T8G+4447eOSRR3jvvff4xz9+G4/zf//3f1x33XVERUVx88034+Hhwc6dO9m1axfPPvssCxYswG6307t3bwICAvj444/x9/enefOqn0G6oBviHThwgH379mEYBh06dKBt27bOrqra6IyMiIjUecX3kTledDmpBu8jM3bsWL777rtSU7FXrVrF008/zfbt2/H29qZ9+/bcddddTJo0ia+//pq5c+eyd+9e7HY7Xbp04dlnn2XQoEFV3r7u7CsiIiJOGzJkCB06dHDqHjCu4PSdfU+ePMmyZcs4ceIE+fn5JfpeeumlCy5MREREaq+UlBRWr17N999/zxtvvOG2OpwKMmvXruWGG26gZcuW7N+/n86dO3Ps2DEMw6jyIB0RERExn8suu4zU1FReeOEF2rVr57Y6nLq01KtXL4YNG8bTTz9NcHAwv/76KxEREdxxxx0MGzaMKVOmVEetTtGlJRERkbqr0nf2/b29e/cybtw4ALy8vMjNzSUoKIinn36aF154waUFioiIiJTHqSATGBiIzWYDoHHjxhw+fLi4Lzk52TWViYiIiJyHU2Nk+vTpw8aNG+nYsSPXXnstDz/8MLt27eKrr76iT58+rq5RREREpExOBZmXXnqJrKwsoOgx3FlZWXz++ee0bt2al19+2aUFioiIiJRH95ERERER03JqjAxAWloa77//PjNnziQlJQWAbdu2cerUKZcVJyIiIlIRpy4t7dy5k8GDBxMSEsKxY8eYNGkSYWFhLF26lOPHj5d43oKIiIhIdXHqjMxDDz3E+PHjOXjwIH5+fsXtw4cPZ8OGDS4rTkRERKQiTgWZzZs3M3ny5FLtTZo0ISEh4YKLEhEREakMp4KMn58fGRkZpdr3799PgwYNLrgokQtmL4CcFMjPrtzy+dlFy9sLq7Ws3IJC0rLzyS+0V+t2zknPLSAjt+C3huLPWVDuezJyC0jPLb/fGXaHQVpOPtm2CtZbmFdUW0GeS7ft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+BUXF1ed5Veeh2fReIvytL8O/OvVXD11zLBOkeX2DWjbAKufV9mdvlZofGn5K2414MIKExGRauX2IOPj40Pr1q3p0aMHc+bMoWvXrrz66qvF/QUFBfzpT3/i6NGjrFmz5rzjXHx9fYtnQZ171RqNL4VG0aXb/ULgimng7V/zNdURLeoH0veS+qXafb08mDG8A8F+3mW/MbB+0aBejzKCTqebILixiysVERFXKufPVPcxDAObzQb8FmIOHjzIunXrCA8Pd3N1F8gaCbd/Dr8ugi0fQEEOtLserngQ6rVwd3Wm1iDYl5du6cqKXfF8sPEoGbmFDGjXgPuuakOL8ApmLEHRrLHJG2Ddc3D8JwgIh74PQtuhEGjyY05EpI5z66ylWbNmMXz4cKKiosjMzGTRokXMnTuXlStXMnDgQEaNGsW2bdv49ttvadiwYfH7wsLC8PHxqdQ2atWspXMc9qKBvYaj6HKSzsS4jGEYJGXZcDgMrH7eBPhWIavbMoteHl4QFFF9RYqIiMu49YzMmTNnGDNmDPHx8YSEhBAdHc3KlSsZMmQIx44dY9myZQB069atxPvWrVvHgAEDar5gV/HwhOBG7q6iTrJYLEQE+zn3Zt/gopeIiJhGrbuPjKvVyjMyIiIi4hJuH+wrIiIi4iwFGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLbcGmfnz5xMdHY3VasVqtRITE8OKFSuK+w3DYPbs2TRu3Bh/f38GDBjA7t27a77QwnxIPQ57v4MtH0H8r5CdXPN1uFtmPBz/uWgfHF4H6SfdXVH1yc+ClCOw8wvY9jEkHYDcNHdXJSIif+Dlzo03bdqUuXPn0rp1awAWLlzIiBEj2L59O506deJvf/sbL730EgsWLKBt27Y8++yzDBkyhP379xMcHFwzRdrz4cRP8M9boSD3t/aWA+DGt8EaWTN1uFvqMfhkFJw99FtbYAMYtwwiOrqtrGqRl14UYFY8Bobjt/be90C/RyGwvvtqExGREiyGYRjuLuL3wsLCmDdvHhMmTKBx48Y8+OCDTJ8+HQCbzUbDhg154YUXmDx5cqXWl5GRQUhICOnp6Vit1qoXlHoM3uwFhbbSfZffD1f9Fbx8qr5eM8lJhc/vgOMbS/eFRMHENXUr0MX/Cu/0K7vvlk+hw3U1W4+IiJSr1oyRsdvtLFq0iOzsbGJiYjh69CgJCQlcffXVxcv4+vrSv39/fvrpp3LXY7PZyMjIKPG6IMc3lh1iALZ8CNmJF7Z+M8hJLjvEAKTHQWZCzdZTnewF8Ms75ff/+CLkpNRcPSIiUiG3B5ldu3YRFBSEr68v99xzD0uXLqVjx44kJBT9cmzYsGGJ5Rs2bFjcV5Y5c+YQEhJS/IqKirqwAtPiyu/Lzyr6xVfXFeRU3J+XWjN11AR7fsVjf7ISi5YREZFawe1Bpl27duzYsYNNmzYxZcoUxo0bx549e4r7LRZLieUNwyjV9nszZ84kPT29+BUXV0EQqYxmMeX3hbUC74ALW78Z+IWCl1/5/SEXGBZrEy9/uOSq8vujeoNvDY3PEhGR83J7kPHx8aF169b06NGDOXPm0LVrV1599VUaNWoEUOrsS2JiYqmzNL/n6+tbPAvq3OuC1G8L9duU3Tf0OQguv5Y6I7gh9H2g7L6OI+vW4FcPD+h0Y1F4+yNP76LBvj6BNV6WiIiUze1B5o8Mw8Bms9GyZUsaNWrEmjVrivvy8/NZv349l19+ec0VZI2EPy+FjjeCh+f/2prAzQuhWd+aq8OdvPyg1yQY8vRvv+C9/aHPvTD8BfCv59byXC60GUxYCc1/9/2N6AjjlxedhRMRkVrDrbOWZs2axfDhw4mKiiIzM5NFixYxd+5cVq5cyZAhQ3jhhReYM2cOH330EW3atOH5558nNja2StOvL3jW0jm2rKJBr4X54BsE1sbOr8us7IWQFQ/5OUVBJqghePm6u6rqk5MKuSlFU7D9QiGogbsrEhGRP3DrfWTOnDnDmDFjiI+PJyQkhOjo6OIQA/DYY4+Rm5vLvffeS2pqKr1792b16tU1dw+Z3/MNKnpdzDy96tZ4mPMJqFf0EhGRWqvW3UfG1Vx2RkZERERqnVo3RkZERESkshRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS03Pr065pw7pmYGRkZbq5ERESkpODgYCwWi7vLMLU6H2QyMzMBiIqKcnMlIiIiJaWnp2O1Wt1dhqlZjHOnLOooh8PB6dOn3ZJ6MzIyiIqKIi4uTgdqGbR/zk/76Py0jyqm/XN+7txHOiNz4er8GRkPDw+aNm3q1hqsVqt+gFRA++f8tI/OT/uoYto/56d9ZE4a7CsiIiKmpSAjIiIipqUgU418fX158skn8fX1dXcptZL2z/lpH52f9lHFtH/OT/vI3Or8YF8RERGpu3RGRkRERExLQUZERERMS0FGRERETEtBxklz5syhZ8+eBAcHExERwciRI9m/f/9537d+/Xq6d++On58frVq14u23366BamueM/snNjYWi8VS6rVv374aqrpmzZ8/n+jo6OJ7V8TExLBixYoK33OxHD/nVHUfXWzH0B/NmTMHi8XCgw8+WOFyF9txdE5l9s/FfgyZkYKMk9avX89f/vIXNm3axJo1aygsLOTqq68mOzu73PccPXqUa665hiuvvJLt27cza9Ys7r//fpYsWVKDldcMZ/bPOfv37yc+Pr741aZNmxqouOY1bdqUuXPnsmXLFrZs2cJVV13FiBEj2L17d5nLX0zHzzlV3UfnXCzH0O9t3ryZd999l+jo6AqXuxiPI6j8/jnnYjyGTMsQl0hMTDQAY/369eUu89hjjxnt27cv0TZ58mSjT58+1V2e21Vm/6xbt84AjNTU1JorrJapV6+e8f7775fZdzEfP79X0T66WI+hzMxMo02bNsaaNWuM/v37Gw888EC5y16Mx1FV9s/FegyZmc7IuEh6ejoAYWFh5S7z888/c/XVV5doGzp0KFu2bKGgoKBa63O3yuyfcy699FIiIyMZNGgQ69atq+7SagW73c6iRYvIzs4mJiamzGUu5uMHKrePzrnYjqG//OUvXHvttQwePPi8y16Mx1FV9s85F9sxZGZ1/llLNcEwDB566CGuuOIKOnfuXO5yCQkJNGzYsERbw4YNKSwsJDk5mcjIyOou1S0qu38iIyN599136d69OzabjY8//phBgwYRGxtLv379arDimrNr1y5iYmLIy8sjKCiIpUuX0rFjxzKXvViPn6rso4vxGFq0aBHbtm1j8+bNlVr+YjuOqrp/LsZjyOwUZFxg6tSp7Ny5kx9//PG8y/7xKafG/+5HWJefflrZ/dOuXTvatWtX/HVMTAxxcXH8/e9/r7M/QNq1a8eOHTtIS0tjyZIljBs3jvXr15f7i/piPH6qso8utmMoLi6OBx54gNWrV+Pn51fp910sx5Ez++diO4bqAl1aukD33Xcfy5YtY926ded9ynajRo1ISEgo0ZaYmIiXlxfh4eHVWabbVGX/lKVPnz4cPHiwGiqrHXx8fGjdujU9evRgzpw5dO3alVdffbXMZS/G4weqto/KUpePoa1bt5KYmEj37t3x8vLCy8uL9evX89prr+Hl5YXdbi/1novpOHJm/5SlLh9DdYHOyDjJMAzuu+8+li5dSmxsLC1btjzve2JiYvjmm29KtK1evZoePXrg7e1dXaW6hTP7pyzbt2+vc6e6K2IYBjabrcy+i+n4qUhF+6gsdfkYGjRoELt27SrRduedd9K+fXumT5+Op6dnqfdcTMeRM/unLHX5GKoT3DbM2OSmTJlihISEGLGxsUZ8fHzxKycnp3iZGTNmGGPGjCn++siRI0ZAQIAxbdo0Y8+ePcYHH3xgeHt7G4sXL3bHR6hWzuyfl19+2Vi6dKlx4MAB47///a8xY8YMAzCWLFnijo9Q7WbOnGls2LDBOHr0qLFz505j1qxZhoeHh7F69WrDMC7u4+ecqu6ji+0YKssfZ+XoOCrpfPtHx5D56IyMk+bPnw/AgAEDSrR/9NFHjB8/HoD4+HhOnDhR3NeyZUuWL1/OtGnTePPNN2ncuDGvvfYao0aNqqmya4wz+yc/P59HHnmEU6dO4e/vT6dOnfjuu++45ppraqrsGnXmzBnGjBlDfHw8ISEhREdHs3LlSoYMGQJc3MfPOVXdRxfbMVQZOo4qpmPI/PT0axERETEtDfYVERER01KQEREREdNSkBERERHTUpARERER01KQEREREdNSkBERERHTUpARERER01KQEREREdNSkBGphQYMGMCDDz5Ybn+LFi145ZVXqmXdrnbs2DEsFgs7duyo9HsWLFhAaGhotdUkInWHHlEgYkKbN28mMDCwwmViY2MZOHAgqampbg0FUVFRxMfHU79+fZeud/z48aSlpfH111+7dL0iYi4KMiIm1KBBgwr7CwoKaqiS8/P09KRRo0buLkNE6ihdWhKppQoLC5k6dSqhoaGEh4fzxBNPcO7RaH+8tGSxWHj77bcZMWIEgYGB3HXXXQwcOBCAevXqYbFYih/WCeBwOHjssccICwujUaNGzJ49u7jv4Ycf5vrrry/++pVXXsFisfDdd98Vt7Vr14533nmn+OuPPvqIDh064OfnR/v27XnrrbeK+8q6tLRs2TLatGmDv78/AwcOZOHChVgsFtLS0krsg1WrVtGhQweCgoIYNmwY8fHxAMyePZuFCxfyr3/9C4vFgsViITY2tqq7WETqAjc/fVtEytC/f38jKCjIeOCBB4x9+/YZn3zyiREQEGC8++67hmEYRvPmzY2XX365eHnAiIiIMD744APj8OHDxrFjx4wlS5YYgLF//34jPj7eSEtLK1631Wo1Zs+ebRw4cMBYuHChYbFYjNWrVxuGYRjLli0zQkJCDLvdbhiGYYwcOdKoX7++8eijjxqGYRjx8fEGYOzdu9cwDMN49913jcjISGPJkiXGkSNHjCVLlhhhYWHGggULDMMwjKNHjxqAsX379uKvvb29jUceecTYt2+f8c9//tNo0qSJARipqamGYRjGRx99ZHh7exuDBw82Nm/ebGzdutXo0KGDcfvttxuGYRiZmZnGn/70J2PYsGFGfHy8ER8fb9hstur7hohIraUgI1IL9e/f3+jQoYPhcDiK26ZPn2506NDBMIyyg8yDDz5YYh3r1q0rEQ5+v+4rrriiRFvPnj2N6dOnG4ZhGGlpaYaHh4exZcsWw+FwGOHh4cacOXOMnj17GoZhGJ999pnRsGHD4vdGRUUZn332WYn1PfPMM0ZMTIxhGKWDzPTp043OnTuXWP7xxx8vFWQA49ChQ8XLvPnmmyW2O27cOGPEiBGl9p2IXFx0aUmklurTpw8Wi6X465iYGA4ePIjdbi9z+R49elR63dHR0SW+joyMJDExEYCQkBC6detGbGwsu3btwsPDg8mTJ/Prr7+SmZlJbGws/fv3ByApKYm4uDgmTpxIUFBQ8evZZ5/l8OHDZW57//799OzZs0Rbr169Si0XEBDAJZdcUmaNIiLnaLCvSB1xvllMv+ft7V3ia4vFgsPhKP56wIABxMbG4uPjQ//+/alXrx6dOnVi48aNxMbGFk/fPvee9957j969e5dYp6enZ5nbNgyjREA711aZGstaTkQubgoyIrXUpk2bSn3dpk2bcgPCH/n4+ACUewanIgMGDOCDDz7Ay8uLwYMHA9C/f38WLVrEgQMHis/INGzYkCZNmnDkyBHuuOOOSq27ffv2LF++vETbli1bqlyjj4+PU59NROoWXVoSqaXi4uJ46KGH2L9/P//85z95/fXXeeCBByr9/ubNm2OxWPj2229JSkoiKyur0u/t168fmZmZfPPNNwwYMAAoCjeffPIJDRo0oGPHjsXLzp49mzlz5vDqq69y4MABdu3axUcffcRLL71U5ronT57Mvn37mD59OgcOHOCLL75gwYIFAKXO1FSkRYsW7Ny5k/3795OcnFyrppyLSM1RkBGppcaOHUtubi69evXiL3/5C/fddx933313pd/fpEkTnnrqKWbMmEHDhg2ZOnVqpd8bEhLCpZdeSlhYWHFoufLKK3E4HMVnY8656667eP/991mwYAFdunShf//+LFiwgJYtW5a57pYtW7J48WK++uoroqOjmT9/Po8//jgAvr6+la5x0qRJtGvXjh49etCgQQM2btxY6feKSN1hMXTRWUTc7LnnnuPtt98mLi7O3aWIiMlojIyI1Li33nqLnj17Eh4ezsaNG5k3b16VzhiJiJyjICMiNe7gwYM8++yzpKSk0KxZMx5++GFmzpzp7rJExIR0aUlERERMS4N9RURExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtBRkRERExLQUZERERMS0FGRERETEtP4fByL7NbVIsOsAAAAASUVORK5CYII=)

---

Up until now, we have been using the default theme for the visualization from matplotlib. Let's switch to Seaborn's default theme to see if there is any difference.

**[Input:]**

```python
sns.set_theme()
```

---

**[Input:]**

```python
sns.displot(data, x = "birthweight", hue = "location", multiple = "stack")
```

**[Output:]**

```
<seaborn.axisgrid.FacetGrid at 0x321441310>
```

![output image](data:image/png;base64,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V1RUlBo2bJhnXWRkpMaNG6d58+apd+/eeu+991SjRo2AFwsAAEqGuLg4Scr3RIZJkybp3LlzkqSFCxfqk08+0c6dO5WZmamkpKQ8254/fz7PyZ6EhARFRET4/l2xYkXl5ORIUpHauFhKSoq2b9+u6dOn68CBA9q7d6++++67sLwrtNChbM6cOYqLi9Obb76pq666Ks+6ChUq6N5771XXrl1155136tVXX+VmfwAAyrA6deqoatWq2rRpk37729/6ll8cdipVqiRJ8nq9qlevnmbPnp2vnaioKN/fIyMjL9lfYdsoX758nnVz587VjBkz1LNnTyUlJalv375av369/v73vxdiLwOr0JcvN2zYoMGDB+cLZBerXLmyBgwYoA0bNgSiNgAAUEI5nU7169dPK1eu1DfffON3m6NHj0qSGjVqpCNHjqhixYpKSEhQQkKCatWqpSlTpmjz5s2F6q+4bcyePVsjR47UxIkTdffdd6tVq1bav3+/bDv0D8wt9JmyEydOFOr5Y40aNdKxY8euqCgAAOBf1biogjcypL/Bgwdr586d6t27t4YOHarOnTsrJiZGu3fv1qJFi/TFF1/ojjvu0O233645c+Zo5MiRGj16tCpWrKhXX31V//rXvzRq1KhC9VXcNmrWrKkvvvhCKSkpsixL7733nj766KOwPDut0KEsPj5eqampBW6XlpZ22bNpAACgeLxe+4qern8l/VqWo8ivsyxLU6dO1dq1a7V8+XK98cYbysjIUJUqVdS2bVstWrRI7dq1kyQtWrRIL7zwggYPHiyPx6OmTZtq/vz5uvbaawvVV8WKFYvVxgsvvKCnnnpKd9xxh6Kjo9WyZUtNmjRJEydO1KFDh1S7du0i73dxOexCnp8bPXq0Tp06pfnz5192u6FDh8qyLL366qsBKTAYPB6v0tJC9zRkl8tSXFy00tPPyO32hqxf04ViXHL7mLpkqw6fyAxKH4HmcDjkcjnldnv8nj6vXa2i/tSrtU78c5myvt8RhgoDL6p+C1XtfLemLd2mQ6k/+d2moHExTa2qMXqwd5ugf99zfPEvHONStWrFkPSD0qvQ95T17dtXGzdu1HPPPafz58/nW5+dna3nn39en332mfr06RPQIgEAAEq7Ql++vP766/XYY4/pmWee0XvvvaeOHTuqdu3a8ng8OnLkiDZu3Kj09HT96U9/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237raNeunT799FOdP3/et2zXrl2+++CKojCXbAGgpOIIBxjg5MmTGjVqlL788kstWbJE48ePV6dOndSxY8dCvb5ixYqSLtzztX379iL1fdNNN2nHjh1KTU1VUlKSJKl9+/Y6duyYDh8+nCeU9e/fX16vV/3799eaNWu0YcMGPfnkk3rjjTdUv359v+0PHz5cP/30kwYPHqx//OMfeu+99zRixAg5HA7f5dTCio2N1b59+7Rhwwb9+OOPRXotAJiOUAYY4K677lKVKlU0YsQITZs2Td27d9crr7xS6NASExOjAQMG6OOPP9bgwYOVnZ1d6L7btGmjihUrql69eqpWrZokqWnTpqpUqZLq1q2b5xJj9erV9eabb6pWrVqaOHGihg8frh07dujpp5/2PfbilxISEjR//nydP39eDzzwgF5++WUNGTJEVatWVXR0dKHrlKQ+ffooIiJCQ4YM8T1vDQBKC4fNXbQAgmjDhg2KiIjI887KH3/8UZ06ddLo0aPVr1+/MFYHAObgRn8AQfX1119r+vTpevjhh9W8eXOlp6frr3/9qypWrKjbbrst3OUBgDEIZQCCauDAgcrOztbSpUt19OhRRUVFKSkpSc8//7zi4+PDXR4AGIPLlwAAAAbgRn8AAAADEMoAAAAMQCgDAAAwAKEMAADAAIQyAAAAAxDKAAAADEAoAwAAMAChDAAAwAD/H/de0uaM8US7AAAAAElFTkSuQmCC)

---

**[Input:]**

```python
sns.relplot(data, x = "birthweight", y = "head.circumference", hue = "smoker")
```

**[Output:]**

```
<seaborn.axisgrid.FacetGrid at 0x321501e50>
```

![output image](data:image/png;base64,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nNQb0zSItHMo2vUj+dvW4opOILrP2XjCEii0Av+Zqaa9Mf77TJYtuzL46offiQl3cd5JSSSFe4mKiSaPKKyKLiapY4ZpkO+x+HL9Xn7be5iOrZpweu+WRIaaWOVcnHvM3pgGuYU+Pl+7mz0Hc+jeLpGUHi0Idxvlrq+hCcbPVVJSTJ1spzEKapAByM7OZvr06SxdupTs7Gz69u3L5MmTS27J/vLLL5kzZw5bt24lPj6ec845h9tvv53IyEi/t6kgU7+oNxVzYm/cbhOXYWNh4PHUXs2B6o3LZWKYBiFuA8vrxWuZ9XYYLyTEhW3bxSGsgguAoeq9ObI+MPB6K15fQ6Mg07AEPcgEg4JM/aLeVEy9qZh6UzH1pnIKMg2L7j0TERERx1KQEREREcdSkBERERHHUpARERERx1KQEREREcdSkBERERHHUpARERERx1KQEREREcdSkBERERHHUpARERERx1KQEREREcdSkBERERHHUpARERERx1KQEREREcdSkBERERHHUpARERERx1KQEREREcdSkBERERHHUpARERERx1KQEREREcdSkBERERHHUpARERERx1KQEREREcdSkBERERHHUpARERERx1KQEREREcdSkBERERHHUpARERERx1KQEREREcdSkBERERHHUpARERERx3IHuwARkZoyDAh1+XD5irDNEDAMDF8RPjOUIsuFbQe7wsBxuU0KvRYAYS4Tn88KckUiwaUgIyKO5jZ8hBcd5PA3b1G0fzvuuKbEnnw+nsOHyN+9ibhT/4wnIokiyxXsUmvENA0KLfjwmx0s3/A7IW4X56W0YUC3FrixGlRYE6kOBRkRcSzbtjEPbWPfG4+CXXxmwpt1kILdm2hyyqW4wiPZ/9K9JF1+N65m3fH5nPtuX+izmfzPb8jILiyZNv/dn1i2bjeTr+uLC+fum0hN6BoZEXEsX046hz6cWxJijpb57b+J7n4aYJP+8TOEW7l1X2CAuFwmH327s1SIOeLXPYfZtvcwpmkEoTKR4FOQERHH8uXn4MtOL3+m5cObk4EZHoUv9zAU5tRtcQFU4LX45offK5z/2drdGAoy0kgpyIiIYxlG5W/ehunCtv57tsZ07q87wwCXq+J9DXGZKMZIY+Xcn2wRafTMiBhCEo8vd57hDsUMi8IuysfdpDl2aFQdVxc4YS6Tc/qfUOH88we2wbJ0jYw0TgoyIuJY7uh4Ei/6K4Y79A9zDBKGDCfru/9guEJIvGg8hYZzg4zPZzGoz/Gc0DymzLyU7i1o2TRKQUYaLd21JCKO5o1uyXE3TSf3xy8o3LuZkITjiO5+Gvm7NhLSrC3xZ99Ivhnr+OetuLH5+w39+WVnBp+v202Iy+TCU9rSqlk0Lt17LY2YgoyIOJrPNsi2YwjpM4zo3h5sw0URBu7urbAMN9leG5ydYQCw7eIw07t9Aj3bJxRfE2PbOhMjjZ6CjIg0CB6vBRx56J393/9ueG/yR84sNbw9E/GPrpERERERx1KQEREREcdSkBERERHHUpARERERx1KQEREREcdSkBERERHHUpARERERx1KQEREREcdSkBERERHHUpARERERx1KQEREREcdSkBERERHHUpARERERx1KQEREREcdSkBERERHHUpARERERx1KQEREREcdSkBERERHHUpARERERx1KQEREREcdSkBERERHHUpARERERx1KQEREREcdSkBERERHHUpARERERx1KQEREREcdSkBERERHHUpARERERx1KQEREREcdy+/vCoqIi3nrrLVasWMHBgwd55JFHWL16Nd27d6dXr16BrFFERESkXH6dkUlPT+fyyy/n4YcfZufOnWzYsIGCggK+/PJLhg8fzvfffx/oOkVERETK8CvIPPHEE+Tm5vLhhx+yePFibNsGYObMmfTs2ZNZs2ZVeV1paWncfffdpKSkkJyczOjRo9m2bVvJ/NTUVCZMmEDfvn0ZMGAAEydOJD093Z+yRaSaXG4TH2AZBi7X/35dGK7i6ZgmhmGUek2oGyKMQsJdXkyz9DwpyzAgzGURYRQS5rIwGmnL3EeONQzcbl31IFXn19DSsmXLuO+++2jTpg0+n69kelhYGDfeeCOTJ0+u8rrGjBmDaZo899xzREZGMnPmTEaOHMmnn36Ky+XixhtvJCIighdffBGfz8e9997LPffcw3PPPedP6SJSBaZpUGTBl9/t5cvv9+J2mVwwsA19OiWRV+hlydKtbNmdSbMmEVx+Zkeax0fgNiDSOkz26v9QsOMHXJGxxA64BKNpW/J8ocHepXop1PQRWphO1qrFFKXuIiShJbEDL8UbkUSh5ffIv6MYhoHHhuU/7GPZut2YhsF5KW1I7pyEG5v/fk4WqZBfPymFhYU0adKk3HkulwuP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MQ0Dt0Glz5A5wjQNwowiTNuDjUGRGfwzMYHuTUOi3lRMvalcMPqTlBRTJ9tpjIJ6RsYwDJ566immT5/OHXfcQXZ2Nn379uW1116jRYsWfPjhh3g8HkaMGFHmtZ999hmtWrUKQtWB5fGBB11wFkg+n0VJxLXtcq+ZKY9l2eQTAoQcmVAL1YmISCAF9YxMsNSnMzKi3lRGvamYelMx9aZyOiPTsDS+cQwRERFpMBRkRERExLEUZERERMSxFGRERETEsRRkRERExLEUZERERMSxFGRERETEsRRkRERExLEUZERERMSxFGRERETEsRRkRERExLEUZERERMSxFGRERETEsRRkRERExLEUZERERMSxFGRERETEsRRkRERExLEUZERERMSxFGRERETEsRRkRERExLEUZERERMSxFGRERETEsRRkRERExLEUZERERMSxFGRERETEsRRkRERExLEUZERERMSxFGRERETEsRRkRERExLEUZERERMSxFGRERETEsRRkRERExLEUZERERMSxFGRERETEsRRkRERExLEUZERERMSxFGRERETEsRRkRERExLEUZERERMSxFGRERETEsRRkRERExLEUZERERMSxFGRERETEsRRkRERExLEUZERERMSxFGRERETEsRRkRERExLEUZERERMSxFGRERETEsRRkRERExLEUZERERMSxFGRERETEsRRkRERExLEUZERERMSxFGRERETEsRRkRERExLEUZERERMSxFGRERETEsRRkRERExLEUZERERMSxFGRERETEsRRkRERExLEUZERERMSxFGRERETEsRRkRERExLEUZERERMSxFGRERETEsRRkRERExLEUZERERMSxFGRERETEsRRkRERExLEUZERERMSxgh5k0tLSuPvuu0lJSSE5OZnRo0ezbdu2kvmbNm3iuuuuo0+fPgwePJjnn38+iNX+j2kauN0uXC4j2KUERWPaf7fbxO0O+o+KiIiUI+i/nceMGcPu3bt57rnneOuttwgPD2fkyJHk5+eTkZHBDTfcQNu2bXn77bcZP348M2fO5O233w5avaZpEG3mE5r2C9YP7+Las45oMxdX0DtZN8rdf6Nh7n+EWUhU0QGsHz/E3vQp0VYGYaYn2GWJiMhR3MHceEZGBq1atWLMmDF06tQJgLFjxzJs2DC2bt3KypUrCQ0NZerUqbjd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yZMnY5rFn0327NkDFA9DdevWrWQ5y7KYM2cOHTp0ACAsLIwbbriB9evXc9ZZZ9G/f39WrlzJqFGjAFi5ciXdu3dn9erVJev46quvOP3003G73bz00ktkZmayaNEijj/+eAAGDRrEhRdeyMyZM5k1a1aZWp955hmio6OZP38+ERERALRv356//OUvZZY977zzuPfeewEYOHAg33zzTUm46tixY0l/NHQl0njpjIxIPXTGGWeUvElD8fBRSEhIqbMlR+vQoUNJiKlMfHx8SYgBaN26NQDZ2dkADB48mLVr11JUVMTu3bvZu3cvt956K6mpqezYsYO8vDzWrl3LmWeeCRQHnRNPPJHmzZvj9Xrxer2YpsmgQYMqrPXbb7/ljDPOKAkxAMnJySVB6Gh9+/Yt9ffWrVuTlZV1zP0UkcZDZ2RE6qGmTZuW+rtpmjRp0qTCN/E/Ll+RyMjIUn83DAMoPlMDxUHmoYce4rvvvmPXrl20bduWs846i6ioKFavXk1iYiI+n49BgwYBkJmZyc6dOysc1snPzy8zLT09ncTExDLTk5KSykw7OuxAcR/03BgROZqCjEg99MfA4vP5yMjIIDExkQMHDtTadlu3bk379u1ZuXIlu3fvpn///rhcLvr27cvq1auJiori5JNPJi4uDoCYmBj69+/PpEmTyl1faGhomWktWrQgLS2tzPS0tDTatWsX2B0SkQZPQ0si9dCKFStKPQPmP//5D16vlwEDBlTp9S6Xy+9tDx48mBUrVrBmzZqS7aWkpLBmzRq+/vrrkmElgP79+7N9+3batWtHz549S/78+9//5s033yy3jn79+vHVV19RWFhYMm3Tpk0l1/VUR1WG00SkYdNvAZF66NChQ4wfP54VK1awcOFC7r//fk499VQGDhxYpdfHxMQAxdew/PDDD9Xa9hlnnMGGDRtITU2lf//+AAwYMID9+/ezd+/eUkFm5MiRWJbFyJEj+fDDD1m5ciVTpkzh5Zdfpn379uWu/9ZbbyU7O5tRo0axbNky3n33XcaNG4dhGCVDXVUVGxvL9u3bWblyJYcPH67Wa0WkYVCQEamHrrzySpo2bcq4ceOYOXMmF198MbNnz67yG310dDQ33HADS5cuZdSoURQVFVV52yeffDIxMTG0a9eOZs2aAXDiiScSFxdH27ZtSw3/NG/enNdff53jjz+eqVOncuutt7JhwwYefvjhklus/6hNmzY8//zzFBYWctttt/Hkk09y8803k5SURFRUVJXrBLj22msJCQnh5ptvLnkejog0LoatK+dEpA6tXLmSkJCQUnckHT58mFNPPZVJkyZx/fXXB7E6EXEaXewrInXq559/ZtasWUyYMIHu3buTkZHBCy+8QExMDBdddFGwyxMRh1GQEZE6deONN1JUVMSiRYvYt28fkZGR9O/fn8cff5yEhIRglyciDqOhJREREXEsXewrIiIijqUgIyIiIo6lICMiIiKOpSAjIiIijqUgIyIiIo6lICMiIiKOpSAjIiIijqUgIyIiIo6lICMiIiKO9f8BPydw8/ZkWwoAAAAASUVORK5CYII=)

---

**[Input:]**

```python

```

---

