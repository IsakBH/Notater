```js
const prompt = require("prompt-sync")(); // fakk node.js bro hvorfor FAEN er ikke "prompt" en innebygd funksjon? hva for noe homse greier er det for noe?
let tall1 = parseFloat(prompt("Skriv inn tall 1: "));
let operatør = prompt("Skriv inn operatøren du vil bruke (+, -, *, /, %): ");
let tall2 = parseFloat(prompt("Skriv inn tall 2: "));
let sum = null;

switch(operatør){
    case "+": // pluss
        sum = tall1 + tall2;
        console.log(sum);
        break;
    case "-": // minus
        sum = tall1 - tall2;
        console.log(sum);
        break;
    case "*": // ganging
        sum = tall1 * tall2;
        console.log(sum);
        break;
    case "/": // deling
        if(tall2 === 0){
            sum = "ERROR! Du kan ikke dele på null.";
            console.log(sum);
        }
        else{
            sum = tall1 / tall2;
            console.log(sum);
        }
        break;
    case "%":
        sum = tall1 % tall2;
        console.log(sum);
        break;
    default:
        console.log("Ja, det er meningen du skal bruke en av operatørene som står i parantes i prompten da, din apekatt.")
        break;
}

```
