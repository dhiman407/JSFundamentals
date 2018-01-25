# Closure

A Closure is the combination of a function and the lexical environment within which that function was declared.

```js
function outerFunction(){
  var name = "Test"; // local variable created by outerFunction
  function innerFunction(){ // innerFunction is the inner function, a closure
    console.log(name); // use variable declared in the parent function
  }
}
```
Closure lets the function continue to access the lexical scope it was defined in at author-time.

# Modules Pattern
Code pattern which leverage the power of closure is Module Pattern. JavaScript does not provide a native way of declaring private methods.

The following code describe how to use closures to define public methods which can access private functions and variables.
```js
var makeCounter = function(){
  var privateCounter = 0;
  function changeBy(val){
    privateCounter += val;
  }
  return {
    increment : function(){
      changeBy(1);
    },
    decrement : function(){
      changeBy(-1);
    },
    value : function(){
      return privateCounter;
    }
  }
};
var counter  = makeCounter();
console.log(counter.value());// Output : 0
counter.increment();
counter.increment();
console.log(counter.value());// Output : 2
counter.decrement();
console.log(counter.value());// Output : 1
```
