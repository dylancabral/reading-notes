# In Memory storage

## What is a ‘call’?
function invocation

## How many ‘calls’ can happen at once?
one, the are acted upon like a list which can be sycnronous or asychronus

## What does LIFO mean?
last in first out


## Draw an example of a call stack and the functions that would need to be invoked to generate that call stack.
![Callstack example](call.png)

## What causes a Stack Overflow?
A stack overflow occurs when there is a recursive function (a function that calls itself) without an exit point. The browser (hosting environment) has a maximum stack call that it can accomodate before throwing a stack error


---

## What is a ‘reference error’?
This is as simple as when you try to use a variable that is not yet declared

## What is a ‘syntax error’?
this occurs when you have something that cannot be parsed in terms of syntax, like when you try to parse an invalid object using JSON.parse.


## What is a ‘range error’?
when you try to manipulate something out side of its paramaters like the 10 index of an array of 5

## What is a ‘type error’?
these type of errors show up when the type (number, string and so on) you are trying to use or access are incompatible, like accessing a property in an undefined type of variable.

## What is a breakpoint?
a stopping point for a section of code


## What does the word ‘debugger’ do in your code?
adds a breakpoint into your code


[JS Callstack](https://www.freecodecamp.org/news/understanding-the-javascript-call-stack-861e41ae61d4)

[JS Error Messages](https://codeburst.io/javascript-error-messages-debugging-d23f84f0ae7c?gi=59631fb27be5)
