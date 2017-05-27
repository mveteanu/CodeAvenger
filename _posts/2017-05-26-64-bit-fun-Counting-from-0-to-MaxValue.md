64 bit fun. Counting from 0 to MaxValue
=======================================

64 bit computing was futuristic a few decades ago. With the exception of mainframes and other specialized computers, all personal computer of the recent past had data path widths (registers, etc.) of either 8 or 16 bits. Introduction of 32 bit was a big revolution in personal computing.

Nowadays virtually every CPU supports 64 bit operations. Even low powered mobile processors are now 64 bit. In a 64 bit architecture, the CPU can process / store more information using 64 bit registers as well as address more memory.

How big is 64 bit?
------------------

Since this is a fun article, I won’t go into the math of 64 bit arithmetic nor in the computer science of 64 bit architectures. Instead I will propose to do a small comparative test in assembly or any programming language that supports 64 bit data types:

Count from 0 to maximum value that can be stored in a variable. First time use a 32 bit wide variable and second time use a 64 bit wide variable. Try to estimate the results.

In C#, the code may look like this for 32 bit variable (... ignore please the off by one issue):

```csharp
for (uint i = 0; i < uint.MaxValue; i++)
{
    Process(i);
}
```

uint.MaxValue is the number that you obtain when you set all bits of the variable to 1. It is basically equal to 2^32 – 1 = 4294967295. This is about 4.2 billion.

The test code for the case with 64 bit variable is similar:

```csharp
for (ulong i = 0; i < ulong.MaxValue; i++)
{
    Process(i);
}
```

ulong.MaxValue is this time 2^64 – 1 = 18446744073709551615 (a 20 digit number).

At about 1 billion Process() operations / second, the first program will finish its job in: 
2^32 / 1000000000 = 4.29 seconds

At the same processing speed, the second program will finish its job in:
2^64 / 1000000000 / 3600 / 24 / 365 = 585 years! 

That's quite a difference!!! Who has the time to wait 585 years for a basic for to finish its job! 

And the funny part is that 1 billion operations per second is quite aggressive! For a more realistic scenario where you execute from 1 million to a couple hundred million operations per second, the time explodes to thousands even hundreds of thousands of years to do a single for!!!

For majority of people the above exercise is a fun visualization of 64 bit power. But this exercise also shows the reality faced by computer science engineers working with algorithms. A poorly implemented algorithm (e.g. search or computational problem), that takes a brute force approach, can very well ruin your software.

Other big numbers
-----------------

As a recap, remember that the maximum number stored in a 64 bit register / variable is 2^64 – 1 = 18446744073709551615 (a 20 digit number). As big at it seems this number is still small when compared for instance with 1 googol which is 10^100 (1 followed by 100 zeros) !

And even the big googol is smaller than 70! (70 factorial which is 1 * 2 * ... * 70). Wow! This really shows the power of multiplication!

And you know what: the googol is well within the range of the double data type (IEEE 754 floating point) – also a 64 bit structure. How double manages to store such big numbers will be presented in a future article.

I hope you had fun!

VMA
