# Scope

Scope is the accessibility of variables, functions and objects in particular part of your code at runtime.

## Scope in JavaScript
 * Global Scope
 * Local Scope
 * Block Level Scope // ES6

```js
var name = "First Last"; // Global Scope
//Function in global scope
function someFunction(){
  var age = 30; // Local Scope #1
  //function in local scope
  function innerFunction(){
    //Local Scope#2
  }
  console.log("age : " + age + ", Name :" +name);
}
console.log(age); // Output : undefined
console.log(someFunction()); // Output : Age : 30, Name : First Last
console.log(innerFunction()); // Output : undefined
```
## Block scope
Variable defined inside of a block statement (if, switch, for, while) will remain in the scope. ES6 came up with "let" statement to declare a block scope variable.

```js
if(somecondition){
  let x=2;
  console.log(x); // Output : 2
}
console.log(x); // Output : undefined
```
"let" statement makes the code cleaner when inner functions as used.
```js
for(let i=0;i<5;i++){
  setTimeout(function(){
    console.log(i);
  },1000);
}
// Print Accurate result

// to achieve the same effect with 'var', you have to create a different context using a closure to preserve the values
 for(var i=0;i<5;i++){
   (function(i){
     setTimeout(function(){
       console.log(i);
     },1000);
   })(i);
 }
```
