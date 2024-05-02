# Learning-javascript
Taking notes from Jonas Schmedtmann's Javascript course.
<hr>

## Value And Variable

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
<hr>

## Data Types

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

### Primitive Data Types :
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

## "Type of" Operator 
We can use to show the type of a value.

*Example:* <br>
```javascript
constole.log(typeof 'Naz')
```

## Assigning a New Value

```javascript
let firstName = 'Naz'
firstName = 'Ash'
console.log(firstName)
```
