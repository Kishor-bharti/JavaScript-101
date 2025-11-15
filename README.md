# JavaScript 101;

> console.log("Let's Begin!");
BY BroCode [watch](https://www.youtube.com/watch?v=lfmg-EJ8gm4&t=4618s)

***Watch the above video and follow through these notes for better understanding😎🚀🔥***

## Table of Content

[JavaScript tutorial for beginners 🌐](#javascript-tutorial-for-beginners)
[Variables 📦](#variables)
[Arithmetic operators ➕](#arithmetic-operators)
[Accept user input 💬](#accept-user-input)
[Type conversion 💱](#type-conversion)
[Constants 🚫](#constants)
[⭐ Counter program 🔢](#counter-program)
[Math object 🧮](#math-object)
[Random number generator ⁉](#random-number-generator)
[If statements 🤔](#if-statements)
[Checked property ✅](#checked-property)
[Ternary operator ❓](#ternary-operator)
[Switches 💡](#switches)
[String methods 🧵](#string-methods)
[String slicing ✂️](#string-slicing)
[Method chaining ⛓](#method-chaining)
[Logical operators ❗](#logical-operators)
[Strict equality 🟰](#strict-equality)
[While loops 🔁](#while-loops)
[For loops 🔂](#for-loops)
[⭐ Number guessing game ↕](#number-guessing-game)
[Functions 📞](#functions)
[Variable scope 🏠](#variable-scope)
[⭐ Temperature conversion program 🌡️](#temperature-conversion-program)
[Arrays 🗃](#arrays)
[Spread operator 📖](#spread-operator)
[Rest parameters 🗄](#rest-parameters)
[⭐ Dice Roller program 🎲](#dice-roller-program)
[⭐ Random password generator 🔑](#random-password-generator)
[Callbacks 🤙](#callbacks)
[forEach() ➿](#foreach)
[map() 🗺](#map)
[filter() 🚰](#filter)
[reduce() ♻](#reduce)
[Function expressions 🐣](#function-expressions)
[Arrow functions 🎯](#arrow-functions)
[JavaScript Objects 🧍](#javascript-objects)
[What is THIS 👈](#what-is-this)
[Constructors 🛠](#constructors)
[Classes 🏭](#classes)
[STATIC keyword ⚡](#static-keyword)
[Inheritance 🐇](#inheritance)
[SUPER keyword 🦸‍♂️](#super-keyword)
[Getters & Setters 📐](#getters--setters)
[Destructuring 💥](#destructuring)
[Nested objects 📫](#nested-objects)
[Arrays of objects 🍎](#arrays-of-objects)
[Sorting 🗃](#sorting)
[Shuffle an array 🔀](#shuffle-an-array)
[Dates 📅](#dates)
[Closures 🔒](#closures)
[setTimeout() ⏰](#settimeout)
[⭐ Digital Clock program 🕐](#digital-clock-program)
[⭐ Stopwatch program ⏱](#stopwatch-program)
[ES6 Modules 🚢](#es6-modules)
[Asynchronous code 💤](#asynchronous-code)
[Error handling ⚠](#error-handling)
[⭐ Calculator program 🖩](#calculator-program)
[What is the DOM? 🌳](#what-is-the-dom)
[Element selectors 📑](#element-selectors)
[DOM navigation 🧭](#dom-navigation)
[Add & change HTML 🛠️](#add--change-html)
[Mouse events 🖱](#mouse-events)
[Key events ⌨](#key-events)
[Hide/show HTML 🖼](#hideshow-html)
[NodeLists 📃](#nodelists)
[classList 🧾](#classlist)
[⭐ Rock Paper Scissors 👊](#rock-paper-scissors)
[⭐ Image Slider 🖼️](#image-slider)
[Callback Hell? 🔥](#callback-hell)
[Promises 🤞](#promises)
[Async/Await ⏳](#asyncawait)
[JSON files 📄](#json-files)
[Fetch data from an API ↩️](#fetch-data-from-an-api)
[⭐ Weather App project ☀️](#weather-app-project)


## Starting...
* JavaScript is a programming language, used to create Dynamic and Interactive web pages!
* Js runs on web browsers
* By using JS, we respond to user actions and transform user input whenever somebody interacts with our site (eg. Calculator app!)

`create a folder named website and html, css and js files for structure , styles and actions!`

```html
<link rel="stylesheet" href="style.css">
<script src="index.js"></script>
<p>Don't forget to use these two tags!</p>
```
* We put our JavaScript tag at the bottom of the body tag just to make sure atleast our html gets render in case of any error in the JS code!

```js
console.log(`This is a template literal aka backtick`);
console.log("Hello");

window.alert("This is an alert");
window.alert(`I like Pizza`);

// comment
document.getElementById("myH1").textContent = `Hello`;
document.getElementById("myP").textContent = `I like Pizza!`;
```
* When working with basic output , we use console.log()
*  To create an alert we can use window.alert
*  To change the text content of an HTML element , you first have to select that element then change the text content and then set it equal to some text


## Variables 📦

* A container that stores a value. Behaves as if it were the value it contains.
1. declaration     let x;
2. assignment    x = 100;

* Variable names should be unique!
```js
// Eg.,
let x;
let x;
// This will raise a SyntaxError: Identifier 'x' hass already been declared!
```

* You can declare and assign a variable together or in two steps if it requires user input
* The variable declaration should be discriptive (that means meaningful!)
```js
let age = 25;
let price = 10.99;
let gpa = 2.1;

console.log(`you are ${age} years old`);
console.log(`The price is $${price}`);
console.log(`Your gpa is: ${gpa});
// you can also display the datatype of a variable using:
console.log(typeof gpa);

// lets use other datatypes!
```

```js
// Strings: Strings is a series of characters that can contain numbers but we cannot use these numbers for any sort of maths 

let firstName = "Bro"; // we can use single quotes or template literals
let favoriteFood = "pizza";

console.log(typeof firstName); 
console.log(`Your name is ${firstName}`);
console.log(`You like ${favoriteFood}`);

// Boolean: is either true or false and they are typically used as a sort of flag

let online = false;
let forSale = true;
let isStudent = true;

console.log(`Bro is online: ${online}`);
console.log(`Is this car for sale: ${forSale}`);
console.log(`Enrolled: ${isStudent}`); // Enrolled: true
// Typically, we use them with if statements!

// Now, we will display this in the html element!
```

```html
HTML
<p id="p1"></p>
<p id="p2"></p>
<p id="p3"></p>

```

```js
let fullName = "Bro Code";
let age = 25;
let isStudent = false;

// To change the text content of an html element we'll type document (to get the document of our webpage):
document.getElementById("p1").textContent = fullName;
document.getElementById("p1").textContent = age;
document.getElementById("p1").textContent = isStudent;

//we can also use a template literal :
document.getElementById("p1").textContent = `Your namne is ${fullName}`;
```

## Arithmetic operators ➕

arithmethic operators = operands (values, variables, etc.)
                                                operators (+ - * /)
                                                ex. 11 = x + 5;

```js

let students = 30;

students = students + 1; // and soo on...
// using modules operator, it is recom. to use a separate variable!

// We can also use Augmented assignment operators! which is a short hand for it!
students += 1;
students -= 1;
students *= 2;
students /= 2;
students **= 2;
students %=  2;

// % can be useful to determine if a number is odd or even!

// Increment or Decrement Operators:
students++;
students--;



console.log(students);
```

Operators Precedence(VVI):

1. Parenthesis ()
2. exponents
3. multiplication & division & modulo 
4. addition & subtraction

```js
let result = 1 + 2 * 3 + 4 ** 2; // 23
let result = 12 % 5 + 8 /2;
let result  = 6/2 ** (2+5);
```

> how about making a program using stack for it??

## Accept user input 💬

How to accept user input
1. EASY WAY = window prompt
2. PROFESSIONAL WAY = HTML textbox


```js
// Easy way:

let username;

username = window.prompt("What's your username?");
console.log(username);
```

```html
<h1>Welcome</h1>

<label>username: </label>
<input id="myText"><br><br>
<button id="mySubmit">submit</button>
```
```js
let username;

document.getElementById("mySubmit").onclick = function(){
    username = document.getElementById("myText").value;
    console.log(username);
}

// Now, check this runs perfectly! 
// Now, we'll change the h1 text using this!
// Remove console.log from here and add id="myH1" along with this:

document.getElementById("mySubmit").onclick = function(){
    username = document.getElementById("myText").value;
    document.getElementById("myH1").textContent = `Hello ${username}`
}
```

## Type conversion 💱

type conversion = change the datatype of a value to another (strings , numbers, booleans)

* Why we even need this? Sometimes , we need to do some calculations on users input (which is a string by default ig!)
* eg.,
 
```js
let age = window.prompt("How old are you?");

age+=1;
console.log(age); //Output: 251 (we're doing string concatination here by default!
// To make it work, we'll need to typecast it first as:
age = Number(age);

// Along with the age variable, we can display the age type as:
console.log(age, typeof age); // 26 'number' prev, it'd be 251 string
```

```js
let x = "pizza";
let y = "pizza";
let z = "pizza";

x = Number(x);
y = String(y);
z = Boolean(z);

console.log(x, typeof x);
console.log(y, typeof y);
console.log(z, typeof z);
```

```outputs
NaN 'number'
pizza string
true 'boolean'
```

* If you convert a string to a number , the value will be a NaN, i.e, Not a number!
* As long as there's some value , the boolean convert of it will be true!
* Try change the values "pizza" with "0" this time!

```outputs
0 'number'
0 string
true 'boolean'
```

* Try change the values "0" with "" this time!

```outputs
0 'number'
string
false 'boolean'
```

* What if for variables declared but not assigned!

```outputs
NaN 'number'
undefined string
false 'boolean'
```

## Constants 🚫

* const = a variable that can't be changed once is assigned!

```js
// Let first do it using let!
let pi  = 3.14159;
let radius;
let circumference;

radius = window.prompt('Enter the radius of a circle');
radius = Number(radius);

circumference = 2 * pi * radius;
console.log(circumference);
// Works just fine!
```

* so, why do we use const? You may accidently or somebody else may maliciously change the value of a variable, so that the program does behave as intended!
* so, change the let to const above and it is a good practice to make all of the letters in the const variable name uppercase. so, it becomes `const PI = 3.14159;`
* BRO FROM THE FUTURE: capitalizing your constants is usually only done with primitive data types such as numbers & booleans, reference data types such as strings don't normally follow this convention you'll see this in the next few upcoming videos, PI is a number thats why uppercase, if it was a string then we wouldn't! 
* If we, now , tryna change it , it will raise a TypeError: Assignment to constant variable.

* Now, within our web page we will accept some user input via a text box (we'll right the same program)

```html
<h1 id="myH1">Enter the radius of a circle: </h1>
<label>radius:</label>
<input type="text" id="myText"><br><br>
<button id="mySubmit">submit</button>

```

```js

const PI  = 3.14159;
let radius;
let circumference;

document.getElementById("mySubmit").onclick = function(){
    radius = document.getElementById("myText").value;
    radius = Number(radius);
    circumference = 2 * PI * radius;
    //make an h3 tag
    document.getElementById("myH3").textContent = circumference+ "cm";
}
```

## Counter program 🔢

*first, we'll create the html file, then style it, and then add functionalities to it!

```html
<body>
    <lable id="countLabel">0</label><br>
    <div id="btnContainer">
        <button id="decreaseBtn" class="butons">decrease</button>
        <button id="resetBtn" class="butons">reset</button>
        <button id="increaseBtn class="butons">increase</button>  
    </div>
</body>
```

```css
#countLabel{
    display: block;
    text-align: center;
    font-size: 10em;
    font-family: Helvetica;
}
#btnContainer{
    text-align: center;
}
.buttons{
    padding: 10px 20px;
    font-size: 1.5em; -- Translates to 150%
    color: white;
    background-color: hsl(214, 100%, 74%);
    border-radius: 5px;
    cursor: pointer;
    transition: background-color 0.25s;
}
.buttons:hover{
    background-color: hsl(214, 100%, 56%);
}
```

* Bro says he'll individually assign all of these buttons so that each is stored within a constant

```js
const decreaseBtn = document.getElementById("decreaseBtn");
const resetBtn = document.getElementById("resetBtn");
const increaseBtn = document.getElementById("increaseBtn");
const countLabel = document.getElementById("countLabel");

let count = 0; // we'll be reassigning count we'll be incrementing and decrementing count!
// With our HTML elements, we do not plan on reassigning them so we can set them as constants
// Now , we need three functions (for each decrease, reset and increase)

increaseBtn.onclick = function(){
    count++;
    countLabel.textContent = count;

}
decreaseBtn.onclick = function(){
    count--;
    countLabel.textContent = count;
        
}
resetBtn.onclick = function(){
    count = 0;
    countLabel.textContent = count;
}
```

## Math object 🧮
* Math = build-in object that provides a collection of properties and methods

```js
let x = -3.21;
let y = 2;
let z;

//z = Math.round(x);
//z = Math.floor(x);
//z = Math.ceil(x);
//z = Math.trunc(x);
//z = Math.pow(x,y);
//z = Math.sqrt(x);
//z = Math.log(x);
//z = Math.sin(x); // for x=45
//z = Math.cos(x);
//z = Math.tan(x);
//z = Math.abs(x);
//z = Math.sign(x); // for sign -1,0 and 1 , can be used to determine
let max = Math.max(x,y,z);
let min = Math.min(x,y,z);


console.log(z);
```



## Random number generator ⁉

```js
let randonNum = Math.random();
randomNum = Math.random() * 6; // this will give the random numbers between 0 to 5 but in decimals!
randomNum = Math.floor(Math.random() * 6) +1; // this will give from 1 to 6!

//to get a random number between a range:  
const min = 50;
const max = 100;

let randomNum = Math.floor(Math.random() * (max - min)) + min;


console.log(randomNum);  

```

* Random Number generator

```html
<button id="myBtn"> roll </button>
<label id="myLabel"></label>
```

```css
body{  
    font-family: Verdana;
    text-align: center;
}
#myBtn{
    font-size: 3em;
    padding: 5px 25px;
    border-radius: 5px;
}
#myLabel{
    font-size: 3em;
}
```

```js
const myButton = document.getElementById("myBtn");
const myLabel = document.getElementById("myLabel");
const min = 1;
const max = 6;
let randomNum;

myButton.onclick = function(){
    randomNum = Math.floor(Math.random() * max) + min;
    myLabel.textContent = randomNum;
}


```

* Now, make 3 Labels with different numbers for roll btn yourself!

## If statements 🤔

* IF STATEMENTS =  if a condition is true, execute some code, if not , do something else!
* eg.,

```js
let age = 13;

if(age >= 18){
    console.log("You are old enough to enter this site");
}
else{
    console.log("You must be 18+ to enter this site");
}
```
```js
let isStudent = true;

if(isStudent){
    console.log("You are a student!");
}
else{
    console.log("You are NOT a student!");
}
```
* Nested if

```js
let age = 25;
let hasLicense = false;

if(age >= 16){
    console.log("you are old enouth to drive");
    if(hasLicense){
        console.log("You have your license!");
    }
    else{
        console.log("You do not have your license yet!");
    }
}
else{
    console.log("you must be 16+ to have a license");
}

```

* Else-if statements:
* eg.,
```js
if(){}
else if(){}
else{}
```
* Now, create it using html! yourself!

## Checked property ✅
* .checked = property that determines the checked state of an HTML checkbox or radio button element

```html
<body>
    <input type="checkbox" id="myCheckBox">
    <label for="myCheckBox">subscribe</label><br><br><!-- this for attribute makes the label clickable!-->

    <input type="radio" id="visaBtn" name="card">
    <label for="visaBtn">Visa</label><br>
    <input type="radio" id="masterBtn" name="card">
    <label for="masterBtn">MasterCard</label><br>
    <input type="radio" id="payPalBtn" name="card">
    <label for="payPalBtn">PayPal</label><br>

    <!-- to make them all linked together, we'll use the name attribute!
    
    <button type="submit" id="mySubmit">submit</button>

    <p id="subResult"></p>
    <p id="paymentResult"></p>

```

```css
body{
    font-family: verdana;
    font-size: 2em;
}
#mySubmit{
    font-size: 1em;
}

```

```js
const myCheckBox = document.getElementById("myCheckBox");
const visaBtn= document.getElementById("visaBtn");
const masterCardBtn= document.getElementById("masterCardBtn");
const payPalBtn = document.getElementById("payPalBtn");
const mySubmit= document.getElementById("mySubmit");
const subResult = document.getElementById("subResult");
const paymentResult = document.getElementById("paymentResult");

mySubmit.onclick = function(){

}

```

## Ternary operator ❓
* A shortccut to if{} and else{} statements helps to assign a variable based on a condition.
`condition ? codeIfTrue : codeIfFalse;`

```js
let age = 21;
let message = age >= 18 ? "You're an adult" : "You're a minor";
// This is useful if you want to assign a variable based on a condition.
```

* It's an alternative to write something like this!
```js
let message;

if(age >= 18){
    message = "You're an adult";
}else{
    message = "You're an minor";
}
```

* More examples
```js
let time = 16;
let greeting = time < 12 ? "Good morning!" : "Good afternoon!";
console.log(greeting);

let isStudent = true;
let message = isStudent ? "You are a student" : "You are NOT a student";
console.log(message);

// Challenge Round!!!
// We'll have a purchase amount , as if someone is buying something! If somebodies purchase amount is over 100$ , they get a 10% discount!
let purchaseAmount = 125;
let discount = purchaseAmount >= 100 ? 10 : 0;
console.log(`Your total is $${purchaseAmount - purchaseAmount * (discount / 100)}`);
```

## Switches 💡
- SWITCH = can be an efficient replacement to many else if statements
```js
//eg.,
let day = 1;

if(day == 1){
    console.log("It is Monday");
}
else if(day == 2){
    console.log("It is Tuesday");
}
//...and so on...
```

```js
//now with switch!
let day = 1;
switch(day){
    case 1:
        console.log("It is Monday");
        break;
    case 2:
        console.log("It is Tuesday");
        break;
    case 3:
        console.log("It is Wednesday");
        break;
    case 4:
        console.log("It is Thursday");
        break;
    case 5:
        console.log("It is Friday");
        break;
    case 6:
        console.log("It is Saturday");
        break;
    case 7:
        console.log("It is Sunday");
        break;
    default:
        console.log(`${day} is not a day`); // notice no break req. here!
}
```

```js
// more complex eg.,
// Instead of values, we can also pass conditions in the switch cases as below!
let testScore = 92;
let letterGrade;

switch(true){
    case testScore >= 90:
        letterGrade = "A";
        break;
    case testScore >= 80:
        letterGrade = "B";
        break;
    case testScore >= 70:
        letterGrade = "C";
        break;
    case testScore >= 60:
        letterGrade = "D";
        break;
    default:
        letterGrade = "F";
}

console.log(letterGrade);

```

## String methods 🧵
* string methods = allow you to manipulate and work with text (also known as strings)
* strings have different built-in methods where we can manipulate this text one way or another!

```js
// eg., 
let username = "BroCode";

console.log(userName.charAt(0)); // B
console.log(userName.indexOf("O")); // returns the index of the first occurance of the character!
console.log(userName.lastIndexOf("o")); // returns the last index of char!
console.log(userName.length);
// to trim white space in a string like "     BroCode" or "BroCode     "
console.log(userName.trim());
console.log(userName.toUpperCase());
console.log(userName.toLowerCase());
console.log(userName.repeat(3)); // will repeat the userName 3 times!
// we could also do this => userName = userName.repeat(3); console.log(userName);
// To determine if a string starts with a given character we can use the starts with method, this will retrun a boolean!
let result = userName.startsWith(" "); // userName = " BroCode";
console.log(result); // true!
//This could be useful in if statement as:
if(result){
    console.log("Your username can't begin with ' '");
}else{
    console.log(userName);
}

// there's also a .endsWith()
userName.endsWith(" ");
// .includes()
let result = userName.includes(" "); // eg., userName = "Bro Code";
if(result){
    console.log("Your username can't include ' '");
}else{
    console.log(userName);
}

// now, we'll create a phone number with - and we'll eliminate all the dashes using the .replaceAll()
let phoneNumber = "123-456-7890";
phoneNumber = phoneNumber.replaceAll("-","");
console.log(phoneNumber);
// then we have .padStart() method!
phoneNumber = phoneNumber.padStart(15, "0");
phoneNumber = phoneNumber.padEnd(15, "0");
```

## String slicing ✂️
* String slicing is the process of creating a substring from a portion of another string. (This won't alter the origin string)
- eg., `string.slice(start, end)`

```js
// we'll extract the first name and make a new string
const fullName = "Bro Code";

let firstName = fullName.slice(0, 3); //end is exclusive
let lastName = fullName.slice(4,8);
let lastName = fullName.slice(4); //this both works the same! 

let firstChar = fullName.slice(0,1);
//Negative indices works as well!
let lastChar = fullName.slice(-1); // e
let fromLast = fullName.slice(-4); // code

//to make this program more dynamic, we can combine string slicing with indexof method!
//and in the next example, we're gonna do exactly that!
```

```js
const fullName = "Broseph Code";

let firstName = fullName.slice(0, fullName.indexOf(" ")); //Broseph
let lastName = fullName.slice(fullName.indexOf(" ")); // Code (with a space)
//To remove padding..
lastName = fullName.slice(fullName.indexOf(" ")+1); //code 
```

```js
//Exercise
const email = "kishor010@gmail.com";

let userName = email.slice(0, email.indexOf("@"));
let extension = email.slice(email.indexOf("@")+1);
```
## Method chaining ⛓
- Method Chaining (Programming technique) = Calling one method after another in one continuous line of code.

- NO METHOD CHAINING DEMONSTRATION
```js
let userName = window.prompt("Enter your username:"); // Input:      brOcOdE
//after this, we'll take the entered username and trim all the white spaces , make the first char UPPERCASE and all other lower and display the output!

userName = userName.trim();
let letter = userName.charAt(0);
letter = letter.toUpperCase();

let extraChars = userName.slice(1);
extraChars = extraChars.toLowerCase();
userName = letter + extraChars;

console.log(userName); // Output: Brocode
```

- METHOD CHAINING DEMONSTRATION
```js
let userName = window.prompt("Enter your username: ");
userName = userName.trim().charAt(0).toUpperCase() + userName.trim().slice(1).toLowerCase(); //see the use of string concatination!
// Though, it helps avoiding extra variables use, but can make it harder to read if it's long! (like here we're pushing it to the limits!)

console.log(userName); // Works the same!
```
## Logical operators ❗
- logical operators = used to combine or manipulate boolean values (true or false)

| Logical Operator | Symbol |
|------------------|---------|
| AND              | &&      |
| OR               | \|\|    |
| NOT              | !       |

- eg,
```js
const temp = 20;

if(temp > 0 && temp <= 30){
    console.log("The weather is GOOD");
}else{
    console.log("The weather is BAD");
}

if(temp <= 0 || temp > 30){
    console.log("The weather is BAD");
}else{
    console.log("The weather is GOOD");
}

const isSunny = false;

if(!isSunny){
    console.log("It is CLOUDY");
}else{
    console.log("It is SUNNY");
}
```

## Strict equality 🟰
- = assignmetn operator
- == comparison operator (compare if values are equal)
- === strict equality operator (compare  values & datatype are equal)
- != Inequality operator
- !== strict inequality operator

## While loops 🔁
- while loop = repeat some code WHILE some condition is true

```js
let username = "";

while(username === ""){
    console.log(`You didn't enter your name`);
}
console.log(`Hello ${username}`);
//but this block of code runs forever and doesn't do anything! so , we'll re-write this code!
```

```js
let username ="";

while(username === ""){
    username = window.prompt("Enter your name");
}
console.log(`Hello ${username}`); // but it will print null if pressed cancel
//to fix that, we can:
/*
    update the while loop as:
    while(username === "" || usernamm === null)
*/
```
- Do while loop is an another variation of while loop (study yourself!)

```js
// another example
let loggedIn = false;
let username;
let password;

while(!loggedIn){
    username = window.prompt("Enter your username");
    password = window.prompt(`Enter your password`);

    if(username === "myUsername" && password === "myPassword"){
        loggedIn = true;
        console.log("You are logged in!");
    }else{
        console.log("Invalid credentials! Please try again!");
    }
}
```
## For loops 🔂
- For loop = repeat some code a LIMITED amount of times
- eg.,
```js
for(let i = 0; i <= 2; ++i){
    console.log(i);
}
```
## Number guessing game ↕
- try playing with the `Math.random()` function and find out why this code below generates a random number between the specified range!
```js
const minNum = 1;
const maxNum = 100;
const answer = Math.floor(Math.random() * (maxNum - minNum + 1)) + minNum;
```

- Source code:
```js
const minNum = 1;
const maxNum = 100;
const answer = Math.floor(Math.random() * (maxNum - minNum + 1)) + minNum;

let attempts = 0;
let guess;
let running = true;

while(running){
    guess = window.prompt(`Guess a number between ${minNum} - ${maxNum}`);
    guess = Number(guess);

    if(isNaN(guess)){
        window.alert("Please enter a valid number");
    }
    else if(guess < minNum || guess > maxNum){
        window.alert("Please enter a valid number");
    }
    else{
        attempts++; //what if we just write attempts; here??
        if(guess < answer){
            window.alert("TOO LOW! TRY AGAIN!");
        }
        else if(guess > answer){
            window.alert("TOO HIGH! TRY AGAIN!");
        }
        else{
            window.alert(`CONGRATS! ${answer} is the correct number! It took you ${attempts} attempts to guess!);
            running = false;
        }
    }
}


```

## Functions 📞
- Function = A section of reusable code. 
- Declare code once, use it whenever you want.
- Call the function to execute that code.
- eg., 

```js
function happyBirthday(){
    console.log("Happy Birthday to you");
    console.log("Happy Birthday to you");
    console.log("Happy Birthday dear you");
    // console.log(`Happy Birthday dear ${username}, You're ${age} year old!`); // this will raise an Uncaught ReferenceError as username is not defined! You can use function arguments for this! but for that you'll need to set parameters! let's do this now in the next code snippet!
    console.log("Happy Birthday to you");
}

happyBirthday();
happyBirthday(); // shows code reusability!

```

```js
function happyBirthday(username, age){ // Order of parameters matters here! (try switching username and age here and see!)
    console.log("Happy Birthday to you");
    console.log("Happy Birthday to you");
    console.log(`Happy Birthday Dear ${username}`);
    console.log("Happy Birthday to you");
    console.log(`You are ${age} year old`);
}

happyBirthday("Brocode", 25);
happyBirthday("Kishor", 22);

```
- Return keyword:

```js
function add(x,y){
    let result = x + y;
    return result; // or shortcut: return x+y;
}

let answer = add(2,3);
console.log(answer);
// or console.log(add(2,3));

// similarly, make subtract, multiply, divide and isEven, isValidEmail functions yourself!
```
## Variable scope 🏠
- variable scope = where a variable is recognized and accessible (local vs global)
- variables need to have unique names
```js
let x = 1;
let x = 2;
//doing this will raise an error : caught SyntaxError: Identifier 'x' has already been declared
// We cannot declare variables with the same name until the scope is different!
```

```js
function1(); // invoke function1 before declaration! (valid in js!)
function2(); // functions are Hoisted (but not the Function Expression or Arrow Functions!)

function function1(){
    let x = 1;
    console.log(x);
}

function function2(){
    let x = 2; // here in this example, we can declare x since it's in different scope! (This is known as Local scope)
    console.log(x);
}

```
- Analogy: Think of functions to houses and you can't see inside it! So, the local scope variables, only visible from inside of a house (ie, function) but a global variable is like a tree outside on the road, so every house can see it!

- It is not recommended to have a lot of global variables as it is accessible to every functions and are mutable which makes debugging a tedious task later! (Just like how functional programming avoids having global mutable variables!)
## Temperature conversion program 🌡️
- Check the source code in video!
## Arrays 🗃
- Array = a variable like structure that can hold more than 1 value
- eg.,
```js
let fruits = ["apple", "orange", "banana"];
console.log(fruits); 
// output: ['apple', 'orange' , 'banana']
console.log(fruits[1]); // orange
console.log(fruits[10]); //if you try to access an index that does not exists yet, it will print undefined!
//we can also modify elements at a index as:
fruits[1] = "coconut";
// although, we can add a new element like avoid but we can also use the built-in method .push
fruits.push("mango");
fruits.pop(); // removes elements from last!
fruits.unshift("Guava"); // add an element to the beginning
fruits.shift(); // to remove an element from the beginning
fruits.length; // built-in method to count the number of elements in an array! (not .length has no parenthesis()! Why?)
let index  = fruits.indexOf("apple"); // return the index of "element" if found! and -1 if not found! (which can be used in if(statement)!)

for(let i=0; i<fruits.length; ++i){
    console.log(fruits[i]);
}
//enhanced for loop =>
for(let fruit of fruits){
    console.log(fruit);
}

fruits.sort(); // sort elements in alphabetical order!
fruits.sort().reverse(); // for reverse order!
```
## Spread operator 📖
- Spread operator = ... allows an iterable such as an array or string to be expanded into separate elements (unpacks the elements)
- eg.,
```js
let numbers = [1,2,3,4,5];
let maximum = Math.max(numbers); // to find the max

console.log(maximum); // NaN ❌
// for this we would need to use the spread operator!
maximum = Math.max(...numbers);
console.log(maximum); // 5 ✔️
console.log(let minimum = Math.min(...numbers)); // 1
```
- we can also do this with strings!
```js
let username = "Bro Code";
let letters = [...username];

console.log(letters); // ['B', 'r', 'o', ' ' , 'C', 'o' , 'd' , 'e']

letters = [...username].join("-"); // this joins the characters into string and also insert - in between them! Output: B-r-o- -C-o-d-e
```

- Now, we will create a shallow copy of an array using the spread operator!
- Shallow copy = A different data structure but contains identical values!
- Shallow copy doesn't mean editing one will reflect in both! eg., 
```js
// test.js
let fruits = ["apple", "orange", "banana"];
let newFruits = [...fruits];

newFruits[0] = "mango";

console.log(fruits);
console.log(newFruits);
```

```js
// we can use the spread operator to combine arrays!
let fruits = ["Apple", "Orange", "Banana"];
let vegies = ["carrots", "celery", "potatoes"];

let foods = [...fruits, ...vegies];

console.log(foods);
// it also have this ability to append new data in the array, as:
vegies = [...fruits, ...vegies, "eggs", "milk"];
```
## Rest parameters 🗄
- Rest parameters = {...rest} allow a function work with a variable number of arguments by bundling them into an array.
- spread = expands an array into seperate elements
- rest = bundles seperate elements into an array

```js
//eg. 1, 
function openFridge(...foods){
    console.log(...foods);
}
function getFood(...foods){
    return foods;
}

const food1 = "pizza";
const food1 = "hamburger";
const food1 = "hotdog";
const food1 = "sushi";
const food1 = "ramen";

//openFridge = getFood(food1, food2, food3, food4, food5);

console.log(foods);
```

```js
// eg. 2,
function sum(...numbers){
    let result = 0;
    for(let number of numbers){
        result += number;
    }
    return result;
}

const total = sum(1,2,3,4,5);

console.log(`Your total is $${total}`);
```

```js
//eg. 3,
function sum(...numbers){
    let result = 0;
    for(let number of numbers){
        result += number;
    }
    return result;
}

function getAverage(...numbers){

    let result = 0;
    for(let number of numbers){
        result += number;
    }
    return result / numbers.length;
}

const total = getAverage(75, 100, 85, 90, 50);

console.log(total);

```

```js
//eg. 4, (we can also combines strings using ...rest operator!)
function combineStrings(...strings){
    return strings.join(" ");
}

const fullName = combineStrings("Mr." , "Spongebob", "Squarepants", "III");

console.log(fullName);
```
## Dice Roller program 🎲
- Check the source code in video
## Random password generator 🔑
- Check the source code in video
## Callbacks 🤙
- callback = a function that is passed as an argument to another function.
- It is used to handle asynchronous operations:
1. Reading a file
2. Network requests
3. Interacting with databases
- These activities take some time to complete. Now with JavaScript, we don't necessarily wait for a process to finish before continuing with the rest of the program. For example, If we were to read a file, if it takes a long time to read that file, JavaScript might continue on with the rest of the program. We might attempt to display the contents of that file before we're finished reading it. That's where callbacks come in! 
- It's like we're telling JavaScript: `Hey, when you're done, call this next`.
- `When you're done reading the files , then display the contents only after that process is complete`
```js
//eg. 1,
hello();
goodBye();

function hello(){
    console.log("Hello!");
}
function goodBye(){
    console.log("Goodbye!");
}

//Output: Hello!\nGoodbye!

//now, suppose for some reason the hello() takes some time to execute! Js won't wait for it and execute the next line and print Goodbye!\nHello! 
// we'll use setTimeOut() to demonstrate that! =>

{
    hello();
    goodBye();

    function hello(){
        setTimeout(function(){
            console.log("Hello!");
        },3000);
    }
    function goodBye(){
        console.log("Goodbye!");
    }
    // Output: Goodbye! *(after 3s) \nHello!
    // But the desired result was the other way around!
    // this is where callback function comes in picture and could be used to acheive the desired result!
}

{
    //now with callback()
    hello(goodBye); // using hello(goodBye()); will immediately invoke the goodBye function!

    hello(leave);
    hello(wait);

    function hello(callback){
        console.log("Hello!");
        callback();
    }

    function wait(){
        console.log("Wait!");
    }

    function leave(){
        console.log("Leave!");
    }

    function goodbye(){
        console.log("Goodbye!");
    }

    /*
        Output: 
        Hello!
        Goodbye!
        Hello!
        Leave!
        Hello!
        Wait!
    */
}
```
- So, by using callbacks we are guaranteeing that the function passed in will execute next!

```js
// eg. 2,

//invoke
sum(displayConsole, 1, 2); // output: 3

function sum(callback, x, y){
    let result = x + y;
    callback(result); //invoke
}

function displayConsole(result){
    console.log(result);
}

//lets create a function to display result on the webpage (DOM)
/*
    (required!)
    <h1 id="myH1"></h1>
*/
function displayPage(result){
    document.getElementById("myH1").textContent = result;
}

sum(displayPage, 2, 3); // DOM: 5

```
## forEach() ➿
- forEach() = method used to iterate over the elements of an array and apply a specified function (callback) to each element
- we have an array, we can use the built-in for each method of arrays and send each element through a callback to a function
- `array.forEach(callback)` element, index, array are provided 
- eg.,
```js
let numbers = [1,2,3,4,5];

numbers.forEach(display); //where is the element argument??

function display(element){
    console.log(element);
}
// output: 1\n2\n3\n4\n5
```
- Believe it or not, the element argument is provided for us with the for each method!
- Behind the scenes, the forEach method will provide to a callback an element, index and array argument.
- An element for the current element that we're on when looping through this array, an index that keeps track of the current index number and the location of the array itself, that in this case it would be numbers!
- That's why when we pass the display function as a callback, we're already provided with an element argument behind the scenes
- Now, we'll double the elements of the array before displaying it, in this next example!

```js
// eg. 2,
let numbers = [1,2,3,4,5];

numbers.forEach(double);
numbers.forEach(display);

function double(element, index, array){ //these are already provided
    array[index] = element * 2;
}

function display(element){
    console.log(element);
}
```

```js
//eg. 3, more practical method!
let fruits = ["apple", "orange", "banana", "coconut"];

fruits.forEach(upperCase);
fruits.forEach(display);

function upperCase(element, index, array){
    array[index] = element.toUpperCase(); // rem: methods alway belongs to something where functions are Standalone
}

// similarly, make lowerCase() and capitalize() functions!

function display(element)){
    console.log(element);
}
```

## map() 🗺
- .map() = accepts a callback and applies that function to each element of an array, then return a new array. 
- It's very similar to the forEach method, except that it returns a new array!
```js
//eg., 
const numbers = [1,2,3,4,5];
const squares = numbers.map(square);
const cubes = numbers.map(cube);

console.log(squares); // output: [1, 4, 9, 16, 25]
console.log(cube); // output: [1, 8, 27, 64, 125]

function square(element){
    return Math.pow(element, 2);
}

function cube(element){
    return Math.pow(element, 3);
}

// we still have our original numbers array as it is!
```

```js
//eg. 2,
const students = ["Spongebob", "Patrick", "Squidward", "Sandy"];
const studentsUpper = students.map(upperCase);
const studentsLower = students.map(lowerCase);

console.log(studentsUpper);
console.log(studentsLower);

function upperCase(element){
    return element.toUpperCase();
}

function lowerCase(element){
    return element.toUpperCase();
}
```

```js
// a more practical example (date format)
const dates = ["2024-1-10", "2025-2-20", "2026-3-30"];
const formattedDates = dates.map(formatDates);

console.log(formattedDates);

function formatDates(element){
    const parts = element.split("-");
    return `${parts[1]}/${parts[2]}/${parts[0]}`;
}
```

## filter() 🚰
- filter() = creates a new array by filtering out elements
```js
let numbers = [1, 2, 3, 4, 5, 6, 7];
let evenNums = numbers.filter(isEven);
let oddNums = numbers.filter(isOdd);

console.log(evenNums); // output: [2, 4, 6]
console.log(oddNums); // output: [1, 3, 5, 7]

function isEven(element){
    return element % 2 === 0; //this will return a boolean!
}

function isOdd(element){
    return element % 2 !== 0; //this will return a boolean!
}
```
```js
// eg. 3,
const ages = [16, 17, 18, 19, 20, 60];
const adults = ages.filter(isAdult);
const children = ages.filter(isChild);

console.log(adults);
console.log(children);

function isAdult(element){
    return element >= 18;
}

function isChild(element){
    return element < 18;
}
```
```js
//eg. 4, 
const words = ["apple", "orange", "banana", "kiwi", "pomegranate", "coconut"];
const shortWords = words.filter(getShortWords);
const longWords = words.filter(getLongWords);

console.log(shortWords);
console.log(longWords);

function getShortWords(element){
    return element.length <= 6;
}

function getLongWords(element){
    return element.length > 6;
}
```
## reduce() ♻
- reduce() = reduce the elements of an array to a single value
- it also needs a callback, just like the above two!
```js
//eg. 1,
const prices = [5, 30, 10, 25, 15, 20];

const total = prices.reduce(sum); // callback required!

console.log(`$${total.toFixed(2)}`);

function sum(accumulator, element){ // we could also write previous , next here!
    return accumulator + element;
}
```
```js
//eg. 2,
const grades = [75, 50, 90, 80, 65, 95];

const maximum = grades.reduce(getMax); //95
const minimum = grades.reduce(getMin); //65

console.log(maximum);
console.log(minimum);

function getMax(accumulator, element){
    return Math.max(accumulator, element);
}

function getMin(accumulator, element){
    return Math.min(accumulator, element);
}
```
## Function expressions 🐣
- Function declaration = define a reusable block of code that performs a specific task
```js
//eg., 
function hello(){
    console.log("Hello");
}
```
- Function expression = a way to define functions as values or variables
```js
//eg. passing a function expression as a variable, 
const hello = function(){
    console.log("Hello");
}

hello(); // invoke to use that hello() function!

//eg. passing a function expression as a value,
function hello(){
    console.log("Hello");
}

setTimeout(hello, 3000); //setTimeout(callback, delay);

// instead of a callback, we will pass a function expression as a value to this function!
setTimeout(function(){
    console.log("Hello again!");
}, 3000);
```

```js
//eg. 2, 
{
    // here in this block of code, we are using the function declaration!
    const numbers = [1, 2, 3, 4, 5];
    const squares = numbers.map(square); // taking a callback
    
    console.log(squares);
    
    function square(element){
        return Math.pow(element, 2);
    }
}

{
    // In this block of code, we have used the function expression passed as the value!
    const numbers = [1, 2, 3, 4, 5];
    const squares = numbers.map(function(element){
        return Math.pow(element, 2);
    });

    console.log(squares); // works the same!

/*
    Note: We don't need to think of a function name, one of the benefits of doing this is that we're not polluting the global Name space with function names. We're only going to be using this  function once, there's no need to declare a function!    
*/
}

{
    //similarly, make the cube function with function expression!
}
```

```js
// Now, function expressions with filter!
const numbers = [1, 2, 3, 4, 5];

const evenNums = numbers.filter(function(element){
    return element % 2 === 0;
});

// make oddNums yourself!

console.log(evenNums);
```

```js
//Now, function expression with reduce!
const numbers = [1, 2, 3, 4, 5];

const total = numbers.reduce(function(accumulator, element){
    return accumulator + element;
});

console.log(total);
```
- In the next topic, we'll make this even shorter! using the arrow functions!

- More Topics to discuss:
1. Callbacks in asynchronous operations 
2. Higher-Order functions
3. Closures
4. Event Listeners
(We'll discuss it later!)

## Arrow functions 🎯
- Arrow functions = a concise way to write function expressions, good for simple functions that you use only once
- `(parameters) => some code`
```js
{
    // Normal way!
    hello();
    
    function hello(){
        console.log("Hello");
    }
}
{
    // we'll first create a function expression and then convert it to an arrow function!
    const hello = function(){
        console.log("Hello");
    }

    hello(); // Invoked below declaration because function expressions are not hoisted!
}
{
    // Now with arrow function => 
    const hello = () => console.log("Hello");

    hello(); //works the same!
}
{
    //WE CAN ALSO PASS ARGUMENTS IN IT! 
    const hello = (name) => console.log(`Hello ${name}`);

    hello("Kishor"); // prints: Hello Kishor
}
{
    // within your code, if you want to insert more than one statement, wrap them in {}
    const hello= (name, age) => { //{} used for more statements, i.e, two console.log()'s
        console.log(`Hello ${name}`);
        console.log(`You're ${age} year old!`);
    }
    // Notice how we used multiple parameters this time!
    hello("Kishor", 22);
}
```

```js
{
    // another example
    setTimeout(hello, 3000); //setTimeout(callback, delay)

    function hello(){
        console.log("Hello");
    }
}

{
    // Now with function expression =
    setTimeout(function(){
        console.log("Hello");
    },3000);
}

{
    // Now with arrow function =>
    setTimeout(() => console.log("Hello"), 3000); // works the same!    
}
```

```js
// now, we'll use arrow functions with map, filter, and reduce!
const numbers = [1, 2, 3, 4, 5];

const squares = numbers.map((element) => Math.pow(element, 2));
const cubes = numbers.map((element) => Math.pow(element, 3));
const evenNums = numbers.filter((element) => element % 2 === 0); // we don't necessarily need to return statement if we have only one line of code! (like here!)
const oddNums = numbers.filter((element) => element % 2 !== 0);
const total = numbers.reduce((accumulator, element) => accumulator + element);

console.log(squares);
console.log(cubes);
console.log(evenNums);
console.log(oddNums);
console.log(total);
```

## JavaScript Objects 🧍
- Object = A collection of related properties and/or methods, Can represent real world objects (people, products, places)
- properties are the things that an object has! such as name or age
- a method is a function that belong to an object 
- `object = {key:value, function()}`

```js
const person1 = {
    firstName: "Spongebob",
    lastName: "Squarepants",
    age: 30,
    isEmployed: true,
    // objects can have functions as well!
    sayHello: function(){console.log("Hi! I am Spongebob!")}, //this is going to be a function expression 

}

const person2 = {
    firstName: "Patrick",
    lastName: "Star",
    age: 42,
    isEmployed: false,
    sayHello: () => console.log("Hi! I am Patrick!..."), // here, we have used the arrow function =>
}

console.log(person1.firstName);
console.log(person1.lastName);
console.log(person1.age);
console.log(person1.isEmployed);
person1.sayHello();

console.log(person2.firstName);
console.log(person2.lastName);
console.log(person2.age);
console.log(person2.isEmployed);
person2.sayHello();
``` 
## What is THIS 👈
- this = reference to the object where THIS is used (the object depends on the immediate context)
- `person.name = this.name`

```js
const person1 = {
    name: "Spongebob",
    favFood: "hamburgers",
    sayHello: function(){console.log(`Hi! I am ${this.name})`}, // Hi! I am , will be printed if not used this keyword! using this.name is same as using person1.name!
    eat: function(){console.log(`${this.name} is eating ${this.favFood}`)},
}
// one of the cool features of it , is when we copy this code for person2 , we only need to update the name and favFood property and it will work!
const person2 = {
    name: "Patrick",
    favFood: "Pizza",
    sayHello: function(){console.log(`Hi! I am ${this.name})`}, // Hi! I am , will be printed if not used this keyword! using this.name is same as using person1.name!
    eat: function(){console.log(`${this.name} is eating ${this.favFood}`)},
}

person1.sayHello();
person1.eat();
person2.sayHello();
person2.eat();
```
- If you were to use `this` outside of any objects, I'm going to `console.log(this)` as:
```js
console.log(this);
```
- It will return a window object (in case you're in a browser)
- Basically, we are returning the window to see our website  
- Technically we're inside of an object already, our window object! And we have all of these properties, but since we're using this keyword inside the context of person1 and person2 , we'll instead make a reference to those objects
> Very Important: this keyword doesn't work with arrow functions!

```js
const person1 = {
    name: "Spongebob",
    favFood: "hamburgers",
    eat: () => console.log(`${this.name} is eating ${this.favFood}`),
}
person1.eat(); // output:  is eating undefined
```
- when you use `this` within an arrow function, it's making a reference to that window object still
- Our window object does have a name, that's why it's appearing empty but favFood is undefined because our window object doesn't have a favFood property!
## Constructors 🛠
- constructor = special method for defining the properties and methods of objects
```js
// In previous examples, we have learn to create objects and assign properties to each of those object, but what if we had to make a lot of objects?? There the constructor comes into picture! WE WILL USE CONSTRUCTORS TO CONSTRUCT MULTIPLE OBJECTS AUTOMATICALLY!

// First we'll make a function
function Car(make, model, year, color){ // DO PAY ATTENTION TO THE CAPITALISATION!
    this.make = make,
    this.model = model,
    this.year = year,
    this.color = color,
    this.drive = function(){console.log(`You drive the ${this.model}`)}
}
// Our Car constructor is a reusable method, where we can define the properties and methods of objects we create
// To use this constructor, we will create an instance of an object

const car1 = new Car("Mclaren", "P1", 2025, "Orange"); // Car() is a special method, we'll need to pass in some arguments!

console.log(car1.make);
console.log(car1.model);
console.log(car1.year);
console.log(car1.color);
car1.drive();

//similarly, make more cars!
```
## Classes 🏭
- class = (ES6 feature) provides a more structured and cleaner way to work with objects compared to traditional constructor functions
- eg., static keyword, encapsulation, inheritance
```js
// here in this eg., we have used the constructor
function Product(name, price){
    this.name = name;
    this.price = price;

    this.display = function(){
        console.log(`Product: ${this.name}`);
        console.log(`Price: $${this.price.toFixed(2)}`);
    };

    this.calculateTotal = function(salesTax){
        return this.price + (this.price * salesTax);
    }
}

const salesTax = 0.05;

const product1 = new Product("Shirt", 19.99);
const product1 = new Product("Pants", 22.50);
const product1 = new Product("Underwear", 100.00);

product1..displayProduct();

const totalPrice = product1.calculateTotal(salesTax);

console.log(`Total Price (with tax): $${totalPrice.toFixed(2)}`);
```

```js
// we'll use classes to do the same thing but in much better/ efficient way!
class Product{ // our class will serve as a blueprint!
    constructor(name, price){
        this.name = name;
        this.price = price;
    }

    //inside of a class, we don't need to use the `function` keyword!
    displayProduct(){
        console.log(`Product: ${this.name}`);
        console.log(`Price: $${this.price.toFixed(2)}`);
    }

    calculateTotal(salesTax){
        return this.price +(this.price * salesTax);
    }
}

const salesTax = 0.05; // that is , 5%

// lets create some Product objects
const product1 = new Product("shirt", 19.99); // we use the `new` keyword to use the constructor of an object! (eg., const array = new Array(1,2,3)); )

product1.displayProduct();

const total = product1.calculateTotal(salesTax);
console.log(`Total price (with tax): $${total.toFixed(2)}`);


// similarly, create more products!
```
## STATIC keyword ⚡
- Static = keyword that defines properties or methods that belong to a class itself rather than the objects created from that class (class own anything static, not the objects)
- We're going to create a class for Math utilities
```js
class MathUtil{
    static PI = 3.14159;

    static getDiameter(radius){
        return radius * 2;
    }

    static getCircumference(radius){
        return 2 * this.PI * radius;
    }

    static getArea(radius){
        return this.PI * radius * radius;
    }
}

console.log(MathUtil.PI); // here, we didn't need to create an object for class MathUtil in order to use that PI property of it! (If we call it via an object, it'll say undefined!)
// anything declared static, belong to the class itself! Not to the objects!

console.log(MathUtil.getDiameter(10)); // 20
console.log(MathUtil.getCircumference(10)); // 62.8318
console.log(MathUtil.getArea(10)); // 314.159
```

```js
// In this example, we'll have a mix of regular properties and methods and static property and methods
class User{

    static userCount = 0;

    constructor(username){
        this.username = username;
        User.userCount++;
    }

    static getUserCount(){
        console.log(`There are ${User.userCount}  users online`); // here , this.userCount also does the same thing!
    }

    sayHello(){
        console.log(`Hello! My username is ${this.username}`);
    }
}

const user1 = new User("Spongebob");
const user2 = new User("Patrick");
const user3 = new User("Sandy");

// console.log(user1.username);
// console.log(user1.userCount); // this will print undefined, as static properties do not belong to the object!

console.log(user1.username);
console.log(user2.username);
console.log(user3.username);

user1.sayHello();
user2.sayHello();
user3.sayHello();
console.log(User.userCount); // prints : 1
User.getUserCount();
```

## Inheritance 🐇
- inheritance = allows a new class to inherit properties and methods from an existing class (parent -> child) helps with code reusability
- It's kind of like a family tree!
```js
class Animal{
    alive = true; // Notice bro didn't wrote let or const here?? why??

    eat(){
        console.log(`This ${this.name} is eating`);
    }
    sleep(){
        console.log(`This ${this.name} is sleeping`);
    }
}
class Rabbit extends Animal{
    name= "rabbit";
}
class Fish extends Animal{
    name= "fish";
}
class Hawk extends Animal{
    name= "hawk";
}

const rabbit = new Rabbit();
const fish = new Fish();
const hawk = new Hawk();

//Ok, lets see if our rabbit is alive

// rabbit.alive = false;
console.log(rabbit.alive); // true
rabbit.eat();
rabbit.sleep();

console.log(fish.alive); // true
fish.eat();
fish.sleep();

console.log(hawk.alive); // true
hawk.eat();
hawk.sleep();
```
- Our children classes of Rabbit , Fish and Hawk al inherited the properties and methods of the parent Animal class.
- This helps in code reusability! (because, we don't need to declare all of these properties and methods within each of the children classes!)
- Not only that, the children can have their own unique properties and methods!
- eg., Rabbits will be able to run, but fish and hawk cannot be! (that's a method that only belong to the Rabbit class)

```js
class Rabbit extends Animal{
    name= "rabbit";
    run(){
        console.log(`This ${this.name} is running!`);
    }
}
}
class Fish extends Animal{
    name= "fish";
    swin(){
        console.log(`This ${this.name} is swimming!`);
    }
}
class Hawk extends Animal{
    name= "hawk";
    fly(){
        console.log(`This ${this.name} is flying!`);
    }
}
```


## SUPER keyword 🦸‍♂️
- super = keyword is used in classes to call the constructor or access the properties and methods of a parent (aka superclass)
- `this = this object`
- `super = the parent`
```js
class Animal{
    constructor(){

    }
}
class Rabbit extends Animal{
    constructor(name, age, runSpeed){
        super();
        this.name = name;
        this.age = age;
        this.runSpeed = runSpeed;
    }
}

class Fish extends Animal{
    constructor(name, age, swimSpeed){
        super();
        this.name = name;
        this.age = age;
        this.swimSpeed = swimSpeed;
    }
}

class Hawk extends Animal{
    constructor(name, age, flySpeed){
        super();
        this.name = name;
        this.age = age;
        this.flySpeed = flySpeed;
    }
}

const rabbit = new Rabbit("rabbit", 1, 25);
const fish = new Fish("fish", 2, 12);
const hawk = new Hawk("hawk", 3, 50);
```
- Running the above code will result in : `ReferenceError: Must call super constructor in derived class before accessing 'this' or returning from derived constructor`
- To resolve it, use the `super()` keyword! (un-comment that super() part in each of those constructors!)
- So, the JS is telling us, before using `this` keyword, call the constructor of the parent class!
- So, one of the benefits of using Constructors is that if there's any properties that the children all share in common, we can send them to the Constructor of the parent.
- In the above code, as you can see , we are repeating ourselves a lot! Each of these children classes has a name and age property that we're assigning to each! We would like to follow the `DRY principle` `DO NOT REPEAT YOURSELF` (Next, we will do just that!)

```js
class Animal{
    constructor(name, age){
        this.name = name;
        this.age = age;
    }
}
class Rabbit extends Animal{
    constructor(name, age, runSpeed){
        super(name, age); // we need to pass in the arguments to the parent constructor!
        this.runSpeed = runSpeed;
    }
}

class Fish extends Animal{
    constructor(name, age, swimSpeed){
        super(name, age);
        this.swimSpeed = swimSpeed;
    }
}

class Hawk extends Animal{
    constructor(name, age, flySpeed){
        super(name, age);
        this.flySpeed = flySpeed;
    }
}

const rabbit = new Rabbit("rabbit", 1, 25);
const fish = new Fish("fish", 2, 12);
const hawk = new Hawk("hawk", 3, 50);


console.log(rabbit.name);
console.log(rabbit.age);
console.log(rabbit.runSpeed);

console.log(fish.name);
console.log(fish.age);
console.log(fish.runSpeed); // undefined as fishes don't have legs so they can't run , but they do have a swimSpeed!
console.log(fish.swimSpeed);

// works the same!
// So, all the sharing properties of children, can be passed in the parent class constructor for avoiding redundant code!
```

```js
// now, in this example, we'll make a move() in parent class and in each of these children class, will write a function that extends this move() method! 
class Animal{
    constructor(name, age){
        this.name = name;
        this.age = age;
    }

    // NEW UPDATE HERE.......✔️✔️✔️✔️✔️✔️✔️✔️✔️✔️
    move(speed){
        console.log(`The ${this.name} moves at a speed of ${speed}km/h`);
    }

}
class Rabbit extends Animal{
    constructor(name, age, runSpeed){
        super(name, age); // we need to pass in the arguments to the parent constructor!
        this.runSpeed = runSpeed;
    }

    run(){
        console.log(`This ${this.name} can run!`);
        super.move(this.runSpeed);
    }
}

class Fish extends Animal{
    constructor(name, age, swimSpeed){
        super(name, age);
        this.swimSpeed = swimSpeed;
    }

    swim(){
        console.log(`This ${this.name} can swim!`);
        super.move(this.swimSpeed);
    }
}

class Hawk extends Animal{
    constructor(name, age, flySpeed){
        super(name, age);
        this.flySpeed = flySpeed;
    }

    fly(){
        console.log(`This ${this.name} can fly!`);
        super.move(this.flySpeed);
    }
}

const rabbit = new Rabbit("rabbit", 1, 25);
const fish = new Fish("fish", 2, 12);
const hawk = new Hawk("hawk", 3, 50);

rabbit.run();
fish.swim();
hawk.fly();
```
## Getters & Setters 📐
- getter = special method that makes a property readable
- setter = special method that makes a property writeable
- we can use them to validate and modify a value when reading/writing a property
- It helps with validation when creating an object or updating one of its properties
- eg.,

```js
class Rectangle{
    constructor(width, height){
        this.width = width;
        this.height = height;
    }
}

const rectangle = new Rectangle(-1000000, "pizza");

console.log(rectangle.width);
console.log(rectangle.height);
// output: -100000\npizza
```
- We don't want people to enter in garbage values like these in our program! To avoid that, we use getters and setters (for input validation!)
- setters : When setting one of these properties (width, height) either initially through a Constructor or updating one of them later, such as setting the width or height equal to some value, we can go to a setter first!

```js
class Rectangle{
    constructor(width, height){
        this.width = width;
        this.height = height;
    }

    set width(newWidth){ // this will be a special type of method!
        if(newWidtt > 0){
            this._width = newWidth; // using the _underscore prefix, it tells other developers that this is a private property (you shouldn't touch it at all!) 
            // you could say that this private property of width is different than our standard width property!
        }else{
            console.error("Width must be a positive number"); //and it makes the width value `undefined` in the console window (if used a negative width!)
        }
    }

    set height(newHeight){ // this will be a special type of method!
        if(newWidtt > 0){
            this._height = newHeight; // using the _underscore prefix, it tells other developers that this is a private property (you shouldn't touch it at all!) 
            // you could say that this private property of width is different than our standard width property!
        }else{
            console.error("Height must be a positive number"); //and it makes the width value `undefined` in the console window (if used a negative width!)
        }
    }

    // NOW EVEN WITH A VALID NUMBERS, THE OUTPUT WILL STILL BE UNDEFINED! THAT'S WHERE THE GETTER METHOD COMES IN!

    get width(){
        return this._width;
    }

    get height(){
        return this._height;
    }

    // Every thing works fine now!

    // WITH GETTERS WE CAN EVEN USE THE PROPERTY ACCESSOR THAT DOT TO ACCESS A PROPERTY THAT DOESN'T NECESSARILY EXIST! FOR EXAMPLE:

    get area(){
        return this._width * this._height;
    }
}

```
- See the second example in the video!

## Destructuring 💥
- Destructuring =  extract values from arrays and objects, then assign them to variables in a convenient way
- [] = to perform array destructuring
- {} = to perform object destructuring
- 5 examples
```js
// -----------EXAMPLE 1------------------
// SWAP THE VALUE OF TWO VARIABLES

let a = 1;
let b = 2;

//to need array destructuring, we need straight brackets! []
[a, b] = [b, a]; // on the left, we're destructuring and creating a new array on the RHS

console.log(a); // 2
console.log(b); // 1
```

```js
// -------------EXAMPLE 2----------------
// SWAP 2 ELEMENTS IN AN ARRAY

const colors = ["red", "green", "blue", "black", "white"];
// suppose we want to swap the 1st and the last elements of this array

[colors[0], colors[4]] = [colors[4], colors[0]];
console.log(colors);
```

```js
// -------------EXAMPLE 3-----------------
// ASSIGN ARRAY ELEMENTS TO VARIABLES

const colors = ["red", "green", "blue", "black", "white"];

const [firstColor, secondColor, thirdColor, ...extraColors] = colors;

console.log(firstColor); //  red
console.log(secondColor); // green
console.log(thirdColor); // blue
console.log(extaColors); // ['black', 'white'] (new array!)
```

```js
// -------------EXAMPLE 4--------------------
// EXTRACT VAULES FROM OBJECTS

const person1 = {
    firstName: "Spongebob",
    lastName: "SquarePants", 
    age: 30,
    job: "Fry Cook",
}

const person2 = {
    firstName: "Patrick",
    lastName: "Star", 
    age: 34,
}

const {firstName, lastName, age, job} = person1;
// const {firstName, lastName, age, job} = person2;

console.log(firstName);
console.log(lastName);
console.log(age);
console.log(job); // for person2 it's going to be `undefined`

// using object destructuring, we can reassign elements or set a default value as:
const {firstName, lastName, age, job="unemployed"} = person2;
```

```js
// ----------------EXAMPLE 5---------------------
// DESTRUCTURE IN FUNCTION PARAMETERS

// we can destructure in function parameters, we can pass an object to a function and destructure it when it's passed in!

function displayPerson({firstName, lastName, age, job}){ // here, we are destructuring the object argument that we are receiving!
    console.log(`name: ${firstName} ${lastName}`);
    console.log(`age: ${age}`);
    console.log(`job: ${job}`);
}

const person1 = {
    firstName: "Spongebob",
    lastName: "SquarePants", 
    age: 30,
    job: "Fry Cook",
}

const person2 = {
    firstName: "Patrick",
    lastName: "Star", 
    age: 34,
}

console.log(person1);
/*
    output:
    name: Spongebob SquarePants
    age: 30
    job: Fry Cook
*/

console.log(person2);
/*
    output:
    name: Patrick Star
    age: 34
    job: undefined
*/

// again, we can set the default value!
// function displayPerson({firstName, lastName, age, job="unemployed"})
```
## Nested objects 📫
- nested objects = Objects inside of other Objects.
- Allows you to represnt more complex data structures
- Child Object is enclosed by a Parent Object
- Person{Address{}, ContactInfo{}}
- ShoppingCart{keyboard{}, Mouse{}, Monitor{}}

```js
const person = {
    fullName: "Spongebob Squarepants",
    age: 30,
    isStudent: true,
    hobbies: ["karate", "jellyfishing", "cooking"],
    address: {
        street: "124 Conch st.",
        city: "Bikini Bottom",
        country: "Int. Water"
    }
}

console.log(person.fullName) // property accessor => . (name of the property!)
console.log(person.age);
console.log(person.isStudent);
console.log(person.hobbies[0]);
console.log(person.address.street);
console.log(person.address.city);
console.log(person.address.country);

// We can also loop through the collection as:

for(const property in person.address){
    console.log(person.address[property]);
}
```

```js
// LETS MAKE SOMETHING LITTLE MORE COMPLICATED!
// we're going to create a class that utilizes a nested objects

class Person{

    constructor(name, age, ...address){ // for address we are using the rest parameters (we can pass in different parts of an address and store it within an array.)
        this.name = name;
        this.age = age;
        // now, for the address we are going to construct an address object
        this.address = new Address(...address); // we're gonna call the Constructor of our address class and pass in our address (we've utilized the ...spread operator to spread our address)
    }
}

class Address{
    
    constructor(street, city, country){
        this.street = street;
        this.city = city;
        this.country = country;
    }
}

const person1 = new Person("Spongebob", 30, "124 Conch St.", 
                                             "Bikini Bottom", 
                                             "Int. Waters");

const person2 = new Person("Patrick", 37,   "124 Conch St.", 
                                             "Bikini Bottom", 
                                             "Int. Waters");

const person3 = neww Person("SquidWard", 45, "126 Conch St.", 
                                             "Bikini Bottom", 
                                             "Int. Waters");
                                             
console.log(person1.name); // Spongebob
console.log(person1.age); // 30
console.log(person1.address); // {address object}
console.log(person1.address.street);
```
## Arrays of objects 🍎
```js
const fruits = [{name: "apple", color: "red", calories: 95}, // objects can have their own unique properties
                {name: "orange", color: "orange", calories: 45},
                {name: "banana", color: "yellow", calories: 105},
                {name: "coconut", color: "white", calories: 159},
                {name: "pineapple", color: "yellow", calories: 37},
                ];

console.log(fruits[0].name); // apple
fruits.push({name: "grapes", color: "purple", calories: 62});
fruits.pop(); 
fruits.splice(1, 2); // splice() will remove an elements at certain indices!


// -------------------------forEach()-----------------------------
// we can use the forEach() method to loop through the elements of your array!

fruits.forEach(fruit => console.log(fruit.name));


// ------------------------map()-----------------------------
// the map method will run each element through a function and return a new array

const fruitNames = fruits.map(fruit => fruit.name);

console.log(fruitNames);

// -------------------------filter()--------------------------
// the filter() method will return a new array after using each element and checking a condition

const yellowFruits = fruits.filter(fruit => fruit.color === "yellow");
const lowCalFruits = fruits.filter(fruit => fruit.calories < 100);

console.log(yellowFruits);
console.log(lowCalFruits);

// --------------------------reduce()--------------------------
// the reduce() method will return a single value, in this case an object (one of these objects!)

const maxFruit = fruits.reduce((max, fruit) => 
                                fruit.calories > max.calories ? 
                                fruit :  max);

const minFruit = fruits.reduce((min, fruit) => 
                                fruit.calories < min.calories ? 
                                fruit :  min);

console.log(maxFruit);
console.log(minFruit);

```
## Sorting 🗃
- sort() = method used to sort elements of an array in place. 
- Sorts elements as strings in lexicographic order, not alphabetical 
- lexicographic = (alphabet + numbers + symbols) as strings

```js
//eg, sorting in alphabetical order:
const fruits = ["apple", "orange", "banana", "coconut", "pineapple"];

fruits.sort();

console.log(fruits); // sorted array
```

```js
//eg, sorting numbers:
let numbers = [1, 10, 2, 9, 3, 8, 4, 7, 5, 6];

numbers.sort();

console.log(numbers); // UNEXPECTEDLY!❗❗❗❗❗❗❗❗❗ THE ANSWER IS NOT SORTED NUMBERICALLY!
//output: [1, 10, 2, 3, 4, 5, 6, 7, 8, 9]
// we are sorting it not numberically, but lexicographically!
```

```js
// To sort the numbers array in numberic order, we have to take some extra steps
// Inside the sort() method, we have to write a custom comparison function
// this is normally a callback, but you can write a function expression or even better yet an arrow function
let numbers = [1, 10, 2, 9, 3, 8, 4, 7, 5, 6];

numbers.sort((a,b) => a - b); // our function (a-b) will return a negative zero or a positive value, depending on what values we're examining.
// the sort method will sort those values into place depending on what the value returned is! 

console.log(numbers); // now, the numbers are sorted as required!

// for reverse order , you can write :
numbers.sort((a,b) => b - a);
```

```js
// You can also sort objects by a given property

const people = [
    {name: "Spongbob", age: 30, gpa: 3.0},
    {name: "Patrick", age: 37, gpa: 1.5},
    {name: "Squidward", age: 51, gpa: 2.5},
    {name: "Sandy", age: 27, gpa: 4.0},
]

//we would like to sort this array of objects by each person's age

people.sort((a,b) => a.age - b.age);

console.log(people); //  this sorts the people array by their age! (ofcourse! to reverse it change a.age - b.age in reverse!)
// similarly, we can sort it by gpa and it works fine! but when you try to sort the array by the name property, you will see some logical error! 

// if you need to sort by a property that contains a string within an object , there's a different formula

people.sort((a,b) => a.name.localeCompare(b.name));
// this method will examine two strings for lexicographic order!
// for reverse => b.name.localeCompare(a.name);
```
## Shuffle an array 🔀
- EXTRA LECTURE!!
```js
// Fisher-Yates algorithm

const cards = ['A', 2, 3, 4, 5, 6, 7, 8, 9, 10, 'J', 'Q', 'K'];

shuffle(cards);

console.log(cards);

function shuffle(array){
    for(let i = array.length - 1; i > 0; i--){
        const random = Math.floor(Math.random() * (i + 1));

        [arra[i], array[random]] = [array[random], array[i]];
    }
}
```
## Dates 📅
- Date objects = Objects that contain values that represent dates and times
- These date objects can be changed and formatted
```js
{
    const date = new Date();

    console.log(date); // 2025-10-12T18:19:24.753Z
}

{
    // If you would like to create your own custom date and time object, you'll have to pass in some arguments
    // you should follow this order for the date Constructor!
    // Date(year, month, day, hour, minute, second, ms)
    const date = new Date(2025, 0, 1, 2, 3, 4, 5);
    // passing a string is also valid!
    const date = new Date("2025-01-02T12:00:00z");

    // about epic date in video!

    console.log(date);
}

{
    // you can also extract individual values from a date object!

    const date = new Date();

    const year = date.getFullYear();
    const month = date.getMonth();
    const day = date.getDate(); // if used .getDay() , it will give the day of the week (like monday)
    const hour = date.getHours();
    const minutes = date.getMinutes();
    const seconds = date.getSeconds();
    const dayOfWeek = date.getDay();

    console.log(year);
    console.log(month);
    console.log(day);
}

{
    // now with the date object, we can even set the date with a method!

    const date = new Date();

    date.setFullYear(2024);
    date.setMonth(0);
    date.setDate(1);
    date.setHours(2);
    date.setMinutes(3);
    date.setSeconds(4);
}

{
    // you can even compare dates as well!
    const date1 = new Date("2023-12-31");
    const date2 = new Date("2024-01-01");

    if(date2 > date1){
        console.log("HAPPY NEW YEAR!");
    }
}
```
## Closures 🔒
- closures = A function defined inside of another function, the inner function has access to the variables and scope of the outer function.
- Allow for private variables and state maintenance
- Used frequently in JS frameworks: React, Vue, Angular
- You'll see closures fairly often with function-based components (you have functions inside of other functions!)

```js
function outer(){
    let message = "Hello";

    function inner(){
        console.log(message);
    }

    inner();
}

outer(); // output: Hello

// everything within the outer function is part of a closure (we have a function, inside of a function)

// one of the benefits of closures is that it makes the properties private by encapsulating the variables in the outer function!
```

```js
// closures can also maintain the state of a variable!
{
    function increment(){
        let count = 0;
        count++;
        console.log(`Count increase to ${count}`);
    }

    increment(); // 1
    increment(); // 1
    increment(); // 1 (everytime we invoke this function(), it reassign the count and make it 0!)

    // although, we can make a global count variable but that makes it accessible to everyone! (hence not secure!)
    // so, closures makes variables private as well as allow them to maintain their state!
}

{
    function createCounter(){

        let count = 0;

        function increment(){
            count++;
            console.log(`Count increased to ${count}`);
        }

        return {increment}; // here, we are returning an object and {increment} is a short-hand version of passing the property with it's associate value, i.e., (property:associate) 
        // you can just use the function name for the property!
    }

    const counter = createCounter();

    counter.increment(); // 1
    counter.increment(); // 2
    counter.increment(); // 3 (now works!)

    // counter.count = 0; 
    // console.log(count); // Uncaught ReferenceError! 
    // console.log(counter.count); // undefined!
    // here also we cannot access the private property count! (hence, making it secure, yet modifiable!)
}
{
    // we can have make more functions inside a closure!
    function createCounter(){

        let count = 0;

        function increment(){
            count++;
            console.log(`Count increased to ${count}`);
        }
        
        function getCount(){
            return count;
        }

        return {increment, getCount};
    }

    const counter = createCounter();

    counter.increment();
    counter.increment();
    counter.increment();

    console.log(`The current count is ${counter.getCount()}`);

}
```

```js
{
    // last example!!
    // we're going to create a closure for a game, where we keep track of points!

    let score = 0;

    function increaseScore(points){
        score += points;
        console.log(`+${points}pts`);
    }

    function decreaseScore(points){
        score -= points;
        console.log(`-${points}pts`);
    }

    function getScore(){
        return score;
    }

    increaseScore(5); // +5pts
    increaseScore(6); // +6pts
    decreaseScore(6); // -3pts

    console.log(`The final score is ${getScore()}pts`); // The final score is 8pts

    // the problem with this is: 
    // we can set score to anything!!
    score = 10000000000000;

    // so, for some security! Lets enclose all of this code within a closure
}

{
    // *Bro starts with creating a function that will return an object!
    function createGame(){ // this function acts as a class and returns an object!
        let score = 0;

        function increaseScore(points){
            score += points;
            console.log(`+${points}pts`);
        }

        function decreaseScore(points){
            score -= points;
            console.log(`-${points}pts`);
        }

        function getScore(){
            return score;
        }

        return {increaseScore, decreaseScore, getScore};
    }

    const game = createGame(); // object creation!

    game.increaseScore(5); // +5pts
    game.increaseScore(6); // +6pts
    game.decreaseScore(6); // -3pts
    console.log(`The final score is ${game.getScore()}pts`);

    // now you cannot access the score property from outside!
}
```
## setTimeout() ⏰
- setTimeout() = function in JavaScript that allows you to schedule the execution of a function after an amount of time (milliseconds)
- Times are approximate (varies based on the workload of the JavaScript runtime env.)
- `setTimeout(callback,delay)`
- `clearTimeout(timeoutId) = can cancel a timeout before it triggers`

```js
{
    //eg. 1, 

    function sayHello(){
        window.alert("Hello");
    }

    setTimeout(sayHello, 3000);
}
{
    // an anonymous function works too!
    setTimeout(function(){window.alert("Hello")},3000);

    // using arrow function =>

    setTimeout(() => window.alert("Hello"),3000);
}
{
    // You can use the clear timeout function to cancel a timeout before it triggers! 
    // but we have to pass a (timeoutId)
    const timeoutId = setTimeout(() => window.alert("Hello"),3000);

    clearTimeout(timeoutId); // prints nothing!
}
```

```html
<!-- Now, we'll create a button using HTML -->
 <!-- When we click on the button, we'll set a timeout to display the word "Hello" -->
  <button onClick = "startTimer()">START</button>
  <button onClick = "clearTimer()">CLEAR</button>
```

```js
let timeoutId; // but how this timeoutId initiated?? and with what!!!????

function startTimer(){
    setTimeout(() => window.alert("Hello"), 3000);
    console.log("Started");
}

function clearTimer(){
    clearTimeout(timeoutId);
    console.log("Cleared");
}
```
## Digital Clock program 🕐
- Source code in the video!
## Stopwatch program ⏱
- Source code in the video!
## ES6 Modules 🚢
- ES6 = (a module is...) An external file that contains reusable code that can be imported into other JavaScript files. (any part of a JS file, can be exported for reusability) Write reusable code for many different apps.
- It can contain variables, classes, functions... and more
- Introduced as part of ECMAScript 2015 update
- eg.,

```txt
1. Bro creates a new js file *mathUtil.js*
2. Sets the type attribute to be equal to `module` as below! (So, now our `index.js` file will be treated as a module!)
3. We can import or export other modules freely! But we have to be sure to set this attribute = "module"
```

```html
<body>
    <script type="module" src="index.js"></script>
</body>
```

```js
// mathUtil.js

// Inside our mathUtil module, we can write some reusable code for other programs!

export const PI = 3.14159;

export function getCircumference(radius){
    return 2 * PI * radius;
}

export function getArea(radius){
    return PI * radius * radius;
}

export function getVolume(radius){
    return (4/3) * PI * Math.pow(radius, 3);
    // return 4 * PI * radius * radius // for surface area!
}

// we can reuse these variables and functions for any JavaScript program that we have, by importing them 
// but first we have to export it!
```

```js
// index.js

import {PI, getCircumference, getArea, getVolume} from './mathUtil.js'; 

console.log(PI);
const circumference = getCircumference(10);
const area = getArea(10);
const volume = getVolume(10);

console.log(`${circumference.toFixed(2)}cm`);
console.log(`${area.toFixed(2)}cm^2`);
console.log(`${volume.toFixed(2)}cm^3`);
```
## Asynchronous code 💤
- Synchronous = Executes line by line consecutively in a sequential manner. Code that waits for an operation to complete. (Has order of operation!)

```js
// Example of Synchronous code:
console.log("Task 1");
console.log("Task 2");
console.log("Task 3");
```

- Asynchronous = Allows multiple operations to be performed concurrently without waiting. Doesn't block the execution flow and allows the program to continue (I/O operations, network requests, fetching data). Handled with: Callbacks, Promises, Async/Await

```txt
* Asynchronous code is like a time traveler!
* A time traveler can move out of the flow of time but the rest of the world continues, time resumes normally
* Asynchronous code doesn't block the execution flow
* It is typically found with input output operations, Network requests and fetching data (anything that require an indeterminate amount of time!)
```

```js
// eg. of async:

setTimeout(() => console.log("Task 1"), 3000);

console.log("Task 2");
console.log("Task 3");
```

```js
// There are different ways to handle asychronous code : Callbacks, Promises, Async/Await
// We're Familier with Callbacks, so we'll use it!

function func1(callback){ // asynchronous code!!!
    setTimeout(() => {
        console.log("Task 1");
        callback() // runs after Task 1 is completed!
    }, 3000);
}

function func2(){ // synchronous code!!!
    console.log("Task 2");
    console.log("Task 3");
    console.log("Task 4");
}

func1(func2);

```
- we'll discuss how to handle asynchronous codes via Promises, Async/Await later!
## Error handling ⚠
- Error = An Object that is created to represented a problem that occurs
- Occur often with user input or establishing a connection

```js
{
    // Error eg. 1, : Uncaught TypeError: console.lag is not a function

    console.lag("Hello");

    console.log("You have reached the end!"); // this line doesn't executes!
    // hence, Errors when they are Uncaught interrupt the normal flow of our program!!
}

{
    // Error eg. 2, : Uncaught ReferenceError: x is not defined!
    console.log(x);

    console.log("You have reached the end!");
}
{
    // Errors can be generated due to various reasons!
    // NETWORK ERRORS
    // PROMISE REJECTION
    // SECURITY ERRORS
}
```

- we can handle these errors via error handling! (using...)
- try { } = Encloses code that might potentially cause an error
- catch { } = Catchand handle any thrown Errors from try { }
- finally { } = {optional} Always executes. Used mostly for clean up
- ex. close files, close connections, release resources

```js
{
    try{
        console.log(x);
    }
    catch(error){
        // console.log(error); //for displaying errors, always use console.error()
        console.error(error); // this highlights the error!
    }
    finally{
        // CLOSE FILES
        // CLOSE CONNECTIONS
        // RELEASE RESOURCES
        console.log("This always executes");
    }
    console.log("You have reached the end!"); // now, we have reached the end!
}
{
    // Errors can also occur when accepting user input! bcoz we don't know what users gonna type in!
    // In the worst case, it can be a malicious script!
    const dividend = window.prompt("Enter a dividend: ");
    const divisor = window.prompt("Enter a divisor: ");

    const result = dividend/ divisor;
    console.log(result); // works fine but number/ 0 is mathematically incorrect! (prints: infinity!)
}

{
    // fixed!
    try{
        const dividend = Number(window.prompt("Enter a dividend: "));
        const divisor = Number(window.prompt("Enter a divisor: "));

        // within the try block, (in certain situations) we can intentionally cause an error!
        if(divisor === 0){
            throw new Error("You can't divide by zero!"); // we're calling the error constructor to construct a new error objecct!
        }

        // users can also input in a string (like pizza) instead of a number! 
        // for that case, we've type-casted our dividend and divisor and handle that error below!
        if(isNaN(dividend) || isNaN(divisor)){
            throw new Error("Values must be a number!");
        }

        const result = dividend/ divisor;
        console.log(result);
    }
    catch(e){
        console.error(e);
    }
}
```
## Calculator program 🖩
- Source code in the video!
## What is the DOM? 🌳
- DOM = DOCUMENT OBJECT MODEL
- Object{} that represents the page you see in the web browser and provides you with an API to interact with it.
- Web browser constructs the DOM when it loads an HTML document, and structures all the elements in a tree-like representation.
- JavaScript can access the DOM to dynamically change the content, structure, and style of a web page.
- `document.getElementById("myH1");` Document here is an object, it contains properties and methods and other nested objects!

```js
console.log(document); // it will display the html document!
console.dir(document); // list all the properties of this object

// we can access this object and change it's properties! eg,

document.title = "My website";
console.dir(document); // check the title!
{
    // we can change the background as:
    document.body.style.backgroundColor = "hsl(0, 0%, 15%)";
    // we have dynamically changed the style property without using css!
}
```
```html
<h1 id="welcome-msg">Welcome</h1>
<script src="index.js"></script>
```
```js
// we are conditionally going to change the username!

const username = "Bro code";
const welcomeMsg = document.getElementById("welcome-msg");

welcomeMsg.textContent += username === "" ? `Guest` : username;
```

```txt
when username is empty:
    Welcome Guest

when username is `something`:
    welcome something
```
## Element selectors 📑
- Element selectors = Methods used to target and manipulate HTML elements 
- They allows you to select one or multiple HTML elements from the DOM (Document Object Model)

```txt
// built-in methods
1. document.getElementById() // returns... ELEMENT OR NULL
2. document.getElementsClassName() // HTML COLLECTION
3. document.getElementsByTagName() // HTML COLLECTION
4. document.querySelector() // ELEMENT OR NULL
5. document.querySelectorAll() // NODELIST
```

- example 1: document.getElementById()
```html
<h1 id="my-heading">Food R Us</h1>
<sript src = "index.js"></script>
```
```js
const myHeading = document.getElementById("my-heading"); // this const stores a reference to this element id = 'my-heading' (we're accessing the DOM with `document` keyword)
myHeading.style.backgroungColor = "yellow"; // if we're accessing the CSS properties in JS , they have a camelCase naming convention but in CSS it has a hyphen-ated naming convention!
myHeading.style.textAlign = "center";

console.log(myHeading); // it displays our HTML element (including style), rather than `Food R Us`

//it returns null in case of wrong id!

```

- example 2: document.getElementsClassName()
- It's returns an HTML collection (similar to an array but limited to it's built-in methods!)
```html
<body>
    <h1 id="my-heading">Food R Us</h1>

    <div class="fruits">Apple</div>
    <div class="fruits">orange</div>
    <div class="fruits">banana</div>

    <sript src = "index.js"></script>
</body>
```

```js
    const fruits = document.getElementByClassName("fruits");

    console.log(fruits); // outputs: HTML collection with textContent = Apple, orange, banana

    // we can access these elements via index!
    fruits[0].style.backgroundColor = "yellow"; 

    // we can also iterate through these elements! (ie, HTML collections are iterable!)
    for(let fruit of fruits){
        fruit.style.backgroudColor = "yellow";
    }

    // HTML collections ,although, are like arrays but is limited!
    fruits.forEach(); // (using array method) this will raise an Uncaught TypeError: fruits.forEach is not a function!

    // for this, we first need to type-caste the html collection to an array!
    Array.from(fruits).forEach(fruit => {
        fruit.style.backgroundColor = "yellow";
    }); // works fine!
```
- example 3 : document.getElementsByTagName()
```html
<h4>Root Vegetables</h4>
<ul>
    <li>Beats</li>
    <li>Carrots</li>
    <li>Potatoes</li>
</ul>

<h4>Non-Root Vegetables</h4>
<ul>
    <li>Broccoli</li>
    <li>Celery</li>
    <li>Onions</li>
</ul>

```
```js
const h4Elements = document.getELementsByTagName("h4");
const liElement = document.getELementsByTagName("li");

// console.log(h4Elements); // output: 2 HTML collections

h4Elements[0].style.backgroundColor = "yellow";

// to highlight all, we can use the enhanced for loop!
for(let h4Element of h4Elements){
    h4Element.style.backgroundColor = "yellow";
}

for(let liElement of liElements){
    liElement.style.backgroundColor = "lightgreen";
}

// similarly, we can type caste it and use the array methods on it!

```

- example 4: document.querySelector() 
- querySelector will return the first matching element or null if it doesn't find any matches!

```js
const element = document.querySelector(".fruits"); // to select an element by a class name, we'll use `dot` (".") `the name of the class` (eg, .fruits)

element.style.backgroundColor = "yellow"; // it will highlight Apple only (since, it only selects the first match!)

// change .fruits to h4 (it'll only highlight the Root vegetables, although we have two h4)
// similarly, try to select li, ul and observe the results
// also, try to select something that doesn't exists (like ol) and observe the result!
```
- example 5: document.querySelectorAll()
- It returns a NodeList
- A node list is similar to an HTML collection expect it has built-in methods similar to arrays
- However, node lists are static, HTML collections are live 
- Since node lists are static, they do not update automatically in the DOM
- HTML collections are live, they will!
```js
const fruits = document.querySelectorAll(".fruits");
const foods = document.querySelectorAll("li");

fruits[0].style.backgroundColor = "yellow"; // works the same as above

console.log(foods); // outputs a node list (with forEach built-in method!)
// so, now we don't need to type caste it

foods.forEach(food => {
    food.style.backgroundColor = "yellow"; // observe the results!
});
```
## DOM navigation 🧭
- DOM Navigation = The process of navigating through the structure of an HTML document using JavaScript.
```txt
.firstElementChild
.lastElementChild
.nextElementSibling
.previousElementSibling
.parentElement
.children
```

```html
<ul id="fruits">
    <li>apple</li>
    <li>orange</li>
    <li>banana</li>
</ul>

<ul id="vegetables">
    <li>carrots</li>
    <li>onions</li>
    <li>potatoes</li>
</ul>

<ul id="desserts">
    <li>cake</li>
    <li>pie</li>
    <li>ice cream</li>
</ul>

```
```js
// ---------------------.firstElementChild------------------------

const element = document.getElementById("desserts");
const firstChild = element.firstElementChild;
firstChild.style.backgroundColor = "yellow"; // highlights cake

{
    const ulElements = document.querySelectorAll("ul");

    ulElements.forEach(ulElement => {
        const firstChild = ulElement.firstElementChild;
        firstChild.style.backgroundColor = "yellow";
    }); // highlights all first elements under ul
}

```

```js
// ----------------------.lastElementChild-----------------------

const element = document.getElementById("fruits");
const lastChild = element.lastElementChild;
lastChild.style.backgroundColor = "yellow";
// make a small project that highlights these list items with arrow keys!
{
    const ulElements = document.querySelectorAll("ul"); // returns a node list (unordered)

    ulElements.forEach(ulElement => {
        const lastChild = ulElement.lastElementChild;
        lastChild.style.backgroundColor = "yellow";
    });
}
```

- next we have : .nextElementSibling
- for this, we'll make some changes in our html :
```html
<!-- giving each li, a unique id -->
<ul id="fruits">
    <li id="apple">apple</li>
    <li id="orange">orange</li>
    <li id="banana">banana</li>
</ul>

<ul id="vegetables">
    <li id="carrots">carrots</li>
    <li id="onions">onions</li>
    <li id="potatoes">potatoes</li>
</ul>

<ul id="desserts">
    <li id="cake">cake</li>
    <li id="pie">pie</li>
    <li id="ice cream">ice cream</li>
</ul>

```

```js
// ---------------------------.nextElementSibling--------------------

const element = document.getElementById("banana"); 
const nextSibling = element.nextElementSibling;
nextSibling.style.backgroundColor = "yellow";
// try to select ul ie fruits/ vegetables ... and find out!

```

```js
// ---------------------------.previousElementSibling--------------------

const element = document.getElementById("banana"); 
const prevSibling = element.previousElementSibling;
prevSibling.style.backgroundColor = "yellow";
// try to select ul ie fruits/ vegetables ... and find out!

```

```js
// ---------------------------.parentElement--------------------

const element = document.getElementById("orange"); 
const parent = element.parentElement;
parent.style.backgroundColor = "yellow";

```

```js
// ---------------------------.children--------------------

const element = document.getElementById("fruits"); 
const children = element.children;
children.style.backgroundColor = "yellow";

Array.from(children).forEach(child => {
    child.style.backgroundColor = "yellow";
});

// we can even access these children by it's index number!
// eg.,

children[1].style.backgroundColor = "yellow";
```

## Add & change HTML 🛠️
```js
// -------------------- EXAMPLE 1 <h1> --------------------

// STEP 1 CREATE THE ELEMENT

// STEP 2 ADD ATTRIBUTES/PROPERTIES

// STEP 3 APPEND ELEMENT TO DOM

// REMOVE HTML ELEMENT
```

```html
<div id= "box1" class = "box">
    <p>Box1</p>
</div>

<div id= "box2" class = "box">
    <p>Box2</p>
</div>

<div id= "box3" class = "box">
    <p>Box3</p>
</div>

<div id= "box4" class = "box">
    <p>Box4</p>
</div>

```

```css
.box{
    border: 3px solid;
    width: 100%;
    height: 125px;
}
```

```js
// -------------------- EXAMPLE 1 <h1> --------------------

// STEP 1 CREATE THE ELEMENT
const newH1 = document.createElement("h1");
newH1.id = "myH1";
newH1.style.color = "tomato";
newH1.style.textAlign = "center";

// STEP 2 ADD ATTRIBUTES/PROPERTIES
newH1.textContent = "I like pizza!";

// STEP 3 APPEND ELEMENT TO DOM
document.body.append(newH1); // this appends a new element with textContent = I like pizza!
document.body.prepend(newH1); // see what it does!
{
    // now we'll append this newH1 in the box1
    document.getElementById("box1").append(newH1); // similarly, box2, box3...
    // now , if this box previously contained a child (which it does!) , this newH1 will be appended after it! (ie, new child is always appended at the last!)
    // if we want it to be the first child , we can prepend it!
}
{
    document.getElementById("box1").prepend(newH1);
}
{
    // if we want to insert it in between of box1 and box2:
    const box2 = document.getElementById("box2");
    document.body.insertBefore(newH1,box2); // (newElement, currentElement)
}
{
    // we can even do this without using the element id!
    const boxes = document.querySelectorAll(".box");
    boxes.body.insertBefore(newH1, boxes[2]);
}
// REMOVE HTML ELEMENT (this is optional!)
document.body.removeChild(newH1); // works when the newH1 is in the body
{
    // in the case, this newH1 being in one of the boxes!
    document.getElementById("box1").removeChild(newH1);
}
```

```js
// CHECK 2ND EXAMPLE IN THE VIDEO!
```
## Mouse events 🖱
- eventListener = Listen for specific events to create interactive web pages
- events: click, mouseover, mouseout
- `.addEventListenerF(event, callback);` 

```html
<div id="myBox">
    Click Me 😎
</div>
```

```css
#myBox{
    background-color: lightgreen;
    width: 300px;
    height: 300px;
    font-size: 4.5rem; /* 4.1 is better! */
    font-weight: bold;
    display: flex;
    align-items: center;
    text-align: center;
}
```

```js
const myBox = document.getElementById("myBox");

function changeColor(event){ // event is an object, it is provided automatically by the web browser when something happends (when some event occurs, like mouse-click!)

    // temporarily, we'll console log it!
    console.log(event); // when we clicked on that box, the web browser provided us with an event object (it's a pointer event!)
    // this object contains details about what happened exactly!
    // for example, we have the target => what did we click on! 
    // [target: div#myBox shows we clicked on the div element with id = myBox]

    // After this line-----------> comment the above console.log();
    event.target.style.backgroundColor = "tomato";
    event.target.textContent = "OUCH!😣";

}

myBox.addEventListener("click", changeColor);

{
    // now , in this block of code, we'll use the anonymous function instead of callback!
    const myBox = document.getElementById("myBox");

    // myBox.addEventListener("click", function(event){
    //     event.target.style.backgroundColor = "tomato";
    //     event.target.textContent = "Ouch!";
    // }));

    myBox.addEventListener("click", event => {
        event.target.style.backgroundColor = "tomato";
        event.target.textContent = "Ouch!";        
    });

    // now so other event listeners=>
    myBox.addEventListener("mouseover", event =>{
        event.target.style.backgroundColor = "yellow";
        event.target.textContent = "Don't do it! 🤨";  
    });

    myBox.addEventListener("mouseout", event =>{
        event.target.style.backgroundColor = "tomato";
        event.target.textContent = "Ouch!";    
    });
}
```

- Now, tryna implement this effect using a button yourself!😁
## Key events ⌨
- eventListener = Listen for specific events to create interactive web pages 
- events: keydown, keyup, keypress (according to the official documentation, this last event is't compatible with all web browsers, so you should avoid using keypress)
- `document.addEventListener(event, callback);`

```js
document.addEventListener("keydown", event => {
    console.log(event); // tryna press a key and check console of your browser!
    // pressed `q` key
    // the web browser provided us with a keyboard event

    console.log(event.key);
});

{
    document.addEventListener("keydown", event => {
        console.log(`Key down = ${event.key}`);
    });

    document.addEventListener("keyup", event => {
        console.log(`Key up = ${event.key}`);
    });
}
```

- Now, we'll do a cool thing! (as always!😎)
```html
<div id="myBox">😀</div>
```

```css
body{
    margin: 0;
}
#myBox{
    background-color: lightblue;
    width: 200px;
    height: 200px;
    font-size: 7.5rem;
    display: flex;
    justify-content: center;
    align-items: center;
    position: relative;
    /* this last one  is very important for positioning! */
}
```
```js
const myBox = document.getElementById("myBox");

document.addEventListener("keydown", event => {
    myBox.textContent = "😲";
    myBox.style.backgroundColor = "tomato";
});

document.addEventListener("keyup", event => {
    myBox.textContent = "😀";
    myBox.style.backgroundColor = "lightlue";
});

// now, when pressing a key and holding will change the box and releasing will reset it back to original!

```
```js
// now in this next example, we will make the box move!
const myBox = document.getElementById("myBox");
const moveAmount = 10;
let x = 0;
let y = 0;

document.addEventListener("keydown", event => {

    if(event.key.startsWith("Arrow")){

        event.preventDefault();

        switch(event.key){
            case "ArrowuUp": 
                y -= moveAmount;
                break;
            case "ArrowDown":
                y += moveAmount;
                break;
            case "ArrowLeft":
                x -= moveAmount;
                break;
            case "ArrowRight":
                x += moveAmount;
                break;
        }

        myBox.style.top = `${y}px`;
        myBox.style.left = `${x}px`;
    }
});

// now try to merge these last two projects together!
```
## Hide/show HTML 🖼
- for this, you'll need an image to work with (we'll make it show or hide in our html!)
```html
<button id="myButton">Hide</button><br>

<img id="myImg" src="car.jpg" width="400px">
```
```css
#myButton{
    font-size:2rem;
}
```
```js
const myButton = document.getElementById("myButton");
const myImg = document.getElementById("myImg");

myButton.addEventListener("click", event => {
    // we will toggle between hide and show button!

    if(myImg.style.display === "none"){
        myImg.style.display = "block";
        myButton.textContent = "Hide";
    }
    else{
        myImg.style.display = "none";
        myButton.textContent = "Show";
    }

    {
        // you can also set the space reserved for the image when it hides!
        if(myImg.style.visibility === "hidden"){
            myImg.style.visibility = "visibility";
            myButton.textContent = "Hide";
        }
        else{
            myImg.style.visibility  = "hidden";
            myButton.textContent = "Show";
        }
    }

});
```
## NodeLists 📃
- NodeList = Static collection of HTML elements by (id, class, element)
- Can be created by using querySelectorAll()
- Similar to an array, but no (map, filter, reduce) `they do have a forEach() method tho!`
- NodeList won't update to automatically reflect changes
- eg.1, 

```html
<button class="myButtons">Button 1</button>
<button class="myButtons">Button 2</button>
<button class="myButtons">Button 3</button>
<button class="myButtons">Button 4</button>
```

```css
/* Little bit css!*/
.myButtons {
    font-size: 4rem;
    margin: 10px;
    border: none;
    border-radius: 5px;
    padding: 10px 15px;
    background-color: hsl(202,100%, 60%);
    color: white;
}
```
- one way in which we can create a NodeList is by using querySelectorAll() `{as already have been discussed}` but we'll see few more advanced things we can do with NodeLists!
- We can select Elements by an ID, a class or an element type
- we will create a NodeList of let buttons....

```js
let buttons = document.querySelectorAll(".myButtons"); // we can also pass in here the element button or an id!

// now we'll just console.log() it, to see our NodeList of buttons!
console.log(buttons);

/*
* In the console window, we do have a length property, a few methods (entries, forEach, item,...)
*
* Now we'll change the HTML and CSS properties of all elements within a NodeList
*/

// CHANGING HTML AND CSS USING NODELIST🚀🚀🚀🚀🚀

buttons.forEach(button => {
    button.style.backgroundColor = "green"; // color changes to green
    button.textContent += "😀";
});

// CLICK EVENT LISTENER

buttons.forEach(button => {
    button.addEventListener("click", event => {
        event.target.style.backgroundColor = "tomato";
    });
});

// EVENT LISTENER FOR MOUSEOVER + MOUSEOUT

buttons.forEach(button => {
    button.addEventListener("mouseover", event => {
        event.target.style.backgroundColor = "hsl(205, 100%, 40%)";
    });
});

buttons.forEach(button => {
    button.addEventListener("mouseout", event => {
        event.target.style.backgroundColor = "hsl(205, 100%, 60%)";
    });
});

// ADD AN ELEMENT

const newButton = document.createElement("button"); // STEP 1 (create new element)
newButton.textContent = "Button 5"; // STEP 2 (add properties)
newButton.classList = "myButtons"; // when working with Element's class we work with classList✔️ not class! ❌
document.body.appendChild(newButton); // STEP 3 (append this element to DOM!) (important thing here! watch in the video!)

// now if we console.log() our NodeList again
console.log(buttons); 
// it will still show 4 buttons! (as previous!)
// this is because, NodeLists are a static collection, they won't update automatically to reflect changes to the DOM
// Even though button five is within the DOM we would need to manually add it to our NodeList, if we want to work with it
// So to do that, we can just use querySelectorAll() again and select all elements by the class
// since, we are reassigning buttons that's why i declared buttons with let instead of const 
// comment console.log(buttons) after this line------------------------------

buttons = document.querySelectorAll(".myButtons");

console.log(buttons); // now NodeList has 5 elements!

// REMOVE AN ELEMENT

buttons.forEach(button => {
    button.addEventListener("click", event => {
        event.target.remove();
        // even if you remove all the buttons, the nodelist will show 4 elements! (if you console.log(buttons) at this point! (to fix this, you again have to reassign buttons or update it mannually!)
        buttons = document.querySelectorAll(".myButtons"); // now works fine! ✔️
    });
});
```
## classList 🧾
- classList = Element property in JavaScript used to interact with an element's list of classes (CSS classes), Allows you to make reusable classes for many elements across your webpage.

- add()
- remove()
- toggle(Remove if present, Add if not)
- replace(oldClass, newClass)
- contains()
- eg., 

```html
<button id="myButton">My button</button>
```
<!-- We'll add little bit css first! -->

```css
#myButton {
    font-size: 4rem;
    margin: 10px;
    border: none;
    border-radius: 5px;
    padding: 10px 15px;
}

/* we'll create a class selector and we'll apply this class to this button using JavaScript */

.enabled {
    background-color: hsl(204, 100%, 50%);
    color: white;
}

/* so, the above button doesn't have this class yet!
*  we'll add this dynamically using JavaScript!
*/

.hover {
    box-shadow: 0 0 10px hsla(0, 0%, 0%, 0.2);
    font-weight: bold;
}
```

```js
// first, we'll create a reference to this button!
const myButton = document.getElementById("myButton");

myButton.classList.add("enabled"); // this will dynamically add the class, unlike NodeList!
myButton.classList.remove("enabled"); // to remove the class!

// now with .hover class!
myButton.classList.add("hover"); // works fine but now we'll add an eventListener for mouseover with this effect!
// (comment the above loc!)
myButton.addEventListener("mouseover", event => {
    event.target.classList.add("hover");
});

myButton.addEventListener("mouseout", event => {
    event.target.classList.remove("hover");
});

// THERE IS ALSO TOGGLE!------------------------------------------
/*
* if we toggle a class, we'll remove it! if the class is present, add that class!, if it's not!
* so let's replace .add() with .toggle() in the above LOC!
*/

{
    myButton.addEventListener("mouseover", event => {
        event.target.classList.toggle("hover");
    });

    myButton.addEventListener("mouseout", event => {
        event.target.classList.toggle("hover");
    });
}

// now we're going to use the replace method to replace one class with another!
// we'll create a new class of .disabled!
```

```css
.disabled {
    background-color: hsl(0, 0%, 60%);
    color: hsl(0, 0%, 80%);
}
```

```js
const myButton = document.getElementById("myButton");

myButton.classList.add("enabled");

myButton.addEventListener("click", event => {
    event.target.classList.replace("enabled", "disabled");
});
```
<!-- Then we hae the contains() method! 
     if an element contains a class, this will return true and if it doesn't, it returns false!    
-->

```js
const myButton = document.getElementById("myButton");

myButton.classList.add("enabled");

myButton.addEventListener("click", event => {

    if(event.target.classList.contains("disabled")){
        event.target.textContent += "🤬";
    }else{
        event.target.classList.replace("enabled", "disabled"); // if we click and disable our button twice, this append will happen!
    }
});
```
- Now the nice thing about using classList, elements have a class list property we can reuse CSS classes amongst many HTML elements
- We'll create an H1 element now!
- please note that these codes below, are additions to the above HTML, CSS, JS file!

```html
<h1 id="myH1">Hello</h1>
```
```css
#myH1 {
    font-size: 5rem;
}
```
```js
const myH1 = document.getElementById("myH1");

myH1.classList.add("enabled"); // with just this bear LOC, we've added the enabled css property to it!

myH1.addEventListener("click", event => {

    if(event.target.classList.contains("disabled")){
        event.target.textContent += "🤬";
    }else{
        event.target.classList.replace("enabled", "disabled"); // if we click and disable our button twice, this append will happen!
    }
});
```
- check the challenge round! @ 9:53:30
## Rock Paper Scissors 👊
- Find the Source code in the video!
## Image Slider 🖼️
- Find the Source code in the video!
## Callback Hell? 🔥
- Callback Hell : Situation in JavaScript where callbacks are nested within other callbacks to the degree where the code is difficult to read. (If you nest too many callbacks with another callbacks, you code starts to form a pyramid and it's really difficult to work with!)
- Old pattern to handle asynchronous functions. 
- Use Promises + async/await to avoid Callback Hell
- Eg. of Synchronous code:
```js
function task1(){
    console.log("Task 1 complete");
}

function task2(){
    console.log("Task 2 complete");
}

function task3(){
    console.log("Task 3 complete");
}

function task4(){
    console.log("Task 4 complete");
}

task1();
task2();
task3();
task4();
console.log("All tasks complete!");
// runs synchronously! but what if these were aschynchronous?
```

```js
function task1(){
    setTimeout(() => {
        console.log("Task 1 complete");
    }, 2000);
}

function task2(){
    setTimeout(() => {
        console.log("Task 2 complete");
    }, 1000);
}

function task3(){
    setTimeout(() => {
        console.log("Task 3 complete");
    }, 3000);
}

function task4(){
    setTimeout(() => {
        console.log("Task 4 complete");
    }, 1500);
}

task1();
task2();
task3();
task4();
console.log("All tasks complete!");
/*
* OUTPUT: 
    All tasks complete
    Task 2 complete
    Task 4 complete
    Task 1 complete
    Task 3 complete
*/

//  That's the problem with aschynronous code! they can be completed in any time! The rest of the program doesn't for them to be finished!
// IF we absolutely need our tasks to be complete in order, we can use callback! as:

```

```js
function task1(callback){
    setTimeout(() => {
        console.log("Task 1 complete");
        callback();
    }, 2000);
}

function task2(callback){
    setTimeout(() => {
        console.log("Task 2 complete");
        callback();
    }, 1000);
}

function task3(callback){
    setTimeout(() => {
        console.log("Task 3 complete");
        callback();
    }, 3000);
}

function task4(callback){
    setTimeout(() => {
        console.log("Task 4 complete");
        callback();
    }, 1500);
}

function task5(callback){
    setTimeout(() => {
        console.log("Task 5 complete");
        callback();
    }, 3500);
}

function task6(callback){
    setTimeout(() => {
        console.log("Task 6 complete");
        callback();
    }, 1700);
}

// callback hell🔥🔥
task1(() => {
    task2(() => {
        task3(() => {
            task4(() => {
                task5(() => {
                    task6(() => {
                        console.log("All task complete!");
                    });
                });
            });
        });
    });
});

// It's a old pattern to handle asynchronous functions!
```
- After 4 levels of nested callbacks, it becomes really difficult to manage or read/understand or to work with, that's why we should avoid callback hells!
- To avoid callback hells, we use Promises or Async/Await
## Promises 🤞
- Promise = An Object that manages asynchronous operations (such as querying a database, fetching a file, Gathering resources etc... , Asynchronous code basically takes an indeterminate amount of time). Wrap a Promise Object around {asynchronous code} 
- "I promise to return a value"
- PENDING -> RESOLVED or REJECTED
- new Promise((resolve, reject) => {asynchronous code})

```txt
DO THESE CHORES IN ORDER

1. WALK THE DOG
2. CLEAN THE KITCHEN
3. TAKE OUT THE TRASH
```

```js
// first we'll do this using the callback functions!

function walkDog(callback){
    setTimeout(() => {
        console.log("You walk the dog 🦮");
        callback();
    }, 1500);
}

function cleanKit(callback){
    setTimeout(() => {
        console.log("You clean the kitchen");
        callback();
    }, 2500);
}

function takeOutTrash(callback){
    setTimeout(() => {
        console.log("You take out the trash");
        callback();
    }, 500);
}

walkDog(() => {
    cleanKtchen(() => {
        takeOutTrash(() => console.log("You finished all the chroes!"));
    });
});

```

- Now with promises!
- With all of these async code, we'll wrap it within a promise by using a promise, we don't need callbacks!
- Instead of using callbacks, we'll use method chaining!
- We'll method chain our promises! here's how =>

```js
// how we'll modify these functions is that at the end of each function, we will return an object. 
// return new Promise(); and follow the given formula [new Promise((resolve, reject) => {...async code!}]

function walkDog(){

    return new Promise((resolve, reject) => {
        // Do all the asynchronous code!.. (remove the callback!)
        // If we'd like to display a message when the promise resolves, when it finishes successfully, we will instead call the resolve parameter [resolve is a function and "you walk the dog" instead of it, is the value!]
        setTimeout(() => {
            resolve("You walk the dog 🦮");
        }, 1500);        
    });
}

function cleanKit(){
    return new Promise((resolve, reject) => {
        setTimeout(() => {
            resolve("You clean the kitchen");
        }, 2500);
    });
}

function takeOutTrash(){
    return new Promise((resolve, reject) => {
    setTimeout(() => {
        resolve("You take out the trash");
    }, 500);
    });
}

// we no longer need to use callback hell! we'll instead use method chaining!

// walkDog().then(value => console.log(value)); // this prints only "You walk the dog"

walkDog().then(value => {console.log(value); return cleanKitchen()})
         .then(value => {console.log(value); return takeOutTrash()})
         .then(value => {console.log(value); console.log("You finished all the chores!")});

// Now, it's lot easier to work with, then nesting callbacks!

```
- Now, sometimes with asynchronous functions depending on the task, the task may Fail! 
- Let's say we're trying to locate a resource (a file), if we can't locate that file and we're using promises we don't want to resolve that promise, because we couldn't locate that file! Instead, we want to reject!
- That's what happens when an asynchronous function fails to do something, when inside a promise! so let's change our functions around!

```js
function walkDog(){

    return new Promise((resolve, reject) => {
        setTimeout(() => {

            const dogWalked = true;

            if(dogWalked){
                resolve("You walk the dog 🦮");
            } else {
                reject("You DIDN'T walk the dog!");
            }

        }, 1500);        
    });
}

function cleanKit(){
    return new Promise((resolve, reject) => {
        setTimeout(() => {

            const kitchenCleaned = true;

            if(kitchenCleaned){
                resolve("You clean the kitchen");
            } else{
                reject("You DIDN't clean the kitchen");
            }
        }, 2500);
    });
}

function takeOutTrash(){
    return new Promise((resolve, reject) => {
    setTimeout(() => {

        const trashTakenOut = false;

        if(trashTakenOut){
            resolve("You take out the trash");
        } else{
            reject("You DIDN't take out the Trash");
        }

    }, 500);
    });
}

// If a promise might reject!, there's one more method we need to add to the end of this chain!

walkDog().then(value => {console.log(value); return cleanKitchen()})
         .then(value => {console.log(value); return takeOutTrash()})
         .then(value => {console.log(value); console.log("You finished all the chores!")})
         .catch(error => console.error(error));

```
```output
/*
* OUTPUT: 
    You walked the dog
    You clean the kitchen
    ❗❗❗ERROR: You DIDN'T take out the trash!
*/

// if the first task was false! (and rest all are true!), or if the first promise is rejected then we even attempt to resolve these other promises!

```

## Async/Await ⏳
- Async/Await = `Async = makes a function return a promise`  `Await = makes an async function wait for a promise`

- Allows you write asynchronous code in a synchronouse manner
- Async doesn't have resolve or reject parameters
- Everything after Await is placed in an event queue

```js
function walkDog(){

    return new Promise((resolve, reject) => {
        setTimeout(() => {

            const dogWalked = true;

            if(dogWalked){
                resolve("You walk the dog 🦮");
            } else {
                reject("You DIDN'T walk the dog!");
            }

        }, 1500);        
    });
}

function cleanKit(){
    return new Promise((resolve, reject) => {
        setTimeout(() => {

            const kitchenCleaned = true;

            if(kitchenCleaned){
                resolve("You clean the kitchen");
            } else{
                reject("You DIDN't clean the kitchen");
            }
        }, 2500);
    });
}

function takeOutTrash(){
    return new Promise((resolve, reject) => {
    setTimeout(() => {

        const trashTakenOut = false;

        if(trashTakenOut){
            resolve("You take out the trash");
        } else{
            reject("You DIDN't take out the Trash");
        }

    }, 500);
    });
}

async function doChores(){

    try{
        const walkDogResult = await walkDog();
        console.log(walkDogResult);

        const cleanKitchenResult = await cleanKitchen();
        console.log(cleanKitchenResult);

        const takeOutTrashResult = await takeOutTrash();
        console.log(takeOutTrashResult);

        console.log("You finished all the chores!");
    }
    catch(error){
        console.error(error);
    }
}

doChores();

```
## JSON files 📄
- JSON = (JavaScript Object Notation) data-interchange format
- Used for exchanging data between a server and a web application
- JSON files {key:value} OR [value1, value2, value3]

- JSON.stringify() = converts a JS object to a JSON string.
- JSON.parse() = converts a JSON string to a JS object

```json
// names.json
// array!
["Spongebob", "Patrick", "Squidward", "Sandy"] // this is a valid json format!
```

```json
// person.json
// object!
{
    "name" : "Spongebob",
    "age" : 30, 
    "isEmployed" : true,
    "hobbies" : ["Jellyfishing", "karate", "cooking"]
} // this is also a valid format (objects can even have arrays as one of their values as above)
```

```json
// people.json
// this will be an array of objects!
[{
    "name" : "Spongebob",
    "age" : 30, 
    "isEmployed" : true
},
{
    "name" : "Patrick",
    "age" : 34, 
    "isEmployed" : false
},
{
    "name" : "Squidward",
    "age" : 50, 
    "isEmployed" : true
},
{
    "name" : "Sandy",
    "age" : 27, 
    "isEmployed" : false
}]
```
- JSON.stringify() = converts a JS object to a JSON string.
- JSON.parse() = converts a JSON string to a JS object

- So, Json formats, they're one long string to represent that object or array.
- Using the stringify() method of JSON, we can convert a JS object or an array into a JSON string!

```js
// so let's copy the array of names!
const names = ["Spongebob", "Patrick", "Squidward", "Sandy"];

// we'll convert it to a Json string!
const jsonString = JSON.stringify(names); // JSON is a built-in object that's provided to us to work with Json

console.log(names); // If we console.log() our names before stringifying it, we will have an array of strings to work with!
/*
*   OUTPUT:
*       (4) ['Spongebob', 'Patrick' , 'Squidward', 'Sandy'] 
          0: "Spongebob"
          1: "Patrick"
          2: "Squidward"
          3: "Sandy"
          length: 4 
*/

console.log(jsonString);// after using stringify() method on names, we'll be given one long string to represent this array!
/*
*  OUTPUT:
    ["Spongebob", "Patrick" , "Squidward", "Sandy"]
*/

{
    // if we were to use this on an object =>
    const person = {
    "name" : "Spongebob",
    "age" : 30, 
    "isEmployed" : true,
    "hobbies" : ["Jellyfishing", "karate", "cooking"]
    };

    const jsonString = JSON.stringify(person);

    console.log(person);
    console.log(jsonString);

}

{
    // let's stringify our people it'san array of objects!
    const people = [{
    "name" : "Spongebob",
    "age" : 30, 
    "isEmployed" : true
},
{
    "name" : "Patrick",
    "age" : 34, 
    "isEmployed" : false
},
{
    "name" : "Squidward",
    "age" : 50, 
    "isEmployed" : true
},
{
    "name" : "Sandy",
    "age" : 27, 
    "isEmployed" : false
}];

// console.log(people) before it!
    const jsonString = JSON.stringify(people);
    console.log(jsonString); // one extremely long string!
}

```

- Now, we'll use JSON.parse() which converts a JSON string to a JS object!

```js
// you just need to enclose the JS object within `` to parse it in a string!
const jsonNames = `["Spongebob", "Patrick", "Squidward", "Sandy"];`
const jsonPerson = `{ "name" : "Spongebob", "age" : 30, "isEmployed" : true,"hobbies" : ["Jellyfishing", "karate", "cooking"] };`
const jsonPeople = `[{ "name" : "Spongebob", "age" : 30, "isEmployed" : true },
                 { "name" : "Patrick", "age" : 34, "isEmployed" : false },
                 { "name" : "Squidward", "age" : 50, "isEmployed" : true },
                 { "name" : "Sandy", "age" : 27, "isEmployed" : false }];`

const parseData = JSON.parse(jsonNames);

// console.log(jsonNames); // this will print a string representation of an array!
console.log(parseDate); // it becomes a JS array!

const parseData = JSON.parse(jsonPerson); 
console.log(jsonPerson); // JS string!
console.log(parseData); // JS object

const parseData = JSON.parse(jsonPeople);
console.log(jsonPeople); // JS string! 
console.log(parseData); // Array of object!
```

```js
// now we'll fetch() the json files!
// fetch is a function, as an argument, we can pass an absolute or relative path or a url! (next topic!) 
fetch("person.json") // relative file (these files are right next to each other!) (fetch returns a promise! we'll follow this with .then() method!)
    .then(response => response.json()) // we'll be provided with a response object! we'll convert it to a json format using the .json() method and this response.json() will also return a promise!
    .then(value => console.log(value)) // do we need semi colon here??

// now we have successfully fetched a json file!
// now change the relative file path to other twos and observe the result!

// if we want to iterate through the array of objects, we can use the array's forEach() method!
fetch("people.json")
    .then(response => response.json())
    .then(values => values.forEach(value => console.log(value.name)))
    .catch(error => console.error(error));

// OUTPUT: Spongebob
// Patrick
// Squidward
// Sandy

```


## Fetch data from an API ↩️
- fetch = Function used for making HTTP requests to fetch resources.
- (JSON Style data, images, files)
- Simplifies asynchronous data fetching in JavaScript and used for inteeraacting with APIs t retrieve and send data asynchronously over the web.
- fetch(url, {options})

```js
fetch("https://pokeapi.co/api/v2/pokemon/pikachu")
    .then(response => console.log(response)) // prints huge response! (gaigantic object!!)
    .catch(error => console.error(error));
    // now our next step would be to convert it to a readable format! 
    // there's a few different metthds, there's array buffer, blob, text and Json (we are interested in JSON)
    // so our next step would be is to convert this response into json!

{
    fetch("https://pokeapi.co/api/v2/pokemon/pikachu")
    .then(response => response.json())
    .then(data => console.log(data)) // just to see what it is!
    .catch(error => console.error(error));

    // you can write data.name or data.weight in above console.log()
}

{
    // even if the pokimon doesn't exists! how promise won't get rejected! so in that case we'll throw a custome error!
        fetch("https://pokeapi.co/api/v2/pokemon/kishor")
            .then(response => {

                if(!response.ok){
                    throw new Error("Could not fetch resource"); // and now we'll catch it in the catch block!
                }
                return response.json();
            })
            .then(data => console.log(data.name)) // just to see what it is!
            .catch(error => console.error(error));
}

{
    // if you like to use async/await!
    
    fetchData();

    async function fetchData(){

        try{
            const response = await fetch("https://pokeapi.co/api/v2/pokemon/typhlosion");

            if(!response.ok){
                throw new Error("Could not fetch resources");
            }

            const data = await response.json();
            console.log(data;)
        }
        catch(error){
            console.error(error);
        }
    }
}
```

- Now, the actual sprites fetching api app!

```html
<input type="text" id="pokemonName" placeholder="Enter Pokemon name">
<button onClick = "fetchData()">Fetch Pokemon</button><br>

<img src="" alt = "Pokemon Sprites" id = "pokemonSprite" style = "display: none">
```

```js
    async function fetchData(){

        try{

            const pokemonName = document.getElementById("pokemonName").value.toLowerCase();

            const response = await fetch(`https://pokeapi.co/api/v2/pokemon/${pokemonName}$`);

            if(!response.ok){
                throw new Error("Could not fetch resources");
            }

            const data = await response.json();
            const pokemonSprite = data.sprites.front_default;
            const imgElement = document.getElementById("pokemonSprite");

            imgElement.src = pokemonSprite;
            imgElement.style.displayy = "block";
        }
        catch(error){
            console.error(error);
        }
    }
```
## Weather App project ☀️
- Find the Source code in the video!