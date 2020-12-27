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
