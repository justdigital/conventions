# Coding Standards

## Text editor configurations:
Indentation: 2 spaces
Encoding: utf-8

## Commenting
Single item commenting:
```Javascript
var name = ""; // this is the user name
var age = 0;  // this is the user age
```
Block commenting:
```Javascript
/*
 * this will do that thing when foo is exactly equals bar.
 */
if (foo === bar) {
  doIt();
}
```
Do not rely only on comments. Use good variable names:
```Javascript
var myVar = "foo"; // This is the user name (bad)
var userName = "foo"; // This is the user name (good)
```

## Variables
Always declare variables at the beginning of the scope they are used:
```Javascript
function fooAndBar () {
  var foo = "";
  var bar = 0;

  doThat(foo, bar);
}
```
Use plural for arrays:
```Javascript
var fruit = 'apple'; // a single string for fruit
var fruits = ['tomato', 'apple', 'banana']; // an array of fruits for fruits
```

## Conditions
Use spaces before opening parenthesis and after closing them:
```javascript
/*
 * Good:
 */
if (true) {
  foo();
} else {
  bar();
}

/*
 * Bad
 */
if(true){
  foo();
} else{
  bar();
}
```

## Functions
Use camelCase for function names:
```Javascript
/*
 * good stuff:
 * pascal case for names
 */
function myTestFunction(x, y) {

}

/*
 * bad stuff
 * underlines, capital for first letter
 */
function My_test_function(foo,bar){

}
```

Anonymous functions declaration:
```Javascript
/*
 * Self executing
 */
(function($){
    // Do some stuff
})(jQuery);

/*
 * Callback
 */
array.forEach(function (v, k) {
    // Do some stuff
});
```

## Never declare number, string, or boolean objects
Always start variable with default values instead:
```Javascript
/*
 * good stuff:
 */
var name = '';
var age = 0;
var checked = true;
var fruits = [];
var properties = {};
var cb = function () {};

/*
 * bad stuff
 */
var name = new String();
var age = new Number();
var checked = new Boolean();
var fruits = new Array();
var properties = new Object();
var cb = new Function(args);
```

## Declarations on top
Always declare your variables at the top.
```Javascript
var foo = 0;
function someFunction(arg) {
    foo = arg;
}
```

## Spaces after reserved words
Always declare your variables at the top.
```Javascript
if (condtion) {
    // Do somenthing
} else {
    // Do another stuff
}

function () {
}

for () {
}

while () {
}

switch () {
    case 1:
        console.log('Hello!');
        break;
    default:
        // Do somenthing
}
```

## No comma after last Object property or Array item
Make sure to not let comma after the last item
```Javascript
/*
 * Good stuff
 */
var fruits = {
    'apple',
    'orange'
}
/*
 * Bad stuff
 */
var fruits = {
    'apple',
    'orange',
}
```