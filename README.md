# Learning-javascript
<hr>

## Value And Variable

**Value**: a piece of data <br>
*Example:* 
```javascript
console.log("Naz")``` <br>

**Variable** : It's a box that we can store a value in.

We can store values into variables. So this way we can reuse them over and over again. <br>
let firstName = "Naz" <br>
"Naz" is a value and we assigned it to a variable. It's called *declaring a variable*.
<br>
<hr>

## Data Types

Evey value is either:
1. Object : <br>
let me  { <br>
        name: "Naz" <br>
}

2. Primitive : <br> 
let firstName = "Naz" <br>
let age = 30 

A value is only primitive when it's not an object.

### Primitive Data Types :
1. number  
2. string
3. boolean
4. undefined
5. null
6. symbol
7. big int

**Number**: <br>
let age = 30 

**Strings**: <br>
let firstName = "Naz"

**Boolean**: <br>
It's always either true or false. <br>
let fullAge = true

**Undefined**:<br>
A value hasn't been defined for the variale (empty value) <br>
let age;

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

## "Type of" Operator 
We can use to show the type of a value.

*Example:* <br>
constole.log(typeof 'Naz')<br>

## Assigning a New Value

let firstName = 'Naz'<br>
firstName = 'Ash'<br>
console.log(firstName)<br>
