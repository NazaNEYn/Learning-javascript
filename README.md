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

Evey value is either:
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

*Example*

```javascript
const year = "2024";
console.log(year + 5); // 20245
```

It doesn't automatically conver the string `("2024")` into number type.<br>
We need to convert it by `Number()` function.<br>

```javascript
const year = "2024";
console.log(Number(year) + 5); // 2029

```
