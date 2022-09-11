# Random password generator (pure js)

## Password generation created in pure javascript, the ability to configure the generation is implemented. 
![preview-1](https://i.ibb.co/LpHmpWD/1.png)
### The algorithm that generates the password is as follows (the choice of characteristics is built into this part of the code)
```
function generatePassword(passwordLength) {
    const numberChars = "0123456789";
    const upperChars = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
    const lowerChars = "abcdefghijklmnopqrstuvwxyz";
    const symbolChars = "!@#$%^&*()_+";

    let allChars = '';

    if (document.getElementById('one').checked) {
        allChars += numberChars;
    }

    if (document.getElementById('two').checked) {
        allChars += upperChars;
    }

    if (document.getElementById('three').checked) {
        allChars += lowerChars;
    }

    if (document.getElementById('four').checked) {
        allChars += symbolChars;
    }

    let randomString = '';

    for (let i = 0; i < passwordLength; i++) {
        let randomNumber = Math.floor(Math.random() * allChars.length);
        randomString += allChars[randomNumber];
    }
    return randomString;
}
```
___
### Password generation created in pure javascript, the ability to configure the generation is implemented.
![preview-2](https://i.ibb.co/J2GJsLt/2.png)
### Selection is activated with custom checkboxes made in pure css.
```
input[type="checkbox"] {
    width: 40px;
    height: 20px;
    -webkit-appearance: none;
    outline: none;
    background: #c6c6c6;
    border-radius: 20px;
    transition: .5s;
    box-shadow: inset 0 0 5px rgba(0,0,0,.2);
}

input:checked[type="checkbox"] {
    background: #2C5364
}

input[type="checkbox"]:before {
    content: '';
    position: absolute;
    width: 20px;
    height: 20px;
    border-radius: 20px;
    top: 0;
    left: 0;
    background: #fff;
    transition: .5s;
    transform: scale(1.1);
    box-shadow: 0 2px 5px rgba(0,0,0,.2);
}

input:checked[type="checkbox"]:before {
    left: 20px;
}
```
___
### Styles used for button css.
```
.password-button {
    font-size: 20px;
    background: linear-gradient(to left, #0F2027, #203A43, #2C5364);
    text-decoration: none;
    padding: 8px 40px;
    margin: 5px;
    border-radius: 17px;
    border: none;
    background-size: 200%;
    transition: .5s;
    font-family: 'Raleway', sans-serif;
}

.password-button:hover {
    background-position: right;
}
```
#### Gradients used for button design css - [available here](https://uigradients.com/#MoonlitAsteroid)
