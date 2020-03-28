# Javascript-codingnotes
Learning how to create .md files and compiling JS tutorials

## 1. Introduction
### List of IDEs, websites and ways to code JS
* Any IDE like VSCode, Sublime, etc.
* Save it as a script in a html file and run it in any web browser (Open JS console)
* freecodecamp.org, web editor
* https://codepen.io.pen/ (3-in-1 Editor with HTML, CSS and JS)
* https://scrimba.com (Both Popup and Console Logs)

## 2. Javascript Syntax Features
### 2.1 Comments!
Comments are meant to increase readability for programmers, and will be ignored by computers!
```
var number = 5; //in-line comment

/*
This is a
multi-line comment
*/
 ```
### 2.2 Data Types
Javascript provides 7 common datatypes:
Undefined, null, boolean, string, symbol, number and object

```javascript
// 1.Undefined - Basically any variable that hasn't been initialized before
var a;

// 2. null - A value of nothing, any variable that is equal to null takes no memory space
var b = null;

// 3. Boolean - Either a True or False, or a 0 or 1 in binary
var a = true; 
var b = false;

// 4. String - A list of characters, intialized using '', "", or ``
var string1 = 'Hello!';
var string2 = "'Hello!'"; //Insert '' by using double quotes
var string3 = `"'Hello!'"`; //Insert both '' and "" by using backticks!

// 5. Symbols - Come back to this later

// 6. Number - A numerical value
var myNumber = 1997;
var myFloat = 3.1415;

// 7. Objects - Container for Key Value Pairs (Come back later!)
```

### 2.3 Initializing Variables
```javascript
var myName = "Alex"; // global variable
let ourName = 'Alex and John'; // local variable, only accessible to current scope
const pi = 3.1415 // Any variable that is not meant to be changed, will return error if you try to change it
```

### 2.4 Printing to Console
Similar to the print functions of other languages, we use console.log(string) instead
```javascript
console.log(10);
console.log("Hello World!");
```

### 2.5 Operators
Add numbers together
```javascript
var add = 5 + 5;
var sub = 6 - 3;
var mul = 6 * 2;
var div = 8 / 2;
var mod = 8 % 2;
var exp = 3 ** 3;
var add += 5;
var sub -= 5;
var increment++;
var decrement--;
```

### 2.6 String Formatting
### Escape Sequences
Code | Output
------------ | -------------
\' | Single Quote
\" | Double Quote
\\ | Backslash
\n | Newline
\t | Tab
\r | Carriage Return
\b | Backspace
\f | Form Feed

### String Concatenation
```javascript
var name = "Song" + " " + "Gee"
var name += "is the best!" // Same for -=. *=, /=

var ending = "\n Yours Sincerely";
name += ending
```

### Accessing String Characters
```javascript
var firstName = "ada";
var secondLetterOfFirstName = firstName[1];

// Strings are Immutable!
firstName[0] = 'M'; // We CAN'T do this!

// Find the length of any string
var stringLength = firstName.length
```

### 2.7 Arrays

