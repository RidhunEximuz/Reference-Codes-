# Scroll To Top Button 

CSS

```css

html {
  scroll-behavior: smooth;
}

#GotoTop {
  font-family: Arial, Helvetica, sans-serif;
  font-size: 20px;
  display: none;
  position: fixed;
  bottom: 20px;
  right: 30px;
  z-index: 99;
  font-size: 18px;
  border: none;
  outline: none;
  background-color: red;
  color: white;
  cursor: pointer;
  padding: 15px;
  border-radius: 4px;
}

#GotoTop:hover {
  background-color: #555;
}

```

HTML

```html
<button onclick="topFun()" id="GotoTop" title="Go to top">Top</button>

<div style="background-color:lightgrey;padding:30px 30px 2500px">
    <p>This example demonstrates how to create a "scroll to top" button that becomes visible </p>
</div>
```


JS

```javascript

var varTop = document.getElementById("GotoTop");

// Scroll
window.onscroll = function() {
  scrollFunction()
  };

function scrollFunction() {
  if (document.body.scrollTop > 20 || document.documentElement.scrollTop > 20) {
    varTop.style.display = "block";
  } else {
    varTop.style.display = "none";
  }
}

// Click
function topFun() {
  document.body.scrollTop = 0;
  document.documentElement.scrollTop = 0;
}
  
 ```
