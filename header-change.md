## Create a web app where I can input a text. Now, create three buttons h1, h2, h3. When I click on any of the button, the text should become h1, h2, or h3.

## Create a web app where I can input a text. Now, create three buttons: red, green, blue. Clicking on the button should change the text color.

<details> 
<summary> index.html </summary>
  
```
 <input type="text" id="input-value" placeholder="enter text here now."> </input>

    <div>
    <button id="btn-h1"> h1 </button>
    <button id="btn-h2"> h2 </button>
    <button id="btn-h3"> h3 </button>
    <button id="btn-reset"> reset </button>
    </div> 

    <div>
        <button id="btn-red"> red </button>
        <button id="btn-blue"> blue </button>
        <button id="btn-green"> green </button>
        <button id="btn-reset2"> reset </button>
        </div> 

    <p id="output-value"> </p>
    <script src="app.js"></script>
  ```
</details>

<details>
<summary> app.js </summary> 

```
let btnHeaderOne = document.querySelector("#btn-h1"); 
let btnHeaderTwo = document.querySelector("#btn-h2");
let btnHeaderThree = document.querySelector("#btn-h3");
let inputValue = document.querySelector("#input-value"); 
let outputValue = document.querySelector("#output-value"); 
let btnReset = document.querySelector("#btn-reset");
let btnReset2 = document.querySelector("#btn-reset2");

let btnRed = document.querySelector("#btn-red");
let btnBlue = document.querySelector("#btn-blue");
let btnGreen = document.querySelector("#btn-green");

function headerOne() { 
inputValue.style.fontSize = "2em";
}

function colorRed() { 
    console.log("red");
    inputValue.style.color = "red";
}

function colorGreen() { 
    inputValue.style.color = "green";
}

function colorBlue() { 
    inputValue.style.color = "blue";
}

function headerTwo() { 
    inputValue.style.fontSize = "1.5em";
 
}

function headerThree() { 
    inputValue.style.fontSize = "1.3em";
}

function reset() { 
    inputValue.style.fontSize = "1em";
    inputValue.style.color = "black"; 
}

btnHeaderOne.addEventListener("click",headerOne);
btnHeaderTwo.addEventListener("click",headerTwo);
btnHeaderThree.addEventListener("click",headerThree); 
btnReset.addEventListener("click",reset); 
btnRed.addEventListener("click",colorRed);
btnBlue.addEventListener("click",colorBlue);
btnGreen.addEventListener("click",colorGreen);
btnReset2.addEventListener("click",reset); 

```
    
