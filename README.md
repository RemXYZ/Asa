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

**exemple**
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

**exemple**
```javascript

const abc = getEl(".abcClass");

abc.CSSinfo().display    //block

```

<br>
<br>

css() method
---

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

sets the css style. --
With no arguments show css information,

