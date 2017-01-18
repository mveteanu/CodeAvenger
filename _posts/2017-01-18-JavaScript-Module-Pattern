JavaScript Module Pattern
=========================

One of the challenges JavaScript beginners are trying to solve is finding a way to encapsulate all the attributes and behaviors related to a certain entity. Encapsulating all the data in a single entity, and then exposing only the public data, is one of the most basic concepts in implementing efficient libraries of APIs.

The module pattern, implemented by using JavaScript closures, comes handy when you want to encapsulate data as well as control what data is private and what public.
Without further ado, let’s see an example:

Without further ado, let’s see an example:

```JavaScript
// Use closure to protect private data
function CreateShapeObject()
{
    var radius = 50;

    function incRadius(n)
    {
        radius += n;
    }

    function decRadius(n)
    {
        radius -= n;
    }

    function drawShape(x, y)
    {
        ellipse( x, y, radius * 2, radius * 2 );
    }

    // Public API (module pattern)
    return {
        inc : incRadius,
        dec : decRadius,
        draw : drawShape,
    }
}
```

The public API, exported from the function is available to consumers like this:

```JavaScript
shape.draw( width / 2, height / 2);    
...
shape.inc(10);
...
shape.dec(10);
```

You can find the whole example, together with other ways of achieving encapsulation in JavaScript in the following GitHub Gist:

[Encapsulation in JavaScript](https://gist.github.com/mveteanu/d40f344802f18be67caccdf22ee98b82)

