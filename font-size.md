## Create a web app where I can input a text. Now create two buttons + and -. On clicking + increase the fontSize by 2px and vice versa.

<details> 
<summary> index.html </summary>
  
```
<label for="font-size"> Enter text </label>
<input type="text" id="font-size" placeholder="enter text here now"> </input>

<div id="btn-container">
<button id="btn-add"> + </button>
<button id="btn-minus"> - </button>
</div>
    
<script src="app.js"></script>
```
</details> 

<details>
<summary> app.js </summary> 

```
btnAdd = document.querySelector("#btn-add");
btnMinus = document.querySelector("#btn-minus"); 
inputFontSize = document.querySelector("#font-size");

function add() {
let newStyle = parseInt(window.getComputedStyle(inputFontSize).getPropertyValue("font-size").slice(0,-2)) + 2; 
inputFontSize.style.fontSize = newStyle+"px";  
}

function subtract() { 
let newStyle = parseInt(window.getComputedStyle(inputFontSize).getPropertyValue("font-size").slice(0,-2)) - 2; 
inputFontSize.style.fontSize = newStyle+"px"; 
}

btnAdd.addEventListener("click",add);
btnMinus.addEventListener("click",subtract); 
```
