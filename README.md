# _Roman Numeral_

#### _ Aug 20, 2020_

#### By _**Natalie Murphy & William Donovan - Seid**_

## Description

Write a method to convert numbers into Roman numerals. Roman numerals are based on seven symbols:

Symbol = Value
* I = 1
* V = 5
* X = 10
* L = 50
* C = 100
* D = 500
* M = 1,000

* The most basic rule is that you add the value of all the symbols: so II is 2, LXVI is 66, etc.

* The exception is that there may not be more than three of the same characters in a row.
Instead, you switch to subtraction.

* So instead of writing IIII for 4, you write IV (for 5 minus 1); and instead of writing LXXXX for 90, you write XC.

* You also have to separate ones, tens, hundreds, and thousands. 

* In other words, 99 is XCIX, not IC. You cannot count higher than 3,999 in Roman numerals.

* Do not add any UI logic until you've completed your business logic (and included testing).

* The program recognizes number input

---------------------------------------- 
# Test 1

the program would literal traslation of numbers to strings of Is
  input example: number 14
  output example:  IIIII IIIII IIII

### Code: 
let number = 10;
let numberArray = [];
while (number > 0) {
  numberArray.push("I");
  number --;
}
console.log(numberArray);

# Test 2
the program counts the number of Is and translate I to one of the V symbol
 input example: 5
 output example: IIIII = V change to V 
### code
let number = 10;
let iArray = [];
let finalArray = []
let check = 0
while (number > 0) {
  iArray.push("I");
  number --;
}
for (const element of iArray) {
	check += 1;
  if (check === 5) {
  	finalArray.push("V")
    check = 0;
  }
}

const roman = finalArray.join("");
console.log(finalArray);
console.log(roman)

# Test 3
the program counts the number of Is and translate I to the varriang sombols:
V       5
X       10
L       50
C       100
D       500
M       1,000

 input example: 15
 output example: IIIII IIIII IIIII = VVV = XV 

### CODE:

let number = 26;
let iArray = [];
let finalArray = []
let check = 0
while (number > 0) {
  iArray.push("I");
  number --;
}
for (const element of iArray) {
	check += 1;
  if (check === 10) {
  	for (i=0; i<check; i++) {
  		iArray.shift();
    }
  	finalArray.push("X")
    check = 0;
  }
}
for (const element of iArray) {
 	check += 1;
  if (check === 5) {
  	for (i=0; i<check; i++) {
  		iArray.shift();
    }
    finalArray.push("V")
    check = 0;
  }
}
let romanArray = finalArray.concat(iArray);
const roman = romanArray.join("");
console.log(finalArray);
console.log(roman)




The program recognizes that X IIII is too long and adjust to the rule of Three 
 input example : X IIII
 output example : XIV




### Specs
I = 1
II = 2
III = 3 

IV=4 

V=5
VI=6
Vii=7
Viii=8

ix=9

x=10

## Setup/Installation Requirements

* _This is a great place_
* _to list setup instructions_
* _in a simple_
* _easy-to-understand_
* _format_

_{Leave nothing to chance! You want it to be easy for potential users, employers and collaborators to run your app. Do I need to run a server? How should I set up my databases? Is there other code this app depends on?}_

## Known Bugs

_{Are there issues that have not yet been resolved that you want to let users know you know?  Outline any issues that would impact use of your application.  Share any workarounds that are in place. }_

## Support and contact details

_{Let people know what to do if they run into any issues or have questions, ideas or concerns.  Encourage them to contact you or make a contribution to the code.}_

## Technologies Used

_{Tell me about the languages and tools you used to create this app. Assume that I know you probably used HTML and CSS. If you did something really cool using only HTML, point that out.}_

### License

*{Determine the license under which this application can be used.  See below for more details on licensing.}*

Copyright (c) 2016 **_{List of contributors or company name}_**