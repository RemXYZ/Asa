# Asa
    Java Script Library
    Version: 0.4.8




### Documentation mini

```javascript
getEl(selectors)
``` 
Returns element or elements (if there are many).
**NOTE**

Once you use this command, new methods will be added to all these elements!

---

**exemple**
```html
<div class="abcClass">Hello</div>
<div id="abcId">Hi</div>
```
```javascript
getEl("#abcId") // <div id="abcId">Hi</div>
getEl(".abcClass") // <div class="abcClass">Hello</div>
```
 

