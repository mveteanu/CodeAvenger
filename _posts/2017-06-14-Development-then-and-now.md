#Development: Then and Now

##Client: I need to develop an application.

##Developer

###1997

Sure. I can create for you a modern Windows application. I just need to install Visual Basic or Delphi from the CD and I will be up and running in 1 hour. I will deliver the application next month together with a step by step installation kit.

###2017

Sure. I can create for you a modern Web application. Today is easier than ever. Today we have granularity and choice ... not like 20 years ago. I just need to glue together a few prebuild frameworks and technologies.

 The client-side is easy. [HTML5](https://www.w3schools.com/html/html5_intro.asp) and [CSS3](https://www.w3schools.com/css/css3_intro.asp) together with [JavaScript](https://www.ecma-international.org/publications/standards/Ecma-262.htm) are great for building interactive Web applications. 

 Although I don't quite like the JavaScript implementation in the current browsers so I will probably use a [transpiler](https://en.wikipedia.org/wiki/Source-to-source_compiler). I can go with [Typescript](https://www.typescriptlang.org), [Babel](https://babeljs.io) or even [Traceur](https://github.com/google/traceur-compiler). 

 Good! I just improved the language. Now let me take the initiative to improve the CSS3 as well. I heard that [LESS](http://lesscss.org), [SASS](http://sass-lang.com) and [Compass -- a SASS framework](http://compass-style.org) are great [CSS preprocessors](https://htmlmag.com/article/an-introduction-to-css-preprocessors-sass-less-stylus) that will save me from coding boring CSS.

 Once I have these, I can go ahead and select a [CSS framework](https://en.wikipedia.org/wiki/CSS_framework). [Bootstrap](http://getbootstrap.com/), [Foundation](http://foundation.zurb.com), [Semantic](http://semantic-ui.com) and [PureCSS](https://purecss.io) are popular options.

 I left selection on the main framework last ... but I should definitely go with either [Angular](https://angularjs.org), [React](https://facebook.github.io/react/), [Ember](http://emberjs.com) or [Vue](https://vuejs.org)... These are pretty popular.

 Well... that pretty much is everything. Although I may still use one or two libraries here and there... perhaps [jQuery](https://jquery.com), [MooTools](https://mootools.net) or [Underscore](http://underscorejs.org) and maybe a few other [polyfills](https://github.com/Modernizr/Modernizr/wiki/HTML5-Cross-Browser-Polyfills) and [shimms](https://github.com/es-shims/es5-shim) to adress browser differences... I need to reseach these.

 And to be sure that I will introduce errors, I will setup also a JavaScript linter such as [ESLint](http://eslint.org/). Of course, I will not do all this linting manually. I will use a JavaScript task runner. [Grunt](https://gruntjs.com/) is an excellent task runner that can also do [minification](https://en.wikipedia.org/wiki/Minification_(programming)). Maybe I should also check out [Gulp](http://gulpjs.com/) and compare it with Grunt.

 On a second though I think I should also look into [RequireJS](http://requirejs.org/) and [Browserify](http://browserify.org/). They are great module packers, although some people really like [WebPack](http://webpack.github.io/) module bundler. These packers will allow me to work decently with a module format like [CommonJS](https://en.wikipedia.org/wiki/CommonJS) or [AMD](https://en.wikipedia.org/wiki/Asynchronous_module_definition).

 
 For the server side I can choose a popular technology such as [ASP.NET](https://www.asp.net/), [PHP](http://php.net/) with [Symphony](https://symfony.com/) or [Laravel](https://laravel.com/), [Python](https://www.python.org/) with [Django](https://www.djangoproject.com/), [Ruby](https://www.ruby-lang.org/) with [Rails](http://rubyonrails.org/), [node.js](https://nodejs.org/en/) with [Express](https://expressjs.com/), [Swift](https://en.wikipedia.org/wiki/Swift_(programming_language)) with [Kitura](http://www.kitura.io/) or [Go](https://golang.org/) with [Revel](https://revel.github.io/). 

 You know what: I think I will go with [node.js](https://nodejs.org/en/) since is JavaScript based like the client-side. I just need to install [node.js](https://nodejs.org/en/) runtime, [NPM](https://www.npmjs.com/) package management and [Express](https://expressjs.com/) web framework. 
 
 ... or maybe I should use [Hapi](https://hapijs.com/) or even better [Koa](http://koajs.com/) and leverage thouse JavaScript generators.

 I can select then a template engine. I'm still not decided if I should select a logic or logicless template engine. I have plenty of options... but I think I will go with [Pug/Jade](https://pugjs.org) or maybe [Handlebars](http://handlebarsjs.com). [Mustache](http://mustache.github.io) and [EJS](http://www.embeddedjs.com) are quite fine as well... Or maybe I should forget about server-side templates and start considering using a template engine on the client-side. Those browsers are quite powerful.

 Perhaps I should also investigate a full-stack framework such as [Meteor](https://www.meteor.com/) or [Derby](http://derbyjs.com/).

 As for deployment I say we should go for the public [cloud](https://en.wikipedia.org/wiki/Cloud_computing). There are plenty of options but you cannot go wrong with either [Azure](https://azure.microsoft.com/en-us/) or [AWS](https://aws.amazon.com/) or [Google cloud](https://cloud.google.com/) or even [Digital Ocean](https://www.digitalocean.com/).

 We should watch though for [cloud lock in](http://www.computerweekly.com/opinion/Cloud-vendor-lock-in-our-experience). Perhaps we should [dockerize](https://www.docker.com/) your application until we further investigate the [PaaS](https://en.wikipedia.org/wiki/Platform_as_a_service) model.

 Well... dear customer I think we are in good shape. I expect to finish the selection next month, then I will use the next month to download, install and configure the tools from [github](https://github.com/) and other stores. We can soon after meet and discuss the functional business requirements.

 Do you want a relational database or a [NOSQL](https://en.wikipedia.org/wiki/NoSQL) database?

 And finally I totally recommend building also a companion mobile application. HTML5 web applications cannot realy access the hardware of modern mobile devices. But don't worry: we have plenty of options here too...
