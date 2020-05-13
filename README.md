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
#### Escape Sequences
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

#### String Concatenation
```javascript
var name = "Song" + " " + "Gee"
var name += "is the best!" // Same for -=. *=, /=

var ending = "\n Yours Sincerely";
name += ending
```

#### Accessing String Characters
```javascript
var firstName = "ada";
var secondLetterOfFirstName = firstName[1];

// Strings are Immutable!
firstName[0] = 'M'; // We CAN'T do this!

// Find the length of any string
var stringLength = firstName.length
```

### 2.7 Arrays
Allows you to store list of values
Can be of **different** datatypes
```
var ourArray = ["John", 23];
var nextArray = [true, false, 17, "Hello World!"];
```

#### Nested Arrays
Arrays can be stored within other arrays
```
var nestedArray = [["the universe", 42], ["everything", 101010]];
```
#### Accessing Array Elements
```
var myArray = [50, 60, 70];
var myNumber = myArray[0]; //myNumber has value 50

myArray[1] = 35; // myArray is now [50, 35, 70];
```
For nested arrays, use multiple sqaure brackets
```
var nestedArray = [[1, 2], [3, 4]];
myNumber = nestedArray[0][1]; // Equals to 2, left most square bracket is the outer array
```

#### Manipulating Array Elements
Using *push()*, append one or more elements at the END of the array
```
var myArray = [50, 60, 70];
mrArray.push(80, 90); // myArray is now [50, 60, 70, 80, 90];
```

Using *pop()*, returns and removes the LAST element of an array
```
var ourArray = [10, 20, 30];
var removedNumber = ourArray.pop();
//removedNumber is 30, and ourArray is now [10, 20]
```

Using *shift()*, similar to pop, but returns and removes the FIRST element from the array
```
var ourArray = [10, 20, 30];
var removedNumber = ourArray.pop();
//removedNumber is 10, and ourArray is now [20, 30]
```

Using *unshift()*, similar to push, but appends one or more elements at the START of the array
```
var ourArray = ["B", "C", "D"];
ourArray.unshift("A");
// ourArray is now ["A". "B", "C", "D"]
```

## 3. Creating Functions!
Create your own reuseable pieces of code using the *function* keyword!
```
function ourNewFunction() {
 console.log("Hello, World!");
}

function argsFunction(a, b){
 return a - b; // Returns the result of a minus b
}

var myvalue = argsFunction(5, 3); // Gives you 2
```

Global scope applies, functions can use variables outside it as long as they are in the main program
However, variables inside functions have **local scope** , and are not be able to be accessed by other functions
When you have 2 variables with the same name, one local and one global, in a local scope, the local variable takes priority

## 4. Creating Conditional Statements

### Using If, Else If, and Else Statements
```
if (trueOrFalse) {
 // Do Something
} else if (trueOrFalse){
 // Do Something else
} else {
 // Do the last thing if the other 2 are not fulfilled
}
```
### Using Switch, Case, Default Statements
```
switch(val){
 case 1:
  answer = "One";
  break;
 case 2:
  answer = "Two";
  break;
 case 3:
  answer = "Three";
  break;
 default:
  answer = "Zero";
  break;
  
}

// To accept multiple values, don't include break for all of them
switch(val){
 case 1:
 case 2:
 case 3:
  answer = "Small";
  break;
  
 case 4:
 case 5:
 case 6:
  answer = "Medium";
  break;
  
 case 7:
 case 8:
 case 9:
  answer = "Large";
  break;
}

// Equality Operator is ==, returning either true or false
if (name == "Bob"){
 console.log("Yay!");
}

// Triple equality === can be used to tell if a value has BOTH the same value and of the same type
// 3 == "3" is TRUE
// 3 === "3" is FALSE

// Similarly, use != and !== to check if a value is NOT equal to something

// You can use >, >=, <, <= to compare numbers or strings
// For strings, we refer to https://javascript.info/comparison
alert( 'Z' > 'A' ); // true
alert( 'Glow' > 'Glee' ); // true
alert( 'Bee' > 'Be' ); // true

/*
The algorithm to compare two strings is simple:

1. Compare the first character of both strings.
2. If the first character from the first string is greater (or less) than the other string’s, then the first string is greater (or less) than the second. We’re done.
3. Otherwise, if both strings’ first characters are the same, compare the second characters the same way.
4. Repeat until the end of either string.
5. If both strings end at the same length, then they are equal. Otherwise, the longer string is greater.
*/

// Use && and || for AND and OR respectively
