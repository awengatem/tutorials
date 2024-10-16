# tutorials
this is a repo for tutorials

#JAVASCRIPT TUTORIALS

##### PART ONE

1. ### Array - is a data structure that is used to store multiple values in a single variable
   
#Example:

const fruits = ['apple', 'mango', 'banana', 'berry'];
/* fruits.push('pineapple');  */ - Add elements to the End of an array
/* fruits.pop(); */ - remove elements from the End of an Array
/* fruits.unshift('pineapple'); */ - Add elements to the begining of array
/* fruits.shift() */ - remove an element from the begining of an array
console.log(fruits);


#Array Methods

push - add an element to the end of an array
pop - remove an element from the end of an array
shift - remove an element from the beginning of an array
unshift - add an element to the beginning of an array
sort - arrange elements in an array from ascending to descending and vice versa
concat - adding tow or more arrays to form a single array
reverse - reverse the order of an array
include - check whther an element is available or not
slice - used to trim an array

Example:

const list1 = ['apple', 'mango', 'banana', 'berry'];
const list2 = [1, 2, 3, 4, 5];
const newList = list1.concat(list2);
console.log(newList);

#Accessing Arrays - Arrays can be accessed using the bracket notation e.g 

const fruits = ['apple', 'orange', 'mango', 'pineapple'];
console.log(fruits[0]);
console.log(fruits[1]);
console.log(fruits[2]);
console.log(fruits[3])

2. ### Object - is a data structure which allows us to store data with labels.
   Example:
   
const users = {
  name: 'aweng',
  id: 1717,
  email: 'aweng@gmail.com',
  location: 'nakuru',
};

#Objects can be accessed using the dot notation

Example: 

const users = {
  name: 'aweng',
  id: 1717,
  email: 'aweng@gmail.com',
  location: 'nakuru',
};
console.log(users.name);

#Objects can also be accessed using the bracket notation but in few cases

##adding elements to an object

const person = {
  name: 'aweng',
  id: 1717,
  email: 'aweng@gmail',
  location: 'nakuru',
};

person.nickname=("jon agata")
console.log(person);

##updating elements in an object

const person = {
  name: 'aweng',
  id: 1717,
  email: 'aweng@gmail',
  location: 'nakuru',
};
person.name = 'atem';
console.log(person.name);

##deleting elements from an objects

const person = {
  name: 'aweng',
  id: 1717,
  email: 'aweng@gmail',
  location: 'nakuru',
};

delete person.name;
console.log(person);

3. ### FUNCTION - is a block of code that performs a specific task

Example:

function myfunc() {
console.log('Hello World');
}
myfunc();

the code above is an example a of function declaration

function expression is storing the function inside a variable. e.g

const myfunc = () => {
  console.log('Hello World');
};
myfunc();

#Callback function - 
A callback function - is when we provide a function as an arguement to other function, that function is known as a callback function.

example:

function myFunc(fn) {
  let value = 10;
  fn(value);
}
myFunc(function (value) {
  console.log(`the value is ${value}`);
});

4. ### Methods - are functions available inside an object only.

Example: 

const person = {
  name: 'Aweng',
  age: 33,
  greet: function () {
    return `Hello, my name is ${person.name} & I am ${person.age} years old.`;
  },
};
console.log(person.greet());

### A scope

A scope in JavaScript is the current context of the code, which determines the accessibility of variables to JavaScript
there are two types:
a. Global scope variables - are those variables declared outside a block

Example: 

let x = 200;

function myFunc() {

}
console.log(myFunc());

/* x is a global variable because it can be accessed anywhere in the code */


b. Local scope variables are those declared inside a block of code.

Example:

function myFunc() {
  let x = 200;
}
console.log(myFunc());

/* x is a local variable because it can only be accessed with the function */

5. ### JSON - JavaScript Object Notation - used to transmit data btw the server and application
6. 
example: 

{
  "name": "aweng",
  "age": 33,
  "email": "aweng@gmail.com",
  "isSubscribed": true,
  "hobbis": ["reading", "Running", "Cooking"],
  "address": {
    "city": "Nairobi",
    "idk": true
  }
}

#How to convert an object to a json string

const person = {
  "name": "aweng",
  "age": 33,
  "email": "aweng@gmail.com",
  "isSubscribed": true,
  "hobbis": ["reading", "Running", "Cooking"],
  "address": {
    "city": "Nairobi",
    "idk": true
  }
}

const jsonString = JSON.stringify(person);
console.log(jsonString);

#How to convert back to an object

const person = {
  "name": "aweng",
  "age": 33,
  "email": "aweng@gmail.com",
  "isSubscribed": true,
  "hobbis": ["reading", "Running", "Cooking"],
  "address": {
    "city": "Nairobi",
    "idk": true
  }
}

const jsonString = JSON.stringify(person);
console.log(jsonString);

const parsedObject = JSON.parse(jsonString)
console.log(parsedObject);

6. ####DATE

const date = new Date()
const year = date.getFullYear()
const month = date.getMonth()
const day = date.getDay()
const hours = date.getHours()
const minutes = date.getMinutes()
console.log(year);
console.log(month);
console.log(day);
console.log(hours);
console.log(minutes);

7. #### SetInterval & SetTimeout

###setInterval - is used to execute a code a number of time
example...

setInterval(()=> {
  console.log("This code wil"); 
  
}, 2000)

####setTimeout - used to execute a code after a specify delay
example...
setTimeout(()=>{
  console.log("This code will be executed!!");
  
}, 3000)

###clearInterval is used to stop the interval

example for setinterval, setTimeout and clearinterval
/* This function will run for 10 seconds and then stopped */

const intervalId = setInterval(()=>{
  console.log("This function is being executed at the interval");
  
}, 1000)

/* Stop the interval after 10 seconds */

setTimeout(()=>{
  clearInterval(intervalId)
  console.log("Interval Stopped");
  
}, 10000)


##### PART TWO

1. ## template strings - also known as template literals. Are a feature in JavaScript that allows you to create strings with embedded expressions.
2. 
They are denoted by backticks `` instead of single or double quotes. Template strings provide a more flexible and concise way to construct strings, especially when they involves variables or expressions.
N/B: This temple literals enable you to write a string inside them.

Example:
 
const fname = 'Aweng';
const lname = 'Atem';
console.log(`My first name is ${fname} and my last name is ${lname}`);

2. ### Arroy Functions in js - also known as fat arrow functions, are a shorter way of writing functions in JavaScript

##normal function below

function myFunc() {
  console.log('Hello World');
}
myFunc();

--in this normal function you can remove the bracket if you have one variable
--you can also remove the curly braces together with the return keyword. You cannot remove one. You have to remove both of them or leave both of them.

###an arrow function

const greet = () => console.log('Hello World');

greet();

3. ### Enhanced object literals - area a set of enhancements to the syntax for defining objects in Javacript
   
Example:

function user(name, age, work) {
  return {
    name: name,
    age: age,
    work: work,
  };
}

const res = user('aweng', 33, 'Programmer');

console.log(res.name);
console.log(res.age);
console.log(res.work);

###in enhanced object property, the key and value are the same e.g name = name, age = age but you can remove one name or age and the code will still run.

4. ### Default function parameters - allows you to assign default values to function parameters. When a function is called, and an argument is not provided for a parameter, the default value will be used instead.
   
example:

function loop(count = true) {
  if (count == true) {
    for (i = 0; i <= 5; i++) {
      console.log(`Count: ${i}`);
    }
  }
}
loop(true);



5. ####spread operators in JavaScript - is used to make copies of an object. it uses three dot (...). It is also used to combine arrays and objects.

##spread operator by using a function

Example:

function myFunc(a, b, c, d) {
  console.log('a', a);
  console.log('b', b);
  console.log('c', c);
  console.log('d', d);
}
const colors = ['red', 'green', 'blue', 'teal'];
myFunc(...colors);

##spread operator by using an array

Example: 

const num1 = ['one', 'two', 'three', 'four'];
const num2 = ['five', 'six', 'seven', 'eight'];
const newNum = [...num1, ...num2];
console.log(newNum);

##spread operator by using object

Example: 

const obj1 = { x: 1, y: 2 };
const obj2 = { z: 3 };
const obj3 = { ...obj1, ...obj2 };
console.log(obj3);


6. ### The rest operator syntax allows a function to accept an infinite number of arguments. It is basically used for cloning elements
       As an array, providing a way to represent variadic functions in JavaScript. Variadic functions are functions which accept unlimited number of arguments.
	A rest operator must be written after parameters if they are many

Example: 

function user(...userData) {
  console.log(userData);
}
user('aweng', 'programming', 'football');

7. ### Destructuring - allows us to unpack values from data structures such as arrays, objects into distinct variables.

###Array destructuring - in array destructuring, the order does matter and the name doesn't matter

Example: 

const num = ['one', 'two', 'three', 'four']; - This is an array

const [one, two, three, four] = num; - this is a destructuring syntax. the brackets are used to store elements from array

console.log(one);
console.log(two);
console.log(three);
console.log(four);

Example2:

function fn() {
  return [1, 2, 3, 4];
}
let a, b, c, d;
[a, , c, d] = fn(); - this is how to ignore the values in desructuring by proving an empty space and a comma.  This can only work in array destructuring
console.log(a);
console.log(b);
console.log(c);
console.log(d);


###object destructuring - Here the order doesn't matter but the name does.

Example: 

const students = {
  name: 'aweng',
  id: 1717,
  age: 33,
};

const { name, id, age } = students; - when you replace for example age with another variable name, it wont work.
console.log(name);
console.log(id);
console.log(age);

#renaming variables in destructuring

const num = {
  x: 100,
  y: 200,
};
const { x: new1, y: new2 } = num; - this is how we will be renaming variables in object destructuring
console.log(new1);
console.log(new2);

##object destructuring and rest operator

Example:

let { a, b, ...rest } = { a: 100, b: 200, c: 300, d: 400, e: 500 };
/* console.log(a);
console.log(b); */
console.log(rest);

##function destructuring in JavaScript

Example:

const person = {
  name: 'aweng',
  age: 33,
  country: 'USA',
};

function fn({ name, age, country }) {
  console.log(`${name}`);
  console.log(`${age}`);
  console.log(`${country}`);
}
fn(person);

###nested destructuring - destructuring inside a destructuring 

Example:


const songs = [
  {
    name: 'Lucky you',
    singer: 'Joyner',
    duration: 4.34,
  },
  {
    name: 'Just like you',
    singer: 'NF',
    duration: 3.23,
  },
  {
    name: 'Humble Singer',
    singer: 'Joyner',
    duration: 2.33,
  },
  {
    name: 'Old town Road',
    singer: 'Kendrick Lamar',
    duration: 1.43,
  },
  {
    name: 'Cold Sholder',
    singer: 'Central Cee',
    duration: 5.23,
  },
];

const [, , , , { singer }] = songs; -- we use commas to ignore people. like comma one will ignore Joyner, two Nf and so on to get at the singer you want
console.log(singer);


8. ### Ternary operator in JavaScript - is a shorter way of writing conditional expressions. 

syntax:

// condition ? exprIfTrue : exrIfFalse - It doesn't have else if statement. it is only if and else statement

Example: 

let x = 10;

x < 9 ? console.log('Hello') : console.log('Hi');

9. #### For...in loop in JavaScript - is used to iterate over the enumerable properties of an object. It is a way to loop through the keys (property name) of an object.

syntax: 

for (variable in iterable){.....}

Example:

##iterating over an object

const person = {
  name: 'aweng',
  age: 33,
  gender: 'male',
};

for (let keys in person) {
  console.log(keys, person[keys]); -- person[keys] is used to print out the values
}


##iterating over an array

Example1: 

let list = ['one', 'two', 'three', 'four'];

for (let index in list) {
  console.log(list[index]);
}

Example2:

const object = {
  a: 1,
  b: 2,
  c: 3,
};
for (let index in object) {
  console.log(`${index}: ${object[index]}`); -- this print out the index and the values
}



### for...of loop - is a modern iteration statement that provides a concise and easy way to loop over elements in iterable objects like arrays, strings, maps, sets, and more, it allows you to iterate directly over the values of the elements, rather than dealing with their indices or keys, which makes the code more readable and less error-prone.

syntax:

for(variable of iterable){...}

Example:

const peoples = ['aweng', 'peter', 'andrew', 'john'];

for (let people of peoples) {
  console.log(people);
}

######################## Helpers

10. ###{foreach} For Each Helper - when we call the foreach helper we pass in anonymous callback function, this function gets called one time for every element in the array.

Example:

const colors = ['teal', 'blue', 'red', 'green'];

colors.forEach(function update(color) {
  console.log(color);
});

---example with arrow function

const colors = ['teal', 'blue', 'red', 'green'];

colors.forEach((color) => console.log(color));

11. ### {MAP()}Map Helper -- Map() method creates a new array populated with the results of calling a provided function on every element in the calling array.

Example: 

let numbers = [1, 2, 3, 4, 5];

let double = numbers.map((num) => num * 2);

console.log(double);
 

---the difference between map and foreach is that map creates entirely a new and modified array while foreach just modified the previous array and doesn't create a new array.

Example2:

const numbers = [65, 44, 12, 4];

function myFunc(num) {
  return num * 10;
}

const res = numbers.map(myFunc);

console.log(res);

12. #### filter() - is a built-in array method in JavaScript that allows you to create a new array containing elements that pass a certain condition. it provides a clean and concise way to filter out elements from an array on a specified criteria.

Exampe:

const songs = [
  { name: 'Lucky You', duration: 4.43 },
  { name: 'Just like you', duration: 3.43 },
  { name: 'The Search', duration: 2.43 },
  { name: 'The Box', duration: 1.43 },
];

console.log(songs.filter((song) => song.duration < 3)); --- it filter out stuffs based on the condition given in the arrow function

Example: 2

const computers = [
  { ram: 4, hdd: 100 },
  { ram: 8, hdd: 200 },
  { ram: 16, hdd: 300 },
  { ram: 32, hdd: 400 },
];

console.log(computers.filter((computer) => computer.ram > 16));

Example3: 

const ages = [32, 33, 16, 40];

function checkAge(age) {
  return age >= 18;
}
console.log(ages.filter(checkAge));

Exanple: 4

const words = [
  'spray',
  'limit',
  'elite',
  'exuberant',
  'destruction',
  'present',
];

console.log(words.filter((word) => word.length >= 6));


13. #### Find() Method - is another built-in array helper in JavaScript that allows us to find the first element in an array that matches a specific condition. it returns the value of the first element that satisfies the given testing functions, or undefined if no element is found.

Example:

const peoples = [
  { name: 'aweng', age: 33 },
  { name: 'john', age: 34 },
  { name: 'peter', age: 67 },
  { name: 'james', age: 32 },
  { name: 'andrew', age: 45 },
];
console.log(peoples.find((people) => people.name == 'aweng'));


### every() method - tests whether all elements in the array pass the condition specified by the provided callback function....

Example: 

const peoples = ['huxn', 'jordan', 'alex'];

console.log(peoples.every((people) => people.length == 4)); the result is 4 because not the length of every element in the array is 4


### some() method - tests whether at least one element in the array passes the condition specified by the provided callback function. It returns true if the callback function returns true for at least one element, and false if no element passes the condition.

Example:

console.log(peoples.some((people) => people.length == 4)); - the result is true because the length of some elements in the array is equal to 4


## reduce() method - applies the reducer function to each element of an array, accumulating the results into a single value. It is often used to perform calculations or aggregation on array elements  and simplify the array into a single value.


Example:

const numbers = [1, 2, 3, 4, 5];

const sum = numbers.reduce((p, c) => {  -- the p is the previous value of the array and the c is the current value of the array
  return p + c;
}, 0);
console.log(sum);


14. #### Map - is a built-in data structure that allows you to store key-values pairs where both the keys and values can be of any data type. It is similar to an object, but with a few key differences.

keys can be of any data type: unlike objects, where keys are limited to strings and symbols, Map allows you to use any data type as keys, including numbers, Booleans, objects, and even other Map instances.

Example: 

const map = new Map();

const keyOne = 'Huxn';  ---- these are keys declared
const keyTwo = {};
const keyThree = function () {};

map.set(keyOne, 'Value of Key One'); --- this is how to add keys
map.set(keyTwo, 'Value of Key One');
map.set(keyThree, 'Value of Key One');

console.log(map);






































