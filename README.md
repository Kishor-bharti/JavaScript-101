# JavaScript 101;

> console.log("Let's Begin!");
BY BroCode [watch](https://www.youtube.com/watch?v=lfmg-EJ8gm4&t=4618s)

## Starting...
* JavaScript is a programming lang used to create Dynamic and Interactive web pages!
* Js runs on web browsers
* By using JS, we use respond to user actions and transform user input whenever somebody interacts with our site (eg. Calculator app!)

`creates a folder named website and html, css and js files for structure , styles and actions!`

```html
<link rel="stylesheet" href="style.css">
<script src="index.js"></script>
<p>Don't forget these two tags!</p>
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
## Arrow functions 🎯
## JavaScript Objects 🧍
## What is THIS 👈
## Constructors 🛠
## Classes 🏭
## STATIC keyword ⚡
## Inheritance 🐇
## SUPER keyword 🦸‍♂️
## Getters & Setters 📐
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