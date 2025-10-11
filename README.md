# JavaScript 101;

> console.log("Let's Begin!");
BY BroCode [watch](https://www.youtube.com/watch?v=lfmg-EJ8gm4&t=4618s)

***Watch the above video and follow through these notes for better understanding😎🚀🔥***

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
## Nested objects 📫
## Arrays of objects 🍎
## Sorting 🗃
## Shuffle an array 🔀
## Dates 📅
## Closures 🔒
## setTimeout() ⏰
## Digital Clock program 🕐
## Stopwatch program ⏱
## ES6 Modules 🚢
## Asynchronous code 💤
## Error handling ⚠
## Calculator program 🖩
## What is the DOM? 🌳
## Element selectors 📑
## DOM navigation 🧭
## Add & change HTML 🛠️
## Mouse events 🖱
## Key events ⌨
## Hide/show HTML 🖼
## NodeLists 📃
## classList 🧾
## Rock Paper Scissors 👊
## Image Slider 🖼️
## Callback Hell? 🔥
## Promises 🤞
## Async/Await ⏳
## JSON files 📄
## Fetch data from an API ↩️
## Weather App project ☀️