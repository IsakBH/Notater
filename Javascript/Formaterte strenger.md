Når du skal skrive formaterte strenger (strenger med variabler inni dem), må du bruke ``` `blah blah` ``` isteden for ``` "blah blah" ```

##### Hvorfor?
Ingen anelse.

### Eksempel
```js
function kalkulator(tall1, tall2){
    const prompt = require("prompt-sync")();
    let sum;
    let operatør = prompt("Deling (/) eller ganging (*)? ");

    if(operatør == "/"){
        sum = tall1 / tall2;
    }
    else if(operatør == "*"){
        sum = tall1 * tall2;
    }
    else{
        console.log("ja ok bro velg en god operatør da din jævla imbisil");
    }
```
==console.log(`${tall1} ${operatør} ${tall2} = ${sum}`);==  
```js
}


kalkulator(20, 2); // caller kalkulator med argumentene 20 og 2
```
