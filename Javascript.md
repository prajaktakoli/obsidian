
-add javascript code at the end of the body section
-------
variables: value of varible can change
let keyword to declare a variable
eg. let name;
- cannot be a reserved keyword
- cannot start with a num
- cannot contain space or hyphen
- case sensitive
- use camelCase
-------------------------
constants : value of constants do not change

let interestRate = 0.3;
interesetRate = 1;
console.log(interestRate) //it will give error as constants cannot be reassigned.

Types 
1. Primitive:
	1. string
	2. boolean
	3. number
	4. undefined - it is also a type and a value
	5. null
2. reference 
	1. Objects
	2. Arrays
	3. Functions
	----------------------
	Objects :
	let person = {
			name : 'Mosh',
			age : 30
		}
	console.log(person);
Accessing properties of objects using below methods:
1. Dot Notation
		person.name = 'John';

-------------
Arrays : to store a list
length is dynamic.
to access elements using square brackets - selectedColors[2];

let selectedColors = ['red', 'blue'];

selectedColors[2] = 'green';

console.log(selectedColors);
----------------------
we can also store multiple types in an array like - ['red', 'blue', 1];

----------------
Functions :

function greet(){
	console.log('Hello World);
}
greet();

Passing parameters to a function:

function greet(name)
{
	console.log('Hello ' + name);
}
greet('John');