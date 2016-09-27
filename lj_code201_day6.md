#LJ Code 201 - Day 6

“Tomorrow is gonna be loooong” - Sam

## Abstraction
001011010110010  
Machine Language  
OS  
Physical System (mouse/keyboard)  
Browser  
HTML/CSS/JavaScript
Server-Side Languages
Cat Pictures

—> Layers of Abstraction  
Interface  

## Domain Modeling
programming is easy if you understand the problem domain  
take a big problem, and break it into smaller pieces, solve smaller pieces, voila -> solved for big problem  
aka divide and conquer  
if you don’t know what to do next, you haven’t worked hard enough to understand your domain and break it into workable smaller problems.  
keep checking in code. small chunks. easier to debug.   
smaller solutions can be reusable.  

TDD = Test-Driven Development

### Sobol - article on domain modeling
small methods that focus on doing one job well

### Sonmez on Domain Modeling
make sure how you construct your js objects make sense to outside world. (hotel: availability, price, roomTypes). makes sense to outside world.  

## JS Chapter 5, Document Object Model (DOM)

Every html page is an object, built like a tree  
API (Application Programming Interface). Working with a DOM is working with an API.  

Tree layout within the object:

Body  
  Div
    H1
    H2
      UL
        LI

each element is a node.  

.appendChild() 

<li id=“one” class=“hot”><em>fresh</em></em> figs</li>  
<li id=“two” class=“hot”>pine nuts</li>  
use IDs to access these elements.  

<script> tag should be the very last item of your <body>  

http://codepen.io/  

Code Example of changing the DOM:  
  
### HTML
<h1>Sam's Pets</h1>  
<ul id="beasts"></ul>  
  
### CSS
* {  
  outline: 2px dotted orange;  
}  
  
ul {  
  outline: 2px dashed green;  
  padding: 10px;  
}  
  
### JS
// make var same name as HTML ID. good practice.  
// Put your getElement at top of js. good practice.  
var beasts = document.getElementById('beasts’);  
  
var pets = ['Parkey', 'Demi', 'Buddy', 'Alistair', 'Trillian’];  
  
for (var i = 0; i < pets.length; i++) {  
  // create an element. same name is good practice.  
  // li -> making LIs, EL -> elements  
  var liEl = document.createElement('li’);  
  // give an element content  
  liEl.textContent = pets[i];  
  console.log(liEl);  
  // append the element to the DOM  
  beasts.appendChild(liEl);  
}  

## Objects Demo
object {  
  0: “a”,  
  1: “b”,  
  2: “c”,  
  3: “d”	<— no comma in last element of object  
}

object {};  
object.Frazier = ‘Fraz’;  

### Object literal notation:  
var genericObject = {  
  key1: ‘value1’,  
  key2: ‘value2’,  
  multi-word key’: ‘value’,  
  method: function() {  
    // do stuff  
  }  
};  

#### Object Literal Code Example  
var sam = {  
  // properties  
  firstName: 'Sam’,  
  middleName: null,  
  lastName: 'Hamm’,  
  rating: 0,  
  isABoss: true,  
  underlings: ['Rachel', 'Frazier', 'Aliza', 'Maelle’],  
  
  methods  
  getRating: function() {  
    return this.rating;  
  },  
  setRating: function(num) {  
    return this.rating = num;  
  }  
 };  
  
// adding new properties and methods to object.  
sam.employer = {  
  name: 'Code Fellows’,  
  location: ‘Seattle'  
};  
  
sam.logName = function() {  
  console.log(this.firstName + ' ' + this.lastName);  
};  
  
sam.whatIsThis = function() {  
  console.log(this);  
};  
  
 sam.whatIsThis(); // logs the sam object  

Put properties at top in an object, put methods at the bottom of the object  

### Lab Setup
make a new repository called cookie-stand (on GH, with readme, MIT license)  and clone
make branch (name branch by date)  
// every time you add something that works, do a add/commit, then after a few push, merge, then git pull origin master
   
The minimum number of customers per hour.  
The maximum number of customers per hour.  
The average number of cookies purchased per customer.  

create sales.html (index will be public-facing page)  
build object literals that stores the min/max hourly customers, and the average cookies per customer, in object properties.  
Uses a method of that object to generate a random number of customers per hour. Objects/Math/random  
Calculate and store the simulated amounts of cookies purchased for each hour at each location using average cookies purchased and the random number of customers generated  
Store the results for each location in a separate array... perhaps as a property of the object representing that location
Display the values of each array as unordered lists in the browser


5 locations (5 object literals), but build one, and copy to make other 4  
properties for min, max, and avg  (minimum/maximum custPerHour, and average cookies per customer).
var hours = [‘6am’, ‘7am’,…’8pm]; - sits outside the 
property for randCustPerHour [32, 19, 72], and a method to calculate those random customers per hour
property to store & method to generate total cookies sold per hour [77, 34,] <— this goes into the list
calc/store/display total daily sales per location
property that holds name of the location “Fist and Pike”

<ul id=“firstandpike”></ul>
<ul id="seatac”></ul>
<ul id=“seattlecenter”></ul>
<ul id=“caphill”></ul>
<ul id=“alki”></ul>

var hours = [‘6am’, ‘7am’, ‘8am’, ‘9am’, ‘10am’, ‘11am’, ‘12pm’, ‘1pm’, ‘2pm’, ‘3pm’, ‘4pm’, ‘5pm’, ‘6pm’, ‘7pm’, ‘8pm’]; 

Each object should have a .render() method that displays the list of store data

var firstandpike = {
  name: 


calcRandCustByHour: function() {
var function getRandomIntInclusive(min, max) {
  min = Math.ceil(min);
  max = Math.floor(max);
  return Math.floor(Math.random() * (max - min + 1)) + min;
}