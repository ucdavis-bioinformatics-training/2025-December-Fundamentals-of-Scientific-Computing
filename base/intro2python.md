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
We are going to use a python distribution platform, Anaconda. Anaconda is an open source distribution platform for python and R. It was designed to meet the demand of Data Sciences and AI projects. It can be installed on all three operating systems and has 45 million users as of 2024. It includes over 300 packages, offers jupyter Notebooks and jupyter Lab and includes _conda_, the package and environment manager. It makes installing a lot of python packages very easy. Please follow the instructions below to install Anaconda. Instructions for all platforms can be found at <https://www.anaconda.com/docs/getting-started/anaconda/install>
- Macs: Two options are available. One is to use the graphic installer. The other is to use the Command Line installer.
  - For graphic installer, please go to https://www.anaconda.com/download and follow the instructions in the "Download Now" panel. This option installs Anaconda in /opt/anacondas in the file system. In order to install Anaconda into your Home directory (especially in the case where there are multiple users), Command Line installation is recommended.
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
- Windows: Please install in your ubuntu subsystem so that conda is available for installing other python packages
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
<tr><td>Sequence</td><td>list[], tuple()/(), range()</td></tr>
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
Creat different data types and perform some operations.

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
Cell In[27], line 1
----> 1 range_example[0] = 3

TypeError: 'range' object does not support item assignment
```

---

**[Input:]**

```python
range_example
```

---

**[Input:]**

```python
len(range_example)
```

---

**[Input:]**

```python
range_example[5]
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
Cell In[28], line 1
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

We see a new syntax, __variable.function()__. This is the way to call a method that is bound to an object in python. In order to know what methods are bound to an object, we can use the following operation:
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
gene_name:  test
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
{'gene_name': 'test',
 'gene_biotype': 'protein_coding',
 'n_transcripts': 32,
 'n_orthologues': 217,
 'n_paralogues': 4,
 'ensembl_id': 'ENSG00000131730',
 'discription': 'creatine kinase, mitochondrial 2',
 'loc': 'Chromosome 5: 81,233,320-81,266,399',
 'strand': '+',
 'pathway': 'Mitochondria disease pathway',
 'pathway2': 'Mitochondria disease pathway',
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

__New_list = [expression for item in iterable if condition == True]__

**[Input:]**

```python

```

---

