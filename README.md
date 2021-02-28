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
