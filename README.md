
#Intro to Python
You have learned three languages so far - HTML, CSS and JavaScript. Each one had it's own purpose: HTML for the content and structure of a page, CSS for the style of a page and JavaScript for some interactivity. All three of those languages are the building blocks of the front-end of an app, the parts that the user sees and manipulates. The next section of the prework goes to the other side of the action, the behind-the-scenes backend. If the front-end as the aesthetic of a car (what it looks and feels like), the back-end is the engine. In this unit, you will learn how to write Python programs and build the framework for a fully functional web app.

##Objectives:
+ Understand why back-end languages are necessary
+	Interact with Python (interpreter, text editor + run from command line)
+ Understand Basic Concepts in Python
+ Print a String
+ Math Operations
+ Variables in Python
+ Writing and Running a Script


## Python - Our Backend Language
All web-applications need to have a front-end. By definition, they need to get information from a user or other data source. Generally, (but not always) web-applications need to have a back-end to store that data, access other data and route everything appropriately. The back-end is like the Oz behind the curtain, it is the framework that allows an app to pass data around in response to the requests of the user.

There are many types of back-end languages including Ruby, Java (no relation to JavaScript) and Python. Python is a language that is ubiquitous at Google and for good reason: it has has a shallow learning curve, it's syntax makes it readable and  easy to reproduce, and it is extremely powerful.

Like JavaScript (and unlike HTML and CSS), Python is a scripting language - it is used to perform tasks. Those tasks might be data modeling and forecasting, binding together the pieces of a game engine, or, as you'll be using it, running a web app. When we run Python, we don't run it through the browser, we run it directly on our machines. Since you've already spent a significant amount of time learning JavaScript, you'll see that Python (and almost any other programming language) is very similar in terms of the fundamentals: variables, functions, conditionals, iterations, etc. The big differences are syntactic - that is, in the *way* things are written as opposted to what those things actually are. Pay attention to the differences in JavaScript and Python syntax as you jump in to this unit!

##Python Interpreter vs Python Script

Just like with JavaScript, we can run Python through two ways: the interpreter and a script.

**Python Interpreter** is started from the command line and is most useful when we want to test things out or quickly do a calculation. Just like the JavaScript console, the interpreter evaluates statements and immediately prints the return value back to us.

**Python Scripts** are text files saved with a .py extension and run from the command line. Scripts are full programs - we can save them, change them, share them, and reuse them. Scripts are used to write much more complex code than we could in the interpreter.

## The Python Interpreter
Open your terminal and type...
```
$ python
```
You'll see something like...
```
Python 2.5.1 (r251:54863, Jun 17 2009, 20:37:34)
[GCC 4.0.1 (Apple Inc. build 5465)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>>
```
The interpreter allows you to run individual lines of Python code one at a time. For now, all you need to know is that if you invoke the command `python`, it will open up the interactive mode (sometimes called a "REPL") and allow you to try things out quickly.

###Strings
Just like in JavaScript, any character or group of characters can be wrapped in single or double quotes to be interpreted as a string. Python has it's own string methods which you will learn about in an upcoming lesson.
```
>>> print 'hello world'
hello world
```
`print` is Python's equivalent of `console.log()` in JavaScript. It lets us print a string out. What happens if we just type the string?

```
>>> 'hello world'
'hello world'
>>>
```
The interpreter tries to be helpful and prints out the return value of every line that we enter. When we just enter a string, Python tells us that the line would evaluate to a string.

### Math Operations
Let's try some basic math. The basic math operations work the same as they do in JavaScript.
```
>>> 6 + 8
14
>>>
```
Python math can get pretty complicated, but arithmetic is pretty straightforward. Experiment with the order of operations in Python.
```
>>> 7 + 6 * 8
>>> 7 + (6 * 8)
>>> (7 + 6) * 8
```

### Operators and Boolean Values
Just like JavaScript, Python has the == operator for checking equality. It returns a boolean value, which is either True or False (note that Javascript returns lowercase true and false).

```
>>> 5==4
False
>>> 5 == "5"
False
>>> 'five' == 'five'
True
```
Most of our results are similar to what we learned about in JavaScript. Did you notice the second command though? In JavaScript `5=="5"` is true. JavaScript has *type coercion*, which means that when two different data types are compared in an operator, one will be forced to match the other's type. In general, Python is much less forgiving when it comes to data types, so it is a great language to hold ourselves accountable for well-written code.

### Variables
In Python we don't need to explicitly declare a variable with  'var'. The naming conventions are also different. In JavaScript, use camelCase. In Python, use all lowercase letters. Variable names can not have spaces but instead use underscores: this_style_is_called_snake_case.
```
> my_variable = 15
> my_variable + 10
25
```

Just like in JavaScript, we can change reassign variables at any time.
```
>>> minion = "Kevin"
>>> print minion
Kevin
```
What will happen when we run the following?
```
>>> name = "Kevin"
>>> name = "Carl"
>>> print name
```

On the first line, we assigned the variable name to store Kevin. On the next line, we reassigned the value of the variable name to store Carl. Each variable can only store one value. This is because at its core, a variable is an assigned space in memory which can only be occupied by one value. So when we print name on the last line, we will print the most recent value that was assigned to name: Carl.


### Exiting the Interpreter
Close the prompt with
```
>>> quit()
```
A few thing to note:
+ When you close the prompt, the session is not saved anywhere
+ The three carrots >>> are the python prompt.  
+ The interactive mode should be used for testing out Python code - if you want to be able to save your work, put it in a file!

##Creating and Running a Python Script

In order to save our Python programs, we will need to create a Python script. With JavaScript, our files ended with the extension `.js`. In Python, our files will end with the `.py` extension. Let's walk though how to execute a new Python script. First, open up the terminal and make a new directory for all of your Python prework: `mkdir python_practice`.

Then execute the following commands in the terminal to change into your new directory, create a new script, practice.py and to open that script in Atom - our editor.
```
> cd python_practice
> touch practice.py
> open -a Atom practice.py
```

Like obedient novice programmers, let's write the most basic Hello World file we can, to test that we can run a script.
```
print 'hello world!!!'
```
Save this in Atom.

To run scripts from the command line, we just need to call `python` and then the name of your script that we want to run, like this:

```
$ python practice.py
```

A few things to note here:
+ The .py extension tells us that it is a Python file
+ The script needs to be in the current working directory, otherwise it must be referenced using it's path
+ Python scripts are lines of code that are executed from top to bottom
