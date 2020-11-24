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
