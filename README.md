# Iterators Lab

### Description

In the iterators lab we will be continuing our exploration of
iterators. We have a series of challenges that require you to use the
iterators we discussed in class. We will try to use various testing
methods to verify that your code is working.

### Phase-1

Research the following term and summarize your findings on it two to
three sentences:

* `higher-order function`


Update this README with a description of each of the following and an
example you've created:

* `forEach`: [note](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach)

Definition: Replacement for the standard for loop. Take the body from the for loop, wrap it in a function, and pass the argument to forEach.

Example:

var genre = ["rock", "pop", "oldies", "blues", "classical", "terrible"];
genre.forEach(function (word) {
	console.log("I like " + word + " music!");
});


* `map`: [note](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map)

Definition: Looping through elements of an array to build a new array in the process, returning a new array:

Example:
var genre = ["ROCK", "POP", "OLDIES", "BLUES", "CLASSICAL", "TERRIBLE"];

var lowerCased = genre.map(function (music) {
	return music.toLowerCase();
});
	console.log(lowerCased);


* `filter`: [note](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter)

Definition: Creates a new array with all elements that pass the test implemented by provided function.

var genre = ["rock", "pop", "oldies", "blues", "classical", "terrible"];

var fourWords = function (music) {
	return music.length === 4;
}

var bigWords = function (music) {
	return music.length > 4;
}

var smallWords = genre.filter(fourWords);
var largeWords = genre.filter(bigWords);

console.log(smallWords);
console.log(largeWords);

* `reduce`: [note](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce)

Definition: Iterates over the array and converts into one accumulated value.

Example:

var coolNumbers = [45, 6, 130, 45, 1];

var multiply = function (a, b) {
	return a*b;
}; 

var times = coolNumbers.reduce(multiply);


* `some`: [note](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/some)

Definition: Run through an array and return the result of true if any element meets one condition.

Example:

var byThree = function (num) {
	return num % 3 === 0;
};

[27, 16, 15].some(byThree);
=> true


* `every`: [note](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/every)

Definition: Returns true is ALL elements in array meet the condition.

Example:

var byThree = function (num) {
	return num % 3 === 0;
};

[27, 16, 15].every(byThree);

=> false

Use the notes provided to help guide you explanation.

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
```




