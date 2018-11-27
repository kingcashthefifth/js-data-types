# Javascript Data Types Exercises

> This worksheet will double as Javascript notes for future reference! Copy it into your preferred note-taking program at the end of class.

## Data Types

For each expression, predict what you think the output will be in a comment (`//`) ***without first running the command***. Then run the expression in the console. Note the actual output in a comment and compare it with your prediction.

#### Example

```js
typeof("potato")
// Prediction: Vegetable
// Actual: String
```

What is the output of each of the expressions below?

```js
typeof(15)
// Prediction: int
// Actual: "number"

typeof(5.5)
// Prediction: int
// Actual: "number"

typeof(NaN)
// Prediction: NaN
// Actual: "number"

typeof("hello")
// Prediction: string
// Actual: "string"

typeof(true)
// Prediction: boolean
// Actual: Boolean

typeof(1 != 2)
// Prediction: boolean
// Actual: Boolean


"hamburger" + "s"
// Prediction: "hamburgers"
// Actual: "hamburgers"

"hamburgers" - "s"
// Prediction: "hamburger"
// Actual: NaN

"1" + "3"
// Prediction: "13"
// Actual: "13"

"1" - "3"
// Prediction: ""
// Actual: "-2"

"johnny" + 5
// Prediction: johnny5
// Actual: johnny5

"johnny" - 5
// Prediction: error
// Actual: NaN

99 * "luftbaloons"
// Prediction: error
// Actual: NaN
```

What's going on in the second half of the previous question? Are there any "rules" we can pull from those examples?

You usually get NaN when the result of a math operation is not real (e.g., dividing 0 by 0, multiplying strings together).

## Data Structures

> Data structures include arrays and objects. We will go over objects in a later class.

### Arrays

Javascript provides us with a number of native methods that allow us to interact with arrays. Find methods that do each of the following and provide an example...
* Add an element to the back of an array.
numbers.push()
* Remove an element from the back of an array.
numbers.pop()
* Add an element to the front of an array.
numbers.unshift()
* Remove an element from the front of an array.
numbers.shift()
* Concatenates all the elements in an array into a string.
numbers.join()
* Separates the characters of a string into an array. This one is a string method.
var a = numbers.split('')

> This is a great exercise for practicing your "Google Fu"! If you need a starting point, check out [MDN's documentation page on arrays](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array).

```js
// Your answers go here.
```

What will the contents of the below arrays be after the code samples are executed? Come up with an answer yourself before testing it out in the console.

```js
var numbers = [2, 4, 6, 8]
numbers.pop()
numbers.push(10)
numbers.unshift(3)

```

```text
numbers = [3, 2, 4, 6, 10]
```

What is the return value of the below code sample? Come up with an answer yourself before testing it out in the console.

```js
var morse = ["dot", "pause", "dot"]
var moreMorse = morse.join(" dash ")
moreMorse.split(" ")
```

```text
moreMorse = ["dot", "pause", "dot", "dash"]
```

What will the contents of the below array be after the below code sample is executed? Come up with an answer yourself before testing it out in the console.

```js
var bands = []
var beatles = ["Paul", "John", "George", "Pete"]
var stones = ["Brian", "Mick", "Keith", "Ronnie", "Charlie"]
bands.push(beatles)
bands.unshift(stones)
bands[bands.length - 1].pop()
bands[0].shift()
bands[1][3] = "Ringo"
```

```text
var bands = [["Mick", "Keith", "Ronnie", "Charlie"], ["Paul", "John", "George", "Ringo"]]
```
### Objects
```
var phoneBook = {
  "Abe": "111-111-1111",
  "Bob": "222-222-2222",
  "Cam": "333-333-3333",
  "Dan": "444-444-4444",
  "Ern": "555-555-5555",
  "Fry": "111-111-1111",
  "Gil": "222-222-2222",
  "Hal": "333-333-3333",
  "Ike": "444-444-4444",
  "Jim": "555-555-5555",
  "Kip": "111-111-1111",
  "Liv": "222-222-2222",
  "Mia": "333-333-3333",
  "Nik": "444-444-4444",
  "Oli": "555-555-5555",
  "Pam": "111-111-1111",
  "Qiq": "222-222-2222",
  "Rob": "333-333-3333",
  "Stu": "444-444-4444",
  "Tad": "555-555-5555",
  "Uwe": "111-111-1111",
  "Val": "222-222-2222",
  "Wil": "333-333-3333",
  "Xiu": "444-444-4444",
  "Yam": "555-555-5555",
  "Zed": "111-111-1111"
};
```

Write a line of code that accesses the phone number for Pam.
phoneBook.Pam;
Write a line of code that creates a new record for John at 435-567-1223.
phoneBook.John = "435-567-1223";
Write your own object and console.log that value.
var obj = {
	"Cash" : "12345678"
};

console.log(obj);
Find out what `Object.keys(phoneBook)` does.
It will list all the keys only in the object "phoneBook".
Look up and use the `delete` keyword with phoneBook to delete a record.
delete phoneBook.John;

## Booleans & Comparison Operators

#### Part 1: Operators
Paste the examples from the gitbook into the chrome dev console.

[https://wdi-sg.github.io/gitbook-2018/02-js/js-intro/js-control-flow/03booleans-and-conditionals.html](https://wdi-sg.github.io/gitbook-2018/02-js/js-intro/js-control-flow/03booleans-and-conditionals.html)

See what the output values are.

Change the operators for each example or change the values to see what happens.

#### Part 2: Conditional if else if else Statements

Create a new html file: touch conditionals.html

Create a new js file: touch conditionals.js

Link them together in your HTML file: <script src="conditionals.js"></script>

Paste the above conditional statement examples into your js file one at a time.

Use console.log to see what values you are getting.

Also try playing with the examples in the chrome console.

#### Part 3:

You're a bouncer at a bar. Given an `age` variable, create a conditional that satisfies the following requirements...
* If a patron is older than `21`, print out `"Come on in!"`.
* If a patron is between `18` and `21`, print out `"Come on in (but no drinking)!"`.
* If a patron is younger than 18, print out `"You're too young to be in here!"`.
* If a patron is older than 75, print out `"Are you sure you want to be here?"`.

```js
var age = 78;
if (age > 21 && age < 75) {
    console.log("Come on in!");
} else if (age >= 18 && age <= 21) {
    console.log("Come on in (but no drinking)");
} else if (age < 18) {
    console.log("You're too young to be in here!");
} else if (age > 75) {
    console.log("Are you sure you want to be here?");
};
```

#### Further: 

Bar patrons must have an ID if the bouncer is even going to consider what age they are.
- If the patron has an ID, the bouncer will then check if they are of the proper age
- If the patron does not have an ID, the bouncer will tell them `"No ID, no entry."`

> Hint: Whether the patron has an ID or not can be stored in a `hasId` variable. What do you think the stored data type should be?


#### Further 2:

Starting at the bottom of your js file, create a variable speed. write the contitional for a traffic stop. If speed is less than 10 console.log "I pulled you over because you were going too slow". If speed is more than 50 console.log "I pulled you over for going to fast".

Create a variable tirePressure. If tire pressure is less than 10 PSI console.log "I pulled you over because you are driving with a flat tire".

Create a variable driverVision. Assign an array value: [6,6]. If driverVision is less than 6/12, console.log "Sorry you can't drive".

Now, write some more complicated conditional logic:

If driverVision is over 6/6 set the speed variable to 60.

If speed is over 50 and tirePressure is under 10 or over 100 console.log "car crash".

If speed was under 10 and tirePressure was over 100 console.log "rolling to a stop".

If driverVision is over 6/12 and speed is over 50 console.log "car crash".

If the car will crash, don't output the traffic stop text.
