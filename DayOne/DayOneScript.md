# Day One

In this phase we are going to go through the following

* [Basics of internet](##basics-of-internet)
* [Programming Languages & Emerging Trends](##programming-languages)
* [History of Javascript](##history-of-javascript)
* [First Web Page](##first-web-page)

## Basics Of Internet

>> Go throug the slides CFR_Understanding_Internet

## Programming langauges & Emerging Trends

>> Go through the slides CFR_Programming

## History of Javscript

>> Go through the slides CFR_HistoryOfJavascript

## First Web Page

>> Go through the slides CFR_FirstWebPage

>> CODE

Ok let's create a file named index.html by;

Open Visual Studio Code and from the `File` menu option choose `New File`

Enter the name of the file `index.html` and click `Save`

Now let's create a

`<h1></h1>`

Inside the html page I would like to add Some text.

```
<h1>Coding 101</h1>
```

After this I would like to add a paragpraph and a link

```
<p>
At Recruiters’ Coding School, you’ll concretely dive into the world of coding with a nice balance of theory and hands-on practice. By joining you’ll gain a deeper industry knowledge which leads to richer discussions with your candidates – not to mention the improved candidate experience!
</p>
```

```
<div>
    <a href="https://talented.fi/recruiterscodingschool/">Sign up page</a>
</div>
```


Ok so we have a heading and a paragraph let's add an image

```
<img src="https://talented.fi/wp-content/uploads/2019/08/nur.jpg" alt="Nurs image">
```

Next lest try to add a list.

```
<ul>
    <li>Intorduction to terminal</li>
    <li>Basics of internet</li>
    <li>First web page</li>
    <li>Into to programming</li>
    <li>First web application</li>
    <li>Introduction to version control</li>
    <li>Introduction to databases</li>
</ul>
```

### HTML EXERCISE

10 min exercise:

* Make one word in the paragraph bold
* Make one word in the paragraph italic
* Add an image with the following url `https://talented.fi/wp-content/uploads/2019/05/janne_talented-300x300.jpg`


>> CSS SLIDES CFR_FirstWebPage

>> CODE CSS

So let's add some style to our elements.

Let's increase the font of the text in the paragraph to 24px

```
<p style="font-size: 24px;">
```

Now let's turn the color to of the H1 to a shade of blue

```
<h1 style="color: dodgerBlue">
```

Let's also increase the font size of the link and remove the underscore and change the color to blue.

```
<a style="font-size: 24px; text-decoration: none; color: dodgerblue;"
```

Let's change the size of the image

```
<img style="height: 200px;"
```

Let's add some margins and width to the document body

```
<body style="margin-top: 20px; margin-left: auto; margin-right: auto; width: 1200px;">
```


### EXERCISE
10-15 Minutes

* Add 10px space under the link
* Change background colour


Now that we got the basic understanding of adding structure and design let's talk why it is not a very good idea to have styles embedded in the HTML tags.

* Bad practice
* Difficult to maintain
* Against the specs (rules)
* Spagetti
* Repeating the same styles over and over again

So to remedy this issue we need to seperate the CSS from the HTML

So let's start by creating a file.

In your Visual Studio Code click `File` from the menu bar and select `New File`

Enter the name `main.css` and save

Next let's add a style to our main.css and see how to connect the html files with the css file

in your `main.css` file let's change the font for the document

```css
body {
    font-family: Arial, Helvetica, sans-serif;
}
```

>> Refresh Page.

As you can see nothing changed in the page. That is because we didn't `link` the css to the HTML page.

In order to do that.

Go to your `index.html` page and add a link to css so it know where to find the style sheet

Add the folling In the `head` tag over the `title` tag

```html
<link rel="stylesheet" type="text/css" href="./main.css">
```

>> Refresh

Now you can see that the fonts have changed.

Alright the next step is to take all of that style in the `index.html` that we wrote and move it to `main.css`file

>> Introduction to classes & Ids

Now that we have moved all of the sytles to the main.css we have partially solved the problem with the maintainability, bad practice and specs problem. However we didn't resolve the issue with not repeating ourselfs.

Right now when we want to style an element we need to call the element directly.

But the problem what if we have more than one paragraph or more than 1 header which we want to style differently.

Enter HTML Class and Id attributes

Let's start with Classes.

The class attribute specifies one or more classnames for an element.

The class attribute is mostly used to point to a class in a style sheet. However, it can also be used by a JavaScript (via the HTML DOM) to make changes to HTML elements with a specified class, which we will discuss it later on.

So how does it work.

>> DEMO

Open up your Visual Studio Code and open index.html

Let's add some more paragraphs under the paragraph that we already have

```html
<p>Talented is the talent agency for experienced developers and designers. We’re here to find the most interesting companies and projects for you.
</p>
<p>Talented specializes in offering tailored career possibilities for experienced developers and members of software development teams. Unlike most Talent Agencies, our focus is on your needs. We fulfil developers and designers’ dreams, not companies’.
</p>
```

Next let's add a class to each of our paragraphs a different font-size

The first paragraph
```html
<p class="font-size-24">
```

The second and third paragrapsh
```html
<p class="font-size-16">
```

Next let's turn our second and 3rd paragraphs to have a lighter font color

```html
<p class="font-size-16 txt-light-black">
```

Now let's head to `main.css` and remove the paragraph style
and edit our style sheet to apply those styles

```css
.font-size-24 {
    font-size: 24px;
}

.font-size-16 {
    font-size: 16px;
}

.txt-light-black {
    color: #676767;
}
```

Ok next let's look at HTML `ID` attribute

The id attribute specifies a unique id for an HTML element (the value must be unique within the HTML document).

The id value can be used by CSS and JavaScript to perform certain tasks for the element with the specific id value.

Ok so basically with classes you target all elements which has the same class attribute. The `ID` attribute would allow us to target a single specific element.

Ok so let's see how it is used.

We have bunch of list elements. Let's target the second list element so it has a different color and a strike through.

in index.html
```html
<li id="secondListElement">Basics of internet</li>
```

Now let's add the style

in main.css
```css
#secondListElement {
    color: red;
    text-decoration: line-through;
}
```


>> THIS IS WHERE WE LEFT THE FIRST DAY

Ok let's take it a notch more interesting and add a hero element

In index.html add the following to the top

```html
<div class="hero-image">
  <div class="hero-text">
    <h1>Recruiters</h1>
    <p>Welcome to Introduction to coding</p>
  </div>
</div>
```

>> TALK about divs

In css

add the following to the body element style rules

```css
body,html {
    height: 100%;
}
```

Add the following styles under the body element style rules
```css
.hero-image {
    background-image: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url("https://talented.fi/wp-content/uploads/2019/08/koodikoulu_talented5.jpg");
    height: 60%;
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    position: relative;
}

.hero-text {
    text-align: center;
    position: relative;
    top: 50%;
    color: white;
}
```

Ok thats nice but I would like the image to be streched and the content to be narrow

So first let's add a div element and put all of our content inside the div element and give it a class `content` so we can style it in the style sheet

```html
<div class="content">
    <h1>Coding 101</h1>
```

Next let's change the `body, html` properties

```css
body, html {
    font-family: Arial, Helvetica, sans-serif;
    margin-top: -12px;
    margin-left: 0px;
    margin-right: 0px;
}
```

Next let's add a rule for `content` element

```css
.content {
    width: 1200px;
    margin-right: auto;
    margin-left: auto;
}
```

Now our page should a little nicer.

### Excersize (30 min)
* Change the style of the header and paragraph with classes
* Add 3 new html element tags from the this list https://www.w3schools.com/tags/default.asp
* Add styles to those elements


>> Continue for JavaScript Slides from CFR_FirstWebPage

>> DEMO

Ok in the browser window right click and select `Inspect Element`

This will open the web inspector.

Next click the `Console` tab in the inspector

now type the following

```javascript
5 + 4
```

This will calculate 5 + 4 and return to you the result.

Congrats you have wrote yoru first line of code.

Ok so let's write our first script

in the `index.html` page add the following;

```html
<h1>Coding 101</h1>
<i id="author"></>
```

As you see we have added an element `<i>` And we left it empty so it doesn't have any text content within.

So if you refresh the page nothing changes

What we want to do is to add the Author name programmatically

Go now to the browser and type the following

```javascript
document.getElementById('author').innerText = 'Nur Ketene'
```

Alright what is happening here?
Let's go step by step.


First with `document` we are getting the HTML document `object`

This object has some methods & properties one of those methods is `getElementById()`

getElementById is a method that looks for an element with the ID of 'author' and it returns that element

This element has also some properties. One of them is called `innerText`.

`innerText` method does two things. It would `GET` the text value of the element or you can use it to `SET` the text value of the element.

In this case we are setting the value of the element with the `author` id by assigning `=` the string value `Nur Ketene`

Ok nice so let's try to add more interactivity by letting the user to show and hide the author name

First let's add the button to show the author.

in your `index.html` file

```html
<button id="showAuthor">Show Author</button>
```

If you go ahead now and refresh the page and click the button nothing will happen. So we need to trigger a function when the user clicks the button. To do that we need to add an `onclick` attribute to the button element like below';

```html
<button id="showAuthor" onclick="showAuthor()">Show Author</button>
```

Nice we are now triggering an event called `showAuthor()` but that event doesn't exist yet. So let's create it

At the bottom of your `index.html` add the following to the bottom of the page

```html
<script>
    function showAuthor(event) {
        document.getElementById('author').innerText = 'Nur Ketene';
    }
</script>
```

Alright now if you go ahead and refresh the page and click the button you will see the author name but the button is still there. It would be maybe better to hide that button.

So let's edit our event as the following by adding a new line to hide the element with id `showAuthor` button

```html
<script>
    function showAuthor(event) {
        document.getElementById('author').innerText = 'Nur Ketene';
        document.getElementById('showAuthor').style.display = 'none';
    }
</script>
```

### Excersize (30 min)

* Add a button to hide author name
* Hide the hide button when user clicks hide button
* Make show button visible again when the user hides the author

Congradulations guys. You have finished the first day!!!!