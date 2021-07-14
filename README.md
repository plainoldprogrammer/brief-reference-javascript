# Brief Reference JavaScript
Brief reference of the JavaScript programming language.

---

#### Print a log on the console
```
console.log("This is a log message");
```

#### Get an element by their id
```
var el = document.getElementById("the-element-id");
```

#### Add an event listener to an element
```
var p = document.getElementById("element-id");

p.addEventListener("click", function(event)
{
  p.innerHTML = "You clicked it";
});
```

#### Set an attribute
```
ul.setAttribute("class", "notes");
```

#### Get elements by tag name
```
list = document.getElementsByTagName("ul")[0];

NOTE:	Retrieve the first list in the DOM.
```

#### Create a new li element and add some text content to it
```
list = document.getElementsByTagName("ul")[0];
newElement = document.createElement("li");
newElement.textContent = "Page manimulation from JS is easy";

list.appendChild(newElement);

NOTE:	The element is appended too the first list in the DOM.
```

#### Define a constant
```
const PI = 3.141593;
```

#### Get the length of an array
```
const elements = [1, -1, -3].length
```

#### Loop an array
```
const places = ["Italy", "France", "Portugal"]

console.log("\nUsing an array function: ")
places.forEach(place => {
  console.log(place)
})

console.log("\nUsing a function: ")
places.forEach(function (place) {
  console.log(place)
})
```

#### Basic arrow function
```
value => {
  console.log(value)
}
```

#### Define a constant array
```
const t = [1, -1, 3];
```

#### Use the map method
```
const t = [1, 2, 3]
const m1 = t.map(value => value *2)
```

#### Transform an array of integers to an array of html li
```
const t = [1, 2, 3]
const m2 = t.map(value => "<li>" + value + </li>)
```

#### Assign individual items of an array to a variable
```
const t = [1, 2, 3, 4, 5]
const [first, second, ...rest] = t
```

#### Define an object using object literals
```
const person = {
  name: "Somebody",
  age: 18,
  education: "Engineer"
}
```

#### Reference a property of an object using dot notation
```
console.log(object1.name);
```

#### Reference a property of an object using field notation
```
console.log(object1[fieldName])
```

#### Add properties to an object on the fly using dot notation
```
object1.address = "Helsinki"
```

#### Add properties to an object on the fly using brackets notation
```
object1["secret number"] = 1234
```

#### Define an arrow function in a normal way or with a shortcut
```
const sum = (p1, p2) => {
  return (p1 + p2)
}
```

```
const sumShorthand = (p1, p2) => (
  p1 + p2
)
```

#### Arrow function with a single parameter
```
const area = width => width * width;
```

#### Assign a method to an object by defining a property that is a function
```
const arto = {
  name: "John Doe",
  age: 18,
  education: "PhD",
  greeting: function () {
    console.log("Hello, my name is "  + this.name)
  }
}
```

#### Assign a method to an object after the creation of such object
```
const arto = {
  name: "Arto",
  age: 35,
  education: "PhD",
  greeting: function ()
  {
    console.log("Hello, this is " + this.name)
  }
}

arto.greeting()

arto.sayBye = function () {
  console.log("Good bye, " + this.name)
}

arto.sayBye()
```

#### Storing a method reference in a variable
```
const arto = {
  name: "Arto Hellas",
  age: 35,
  education: "PhD",
  greet: function () {
    console.log("hello, my name is " + this.name)
  },
  doAddition: function(a, b) {
    console.log(a + b)
  },
}

arto.doAddition(1, 4)

// Storing a method reference
const someAddition = arto.doAddition
someAddition(1, 5)
```

#### Define a class and two objects
```
class Person {
  constructor(name, age) {
    this.name = name
    this.age = age
  }
	
  greet() {
    console.log("Hello, my name is " + this.name)
  }
}

const adam = new Person("Adam Ondra", 35)
adam.greet()

const janja = new Person("Janja Garnbret", 22);
janja.greet()
```

#### Destructure an object
```
props = {
  name: "Arto Hellas",
  age: 35,
}

const { name, age } = props;
```

#### Make repeated calls to refresh function every second
```
setInterval(() => {
  refresh()
  counter += 1
}, 1000)
```


#### The correct way of using console log for debugging variables
Instead of:
```
console.log('props value is ' + props)
```
Use:
```
console.log('props value is', props)
```

#### Arrow function written in compact form
Full form arrow function:
```
(note) => {
  return note.id
}
```
Compact form arrow function:
```
note => note.id
```

#### Use template string syntax
Old:
```
console.log('importance of ' + id + ' needs to be toggled')
```
New:
```
console.log(`importance of ${id} needs to be toggled`)
```

#### Convert to an integer
```
parseInt(id);
```

#### Create and modify an array with map
```
const persons = [
  {
    name: "Tony",
    age: 30
  },
  {
    name: "John",
    age: 27
  },
  {
    name: "Peter",
    age: 21
  }
]

const updatedPersons = persons.map(obj => {
  return  { firstName: obj.name + " old", oldAge: obj.age * 2} 
})

console.log(persons);
console.log(updatedPersons);
```

#### Create an instance of a user defined object type
```
function Car(make, model, year)
{
  this.make = make;
  this.model = model;
  this.year = year;
}

const car1 = new Car("Eagle", "1993", "Tsuru");
console.log(car1.make)
```

#### Create an array with the lenght of each element of another array
```
const names = [
  "The bear is white",
  "The lion is the king",
  "The cat is the traitor"
]

const charactersCount = names.map(x => x.length)
console.log(charactersCount)
```

#### Define a class and instantiate an object
```
class Person {
  constructor(name) {
    this.name = name;
  }

  sayHello() {
    console.log("Hello, I'm " + this.name);
  }
}

let waitress = new Person("Elena");
waitress.sayHello();
```

#### Remove 2 elements from an array
```
const position = id;
this.servers.splice(position, 2);
```

#### A simple promise
```
let promiseExample = new Promise((resolve, reject) => {
  setTimeout(function() {
    resolve('Success!');
  }, 2000);
});

console.log("Some other code is executed");

promiseExample.then((successMessage) => {
  console.log("Yes! " + successMessage);
});
```


#### Create an object with properties
```
let person = {
  firstName: 'John',
  lastName: 'Doe'
};
```

#### Access object properties using array notation
```
let person = {
  firstName: 'John',
  lastName: 'Doe'
};

console.log(person['firstName']);
console.log(person['lastName']);
```

#### Access to a property that contains spaces in their name
```
let person = {
  'full name': 'John Doe'
};

console.log(person['full name']);

NOTE: Is not possible to use the dot notation to access to properties that contains spaces.
```

#### Iterate over properties of an object using for...in loop
```
let person = {
  name: 'John',
  age: 32,
  city: 'New York',
  country: 'USA'
}

for (let key in person) {
  console.log(key + ": " + person[key]);
}
```

#### Add a method to an existing object
```
let person = {
  name: 'John',
  city: 'New York'
}

person.greet = function() {
  console.log('Hi! I am ' + this.name + ' from ' + this.city);
}

person.greet();
```

#### Define a function and add it to an object
```
let person = {
  name: 'John',
  city: 'New York'
}

function greet() {
  console.log('Hello, I am' + this.name + ' from ' + this.city);
}

person.greet = greet;
person.greet();
```

#### Define methods using the object literal syntax
```
let person = {
  name: 'John',
  city: 'New York',
  greet: function() {
    console.log("Hello, I am " + this.name + " from " + this.city);
  }
}

console.log(person.greet());
```

#### Shorthand to define a method in an object
```
let person = {
  name: 'John',
  city: 'New York',
  greet() {
    console.log("Hello, I am " + this.name + " from " + this.city);
  }
}

console.log(person.greet());
```

#### Shorten array
```
const numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9];
console.log(numbers);

numbers.length = 4;
console.log(numbers);
```

#### Short circuit conditionals
```
let age = 23;

age < 21 && console.log('Cant drink alcohol');
age >= 21 && console.log('Can drink alcohol');
```

#### Log an array into a table
```
function Person(firstName, lastName, age) {
  this.firstName = firstName;
  this.lastName = lastName;
  this.age = age;
}

let firstChildren = new Person("Alberto", "Oz", 35);
let secondChildren = new Person("Brenda", "Oz", 29);
let thirdChildren = new Person("Cesar", "Oz", 24);

console.table([firstChildren, secondChildren, thirdChildren]);
```

#### Log an object into a table
```
function Person(firstName, lastName, age) {
  this.firstName = firstName;
  this.lastName = lastName;
  this.age = age;
}

let firstChildren = new Person("Alberto", "Oz", 35);
let secondChildren = new Person("Brenda", "Oz", 29);
let thirdChildren = new Person("Cesar", "Oz", 24);

console.table({firstChildren, secondChildren, thirdChildren});
```

#### Log an object into a table with specific columns
```
function Person(firstName, lastName, age) {
  this.firstName = firstName;
  this.lastName = lastName;
  this.age = age;
}

let firstChildren = new Person("Alberto", "Oz", 35);
let secondChildren = new Person("Brenda", "Oz", 29);
let thirdChildren = new Person("Cesar", "Oz", 24);

console.table({firstChildren, secondChildren, thirdChildren});
```

#### Remove duplicated elements from an array
```
const names = ['Juan', 18, 'Juan', 'Alberto', 'Juan', 'Eduardo', 18];

console.log(names);
console.log([... new Set(names)]);
```

#### Convert a string to a number
```
const error = "404";
console.log(+error);
```

#### Convert a number to a string
```
const error = 404;
console.log(error + '');
```

#### Remove all falsy values from an array
```
const allData = [1, undefined, NaN, 2, null, '@working', true, 3, false];
console.log(allData.filter(Boolean));
```

#### Load data from a file
```
function loadJSON(callback) {
  var xobj = new XMLHttpRequest();
  xobj.overrideMimeType("data.json");
  xobj.open('GET', './js/data.json', false);
  xobj.onreadystatechange = function () {
    if (xobj.readyState == 4 && xobj.status == "200") {
      callback(xobj.responseText);
    }
  };
  xobj.send(null);
}

function loadData() {
  loadJSON(function(response) {
    result = JSON.parse(response);
  });
}

let result;
loadData(result)


NOTE: The file data.json must exists.
```

#### Check if a variable exists
```
if (typeof variable !== 'undefined') {
  // the variable is defined
}
```

#### Pass arguments into an IIFE
```
var someText = "Hello World!";

(function(message) {
  console.log(message);
})(someText);
```

#### Default parameters
```
function printFullName(firstName = 'John', lastName = 'Doe') {
  console.log(`${firstName} ${lastName}`);
}

printFullName();
printFullName('Elon');
printFullName('Elon', 'Musk');
```

#### Import a JavaScript file as a module
```
<script src="js/js.js" type="module"></script>
```

#### Log the type of a value
```
let javaScriptIsFun = true;
console.log(typeof javaScriptIsFun);
```

#### Difference between undefined and null
```
let phone = undefined;
console.log(phone);
console.log(typeof phone);

let year = null;
console.log(year);
console.log(typeof year);
```

#### Check that a variable is not null
```
let phone;

if (phone === undefined) {
  console.log('You should define a value for the phone');
} else {
  console.log('The phone is not undefined');
}
```

#### Show a bug in the typeof operator when using null
```
console.log(typeof null);
```

#### Reverse a string
```
const myName = 'John Doe';
let reversedName = '';

for (let i = myName.length - 1; i >= 0; i--) {
  reversedName += myName[i];
}

console.log(reversedName);
```

#### Create a property on the global object
```
hobby = "programming";
console.log(hobby);

NOTE: This is a very bad practice.
```

#### Log the global object
```
console.log(window);
```

#### Log multiple values
```
const ageJohn = 2037 - 1991;
const ageSammy = 2037 - 2018;
console.log(ageJohn, ageSammy);
```

#### Use the exponentiation operator
```
console.log(2 ** 4);
```

#### Create a multiline
```
console.log('This is a simple multi line \n\
That is created with JavaScript \n\
and can be checked on the console.');
```

#### Create a multiline using template literal syntax
```
console.log(`This is a simple multiline
that is created using the template
literal syntax with javascript`);
```

#### Check the value of NaN
```
console.log(typeof NaN);

NOTE: NaN actually means "invalid number".
```

#### Difference between parseInt and Number
```
console.log(parseInt("123qwerty"));	// Returns 123.

console.log(Number("123qwerty"));	// Return NaN.
```

#### Convert a number to a string
```
console.log(String(23));
```

#### Convert a string to a number
```
console.log(Number("23"));
```

#### Type coercion
```
console.log('23' - '10' + 3);

NOTE:	Using the + it converts to string.

	Using the - it converts to number.
```

#### Declare an empty object
```
{}
```

#### Evaluate a falsy value
```
console.log(Boolean(0));
```

#### Strict equal operator vs loose equal operator
```
const age = '18';

if (age === 18) console.log('You just became an adult (strict)');

if (age == 18) console.log('You just become an adult (loose)')
```

#### Use strict mode
```
"use strict"
```

#### Switch statement
```
const day = 'wednesday';

switch (day) {
  case 'monday':
    console.log('Need to go to work');
    break;
  case 'tuesday':
    console.log('Continue working hard');
    break;
  case 'wednesday':
    console.log('Go to the movies');
    break;
  case 'tursday':
  case 'friday':
    console.log('Go to party');
    break;
  default:
    console.log('Rest');
    break;
}
```

#### Conditional operator as an expression
```
const age = 18;
const drink = age >= 18 ? 'wine' : 'water';
console.log(drink);
```

#### Conditional operator inside a template literal
```
console.log(`I like to drink ${age >= 18 ? 'beer' : 'water'}`);
```

#### Log the console object
```
console.log(console);
```

#### Function declaration
```
function calculateAge(birthYear) {
  return 2037 - birthYear;
}

console.log(calculateAge(1950));
```

#### Function expression
```
const calculateAge = function(birthYear) {
  return 2037 - birthYear;
}

console.log(calculateAge(1950));
```

#### Arrow function
```
const calculateAge = birthYear => 2037 - birthYear;
console.log(calculateAge(1950));
```

#### Arrow function with body
```
const yearsUntilRetirement = birthYear => {
  const age = 2037 - birthYear;
  const retirement = 65 - age;

  return retirement;
}

console.log(yearsUntilRetirement(1989));
```

#### Arrow function with multiple parameters
```
const yearsUntilRetirement = (birthYear, firstName) => {
  const age = 2037 - birthYear;
  const retirement = 65 - age;

  return `${firstName} retires in ${retirement} years`;
}

console.log(yearsUntilRetirement(1989, 'John'));
```

#### Create an array using literal syntax
```
const friends = ['James', 'Willy', 'Davis'];
```

#### Create an array using the Array function
```
const years = new Array(1991, 1984, 2008, 2020);
```

#### Get the last element of an array
```
const friends = ['Jane', 'John', 'Kim'];
console.log(friends[friends.length - 1]);
```

#### Add an element to the end of an array
```
const friends = ['Jane', 'John', 'Kim'];
friends.push('Jay');

NOTE:	push() returns the new size of the array.
```

#### Add an element to beginning of an array
```
const friends = ['Jane', 'John', 'Kim'];
friends.unshift('Jay');

NOTE:	unshift() returns the new size of the array.
```

#### Remove the last element of an array
```
const friends = ['Jane', 'John', 'Kim'];
friends.pop();

NOTE:	pop() returns the removed element.
```

#### Remove the first element of an array
```
const friends = ['Jane', 'John', 'Kim'];
const removed = friends.shift();

NOTE:	shift() returns the removed element.
```

#### Get the index of an element
```
const friends = ['Jane', 'John', 'Kim'];
console.log(friends.indexOf('Ptener'));

NOTE:	If the element doesnt exists indexOf() returns -1.
```

#### Determine if an element exist in an array
```
const friends = ['Jane', 'John', 'Kim'];
console.log(friends.includes('Kim'));

NOTE 1:	includes() is similar to indexOf() but returns true or false.

NOTE 2:	This methods uses strict equality.
```

#### Log two arrays to the same Line
```
const calculateTip = function(bill) {
  return bill >= 50 && bill <= 300 ? bill * 0.15 : bill * 0.2;
}

const bills = [500, 57, 30];
const tips = [calculateTip(bills[0]), calculateTip(bills[1]), calculateTip(bills[2]) ];
console.log(bills, tips);
```

#### Create an object using object literal syntax
```
const softwareDeveloper = {
  firstName: 'John',
  lastName: 'Doe',
  age: 2021 - 1980,
  job: 'developer',
  friends: ['Bill', 'Steve', 'Elon']
};
```

#### Use an expression in the bracket notation
```
const person = {
  firstName: 'John',
  lastName: 'Doe',
  age: 2021 - 1980,
  job: 'developer',
  friends: ['Bill', 'Steve', 'Elon']
};

const nameKey = 'Name';

console.log(person['first' + nameKey])
console.log(person['last' + nameKey]);
```

#### Add a function to an object
```
const person = {
  firstName: 'John',
  lastName: 'Doe',
  age: 2021 - 1980,
  job: 'developer',
  friends: ['Bill', 'Steve', 'Elon'],
  hasDriversLicense: true,

  calcAge: function(birthYear) {
    return 2021 - birthYear;
  }
};

console.log(person.calcAge(1995));
console.log(person['calcAge'](1995));
```

#### Generate a random number between 1 and 6
```
let dice = Math.trunc(Math.random() * 6) + 1;
console.log(dice);
```

#### Merge two arrays
```
const array1 = ['a', 'b', 'c'];
const array2 = ['d', 'e', 'f'];
const array3 = array1.concat(array2);

console.log(array3);
```

#### Set a breakpoint directly on the code
```
debugger;
```

#### Get an element from the dom by their class
```
document.querySelector('.message');
```

#### Change the text content of an element from the dom
```
document.querySelector('.message').textContent = 'Correct Number';
```

#### Change the background color of the body from the dom
```
document.querySelector('body').style.backgroundColor = 'green';
```

#### Change the width of an element through their class name
```
document.querySelector('.number').style.width = '30rem';
```

#### Select multiple elements with the same class
```
const btnsOpenModal = document.querySelectorAll('.show-modal');
```

#### Remove a class from an element
```
message.classList.remove('hidden');

NOTE:	The class name should be specified without the period.
```

#### Add a class to an element
```
message.classList.add('hidden');

NOTE:	The class name should be specified without the period.
```

#### Add an event handler each time a key is pressed
```
document.addEventListener('keydown', function (e) {
  console.log(e.key);
});
```

#### Check if an element contains a specific class
```
const modal = document.querySelector('.message');
modal.classList.contains('hidden');
```

#### Select an element by id
```
const score0El = document.querySelector('#score--0');

const score1El = document.getElementById('score--1');

NOTE:	getElementById is suppose to be a little faster.
```

#### Change dynamically the src of an image
```
const diceEl = document.querySelector('.dice');
diceEl.src = `dice-${dice}.png`;
```

#### Add a class to an element if it doesnt have of remove it if it has
```
const player0El = document.querySelector('.player--0');
player0El.classList.toggle('player--active');
```

#### Skip two elements at the time of destructuring
```
'use strict';

const cities = ['Dallas', 'Vancouver', 'Chicago', 'Seattle'];
const [firstCityToVisit, , , lastCityToVisit] = cities;

console.log(
  `firstCityToVisit = ${firstCityToVisit}\nlastCityToVisit = ${lastCityToVisit}`
);

NOTE:	Add a comma for each element that you want to skip.
```

#### Destructure an array into a variable and put the remainder on their own array
```
const cities = ['Dallas', 'Vancouver', 'Chicago', 'Seattle'];
const [principalCity, ...rest] = cities;
console.log(`principalCity = ${principalCity}\nother cities = ${rest}`);

NOTE:	Doesn't necessarily need call the array rest.
```

#### Provide a default value for destructuring an array with undefined values
```
const companies = ['apple', 'amazon', undefined, 'microsft', 'tesla'];
const [
  bestLaptops = 'unknown',
  bestStore = 'unknown',
  some = 'unknown',
  bestOperatingSystems = 'unknown',
  bestCars = 'unknown',
] = companies;

console.log(
  `bestLaptops =${bestLaptops}\nbestStore = ${bestStore}\nsome = ${some}\nbestOperatingSystems = ${bestOperatingSystems}\nbestCars = ${bestCars}\n`
);
```

#### Rename a property at the time of destructuring
```
const consoles = {
  favorite: 'Snes',
  powerful: 'PS4',
  funny: 'Xbox',
};

const {
  favorite,
  cheapest: nonExistent = 'Non existent',
  powerful,
  funny,
} = consoles;

console.log(
  `favorite = ${favorite}\ncheapest = ${nonExistent}\npowerful = ${powerful}\nfunny = ${funny}`
);
```

#### Destructure only one property from an object
```
const consoles = {
  favorite: 'Snes',
  powerful: 'PS4',
  funny: 'Xbox',
};

const { powerful } = consoles;
console.log(powerful);
```

#### Destructure and rename only one property from an object
```
const consoles = {
  favorite: 'Snes',
  powerful: 'PS2',
  funny: 'Xbox',
};

const { powerful: mostSelled } = consoles;
console.log(mostSelled);
```

#### Copy one object to another object and have 2 different objects
```
const jessica2 = {
  firstName: 'Jessica',
  lastName: 'Williams',
  age: 27,
};

const jessicaCopy = Object.assign({}, jessica2);
jessicaCopy.lastName = 'Davis';

console.log('Before marriage:', jessica2);
console.log('After marriage:', jessicaCopy);

NOTE:	This technique works only on the first level.
	Because of this, this is called "Shallow Copy".
```

#### Switch variables with destructuring
```
let [main, , secondary] = restaurant.categories;
[main, secondary] = [secondary, main];

console.log(main, secondary);
```

#### Destructure nested arrays
```
const nested = [2, 4, [5, 6]];

const [i, , [j, k]] = nested;
console.log(i, j, j);
```

#### Destructure assigment
```
let a = 111;
let b = 999;
const obj = { a: 23, b: 7, c: 14 };

({ a, b } = obj);
console.log(a, b);

NOTE:	When destrucuring a and b, must be wrapping inside parenthesis
	otherwise JavaScript creates a code block an generate an error.
```

#### Create an array with the values from another array using the spread operator
```
const arr = [7, 8, 9];
const newArr = [1, 2, ...arr];
```

#### Get the individual values from an array
```
console.log(...someArray);
```

#### Merge 2 arays using the spread operator
```
const programmingLanguages = ['JavaScript', 'TypeScript'];
const frameworks = ['Angular', 'React', 'Vue'];

const technologies = [...programmingLanguages, ...frameworks];
console.log(technologies);
```

#### Create an array from a string using the spread operator
```
const str = 'Jonas';
const letters = [...str, ' ', 'S.'];
console.log(letters);

NOTE:	arrays, string, maps, sets are iterable. Objects are not.
```

#### Read 3 times from the prompt and create an array
```
const ingredients = [
  prompt("Let's make pasta! Ingredient 1?s"),
  prompt("Let's make pasta! Ingredient 2?s"),
  prompt("Let's make pasta! Ingredient 3?s"),
];
```

#### Collect the unused values in the destructuring assigment using rest pattern
```
const [a, b, ...others] = [1, 2, 3, 4, 5];
console.log(a, b, others);
```

#### Use rest arguments
```
const add = function (...numbers) {
  let sum = 0;

  for (let i = 0; i < numbers.length; i++) {
    sum += numbers[i];
  }

  console.log(sum);
};

add(2, 3);
add(5, 3, 7, 2);
add(8, 2, 5, 3, 2, 1, 4);
```

#### Use the spread operator and rest paraments at the same time
```
const add = function (...numbers) {
  let sum = 0;

  for (let i = 0; i < numbers.length; i++) {
    sum += numbers[i];
  }

  console.log(sum);
};

const x = [23, 5, 7];
add(...x);
```

#### Use the AND operator to call a function
```
if (restaurant.orderPizza) {
  restaurant.orderPizza('mushrooms', 'spinach');
}

Can be replaced using the and operator:

restaurant.orderPizza && restaurant.orderPizza('mushrooms', 'spinach');
````

#### Use the nullish coalescing operator
```
restaurant.numGuests = 0;
const guests = restaurant.numGuests || 10;
console.log(guests);

Can be fixes using the nullish coalescing operator:

// Nullish: null and undefined (NOT 0 or '')
const guestCorrect = restaurant.numGuests ?? 10;
console.log(guestCorrect);
```

#### Use the for of loop
```
const cities = ['Los Angeles', 'Kansas City', 'Dallas'];

for (const city of cities) console.log(city);
```

#### Get the index and the value of each element in a for of loop
```
for (let item of menu.entries()) {
  console.log(`${item[0] + 1}: ${item[1]}`);
}

Or using destructuring:

for (const [i, el] of menu.entries()) {
  console.log(`${i + 1}: ${el}`);
}
```

#### Use the optional chaining operator and the nullish coalescing operator with an array
```
const users = [{ name: 'Jonas', email: 'hello@jonas.io' }];

console.log(users[0]?.name ?? 'User array empty');
console.log(users[1]?.name ?? 'User array empty');
```

#### Iterate throught the keys of an object
```
for (const day of Object.keys(openingHours)) {
  console.log(day);
}
```

#### Create a set
```
const ordersSet = new Set([
  'Soda',
  'Soda',
  'Burger',
  'Soda',
  'Fries',
]);

console.log(ordersSet);
```

#### Get the number of elements from a set
```
const ordersSet = new Set([
  'Soda',
  'Soda',
  'Burger',
  'Soda',
  'Fries',
]);

console.log(ordersSet.size);
```

#### Determine if a set contains a specific element
```
const ordersSet = new Set([
  'Soda',
  'Soda',
  'Burger',
  'Soda',
  'Fries',
]);

console.log(ordersSet.has('Soda'));
console.log(ordersSet.has('Hotdog'));
```

#### Add an element to a set
```
const ordersSet = new Set([
  'Soda',
  'Soda',
  'Burger',
  'Soda',
  'Fries',
]);

ordersSet.add('Hotdog');
ordersSet.add('Hotdog');
console.log(ordersSet);
```

#### Delete an element from a set
```
const ordersSet = new Set([
  'Soda',
  'Soda',
  'Burger',
  'Soda',
  'Fries',
]);

ordersSet.delete('Risotto');
console.log(ordersSet);
```

#### Delete all the values from a set
```
const ordersSet = new Set([
  'Soda',
  'Soda',
  'Burger',
  'Soda',
  'Fries',
]);

console.log(ordersSet);
ordersSet.clear();
console.log(ordersSet);
```

#### Loop through a set
```
const ordersSet = new Set([
  'Soda',
  'Soda',
  'Burger',
  'Soda',
  'Fries',
]);

for (const order of ordersSet) console.log(order);
```

#### Create a set from an array
```
const staff = ['Waiter', 'Chef', 'Waiter', 'Manager', 'Chef', 'Waiter'];
const staffUnique = new Set(staff);
console.log(staffUnique);
```

#### Create an array with unique elements from another array
```
const staff = ['Waiter', 'Chef', 'Waiter', 'Manager', 'Chef', 'Waiter'];
const staffUnique = [...new Set(staff)];
console.log(staffUnique);
```

#### Determine how many unique elements an array has
```
console.log(
  new Set(['Waiter', 'Chef', 'Waiter', 'Manager', 'Chef', 'Waiter']).size
);
```

#### Determine how many unique letters are in a string
```
console.log(new Set('jonasschmedtmann').size);
```

#### Create a map
```
const rest = new Map();
rest.set('name', 'Classico Italiano');
console.log(rest);
```

#### Access to an individual element of a string
```
const plane = 'A320';

console.log(plane[0]);
console.log(plane[1]);
console.log(plane[2])
```

#### Get the length of a string
```
const language = 'This is JavaScript';
console.log(language.length);
```

#### Get the position of an element in a string
```
const language = 'The JavaScript Language';
console.log(language.indexOf('r'));
```

#### Get the last position of an element in a string
```
const language = 'The JavaScript Language';
console.log(language.lastIndexOf('r'));
```

#### Get the position of a word in a string
```
const language = 'The JavaScript Language';
console.log(language.indexOf('JavaScript'));

NOTE:	indexOf is case sensitive.
```

#### Get a substring from a string
```
const language = 'The JavaScript Language';
console.log(language.slice(4, 14));

NOTE 1:	The index specified as first parameter of slice is inclusive.
	and
	The index specified as second parameter of slice is exclusive.

NOTE 2:	The length of the substring is equal to the second parameter - first parameter.
```

#### Get the first and the last word in a string
```
const language = 'The JavaScript Language';

console.log(language.slice(0, language.indexOf(' ')));
console.log(language.slice(language.lastIndexOf(' ') + 1, language.length));
```

#### Get a substring from a string and start counting from the end
```
const language = 'The JavaScript Language';
console.log(language.slice(-2));
```
#### Difference between a normal function and an arrow function
```
const obj = {
  normalFunction: function () {
    console.log("normal function", this);
  },
  arrowFunction: () => {
    console.log("arrow function", this);
  },
};

console.log("this del ambiente", this);
obj.normalFunction(); // Depends of the object which calls the function.
obj.arrowFunction(); // Depends of the enviroments in which the function was defined.
```

#### Multiline string using template literal syntax
```
let firstName = 'Pele';
let country = 'Brazil';
let sum = (a, b) => a + b;

const message = `My name is ${firstName},
and I'm from ${country}.
My total number of goals is ${sum(640, 639)}
Good luck!`;
```

#### Replace the first occurrence in a string
```
const announcement = "This is the first pc in the pc world";
console.log(announcement.replace("pc", "computer"));
```

#### Replace all the occurrences in a string
```
const announcement = "This is the first pc in the pc world";
console.log(announcement.replaceAll("pc", "computer"));
```

#### Check if a string includes a subtring
```
const plane = "Visual Studio Code";
console.log(plane.includes("Code"));
```

#### Destructure an array (from a string)
```
const [firstName, lastName] = "John Doe".split(" ");
```

#### Join an array
```
const [firstName, lastName] = "John Doe".split(" ");
const newName = ["Mr.", firstName, lastName.toUpperCase()].join(" ");
console.log(newName);
```

#### Fill a string with a specific character
```
const sayHello = "Hello";
console.log(sayHello.padEnd(7, "-"));
console.log(sayHello.padStart(7, "-"));
```

#### Mask a number like a credit card
```
const maskCreditCard = function (number) {
  const str = number + "";
  const last = str.slice(-4);
  return last.padStart(str.length, "*");
};
```

#### Repeat a message 5 times
```
const message = "Your computer will restart right now\n";
console.log(message.repeat(5));
```

#### Enhanced object literal
```
const createPerson = function (firstName, lastName) {
  const person = {
    firstName, // instead of firstName: firstName
    lastName, // instead of lastName: lastName
  };

  return person;
};
```

#### Immediately invoked function expression
```
// IIFE using function declaration
(function () {
  console.log('This will never run again');
})();

// IIFE using arrow function
(() => console.log('This will never run again'))();
```

#### Closure
```
const secureBooking = function () {
  let passengerCount = 0;

  return function () {
    passengerCount++;
    console.log(`${passengerCount} passengers`);
  };
};

const booker = secureBooking();
console.log(booker);

booker();
booker();
booker();
```

#### Create a shallow copy of an array
```
let arr = ['a', 'b', 'c', 'd', 'e'];

// Method 1:
// This let's chain methods
console.log(arr.slice());

// Method 2:
console.log([...arr]);
```

#### Reverse an array
```
const arr = ['j', 'i', 'h', 'g', 'f'];
console.log(arr.reverse());

NOTE:	reverse method mutates the original array.
```

#### Concatenate two arrays
```
arr = ['a', 'b', 'c', 'd', 'e'];
const arr2 = ['f', 'g', 'h', 'i', 'i'];

// Using the concat method
console.log(arr.concat(arr2));

// Using the spread operator
console.log([...arr, ...arr2]);

NOTE:	Both methods doesn't mutate the original arrays.
```

#### Retrieve a json file using the fetch api
```
fetch("DatasetMeta.json")
  .then((response) => response.json())
  .then((json) => console.log(json));
```

#### Access to an array using the for of loop
```
const years = [1980, 1990, 2000, 2010, 2020];

for (const year of years) console.log(`Year ${year}`);
```

#### Access to an array using the for of loop and the forEach method
```
const years = [1980, 1990, 2000, 2010, 2020];

years.forEach(function(year, index, array) {
  console.log(`Year ${year}`);
});
```

#### Access to a map using the forEach method
```
const companies = new Map([
  ['MSFT', 'Microsoft'],
  ['AAPL', 'Apple'],
  ['AMZN', 'Amazon'],
]);

companies.forEach(function(value, key, map) {
  console.log(`${key}: ${value}`);
});
```

#### Access to a set using the forEach method
```
const companies = new Set(['MSFT', 'AAPL', 'MSFT', 'AMZN', 'AMZN']);

companies.forEach(function(value, key, map) {
  // Note: In a Set the key and the value is the same.
  console.log(`${key}: ${value}`);
});
```

#### Add an element to the inside of another element at the beginning
```
const html = `
  <div>
    A new element
  </div>
`;

containerMovements.insertAdjacentHTML('afterbegin', html);
```

#### Map method to access to an array elements
```
const purchases = [10, 15, 20];
const tax = .0825;

// Using map with a function
const purchasesAfterTax = purchases.map(function (mov) {
  return mov * (1 + tax);
});
console.log(purchases);
console.log(purchasesAfterTax);

// Using map with an arrow function
const purchasesAfterTaxArrow = purchases.map(mov => mov * (1 + tax));
console.log(purchasesAfterTaxArrow);
```

#### Filter method to get the positive and the negative values in an array
```
const purchases = [10, 15, 20, -300, 8, -16];

// Using an annonymous function.
const debit = purchases.filter(function (mov, i, arr) {
  return mov > 0;
});
console.log(purchases);
console.log(debit);

// Using an arrow function
const credit = purchases.filter(mov => mov < 0);
console.log(purchases);
console.log(credit);
```

#### Reduce method to sum all the values in an array
```
const purchases = [10, 15, 20, -300, 8, -16];

// Reduce method using an annonymous function
const balance = purchases.reduce(function (acc, curr) {
  return acc + curr;
}, 0);
console.log(balance);

// Reduce method using arrow function
const balance = purchases.reduce((acc, curr) => acc + curr, 0);
console.log(balance);
```

#### Reduce method to return the maximum number in an array
```
const purchases = [10, 15, 20, -300, 8, -16];

const maximumValue = purchases.reduce(function (acc, val) {
  return val > acc ? val : acc;
}, purchases[0]);
console.log(maximumValue);

NOTE: The initial value of the accumulator should be the first value in the array and not 0.
```

#### Reduce method to calculate the average of an array of integers
```
const data = [100, 200, 300];
const average = data.reduce((acc, age) => acc + age, 0) / data.length;
console.log(average);
```

#### Use map, filter and reduce methods together
```
const tax = 0.0825;
const movements = [10, 15, 20, -300, 8, -16];

// PIPELINE
const movementsAfterTax = movements
  .filter(mov => mov > 0)
  .map(mov => mov * tax)
  .reduce((acc, mov) => acc + mov, 0);
console.log(movementsAfterTax);
```

#### Debug a chain call of map, filter and reduce
```
const tax = 0.0825;
const movements = [10, 15, 20, -300, 8, -16];

const totalDepositsUSD = movements
  .filter(mov => mov < 0)
  .map((mov, i, arr) => {
    console.log(arr);	// Results of filter operation
    return mov * tax;
  })
  .reduce((acc, mov) => acc + mov, 0);
  ```
  
#### Find method to get the first occurence of an element
```
const movements = [10, 15, 20, -300, 8, -16];
const firstWithdrawal = movements.find(mov => mov < 0);
console.log(movements);
console.log(firstWithdrawal);
```

#### Prevent a form from submitting a form
```
btnLogin.addEventListener('click', function (e) {
  e.preventDefault();
  console.log('LOGIN');
});

// NOTE: "btnLogin" refers to an element inside a form.
```

#### Make an input to lose the focus
```
btnLogin.addEventListener('click', function (e) {
  inputLoginPin.blur();
});
```

#### Check for equality or for a condition
```
const movements = [10, 15, 20, -300, 8, -16];
console.log(movements);

// Checks only for equality
console.log(movements.includes(-300));
```

#### Flattern an array
```
const arr = [[1, 2, 3], [4, 5, 6], 7, 8];
console.log(arr);
console.log(arr.flat());
console.log('');

// Going two levels deeper using an argument
const arrDeep = [[[1, 2], 3], [4, [5, 6]], 7, 8];
console.log(arrDeep.flat(2));
console.log('');
```

#### Sort an array of strings
```
const owners = ['John', 'Zoe', 'Ariel', 'Maury'];
console.log(owners);
console.log(owners.sort()); // This mutates the original array
console.log(owners);
```

#### Create a new array with 7 empty elements
```
const x = new Array(7);
console.log(x);
```

#### Create an array with dynamic values
```
const z = Array.from({ length: 7 }, (_, i) => i + 1);
console.log(z);

NOTE 1:	The first parameter of "Array.from" is an object with the length of the new array.
NOTE 2: The second parameter of "Array.from" is a call back function that returns the value of the new current element.
```

#### Type coersion of a string to a number
```
Instead of:	Number('3');
Can be:		+'3';

NOTE: The + at the beginning does type coersion.
```

#### Parse a string to a number
```
// Integer
console.log(Number.parseInt('2.5rem'));

// Float
console.log(Number.parseFloat('2.5rem'));

NOTE: The string must start with a number.
```

#### Check if a value is not a number
```
console.log(Number.isNaN(20));
console.log(Number.isNaN('20'));
console.log(Number.isNaN(+'20X'));
console.log(Number.isNaN(23 / 0));
```

#### Check if a value is not an integer
```
console.log(Number.isInteger(23));
console.log(Number.isInteger(23.0));
console.log(Number.isInteger(23 / 0));
```

#### Get the maximum number
```
console.log(Math.max(5, 18, 23, 11, 2));
console.log(Math.max(5, 18, '23', 11, 2));
console.log(Math.max(5, 18, '23px', 11, 2));
```

#### Get the minimum number
```
console.log(Math.min(5, 18, 23, 11, 2));
```

#### Generate a random number between a min and max
```
const randomInt = (min, max) => Math.floor(Math.random() * (max - min) + 1) + min;
console.log(randomInt(3, 8));

NOTE 1:	"floor" is used to work fine with decimal numbers.
NOTE 2:	"floor" round any number down.
```

#### Round a decimal number
```
console.log((2.76).toFixed(1));

NOTE: "toFixed" returns a string.
```


#### Represent a very big number
```
// Incorrect:
console.log(4838430248342043823408394849483209);

// Correct:
console.log(4838430248342043823408394849483209n);

// Correct with small integer numbers:
console.log(BigInt(48384302483));

NOTE 1: Add the 'n' at the end of the number to indicate that is a bigInt.
NOTE 2: The "BigInt" construction function works fine only with small integer numbers.
```

#### Create a new date
```
// Using a constructor
new Date();

// Using a string
new Date('Apr 20 2021 23:46:51')
new Date('December 24, 2015')

// Using specific values
new Date(2037, 10, 19, 15, 23, 5);
new Date(2037, 10, 31);
```

#### Getters and setters of a date
```
const future = new Date(2037, 10, 19, 15, 23);
console.log(future);

// Getters
console.log(future.getFullYear());
console.log(future.getMonth());
console.log(future.getDate());
console.log(future.getDay());
console.log(future.getHours());
console.log(future.getMinutes());
console.log(future.getSeconds());
console.log(future.toISOString());
console.log(future.getTime());

// Setters
future.setFullYear(2040);
console.log(future);
```

#### Get the number of milliseconds since unix epoch
```
console.log(Date.now());
```

#### Pass an array to a function that receives integers
```
const sum = (a, b) => a + b;
const numbers = [2, 3];
const total = sum(...numbers);

console.log(total);
```

#### Create an array using values from another array
```
const numbers = [2, 3];
const moreNumbers = [1, ...numbers, 4, 5];

console.log(moreNumbers);
```

#### Create an array from two arrays
```
const numbers = [2, 3];
const moreNumbers = [4, 5];
const concatenate = [...numbers, ...moreNumbers];

console.log(concatenate);
```

#### Put the first element of an array in a variable and the rest in another array
```
const numbers = [2, 3];
const moreNumbers = [1, ...numbers, 4, 5];
const [firstNumber, ...otherNumbers] = moreNumbers;

console.log("moreNumbers: " + moreNumbers);
console.log("firstNumber: " + firstNumber);
console.log("otherNumbers: " + otherNumbers);
```

#### Clone an array using the spread operator
```
const nums = [1, 2, 3, 4, 5];
const numsClon = [...nums];

console.log(numsClon);
```

#### Clone an object and add a property to it using the spread operator
```
const person = {
  firstName: "John",
  lastName: "Doe",
};

const person2 = {
  ...person,
  edad: 999,
};

console.log(person);
console.log(person2);
```

#### Clone an object using the spread operator and modify a property
```
const person = {
  firstName: "John",
  lastName: "Doe",
};

const otherPerson = { ...person };
otherPerson.firstName = "Jane";

console.log(otherPerson);
```

#### Destructure an object and put the rest on another object
```
const person = {
  firstName: "John",
  lastName: "Doe",
  age: 99
};

const { age, ...restPerson } = person;

console.log('person: ', person);
console.log('age: ', age);
console.log('restPerson: ', restPerson);
```

#### Define a class
```
class Rentangle {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }

  area() {
    console.log(`The area of a rectangle is: ${this.height * this.width}`);
  }
}
```

#### Instantiate an object from a class
```
class Rentangle {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }

  area() {
    console.log(`The area of a rectangle is: ${this.height * this.width}`);
  }
}

const rectangle = new Rentangle(2, 3);
rectangle.area();
```

#### Print the timestamp of a date
```
const future = new Date(2037, 10, 19, 15, 23);
console.log(+future);
```

#### Create a date format based in the US
```
const now = new Date();
labelDate.textContent = new Intl.DateTimeFormat('en-US').format(now);
```

#### Create a date format based in the US with specific options
```
const now = new Date();
const options = {
  hour: 'numeric',
  minute: 'numeric',
  day: 'numeric',
  month: 'long',
  year: 'numeric',
  weekday: 'long',
};

labelDate.textContent = new Intl.DateTimeFormat('en-US', options).format(now);
```

#### Create a date format based on your browser
```
const now = new Date();
const options = {
  hour: 'numeric',
  minute: 'numeric',
  day: 'numeric',
  month: 'long',
  year: 'numeric',
  weekday: 'long',
};
const locale = navigator.language;
console.log(locale);

labelDate.textContent = new Intl.DateTimeFormat(locale, options).format(now);
```

#### Create a formatter for US number
```
const num = 3884764.23;
console.log('US: ', new Intl.NumberFormat('en-US').format(num));
```

#### Create a formatter with a specific unit
```
const num = 3884764.23;

const options = {
  style: 'unit',
  unit: 'mile-per-hour',
};

console.log('US: ', new Intl.NumberFormat('en-US', options).format(num));
console.log('Germany: ', new Intl.NumberFormat('de-DE', options).format(num));
console.log('Syria: ', new Intl.NumberFormat('ar-SY', options).format(num));
console.log(
  navigator.language,
  new Intl.NumberFormat(navigator.language, options).format(num)
);
```

#### Create a formatter with a currency unit
```
const num = 3884764.23;

const options = {
  style: 'currency',
  currency: 'EUR',
};

console.log('US: ', new Intl.NumberFormat('en-US', options).format(num));
console.log('Germany: ', new Intl.NumberFormat('de-DE', options).format(num));
console.log('Syria: ', new Intl.NumberFormat('ar-SY', options).format(num));
console.log(
  navigator.language,
  new Intl.NumberFormat(navigator.language, options).format(num)
);

NOTE: The currency must be specified as option because is not determined by the locale.
```

#### Print the date every second
```
setInterval(function () {
  const now = new Date();
  console.log(now);
}, 1000);
```

#### Select the entire document
```
console.log(document.documentElement);
```

#### Get and set inline styles
```
const message = document.createElement('div');
message.style.width = '120%';
message.style.backgroundColor = '#37383d';

// Doesn't get anything because height is not a property in inline style.
console.log(message.style.height);

// Get the background because is a property in inile style.
console.log(message.style.backgroundColor);
```

#### Get all the styles from an element
```
const message = document.createElement('div');
message.style.width = '120%';
message.style.backgroundColor = '#37383d';

// Get all the styles of the element (including the inline)
console.log(getComputedStyle(message));

NOTE:	This get the computed styles of the element.
```

#### Get a specific property from computed styles in an element
```
const message = document.createElement('div');
message.style.width = '120%';
message.style.backgroundColor = '#37383d';

console.log(getComputedStyle(message).backgroundColor);
```

#### Increase the height of a div by getting their computed style
```
const message = document.createElement('div');
message.style.width = '120%';
message.style.backgroundColor = '#37383d';

message.style.height =
  Number.parseFloat(getComputedStyle(message).height, 10) + 30 + 'px';
```

#### Change a custom property value
```
// In the CSS
:root {
  --color-primary: #5ec576;
}
// In JavaScript
document.documentElement.style.setProperty('--color-primary', 'orangered');

NOTE:	"setProperty" works with custom properties and also with properties.
```

#### Get the class name from an element
```
// In the HTML file:
<img
  src="img/logo.png"
  alt="Bankist logo"
  class="nav__logo"
  id="logo"
/>

// In JavaScript:
const logo = document.querySelector('.nav__logo');
console.log(logo.className);
```

#### Change the value of an attribute
```
// In the HTML file:
<img
  src="img/logo.png"
  alt="Bankist logo"
  class="nav__logo"
  id="logo"
/>

// In JavaScript:
const logo = document.querySelector('.nav__logo');
logo.alt = 'Beautiful minimalist logo';
```

#### Get the value of a custom attribute
```
// In the HTML file:
<img
  src="img/logo.png"
  alt="Bankist logo"
  class="nav__logo"
  id="logo"
  designer="Jonas"
/>

// In JavaScript:

// This way does't work
const logo = document.querySelector('.nav__logo');
console.log(logo.designer);

// This way it works
const logo = document.querySelector('.nav__logo');
console.log(logo.getAttribute('designer'));

NOTE:	The custom attributes are ignored for html if they are ignored because they are not standard.
```

#### Set an attribute and their value
```
// In the HTML file:
<img
  src="img/logo.png"
  alt="Bankist logo"
  class="nav__logo"
  id="logo"
  designer="Jonas"
/>

// In JavaScript:
const logo = document.querySelector('.nav__logo');
logo.setAttribute('company', 'Bankist');
```

#### Get the absolute and the relative url of an image
```
// In the HTML file:
<img
  src="img/logo.png"
  alt="Bankist logo"
  class="nav__logo"
  id="logo"
  designer="Jonas"
/>

// In JavaScript:

// Absolute URL:
const logo = document.querySelector('.nav__logo');
console.log(logo.src);

// Relative URL:
const logo = document.querySelector('.nav__logo');
console.log(logo.getAttribute('src'));
```

#### Get the absolute and the relative url of a link
```
// In the HTML:
<a class="nav__link nav__link--btn btn--show-modal" href="#"> Open account </a>

// In JavaScript:

// Absolute URL:
const link = document.querySelector('.nav__link--btn');
console.log(link.href);

// Relelative URL (as written in the HTML):
const link = document.querySelector('.nav__link--btn');
console.log(link.getAttribute('href'));
```

#### Access to data attributes
```
// In the HTML:
<img
   src="img/logo.png"
  alt="Bankist logo"
  class="nav__logo"
  id="logo"
  designer="Jonas"
  data-version-number="3.0"
/>

// JavaScript:
const logo = document.querySelector('.nav__logo');
console.log(logo.dataset.versionNumber);

NOTE 1:	This data attributes start with "data" word in the HTML.

NOTE 2:	In HTML the data attributes are written using dashes.

NOTE 3:	In JavaScript are written using camel case.

NOTE 4:	The data attributes are always stored in the dataset object.

NOTE 5:	Data attributes are used to store data in the UI (in the HTML).
```

#### Common methods to work with classes
```
const logo = document.querySelector('.nav__logo');

logo.classList.add('fake-class');
logo.classList.remove('fake-class');
logo.classList.toggle('fake-class');
logo.classList.contains('fake-class');

NOTE: This are the common and recommended ways to work with classes.
```

#### Set a class to an element
```
const logo = document.querySelector('.nav__logo');
logo.className = 'fake-class';

NOTE: Don't use because it overrides all existing classed and only allows one class on one element.
```

#### Scroll to a specific section
```
const section1 = document.querySelector('#section--1');
const s1coords = section1.getBoundingClientRect();

// Option 1:
Scrolling
window.scrollTo(
  s1coords.left + window.pageXOffset,
  s1coords.top + window.pageYOffset
);

// Option 2:
window.scrollTo({
  left: s1coords.left + window.pageXOffset,
  top: s1coords.top + window.pageYOffset,
  behavior: 'smooth',
});

// Option 3 (The modern way):
section1.scrollIntoView({ behavior: 'smooth' });
```

#### Add an event to an element
```
// The old way:
const h1 = document.querySelector('h1');
h1.onmouseenter = function (e) {
  console.log('onmouseenter: Great! You are reading the heading :D');
};

// The new way:
const h1 = document.querySelector('h1');
const alertH1 = function (e) {
  console.log('addEventListener: Great! You are reading the heading :D');
};
h1.addEventListener('mouseenter', alertH1);

NOTE 1:	Using the event directly (old way) on an element can only add one event handler. If tries to add another, the preivious one is replaced.

NOTE 2:	Using the "addEventListener" method allows to assign multiple events handlers.

NOTE 3:	Using the "addEventListener" method allows to remove an event handler (it should be named, for that reason we create the  function and assign to the variable "alertH1" in order to be specifyed when removed).
```

#### Remove an event after 3 seconds
```
const h1 = document.querySelector('h1');
const alertH1 = function (e) {
  console.log('addEventListener: Great! You are reading the heading :D');
};
setTimeout(() => h1.removeEventListener('mouseenter', alertH1), 3000);
```

#### Stop the event propagation
```
document.querySelector('.some_element').addEventListener('click', function(e) {
  console.log('Clicked on the element');
  e.stopPropagation();
});
```

#### Capture an event in the capturing phase
```
document.querySelector('.some_element').addEventListener('click', function(e) {
  console.log('Clicked on the element');
}, true);


NOTE 1: The third parameter must be true;

NOTE 2: The event handler not longer listen for events in the bubbling phase, instead on the capturing phase.
```

#### Find the closest element that contains a specific class
```
const tabsContainer = document.querySelector('.operations__tab-container');

tabsContainer.addEventListener('click', function(e) {
  const clicked = e.target.closest('.operations__tab');
  console.log(clicked);
});
```

#### Specifying how to handle the scroll
```
window.addEventListener('scroll', function() {
	console.log(window.scrollY);
});

NOTE: The scroll info is in the "window" object and not in the "event".
```

#### Remove the last element of an array in place
```
const names = ['John', 'Jane', 'Doe'];
names.splice(0, 1);
console.log(names);
```

#### Remove the first element of an array
```
const fruits = ['Apple', 'Orange', 'Mango'];
fruits.shift();
console.log(fruits);
```
