Develop 2-tier web applications with Firebase
=============================================

Using the database from the client-side of a web application has been a no-no since the very first days of web development. Having SQL statements on the client-side indicated poor architecture that was prone to security issues. 

It is true that before web time, majority of database applications had 2 tier architecture. Those were simpler times.

Recently with the advances in both cloud computing on one side and internet connected gadgets on the other side (mobile phones and various consumer and industrial IoT devices), the 2 tier architecture is making a comeback in a new formula.

If you are a mobile app developer that spent countless of hours developing the next viral game, the last thing you want to care about is developing a backend for storing hi scores. Luckily you can use one of the many BaaS (Backed as a Service) and / or DBaaS (Database as a Service) options available in a cloud near you.

Even better … you don’t have to be a mobile developer to leverage these new cloud options. Some of the DBaaS options can be used with classical web applications directly.

Parse (https://parse.com/) was one of the first options like this. Unfortunately Parse service was shutdown at short time after Facebook acquire it. Thousands of apps had to find a new solution. Microsoft even welcomed those Parse customers in the Azure cloud with new templates for Parse.

Another option is Google Firebase (http://firebase.google.com/). Firebase is both a storage and real-time database. Firebase can be used in a wide variety of scenarios starting with mobile applications, IoT devices (even Arduino can work with Firebase)… and ending with browser-based, client-side JavaScript web applications.

With Firebase you can finally implement a 2-tier web application where you communicate with the data services directly from the client-side, skipping the classical application server altogether. From this point of view we can place Firebase in the serverless bucket.

Not only that, but Firebase is also a realtime type database. Instead of puling data constantly, you subscribe to Firebase data services from JavaScript and within milliseconds you automatically get new data when becomes available.

To get started with Firebase for web applications takes only a few lines of JavaScript code:

-	First you need to initialize the connection to Firebase, providing the API Key assigned by Google
-	Next you’re good to go to read data. As mentioned before, reading of the data can be done by just subscribing to Firebase via a callback:

```JavaScript
var starCountRef = firebase.database().ref('posts/' + postId + '/starCount');
starCountRef.on('value', OnCountChanged);
// This function gets triggered automatically when data available
function OnCountChanged(eventArgs)
{
}
```

Since not all readers of this article may be code savvy, I will not provide any other examples… but if you are interested you can go to https://firebase.google.com/docs/database/web/start to see a quick introduction.

In conclusion – I think that Firebase worth definitely a look especially if you are a mobile or IoT device developer. 
If you are thinking about using Firebase with your web application (as talked in this article), I advise you to consider carefully this option in parallel with a more traditional architecture that involves a classical backend. There are however niche situations were Firebase used directly from client-side helps you with the cost and maintenance of web applications. 
Perhaps you can use Firebase with those static HTML applications mentioned in this article to give them a little bit of data awareness.

The big concern comes however from the stability of Firebase. Is Google committed to support Firebase in the long run? … or it will discontinue the service in the same way Facebook did with Parse? Of course you may have this concern with other hi-level cloud services as well.

The decision is yours!

Further reading:

- [Firebase Web Codelab](https://codelabs.developers.google.com/codelabs/firebase-web/index.html)
- [Zero to App: Develop with Firebase - Google I/O 2016](https://www.youtube.com/watch?v=xAsvwy1-oxE)
- [Deep Dive into the Realtime Database - Google I/O 2016](https://www.youtube.com/watch?v=cYinms8LurA)


