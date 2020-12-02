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
