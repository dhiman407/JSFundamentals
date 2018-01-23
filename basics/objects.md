# Objects
JavaScript is designed on a simple object-based model. An Object is a collection of properties. Property can be key-value pair or can be function, in which case the property is known as a method.

```js
var myCar =  new Object();
myCar.make = 'Toyota';
myCar.model = "Camry";
myCar.color = "White";
// or
var myCar = {
  make : "Toyota",
  model:"Camry",
  color:"White",
  year:2010
}
```

# Iterating through objects

```js
var myCar = {
  make : "Toyota",
  model:"Camry",
  color:"White",
  year:2010
}

for(var prop in myCar){
  console.log(" Object Property or Key: "+prop+" Property Value: "+ myCar[prop]);
}
```
