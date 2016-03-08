# JavaScript in class exercise

Welcome to programming. Up until now you have been dealing exclusively with markup languages and stylesheets. JavaScript is a full fledged programming language. While it was originally designed to augment webpages, it is used in a variety of ways to on and off the web. In fact Brackets, the text editor we have been using is written in JavaScript.

##Part 1

This first part can be done completely in the **JavaScript console** inside any browser, on any webpage.

### Statements
* Enter <code>alert("Hello World!");</code> into the JavaScript console and hit return.
* Enter <code>console.log("Hello World!");</code> into the console.
* Enter any number. What happens?
* Enter <code>2 + 4</code>. What happens?
* Try some other simple equations and see what happens.

### Variables

Variables are what make programs flexible tools. If we could only enter numbers directly we couldn't change what a program does with different input.

Lets create our first variable.

* Write the following in the console. <code>var x = 3;</code> This creates the variable x and assigns it the value 3.
* Enter <code>x</code> and hit return. You should see its value print out.
* Create another variable <code>y</code>. Assign it the value of <code>x</code>.
* Check y's value.
* Assign the variable <code>x</code> the value 5. 
* What is the value of <code>x</code> and <code>y</code> now? Why?
* Create a variable <code>foo</code> assign it the String "Hello world ".
* Create a variable <code>bar</code> assign it the String "5".

### Operators

* Enter <code>var sum = x + y</code>. We can create new variables and assign them the results of operations like this.
* Subtract <code>x</code> and <code>y</code> and assign it to the variable <code>difference</code>.
* Multiply <code>5</code> and <code>y</code> and assign it to the variable <code>product</code>.
* Divide <code>9</code> and <code>4</code> and assign it to the variable <code>quotient</code>.
* Enter <code>var result = 9 % 4</code>.
* Can you figure out what the <code>%</code> operator(also know as modulo) does? *HINT: It has something to do with division.*

#### Strings
* Add <code>foo</code> and <code>bar</code> and assign to the variable <code>combined</code>. What is the value of <code>combined</code>?
* Add <code>foo</code> and <code>x</code> and assign to <code>d</code>. What is the value of <code>d</code>?
* Add <code>x</code> and <code>foo</code> and assign to <code>e</code>. What is the value of <code>e</code>?
* Can you explain what happened?
* Add <code><code>x</code></code> and <code>bar</code> and assign to <code>f</code>.
* Add <code>x</code> and Number(<code>bar</code>) and assign to <code>g</code>.
* Why are <code>f</code> and <code>g</code> different?
* Enter <code>var h = x + Number(foo)</code>. What is the value of <code>h</code>?

#### Other operators

* What is the current value of <code>x</code>?
* Enter <code>w = x++</code>
* What are the values of <code>x</code> and <code>w</code>? What happened?
* Enter <code>v = ++x</code>
* What are the values of <code>x</code> and <code>v</code>? What happened?
* Enter <code>x += 10;</code> What is the value of <code>x</code> now?

## Part II

Now lets work with JavaScript from within an HTML document. Open the <code>index.html</code> document included in this repository. It should contain the basic tags we have seen before. 

Lets start by recreating our Hello world example from above. 

First we need a place for our JavaScript in the document. Normally you want to load the JavaScript last, after the CSS and most of the HTML has loaded. This way viewers will see the main content first. 

We will place ours just before the closing <code>&lt;/body</code> tag. Enter the following:

<pre><code>
&lt;script&gt;

alert("Hello world");

&lt;/script&gt;
</code></pre>

Normally we will place our JavaScript in a separate file, but today we will just embed it in the HTML document. We will be placing all our code today between these script tags. Open the page in the browser, or if you already have reload it.

## Conditionals

Replace the contents of the <code>&lt;script&gt;</code> tag and replace it with the following:

<pre><code>
var myNumber = 3;

if ( myNumber == 3 ) {
  alert("Its true!");
}
</code></pre>

This statement evaluates whether myNumber is equals 3. If it is we popup an alert message. Note that there are two equal signs between myNumber and 3.

Before we go on lets switch the code to the following:

<pre><code>
var myNumber = 3;

if ( myNumber == 3 ) {
  console.log("Its true!");
} else {
  console.log("Its false");
}
</code></pre>

Sending messages to the console is a little less annoying than an alert window. The else clause allows to run different code if the answer is false. Now make sure the JavaScript console is open and reload the page.

Lets try out some different conditionals statements. Replace the if statement with the following. Be sure to reload the page after each.

* <code>if( 5 &gt; 2 )</code>
* <code>if( 5 &lt; 2 )</code>
* <code>if( myNumber &gt;= 0 )</code>
* <code>if( myNumber == 3 )</code>
* <code>if( myNumber = 6 )</code>
* <code>if( myNumber != 7 )</code>
* <code>if( false || myNumber &gt; 2 )</code>
* <code>if( false && myNumber &gt; 2 )</code>
* <code>if( myNumber &gt; 3 && myNumber &lt; 8 )</code>

## Loops

<pre><code>
  var index = 0;
  
  while( index &lt; 10 ) {
    console.log(index);
    index = index + 1;
  }
</code></pre>

* What does this code do?
* Change it to include the number 10.
* Change it to list just even numbers.
* How would you change it to list from 4 to 20?

<pre><code>
  for(var index = 0; index &lt; 10; index++) {
    console.log(index);
  }
</code></pre>

* What does this code do?
* Change it to include the number 10.
* Change it to list just even numbers.
* How would you change it to list from 4 to 20?

## Arrays and objects

Loops are much more powerful when you add arrays.

<pre><code>
  var fruit = ["Apples", "Bananas", "Oranges", "Kiwi"];
 
  for(var index = 0; index &lt; 4; index++) {
    console.log(fruit[index]);
  }
</code></pre>

* What happens when you run this code?
* What happens when you change <code>index &lt; 4</code> to <code>index &lt; 10</code>?
* You can use fruit.length to see how many values fruit holds. Plug it in where you now have the value 10. Run the code again.

<pre><code>
  var squares = [];
 
  for(var index = 0; index &lt; fruit.length; index++) {
    squares[index] = index * index;
  }
</code></pre>

* What happens when you run this code?

## Functions

<pre><code>
  function hello(name) {
    console.log("Hello " + name);
  }
  
  hello("Fred");
</code></pre>

* What does this code do?

<pre><code>
  function hello(name) {
    return ("Hello " + name);
  }
  
  console.log( hello("Fred") );
</code></pre>






## DOM

## Events



