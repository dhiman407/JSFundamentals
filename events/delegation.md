# Event Delegation

Event delegation allows you to avoid adding event listeners to specific nodes; instead, the event listener is added to one parent.

Example explaining how event delegation works.

```
<ul id="parent">
  <li id='child-1'>Item 1</li>
  <li id='child-2'>Item 2</li>
  <li id='child-3'>Item 3</li>
  <li id='child-4'>Item 4</li>
  <li id='child-5'>Item 5</li>
  <li id='child-6'>Item 6</li>
  <li id='child-7'>Item 7</li>
</ul>
```

Add event listener to the parent "UL" element, when the event bubbles up to the "UL" element

```js
var element  = document.querySelector('#parent');
element.addEventListener('click',function(evt){
  if(evt.target && evt.target.nodeName == "LI"){
    console.log(e.target.id);
  }
})
```
