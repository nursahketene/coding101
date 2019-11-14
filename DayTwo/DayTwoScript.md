# Introduction

Congradulations you have completed Day one and understand the basics of internet and the history that brought us all to this moment. You have already played a little with `HTML`, `CSS`, and even `JavaScript`

Now it is time to dive deeper into Javascript and undertand the language it self.

This time we are going to learn about basic types like `Strings`, `Numbers` and `Boolean`. We are also going to learn about `loops` and how to `reuse` code. What does a `function` mean and what is a
`Class`?

So lets start...

First we need to open our `Editor`

So open up your `Visual Studio Code` and from the menu bar click `File` and `Open`

Lets `Add a new folder` and click open

Now we have an empty Folder.

## Console.log()

So Lets start with our first ever application

Lets add a new file by clicking `File` from the menu bar and selecting `New File`

Save the file by typing `CMD+S` or in Windows `CTRL+S` and give the file the name `hello_world.js`

Next lets create our first program

```javascript
console.log('HELLO WORLD')
```

save the file and lets run our programme in the terminal. To get the integrated terminal in VS Code Go to `View` -> `Terminal` from the menu bar. Once you have the terminal type the following to run your new javascript file;

```sh
node hello_world.js
```

You should have an output similar to below

```sh
node hello_world.js
Hello World
```

So what is happening here?
What is `console` and what is `log`?

`console` is a integrated keyword in javacript. It is an object and it has functions. We have talked about it a little when we were doing our first web page.

Console is generally used for debugging purposes by developers. In this case we just wanted our program to say "HELLO WORLD"

## Excersize (5 min)

Use console to log different strings or maybe even numbers.
Try to put multiple logs in the same file. See what happens.

Alright now lets add some `console.log()`

If you want to add a number
```javascript
console.log(40)
```

Let's add a string with #

```javascript
console.log("Wow. This course is amazing! #coding101")
```

And now let's add a number with decimals

```js
console.log(20.45)
```

What about multiple `console.log()´ entries

```js
console.log("You may write me down in history")
console.log("With your bitter, twisted lies,")
console.log("You may tread me in the very dirt")
console.log("But still, like dust, I'll rise.")

console.log("Maya Angelou")
```

## Arithmetic Operations

So arithmetic operations are methods we are using on a daily basis in our lifes.
Those are `Addition`, `Substraction`, `Division`, and `Multiplication`.

So let's play with them;

### Addition

```js
console.log(3 + 4); // Prints 7
```

### Substraction

```js
console.log(5 - 1); // Prints 4
```

### Multiplication

```js
console.log(4 * 2); // Prints 8
```

### Division

```js
console.log(9 / 3); // Prints 3
```


But arithmetic operators are not only for numbers. We can use `Addition` operator for string concatenation. That means we can merge two string with each other.

```js
console.log("hello" + " friend") // Prints hellofriend
```

## Excersize (5 min)

* Inside console.log() add 5 to your age

* Inside console.log() remove 1968 from the current year

* Inside the console.log() divide 128 by 39

* Inside the console.log() multiply 0.5 with 49

* Inside the console.log() Concatenate "I love you" with 2000. Don't for get to add the space!

* OPTIONAL: Add 5 to your current age remove that from the current year and divide the result by 94.4 inside the console.log()


## Variables

Ok so we have been working with numbers and strings now (we are going to look in to them more in detail) but lets take a look at `variables`

So far we have just printing things using console. But sometimes we might want to save that information somewhere.
That something is called variables.

In programming, a variable is a container for a value. You can think of variables as little containers for information that live in a computer’s memory. Information stored in variables, such as a username, account number, or even personalized greeting can then be found in memory.

Variables also provide a way of labeling data with a descriptive name, so our programs can be understood more clearly by the reader and ourselves.

In short, variables label and store data in memory. There are only a few things you can do with variables:

* Create a variable with a descriptive name.
* Store or update information stored in a variable.
* Reference or “get” information stored in a variable.

There are three variable types, `var`, `let`, `const`.

For the purpose of simplicity, we are just going to focus on variable type `var`


So in your editor lets open a new file called variable.js
and type the following

```js
var name = 'Nur'
console.log(name)
```

Now run the file on your terminal by typeing

```bash
node variable.js
```

>> Explain what is happening here!

There are a few general rules for naming variables:

* Variables names can not start with numbers
* Variables names are case sensitive so myName and name are different
* Variable names can not be the same as keywords, like `new`, or `if`


## Excersize (5 min)

* Declare a variable favoriteFood and assign your favorite food to it and print the value
* Declare a variable numberOfPlates and assigs 12 to it and print the value.

Now lets create some more variable and add arithmetic to it

```js
var susanAge = 35
var johnAge = 32
var totalAge = susanAge + johnAge
console.log(susanAge)
console.log(johnAge)
console.log(totalAge)
```

Now run the JavaScript file with

```bash
node variable.js
```

Lets talk about boolean

Booleans are binary values. They are `true` or `false`

They are quite useful when weare going to work on conditionals. The way we are going to declare it as follows;

```js
var isRedFlag = true
console.log(isRedFlag)
```

Run the JavaScrit file in the terminal

```bash
node variable.js
```

```js
var isGreenFlag = false
console.log(isGreenFlag)
```

Run the JavaScript file in the terminal
```bash
node variable.js
```

Now lets try to reassign a variable value

```js
var isGreenFlag = false
console.log(isGreenFlag)
var isGreeFlag = true
console.log(isGreenFlag)
```

As you can see here we have reassigned the a value to the variable.


## Excersize (10 min)
* Create a variable `age` and assign a 22 to it. Console.log after the assignment
* Add 8 to the `age` variable. Console.log after the addition
* Now create a new variable called `height` and assign 185. Console.log both the age and height variables
* Create a new variable called `total` and assign the total value of `height` and `age`
* Increment the value of age by one. Console.log
* Decrement the value of the height by 10. Console.log

Alright now lets talk about String concatenation with variables

In previous exercises, we assigned strings to variables. Now, let’s go over how to connect, or concatenate, strings in variables.

```js
var firstName = "Nur"
var lastName = "Ketene"
var fullName = firstName + " " + lastName
console.log(fullName)
```

Run the the code in terminal
```bash
node variable.js
```

## Excersize (3 min)

* Create variable favoriteAnimal and assign to it your favorite animal
* Now in console.log() concatenate "My Favorite Animal is" with your favoriteAnimal variable

## Arrays

Ok so lets say that you have a bag and in that bag you have a bunch of fruits. You have a banana, an apple, an orange, and a watermelon.

So you can of course create an array for each of those but that would be too many variables. But what if we can store all of those in one special variable called `array`

```js
var fruits = ['banana', 'apple', 'orange', 'watermelon']
```

so now when you log `fruts` you will get the contents of the fruits array as a result.

```bash
node arrays.js
```

so what is an array

_An array can be defined as an ordered collection of items indexed by contiguous integers._

Now this is important because arrays are indexed that means we can reach each array value by their indexes

so if I wanted to get the orange from the array;

```js
console.log(fruits[2])
```

So what happened. Why did we write 2 when we wanted to get the orange. Isn't orange in the third place?


Array indexes start from `0` so the first element index is `0` and second element index is `1` and the third element index is `2` and so on.

Ok now lets try another one. Lets say I want to have `watermelon`

```js
console.log(fruits[3])
```

now I got the watermelon as a result.

Now we have talked about properties before.

So let's say I want to get how many element there are in the `fruits` array

```js
console.log(fruits.length)
```

Nice So I know that there 4 elements in the fruits array.

Let's do other stuff.

Let's try to add a new element to the fruits array. I want to add `strawberry`

```js
fruits.push('strawberry')
console.log(fruits)
```

Now we have added strawberry as the last element. But what if I want to remove an element from my fruits array. Lets say that I ate the `banana`

```js
fruits.shift()
console.log(fruits)
```

Oh my we have removed the `banana` from the begining of the array.

## Excercise (30 min)

* Add number 22 and 45 to fruits array. log frutis
* Add a new fruit to fruits array at index 2. log fruits
* Remove index 4 from fruits array. log fruits
* log index 2 of fruits array
* Change index 1 item to `Mango`
* Log the first three elements of the fruits array

## Conditionals & Operators

We have talked about booleans for a bit. About true and false. So now we are going to use them more but also introduce operators

Lets start with comparing items with checking if they are equal to one another.

so

```js
console.log("Nur" === "Nur")
```

This will return true. So we know that "Nur" is equal to "Nur". What about numbers. Can we compare them?

```js
console.log(1 === 1)
```

Yeah that seems to work as well.

So how would we check if a value is not equal to another value?

```js
console.log(1 != 2)
```

Well that works as well.


Alright lets try something a little bit more complicated

What if we check an array lenght with a word length?


```js
var fruits = ['banana', 'apple', 'orange', 'watermelon']
var name = "Tomi"
console.log(fruits.length === name.length)
```

Ok now lets check for if a value is bigger then the other?

```js
console.log(8 > 3)
```

That is correct

What if we check for smaller than

```js
console.log(2 < 5)
```

## Exercise (5 min)

* Compare the fruits array with 5 with smaller than or equal to operator and log the result
* Compare the fruits array with 5 with greater than or equal to operator and log the result


Alright lets move to conditionals

We use the if statements when we want to run the code only if a certain criteria is met

```js
var isGreenLight = false
if (isGreenLight === true) {
    console.log('I am walking')
}
```

```js
var isGreenLight = true
if (isGreenLight === true) {
    console.log('I am walking')
}
```

Or you can wite it with a short hand

```js
var isGreenLight = false
if (isGreenLight) {
    console.log('I am walking')
}
```

Eat a banana if there are 5 or more fruits.

So the way you would write in code would be

```js
if (fruits.length >= 5) {
    console.log('I am eating a banana');
}
```

So lets say that I want to eat a fruit if there are any fruits in the array

```js
if (fruits.length) {
    console.log('I am eating a banana');
}
```

Ok next lets try to complicate it a little.

I want to eat bana if the fruit is banana. Otherwise I don't want to eat any!


```js
var fruit = 'apple'
if (fruit === 'banana') {
    console.log('I am eating a banana')
} else {
    console.log("I don't want to eat a " + fruit)
}
```

So First we checked for the fruit if it is a banana. When we realized it is not a banana we jumpted to the second condition and said we don't want to eat the fruit.

Ok let's make it a little bit more complicated!

I want to eat a banana. If that doesn't exist I want to check if the fruit is apple. If it is I want to eat it otherwise I don't want to eat any.
```js
var fruit = 'apple'

if (fruit === 'banana') {
    console.log('I am eating the banana')
} else if (fruit === 'apple') {
    console.log('I am eating an apple even though I wanted a banana');
} else {
    console.log('I do not feel like eating any fruits.')
}
```

So we have added two conditions here. First we checked for the banana and then we have checked for the apple. The third condition will only run if the first condition is not satisfied.

>> We are here

## Excersize (15 min)

* Use an if statement to check if fruits array includes 'banana' (google)
* Check for the fruit in one if statement with an `AND` operator

## Loops

Alright now lets say that we have a cars array;

```js
var cars = ["BMW", "Volvo", "Saab", "Ford", "Fiat", "Audi"];
```

We can go through the array one by one and print the arrays in it

```js
console.log(cars[0])
console.log(cars[1])
console.log(cars[2])
console.log(cars[3])
console.log(cars[4])
console.log(cars[5])
```

This would work but it is repetitive and also very in efficient. What if we have 100 cars or 1000 cars. We have to print them once by one. It would take forever.

So becourse of this we have loops.

There are several loops in javascript but we are going to focus only on two of them. `for` and `while` loops.

The difference between them

For loop will run until it reaches the end statement

While loops on the other hand are going to run until the condition is met.

Let's start with the for loop

I want to print all of the cars in the cars array

```js
var cars = ["BMW", "Volvo", "Saab", "Ford", "Fiat", "Audi"];
for (i = 0; i < cars.length; i++) {
    console.log(cars[i])
}
```

Now go to the terminal and run the file.

You should see the cars listed.

So what happened here. What is `i` and i++ and what is going on?

>> Explain what happened

So ok this is For loops. Lets try a bit more.


I want to say hello world 5 times and print the number next to it

```js
for (i = 0; i < 1; i++) {
    console.log('Hello world' + i)
}
```

## Excersize (30 min)
* Create a for loop for the cars array and only print if the car is a "Audi"
* Create a for loop to print numbers between 5 and 10

Lets do a while loop now.

For loops were for running through an array until you reach the last element. But While loops are for satisfying a condition.

Lets say that I want to print how many cards I have until I collect 10 cards

so it would be

```js
var numberOfCards = 0

while (numberOfCards < 10) {
    console.log(numberOfCards)
    numberOfCards++
}
```

So here we are checking if the number of the cards is still smaller than 10. If it is not smaller than 10 we are going to continue the loop. If you don't add the increment at the end there it will just run foreever.

But the console only loged until 9. What is the value of the `numberOfCards`?

## Exersize (15 min)
* Create a while loop to print numbers from 5 to 10
* Create a while loop to print only the 3rd car in the index


## Functions

A JavaScript function is a block of code designed to perform a particular task.

A JavaScript function is executed when "something" invokes it (calls it).

So lets look at functions

```js
function sayHelloTimes(multiplier) {
    let index = 0
    while (index < multiplier) {
        console.log('HELLO DEAR')
        index++
    }
}
```

So as we have basic understanding of the functions let's play a little with the functions
What happens about the variables

```js
function myFunction() {
    var index = 0
    console.log(index)
}

console.log(index)
```

