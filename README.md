# JavaScript in class exercise

Welcome to programming. Up until now you have been dealing exclusively with markup languages and stylesheets. JavaScript is a full fledged programming language. While it was originally designed to augment webpages and continues in this role. It is used a variety of ways to on and off the web. In fact Brackets, the text editor we have been using is written in JavaScript.

#Part 1

This first part can be done completely in the **JavaScript console** inside any browser, on any webpage.

### Statements
* Enter <code>alert("Hello World!");</code> into the JavaScript console.
* Enter <code>console.log("Hello World!");</code> into the console.
* Enter any number. What happens?
* Enter

### Variables

* Create a variable called <code>x</code>. Assign it the value 3.
* Create another variable <code>y</code>. Assign it the value of "x".
* Assign the variable <code>x</code> the value 5. 
* What is the value of <code>x</code> and <code>y</code> now? Why?
* Create a variable <code>foo</code> assign it the String "Hello world ".
* Create a variable <code>bar</code> assign it the String "5".

### Operators

* Add <code>x</code> and <code>y</code> and assign it to a variable "sum".
* Subtract <code>x</code> and <code>y</code> and assign it to the variable "difference".
* Multiply <code>x</code> and <code>y</code> and assign it to the variable "produce".
* Divide <code>x</code> and <code>y</code> and assign it to the variable "quotient".
* Replace the division operator with the <code>%</code> and assign it to the variable <code>result</code>.
* What does <code>%</code> operator(also know as modulo) do?
* Add <code>foo</code> and <code>bar</code> and assign to the variable <code>concat</code>.
* Add <code>foo</code> and <code>x</code> and assign to <code>d</code>.
* Add <code>x</code> + <code>foo</code> and assign to <code>e</code>.
* Can you explain what happened?
* Add <code><code>x</code></code> and <code>bar</code> and assign to <code>f</code>.
* Add <code>x</code> and Number(<code>bar</code>) and assign to <code>g</code>.
* Why are <code>f </code>and <code>g</code> different?
* Add <code>x</code> + Number(<code>foo</code>) and assign to <code>h</code>. What is the result?

### Other operators

* What is the current value of <code>x</code>?
* Enter <code>w = x++</code>
* What are the values of <code>x</code> and <code>w</code>? What happened?
* Enter <code>v = ++x</code>
* What are the values of <code>x</code> and <code>v</code>? What happened?
* Enter <code>x += 10</code>; What is the value of <code>x</code> now?

## Part II

For this part it is easier if we work with a file. We will be moving back between the text editor and the browser to test our results. You will need the JavaScript console open in the Browser to see some results and any errors in your code.

## Comments

## Conditionals

<pre><code>
var myNumber = 3;

if ( true ) {
  alert("Its true!");
} else {
  alert("Its false");
}
</code></pre>

What are the results if you change the if statement as follows.

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



