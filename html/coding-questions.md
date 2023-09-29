## 1. In which cases will the style for the selector be applied?

<dl>
<dd>

```css
div + p {
  color: red;
}
```

<br/>
<dd>
Option A

```
The style will be applied to <p> tag placed after <div> tag.
```

Option B

```
The style will be applied to <div> tag placed before <p> tag.
```

Option C

```
The selector is invalid.
```

Option D

```
The style will be applied to <div> tag containing <p> tag.
```

Option E

```
The style will be applied to <p> tag containing <div> tag.
```

Option F

```
The style will be applied to all <p> tags.
```

</dd>

<br/>

<details>
<summary>Answer</summary>

Option A

```
The style will be applied to <p> tag placed after <div> tag.
```

</details>

</dd>
</dl>

<br/>

<!------------------------------------------------------->

## 2. How can you make elements of a list display horizontally?

<dl>
<dd>

<dd>
Option A

```
list-type: horizontal;
```

Option B

```
Set the "float: left" property for all <li> elements
```

Option C

```
Set the height of the all <li> equal to the font size
```

Option D

```
list-style: horizontal;
```

</dd>

<br/>

<details>
<summary>Answer</summary>

Option B

```
Set the "float: left" property for all <li> elements
```

</details>

</dd>
</dl>

<br/>

<!------------------------------------------------------->

## 3. What color will be applied to the text?

<dl>
<dd>

```html
<style type="text/css">
  .text {
    color: red;
  }
  span {
    color: blue;
  }
  h1 {
    color: green;
  }
  h1 span {
    color: black;
  }
  p span {
    color: yellow;
  }
</style>

<h1>
  <p>
    <span class="text"><span>Text</span></span>
  </p>
</h1>
```

<br/>
<dd>
Option A

```
Black
```

Option B

```
Blue
```

Option C

```
Green
```

Option D

```
Yellow
```

Option E

```
Red
```

</dd>

<br/>

<details>
<summary>Answer</summary>

Option D

```
Yellow
```

According to the CSS specificity rules, inheritance has the lowest priority, so in this case styles inherited from `.text` and `.h1` will be ignored.
Then we have three selectors `span`, `h1 span` and `p span`, the first one has the lowest specificity, so it will be ignored too.
Finally we have two selectors `h1 span` and `p span`, both have the same specificity, so the last one will be applied.

</details>

</dd>
</dl>

<br/>

<!------------------------------------------------------->

## 4. A next-generation bidirectional communication technology for web applications is?

<dl>
<dd>

<br/>
<dd>
Option A

```
Persistent local storage
```

Option B

```
Server-Sent Events
```

Option C

```
Forms 2.0
```

Option D

```
WebSocket
```

</dd>

<br/>

<details>
<summary>Answer</summary>

Option D

```
WebSocket
```

</details>

</dd>
</dl>

<br/>

<!------------------------------------------------------->

## 5. ?

<dl>
<dd>

```javascript
...
```

<br/>
<dd>
Option A

```

```

Option B

```

```

Option C

```

```

Option D

```

```

</dd>

<br/>

<details>
<summary>Answer</summary>

Option ...

```
...
```

...

</details>

</dd>
</dl>

<br/>

<!------------------------------------------------------->
