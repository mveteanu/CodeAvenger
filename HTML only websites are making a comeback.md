HTML only websites are making a comeback
========================================

About 20 years ago I dipped my toes for the first time into HTML and web design. Back then, creating a fully functional site with navigation menus and content articles was a very tedious job. Although each article was unique and got its own page, there were lots of repetitions between pages – mostly caused by the navigation menu that had to appear on each and every page. Not to mention that changing the style of the website was a project on its own.

That was not only my experience… but everyone else’s. People quickly adopted server-side technologies to assist with dynamic page generation and eliminate the redundancy in HTML sites. Request / Response type technologies were the norm:

-	ASP
-	PHP
-	CGI (Perl scripts, etc.)
-	etc.

Soon after, CMS (Content Management System) industry started to explode. Currently there are countless of options, both paid and open-source for CMS systems. 
What was once just a pure HTML site, it is probably now a WordPress site with a full fledge DB and server technology behind.
Sounds perfect! Right?

And still the industry is making a comeback. Some of the benefits of pure HTML sites such as speed, low server resources and most importantly scalability cannot be obtained with the new modern CMS technologies.

There are entire categories of web sites with the only purpose of presenting some static information to end-users. These sites are updated very rarely … but accessed many – many times by users in between updates. Examples:

-	corporate websites
-	portfolio sites
-	blogs
-	help systems
-	etc.

For this kind of website is not worth the effort of maintaining an entire engine on the server with the only purpose of sending a “text” to the user. These sites can be created in HTML.
But… if we give up to server-side technologies, how do we solve the repetition problem that we had also 20 years ago?
Solution is to use a “static website generator”. There are tons of them!
They work by making use of templating and markdown technologies to heavy lift the task of repetition from the developer therefore eliminating human errors. Static site generators make complex sites such as blog easy to develop and maintain, developers focusing just on the template, leaving the tool the task of compilation and production of standard HTML files.
Perhaps the most common static site generator is Jekyll (http://jekyllrb.com/). I discovered Jekyll when I first opened my GitHub account. Jekyll is backed by GitHub. And since GitHub allows you to host static websites, a lot of people are using Jekyll to generate these sites.
But Jekyll is not the only one. Another popular option is Hugo (https://gohugo.io/)  - a very fast and standalone website generator written in Go.
Middleman (https://middlemanapp.com/) and Roots (http://roots.cx/) are other 2 popular options.

Static sites are huge again. Big corporations are using them to get the benefits. Healthcare.gov switched from a CMS system to a static site implemented with Jekyll.

So… question is: what are you doing for those very few situations when you need to persist some data? Well – the good news is that cloud computing has the answer. With advances in BaaS (Backend as a Service) and DBaaS (Database as a Service) you can basically skip altogether the server-side code in your application and relay on cloud services for that – more about this in a future article.
