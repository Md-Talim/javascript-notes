# Variables

Variables are container for pieces of data. That data can be one of many different data types. It's important to know and understand those data types and you'll learn them in the next lesson, but right now, you're going to learn about the syntax for creating and re-assigning variables as well as the differences between how we declare them.

## Declaring a Variable

In JavScript, we need to first declare a variable with one of three keywords

1. var
2. let
3. const

In modern JavaScript, you probably won't see `var` very much. `var` was the original declaration, but in `ES2015` also known as `ES6`, which was a huge update to the language, they introduced `let` and `const`.

One of the reasons for this is because of `block scoping`. Now, I'm not going to talk about things like scope right now. I just want to focus on how we declare and assign variables and also work with constants.

Just know that on the `global scope`, meaning not inside of a function or any kind of control structure, `var` and `let` work in a very similar way. `const` is a bit different.

So let's say that we want a variable called firstName and lastName. Remember that `string` data types need to be wrapped in either single or double quotes. You can also use backticks.

```javascript
let firstName = "John";
let lastName = "Doe";

// We can do a console.log to show the value
console.log(firstName, lastName);
```

We can store other data types such as numbers:

```javascript
let age = 30;
console.log(age);
```

## Variable Naming Conventions

So different languages have different rules and conventions when it comes to naming things. There are some rules that you have to follow when it comes to the formatting of your variable names.

- Only letters, numbers, underscores and dollar signs.
- Can not start with a number

I wouldn't suggest starting your variable names with a dollar sign or an underscore either.

### Multi-Word Variables

When it comes to variables as well as functions and classes with multiple words, it's really up to you on how you format the case.
What you'll see in JavaScript and what I do is camelCase. This where we start with a lowercase letter but every word after that starts with an uppercase letter.

```javascript
let firstName = "John";
```

You may also see underscores like this

```javascript
let first_name = "Sara";
```

There's also pascal case, where the first word is also capitalized. You typically see this for class names in object oriented programming.

```javascript
let FirstName = "Tom";
```

You might also see all lowercase, which I wouldn't recommend

```javascript
let firtstname = "Bob";
```

## Reassigning Values

Alright, so if we want to reassign a value we can do that here since we're using `var`. When it comes to directly reassigning a primitive type like a number, you can't use `const`.

Const stands for **constant**. So you have to use `var` or `let` if you want to re-assign a variable value. Again, you're not going to see `var` very much, so I will use `let` for this.

```javascript
let x = 100;
```

Let's reassign x to 200

```javascript
x = 200;
```

Now, in some cases, you may want to simply declare a variable and not assign a value to it.

```javascript
let score;
```

In this case, score would be equal to **undefined**, which is actually one of the seven primitive data types that we're gonna talk about in another lesson.

If you want to assign a value to it at any time, you can.

```javascript
score = 1;
```

One reason you might do this is because you have a conditional that says if score equals something, do this, if another, then do something else. Here is an example

```javascript
let score;

if (userScores) {
  score += 1;
} else {
  score -= 0;
}
```

## Constants

Let's look at `const`, which works a bit differently than `let` or `var`. So if you declare a name like this...

```javascript
const x = 100;
```

and then you try and re-assign that value

```javascript
x = 200; // throws an error
```

**Note:** You will get an error. You can't directly re-assign a value to a constant. You also can't initialize a constant as undefined.

```javascript
const score1; // throws an error
```

That will also throw an error. It has to be declared with a value.

Now where this can be a little confusing is when we use `const` with values that are not primitive like objects or reference types such as `arrays` and `object literals`. In that case you can't directly re-assign, but you can change them.

So let's say that you have an array

```javascript
const arr = [1, 2, 3, 4];
```

What you can't do is re-assign

```javascript
arr = [1, 2, 3, 4, 5]; // throws an error
```

But you can add to that array with the push method. You can even take a specific index of the array and change the value that way.

```javascript
arr.push(5); // [1, 2, 3, 4, 5];
arr[0] = 200; // [200, 2, 3, 4, 5];
```

## Declaring multiple values at once

You don't have to declare variables line by line, you can declare multiple values at once. With `let`, you can initialize, with `const`, you have to assign a value.

```javascript
let a, b, c;
const d = 10,
  e = 20,
  f = 30;
```

## Let or Const - Which to Use?

So how do we figure out which to use when it comes to `let` and `const` or even `var`? Well it comes down to preference.

What I do is always use `const` unless it's a primitive value that I think I may need to re-assign at some point. The score example above is a good example. That score number will be re-assigned throughout the game.

So I would use `let`. You'll find in most cases that you don't need to explicitly re-assign values. We're usually dealing objects where we manipulate them but don't re-assign them.

Some people do the opposite and always use `let` no matter what. Which is fine, but I think using `const` is a bit more robust because you know your values can't be re-assigned.

So, I would suggest `const` unless you know you need to either initialize as `undefined` or re-assign. It's all preference though.
