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


**An array can actually hold values with different types :**

```javascript
const bio = ["Naz", "Ashrafi", 2024 - 1993];
```

We can use variables inside an array :
```javascriptconst firstName = "Naz";
const bio = [firstName, "Ashrafi", 30];
```

We can also use an array inside the array :
```javascript
const friends = ["Max", "Alex", "Emma"];
const bio = ['Naz', "Ashrafi", 30, friends];
```
<br>

*Example :*
```javascript
const calcAge = (birthYear) => 2024 - birthYear;

const years = [1763, 1891, 1990, 2007];

console.log(calcAge(years[0])); // 2024 - 1763 = 261

console.log(calcAge(years[years.length - 1])); // 17 
//Calcualte the last array
```

Instead of doing this :
```javascript
console.log(calcAge(years[0])); // 261
console.log(calcAge(years[1])); // 133
console.log(calcAge(years[2])); // 34
console.log(calcAge(years[3])); // 17
```

We can do this:
```javascript
const ages = [
  calcAge(years[0]),
  calcAge(years[1]),
  calcAge(years[2]),
  calcAge(years[3])
];

console.log(ages);
```

<hr>

# Array Methods

![image](https://github.com/NazaNEYn/Learning-javascript/assets/68081983/f2a7de26-7f11-4020-ba40-ff4aafa646a2)


## push()
Push medthod adds elelemnts to the end of the array.

*Example*:
```javascript
const friends = ["Max", "Alex", "Mary", "John"];

friends.push("Bob");

console.log(friends);
// adds 'Bob' to the end of the array
// ['Max', 'Alex', 'Mary', 'John', 'Bob']
```

Since `push()` is a function, it can also return something.<br>
So we can pass arguments into function.<br>
`push()` function return a value and the value that it returns is the length of the new array.<br>
So if we want to capture the data or the value, we can create a new variable for that.

```javascript
const friends = ["Max", "Alex", "Mary", "John"];

const newLength = friends.push("Bob");

console.log(newLength); // 5
```
**Q:**
why does `const newLength = friends.push("Bob");`` only print out the length?<br>

**A:**
The line `const newLength = friends.push("Bob");`` only prints the length (5) because of two key things:<br>

1. What `push` Returns:
* The `push` method in JavaScript doesn't directly print anything.

* Its job is to modify the original array (`friends` in this case) by adding a new element ("Bob") to the end.

* Importantly, it returns the new length of the modified array. This new length (5 in this case) is what gets assigned to the `newLength` variable.

2. What `console.log` Shows:
* The `console.log` function simply displays what you tell it to.

* In this line, you're telling it to display the value of the `newLength` variable, which is just the number 5 (the new length).

* It doesn't automatically show the contents of the array (`friends`).
  <br>

## unshift()
It add elements to the beginning of the Array.<br>

```javascript
const friends = ["Max", "Alex", "Mary", "John"];

friends.unshift("Bob");

console.log(friends);
// (5) ['Bob', 'Max', 'Alex', 'Mary', 'John']
```
 
 ## pop()
 It removes the last element of the array.<br>
 *We don't need to pass any arguments*
 
 ```javascript
 const friends = ["Max", "Alex", "Mary", "John"];
 
 friends.pop();

console.log(friends);
// (3) ['Max', 'Alex', 'Mary']
// John is gone
```

*If we write `friends.pop();` twice, it'll remove two elements from the end of the array.*

 ```javascript
 const friends = ["Max", "Alex", "Mary", "John"];
 
 friends.pop();
 friends.pop();

console.log(friends);
// (3) ['Max', 'Alex']
// John and Mary are gone
```

*`pop()` doens't return length of the array. It returns the removed element*

```javascript
const friends = ["Max", "Alex", "Mary", "John"];

// what pop returns :
// it doesn't return the length.
// it returns the last element that was removed
const pop = friends.pop();

console.log(pop); // John
```

 ## shift()
 It removes the first element of the array.<br>
 
 ```javascript
 const friends = ["Max", "Alex", "Mary", "John"];
 
 friends.shift();

console.log(friends);
// (4) ['Alex', 'Mary', 'John']
```

# indexOf()
It tells us in which position a certain element is in the Array and then we pass the element that we want to reference.

```javascript
const friends = ["Max", "Alex", "Mary", "John"];

console.log(friends.indexOf("Alex")); // 1

console.log(friends.indexOf("John")); // 3
```

If we try the same thing for an element that that is not there, we'll get `-1`

```javascript
const friends = ["Max", "Alex", "Mary", "John"];

console.log(friends.indexOf("Toni")); // -1
```

## includes()

So instead of returning the index of the element, it will return true if the element is in the array and false if it's not. 

```javascript
const friends = ["Max", "Alex", "Mary", "John"];

console.log(friends.includes("Max")); // true

console.log(friends.includes("Toni"));
// the output is false because Toni isn't in the array
```

*This method uses strict equality for the check*<br>
If we add `23` to the array and check for the `'23'`, the result would be false.

```
friends.push(23);
console.log(friends.includes("23"));
```


*We can use `includes()` to write conditionals.*
```javascript
const friends = ["Max", "Alex", "Mary", "John"];

if (friends.includes("Max")) {
  console.log("Hello Max");
} else {
  console.log("You are not Max");
}
// Hello Max
```

<hr>

# Objects


In objects we define key value pairs. Then we can give each of these values, a name.<br>
The key is the variable name.<br>
We use curly braces `{}` for the objects.

### Object Literal

*Syntax*
```javascript
const variableName = {
    key: value,
    key: value,
    key: value
}
```
* *Keys are also called properties*

*Example*:
```javascript
const bio = {
  firstName: "Naz",
  lastName: "Ashrafi",
  Age: 2024 - 1993,
  friends: ["Ted", "John", "Max"]
};
```

**Difference Between Arrays And Objects :**<br>
In objects, the order of the values does not matter at all when we want to retrieve them.<br>
In Array, the order in which we specify the elements matters a lot because that's how we access the elements.<br>
This means we should use arrays for more order data and objects for more unstructured data.


### Getting a property/key from an object :

* Dot Notation `(object.property)`

```javascript
const bio = {
  firstName: "Naz",
  lastName: "Ashrafi",
  Age: 2024 - 1993,
  friends: ["Ted", "John", "Max"]
};

console.log(bio.lastName); //Ashrafi
console.log(bio.friends); // ['Ted', 'John', 'Max']
```

* Bracket Notation `(object["property"])`

We need to specify a string with the property name.

```javascript
const bio = {
  firstName: "Naz",
  lastName: "Ashrafi",
  Age: 2024 - 1993,
  friends: ["Ted", "John", "Max"]
};

console.log(bio["lastName"]);
```

**Differences between dot notation and bracket notation:**

In the bracket notation, we can actually put any expression that we like. We don't have to explicitly write the string here.

```javascript
const bio = {
  firstName: "Naz",
  lastName: "Ashrafi",
  Age: 2024 - 1993,
  friends: ["Ted", "John", "Max"]
};

const nameKey = "Name";
console.log(bio["first" + nameKey]); // Naz
// first + Name = firstName = Naz
console.log(bio["last" + nameKey]); // Ashrafi
// last + Name = latsName = Ashrafi
```

*So what happend here?*
The output would be first the string + nemeKey variable (`first + Name`).<br>
So basically the output will be `firstName`. <br>
And since we alredy have a property named `firstName`, javascript will output the `firstName` property, which is `Naz`.<br>
And the same thing with the second output happend:<br>
`last + Name = latsName = Ashrafi`

This is *not* gonna work with the dot notation.<br>

**Recap :** <br>
* **Dot Notation** `(object.property)` : <br>
  *Simpler and easier to read:* <br>
  When the property name is a valid JavaScript identifier (letters, numbers, underscores, and a dollar sign at the beginning), 
  and it doesn't contain spaces or special characters, dot notation is preferred for readability.<br>

* **Bracket Notation** `(object["property"])`<br>
    *Dynamic property names:* <br> Use bracket notation when the property name is stored in a variable, comes from user input, or 
    contains special characters or spaces.<br>
*Method calls can also use dot notation:* <br>
Because methods are just functions attached to objects, you can call them using dot notation.<br>


**Key points to remember:**

* Dot notation is generally faster than bracket notation because it doesn't require extra string conversion.<br>
* Bracket notation is more flexible but can be less readable.<br>
* Choose the notation that best suits the situation and readability of your code.
<br>

Let's say we wanna let the user pick something and we don't what propertie they are going to choose.<br>


*Example :* <br>

We wanna let the user choose pick a number between 1-5 and get a random fruit name :

**1. Object Creation:**<br>
First we create an object named `fruits`
```javascript
const fruits = {
  1: "Apple",
  2: "Orange",
  3: "Watermelon",
  4: "Banana",
  5: "Strawberry"
};
```


**2. User Input:**<br>
To get a popup question, we use `propmt()` and will store it in a variable named `randomFruit`.<br>
```javascript
const randomFruit = prompt(
  "Pick a number between 1-5 to get a random fruit name"
);
```

**3. Accessing Fruit Name:**
```javascript
console.log(fruits[randomFruit]);
```
*We're trying to access a property within an object using the object's key.*<br>

* This line tries to access a property in the `fruits` object using the value stored in `randomFruit`.
* `fruits` is the object you defined earlier, containing fruit names with numbers (1-5) as keys.
* `randomFruit` is a variable that stores the user's input number (between 1 and 5).
* JavaScript uses square brackets `[]` to access object properties when the property name might not be a valid variable name (like numbers in this case) or when it's dynamically generated (comes from user input).<br>
<br>
So to put it simply, Javascript will replace `randomFruit` with the actual value of the variable and that's the one that will be looked on on the `fruits` object

**Full code snippet:**
```javascript
const fruits = {
  1: "Apple",
  2: "Orange",
  3: "Watermelon",
  4: "Banana",
  5: "Strawberry"
};

const randomFruit = prompt(
  "Pick a number between 1-5 to get a random fruit name"
);

console.log(fruits[randomFruit]);
```

### Adding New Properties To The Objcet

```javascript
const bio = {
  firstName: "Naz",
  lastName: "Ashrafi",
  Age: 2024 - 1993,
  friends: ["Ted", "John", "Max"]
};

// dot notation
bio.job = "Got some boring office job";

// bracket notation
bio["hobby"] = "Playing video games";
```
<hr>

# Object Methods

Any function that is attached to an object is called a method.


```javascript
const bio = {
  firstName: "Naz",
  lastName: "Ashrafi",

  // this is a function value
  calcAge: function (birthYear) {
    return 2024 - birthYear;
  }
};
```

We can **not** do something like this:
```javascript
const bio = {

  function calcAge(birthYear) {
    return 2024 - birthYear;
  }
}
```
Because this a decalartion and we can only write experession in the object.<br>

How to access the `calcAge` propert?
```javascript
const bio = {
  firstName: "Naz",
  lastName: "Ashrafi",

  calcAge: function (birthYear) {
    return 2024 - birthYear;
  }
};

// dot notation
console.log(bio.calcAge(1993));

// bracket notation
console.log(bio["calcAge"](1993));
```

`calcAge` is the function value. In order to call this function we use `()` and the we pass the year to the function.<br>
<br>

In this code snippet
```javascript
const bio = {
  firstName: "Naz",
  lastName: "Ashrafi",
  birthYear: 1993,

  calcAge: function (birthYear) {
    return 2024 - birthYear;
  }
};

console.log(bio.calcAge(1993))
```

We already have the `birthYear`. So wrtiting the same number in two places (`birthYear: 1993` and `console.log(bio.calcAge(1993))
`) is not ideal because we might make a mistake and pass in th wrong year.<br>
If we know the `birthYear`, we should only write it in one place because if it changes we have to change it everywhere.<br>

### A Short Intro Into `this` Keyword
What if there was a way to directly access the `birthYear` from the object instead of having to pass it in as a parameter?<br>

```javascript
const bio = {
  firstName: "Naz",
  lastName: "Ashrafi",
  birthYear: 1993,

  calcAge: function (birthYear) {
    return 2024 - birthYear;
  }
};

console.log(bio.calcAge(1993));
```

In this `calcAge` function, we can read the `birthYear`directly from the object without passing it as a parameter.<br>

In this function, we no longer need the parameter.

```javascript
calcAge: function (birthYear) {
  return 2024 - birthYear;
}
```

```javascript
calcAge: function () {
  return 2024 - birthYear;
}
```
And we will read the birthYear directly from the object and for that we will use the `this` keyword.<br>
`this` keyword/variable is basically equal to the object on which the method is called.<br>

or in other words, it is equal to the object calling the method.<br>
 
 Who is calling the method?<br>
 
 So here, in the `calcAge()` method, the objcet that is calling the method is `bio`
 ```javascript
 console.log(bio.calcAge(1993));
```

That means inside this method, the `this` keyword/variable will point to `bio`
```javascript
calcAge: function (birthYear) {
  return 2024 - birthYear;
}
```
=>

```javascript
const bio = {
  firstName: "Naz",
  lastName: "Ashrafi",
  birthYear: 1993,

  calcAge: function () {
    return 2024 - this.birthYear;
  }
};

console.log(bio.calcAge());
// we don't need to pass a parameter 
```

`this` points to `bio` so then `this.birthYear` points to `birthYear: 1993` <br>

Let's say we need to access `age` multiple times throughout our program. It's be like this : 


```javascript
const bio = {
  firstName: "Naz",
  lastName: "Ashrafi",
  birthYear: 1993,

  calcAge: function () {
    return 2024 - this.birthYear;
  }
};

console.log(bio.calcAge());
console.log(bio.calcAge());
console.log(bio.calcAge());
```
When we call the `calcAge()` function multiple times, it means the computation will happen multiple times. It's not a big deal in this case but in heavier calculations, it will take some more time and that's not a good practice. <br>
What we can do is to calculate `age` once, then store it in the Object and the we can retrieve the Object as a property from the object.<br>
We can use the `this` keyword to store a new property.

```javascript
const bio = {
  firstName: "Naz",
  lastName: "Ashrafi",
  birthYear: 1993,
  
  // we stored age in the object and returned it
  calcAge: function () {
    this.age = 2024 - this.birthYear;
    return this.age;
  }
};

// first we call the calcAge
console.log(bio.calcAge());

// if we check for console.log(bio.age);
// before calling the calcAge the output will be undefined
// because the code checks for the age property of the bio object  before
//the calcAge function has a chance to set it.
console.log(bio.age);
console.log(bio.age);
console.log(bio.age);
```

First we stored `age` in the object and returned it.<br>
Then we call the `calcAge` function **before** the `console.log` statement.<br>
This ensures the function is executed, setting the `age` property with the calculated value.<br>
Then, the `console.log` uses the updated `bio` object with the set `age`.<br>
