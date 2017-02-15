JavaScript compilers. Part I: Better JavaScript dialects
========================================================


JavaScript is great
-------------------

JavaScript is one of the most interesting and in the same time misunderstood programming language. By combining paradigms from different language families it give the user the flexibility to use the language according to his preference. In JavaScript you can do tasks deemed for imperative programming or functional programming or anything in between. In JavaScript you have the liberty to do object oriented programming or plan structured procedural programming.
With all this flexibility it seems unlikely that anyone may need anything else from the old JavaScript.


JavaScript has limitations
--------------------------

And still, in these times when it expected to convert every application imaginable to a web application, JavaScript start to show its weaknesses in being a productive language for creating and maintaining complex applications.
A few shortcomings of the JavaScript language make developing complex applications difficult: modularity, a proper class system and complicated async algorithms implementation.
While ECMAScript specification constantly evolves to address shortcomings such as the ones mentioned above… it usually takes years until all browsers get to implement the new versions of the language.


Transpilers
-----------

Introducing Transpilers. Transpilers are specialized forms of compilers that compile one source language in a different language that supports the same level of abstraction. A basic compiler converts one language to a different language which may not have the same level of abstraction. Transpiler word has been there forever but only recently has been popularized to general public.
The most popular transpilers currently available for JavaScript are:
TypeScript [http://www.typescriptlang.org](http://www.typescriptlang.org) . TypeScript was created by Microsoft as open-source and is used by many projects including Angular.
Babel [http://babeljs.io](http://babeljs.io) (originally named 6to5). Babel was created by an independent Australian developer and is used now by many projects including React.
Traceur. [https://github.com/google/traceur-compiler](https://github.com/google/traceur-compiler)

The main focus of the above mentioned transpilers is to allow developers program against a future specification of JavaScript language.
You can for instance develop against ECMAScript 6 and the transpiler will convert / compile the code to ECMAScript 5 code that all browsers can understand and run. It’s a win-win situation.


Easy async programming in JavaScript
------------------------------------

Another complaint of JavaScript is the messy nature of async programming. Just look at a complex Node.JS code and you’ll have difficulties following the logic due to the nature of imbricated callbacks required by async methods.
This problem was present in other languages as well. Microsoft solved it in C# by introducing async / await keywords. JavaScript promises that will introduce async / await as well.
However, I want to bring to your attention a few special JavaScript enriched dialects that solve the async problem now.

Take a look at the following code snippet:

```JavaScript
while(min != max) {
	var mid = min + Math.round((max-min)/2);

	var ret = form.ShowDialog( dlgCompareNumber, [mid] );
	if ( ret ) {
		max = mid-1;
	} else {
		min = mid;
	}
}
```

In some programming languages it is perfectly fine to call your dialogs in this way. Is a clear way to understand and write the logic.

Normally in HTML5 JavaScript you cannot have blocking calls such as make the code stop until a window is closed.

Actually – if you are using the open-source StratifiedJS you can do this on the web. You can find StratifiedJS at [http://onilabs.com/stratifiedjs](http://onilabs.com/stratifiedjs)

StratifiedJS compiler will basically compile code such as the one above to regular JavaScript code that any browser will run. Think of StratifiedJS as a superset of JavaScript language.

StratifiedJS is not the only JavaScript superset that tries to solve the async programming challenge. Other less-known languages are:

- StreamlineJS: [https://github.com/Sage/streamlinejs](https://github.com/Sage/streamlinejs)
- ContinuationJS: [https://github.com/BYVoid/continuation](https://github.com/BYVoid/continuation)


Please don't forget to check the other parts of this JavaScript compiler series.

VMA
