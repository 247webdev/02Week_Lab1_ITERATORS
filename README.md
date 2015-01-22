Christain Chandler WDI-SF-16
Week 2 Lab 1
# Iterators Lab

### Phase-1

* `higher-order function`
	Is a function that takes at least one function as an input then outputs a function.


* `forEach`: [note](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach)
forEach takes an array and individually applies the given function to each array index, in turn.
var myArray = [1, 1, 2, 3, 5, 8];
var combined="";
myArray.forEach(function (currentValue) {
    combined += currentValue.toString() + " ";
});
// combined now contains  "1 1 2 3 5 8"


* `map`: [note](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map)
map is simular to forEach but map creates a new array by using the passed in array's individual cells in turn.
var myArray = [1, 1, 2, 3, 5, 8];
var combined= myArray.forEach(function (currentValue) {
    return currentValue.toString() + " ";
});
// combined is now a new array that contains  ["1 ","1 ", "2 ", "3 ", "5 ","8"]


* `filter`: [note](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter)
.filter takes an array and creates a new array from the values of the passed in array as long as a give element passes the given expression, in turn.
var myArray = [1, 1, 2, 3, 5, 8];
var combined = myArray.filter(function (currentValue) {
    combined += currentValue.toString() + " ";
});
// combined now contains the array [2, 8]


* `reduce`: [note](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce)



* `some`: [note](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/some)
.some takes an array and returns true if any of the array elements matches some given value. Once one true is found, .some doesn't need to continue.
var names = ["bob", "joe", "Tim"];
var isInstructor = function () {
	person = person.toLowerCase();
	return person == "tim" || person == "alex" || person == "elie"; 
};
var x = names.some(isInstructor);
// x now contains true

* `every`: [note](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/every)
.every takes an array and returns true if all of the array elements matche the given value.
var names = ["bob", "joe", "Tim"];
var isInstructor = function () {
	person = person.toLowerCase();
	return person == "tim" || person == "alex" || person == "elie"; 
};
var x = names.some(isInstructor);
// x now contains false

### Phase-2

* Run `npm install` from the `iterators_lab` directory.
* Looks at the tests we've written in the `test` folder. Run the tests
  with `npm test` (also from the `iterators_lab` directory). They
  should all fail.
* Get all of the tests to pass by writing the necessary code in
  `src/iterators.js`.

### Phase-3

Refactor the following code using `map` to make only one call to the `map` function versus the two below.


```
var myNumbers = [ -1, 2, -3, 4, -5, 6];

var square = function(num) {
	return num * num;
};

var sqrRoot = function(num) {
	return Math.sqrt(num);
};


var sqrNumbers = map(myNumbers, square);
var absNumbers = map(sqrNumbers, sqrRoot);

--------------------




