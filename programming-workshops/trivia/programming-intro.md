---
description: An exercise to review (or introduce) you to some key concepts in programming.
---

# Programming Warm-Up ⏱

## **The Big Picture**

![](../../.gitbook/assets/vidcoming.png)

**A program can be defined simply as** _**a set of instructions that perform defined tasks,**_ and we can use the  diagram below to frame the major components of a program. A program can be written to accept particular _**inputs,**_ like a mouse click, sound from a microphone, or a reading from a temperature sensor. The same program can handle the storage and retrieval of _**data**_, like _to do_ items or historical temperature data. The same program can then **output** something useful, like a current _to do_ list or move robot wheels. Multiple _**functions**_ are written to control and process everything towards some useful end, each function handling a particular task.

![](../../.gitbook/assets/programmingframework.png)

{% hint style="success" %}
**Consider planning an in-class activity where students diagram a computing application** \(whether a social app, an AI driven tractor, or a video game console\). Have them consider what inputs, data, and outputs the program includes. While the students will not know exactly how the engineers designed the application, they can come up with some specific function names to guess how the application processes the information. For example, a phone may have a **function** called "changeScreenBrightness" that takes the light sensor **input** to update the screen's brightness \(**output**\) based on a stored user preference \(**data**\).
{% endhint %}

#### Programming Languages

This exercise will use **JavaScript**, the primary programming language for web applications that work in a standard browser. There are many other popular programming languages. A particular language is chosen for implementation based on several factors related to the context of the need. Here are a few you may have heard of -- **Python, Java \(different from JavaScript!\), Arduino, C++ and C\#**.  Note: While HTML and CSS are languages with a defined syntax, they are usually distinguished from programming languages that provide computation and functions.

## Let's Program: Variables, Functions, and Conditionals

This exercise takes a direct approach to prepare you for programming a CxD project by taking an _"application first"_ perspective. **We will frame this introduction by creating a simplified** _**To Do Application**_ **using Javascript, HTML, and CSS for use in a web browser.** 

{% hint style="info" %}
**You are highly encouraged to build \(and experiment with\) the program as demonstrated in the video to get a feel for the programming.**  It is assumed you completed the "Getting Started with Replit" in the _Workshop Prep_. Also, remember to also try some online tutorials as a supplemental experience as explained in the _Workshop Prep_.
{% endhint %}

![](../../.gitbook/assets/vidcoming.png)

### Declare Variables and Use a Built-in Function

First, in our _script.js_ file, let's **declare** some **variables** of different **data types** and set their **values**.

*  `todo` is a _**string**_
*  `time` is a _**number**_
*  `isComplete` is a _**boolean**_ \(true or false\). 

Then we use a **built-in function** `console.log()` to display the values.

{% code title="script.js" %}
```javascript
//declare some variables for our data
var todo = "Walk the dog.";
var time = 30;
var isComplete = false;

//use a built-in function `console.log()` to output values
console.log(todo); 
console.log(time);
console.log(isComplete);
```
{% endcode %}

### Define a Custom Function

Here we **define** a **custom function** `displayTools()`. This allows us to **call** \(or **invoke**\) the function whenever we want.

{% code title="script.js" %}
```javascript
//declare some variables for our data
var todo = "Walk the dog.";
var time = 30;
var isComplete = false;

//define a custom function to output to do's
function displayTodos() {
  console.log(todo);
  console.log(time);
  console.log(isComplete);
}

//call (or invoke) the displayTodos() function to actually run it
displayTodos();
```
{% endcode %}

### Use a Conditional Statement

Here we use a **conditional statement** \(using **if/else**\) _****_to customize the output.

{% code title="script.js" %}
```javascript
//declare some variables for our data
var todo = "Walk the dog.";
var time = 30;
var isComplete = false;

//define a custom function to output to do's
function displayTodos() {
  console.log(todo);
  console.log(time);
  
  //customize the output based on whether it is complete
  if (isComplete) {
    console.log("This is complete.");
  }
  else {
    console.log("This is not complete");
  }
}

//call (or invoke) the displayTodos() function to actually run it
displayTodos();
```
{% endcode %}

## HTML and JavaScript

Here we cover just the basics of how to update HTML content using JavaScript. This allows us to output content in the normal browser window that can be visually customized.

![](../../.gitbook/assets/vidcoming.png)

### Define HTML Elements for the Content

Here we have **three** _**div**_ **elements** in our HTML to display _the to do item_, _the time to complete_, and _the status of the to do item_. Notice how each element has a defined **attribute**, an _**id**_ that will allow us to update the HTML content with JavaScript next.

{% code title="index.html" %}
```markup
    <!-- all of this HTML goes inside the body element  -->
    <div id="todo-item">My To Do Item</div>
    <div id="time">Time to Complete</div>
    <div id="is-complete">Is it Complete?</div>
    <script src="script.js"></script>
```
{% endcode %}

### Update the HTML Content with JavaScript

Here, rather than use the `console.log()` function, we use `document.querySelector()` to **select** the HTML element we want, based on the **id attribute**, then set the innerHTML to the value we want. 

{% code title="script.js" %}
```javascript
//declare some variables
var todo = "Walk the dog.";
var time = 30;
var isComplete = true;

//define a custom function to display to do's
function displayTodos() {
  document.querySelector("#todo-item").innerHTML = todo;
  document.querySelector("#time").innerHTML = time;
  
  //customize the output based on whether it is complete
  if (isComplete) {
    document.querySelector("#is-complete").innerHTML = "This is complete.";
  }
  else {
    document.querySelector("#is-complete").innerHTML = "This is not complete";
  }
}

//call (or invoke) the displayTodos() function to actually run it
displayTodos();

```
{% endcode %}

## CSS

CSS \(Cascading Stylesheets\) allow us to have fun with the style of web content. Let's update our code a little bit and have some fun with it.

![](../../.gitbook/assets/vidcoming.png)

### Update HTML Elements

Let's update our HTML file a little. First let's wrap our content in another _div_ element with a **class** called _card_. This will allow us to create a visual card with some style. Next, let's change our _todo-item_ element to an _**h2**_ **element** so that it is larger by default.

{% code title="index.html" %}
```markup
    <!-- all of this HTML goes inside the body element  -->
    <div class="card">
        <h2 id="todo-item">My To Do Item</h2>
        <div id="time">Time to Complete</div>
        <div id="is-complete">Is it Complete?</div>
    </div>
    <script src="script.js"></script>
```
{% endcode %}

### Define Some Styles

Here we set the _body_ \(the whole page\) background color and the _h2_ element text color. We also style the element that has a class of "card" with many properties. Notice that we can **select** elements by the **element name** \(like with body and h2\) or by the **class** using a period before the class name \(like with .card\). You could also select elements by _id_ by prefixing the _id_ name with a \#.

{% code title="style.css" %}
```css
body {
  background-color: lightgray;
}

h2 {
  color: red;
}

.card {
  background-color: white;
  border: 5px solid yellow;
  border-radius: 7px;
  padding: 15px;
  box-shadow: 1px 1px 3px black;
}
```
{% endcode %}

## Wrap-Up

That's our warm-up. Please don't hesitate posting questions along with a link to your replit code in our Slack channel for the workshop.

