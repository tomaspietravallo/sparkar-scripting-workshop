# Pre study

Hi! In this section you'll find some material you'll need to be familiar with for the workshop

One thing you need to keep in mind, is that Javascript is a language that was originally developed for the web, as such, there are many resources that will intertwine Javascript content with web one.

I ask you to relax, and not be shied away by unintuitive or weird sounding words, you can always ask questions if you get stuck... speaking of which:

## Ask questions!

Please don't feel afraid to ask questions, the point of all this is to learn.

While reading, please try to read things carefully, but if you cannot make sense of some piece of material on your own, please do ask. Ideally, do so in the group, so that anybody who might've been stuck in the same place can also try and help you and/or learn from the answer too.

> If you are a little bit more experienced with Javascript, remember that not every one in the group is, please avoid highly technical language unless required

## Some basics

Here, I'll cover some basic concepts, so that you can go on to reading external resources more confidently

### Comments

```js
// this is a comment
// any line beginning with two slashes (//) is a comment
// comments are just that
// they do not get executed, they are just there as regular old text
```

### Variables

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

```js
// you can use the `const` keyword to declare variables that have a constant value
const aConstantValueVariable = 1.0;

// trying to reassign them throws an error (because it's not allowed)
// both of the following lines are examples of code that would fail
aConstantValueVariable = 2.0; // (tries to reassign) fails
aConstantValueVariable += 1; // (tries to add one) fails
```

### Data types

One of the most important part of learning any language, is getting familiar with its data types

Data types are just the different ways a language uses to encapsulate data

The following explanations are pretty shallow, but hopefully they can help you understand other resources

Let's start with an easy one

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

#### Strings

Strings are sequences of characters.

You can create them by wrapping your text in ` ' `, ` " `, or ` ` `

```js
let aCoolString = "the text thats part of a string does not get executed as code";
```

```js
aCoolString = aCoolString + " you can also add strings together, which does exactly what youd expect";
```

#### Objects

Objects is one of the most important data types. You'll work with Objects all the time

Objects are collections of *properties*, in other words, you store other data types together

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

## External resources

> Remember that Javascript and it's internal workings are comprised by Standards (notably the ECMA standard), so external resources might reference ECMA or IEEE standards, don't be afraid if you don't understand the language around these standards, they are pretty advanced/ not meant for beginners!

Even though these are external, please, do ask questions you might have while reading them!

- [(Youtube) Learn Javascript in 12 minutes](https://youtu.be/Ukg_U3CnJWI). This video is intended for Web developers, but it's really good and concise :). The only points that are not applicable to Spark:

    - Everything that's wrapped in `<angle brackets>` is HTML (don't focus on that)
    - `alert()` and `document.write()` are web-specific, don't think about them too much. The Spark AR version of these is `Diagnostics.log()`, which prints out a value so you can inspect it

- [LearnXInYMinutes: Javascript](https://learnxinyminutes.com/docs/javascript/)

- [MDN: A re-introduction to Javascript](https://developer.mozilla.org/en-US/docs/Web/JavaScript/A_re-introduction_to_JavaScript)