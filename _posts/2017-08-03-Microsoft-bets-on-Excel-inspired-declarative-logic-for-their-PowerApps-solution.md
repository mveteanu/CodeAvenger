Microsoft bets on Excel-inspired declarative logic for their PowerApps solution
===============================================================================

[PowerApps](https://powerapps.microsoft.com/en-us/) together with [Flow](https://flow.microsoft.com/en-us/) and [Power BI](https://powerbi.microsoft.com/en-us/) are the main pillars of [Microsoft’s Business Platform](https://businessplatform.microsoft.com/en-us/) – a low-code ecosystem for building applications, workflows and data analysis for businesses. 

When faced with the task of building an application, expert programmers are probably choosing to one of the many [options](http://www.codeavenger.com/2017/06/14/Development-then-and-now.html) available today for this task. However, this is beyond the reach of [citizen developers](http://www.codeavenger.com/2017/07/24/From-VB6-to-modern-low-code-platforms-for-citizen-developer.html) of typical corporations. This is where low-code platforms like PowerApps shine.

What attracted my attention to PowerApps and prompted to write this article is Microsoft’s vision of building an app builder tool powered by Excel like formulas. Being [involved](https://www.linkedin.com/in/mveteanu/) myself in designing and building low-code tools, I understand the challenges that you have to solve in order to create easy to use authoring tools for people that don't typically have a computer science background.

![](/img/posts/powerapps.gif)

Imperative logic
----------------

In the common event-driven environments, programmers are building applications writing imperative logic that gets triggered on some events.
Example:

```
Sub Button_OnClick
	IF IsBlank( Name ) Then
		txt.Text = “Red”
	ELSE
		txt.Text = “Black”
	ENDIF	
End Sub
```


Declarative logic
-----------------

In PowerApps, the logic is written in declarative ways, exactly like formulas in Excel. To implement the above logic, you need to assign a formula to txt.Text property as this:

```
txt.Text = If( IsBlank( Name ), Red, Black )
```

The whole logic become in this way backwards. Instead of the “push” model from the imperative programming (when you specify exactly when to set a particular property), you have to switch your application to a “pull” model where each property pulls the data at appropriate time when the application decides to recalculate the formulas.

Excel people should feel very familiar with this model. Actually to smooth the learning curve, Microsoft implemented the same kind of formulas that Excel has in PowerApps.

The downside of this idea is that the entire application becomes a long list of small formulas. You will not have big chunks of code like in typical programming … but just a bunch of formulas like in Excel.

Microsoft played with this formula idea before in Project [Sienna](https://www.microsoft.com/en-us/projectsiena) from which actually PowerApps is derived.


Conclusion
----------

This mode of implementing logic may not appeal to everybody… but one thing is certain. This is a pretty interesting way of addressing the challenge of adding "scripting" capabilities to application builder tools intended for non-programmers.

Those legacy InfoPath / Designer projects seems also to have an upgrade path to PowerApps and Flow.

You can give PowerApps a try and see it for yourself at [create.powerapps.com](http://create.powerapps.com/)
