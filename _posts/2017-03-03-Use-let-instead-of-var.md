Use let instead of var
======================

It is a common knowledge that JavaScript doesn’t have block scoping as other languages. In JavaScript, all variables declared in a function have local scope at the level of the function.
Although seems harmless, this small particularity can be the source of some very hard to catch errors (as we’ll see in the following example). 

```JavaScript
    var functions = [];

    for (var i = 0; i < 3; i++) 
    {
        functions[i] = function() { return i; };
    }

    console.log(functions[0]());	// 3
    console.log(functions[1]());	// 3
    console.log(functions[2]());	// 3
```

What do you think is the result of execution of the above code snippet? At first sight you would be tempted to say that is 0, 1 and 2. Wrong! Take a look in the console. You’ll see 3, 3 and 3.

Let’s see what can we do to the above code to make it produce 0, 1 and 2 in the console log.

Solution 1: Use let
-------------------

In future ECMAScript versions (ES6) the missing block scoping causing the problem above is corrected by introduction of an additional language keyword: let. It’s now up to developers to use let instead of var in their programs.
Check if your JavaScript environment (e.g. browser, etc.) supports ES6 already. If yes, then simply write the above code as:

```JavaScript
    var functions = [];

    for (let i = 0; i < 3; i++) 
    {
        functions[i] = function() { return i; };
    }

    console.log(functions[0]());    // 0
    console.log(functions[1]());    // 1
    console.log(functions[2]());    // 2
```

Solution 2: Use TypeScript
--------------------------

TypeScript transpiler allows you to use let identical as in the previous example and then transpile the code in a JavaScript form supported by older environments.
Compile the Solution 1 in TypeScript and see what’s the output!


Solution 3: Workaround
----------------------

If for various reasons you cannot use the above mentioned solutions, then you can work around the missing block scoping issue by using any of the following technique. 
I would stay away though from the 'with' pattern since this keyword is deprecated in JavaScript (although some [StackOverflow people](http://stackoverflow.com/questions/1293798/javascript-with-function) are considering it OK).

```JavaScript
    var functions = [];

    for (var i = 0; i < 3; i++) 
    {
        (function(i){
            functions[i] = function() { return i; };
        })(i);
    }

    console.log(functions[0]());    // 0
    console.log(functions[1]());    // 1
    console.log(functions[2]());    // 2
```

or

```JavaScript
    var functions = [];

    for (var i = 0; i < 5; i++) 
    {
        with ({ j: i }) 
        {
            functions[i] = function() { return j; };
        }
    }

    console.log(functions[0]());    // 0
    console.log(functions[1]());    // 1
    console.log(functions[2]());    // 2
```
