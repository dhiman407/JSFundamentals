# Arrays

JavaScript arrays are used to store multiple values in a single variable. In traditional programming languages array contains same type of data like array of integers, array of string. But in JavaScript, different type of data can be stored in the single array.

# Example
```js
var array_name = [item1,item2,item3];
var myCarArray = ["Volvo","Merc","BMW"];
//or
var myCarArray = new Array("Volvo","Merc","BMW");
```

#Accessing Array
This statement is used if you know the index of the item you want to Accessing
```js
var mycar = myArray[0];
```
#Iterating through the array
```js
var myCarArray = ["Volvo","Merc","BMW"];
//Using for Loop
for(let i=0;i<myCarArray.length;i++){
  console.log(myCarArray[i]);
}
//Using forEach and callback function
myCarArray.forEach(function(item){
  console.log(item);
});
```

# Array Sort
String array can be sorted by sort()
```js
var myCarArray = ["Volvo","Merc","BMW"];
myCarArray.sort();
```

For Numeric sort, default sort method produce incorrect results because number are sorted as strings "25" is bigger than "100" because 2 is greater than "1".

It can be fixed using compare function

```js
var age = [40,100,1,5,26,10,200,300];
//Ascending Sort
age.sort(function(a,b){
  return a-b;
});
//Descending sort
age.sort(function(a,b){
  return b-a;
});
```
