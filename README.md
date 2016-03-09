# JavaScript in class exercise

Welcome to programming. Up until now you have been dealing exclusively with markup languages and stylesheets. JavaScript is a full fledged programming language. While it was originally designed to augment webpages, it is used in a variety of ways to on and off the web. In fact Brackets, the text editor we have been using is written in JavaScript.

##Part 1

This first part can be done completely in the **JavaScript console** inside any browser, on any webpage.

### Statements
* Enter `alert("Hello World!");` into the JavaScript console and hit return.
* Enter any number. What happens?
* Enter `2 + 4`. What happens?
* Try some other simple math equations and see what happens.
* Here is something more complex. We will talk about the details later. `document.getElementsByTagName("h1")[0].textContent`. For now just see what it does. Don't worry if you get an error.

### Variables

Variables are what make programs flexible tools. If we could only enter numbers directly we couldn't change what a program does with different input.

Lets create our first variable.

* Write the following in the console. `var x = 3;` This creates the variable x and assigns it the value 3.
* Enter `x` and hit return. You should see its value print out.
* Create another variable `y`. Assign it the value of `x`.
* Check y's value.
* Assign the variable `x` the value 5. 
* What is the value of `x` and `y` now? Why?
* Create a variable `foo` assign it the string "Hello world ".
* Create a variable `bar` assign it the string "5".

### Operators

* Enter `var sum = x + y`. We can create new variables and assign them the results of operations like this.
* Subtract `x` and `y` and assign it to the variable `difference`.
* Multiply `5` and `y` and assign it to the variable `product`.
* Divide `9` and `4` and assign it to the variable `quotient`.
* Enter `var result = 9 % 4`.
* Can you figure out what the `%` operator(also know as modulo) does? *HINT: It has something to do with division.*

#### Strings
* Add `foo` and `bar` and assign to the variable `combined`. What is the value of `combined`?
* Add `foo` and `x` and assign to `d`. What is the value of `d`?
* Add `x` and `foo` and assign to `e`. What is the value of `e`?
* Can you explain what happened?
* Add `x` and `bar` and assign to `f`.
* Add `x` and Number(`bar`) and assign to `g`.
* Why are `f` and `g` different?
* Enter `var h = x + Number(foo)`. What is the value of `h`?

#### Other operators

* What is the current value of `x`?
* Enter `w = x++`
* What are the values of `x` and `w`? What happened?
* Enter `v = ++x`
* What are the values of `x` and `v`? What happened?
* Enter `x += 10;` What is the value of `x` now?

## Part II

Now lets work with JavaScript from within an HTML document. Open the `index.html` document included in this repository. It should contain the basic tags we have seen before. 

Lets start by recreating our Hello world example from above. 

First we need a place for our JavaScript in the document. Normally you want to load the JavaScript last, after the CSS and most of the HTML has loaded. This way viewers will see the main content first. 

We will place ours just before the closing `</body>` tag. Enter the following:

```javascript
<script>

alert("Hello world");

</script>
```

Normally we will place our JavaScript in a separate file, but today we will just embed it in the HTML document. We will be placing all our code today between these script tags. Open the page in the browser, or if you already have reload it.

## Conditionals

Conditionals allow us to branch our code. Doing one thing if something is true and another if it is false.

Replace the contents of the `<script>` tag with the following:

```javascript
var myNumber = 3;

if ( myNumber == 3 ) {
  alert("Its true!");
}
```

This statement evaluates whether myNumber equals 3, if it does, we popup an alert message. Note that there are two equal signs between myNumber and 3.

Before we go on lets switch the code to the following:

```javascript
var myNumber = 3;

if ( myNumber == 3 ) {
  console.log("Its true!");
} else {
  console.log("Its false");
}
```

Sending messages to the console is a little less annoying than an alert window. The else clause allows to run different code if the answer is false. Now make sure the JavaScript console is open and reload the page.

Lets try out some different conditionals statements. Replace the if statement with the following. Be sure to reload the page after each. Make sure you can explain why you got each result.

* `if( 5 > 2 )`
* `if( 5 < 2 )`
* `if( myNumber >= 0 )` Use `>=` or `<=` to test greater/less than or equal.
* `if( myNumber == 3 )` Use `==` to test if two things are equal.
* `if( myNumber != 3 )` Use `!=` to test if two things are NOT equal. 
* `if( myNumber = 21 )` Why is this true?

You can use `&&` as a logical 'and' and `||` as a logical 'or'.

* `if( false || myNumber > 2 )`
* `if( false && myNumber > 2 )`
* Can you write an if statement to check if myNumber is between 3 and 10?

## Loops

Loops keep us from writing the same code over and over again. Replace the contents of the `<script>` tag with the following:

```javascript
var index = 0;

while( index < 10 ) {
  console.log(index);
  index = index + 1;
}
```

* What does this code do?
* Change it to include the number 10.
* Change it to list just even numbers.
* How would you change it to list from 4 to 20?

```javascript
  for(var index = 0; index < 10; index++) {
    console.log(index);
  }
```

* What does this code do?
* Change it to include the number 10.
* Change it to list just even numbers.
* How would you change it to list from 4 to 20?
* Can you write a for loop that multiplies all the numbers between 1 and 10 and save the results in a variable?

## Arrays and objects

 Arrays are a list of variables that are accessed via an index. They can contain any value a variable can. Here is an array lists the names of fruits

```javascript
  var fruit = ["Apples", "Bananas", "Oranges", "Kiwi"];
```

To access an element of an array we use the name followed by square brackets containing the index of the element we want. `fruit[0]` would access the first element whose value is "Apples". Arrays always start at zero.

Loops are much more powerful when you add arrays. 

```javascript

  for(var index = 0; index < 4; index++) {
    console.log(fruit[index]);
  }
  
```

* What happens when you run this code?
* What happens when you change `index < 4` to `index < 10`?
* You can use `fruit.length` to see how many values the array `fruit` holds. Plug it in where you now have the value 10. Run the code again.
* Create a new array with a list of values of your choosing.

```javascript
  var squares = [];
 
  for(var index = 0; index < fruit.length; index++) {
    squares[index] = index * index;
  }
```

Objects like arrays let you store more than one value in a single variable but can allow you to name those values and even add additional functionality to the variable that we will talk about later.

Instead of this:

```javascript
  var artistName = "Barry";
  var artistMedium = "Painting";
  var artistAge = 32;
```

I could create an object that holds all of that information.

```javascript
  var artist = { name: "Barry", medium: "Painting", age: 32 };
```  

You can access the values of the object by using square brackets(similar to arrays) or using dot notation. We will primarily use dot notation.

```javascript
artist["name"]

artist.name
```
You will see dot notation frequently. It can be used to refer to an objects properties (variables) or its methods (functions that run code).

## Functions

Functions make it easier to deal with code that you might use again and again.

```javascript
  function hello(name) {
    console.log("Hello " + name);
  }
  
  hello("Fred");
```

* What does this code do?

Functions can do more than just save chunks of code. They can return values to be used else where.

```javascript
  function square( x ) {
    return x * x;
  }
```

* Write your own function that returns a value based on input...

## DOM

## Events



