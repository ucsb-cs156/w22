---
desc: First JavaScript programming assignment 
assigned: 2022-01-19 12:30
due: 2022-01-28 23:59
github_org: ucsb-cs156-w22
layout: lab
num: jspa00
ready: false
---

# NOT READY YET
# NOT READY YET
# NOT READY YET
# NOT READY YET
# NOT READY YET

# Getting Started with JavaScript

To get started with JavaScript, we'll do a few exercises that are not connected with any web browser at all; just exploring JavaScript 
as a programming language.

While JavaScript was [originally developed to be a scripting language for web browsers](https://en.wikipedia.org/wiki/JavaScript#Creation_at_Netscape), with the [introduction of
Node in 2009](https://en.wikipedia.org/wiki/JavaScript#Reaching_maturity), JavaScript began to be used outside of web browsers.

So, we'll use `node` as our tool to interact with JavaScript.

## Step 1: Getting Started with Node

In this section, there are some exercises that I encourage you to work through.

There is nothing for you to turn in.  But if you skip over them, you may find that you are stuck on 
some of the later steps.  These are each here to help you understand something you need later in the
assignment.

I encourage you to read through this section, try the examples for yourself on CSIL or you own machine,
and experiment with the code.

## Step 1.1: Finding the node REPL

On CSIL, you can type `node` to enter a REPL (Read/Eval/Print Loop) for JavaScript.  If you have node installed on your local machine, this will 
likely work there as well:

```
[pconrad@csilvm-03 ~]$ node
Welcome to Node.js v17.4.0.
Type ".help" for more information.
> 2 + 3
5
> "ucsb".toUpperCase()
'UCSB'
> const schools=["UCSB","UCSD","Stanford"]
undefined
> schools.length
3
> schools[0]
'UCSB'
> schools[2]
'Stanford'
> schools[3]
undefined
> 
[pconrad@csilvm-03 ~]$ 
```

To exit the node REPL, use Control-D.

## Step 1.2: Hello World in JavaScript.

The "Hello World" program in JavaScript would look like this.  Put this in a file called `hello.mjs`:

```js
console.log("Hello, World!");
```

The `m` in `mjs` stands for Module.  It allows us to use the `import` statement, and avoids errors such as following that we may get if we try
to use `import` in a file that ends in plain old `.js`:

```
SyntaxError: Cannot use import statement outside a module
```

You'll see later on that we don't need the `.mjs` extension when working with front-end code in our web-apps; this appears to just be a 
standalone node thing.  But we'll keep it for now.


To run it, you can type: `node hello.mjs`:

```
[pconrad@csilvm-03 ~]$ cat hello.mjs 
console.log("Hello, World!");

[pconrad@csilvm-03 ~]$ node hello.mjs
Hello, World!
[pconrad@csilvm-03 ~]$ 
```

## Step 1.3: Getting command line arguments

As you may know:
* In C/C++, we can access command line arguments through the variables `argc` and `argv`  as in:
  ```cpp
  int main(int argc, char *argv[]) { 
  ```
  In this case, `argv[0]` is the name of the file being run, and the arguments start with `argv[1]`.
  The value `argc` tells us how the length of the `argv` array, which is always at least 1.
  
* In Python, we can access command line arguments through `sys.argv` as in:
  ```python
  import sys
  print(sys.argv[0], sys.argv[1], sys.argv[2])
  ```
  In this case, sys.argv[0] is the name of the file that is being run, similar to how C/C++ `argc`/`argv` works.   We use
  `len(sys.argv)` to determine the size of the `sys.argv` list.
* In Java, we can access command line arguments through the variable `args` as in:
  ```java
  public static voic main (String [] args) {
  ```
  In this case, `args` are all the actual command line args; there is no special meaning for `args[0]` as in C/C++ and Python
  
  
What about JavaScript under node.js?  In this case, we access command line arguments thorugh the `process.args`.

Executing this one line program will show us how this works:

```js
console.log("process.argv=",process.argv)
```

Let's try passing in three command line arguments:

```
[pconrad@csilvm-03 try-node]$ node args.mjs foo bar fum
process.argv= [
  '/usr/bin/node',
  '/cs/faculty/pconrad/try-node/args.mjs',
  'foo',
  'bar',
  'fum'
]
```

As you can see: 
* We can print out an entire array with `console.log`; the array starts with `[`, ends with `]` and each value is separated by a comma.
* `process.args[0]` is the full path to the node interpreter (`/usr/bin/node`)
* `process.args[1]` is the full path the script that we are executing (`/cs/faculty/pconrad/try-node/args.mjs`)
* The actually command line arguments start with `process.args[2]` which is `foo`.


## Step 1.4: Classic for loops in JavaScript

The classic for loop in C/C++ and Java both is:

```
  for (int i=0; i<n, i++) {
     // do something with i
  }
```

Let's use a JavaScript for loop to print all of the command line arguments.  Note that in place of `int` we have `var`.

Let's put this into `loop.mjs` and try running it with and without command line arguments:

```js
for (var i=0; i<process.argv.length; i++) {
  console.log("process.argv[" + i + "]=", process.argv[i]);
}
```

Here's what it looks like when we run it:

```
[pconrad@csilvm-03 try-node]$ node loop.mjs foo bar fum
process.argv[0]= /usr/bin/node
process.argv[1]= /cs/faculty/pconrad/try-node/loop.mjs
process.argv[2]= foo
process.argv[3]= bar
process.argv[4]= fum
[pconrad@csilvm-03 try-node]$ 
```

## Step 1.5: JavaScript string interpolation

Let's focus on this line for a moment:

```
  console.log("process.argv[" + i + "]=", process.argv[i]);
```

There's an easier way to write this using a feature called string interpolation.  In any string that is delimited with backticks instead of
double quotes, we can insert values by putting a dollar-size followed by an expression in braces, like this:

```
  console.log(`process.argv[${i}]=${process.argv[i]}`);
```

Same result, but much easier to read the code.

Try modifying your `loop.mjs` code in this way and run it again.

## Step 1.6: A JavaScript tutorial

Please read though this JavaScript tutorial:

* <https://developer.mozilla.org/en-US/docs/Web/JavaScript/A_re-introduction_to_JavaScript>

As you read, here are a few things that you should be looking for.  These are questions that you need to be able to answer (a) in order to be able to work effectively on the JavaScript parts of the legacy code applications in this course (b) to be able to answer questions about JavaScript that might come up in job interviews, (c) for homework/exam questions later in the course.

1.  Does JavaScript have different types for integer and floating point numbers?  Explain your answer.
2.  How do you convert a number in a string form (e.g. "123") to a numeric form?
3.   How do you find the length of a string in JavaScript?
4.  What does it mean to say that a value is "truthy" or "falsy" in JavaScript?
5.  When declaring a variable in JavaScript you can use `let`, `const` or `var`.  What is the meaning of each of these?
6.  A line of code that you'll sometime see in JavaScript takes this form:  `x = y + '';` i.e. adding an empty string.  What is the purpose of adding the empty string?
7.  What are two ways to create an empty object in JavaScript?
8.  Object properties in JavaScript can be accessed with both dot notation and bracket notation.  
    - Give an example of a JavaScript statement that initializes the variable `student` to refer to an object representing a student with a name of "Chris Gaucho" (as a string) and a perm number of 1234567 (as a number)
    - Show how to print the name field using `console.log` accessing the name field using dot notation 
    - Show how to print the perm number field using `console.log` accessing the  field using bracket notation 
9.  Write the JavaScript function equivalent of the following Java method.  (Note that you will not be able to
    restrict the type of parameters in plain JavaScript; that is possible in TypeScript, but let's not go there
    yet.  Just a plain JavaScript function that takes two numbers and returns their product is fine.)
    ```java
    public static double product(double a, double b) {
      return a * b;
    }
    ```
10. Consider the `product` function in the previous question.   
    - In Java, if you call it with no parameters (`double x=product();`) that's a syntax error.  What happens in JavaScript?
    - In Java, if you call it with three parameters (`double x = product(2,3,4);`) that's a syntax error.  What happens in JavaScript?

11. Using the *rest parameter syntax* (`...`) write a JavaScript function `productAll` that can take any number of parameters, and produces the product of all of its parameters (returning the multiplicative identity 1 if there are zero parameters).

    For example:
    * `productAll()` would return 1
    * `productAll(3)` would return 3
    * `productAll(3,2)` would return 6
    * `productAll(3,2,5)` would return 30
    * `productAll(3,2,5,7,10)` would return 2100
    * etc...
   
   
