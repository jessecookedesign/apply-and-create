---
title: Insert HTML text into your website with JavaScript ​
date: 2021-04-06T13:26:57.318Z
description: As a web developer, you're going to run into situations where you
  need to insert text onto a page based on some sort of condition. Maybe the
  text content will change based on the user's membership status, or the time of
  day, or whether or not they're signed in. It's a common problem we need to
  solve, but how do we solve it?
---
## 1. Create an HTML element
Before we write any JavaScript, we need to make an element for our text and give it an ID.
​
In this example, I'll be creating a paragraph tag with an **ID** of "text_area":
`` <p id="text_area></p> ``
​<br><br>
## 2. Select the element with JavaScript
Next, we need to select the element.
There are a few ways to select HTML elements with JavaScript: you can read about them here. For this example, I'll be using `.getElementById`. This will select the element with the **ID** I specify.
​
Then write out `document` to access the page content. Lastly, `.getElementById("");` and fill in the **ID** from step 1.
```
document.getElementById("text_area");
```
​
## 3. Create a variable
We've selected the element but we can't really do anything with it until we turn it into a **variable**. Assigning a variable will let us easily select this element again later in our code.
​
Create a variable by writing `var [name here] =` and give it a name. I'll use "x" as my variable name.
```
var x = document.getElementById("text_area");
```
​
## 4. Set the text to be inserted
The part you've been waiting for! All we need to do here is add the method `.innerText = ""` to our variable.
​
```
x.innerText = "Sample message!";
```
​
#### The whole block of code should look like this:
```
<p id="text_area></p>
​
<script>
	var x = document.getElementById("text_area");
	x.innerText = "Sample message!";
</script> 
```
​
#### Pair it with an if/else statement for conditional messaging!
```
<p id="text_area></p>
​
<script>
	var x = document.getElementById("text_area");
​
	if (userState = "signed in") {
		x.innerText = "You're signed in!";
	} else {
		x.innerText = "Sign in or sign up to use this site";
	}
</script> 
```