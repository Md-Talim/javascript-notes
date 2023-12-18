# Console Methods in JavaScript 

The `global object` in the browser environment gives us access to the `console` object that has a bunch of useful methods that we can use from our JavaScript file to interact with the JavaScript console. 

> **Note:** Method is a function that is attached to an object. In the above case, the 'console' object.


## **`console.log()`**

- This is the most common console method. 

- We pass whatever we want to log to the console as an argument to the `log()` method.

- The argument can be a string, a number, a boolean, an object, an array, or even a function.

### **Log a number**

Different data types will have different colors in the console.

```javascript
console.log(123);
```

### **Log a string**

```javascript
console.log('Hello Amplenote!');
```

### **Log multiple values**

```javascript
console.log(123, 'Hello', true);
```

### **Log a variable**

For the most part, we use the console to debug and log out variables or the result of a function or network request.

```javascript
const firstName = "Talim";
console.log(firstName);
```


## **`console.error()`**

- Outputs an error message.

- It will make the text red.


  ```javascript
  console.error('This is an error!');
  ```


## **`console.warn()`**

- Outputs a warning message.

- It will make the text yellow.


  ```javascript
  console.warn('This is a warning!');
  ```

## **`console.clear()`**

- Clear the console.


  ```javascript
  console.clear();
  ```


## **`console.table()`**

- Displays tabular data as a table.

- You can format an object as a table if you want to log an object.

> **Note:** This method takes on mandatory argument `data`, which must be an array or an object, and one additional parameter `columns`.

Example

```javascript
console.table(\["apples", "oranges", "bananas"\]); 
```

| | |
|-|-|
|(index)|Values|
|0|'apples'|
|1|'oranges'|
|2|'bananas'|


## **`console.group()`**

- Creates a new inline group in the console.

- It takes an *additional parameter called a **`label`.***

- Call `groupEnd()` method to end the group log.


  ```javascript
  console.group('simple');
  console.warn('warning!');
  console.error('error here');
  console.log('Hello World');
  console.groupEnd('simple');
  console.log('new section'); 
  ```


## **Log with styles**

- Use the `%c` directive to apply a CSS style to the console output.


  ```javascript
  console.log(
    "This is %cMy stylish message",
    "color: yellow; font-style: italic; background-color: blue;padding: 2px",
  );
  ```

The text before the directive will not be affected, but the text after the directive will be styled using the CSS declarations in the parameter.

![](https://developer.mozilla.org/en-US/docs/Web/API/console/css-styling.png)
