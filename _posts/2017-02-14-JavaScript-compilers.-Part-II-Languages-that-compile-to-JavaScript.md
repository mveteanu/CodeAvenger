JavaScript compilers. Part II: Languages that compile to JavaScript
===================================================================

In Part I of this JavaScript compilers series, we saw how some popular transpilers are compiling JavaScript dialects to the current dialect of JavaScript.

In this part we’ll mention a few other non-JavaScript languages that compile to JavaScript for in browser execution.

You may ask: why use a non-JavaScript language for developing front-end web applications? There are two reasons:

Reason 1: Better languages
--------------------------

Some researchers believe that they can introduce new and more productive languages for web development. This is the case of Dart [https://www.dartlang.org/](https://www.dartlang.org/) and Elm [http://elm-lang.org/](http://elm-lang.org/)

Dart was invented by Google and is currently used to develop internal Google applications such as AdWords. 
The language is easy to learn and use but as with any new other new language you have a very small user base. This is what determined Google to go with TypeScript (a javascript superset) for Angular rather than Dart. Google wanted to make Angular available to the wide range of JavaScript developers.


Reason 2: Nostalgic users or leveraging existing investments
------------------------------------------------------------

Some people are still very fond of classical programming languages such as BASIC, Pascal or even Python and Ruby.
Other people may have big investments in code bases written in other languages that they want now to run either in the browser on the client-side or on the server on Node.JS. 
Let’s start with BASIC. We have here two interesting options NSBasic [https://www.nsbasic.com/](https://www.nsbasic.com/) (pictured below) and Spider Basic [http://www.spiderbasic.com/](http://www.spiderbasic.com/)

![NSBasic](/img/posts/js_nsbasic.png)

Pascal users can choose between [http://smartmobilestudio.com/](http://smartmobilestudio.com/) (pictured below) and Elevate Web Builder [http://www.elevatesoft.com/products?category=ewb](http://www.elevatesoft.com/products?category=ewb)
 
![SmartMobileStudio](/img/posts/js_smartmobilestudio.png)

Python and Ruby have their own compilers that target JavaScript. There are many, many options available here. I will just mention [http://www.skulpt.org](http://www.skulpt.org) for a Python to JavaScript compiler and [http://opalrb.org/](http://opalrb.org/)  for a Ruby to JavaScript compiler.

.NET developers have their own share of compilers that compile to JavaScript. Some compilers compile directly languages such as C# to JavaScript, while other takes regular .NET bytecodes (MSIL) and compile that to JavaScript. I’m still researching this area. Maybe this will be the topic of a future article.

A special mention goes to Haxe [http://haxe.org/](http://haxe.org/)  which is a cross-platform programming language that compiles to different targets including JavaScript. Haxe is very well regarded by game developers.

In conclusion I want to mention that I just scratched the surface. There are literally hundreds of compilers that target the JavaScript platform. 

If you used a common language in the past there is the chance there is a compiler to JavaScript for that language.

And even if you have a proprietary language in your application there is the possibility to create a compiler for that language and make your entire code base run on JavaScript.

Please don’t forget to check the other parts of this JavaScript compilers series:

- [Part I: Better JavaScript dialects](http://www.codeavenger.com/2017/02/14/JavaScript-compilers.-Part-III-JavaScript-the-new-bytecode.html)
- [Part II: Languages that compile to JavaScript](http://www.codeavenger.com/2017/02/14/JavaScript-compilers.-Part-II-Languages-that-compile-to-JavaScript.html)
- [Part III: JavaScript - the new bytecode](2017-02-14-JavaScript-compilers.-Part-III-JavaScript-the-new-bytecode.md)

VMA
