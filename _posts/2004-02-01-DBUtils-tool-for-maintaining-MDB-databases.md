DBUtils - tool for maintaining codebases and MDB databases
==========================================================

While working on [PowerTests.NET](http://www.powertests.net), I realized that the tools available in Visual Studio and Microsoft Access are sometime insuficient for certain refactoring tasks.
In particular, I found extremely difficult to answer to these questions:

- what are the dependencies of a particular script (e.g. what other scripts is using, what DB tables, etc.)
- what depends on a particular script or table (e.g. what other scripts are using the current script or table) 

To answer these questions and ease the refactoring work, I decided to build DBUtils: 

![](/img/posts/vmasoft/dbutils.png)

For more details about this tool, please check the VMASOFT product [page](http://www.vmasoft.net/dbutils.html).
