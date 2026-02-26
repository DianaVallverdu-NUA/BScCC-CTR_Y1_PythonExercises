# Python Exercises

This repository contains a series of exercises that will help understand the basics of python especially when working in the context of data analysis and ML. This document serves as a guide to navigate the repository that can be used alongside the exercises to better complete them. This repository is thought for students with a knowledge of JavaScript who are moving on to data analysis / ML with Python.

## General Python rules

Some general Python rules that vary from JavaScript are:

- Python uses `snake_case` as opposed to JavaScript's `cammelCase`
- Python **does not** use semicolonds at the end of a line -> in fact a semicolon will break the script
- Comments in Python start with the hash key (`#`) instead of the double forward slash we saw in JavaScript (`//`)
- There is no `const` variable in Python. This means that all variables can potentially be modified. To try to avoid unwanted errors, you will usuall type the names of constants in all caps, e.g. `THIS_IS_A_CONSTANT`.
- Python uses indentation instead of curly brackets (`{ }`) to signify scope changes. We will see this in more detail at exercises in file **01** and **02**.

## Executing a Python script

To execute a python script:

- Open this repository in VSC
- At the top menu, select `Terminal` -> `New Terminal`
- To run a script, execute the command in the terminal:

```cmd
python3 name_of_script
```

For example, to execute `00_basics.py`, you would run from the terminal:

```cmd
python 00_basics.py
```

## 00_basics

In basics we learn how to print and assign different values to python variables.
Key similarities and differences with JavaScript are listed here:

| Action | JavaScript Command | Python Command |
| ---- | ----- | ----- |
| print / display | `console.log()` | `print()` |
| create a variable | `let x = <value>` | `x = <value>` |
| string value | `"string"` or `'string'` | `"string"` or `'string'` |
| number value | `<number>` | `<number>` |
| boolean value | `true` / `false` | `True` / `False` |
| concatenate strings and numbers | `"This is a number:" + 1` | `"This is a number:" + str(1)` |

## 01_variables_and_functions

In Variables and Functions we learn how to operate with variables and functions as well as how to define and execute functions.

Defining a function in python is very different from defining a function in JavaScript.
In JavaScript, you may be used to seeing functions like so:

```JS

function doSomething() {
    let something = "something";
}

```

The equivalent function in python would be the following one:

```Python
def do_something():
    something = "something"
```

As you can see, the key differences are:

- A function is defined with the keyword `def`instead of `function`.
- A colon is added at the end of the function name.
- Instead of the curly bracket system, Python uses indentation to mark different scopes. This means that the following code would be wrong, and the `do_something`function would be detected as blank:

```Python
def do_something:
something = "something"
```

Whereas this function in JS would be acceptable:

```JS
function doSomething() {
let something = "something";
}
```

## 02_conditionals_and_loops

### Conditionals (Ex 1 - 3)

In Conditionals and Loops we learn the basics of these techniques.

An if / else statement in JS looks like this:

```JS
if(something_is_true) {
    console.log("true!");
} 
else {
    console.log("false!");
}
```

In Python, the same statement would be:

```Python

if something_is_true :
    print("true!")
else :
    print("false!")
```

As you can see, Python also uses a colon and indentation to differenciate the scope of the instructions.

Moreover, if statements in Python loose the brackets typically surrounding the condition.

### Loops (Ex 4 - 5)

As expected, loops also use colons and indentation to separate scopes. This is how a while loop compares in each coding language:

JS:

```JS
let i = 0;
while(i < 100) {
    console.log(i);
    i++; // alternatively, i += 1 or i = i + 1;
}
```

Python:

```Python
i = 0
while i in range(100) :
    print(i)
    i += 1 # alternatively, i = i + 1
```

This is how a for loop compares:

JS:

```JS
let i = 0;
for(let i = 0; i < 100; i++) {
    console.log(i);
}
```

Python:

```Python
for i in range(100) {
    print(i)
}
```

## 03_arrays

In the Arrays exercises you will learn how to implement arrays, add and remove elements from arrays, as well as concatenate arrays. You will also learn how to loop through arrays.

Here's a list of key differences and similarities between JS and Python arrays.

| Action | JavaScript Command | Python Command |
| ---- | ----- | ----- |
| create array | `let array = [1, 2, 3]` | `array = [1, 2, 3]` |
| length of array | `array.length` | `len(array)` |
| add element at end | `array.push(<elem>)` | `array.append(<elem>)` |
| remove last element of array | `array.pop()` | `array.pop()` |
| remove first (position 0) element of array | `array.shift()` | `array.pop(0)` |
| remove element at position n of the array | `array.splice(n,1)` | `array.pop(n)` |
| concatenate two arrays | `newArray = arrayOne.concat(arrayTwo)` | `new_array = array_one + array_two` |
| simple loop through array | `for(let elem of array) {...}` | `for elem in array :` |

## 04_matrixes

Matrixes are arrays of dimension 2, meaning that you may have rows and columns. You may have inadvertendly used matrixes in the past in JavaScript, for example when analysing the colours of an image.

To create a Matrix in Python, you'd create it similarly to what you'd do in JS:

```Python
matrix = [
    [<value>, <value>, <value>],
    [<value>, <value>, <value>],
    [<value>, <value>, <value>]
]
```

You can then access a value of the matrix just like you'd access a value in an array. For example, at position 0, 0, you'd have:

```Python
value = matrix[0][0]
```

At the end of the matrixes, you have some challenge exercises to practice some concepts that will be relevant to Machine Learning. You are encouraged to attempt them at your own pace!

### Transposition