# Bubbling
When an event happens on element, it first runs the handlers on it, then on its parent, then all the way up till reaches root element.

Suppose, we have 3 nested elements FORM >  DIV > P with a handler on each of them.
```
<form onclick="alert('form element !')">
  <div onclick="alert('div element !')">
    <p onclick="alert('p element !')">

    </p>
  </div>
</form>
```
A click on the inner "p" first runs onclick:

1) on that "p" element
2) Then on the outer "div"
3) Then on the outer "form"
4) So on upwards till the document object.

# event.target

* event.target is the target element that initiated the event.
* this -  is the current element who is running the event handler on it.

# Stop Bubbling

A Bubbling event starts from the target element and goes upwards till <html>, and then to document object. But sometime handler may decide that event has been fully processed and stop the bubbling. The method for stop it event.stopPropagation();

```js
event.stopPropagation();
```
