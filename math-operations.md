## Create a web app which would take two inputs. It would also have 4 buttons: +, -, x /. Based on the button clicked perform the operation on the two inputs.

<details> 
<summary> index.html </summary>

```
<label for="first-number"> Enter first number: </label>
<input type="number" id="first-number"></input>

<label for="second-number"> Enter second number: </label>
<input type="number" id="second-number"></input>

<div id="container-buttons">
<button id="btn-add"> + </button>
<button id="btn-subtract"> - </button>
<button id="btn-multiply"> x </button>
<button id="btn-divide"> / </button>    
</div>

<p id="display-message"></p>

<script src="app.js"></script>
```
</details>


<details>
<summary> app.js </summary> 

```
let firstNumber = document.querySelector("#first-number");
let secondNumber = document.querySelector("#second-number");
let btnAdd = document.querySelector("#btn-add");
let btnSubtract = document.querySelector("#btn-subtract");
let btnMultiply = document.querySelector("#btn-multiply");
let btnDivide = document.querySelector("#btn-divide");
let displayMessage = document.querySelector("#display-message"); 
console.log(displayMessage);

function add() { 
    console.log(firstNumber.valueAsNumber);
    console.log(secondNumber.value);
    console.log(typeof firstNumber.valueAsNumber);
    let value = firstNumber.valueAsNumber+secondNumber.valueAsNumber; 
    displayMessage.style.display="block";
    displayMessage.innerText = "The sum is:"+value; 
}

function subtract() { 
    let value = firstNumber.valueAsNumber-secondNumber.valueAsNumber; 
    displayMessage.style.display="block";
    displayMessage.innerText = "The subtraction is:"+value;
    
}

function multiply(numberOne,numberTwo) { 
    let value = firstNumber.valueAsNumber*secondNumber.valueAsNumber;
    displayMessage.style.display="block";
    displayMessage.innerText = "The multiplication is:"+value;
}

function divide(numberOne,numberTwo) { 
    let value = firstNumber.valueAsNumber/secondNumber.valueAsNumber;
    displayMessage.style.display="block";
    displayMessage.innerText = "The division is:"+value; 
   
}
btnAdd.addEventListener("click",add);
btnSubtract.addEventListener("click",subtract);
btnMultiply.addEventListener("click",multiply);
btnDivide.addEventListener("click",divide);
```
