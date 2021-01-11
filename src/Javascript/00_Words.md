## Just-in-time compilation

In computing, <b>just-in-time (JIT) compilation</b> (also <b>dynamic translation</b> or <b>run-time compilations</b>) is a way of executing computer code that involves compilation during execution of a program – at run time – rather than before execution. Most often, this consists of source code or more commonly bytecode translation to machine code, which is then executed directly. A system implementing a JIT compiler typically continuously analyses the code being executed and identifies parts of the code where the speedup gained from compilation or recompilation would outweigh the overhead of compiling that code.

JIT compilation is a combination of the two traditional approaches to translation to machine code – <b>ahead-of-time compilation (AOT)</b>, and <b>interpretation</b> – and combines some advantages and drawbacks of both. Roughly, JIT compilation combines the speed of compiled code with the flexibility of interpretation, with the overhead of an interpreter and the additional overhead of compiling and linking (not just interpreting). JIT compilation is a form of dynamic compilation, and allows adaptive optimization such as dynamic recompilation and microarchitecture-specific speedups Interpretation and JIT compilation are particularly suited for dynamic programming languages, as the runtime system can handle late-bound data types and enforce security guarantees.

## Ahead-of-time compilation

In computer science, <b>ahead-of-time compilation (AOT compilation)</b> is the act of compiling a higher-level programming language such as C or C++, or an intermediate representation such as Java bytecode or .NET Framework Common Intermediate Language (CIL) code, into a native (system-dependent) machine code so that the resulting binary file can execute natively.

AOT produces machine optimized code, just like a standard native compiler. The difference is that AOT transforms the bytecode of an extant virtual machine (VM) into machine code.

## Interpreter (computing)

In computer science, an <b>interpreter</b> is a computer program that directly executes instructions written in a programming or scripting language, without requiring them previously to have been compiled into a machine language program. An interpreter generally uses one of the following strategies for program execution:

- Parse the source code and perform its behavior directly;
- Translate source code into some efficient intermediate representation and immediately execute this;
- Explicitly execute stored precompiled code[1] made by a compiler which is part of the interpreter system.

## First-class Function

A programming language is said to have <b>First-class functions</b> when functions in that language are treated like any other variable.

For example, in such a language, a function can be passed as an argument to other functions, can be returned by another function and can be assigned as a value to a variable.

### Ex1: Assign a function to a variable

```js
const foo = function () {
  console.log("foobar");
};
// Invoke it using the variable
foo();
```

We assigned an <b>Anonymous Function</b> in a Variable, then we used that variable to invoke the function by adding parentheses `()` at the end.

<b>Even if your function was named</b>, you can use the variable name to invoke it. Naming it will be helpful when debugging your code. <em>But it won't affect the way we invoke it</em>.

### Ex2: Pass a function as an Argument

```js
function sayHello() {
  return "Hello, ";
}
function greeting(helloMessage, name) {
  console.log(helloMessage() + name);
}
// Pass `sayHello` as an argument to `greeting` function
greeting(sayHello, "JavaScript!");
```

We are passing our `sayHello()` function as an argument to the `greeting()` function, this explains how we are treating the function as a `value`.

The function that we pass as an argument to another function, is called a <b>Callback function</b>. `sayHello` is a Callback function

### Ex3: Return a function

```js
function sayHello() {
  return function () {
    console.log("Hello!");
  };
}

const myFunc = sayHello();
myFunc();

sayHello()();
```

We need to return a function from another function - We can return a function because we treated function in JavaScript as a `value`.

A function that returns a function is called a <b>Higher-Order Function</b>.

## Callback function

A callback function is a function passed into another function as an argument, which is then invoked inside the outer function to complete some kind of routine or action.

```js
function greeting(name) {
  alert("Hello " + name);
}

function processUserInput(callback) {
  var name = prompt("Please enter your name.");
  callback(name);
}

processUserInput(greeting);
```

## Prototype-based programming

Prototype-based programming is a style of object-oriented programming in which classes are not explicitly defined, but rather derived by adding properties and methods to an instance of another class or, less frequently, adding them to an empty object.

In simple words: this type of style allows the creation of an object without first defining its class.

## OOP

OOP (Object-Oriented Programming) is an approach in programming in which data is encapsulated within objects and the object itself is operated on, rather than its component parts.

JavaScript is heavily object-oriented. It follows a prototype-based model (as opposed to class-based).

## Class

In object-oriented programming, a class defines an object's characteristics. Class is a template definition of an object's properties and methods, the "blueprint" from which other more specific instances of the object are drawn.

## Object

Object refers to a data structure containing data and instructions for working with the data. Objects sometimes refer to real-world things, for example a car or map object in a racing game. JavaScript, Java, C++, Python, and Ruby are examples of object-oriented programming languages.
