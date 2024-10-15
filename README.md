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

A scope in JavaScript is the current context of code, which determines the accessibility of variables to JavaScript
there are two types:
a. Global scope variables - are those variables declared outside a block
b. Local scope variables are those declared inside a block of code.

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




































