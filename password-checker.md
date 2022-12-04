## Create a password checker web app. If password is lesser than 10 characters then show an error to user otherwise show success. Someone can ask to make the submit button disabled. Some can ask to make the input field green or red depending on input.
<details> 
  <summary> index.html </summary>
  
```
<body>
    <label for="password-input"> Enter your password: </label>
    <input id="password-input" type="text" name="name"> </input> 
    <button id="btn-submit"> Submit </button>
    <p id="output-message"> </p> 
    <script src="app.js"></script>
</body>
```
</details> 

<details>
<summary> app.js </summary> 

```
let passwordInput = document.querySelector("#password-input"); 
let btnSubmit = document.querySelector("#btn-submit");
let outputMessage = document.querySelector("#output-message"); 

function passwordChecker() {
    if((passwordInput.value).length<10) {
    outputMessage.textContent = "Enter atleast 10 characters to submit password.";
    passwordInput.style.backgroundColor = "red";
    passwordInput.style.color = "white";
    }
    else 
    {    
        outputMessage.textContent =  "Great password created";
        passwordInput.style.backgroundColor = "green";
        passwordInput.style.color = "white";
        btnSubmit.style.display = "none";
    }

}

btnSubmit.addEventListener("click",passwordChecker); 
```
</details> 
