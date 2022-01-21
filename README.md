# Asa
    Java Script Library
    Version: 0.4.8




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

crEl() function
---

```javascript
crEl(selector, object, callback)
```

- ```selector``` - HTML selector(string)
- ```object``` - attribute: {attribute:value}
- ```callback``` - (function)

Create element, sets attribute, and do callback with first argument as new element

**example**
```javascript

const myDiv = crEl("div", {class:"newDiv"} (el)=> {
    console.log(el) // div.newDiv
})

console.log(myDiv) // div.newDiv

```


