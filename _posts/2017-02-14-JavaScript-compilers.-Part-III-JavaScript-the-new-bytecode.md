JavaScript compilers. Part III: JavaScript - the new bytecode
=============================================================

If you read carefully the first two parts of this JavaScript compilers series, you’ll probably have a pretty good picture about what can be compiled to JavaScript and what not.

I want to force your imagination and tell you that even C and C++ can be compiled to JavaScript. In fact for this compiles JavaScript is the new bytecode. 

Years ago mainstream compilers used to target machine op-codes then they start to target VM bytecodes as defined by platforms such as Java or .NET. Nowadays targeting JavaScript opens a huge array of possibilities for exposing on the web classic / desktop like applications.

I want to bring to your attention the Emscripten project [http://kripken.github.io/emscripten-site/](http://kripken.github.io/emscripten-site/). This is an extract from their website:

>> Emscripten is an LLVM-based project that compiles C and C++ into highly-optimizable JavaScript in asm.js format. 
>> This lets you run C and C++ on the web at near-native speed, without plugins.

The Emscripten is a highly regarded compiler by people from all sort of industries. Most notable game industry can benefit of Emscripten to port their games to the web. In other words a classic C++ game can now run in a web page without any plugin. Just check this page for a huge list of games that you can now play in the browser: [https://github.com/kripken/emscripten/wiki/Porting-Examples-and-Demos](https://github.com/kripken/emscripten/wiki/Porting-Examples-and-Demos)

What can you port to web browser is up to your imagination now. 

I will mention though one small project that took advantage of the Emscripten technology: the DOSBOX [http://www.dosbox.com](http://www.dosbox.com) project. 
DOSBOX is an emulator of x86 machines indented to run old DOS programs on top of modern operating systems such as Windows 10 x64.

While DOSBOX is mostly used by people to play old games, it can be successfully used by enterprises to continue run those not yet ported DOS applications. 

Personally I just played with DOSBOX the other days when I use it to revive some of my old applications with the intent to capture a few screenshots and screencasts. I announced in a previous article that I open-source some of my 20+ years old software… therefore I needed a few screenshots. And I got plenty (as seen in Physics [http://www.vmasoft.net/physics.html](http://www.vmasoft.net/physics.html) and MCGA software [http://www.vmasoft.net/mcga.html](http://www.vmasoft.net/mcga.html) ).

Anyway... back to the subject. While I used the regular DOSBOX version in my initial experiment, I soon discovered that there is a DOSBOX version compiled with Emscripten [https://github.com/dreamlayers/em-dosbox](https://github.com/dreamlayers/em-dosbox). This version runs basically in a web page.
And since DOSBOX is basically an emulator, you can run other PC based software (for which you don’t own the source code) inside a web browser. There are plenty of examples of internet ranging from running DOS based games inside browser to running the full Windows 3.1 or even Windows 95 inside a Chrome browser.

And it works! It is true that Windows 95 takes a little bit longer to load and runs a little bit slower to be any good… but it works.

On the other hand Windows 3.1 or regular DOS applications load like a charm. The Internet Archive Web site has a collection of DOS games and Windows 3.1 DOSBOX installations available for testing.

Check out Windows 3.1 running inside my Chrome browser: [https://archive.org/details/win3_stock](https://archive.org/details/win3_stock)

![](/img/posts/js_win311.png) 

Before ending this article let me mention that there are also other ways of running binary legacy code inside a web browser besides using the Emscripten DOSBOX project.

A few years ago a talented engineer created a full PC emulator inside JavaScript (complete with CPU, memory and storage). He then used the emulator to run Linux inside web browser. You can still access his Linux and learn about the inner workings at [http://bellard.org/jslinux/](http://bellard.org/jslinux/) . A similar project is PCE from [http://www.hampa.ch/pce/](http://www.hampa.ch/pce/)

By the way – I focus this article section only on PC emulation. As a matter of fact there are JavaScript emulators for almost all game consoles and old computer systems.

So the question is: Is the browser the new platform of the future? Is JavaScript the bytecode of this platform?

Please don’t forget to check out the other articles in the JavaScript compilers series.

VMA
