Manually code your technical documentation
==========================================

Manually code technical documentation means editing and maintain manuals, guides and articles using a markup description language such as: HTML, MD, TEX, etc. Is this an old school approach or is it still used today? What’s your opinion?

Each and every software product needs to have good documentation. Let’s say that your product is an API library intended for developers. When you publish the library you have to provide also the following documentation:

- Reference documentation: API listing
- Static documentation: guides, tutorials, articles, etc.

Reference documentation
-----------------------

Reference documentation should be generated automatically from code as part of the regular build cycle. We’ll cover more about this in a future article.


Static documentation
--------------------

Static documentation creation has usually a different lifecycle than the regular code activities. For creation of static documentation, modern technical writers are usually reaching to solutions such as:

- Use word processors (e.g. Microsoft Word)
- Use specialized manual creation tools and output the documentation in various formats in the same time: PDF, HTML, etc. (e.g. Help & Manual, RoboHelp, etc.)
- Use a live wiki / blog

With this abundance of visual tools for maintaining technical documentation, how many of you are still manually coding the documentation?

> If you believe that hand coding technical documentation is a thing of past ... then think again and look no further than Microsoft. 
> The technical documentation of Azure cloud is hosted on GitHub as Markdown .MD files in this repository: 
> [https://github.com/Microsoft/azure-docs](https://github.com/Microsoft/azure-docs)

> The Azure documentation is fully open source on GitHub. Anybody can contribute to it.
> Processed .MD files are then presented for end-users on [https://docs.microsoft.com/azure](https://docs.microsoft.com/azure) website.

Microsoft is only one example. A lot of other companies and projects understand the flexibility of maintaining the documentation is a text based format. Are you one of these companies?

P.S. This article is created as an MD file and hosted using GitHub pages at this [location](http://github.com/mveteanu/CodeAvenger/blob/master/_posts/2017-01-11-Manually-code-your-technical-documentation.md). In fact, the whole [CodeAvenger](http://www.codeavenger.com) blog is maintained as a series of MD files on GitHub.
