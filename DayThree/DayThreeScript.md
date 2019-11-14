# Introduction

Congradulations you have made it to Day Three.

In this day we are going to learn about web applications

We are going to download a pre made boilerplate application from the repository and then we are going to install the dependencies.

Once you have installed the dependencies we are going to start modifying our application.

The application in its curretn form is a dumb application.

So there are hardcoded bits here and there. We are going to replace all of that with dunamic data that is coming from the database.


## Installation

Download the code from the repository. https://github.com/nursahketene/c101-todolist

Next lets open the code base with VS Code by going to `File>Open>c101-todolist`

Once you do that lets bring our terminal from the bottom by dragging it out. Or from the menu bar `View>Terminal`

In the terminal run

```bash
npm install
```

this will install all of the dependencies that you need and make sure everything is working.

Next lets run the following command to start our app.

```bash
node app.js
```

Once you have done wit this and see on your terminal

```bash
Server running on http://localhost:5000
```

You are good to go. Lets open our browser and visit the url `localhost:5000`

Congrats your first app is running.

## How it works.

>> Explain how a web application works

## Lets make the form `/done` work

So we have a Form in our view but when we click a button in the form we get an error message.

Lets fix that first.

So go to the code base and open `routes>index.js`

In this file we will have all of our routes to the views

So let's create a route for our form and log if the user clicks the button `Done`

```js
  {
      method: "POST",
      path: "/done",
      handler: (request, h) => {
          console.log('Button Clicked');
          return h.redirect("/")
      }
  }
```

Now here we have created a route for our action and then handled a response and redirect the user to the same page.

Awesome. Next lets try to get the information for the selected items and lets try to log that information

```js
  {
      method: "PUT",
      path: "/done",
      handler: (request, h) => {
          console.log('Button Clicked');
          console.log(request.payload)
          return h.redirect("/")
      }
  }
```

If you re-start the application and select an item from the list and click `Done` You should see the following

```bash
{"todos":"1003"}
```

Ok good so now we are getting some information. Thats nice.

We have now connected our router with our view and also getting the payload information.

Since now we are getting our list items lets try to connect the router to the database.

## Lets make the `/add` form work

So we have made the `/done` form work now it is time to make our Add button work without crashing.

Let's add a new route;

```js
  {
    method: "POST",
    path: "/add",
    handler: (request, h) => {
      console.log("Added new element");
      console.log(JSON.stringify(request.payload));
      return h.redirect("/");
    }
  }
```

In this route we are loging `Added new element` when a user clicks the `Add` button and log the text as well.

So lets restart the server in the terminal and go to the browser.

Here lets Add some text to the input field and click `Add` button. We should stay in the same page and in our terminal we should see

```bash
Added new element
{"todo":"Take trash out"}
```

Awesome. Now both of the buttons are working but it doesn't really add any thing or change anything. We just created the routes but we didn't actually saved the data anywhere. We just loged them.

## Connecting the database

Next lets deal with our database. We want to save stuff to our database and we also want to mark things in our database as done. On top of that we want to update our views with the actual data instead of the hardcoded fake data.


First lets require the database connector

```js
const {getDB} = require('../models/todos');
```

next lets call the method so we can save a todo list item to the database.

In your `/add` path let's add the following;

```js
const idNumber = Math.random().toString().slice(2)
const database = await getDB()
await database.insertOne({_id: idNumber, text: request.payload.newTodo})
```

Nice now are able to add one array let's also fetch now all of the items we have in the database

```js
let todos = await database.find().toArray()
console.log(todos)
```

Now lets restart the server and add a todo list item from the browser. You should see a list of items in the teerminal.

Good job.

Next Lets try to remove the hard coded list items and replace it with data from the database.

First lets send the data to the views.


```js
const database = await getDB()
let todos = await database.find().toArray()
if (todos.length < 1) {
  todos = []
}
return h.view("index", {todos});
```

Next Lets go to the `index.html` and modify the view so it will print the data we get from the database.

So first lets remove all of the hard coded data and replace it with this

```hbs
{{#each todos as |todo|}}
    <div class="form-check form-group">
        <input class="form-check-input" type="checkbox" value="{{todo._id}}" name="todos" id="{{todo._id}}">
        <label class="form-check-label" for="{{todo._id}}">
        {{todo.text}}
        </label>
    </div>
{{/each}}
```

## Marking todos as done

## Handling empty strings

## Handling no list items



