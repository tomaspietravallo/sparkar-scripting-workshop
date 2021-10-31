# Pre study

Hi! In this section you'll find some material you'll need to be familiar with for the workshop

One thing you need to keep in mind, is that Javascript is a language that was originally developed for the web, as such, there are many resources that will intertwine Javascript content with web one.

I ask you to relax, and stand strong in the face of unintuitive or weird sounding words, you can always ask questions if you get stuck... speaking of which:

## Ask questions!

Please don't feel afraid to ask questions, the entire point of this is teaching.

While reading, please try to read things carefully, but if you cannot make sense of some piece of material on your own, please do ask for help. Ideally, do so in the group, so that anybody who might've been stuck in the same place can also try and help you and/or learn from the answer too.

> If you are a little bit more experienced with Javascript, remember that not every one in the group is, please avoid highly technical language unless required

## Some basics

Here, I'll cover some basic concepts, so that you can go on to reading external resources more confidently

---

### History

Javascript is a programming language that was originally developed for the web in 1995, and it has evolved over time to better suit the needs of programmers.

You can think of programming languages like Javascript, as a sort of cooking recipe. In this case, the different instructions in the recipe are your code, and the final result will be the output or behaviors you code for. Unfortunately, the internet has not yet found a way to make code tasty.

---

### Comments

```js
// this is a comment
// any line beginning with two slashes (//) is a comment
// comments are just that
// they do not get executed as instructions, they are just there as regular old text
```

Because they are not executed, they are often used to explain what different parts of a script do. This helps others (as well as future you 😉) understand what you intend to achieve with certain bits code

Comments are also frequently used to comment-out parts of a script, to test what effect adding/removing said parts has

---

### Variables

In Javascript, all data can either be *Fixed*, or *Variable*

Fixed data is data you type out every time you need to use it, while Variable data is assigned to a variable, which can then be used to reference the data

<details>
<summary>An example of how that helps simplify your code (click to open)</summary>

```js
const maxScore = 10 * 5;

// use the value to do things in other parts of the code
// these are functions 👇, you'll learn about them later
createSceneObject(10);
printOutValue(10);
```

If instead you used variables, you would make your code easier to read, as well as making it easier to change in the future!

```js
// create a variable of constant value (the number 10)
const amount = 10;
// create a second variable, based off the value of `amount`
const maxScore = amount * 5;

// use the value to do things in other parts of the code
// these are functions 👇 you'll learn about them later
createSceneObject(amount);
printOutValue(amount);
```

> The ability to easily change code is important! As it lets you test out different values or ideas without having to change multiple values all around your script. [After doing the pre-study, you can see a fun video by Tom Scott explain this concept a little bit better](https://youtu.be/QPZ0pIK_wsc)

---

</details>

#### let
```js
// this is a variable
// think of variables as buckets of memory that store things
let myVariableName = "a string of characters";

// you declare variables with the `let` keyword
// and once you've declared them, you can re-assign their value
myVariableName = "a different string of characters";

// note that when re-assigning, you do not use the `let` keyword again
// the keyword is only used when declaring a variable for the first time
```
#### const
```js
// you can use the `const` keyword to declare variables that have a constant value
const aConstantValueVariable = 1.0;

// trying to reassign them throws an error (because it's not allowed)
// both of the following lines are examples of code that would fail
aConstantValueVariable = 2.0; // (tries to reassign) fails
aConstantValueVariable = aConstantValueVariable + 1; // (tries to add one and reassign) fails
```

#### var

`var` is another keyword that you can use to declare variables, it works in a similar way to `let`, *but not exactly*. For the purpose of keeping it simple, **the use of** `var` **is discouraged**

```js
var aVariable = "a string";
aVariable = "you can reassign, just like when using let";
```

---

### Data types

One of the most important part of learning any language, is getting familiar with its data types

Data types are just the different ways a language uses to encapsulate data. This same concept exists in the Spark AR Studio Patch editor (to see it, create an option picker, and then check out the different data types that you can select)

The following explanations are pretty shallow, but hopefully they can help you understand other resources

Let's start with an easy one

---

#### Number

The number data type is just that, a number

```js
// this variable holds a number
let myCoolNum = 10;

// numbers can be used to do math
myCoolNum = myCoolNum + 10; // adds ten
myCoolNum = myCoolNum / 2; // divides by 2
```

Note that you might see Numbers referred to as Integers and/or Floats, Javascript does not distinguish between the two. All numbers are Floats (meaning they can, and do, have decimal places)

```js
let anotherNum = 3;
anotherNum = anotherNum / 2; // divides 3 by 2, resulting in 1.5
```

---

#### Strings

Strings are sequences of characters.

You can create them by wrapping your text in ` ' `, ` " `, or ` ` `

```js
let aCoolString = "the text thats part of a string does not get executed as code";
```

```js
aCoolString = aCoolString + " you can also add strings together, which does exactly what youd expect";
```

---

#### Arrays

Arrays are Objects which hold a *list* of values.

The values stored in an array may be of different data types

The different values inside an array can be accessed via their **index** in the list

> Computers count from 0! So the 0th item is the first one in the list

```js
let anArrayOfNumbers = [10,20,30];

anArrayOfNumbers[0]; // 10
anArrayOfNumbers[1]; // 20
anArrayOfNumbers[2]; // 30

anArrayOfNumbers[3]; // undefined, the list doesn't have a 4th item
```

---

#### Objects

Objects is one of the most important data types. You'll work with Objects all the time

Objects are collections of *properties*, in other words, you store other values together.

> The values stored may be of completely different data types

Unlike arrays, Objects do not have an order, you need to use the specific keys to retrieve a value

```js
// To create an object, we use curly braces, and place a "key" followed by it's value
// to add multiple key-value pairs, separate them using commas
let myObj = { "thisIsAProperty": 100, "anotherProp": "a string" };

// You can add line breaks to make your code easier to read
let prettierObj = {
    "aNumberProp": 100,
    "aStringProp": "a string"
    "a long key with spaces in it": "Mhhh"
};

// To get a value inside an Object, you can use square brackets followed by the key (as a string)
prettierObj["aNumberProp"]
// or by using a dot
prettierObj.aNumberProp

// note that the dot notation won't work if your key has spaces or non-standard characters

prettierObj["a long key with spaces in it"] // works
prettierObj.a long key with spaces in it // fails
```

> If you read the definition of Array, you might've noticed it says Arrays are Objects, and that's because most things in Javascript (sometimes even other data types), are Objects. Arrays, aside from having their number indexed properties/values, also have different properties indexed by string; for example: `[1,2,0].sort()` (returns the sorted array `[0,1,2]`)

---

## External resources

> **Remember**: that Javascript and it's internal workings are comprised by Standards (notably the ECMA standard), so external resources might reference ECMA or IEEE standards, don't be afraid if you don't understand the language around these standards, they are pretty advanced/ not meant for beginners!

> **Pro tip**: On top of trying to strengthen your knowledge of different data types, while studying, try to keep an eye out for different reasons why using *Variables* and *Iterators* can help simplify your code, and make it easier to read and modify. See an example of this under the definition of [Variables](#variables). You'll learn about *Iterators* with the help of the resources listed below.<br><br>[See a fun video by Tom Scott explain this idea better]((https://youtu.be/QPZ0pIK_wsc))

Even though these are external, please, do ask questions you might have while reading them!

- [(Youtube) Learn Javascript in 12 minutes](https://youtu.be/Ukg_U3CnJWI). This video is intended for Web developers, but it's really good and concise :).<details><summary> The only differences / points that are not applicable to Spark (click to open)</summary>

    - Everything that's wrapped in `<angle brackets>` is HTML (don't focus on that)
        ```html
        <html>
            <head>
            </head>
            <body>
                <script>
                    // some actual javascript code here
                    let myCode = "some javascript code here";
                </script>
            <body>
        </html>
        ```
        Simply becomes
        ```js
        // some actual javascript code here
        let myCode = "some javascript code here";
        ```


    - `alert()`, `document.write()`, `console.log()` are web-specific, don't think about them too much. In this case, the Spark AR version of these is `Diagnostics.log()`, which prints out a value so you can inspect it
</details>

- [LearnXInYMinutes: Javascript](https://learnxinyminutes.com/docs/javascript/)

- [MDN: A re-introduction to Javascript](https://developer.mozilla.org/en-US/docs/Web/JavaScript/A_re-introduction_to_JavaScript)