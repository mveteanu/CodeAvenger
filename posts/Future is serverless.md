Future is serverless
====================

Server is for web applications as is bread for peanut butter sandwich. You cannot have one without the other. If you want to build a web application that processes some data then you need to have a server for that – everybody understands this.
You can buy your own server or you can rent a physical or virtual server from a data center or cloud provider. There are plenty of offers. Once you have the server you can build your application.

And still, one of the hottest trends in architecture is serverless architecture. Confusing? Right?
Serverless doesn’t mean that you eliminate the server – you just use the servers of a cloud provider as a transient function provider. This is one step further than what PaaS promised. You don’t have to rent the servers and most importantly you don’t have to think how to scale the servers when the application demands so. When you need to perform a server function you just use a service that executes that function for you. It’s that simple!
That’s why some experts consider serverless is a misnomer. They better prefer the term Function as a Service… although depending on architecture serverless may go a little bit beyond the FaaS term.
What you get is better cost model and, as mentioned above, scalability. Serverless being a very good candidate for implementing some types of microservices.

And since is a hot topic, all major cloud providers have offering around serverless.

##Amazon AWS Lambda
[https://aws.amazon.com/lambda/](https://aws.amazon.com/lambda/ )

##Microsoft Azure Functions
[https://azure.microsoft.com/en-us/services/functions/](https://azure.microsoft.com/en-us/services/functions/)

##Google Cloud Functions
[https://cloud.google.com/functions/](https://cloud.google.com/functions/ )

##IBM OpenWhisk
[https://developer.ibm.com/openwhisk/](https://developer.ibm.com/openwhisk/ )

And it doesn’t stop here. If you dig dipper into the serverless trend you’ll soon discover entire frameworks that try to help you even further with building event-driven serverless applications. 
One of such frameworks is opensource and is intuitively enough named [Serverless framework](https://serverless.com/framework/)

I cannot end the post without mentioning about vendor lock-in concerns. I understand these concerns – I’ve been there too. However the truth is that at the end of the day you cannot take advantage of what cloud offers if you look only in IaaS. Take an analogy: you cannot build a nice desktop or even web based application nowadays unless you use a 3rd party library or technology. If you want to move your application to a different OS or library you have to port your code. 
The same with PaaS and serverless – adopt them now but be aware of portability challenges. I don’t think any standardization between cloud providers will come anytime soon.

If you want to learn more about serverless, I recommend you to check Martin Fowler’s [article](http://martinfowler.com/articles/serverless.html) about this topic.

