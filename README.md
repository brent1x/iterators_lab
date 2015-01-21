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

>> A higher-order function is essentially a function of a function. It takes one (or more) functions as an input. Then it outputs a function.


Update this README with a description of each of the following and an
example you've created:

* `forEach`: [note](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach)

  ~ forEach function loops through each item in an array

  var lol = ["lmao", "rofl"];

  lol.forEach(function (ok) {
    console.log("sup " + ok);
  });

* `map`: [note](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map)

  ~ map function loops over array and then builds a new array (using return)

  var lol = ["lmao", "rofl"];

  lol.upperCased = lol.map(function (ok) {
    return ok.toUpperCase();
  });

* `filter`: [note](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter)

  ~ filter function loops over an array and then filters it down to a subset of that array

  var lol = ["lmao", "rofl", "lmfao"];

  var isFive = function (ok) {
    return ok.length === 5;
  };

  var isFour = function (ok) {
    return ok.length === 4;
  };

  var fourLettersLong = lol.filter(isFour);
  var fiveLettersLong = lol.filter(isFive);
  
  console.log(fourLettersLong);
  console.log(fiveLettersLong);

* `reduce`: [note](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce)

  ~ reduce function iterates over an array and converts it into one accumulated value

  var numbers = [4, 5, 6];
  var add = function (a, b) {
    return a + b;
  };

  var sum = numbers.reduce(add);
  console.log(sum);

* `some`: [note](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/some)

  ~ some function iterates over an array and returns TRUE if at least 1 element meets the condition

  var numbers = [4, 5, 6];

  var isOdd = function (num) {
    return num % 2 === 1;
  };

  numbers.some(isOdd);

* `every`: [note](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/every)

  ~ every function iterates over an array and returns TRUE if all elements meet the condition

  var numbers = [4, 5, 6];

  var isOdd = function (num) {
    return num % 2 === 1;
  };

  numbers.some(isOdd);

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

  var myNumbers = [ -1, 2, -3, 4, -5, 6];

  var absNumbers = myNumbers.map(function (num) {
    return Math.sqrt(num * num);
  });

  console.log(absNumbers);




