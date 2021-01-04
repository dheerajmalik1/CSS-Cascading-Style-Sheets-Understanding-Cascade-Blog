# CSS-Cascading-Style-Sheets-Understanding-Cascade-Blog


Let's say you have below piece of code in your html file

```<h1>Today I will learn about cascading</h1>``` 

Now you wish to apply apply some CSS to make it pretty, so you do this in your .css file


```
h1{ 
   font-family:Aerial;   
   color:yellow;
}
``` 

What we have here till now in our CSS :-

1. h1 - this is our **selector**
1. Code inside the curly brackets(including brackets) is  **declaration**.
1. Both 1 and 2 combined form a **rule set**

Great!

Just keep these terms in mind.


A key thing to remember while writing CSS is, if you are not applying a style on a particular element, there might be chance you are getting those **styles by default** from the **browser** itself, these are called **User Agent Sheets**. You can remove these by applying your own css styles which are called - **author styles** - the styles (CSS) that you write.

*Supplemental ↓*

> What are the target browsers? Different browsers set different default CSS rules. Try including a CSS reset, such as the meyerweb CSS reset or normalize.css, to remove those defaults. Google "CSS reset vs normalize" to see the differences. [For more info](https://stackoverflow.com/questions/12582624/what-is-a-user-agent-stylesheet) 

> If <!DOCTYPE> is missing in your HTML content you may experience that the browser gives preference to the "user agent stylesheet" over your custom stylesheet. Adding the doctype fixes this. [For more info](https://stackoverflow.com/questions/12582624/what-is-a-user-agent-stylesheet) 
 
We know we can apply styles to our html in 3 different ways.(If not, you can read about it  [here](https://www.tutorialrepublic.com/css-tutorial/css-get-started.php) )

> CSS can either be attached as a separate document or embedded in the HTML document itself. There are three methods of including CSS in an HTML document:
There are three methods of including CSS in an HTML document:
Inline styles;Embedded styles;External style sheets

Inline styles override both External style sheets and Embedded styles, but if you add 
***!important*** it will override your inline styles too, so that style gets the highest priority.

**Specificity**

As a rule of thumb, the **more specific** you keep on getting with your style and element selection, more prioritised your styles will get, we will see more on this below.

We assign ids, classes to elements in html file to make styling and formatting easier, but we often forget that elements with ids and classes will have specificity, that their priority on getting style applied are different, huh?

while applying styles, browsers give priority to styles declare with ids more than styles declared with classes, or tags, because again, the more spicific you get, more is the priority of getting that style applied, lets see this with an example

```<h1 class ="classes"  id="ids">Today I will learn about cascading</h1>``` 

lets say in out .css file we have :


```
h1{
  color: red;
}
.classes{
  color: yellow;
}
#ids{
  color: green;
}


``` 
the priority will be given to style declared with id first, then with class and then with tags, as I said the more specific you get more is priority.

Summary

- Source of css matters, while debugging check if the style you want to apply is coming from prioritised source.

- Selector specificity should be taken care of while writing styles.

- Try to avoid IDs, as one particular id can be used only once per page and they may mess if there are collisions.



Hope you enjoyed.




Sources
- https://css-tricks.com/the-c-in-css-the-cascade/
- https://stackoverflow.com/questions/12582624/what-is-a-user-agent-stylesheet
- https://www.tutorialrepublic.com/css-tutorial/css-get-started.php








