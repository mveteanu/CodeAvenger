Ask about recursion during coding interviews to identify good talent
====================================================================

Let's start by stating the obvious: good talent is a very relative concept. 

What is good for some projects may be totally insufficient for other projects. A developer may perform admirably as application developer but not that great as framework or system developer.  In the same time, some projects may benefit more from resources with solid business knowledge about a particular field while other projects may require developers with good coding or algorithmic skills.

It's up to you to decide what skills will be more useful to your project.

Let's say you are looking for a good developer that you want to write code on a core component of your application. 

> You should not care too much if he knows a certain framework or not but instead see if he has good programming background. One of the questions that you can ask him to validate this is a question about recursion.

We had recently the need to select a few good JavaScript developers. Since the candidates were located remotely, I conducted the interviews via webex. The candidates were sharing the camera and the screen so I can see them typing.

> This is one of the questions I've asked the candidates: Find the maximum number in a jagged array. Each element of the array can be a number or an array of other numbers on indefinite number of levels, like this:

```JavaScript
var ar = [2, 4, 10, [12, 4, [100, 99], 4], [3, 2, 99], 0];
```

Since this was a JavaScript interview, the candidates used Notepad to type the code and Chrome to test it.

To my surprise a lot of candidates that looked good otherwise, had problems creating a function that finds the maximum value in a jagged array!!!

Even if they thought about using recursion they had hard time putting it in practice. They've spent almost an hour trying to create the recursive function without success.

Some may say: how is this test relevant? You may miss some talent if you are asking this kind of questions.

And this gets back to the first statement that I made at the beginning of the article. However, for most programming jobs I consider knowing recursion a basic skill. Do you agree with me? Nowadays, more than ever, you have the need to process hierarchical structures such as XML documents, JSON objects or hierarchies of controls.

While I'm not surprised anymore to see good developers not knowing recursion, in a past interview I had a nice surprise from a candidate. When faced with the problem he asked me back: do you want to do this with recursion or without? Now that's a candidate that you want to hire.

And now, just for fun and to keep the article short, I will include two solutions to the question I mentioned about. The first solution uses recursion while the second solution uses a stack. As a matter of fact all these problems with recursion can be also solved by using the stack approach.

Solution I: Find maximum using recursion
----------------------------------------

```JavaScript
// Use recursion to find the maximum numeric value in an array of arrays
function findMax1(ar)
{
    var max = -Infinity;

    // Cycle through all the elements of the array
    for(var i = 0; i < ar.length; i++)
    {
        var el = ar[i];

        // If an element is of type array then invoke the same function
        // to find out the maximum element of that subarray
        if ( Array.isArray(el) )
        {
            el = findMax1( el );
        }

        if ( el > max )
        {
            max = el;
        }
    }

    return max;
}
```

Solution II: Find maximum using a stack
---------------------------------------

```JavaScript
// Use a stack to find the maximum numeric value in an array of arrays
function findMax2(arElements)
{
    var max = -Infinity;

    // This is the stack on which will put the first array and then 
    // all the other sub-arrays that we find as we traverse an array     
    var arrays = [];

    arrays.push(arElements);

    // Loop as long as are arrays added to the stack for processing
    while(arrays.length > 0)
    {
        // Extract an array from the stack
        ar = arrays.pop();
        
        // ... and loop through its elements
        for(var i = 0; i < ar.length; i++)
        {
            var el = ar[i];

            // If an element is of type array, we'll add it to stack
            // to be processed later
            if ( Array.isArray(el) )
            {
                arrays.push(el);
                continue;
            }
            
            if ( el > max )
            {
                max = el;
            }
        }
    }

    return max;
}
```

Feel free to optimize the above code. You can also find this code as a [gist on github](https://gist.github.com/mveteanu/1f1d49bc6b764bfb1b1000a92bd3b48a).
