# Programming Warm Up

![](../../.gitbook/assets/vidcoming-welcome.png)

{% hint style="info" %}
For our programming warm up we will use [CodePen](https://codepen.io), because it is quick and easy to startup in the browser. For our projects, we will use [repl.it](https://repl.it), which is similar but provides many more features.
{% endhint %}

## HTML Basics

HTML provides the structure for web pages and uses _elements_ with _tag names_ to differentiate items on the page. For example, `<h1>...</h1>` is a large heading element. Notice the _opening tag_ `<h1>` and _closing tag_ `</h1>` that indicates the beginning and end of the element. "h1" is the tag name in this case.

```markup
<h1>Favorite Technology Sites</h1>
<h3>MIT Technology Review</h3>
<p>The <a href="https://www.technologyreview.com/">MIT Technology Review</a> keeps me up to date on innovation.</p>
```

### Try it out

1. Copy and past the HTML above into [**a new CodePen**](https://codepen.io/pen/) and notice how the browser preview looks.
2. Read these explanations on W3schools.com. [Headings](https://www.w3schools.com/html/html_headings.asp), [Paragraphs](https://www.w3schools.com/html/html_paragraphs.asp), and [Links](https://www.w3schools.com/html/html_links.asp)
3. Add two more sites to the list with each having it's own "h3", "p", and "a" elements.

## Using CSS to Add Style

CSS stands for _cascading stylesheets_ and allows us to modify the appearance of HTML elements in a browser. Study [**this W3schools page**](https://www.w3schools.com/css/css_syntax.asp) to understand the syntax of CSS. It is important to understand the concepts of a _selector_, _property_, and _value._

```css
h1 {
  color: red;
}
h3 {
  background-color: black;
  color: white;
}
p {
  font-size: 20px;
}
```

### Try it out

1. Copy the CSS code above and add it to your CodePen from the [**HTML Exercise**](https://docs.idew.org/principles-and-practices/principles/programming-principles/html), and notice how the browser preview has changed.
2. Modify the CSS by changing colors and font-size.
3. Customize your look by adding the style properties below on the HTML elements you choose. 

* [Border](https://www.w3schools.com/cssref/pr_border.asp) 
* [Margin](https://www.w3schools.com/cssref/pr_margin.asp) 
* [Padding](https://www.w3schools.com/cssref/pr_padding.asp) 
* [Box-shadow](https://www.w3schools.com/cssref/css3_pr_box-shadow.asp) - This one is cool. 

## Target Content with Classes and Id

By assigning a class or id to an HTML element you can apply specific styles in a targeted way.

{% code title="HTML" %}
```markup
<div class="card" id="jill-card">Jill - Data Scientist</div>
<div class="card">Johnny - UX Designer</div>
<div class="card">Mia - Software Developer</div>
<div>Patrick - Business Analyst</div>
```
{% endcode %}

{% code title="CSS" %}
```css
.card {
  padding: 5px;
  margin: 20px;
  background-color: lightgray;
  box-shadow: 2px 2px 3px;
}
#jill-card {
  background: yellow;
}
```
{% endcode %}

### Try it out

1. Copy the HTML and CSS above and paste it in a [**new CodePen**](https://codepen.io/pen/).
2. Take a look at the browser preview and try to decipher what is going on.
3. Notice how assigning `id="jill-card"` in the HTML allows the element to be "targeted" with the CSS selector `#jill-card`.
4. Notice how assigning `class="card"` in the HTML allows several elements to be "targeted"  with the CSS selector `.card`.
5. Go ahead and give Patrick's text a _class_ of "card" and then add a unique _id_ to his HTML element and some CSS to make his card stand out from all the others. 

{% hint style="warning" %}
**id** - An HTML _id_ is selected in CSS with a `#` prefix and should be used to target a single element on a page.

**class** - An HTML _class_ is selected in CSS with a `.` prefix and can be used to select several elements that will share a common style.
{% endhint %}

## Hierarchy in HTML

Look at the HTML below. Do you see how the _container_ could be called the **parent** of the three cards? The _cards_ are then **children** of the _container._ This is an example of [**nested HTML**](http://www.developphp.com/lib/HTML/Nesting-and-Indenting)**.**

{% code title="HTML" %}
```markup
<div class="container">
  <div class="card">Jill - Data Scientist</div>
  <div class="card">Johnny - UX Designer</div>
  <div class="card">Mia - Software Developer</div>
</div>
```
{% endcode %}

{% code title="CSS" %}
```css
.container {
  border: 1px dotted black;
  padding: 5px;
  background-color: lightyellow;
}
.card {
  padding: 5px;
  margin: 20px;
  background-color: lightgray;
  box-shadow: 2px 2px 3px;
}
```
{% endcode %}

### Try it out

1. Copy the HTML and CSS above into a [**new CodePen**](https://codepen.io/pen/). 
2. Notice in the browser preview how the nesting becomes visually apparent.
3. Also, notice how the indentation in the HTML is really helpful to see the proper structure. Technically the indentation does not need to be there, but it is a good programming practice.
4. Add a parent `<div>` element with a class of "outer-container" to the _container_  and style it with a solid border line. Use good indentation in your HTML.

