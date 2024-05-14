# Learning-javascript
Taking notes from Jonas Schmedtmann's [Javascript course](https://www.udemy.com/course/the-complete-javascript-course/).
<hr>

# Value And Variable

**Value**: a piece of data <br>

*Example:* 
```javascript
console.log("Naz")
``` 

**Variable** : It's a box that we can store a value in.

We can store values into variables. So this way we can reuse them over and over again. <br>
```javascript
let firstName = "Naz"
```
"Naz" is a value and we assigned it to a variable. It's called *declaring a variable*.
<br>
<br>

* We can define two variables at the same time :

```javascript
let x, y;
// We declared two empty values
```

<hr>

# Data Types

every value is either:
1. Object : 
```javascript
let me  { 
        name: "Naz" 
}
```

2. Primitive : 
```javascript
let firstName = "Naz"
```

```javascript
let age = 30
```

A value is only primitive when it's not an object.

## Primitive Data Types :
1. number  
2. string
3. boolean
4. undefined
5. null
6. symbol
7. big int

**Number**: <br>
```javascript
let age = 30
```

**Strings**: <br>
```javascript
let firstName = "Naz"
```

**Boolean**: <br>
It's always either true or false. <br>
```javascript
let fullAge = true
```

**Undefined**:<br>
A value hasn't been defined for the variale (empty value) <br>
```javascript
let age;
```

**Null**: <br>
Empty value

**Symbol**: <br>
Value that is unique and can not be changed.

**Big int**: <br>
Larger integer than the number type can hold.
<br>
<br>

*Value has a type, NOT variable*. So variables simply store values that have a type.
<hr>

# "Type of" Operator 
We can use `type of` to show the type of a value.

*Example:* <br>
```javascript
constole.log(typeof 'Naz')
```

# Assigning a New Value

```javascript
let firstName = 'Naz'
firstName = 'Ash'
console.log(firstName)
```

# Let, conts, var

**1. Let** : <br>
We1. Let : <br>
We use the `let` keyword to declare variables that can change later. So basically during the execution. 

```javascript
let age = 30
age = 30
```

**2. const** : <br>
We use the `const` keyword to declare variables that are not supposed to change at any point in the future.

```javascript
let birthYear = 1995
```

 * We can not declare empty `const` variables.
`// const job; this is illegal`


**3. var**: <br>
`var` is the old way of defining variables and it shouldn't be used anymore.<br>
it's similiar to `let` on the surface but they're different.
<br>
<br>

## When to use `let` and `const`?

It's best practice to alsways use `const` by default and `let` only when you are really sure that the variables needs to change at some point in the future.<br>

*For example*: Birth year doesn't need to change so you should use `const`

<hr>

# Basic Operators

**Operator**: It allows us to transfer values or combine multiple values and do all kinds of work with values.<br>

### Mathematical/Arthimetic Operators :

# Basic Operators

**Operator**: It allows us to transfer values or combine multiple values and do all kinds of work with values.<br>

## Mathematical/Arthimetic Operators :

**1. addition operator** <br>
The addition operator (+) adds numbers

```javascript
const age = 25 + 5
```

**2. subtraction operator** <br>
The subtraction operator (-) subtracts numbers.

```javascript
const age = 25 + 5
```

**3. multiplication operator** <br>
The multiplication operator (*) multiplies numbers.

```javascript
const age = 25 * 5
```

**4. division operator**
The division operator (/) divides numbers.<br>
<br>

Read more [here](https://www.w3schools.com/js/js_arithmetic.asp).
<br>

### How to add space between variablea
```javascript
const firstName = 'Naz'
const lastName  = 'Ash'

console.log(firstName + lastName)

// Result = NazAsh


// How to fix it
const firstName = 'Naz'
const lastName  = 'Ash'

console.log(firstName + ' ' + lastName)

// Result = Naz Ash
```
<br>

## Assignment Operators

**The Simple Assignment Operator (=)**

*Example*:
```javascript
let x = 5 + 5 // 15

// We have two operators here : = and +
```

**The Addition Assignment Operator (+=)**

```javascript
let x = 10 + 5;
x += 5; // x = x + 5 or x = 15 + 5
```
```javascript
let fullName = 'Naz'
fullName += ' Ash' // 'Naz' + ' Ash'
console.log(fullName)
// Result : Naz Ash
```
**++ Operator**

```javascript
let x = 8
x++ // x = x + 1 = 9
console.log(x)
```

**-- Operator**

```javascript
let x = 8
x-- // x = x - 1 = 7
console.log(x)
```


Read about other assignments [here](https://www.w3schools.com/js/js_assignment.asp)
<br>
<br>

## Comparison Operators

We use comparison operators to produce `boolean` values.

```javascript
const ageMax = 25
const ageDavid = 29

console.log( ageDavid > ageMax) // true
```


Read more [here](https://www.w3schools.com/js/js_comparisons.asp)

<br>
<br>

## Operator precedence

Check [this](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Operator_precedence#table) table out for more info

<hr>

# Strings 

## Template Literals

A template literal can assemble multiple pieces into one final string.<br>

 
```javascript
const firstName = 'Naz'
const birthYear = 1993
const currentYear = 2077
const age = currentYear - birthYear

const bio = "I'm " + firstName + "." + "I'm " + age + " old"

console.log(bio) // I'm Naz.I'm 84 old
```
<br>

To write a temple literal we use "backticks" (```). <br>
The single or double quote won't work.

```javascript
const variable = ` ${variable} `
```

Let'd fix our code by using template literal :

```javascript
const firstName = 'Naz'
const birthYear = 1993
const currentYear = 2077
const age = currentYear - birthYear

const bio = `I'm ${firstName}. I'm ${age} years old.`

console.log(bio) // I'm Naz. I'm 84 years old.
```
<br>
**You can also write multiline string** :<br>
<br>

you could write multiple strings in the old javascript by using `\n\` which means a new line:

```javascript
console.log(`line one \n\
line two \n\
line three`)
```

But with modern javascript we can simplly hit `enter` and write a new line:

```javascript
console.log(`line one
line two
line three`)
```
<hr>

# If / Else Statement 

If the `if` statement is true, then first code block will be executed and if it's false, then the `else` block will be executed.

```javascript
const age = 17;

if (age >= 18) {
  console.log("Max is old enough to get a driver's license");
} else {
  const yearsLeft = 18 - age;
  console.log(`Max is too young. Wait ${yearsLeft} more year(s)`);
}

// Max is too young. Wait 1 more year(s)
```
<br>

* Any variable that we declare inside the block will not be accessible outside of the code block.

<hr>

# Type Conversion And Coercion

**Conversion**:<br>
When we manually convert from one type to another.<br>

**Coercion**: <br>
When javascript automatically converts types behind the scenes for us. <br>

## Type Conversion

* Javascript can only convert to three types :
1. To a number
2. To a string
3. To a boolean <br>

*Example*

```javascript
const year = "2024";
console.log(year + 5); // 20245
```

It doesn't automatically conver the string `("2024")` into number type.<br>
We can convert stirng to numbers by by using `Number()` function.<br>

```javascript
const year = "2024";
console.log(Number(year) + 5); // 2029
// Number(year) will return the string as number

```

## Type Coercion 
Type Coercion happens whenever an opartor is dealing with *two* values that have differetnt type. <br>


*Example*

```javascript
console.log("I'm " + 30 + " years old");
// I'm 30 years old
```
`30` is a number and javascript manually converts it to string.
<br>
<br>
* `+` converts numbers to strings.
* `-` converts strings to numbers.
* `*` converts strings to numbers.
* `/` converts strings to numbers.

*Example*:

```javascript
console.log("23" + "10"); // 2310
// Numbers are converted to strings

console.log("23" - "10"); // 13
// Strings are converted to numbers

console.log("23" * "2"); // 46
// Strings are converted to numbers

console.log("23" / "2"); // 11.5
// Strings are converted to numbers
```
<hr>

# Truthy and Falsy Values

## Falsy Values

Falsy values are values that are not exactly false but will become false when we try to convert them into a boolean. <br>

There are 5 falsy values: <br>
1. 0
2. ' '
3. undefined
4. null
5. NaN (Not a Number)

```javascript
console.log(Boolean(0)); // false
console.log(Boolean(undefined)); //false
console.log(Boolean("Naz")); // true
console.log(Boolean({})); // true
console.log(Boolean("")); // false
```
<hr>

# Equality Operators: (`==` vs `===`)


* Whenever our `if` block only has one line, we actually don't need two curly braces (`{}`)
<br><br>

*Example* 
```javascript
const age = 20;
if (age === 20) console.log("It is time to find a job!");
```

## Strict Equality Operator (`===`):
It's strcit because it doesn't perform type coercion. It only returns true when both values are exactly the same.<br>

*Example*:
```javascript
console.log(20 === "20"); // false
```

## Loose Equality Operator (`==`):
It does perfom type coercion.
<br>
*Example*:
```javascript
console.log(20 == "20"); // true
```
<br>

### `==` vs `===`

| `===`                          | `==` |
| -------------                  |:-------------:|
| equal value and equal type      | equal to    |

```javascript
console.log(20 == "20"); // true
console.log(20 == 20); // true

console.log(20 === "20"); // false
console.log(20 === 20); // true
```

* As a general rule for clean code, avoid using the loose equality operator (`==`) as much as you can. It will also create many bugs.<br>
* When using values, always use strict equality (`===`)
<br>



```javascript
const age = prompt("How old are you?");

console.log(typeof age); // string

if (age === "18") {
  console.log("You are old enough to drive");
} else {
  console.log("You are NOT old enough to drive");
}
// if you enter 18 = You are old enough to drive
```

```javascript
const age = prompt("How old are you?");

console.log(typeof age); // string

if (age === 18) {
  console.log("You are old enough to drive");
} else {
  console.log("You are NOT old enough to drive");
}
// if you enter 18 = You are NOT old enough to drive
```


*Example 2*:
```javascript
const faveNumber = Number(prompt("What is your favorite number?"));

console.log(faveNumber);
console.log(typeof faveNumber); 
// (prompt("What is your favorite number?") was originally a string.
// So we converted it to a number by Number() string.
// And now value and type are the same.

if (faveNumber === 20) {
  console.log("That is a cool number!");
} else if (faveNumber === 8) {
  console.log("Meeeh!!");
} else {
  console.log("Try again!");
}
```
<hr>

# Boolean Logic And Logical Operators
## The `and (&&)`, `or (||)` and `not (!)` operators

### `and (&&)`

<br>

| And       | True  | False |
| --------- |  -----|------- | 
| **True**  |True   | False  |
| **False** |False  |False  |

* The result will *only* be true *if* **ALL** conditions are true. <br>

```javascript
const isAnAdult = true;
const cantDrive = true;

console.log(isAnAdult && cantDrive); // true
```

```javascript
const isAnAdult = true;
const cantDrive = false;

console.log(isAnAdult && cantDrive); // false
```

### `or (||)`

<br>

| And       | True  | False |
| --------- |  -----|------- | 
| **True**  |True   | True  |
| **False** |True  |False  |

* The result will *only* be false *if* **ALL** conditions are false. 
* The result will be *true* only if **ONE** condistion is true <br>

```javascript
const isAnAdult = false;
const cantDrive = false;

console.log(isAnAdult || cantDrive); // false
```

```javascript
const isAnAdult = true;
const cantDrive = false;

console.log(isAnAdult || cantDrive); // true
```

### `not (!)`

```javascript
const isAnAdult = true;

console.log(!isAnAdult); // false
// this stated that the person is not and adult
// which is not true
// because the person is an adult
// therefore the result is false
```
............................................

*Example*

```javascript
const hasDriversLicense = true;
const hasGoodVision = false;

if (hasDriversLicense || hasGoodVision) {
  console.log("You can drive");
} else {
  console.log("let Max take the wheel");
} // You can drive
```

```javascript
const hasDriversLicense = true;
const hasGoodVision = false;

if (hasDriversLicense && hasGoodVision) {
  console.log("You can drive");
} else {
  console.log("let Max take the wheel");
} // let Max take the wheel
```

<hr>

# The switch Statement

It's an alternative way of writing a complicated if/else statement when all we want to do is to compare one value to multiple different options.<br>
It's for equality (day === 'monday'), not for comparing stuff.

```javascript
const day = "friday";

switch (day) {
  case "saturday": // day === 'monday'
    console.log("studying and coding");
    break;
  case "sunday":
    console.log("studying and playing cyberpunk");
    break;
  case "monday":
  case "tuesday":
    console.log("having a coffee chat");
    break;
  case "wednsday":
    console.log("working on a side project");
    break;
  case "thursday":
    console.log("touching grass");
    break;
  case "friday":
    console.log("taking the whole day off");
    break;
  default:
    console.log("Not a valid day!!!");
}
```

* What does `break` do?

```javascript
const day = "sunday";

switch (day) {
  case "saturday": // day === 'monday'
    console.log("studying and coding");
    break;
  case "sunday":
    console.log("studying and playing cyberpunk");
  // break;
  case "monday":
  case "tuesday":
    console.log("having a coffee chat");
    break;
  default:
    console.log("Not a valid day!!!");
}
// result : studying and playing cyberpunk
// AND having a coffee chat
```

So what happened?
Without the `break`, both sunday and monday will be executed untill it reaches to the next `break`.

<hr>

# Statements and Expressions

A decalration is like a complete sentence and expressions are like the words that make up the sentences.


## Expression 
It's a piece of code that produces a value.

*Example*:<br>
* `3 + 4`
* `1990`
* `true && false && !false`


## Statements

It's like a bigger piece of code that is executed and doens't produce a value on itself.

<hr>
  
# The Conditional (Ternary) Operator

 It allows us to write something similar to and if/else statement in one line.
 
 
 Syntax: <br>
 ```condition ? if part : else part```
 
 ```javascript
 const money = 200;

money >= 200
  ? console.log("You saved enough money!")
  : console.log("You are broke and need to start saving!");
  // console.log("You saved enough money!") is the if part
// console.log("You are broke and need to start saving!") is the else part
```

The consitional operator is in fact an operator just as the name says.<br>
And remember that an operator always produces a value.<br>
So in other words an operator is an expression.<br>
It means that if we have a value, we can then assign that value to a variable.<br>

As we just said, ternary operator is an expression, meaning it produce a value, So we can store it into a variable:

```javascript
const budget =
  money >= 200
    ? "You saved enough money"
    : "ou are broke and need to start saving!";

console.log(budget);
```
<hr>

# Activating Strict Mode

 It's a special mode that we can activate in javascript which makes it easier for us to write a secure javascriptt code.<br>
By secure codes we mean to avoid accidental  errors.<br>

 All we have to do is to writ `'use strict';` in our js file. <br>
 
 It has to be the first line of code in our js file.<br>
 
 Strict mode forbids us to do certain things and it will actually create visible errors for us.<br>

 <hr>
 
# Functions

It's a a piece of code that we can reuse over and over again <br>

Syntaxt:

```javascript
function name(parameters) {
  
}
```

1. `function` keyword: This tells JavaScript that you're defining a function.

2. Function name: Choose a descriptive name that reflects what the function does. It follows the same rules as naming variables in JavaScript (letters, numbers, underscores, and dollar signs).

3. Parentheses `()`: These enclose any parameters (inputs) the function might take. If the function doesn't take any inputs, you can leave the parentheses empty.

4. Function body: This is where you write the code that the function will execute. It's enclosed in curly braces `{}`.<br>

*Optional* `return` statement: This statement specifies the value the function will return after its execution. If no return statement is present, the function implicitly returns `undefined`.

*Example*:

```javascript
function firstName() {
  console.log("my name is Naz");
}

firstName();
```

```javascript
function bio(firstName, lastName, age) {
  const bio = `Hello, I'm ${firstName} ${lastName} and I'm ${age} years old`;
  return bio;
}

const person = bio("Naz", "Ashrafi", 30);
console.log(person);
```
<hr>

# Function Declarations vs. Expressions

## Function Declarations

```javascript
function calcAge1(birthYear) {
  return 2077 - birthYear;
}

const age1 = calcAge1(1990);
console.log(age1);
```

## Function Expressions

We write a `function` without a name, then we  define the parameter

```javascript
function (birthYear) {
  return 2077 - birthYear;
}
```
And then we store this into a variable and then that variable is gonna be a function.
```javascript
const calcAge2 = function (birthYear) {
  return 2077 - birthYear;
};
```

And this is an expression. <br>
And remember, an expression produces a value.<br>

```javascript
const calcAge2 = function (birthYear) {
  return 2077 - birthYear;
};

const age2 = calcAge2(1990);
console.log(age2);
```

### Differences Between Function Declarations And Expressions

We can actually call function declarations before they are defined in the code.

*Example*:
```javascript
const age1 = calcAge1(1990);
console.log(age1);

function calcAge1(birthYear) {
  return 2077 - birthYear;
}
```

<hr>

# Arrow Functions

It's a special form of function expression that is shorter and faster to write.<br>

Syntax:
```javascript
const functionName = (parameters) => { functionBody }
```

```javascript
const calcAge = (birthYear) => 2077 - birthYear;

const age = calcAge(1990);
console.log(age);
```

<hr>

# Calling Functions Inside Another Functions


```javascript
function calculateArea(width, heigh) {
  return heigh * width;
}

function calculateTheRoom(roomWidth, roomHeigh) {
  const room = calculateArea(roomHeigh, roomWidth);
  return room;
}

console.log(calculateTheRoom(22, 50));
```

<hr>

# Data Structure

# Arrays

Let's say I want to store my friends' names in variables so that I could use theme later in my program:

```javascript
const friend1 = "Max";
const friend2 = "Alex";
const friend3 = "Emma";
```

Now, this isn't exacly easy to do. Because imagine that you want to write more than 3 friends. Then we would have to create lots of variables.<br>

Array is like a big container into which we can throw variables and then reference them.<br>

So instead of doing that, we can use `arrays`. <br>

**Array Literal Syntax**
```javascript
const myArray = [element1, element2, ..., elementN];
```

```javascript
const friends = ["Max", "Alex", "Emma"];
console.log(friends);
```

**Array Constructor Syntax**

```javascript
new Array([element1, element2, ..., elementN]);
```

Example:
```javascript
const years = new Array(1788, 1833, 1990, 2020);
```


**How To Get an Array Out?**

Arrays are zero-based and start from zero

```javascript
const friend1 = "Max"; // [0]
const friend2 = "Alex"; // [1]
const friend3 = "Emma"; // [2]
```

And now if we were to get `Max` :

```javascript
console.log(friends[0]); // Max
```

```javascript
console.log(friends[1]); // Alex
console.log(friends[2]); // Emma
```

**How to get the number of the elements that are in the array? (How to get the length of an array?)**

```javascript
console.log(friends.length); // 3
```

**How to get the last element of an array?**

To get an element from the array we use `[]`
```javascript
console.log(friends[])
```

To get the index of the last element in the array
```javascript
console.log(friends[friends.length - 1]);
```

*Breakdown of what happened:*

`friends[friends.length - 1]`: This part tries to access an element from a list named friends.<br>

`friends.length`: This calculates the total number of elements (friends) in the list.<br>

`- 1`: This subtracts 1 because arrays start counting at 0. So, if there are 3 friends, the last one would be at index 2 (3 - 1).

*We can put any expression inside `[]`*<br>
*`friends.length - 1` is ans expression*

We can also chane it to add elements to the array:<br>

**Let's say we wanna replace the second array which is 'Alex':**

```javascript
friends[1] = " Toni";
console.log(friends); // ['Max', ' Toni', 'Emma']
```



We said variables with `const` can not be changed. But in this example we were able to change our element in the array. So how did that heppen?<br>
**A:** Only primitive values are immutable, meaning you can not change it.<br>

If we check the type of `friends` we'll see it's an object and not a primitive value:

```javascript
console.log(typeof friends); //object
```

So basically, we can still modify the content of that object or array but we can not replace the entire array.<br>

We can not do something like : 
```javascript
friends = ["Toni", "Ted"];
```

**An array can actually hold values with different types**
