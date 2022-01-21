# Asa
    Java Script Library
    Version: 0.4.8
    Experimental version !
    The library was made for the purpose of studying the work of javascript, and its work is similar to the [jQuery](https://jquery.com/) library
    Methods are added to the prototype of the element, so the library may not be stable in the future




## Documentation mini
<br>
<br>
<br>

getEl() function
---

```javascript
getEl(selectors)
``` 
Returns element or elements (if there are many).

---
**NOTE**

Once you use this command, new asaJS methods will be added to all these elements!

---

**example**
```html
<div class="abcClass">Hello</div>
<div id="abcId">Hi</div>
```
```javascript
getEl(".abcClass") // <div class="abcClass">Hello</div>
getEl("#abcId") // <div id="abcId">Hi</div>
getEl("div") // NodeList(2) [div.abcClass, div#abcId]
```

<br>
<br>

CSSinfo() method
---

```js

element.CSSinfo()

```
Shows elements css information

**example**
```javascript

const abc = getEl(".abcClass");

abc.CSSinfo().display    //block

```

<br>
<br>

css() method
---

Sets the css style. <br>
With no arguments show css information.

**example**
```js
//1.
element.css(property,value);
//2.
element.css({
    property:value,
    property:value,
    ...
})
//3.
element.css() // show css info
```

<br>
<br>


crEl() function / method
---



```javascript
crEl(selector, attribute, callback);
element.crEl(selector, attribute, callback)
```




- ```selector``` - HTML selector(string)
- ```attribute``` - {attribute:value, ...} or set class or id(value)
- ```callback``` - (function)

Create element, sets attribute, and executes a callback with the first argument, which is just the newly created element.
<br>
It can also be used as a method to add a new element to an already created element.

---
**NOTE**

Once you use this command, new asaJS methods will be added to all these elements!

---


**example**
```javascript
//1.
const myDiv = crEl("div", {class:"newDiv"} (el)=> {
    console.log(el) // div.newDiv
})
console.log(myDiv) // div.newDiv

//2.
const myDiv2 = crEl("div", ".abcClass")
console.log(myDiv2) // div.abcClass

//3.
const myDiv3 = crEl("div", "#abcId")
console.log(myDiv3) // div#abcId

//4.
const abcEl = getEl(".abc");
abcEl.crEl("div", ".abcClass");

console.log(abcEl.children)    //HTMLCollection [div.abcClass]


```


