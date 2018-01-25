# Hoisting

Hoisting is a JavaScript mechanism where variables and function declarations are moved to the top of their scope before code execution.

JavaScript builds its execution environment in two passes:

* The declaration pass sets up the runtime environment, where it scans for all variable and function declarations and creates the identifiers.

* The second pass is the execution pass.

Try following code:
 ```js
 var myVar = "Test";

 (function (){
  console.log(myVar);
  var myVar = "Test";
 })();
 // Output : undefined
 ```
 This is because Inner scope of myVar has been declared but still undefined when console.log() executes

 This is how JavaScript interprets the code
```js
var myVar = "Test";

(function (){
  var myVar;
  console.log(myVar);
  myVar = "Test";
})();
 ```

 This is why its good practice to declare and define the variables as first statement in the function scope.
 
