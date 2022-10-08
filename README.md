# Javascript Notes Part 1

## Hello World!

Command + Option + J - Opens the console in Chrome.
Typing - alert(“Hello World”) in the console creates a popup alert box.

Expanding on the above ^

```
let js = “Amazing”
If (js === “Amazing”) alert(“JavaScript is amazing”)
```

The code above explained: We created a variable called js that is assigned (=) the text Amazing.
Then we are saying if js is equal (===) to or the same as Amazing then alert the user, JavaScript is amazing. If js was equal to something else other than Amazing, the alert wouldn’t be displayed.

Variables are ways of storing pieces of information. 

## What Is JavaScript?

JavaScript is a:

High-Level - We dont have to worry about complex stuff like memory management.
Object Oriented - Based on real-life objects for storing data.
Multi-Paradigm - We can use different programming styles.
Programming Language - We can give the computer a set of insturctions to do things.

## Linking A JavaScript File

To write JavaScript directly into a HTML page we use the <script> tag. This is placed within the <head> tag. When we write JavaScript this way, it’s called inline script.

The only advantage of an inline script is that we don't have to load another file. But on the other hand it's pretty bad for separating the website content from the JavaScript logic. And so usually we use external JavaScript files.

## Assigning A Variable

In JavaScript, we use the equals sign (=) to assign a variable to a value.
For example: ```let firstName = “Michael”;```

When we create varibles, it actually creates a variable in your computer’s memory. I honestly didn't realise it wyorked like this!

# Understanding Variables

I like to imagine a variable, like being a box. So in the real world, a box can hold some object for example, a book, and we can then write a label on the box to describe what's in it. And then we can find the object later when we need it by using that label. So giving your variables meaningful names is important for you and for other developers who might be reading your code.

A value can either be an OBJECT or PRIMITIVE.

Object example:

```
let me = {
     name: “Michael”
};
```

Primitive example:

```
let firstName = “Michael”;
```

## Data Types

### 7 Primitive Data Types

**Number:** Floating point numbers. Used for decimals and integers.
**String:** Sequence of characters. Used for text.
**Boolean:** Logical type that can only be true or false. Used for making decisions.
**Undefined:** Value taken by a variable that is not yet defined (‘empty value’). A variable thats not yet defined is simply just a variable that we declared but without assigning a value. For example: let firstName;
**Null:** Also means empty value.
**Symbol:** Value that is unique and cant be changed.
**BigInt (ES2020):** This is used for larger intergers than the Number type can hold.

It’s the value that holds the data type and not the name of the variable.

To find out what data type a value is we can use typeof. 
For example: 
```console.log(typeof “Hello”)``` prints out ```string``` to the console.
```console.log(typeof 24)``` prints out ```number``` to the console.
```console.log(typeof true)``` prints out ```boolean``` to the console.

# Dynamic Typing

Dynamic Typing simply means that we can easily change the type of a value that is held by a variable.

When reasigning a variable we don’t include let. 
So for example:

```
let codingIsFun = true; // prints out boolean 
codingIsFun = 24; // value is changed and prints out number
```

# LET, CONST And VAR

Var is the old way of declaring variables.
We use the let keyword to declare variables that can change later so basically during the execution.

```
let myNumber = 234;
console.log(myNumber);
myNumber = 456;
console.log(myNumber);
```

We use the **const** keyword to declare variables that are not supposed to change at any point in the future.

```
const ireland = "Europe";
console.log(ireland);
ireland = "Africa";
console.log(ireland); // creates a variable that we cannot reassign or in technical terms, an immutable variable.So, a variable that cannot be mutated.
```
By default, always just use const and let, when you're sure that the value of the variable needs to change at some point in your code. It's a good practice to have as little variable mutations or variable changes as possible because changing variables introduces a potential to create bugs.

# Operators

```
const ageTrisha = 2022 - 2005;
const ageRich = 2022 - 1984;

console.log(ageRich, ageTrisha); // 38 17
```
Although there’s nothing actually wrong with the above, it’ll still work but we have repeating values, which is not good in both ```ageTrisha``` and ```ageRich```. So if the year now changes then we would have to change it in these both places. And we don't like that.

So what we do is this:
```
const year = 2022;
const ageTrisha = year - 2005;
const ageRichie = year - 1984;

console.log(ageTrisha, ageRichie); // 17 38
```
# Concatenation
```
const firstName = "Michael";
const lastName = "McCann";
// "" adds a space between the two words
console.log(firstName + " " + lastName);
```
# Reassignment
```
let x = 5 + 10; // x is 15 because 5 + 10 = 15
x += 10; // reasignment. += means x = x + 10 = 25. So 15 + 10
x += 5; // reasignment. now we just added 5 on to the 25. value is 30
x *= 4; // reasignment. 30 * 4 = 120
x++; // increases the value by 1 = 121
x--; // decreases the value by 1 = 120
```
# Comparison Operators
```
console.log(ageRichie > ageTrisha); // 38 > 17 = true
console.log(ageTrisha >= 18); // is 17 greater than or equal to 18? false
console.log(ageRichie >= 18); // is 38 greater than or equal to 18? true
```
# Operator Precedence

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Operator_Precedence

Maths operators are executed before comparison operators.
```
const averageAge = ageJonas + ageSarah / 2;
console.log(ageJonas, ageSarah); // 46, 19
console.log(averageAge) // 55.5
```
Division has a higher precedence than addition so that's executed first. So it goes like ```19 / 2 + 46 = 55.5.``` That's not how we find the average. We want to add ```ageJonas(46)``` and ```ageSarah(19)``` first before division. In order to get the correct sum we use brackets.
```
const averageAgeSum = (ageJonas + ageSarah) / 2; // Whatever is in brackets gets executed first
console.log(ageJonas, ageSarah); // 46, 19
console.log(averageAgeSum) // 32.5
```

# Coding Challenge No. 1

Mark and John are trying to compare their BMI (Body Mass Index), which is calculated using the formula:

BMI = mass / height ** 2 or we can do it like this - mass / (height * height) (mass in kg and height in meter).

Your tasks:

Store Mark's and John's mass and height in variables
Calculate both their BMIs using the formula (you can even implement both versions)
Create a Boolean variable 'markHigherBMI' containing information about whether Mark has a higher BMI than John.

Test data:
Data 1: Marks weights 78 kg and is 1.69 m tall. John weights 92 kg and is 1.95 m tall.
Data 2: Marks weights 95 kg and is 1.88 m tall. John weights 85 kg and is 1.76 m tall.

## Solution

I used LET instead of CONST so I could reasign the variables to produce both test datas.

```
// Mark's information

let massMark = 78;
massMark = 95;
let heightMark = 1.69;
heightMark = 1.88;

// John's information

let massJohn = 92;
massJohn = 85;
let heightJohn = 1.95;
heightJohn = 1.76;

// BMI calculation
let BMIMark = massMark / heightMark ** 2;
let BMIJohn = massJohn / heightJohn ** 2;

// Compared both BMIs
let markHigherBMI = BMIMark > BMIJohn;

console.log("BMI Mark: ", BMIMark);
console.log("BMI John: ", BMIJohn);
console.log("BMI Mark greater than BMI John: ", markHigherBMI);
```

# Strings and Template Literals
```
const firstName = 'Michael';
const profession = 'Web Developer';
const birthYear = 1980;
let currentYear = 2022;
const age = currentYear - birthYear;

// Concatenation without template literals
console.log("I'm " + firstName + ". My job is a " + profession + " and I am " + age + " years-old!");

// Concatenation with template literals
console.log(`I'm ${firstName}. My job is a ${profession} and I am ${age} years-old!`);
```

Using template literals is a much easier and cleaner way to concatenate variables in our strings, as we don’t have to worry about where to put the space. It’s also easier to read.

# If Else Statements

IF ELSE Statements helps us to make decisions.
A condition is a piece of code that returns a true or false value.
If the condition is true, the if block runs.
If the condition is false, JavaScript skips the if block and runs the else block.
Else block is optional.

Any variable created inside a code block won’t be accessible outside.
```
if () {
    // This is a code block
} else {
    // This is a code block
}
```
```
const birthYear = 1988;

if (birthYear <= 2000) {
    let centuary = 20; // 20th centuary
} else {
    let centuary = 21; // 21st centuary
}

console.log(centuary);
```
Because I created ```let centuary``` inside the ```if else```, it won’t be accessible outside of the code block.

```
// Check to see if a person is old enough to drive
const ageDrivingLicense = 17;
const ageMartin = 14;

// If Martin's age is greater than or equal to 17 then the if statement is executed
if (this is a condition >> ageMartin >= ageDrivingLicense) {
    console.log("You are old enough to apply for a driving license 🚙.")
} else {
    // If Martin's age IS NOT greater than or equal to 17, the else statement is executed
    const yearsLeft = ageDrivingLicense - ageMartin;
    console.log(`Sorry, you have to wait ${yearsLeft} year/s before you can apply 😢.`)
}
```

# Type Conversion and Coercion

Type Conversion is when we manually convert from one type to another.
Type Coercion is when JavaScript automatically converts types behind the scenes for us.

When a user inputs a number on an input form on a website it's usually returned as a string.
As developers we have to find a way to convert strings to numbers because if we try to do calculations it won't work.

## Type Conversion
```
const inputYear = '1991';
console.log(Number(inputYear), inputYear); // Number converts a String to a Number
console.log(inputYear + 18); // Outputs 199118 becausee of concatenation
console.log(Number(inputYear) + 18); // Now that 1991 has been converted to a number we can now perform the calculation correctly. Outputs 2009 rather than 199118.
// What happens if we try to convert a string to a Number?
console.log(Number('JavaScript')); // JavaScript trys to convert the operation. Returns NaN when an operation fails to produce a new number - Not a Number. Means an invalid number.
console.log(String(34), 34); // Converts a number to a string
```

## Type Coercion

Type coercion happens whenever an operator is dealing with two values that have different types.
JavaScript will behind the scenes convert one of the values to match the other value.
```
console.log('I am ' + 23 + ' years old.') // String. Number. String. + operator triggers type coercion.
// Not all operators do type coercion
console.log('23' - '10' - 3); // 10. - operator triggers opposite conversion. In this case strings are converted to numbers.
console.log('23' + '10' + 3); // 23103. Strings concatenated.
console.log('23' * '2'); // 46.
console.log('23' / '2'); // 11.5.

let n = '1' + 1;
n = n - 1;

console.log(n); // 10

console.log(2 + 3 + 4 + '5'); // 95.
console.log('7' - '2' - '2' + 3); // 6.
console.log('9' - '5'); // 4
console.log('19' - '13' + '17') // 617
console.log('19' - '13' + 17) // 23
console.log('123' < 57); // false
console.log('abcde' > 'abc'); // true
console.log(5 + 6 + '4' + 9 - 4 - 2); // 1143
```
Type coercion can introduce many unexpected bugs but knowing it well alows us to write less code and more readable code.

# Truthy and Falsy Values

Falsy values are values that are not exactly false, but will become false when we try to convert them into a boolean.

Five Falsy values:
0
“ ” // empty string
Undefined // variable without a value e.g. let name;
null
NaN

All of these five values will be converted to false when we attempt to convert them to a boolean.
They're not exactly false initially, but they will become when converted to a boolean.
```
console.log(Boolean(0)); // false
console.log(Boolean(undefined)); // false
console.log(Boolean('Michael')); // true. Any string that's not an empty string is truthy
console.log(Boolean('')); // false
console.log(Boolean({})); // empty object
```

Example 1:

```
const money = 0;

if (money) {
    console.log(`Your account is €${money}. Careful not to spend all your money!`);
} else {
    console.log(`Your account is €${money}. Time to get yourself a job!`);
}
```
else statement is executed here because 0 evaluates to being falsy. If we change the variable to any other number e.g 700, then the if statement runs.

Example 2:
```
let height;

if (height) {
    console.log('Height is defined.');
} else {
    console.log('Height is undefined.');
}

console.log(typeof(height)); // undefined
```
else block runs because let height is undefined, we haven't assigned it a value. Assigning height to any number then the if block runs.

# Equality Operators: == Vs ===

=== checks if age is exactly 18
=== returns a true or false value - Boolean value
=== also called strict equality operator. Strict because it DOES NOT perform Type Coercion 
== loose equality. DOES perform Type Coercion.
true will only be the result of this operator in case that both sides are exactly the same.

Example 1:
```
const age = 18;
if (age === 18) console.log('Strict. You are an adult.');
if (age == 18) console.log('Loose. You are an adult.’);
```
Both if statements are ran

Example 2:
```
const age = ’18’;
if (age === 18) console.log('Strict. You are an adult.');
if (age == 18) console.log('Loose. You are an adult.’);
```
Only the second if statement runs


# Loose (==) and Strict (===) Comparisons

```'18' === 18```
**false** - one's a string the other is a number. Even though both are 18, they are not exactly the same.

```18 === 18```
**true** - both values are numbers and both are the same number. They are exactly the same.

```18 == 18```
**true** - both values are the same number

```'18' == 18```
**true** - even though one's a string and the other is a number, the string is coverted to a number and it's true because both have the same number.

As a general rule for clean code, avoid the loose equality operator (==) as much as you can, as it can introduce bugs. Keep it strict (===)!

Example 3:
```
const favNumber = prompt(‘What is your favourite number?’);

if (favNumber == 23) {
    console.log(`That's a great choice, 23 is an excellent number!`);
} else {

}
```
In example 3 we make use of the ‘loose’ equality operator, which we should avoid. So in order to use the (===) strict equality operator we must convert the prompt function to a number. 
```
const favNumber = Number(prompt(`What's your favourite number?`));
console.log(favNumber);
console.log(typeof(favNumber)); // String

if (favNumber === 23) {
    console.log(`That's a great choice, 23 is an excellent number!`);
} else if (favNumber === 7) {
    console.log(`7 is also a pretty cool choice!`)
} else if (favNumber === 9) {
    console.log(`9 is also a pretty cool choice!`)
} else {
    console.log(`You didn't pick a cool number, which 23, 9 or 7!`)
}

if (favNumber !== 23) console.log(`You didn't pick 23.`);
```
# Different operator:

Strict - !==
Loose -!=

**Always use Strict**

# Boolean Logic
```
const hasDrivingLicense = true;
const hasGoodVision = false;
const isTired = true;

console.log(hasDrivingLicense && hasGoodVision);
console.log(hasDrivingLicense || hasGoodVision);
console.log(!hasDrivingLicense);

// Reads as: If Sarah has a driving license and has good vision and is not tired.
if (hasDrivingLicense && hasGoodVision && !isTired) {
    console.log('Sarah is able to drive.');
} else {
    console.log('Somerone else should drive.');
}
```
**! means NOT**
The ! operator inverts one of the values.

**&& means AND**
If both values are true. The output is true. true + true = true
If one value is true AND the other is false. The output is false. true + false = false.
It's enough for one variable to be false for the result of the operation to be false.

**|| means OR**
If one value is true OR the other is false. The output is true.
It's enough for one of the variables to be true for the whole operation to become true.

# Challenge

Object is to create a scoring system whereby the team with the highest average score wins. Include a requirement for a minimum score of 100. With this rule, a team only wins if it has a higher score than the other team, and the same time a score of at least 100 points. Minimum score also applies to a draw! So a draw only happens when both teams have the same score and both have a score greater or equal 100 points. Otherwise, no team wins the trophy. 
```
const averageScoreDolphin = (97 + 112 + 101) / 3;
const averageScoreKoalas = (109 + 95 + 106) / 3;

if (averageScoreDolphin > averageScoreKoalas && averageScoreDolphin >= 100) {
    console.log(`Dolphin's win with an average score of: ${averageScoreDolphin}.`);
} else if (averageScoreDolphin < averageScoreKoalas && averageScoreDolphin <= 100) {
    console.log(`Koalas's win with an average score of: ${averageScoreKoalas}.`);
} else if (averageScoreDolphin === averageScoreKoalas && averageScoreDolphin >= 100 && averageScoreKoalas >= 100) {
    console.log(`Dolphin's average score is: ${averageScoreDolphin}. 
Koala's average score is: ${averageScoreKoalas}. Both teams win!`);
} else {
    console.log('No one wins the trophy 😢.')
}

console.log(averageScoreDolphin, averageScoreKoalas);

Same code as above, but this snippet enables the user to input their own scores.

// Dolphin's scores
const scoreDolphin1 = Number(prompt("Dolphin's, please input your first score."));
const scoreDolphin2 = Number(prompt("Dolphin's, please input your second score."));
const scoreDolphin3 = Number(prompt("Dolphin's, please input your third score."));
const averageScoreDolphin = (scoreDolphin1 + scoreDolphin2 + scoreDolphin3) / 3;

// Koala's scores
const scoreKoala1 = Number(prompt("Koala's, please input your first score."));
const scoreKoala2 = Number(prompt("Koala's, please input your second score."));
const scoreKoala3 = Number(prompt("Koala's, please input your third score."));
const averageScoreKoalas = (scoreKoala1 + scoreKoala2 + scoreKoala3) / 3;

if (averageScoreDolphin > averageScoreKoalas && averageScoreDolphin >= 100) {
    alert(`Dolphin's win with an average score of: ${averageScoreDolphin}.`);
} else if (averageScoreDolphin < averageScoreKoalas && averageScoreDolphin <= 100) {
    alert(`Koalas's win with an average score of: ${averageScoreKoalas}.`);
} else if (averageScoreDolphin === averageScoreKoalas && averageScoreDolphin >= 100 && averageScoreKoalas >= 100) {
    alert(`Dolphin's average score is: ${averageScoreDolphin}. 
Koala's average score is: ${averageScoreKoalas}. Both teams win!`);
} else {
    alert('No one wins the trophy 😢.')
}

console.log(averageScoreDolphin, averageScoreKoalas);
```
# Switch Statement

A Switch statement is an alternative way of writing a complicated if else statement
```
const day = 'Monday';

switch (day) {
    case 'Monday': // <-- The same as day === 'Monday'
        console.log('Plan course structure.');
        console.log('Go attend a coding meetup.');
        break; // Without a BREAK the code will continue excuting.
    case 'Tuesday':
        console.log('Prepare therory videos.');
        break;
    case 'Wednesday':
    case 'Thursday':
        console.log('Write code examples.');
        break;
    case 'Friday':
        console.log('Record videos.');
        break;
    case 'Saturday':
    case 'Sunday':
        console.log('Enjoy the weekend.');
        break;
    default:
        console.log('Not a valid day.');
}
```
Above code written in an if else statement.
```
if (day === 'Monday') {
    console.log('Plan course structure.');
    console.log('Go attend a coding meetup.');
} else if (day === 'Tuesday') {
    console.log('Prepare therory videos.');
} else if (day === 'Wednesday' || day === 'Thursday') {
    console.log('Write code examples.');
} else if (day === 'Friday') {
    console.log('Record videos.');
} else if (day === 'Saturday' || day === 'Sunday') {
    console.log('Enjoy the weekend.');
} else {
    console.log('Not a valid day.');
}
```
# Statement and Expressions

An expression is a piece of code that produces a value.
For example 3 + 4 is an expression because it’s going to produce a value.
2005, this is also an expression because it will produce a value in javascript.
```true && false && !true``` this is also an expression because it’ll retrurn a Boolean value.

A statement is like a bigger piece of code that is executed and which does not produce a value on itself.

# Conditional Operator

Allows us to write something similar to an if-else but all on one line.
ALso called a ***Ternary Operator***.
```
const age = 18;

age >= 18 ? console.log('Old enough to drink beer 🍺') : console.log('Get some water instead!');
```
Because a Ternary operator produces a value we can actually store it in a variable.
```
const drink = age >= 18 ? 'drink beer 🍺' : 'drink water 🚰'; 
// This whole operator is an expression
console.log(drink);
```
The above code written in an if-else block for comparison.
```
let drink2;
if (age >= 18) {
    drink2 = 'drink beer 🍺';
} else {
    drink2 = 'drink water';
}

console.log(drink2);
```
We can include ternary operator in a template literate.
```console.log(`I like to ${18 ? 'drink beer 🍺' : 'drink water 🚰’}`);```

A simple tip calculator to determine if the bill value is between 50 and 300. Regular tipping cost is 15%. If the value is different, the tip is 20%. 
```
const bill = Number(prompt('Please input your bill.'));
const tip = bill >= 50 && bill >= 300 ? bill * 0.2 : bill * 0.15;

alert(`The bill was €${bill}, the tip was €${tip}, and the total value is €${bill+tip}.`);
```